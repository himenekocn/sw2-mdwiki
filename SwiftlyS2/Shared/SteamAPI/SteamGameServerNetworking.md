<a id="steamgameservernetworking"></a>

# 📦 SteamGameServerNetworking

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### SendP2PPacket (静态)

```csharp
bool SendP2PPacket(CSteamID steamIDRemote, byte[] pubData, uint cubData, EP2PSend eP2PSendType, int nChannel = 0)
```

<para> </para> <para> UDP风格（无连接）网络接口。这些函数使用基于目标组织的API发送消息。</para> <para> 支持可靠和不可靠消息。</para> <para> 如需更多TCP风格接口（即拥有连接句柄），请参见下方函数。</para> <para> 两种接口风格均可发送可靠和不可靠消息。</para> <para> 自动建立NAT穿透或中继服务器连接</para> <para> 这些API已弃用，可能在Steamworks SDK未来版本中移除。</para> <para> 参见ISteamNetworkingMessages。</para> <para> 向指定用户发送P2P数据包</para> <para> 类似UDP协议，不可靠且最大数据包大小为1200字节</para> <para> 首个数据包可能因NAT穿透代码运行而延迟发送</para> <para> 若无法到达目标用户，将通过回调P2PSessionConnectFail_t返回错误</para> <para> 不同数据包发送方式的描述参见上方EP2PSend枚举</para> <para> nChannel是路由编号，可用于将消息路由至不同系统——您需要调用ReadP2PPacket()</para> <para> 并传入相同通道编号才能在另一端检索数据</para> <para> 使用不同通道与同一用户通信仍将复用底层p2p连接，以节省资源</para>

**参数:**

- `steamIDRemote` (`CSteamID`)
- `pubData` (`byte[]`)
- `cubData` (`uint`)
- `eP2PSendType` (`EP2PSend`)
- `nChannel` (`int`) = `0`

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworking.SendP2PPacket(remoteSteamID, dataBuffer, (uint)dataBuffer.Length, EP2PSend.k_EP2PSendUnreliable, 0);
```

### IsP2PPacketAvailable (静态)

```csharp
bool IsP2PPacketAvailable(out uint pcubMsgSize, int nChannel = 0)
```

<para> 如果有任何数据可供读取，则返回 true，同时返回需要读取的数据量</para>

**参数:**

- `pcubMsgSize` (`out uint`)
- `nChannel` (`int`) = `0`

**返回值:** `bool`

**用法示例:**
```csharp
bool available = SteamGameServerNetworking.IsP2PPacketAvailable(out uint size, 0);
```

### ReadP2PPacket (静态)

```csharp
bool ReadP2PPacket(byte[] pubDest, uint cubDest, out uint pcubMsgSize, out CSteamID psteamIDRemote, int nChannel = 0)
```

<para>读取通过 SendP2PPacket() 从其他用户发送的数据包</para>  
<para>在最后两个参数中返回消息大小以及发送该消息的用户的SteamID</para>  
<para>如果传入的缓冲区太小，消息将被截断</para>  
<para>此调用不会阻塞，如果没有可用数据则返回 false</para>

**参数:**

- `pubDest` (`byte[]`)
- `cubDest` (`uint`)
- `pcubMsgSize` (`out uint`)
- `psteamIDRemote` (`out CSteamID`)
- `nChannel` (`int`) = `0`

**返回值:** `bool`

**用法示例:**
```csharp
byte[] buffer = new byte[1024];
bool hasData = SteamGameServerNetworking.ReadP2PPacket(buffer, (uint)buffer.Length, out uint msgSize, out CSteamID remoteId, 0);
```

### AcceptP2PSessionWithUser (静态)

```csharp
bool AcceptP2PSessionWithUser(CSteamID steamIDRemote)
```

<para> AcceptP2PSessionWithUser() 仅应在响应 P2PSessionRequest_t 回调时调用</para> <para> 当其他用户试图向您发送尚未建立通信的数据包时，将发布 P2PSessionRequest_t</para> <para> 如果您不想与该用户通信，只需忽略该请求</para> <para> 如果该用户持续向您发送数据包，系统将定期重新发布 P2PSessionRequest_t</para> <para> 同一用户可能多次触发此调用</para> <para> （如果您已对另一用户调用了 SendP2PPacket()，则隐式接受该会话请求）</para>

**参数:**

- `steamIDRemote` (`CSteamID`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworking.AcceptP2PSessionWithUser(steamIDRemote);
```

### CloseP2PSessionWithUser (静态)

```csharp
bool CloseP2PSessionWithUser(CSteamID steamIDRemote)
```

