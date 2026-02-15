# 📦 SteamGameServerNetworking

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### SendP2PPacket (静态)

```csharp
bool SendP2PPacket(CSteamID steamIDRemote, byte[] pubData, uint cubData, EP2PSend eP2PSendType, int nChannel = 0)
```

<para> </para> <para> UDP风格（无连接）的网络接口。这些函数使用以目标为中心的API来发送消息。支持可靠和不可靠消息。</para> <para> 如需更TCP风格的接口（意味着您拥有一个连接句柄），请参见下方的函数。</para> <para> 两种接口风格都可以发送可靠和不可靠消息。</para> <para> 自动建立NAT穿透或中继服务器连接</para> <para> 这些API已被弃用，并可能在未来的Steamworks SDK版本中被移除。</para> <para> 请参见ISteamNetworkingMessages。</para> <para> 向指定用户发送P2P数据包</para> <para> 类似UDP，不可靠，最大数据包大小为1200字节</para> <para> 首次发送数据包时可能会延迟，因为NAT穿透代码正在运行</para> <para> 如果无法与用户建立连接，将通过回调P2PSessionConnectFail_t报告错误</para> <para> 有关不同发送数据包方式的描述，请参见上方的EP2PSend枚举</para> <para> nChannel是一个路由编号，可用于帮助将消息路由到不同的系统 - 您必须在另一端使用相同的通道编号调用ReadP2PPacket()才能检索数据</para> <para> 使用不同的通道与同一用户通信仍将使用相同的底层p2p连接，从而节省资源</para>

**参数:**

- `steamIDRemote` (`CSteamID`)
- `pubData` (`byte[]`)
- `cubData` (`uint`)
- `eP2PSendType` (`EP2PSend`)
- `nChannel` (`int`) = `0`

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworking.SendP2PPacket(targetSteamID, dataBuffer, (uint)dataBuffer.Length, EP2PSend.k_EP2PSendUnreliable, 0);
```

### IsP2PPacketAvailable (静态)

```csharp
bool IsP2PPacketAvailable(out uint pcubMsgSize, int nChannel = 0)
```

<para>如果存在可供读取的数据，则返回 true，并返回需要读取的数据量</para>

**参数:**

- `pcubMsgSize` (`out uint`)
- `nChannel` (`int`) = `0`

**返回值:** `bool`

**用法示例:**
```csharp
uint packetSize;
bool hasPacket = SteamGameServerNetworking.IsP2PPacketAvailable(out packetSize, 0);
if (hasPacket) { /* 处理数据包 */ }
```

### ReadP2PPacket (静态)

```csharp
bool ReadP2PPacket(byte[] pubDest, uint cubDest, out uint pcubMsgSize, out CSteamID psteamIDRemote, int nChannel = 0)
```

<para>读取通过 SendP2PPacket() 从其他用户发送过来的数据包</para> <para>通过最后两个参数返回消息的大小以及发送该消息的用户 SteamID</para> <para>如果传入的缓冲区过小，消息将被截断</para> <para>此调用是非阻塞的，如果没有可用数据，将返回 false</para>

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
SteamGameServerNetworking.ReadP2PPacket(buffer, (uint)buffer.Length, out uint msgSize, out CSteamID remoteId, 0);
```

### AcceptP2PSessionWithUser (静态)

```csharp
bool AcceptP2PSessionWithUser(CSteamID steamIDRemote)
```

<para> AcceptP2PSessionWithUser() 仅应在响应 P2PSessionRequest_t 回调时调用</para> <para> 如果其他用户尝试向您发送您尚未交谈过的数据包，则会发布 P2PSessionRequest_t</para> <para> 如果您不想与该用户交谈，只需忽略此请求即可</para> <para> 如果该用户继续向您发送数据包，则会定期发布另一个 P2PSessionRequest_t</para> <para> 对于单个用户，此函数可能会被多次调用</para> <para> （如果您已对其他用户调用了 SendP2PPacket()，则这会隐式接受会话请求）</para>

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

<para> 当您与用户通话结束后，请调用 CloseP2PSessionWithUser()，它将在底层释放资源。</para> <para> 如果远程用户再次尝试向您发送数据，将再次发布一个 P2PSessionRequest_t 回调。</para>

**参数:**