<para> 当您结束与用户的通信时，调用 CloseP2PSessionWithUser() 将释放底层资源</para> <para> 如果远程用户再次尝试向您发送数据，将发布另一个 P2PSessionRequest_t 回调</para>

**参数:**

- `steamIDRemote` (`CSteamID`)

**返回值:** `bool`

**用法示例:**
```csharp
CSteamID remoteUser = new CSteamID(76561198000000000);
SteamGameServerNetworking.CloseP2PSessionWithUser(remoteUser);
```

### CloseP2PChannelWithUser (静态)

```csharp
bool CloseP2PChannelWithUser(CSteamID steamIDRemote, int nChannel)
```

<para>在与特定频道上的用户通信完毕后，调用 CloseP2PChannelWithUser()。一旦某个用户的所有</para> <para>开放频道均已关闭，与该用户的开放会话将被关闭，来自该用户的新数据将触发</para> <para>P2PSessionRequest_t 回调</para>

**参数:**

- `steamIDRemote` (`CSteamID`)
- `nChannel` (`int`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworking.CloseP2PChannelWithUser(steamIDRemote, 0);
```

### GetP2PSessionState (静态)

```csharp
bool GetP2PSessionState(CSteamID steamIDRemote, out P2PSessionState_t pConnectionState)
```

<para> 使用与用户底层连接的详细信息填充P2PSessionState_t结构体</para> <para> 仅应在调试目的时使用</para> <para> 如果与指定用户不存在连接，则返回false</para>

**参数:**

- `steamIDRemote` (`CSteamID`)
- `pConnectionState` (`out P2PSessionState_t`)

**返回值:** `bool`

**用法示例:**
```csharp
P2PSessionState_t state;
bool connected = SteamGameServerNetworking.GetP2PSessionState(steamIDRemote, out state);
```

### AllowP2PPacketRelay (静态)

```csharp
bool AllowP2PPacketRelay(bool bAllow)
```

<para> 允许P2P连接在无法建立直连或NAT穿透时，通过Steam服务器中继回退。</para>
<para> 仅适用于设置此值后建立的连接，或此值设置后需要自动重连的现有连接。</para>
<para> P2P数据包中继默认为允许。</para>
<para> 注意：此函数已弃用，可能在SDK未来版本中移除。出于安全目的，即使向此函数传递false，我们仍可能决定向特定对等节点中继流量，以防止向其他对等节点泄露客户端IP地址。</para>

**参数:**

- `bAllow` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworking.AllowP2PPacketRelay(true);
```

### CreateListenSocket (静态)

```csharp
SNetListenSocket_t CreateListenSocket(int nVirtualP2PPort, SteamIPAddress_t nIP, ushort nPort, bool bAllowUseOfPacketRelay)
```

<para> </para> <para> LISTEN / CONNECT 面向连接接口函数</para>  
<para> 这些函数更类似于客户端-服务器TCP API。一方作为"服务器"</para>  
<para> 并"监听"传入的连接，随后必须"接受"这些连接。"客户端"</para>  
<para> 通过"连接"发起连接。发送与接收通过连接句柄完成。</para>  
<para> 若需更接近UDP风格的接口（无需跟踪连接句柄，仅需向SteamID发送消息），</para>  
<para> 请使用上述UDP风格函数。</para>  
<para> 两种方法均可发送可靠与不可靠消息。</para>  
<para> 此API已弃用，可能在Steamworks SDK未来版本中移除。</para>  
<para> 请参考ISteamNetworkingSockets。</para>  
<para> </para>  
<para> 创建套接字并监听其他客户端连接</para>  
<para> 当其他客户端连接时，将触发SocketStatusCallback_t回调</para>  
<para> nVirtualP2PPort是客户端连接的唯一标识符，适用于多端口场景</para>  
<para> 除非需要多组连接，否则通常设为0即可</para>  
<para> unIP为绑定的本地IP地址</para>  
<para> 若仅需默认本地IP，传入0</para>  
<para> unPort为使用的端口</para>  
<para> 若不允许用户通过IP/端口连接，仅期望纯点对点连接，则传入0</para>

**参数:**

- `nVirtualP2PPort` (`int`)
- `nIP` (`SteamIPAddress_t`)
- `nPort` (`ushort`)
- `bAllowUseOfPacketRelay` (`bool`)

**返回值:** `SNetListenSocket_t`

**用法示例:**
```csharp
var socket = SteamGameServerNetworking.CreateListenSocket(0, default, 27015, true);
```

### CreateP2PConnectionSocket (静态)

```csharp
SNetSocket_t CreateP2PConnectionSocket(CSteamID steamIDTarget, int nVirtualPort, int nTimeoutSec, bool bAllowUseOfPacketRelay)
```

<para> 创建套接字并开始连接到远程目标</para>
<para> 可通过已知的SteamID（客户端或游戏服务器）或直接通过IP进行连接</para>
<para> 成功时将触发SocketStatusCallback_t回调</para>
<para> 失败或超时时将触发SocketStatusCallback_t回调，并在m_eSNetSocketState中包含失败代码</para>

**参数:**

- `steamIDTarget` (`CSteamID`)
- `nVirtualPort` (`int`)
- `nTimeoutSec` (`int`)
- `bAllowUseOfPacketRelay` (`bool`)

**返回值:** `SNetSocket_t`

**用法示例:**
```csharp
var socket = SteamGameServerNetworking.CreateP2PConnectionSocket(targetSteamID, 0, 30, true);
```

### CreateConnectionSocket (静态)

```csharp
SNetSocket_t CreateConnectionSocket(SteamIPAddress_t nIP, ushort nPort, int nTimeoutSec)
```

**参数:**

- `nIP` (`SteamIPAddress_t`)
- `nPort` (`ushort`)
- `nTimeoutSec` (`int`)

**返回值:** `SNetSocket_t`

**用法示例:**
```csharp
var socket = SteamGameServerNetworking.CreateConnectionSocket(new SteamIPAddress_t(), 27015, 30);
```

### DestroySocket (静态)

```csharp
bool DestroySocket(SNetSocket_t hSocket, bool bNotifyRemoteEnd)
```

<para> 断开与套接字的连接（如有），并使句柄失效</para>
<para> 套接字上任何未读取的数据将被丢弃</para>
<para> 如果设置了bNotifyRemoteEnd，套接字在远程端确认断开连接之前不会完全销毁</para>

**参数:**

- `hSocket` (`SNetSocket_t`)
- `bNotifyRemoteEnd` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworking.DestroySocket(socketHandle, true);
```

### DestroyListenSocket (静态)

```csharp
bool DestroyListenSocket(SNetListenSocket_t hSocket, bool bNotifyRemoteEnd)
```

<para>销毁监听套接字将自动终止由其所生成的所有常规套接字</para>

**参数:**

- `hSocket` (`SNetListenSocket_t`)
- `bNotifyRemoteEnd` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworking.DestroyListenSocket(listenSocket, true);
```

### SendDataOnSocket (静态)

```csharp
bool SendDataOnSocket(SNetSocket_t hSocket, byte[] pubData, uint cubData, bool bReliable)
```

<para> 发送数据</para> <para> 必须是一个已连接套接字的句柄</para> <para> 数据全部通过UDP发送，因此发送大小限制为1200字节；超过此限制后，许多路由器将开始丢弃数据包</para> <para> 谨慎使用可靠标志；尽管重发速率相当激进，</para> <para> 它仍可能导致接收数据时出现停滞（类似TCP）</para>

**参数:**

- `hSocket` (`SNetSocket_t`)
- `pubData` (`byte[]`)
- `cubData` (`uint`)
- `bReliable` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
byte[] data = new byte[100];
SteamGameServerNetworking.SendDataOnSocket(socketHandle, data, (uint)data.Length, true);
```

### IsDataAvailableOnSocket (静态)

```csharp
bool IsDataAvailableOnSocket(SNetSocket_t hSocket, out uint pcubMsgSize)
```

<para>接收数据</para>
<para>若无剩余数据则返回false</para>
<para>以字节为单位将下一条消息的大小填充至*pcubMsgSize</para>

**参数:**

- `hSocket` (`SNetSocket_t`)
- `pcubMsgSize` (`out uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint msgSize;
bool hasData = SteamGameServerNetworking.IsDataAvailableOnSocket(socket, out msgSize);
```

### RetrieveDataFromSocket (静态)

```csharp
bool RetrieveDataFromSocket(SNetSocket_t hSocket, byte[] pubDest, uint cubDest, out uint pcubMsgSize)
```

/// <summary>
/// 将消息内容填入pubDest。
/// </summary>
/// <remarks>
/// 消息始终完整，大小与发送时一致（即采用分包方式，非流式传输）。
/// 若*pcubMsgSize小于cubDest，则仅写入部分数据。
/// 若无可用数据则返回false。
/// </remarks>

**参数:**

- `hSocket` (`SNetSocket_t`)
- `pubDest` (`byte[]`)
- `cubDest` (`uint`)
- `pcubMsgSize` (`out uint`)

**返回值:** `bool`

**用法示例:**
```csharp
byte[] buffer = new byte[1024];
bool hasData = SteamGameServerNetworking.RetrieveDataFromSocket(socketHandle, buffer, 1024, out uint msgSize);
```

### IsDataAvailable (静态)

```csharp
bool IsDataAvailable(SNetListenSocket_t hListenSocket, out uint pcubMsgSize, out SNetSocket_t phSocket)
```

<para> 检查与此监听套接字建立连接的任何套接字的数据</para>
<para> 如果没有剩余数据则返回false</para>
<para> 用下一条消息的大小（以字节为单位）填充 *pcubMsgSize</para>
<para> 用可用数据的套接字填充 *phSocket</para>

**参数:**

- `hListenSocket` (`SNetListenSocket_t`)
- `pcubMsgSize` (`out uint`)
- `phSocket` (`out SNetSocket_t`)

**返回值:** `bool`

**用法示例:**
```csharp
bool hasData = SteamGameServerNetworking.IsDataAvailable(hListenSocket, out uint msgSize, out SNetSocket_t socket);
```

### RetrieveData (静态)

```csharp
bool RetrieveData(SNetListenSocket_t hListenSocket, byte[] pubDest, uint cubDest, out uint pcubMsgSize, out SNetSocket_t phSocket)
```

<para> 从通过此监听套接字建立的任何已连接套接字中检索数据</para>  
<para> 用消息内容填充 pubDest</para>  
<para> 消息始终完整，大小与发送时一致（即基于数据包，非流式）</para>  
<para> 如果 *pcubMsgSize &lt; cubDest，则仅写入部分数据</para>  
<para> 若无可用数据则返回 false</para>  
<para> 通过 *phSocket 填充有可用数据的套接字</para>

**参数:**

- `hListenSocket` (`SNetListenSocket_t`)
- `pubDest` (`byte[]`)
- `cubDest` (`uint`)
- `pcubMsgSize` (`out uint`)
- `phSocket` (`out SNetSocket_t`)

**返回值:** `bool`

**用法示例:**
```csharp
byte[] buffer = new byte[1024];
bool hasData = SteamGameServerNetworking.RetrieveData(listenSocket, buffer, 1024, out uint msgSize, out SNetSocket_t socket);
```

### GetSocketInfo (静态)

```csharp
bool GetSocketInfo(SNetSocket_t hSocket, out CSteamID pSteamIDRemote, out int peSocketStatus, out SteamIPAddress_t punIPRemote, out ushort punPortRemote)
```

<para> 返回指定套接字的信息，填充指针的内容</para>

**参数:**

- `hSocket` (`SNetSocket_t`)
- `pSteamIDRemote` (`out CSteamID`)
- `peSocketStatus` (`out int`)
- `punIPRemote` (`out SteamIPAddress_t`)
- `punPortRemote` (`out ushort`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworking.GetSocketInfo(socket, out var remoteId, out var status, out var remoteIp, out var remotePort);
```

### GetListenSocketInfo (静态)

```csharp
bool GetListenSocketInfo(SNetListenSocket_t hListenSocket, out SteamIPAddress_t pnIP, out ushort pnPort)
```

<para> 返回监听套接字所绑定的本地端口</para> <para> 如果套接字设置为仅监听P2P连接，则*pnIP和*pnPort将为0</para>

**参数:**

- `hListenSocket` (`SNetListenSocket_t`)
- `pnIP` (`out SteamIPAddress_t`)
- `pnPort` (`out ushort`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerNetworking.GetListenSocketInfo(listenSocket, out SteamIPAddress_t ip, out ushort port);
```

### GetSocketConnectionType (静态)

```csharp
ESNetSocketConnectionType GetSocketConnectionType(SNetSocket_t hSocket)
```

<para>返回真值以描述套接字最终如何完成连接</para>

**参数:**

- `hSocket` (`SNetSocket_t`)

**返回值:** `ESNetSocketConnectionType`

**用法示例:**
```csharp
var connectionType = SteamGameServerNetworking.GetSocketConnectionType(socketHandle);
```

### GetMaxPacketSize (静态)

```csharp
int GetMaxPacketSize(SNetSocket_t hSocket)
```

<para>最大数据包大小，以字节为单位</para>

**参数:**

- `hSocket` (`SNetSocket_t`)

**返回值:** `int`

**用法示例:**
```csharp
SNetSocket_t socket = default;
int maxSize = SteamGameServerNetworking.GetMaxPacketSize(socket);
```