- `steamIDRemote` (`CSteamID`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworking.CloseP2PSessionWithUser(steamIDRemote);
```

### CloseP2PChannelWithUser (静态)

```csharp
bool CloseP2PChannelWithUser(CSteamID steamIDRemote, int nChannel)
```

<para> 当您完成与特定通道上用户的对话后，请调用 CloseP2PChannelWithUser()。一旦与该用户的所有已打开通道均被关闭，与该用户的会话也将被关闭，此后来自该用户的新数据将触发 P2PSessionRequest_t 回调。</para> <para> </para> <para> </para>

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

<para> 用有关与用户底层连接的详细信息填充 P2PSessionState_t 结构</para> <para> 仅用于调试目的</para> <para> 如果与指定用户不存在连接，则返回 false</para>

**参数:**

- `steamIDRemote` (`CSteamID`)
- `pConnectionState` (`out P2PSessionState_t`)

**返回值:** `bool`

**用法示例:**
```csharp
CSteamID remoteID = new CSteamID(123456);
P2PSessionState_t state;
bool result = SteamGameServerNetworking.GetP2PSessionState(remoteID, out state);
```

### AllowP2PPacketRelay (静态)

```csharp
bool AllowP2PPacketRelay(bool bAllow)
```

<para> 允许点对点 (P2P) 连接在无法建立直接连接或进行网络地址转换 (NAT) 穿透时，回退到通过 Steam 服务器中继。此设置仅适用于在设置此值后创建的连接，或需要在此值设置后自动重新连接的现有连接。</para> <para> 点对点 (P2P) 数据包中继默认是允许的。</para> <para> 注意：此函数已被弃用，并可能在 SDK 的未来版本中被移除。出于安全目的，即使您将此函数的参数设置为 false，我们可能仍会决定将流量中继到某些对等方，以防止向其他对等方泄露客户端的 IP 地址。</para>

**参数:**

- `bAllow` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworking.AllowP2PPacketRelay(false);
```

### CreateListenSocket (静态)

```csharp
SNetListenSocket_t CreateListenSocket(int nVirtualP2PPort, SteamIPAddress_t nIP, ushort nPort, bool bAllowUseOfPacketRelay)
```

<para> </para> <para> LISTEN / CONNECT 面向连接的接口函数</para> <para> 这些函数更类似于客户端-服务器 TCP API。一方是“服务器”，</para> <para> 并“监听”传入的连接，然后必须“接受”这些连接。“客户端”</para> <para> 通过“连接”来发起连接。发送和接收通过一个</para> <para> 连接句柄完成。</para> <para> 对于更接近 UDP 风格的接口，即不跟踪连接句柄，而是</para> <para> 直接向 SteamID 发送消息，请使用上面的 UDP 风格函数。</para> <para> 两种方法都可以发送可靠和不可靠的消息。</para> <para> 这些 API 已被弃用，并可能在未来的 Steamworks</para> <para> SDK 版本中被移除。请参阅 ISteamNetworkingSockets。</para> <para> </para> <para> 创建一个套接字并监听其他连接</para> <para> 当其他客户端连接时会触发 SocketStatusCallback_t 回调</para> <para> nVirtualP2PPort 是客户端将连接到的唯一 ID，如果您有多个端口</para> <para> 通常可以将其设为 0，除非您需要多组连接</para> <para> unIP 是要绑定的本地 IP 地址</para> <para> 如果您只需要默认的本地 IP，请传入 0</para> <para> unPort 是要使用的端口</para> <para> 如果您不希望用户能够通过 IP/端口连接，但期望仅使用点对点连接，请传入 0</para>

**参数:**

- `nVirtualP2PPort` (`int`)
- `nIP` (`SteamIPAddress_t`)
- `nPort` (`ushort`)
- `bAllowUseOfPacketRelay` (`bool`)

**返回值:** `SNetListenSocket_t`

**用法示例:**
```csharp
SteamGameServerNetworking.CreateListenSocket(0, new SteamIPAddress_t(), 27015, true);
```

### CreateP2PConnectionSocket (静态)

```csharp
SNetSocket_t CreateP2PConnectionSocket(CSteamID steamIDTarget, int nVirtualPort, int nTimeoutSec, bool bAllowUseOfPacketRelay)
```

<para>创建一个套接字并开始连接到远程目标</para> <para>可以通过已知的 SteamID（客户端或游戏服务器）连接，或直接连接到 IP 地址</para> <para>成功时将触发 SocketStatusCallback_t 回调</para> <para>失败或超时时将触发 SocketStatusCallback_t 回调，并在 m_eSNetSocketState 中包含一个失败代码</para>

**参数:**

- `steamIDTarget` (`CSteamID`)
- `nVirtualPort` (`int`)
- `nTimeoutSec` (`int`)
- `bAllowUseOfPacketRelay` (`bool`)

**返回值:** `SNetSocket_t`

**用法示例:**
```csharp
SteamGameServerNetworking.CreateP2PConnectionSocket(new CSteamID(123456789), 0, 30, true);
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
SteamIPAddress_t ip = new SteamIPAddress_t();
ip.SetIPv4(127, 0, 0, 1);
var socket = SteamGameServerNetworking.CreateConnectionSocket(ip, 27015, 30);
```

### DestroySocket (静态)

```csharp
bool DestroySocket(SNetSocket_t hSocket, bool bNotifyRemoteEnd)
```

断开与套接字的连接（如果存在），并使句柄失效
套接字上任何未读取的数据将被丢弃
如果设置了 bNotifyRemoteEnd，则套接字不会在远程端确认断开连接之前被完全销毁

**参数:**

- `hSocket` (`SNetSocket_t`)
- `bNotifyRemoteEnd` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworking.DestroySocket(hSocket, true);
```

### DestroyListenSocket (静态)

```csharp
bool DestroyListenSocket(SNetListenSocket_t hSocket, bool bNotifyRemoteEnd)
```

销毁监听套接字将自动终止由其生成的所有常规套接字

**参数:**

- `hSocket` (`SNetListenSocket_t`)
- `bNotifyRemoteEnd` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworking.DestroyListenSocket(hSocket, false);
```

### SendDataOnSocket (静态)

```csharp
bool SendDataOnSocket(SNetSocket_t hSocket, byte[] pubData, uint cubData, bool bReliable)
```

<para>发送数据</para> <para>必须是已连接套接字的句柄</para> <para>所有数据均通过UDP发送，因此发送大小限制为1200字节；超过此限制后，许多路由器将开始丢弃数据包</para> <para>谨慎使用可靠标志；尽管重传速率相当激进，</para> <para>它仍可能导致接收数据停滞（类似TCP）</para>

**参数:**

- `hSocket` (`SNetSocket_t`)
- `pubData` (`byte[]`)
- `cubData` (`uint`)
- `bReliable` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
byte[] data = Encoding.UTF8.GetBytes("Hello, Steam!");
SteamGameServerNetworking.SendDataOnSocket(hSocket, data, (uint)data.Length, false);
```

### IsDataAvailableOnSocket (静态)

```csharp
bool IsDataAvailableOnSocket(SNetSocket_t hSocket, out uint pcubMsgSize)
```

<para>接收数据</para> <para>如果没有剩余数据，则返回 false</para> <para>用下一个消息的大小（以字节为单位）填充 *pcubMsgSize</para>

**参数:**

- `hSocket` (`SNetSocket_t`)
- `pcubMsgSize` (`out uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint messageSize;
bool hasData = SteamGameServerNetworking.IsDataAvailableOnSocket(mySocket, out messageSize);
```

### RetrieveDataFromSocket (静态)

```csharp
bool RetrieveDataFromSocket(SNetSocket_t hSocket, byte[] pubDest, uint cubDest, out uint pcubMsgSize)
```

<para>将消息内容填充到 pubDest 中</para> <para>消息总是完整的，其大小与发送时相同（即分组的，而非流式的）</para> <para>如果 *pcubMsgSize &lt; cubDest，则只写入部分数据</para> <para>如果没有可用数据，则返回 false</para>

**参数:**

- `hSocket` (`SNetSocket_t`)
- `pubDest` (`byte[]`)
- `cubDest` (`uint`)
- `pcubMsgSize` (`out uint`)

**返回值:** `bool`

**用法示例:**
```csharp
byte[] buffer = new byte[1024];
uint messageSize;
bool success = SteamGameServerNetworking.RetrieveDataFromSocket(SNetSocket_t.Invalid, buffer, (uint)buffer.Length, out messageSize);
```

### IsDataAvailable (静态)

```csharp
bool IsDataAvailable(SNetListenSocket_t hListenSocket, out uint pcubMsgSize, out SNetSocket_t phSocket)
```

<para>检查从该监听套接字连接的任何套接字上是否有数据</para> <para>如果没有剩余数据，则返回 false</para> <para>用下一个消息的大小（以字节为单位）填充 *pcubMsgSize</para> <para>用有可用数据的套接字填充 *phSocket</para>

**参数:**

- `hListenSocket` (`SNetListenSocket_t`)
- `pcubMsgSize` (`out uint`)
- `phSocket` (`out SNetSocket_t`)

**返回值:** `bool`

**用法示例:**
```csharp
uint msgSize; SNetSocket_t socket;
bool hasData = SteamGameServerNetworking.IsDataAvailable(SNetListenSocket_t.Invalid, out msgSize, out socket);
```

### RetrieveData (静态)

```csharp
bool RetrieveData(SNetListenSocket_t hListenSocket, byte[] pubDest, uint cubDest, out uint pcubMsgSize, out SNetSocket_t phSocket)
```

<para>从通过此监听套接字建立的任何套接字中检索数据</para> <para>用消息内容填充 pubDest</para> <para>消息始终是完整的，大小与发送时相同（即分组的，而非流式的）</para> <para>如果 *pcubMsgSize &lt; cubDest，则只写入部分数据</para> <para>如果没有可用数据，则返回 false</para> <para>用数据可用的套接字填充 *phSocket</para>

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
uint messageSize;
SNetSocket_t socket;
bool success = SteamGameServerNetworking.RetrieveData(SteamGameServerNetworking.k_hListenSocket, buffer, (uint)buffer.Length, out messageSize, out socket);
```

### GetSocketInfo (静态)

```csharp
bool GetSocketInfo(SNetSocket_t hSocket, out CSteamID pSteamIDRemote, out int peSocketStatus, out SteamIPAddress_t punIPRemote, out ushort punPortRemote)
```

<para> 返回有关指定套接字的详细信息，并填充指针所指向的内容</para>

**参数:**

- `hSocket` (`SNetSocket_t`)
- `pSteamIDRemote` (`out CSteamID`)
- `peSocketStatus` (`out int`)
- `punIPRemote` (`out SteamIPAddress_t`)
- `punPortRemote` (`out ushort`)

**返回值:** `bool`

**用法示例:**
```csharp
CSteamID steamID;
int socketStatus;
SteamIPAddress_t ipAddr;
ushort port;
bool result = SteamGameServerNetworking.GetSocketInfo(hSocket, out steamID, out socketStatus, out ipAddr, out port);
```

### GetListenSocketInfo (静态)

```csharp
bool GetListenSocketInfo(SNetListenSocket_t hListenSocket, out SteamIPAddress_t pnIP, out ushort pnPort)
```

<para>返回监听套接字绑定的本地端口</para> <para>如果套接字设置为仅侦听P2P连接，则*pnIP和*pnPort将为0</para>

**参数:**

- `hListenSocket` (`SNetListenSocket_t`)
- `pnIP` (`out SteamIPAddress_t`)
- `pnPort` (`out ushort`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworking.GetListenSocketInfo(hListenSocket, out var ip, out var port);
```

### GetSocketConnectionType (静态)

```csharp
ESNetSocketConnectionType GetSocketConnectionType(SNetSocket_t hSocket)
```

<para> 返回 true 以描述套接字最终如何建立连接 </para>

**参数:**

- `hSocket` (`SNetSocket_t`)

**返回值:** `ESNetSocketConnectionType`

**用法示例:**
```csharp
SteamGameServerNetworking.GetSocketConnectionType(hSocket);
```

### GetMaxPacketSize (静态)

```csharp
int GetMaxPacketSize(SNetSocket_t hSocket)
```

<para> 最大数据包大小，以字节为单位</para>

**参数:**

- `hSocket` (`SNetSocket_t`)

**返回值:** `int`

**用法示例:**
```csharp
int maxPacketSize = SteamGameServerNetworking.GetMaxPacketSize(hSocket);
```

