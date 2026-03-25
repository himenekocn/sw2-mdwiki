# 📦 SteamGameServerNetworking

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### SendP2PPacket (静态)

```csharp
bool SendP2PPacket(CSteamID steamIDRemote, byte[] pubData, uint cubData, EP2PSend eP2PSendType, int nChannel = 0)
```

<para> </para><para> 类 UDP（无连接）网络接口。这些函数围绕目标地址组织 API 以发送消息，支持可靠和不可靠消息。</para><para> 如需更具 TCP 风格的接口（即拥有连接句柄），请参见下方的相关函数。</para><para> 两种接口风格均可发送可靠和不可靠消息。</para><para> 自动建立 NAT 穿透或中继服务器连接。</para><para> 这些 API 已被弃用，可能在未来的 Steamworks SDK 版本中被移除。请参阅 ISteamNetworkingMessages。</para><para> 向指定用户发送 P2P 数据包。</para><para> 行为类似 UDP：不可靠，最大数据包大小为 1200 字节。</para><para> 首个发送的数据包可能会因执行 NAT 穿透代码而延迟。</para><para> 若无法连接到该用户，将通过回调 P2PSessionConnectFail_t 发布错误。</para><para> 有关不同数据包发送方式的描述，请参见上方的 EP2PSend 枚举。</para><para> nChannel 是一个路由编号，可用于将消息路由至不同的系统；需在另一端调用 ReadP2PPacket() 并传入相同的通道号以检索数据。</para><para> 使用不同通道与同一用户通信仍会复用底层 P2P 连接，从而节省资源。</para>

**参数:**

- `steamIDRemote` (`CSteamID`)
- `pubData` (`byte[]`)
- `cubData` (`uint`)
- `eP2PSendType` (`EP2PSend`)
- `nChannel` (`int`) = `0`

**返回值:** `bool`

**用法示例:**
```csharp
byte[] data = System.Text.Encoding.UTF8.GetBytes("hello");
SteamGameServerNetworking.SendP2PPacket(steamIDRemote, data, (uint)data.Length, EP2PSend.Unreliable, 0);
```

### IsP2PPacketAvailable (静态)

```csharp
bool IsP2PPacketAvailable(out uint pcubMsgSize, int nChannel = 0)
```

返回 true 表示有可用数据可供读取，并返回需要读取的数据量。

**参数:**

- `pcubMsgSize` (`out uint`)
- `nChannel` (`int`) = `0`

**返回值:** `bool`

**用法示例:**
```csharp
uint msgSize;
if (SteamGameServerNetworking.IsP2PPacketAvailable(out msgSize, 0)) { }
```

### ReadP2PPacket (静态)

```csharp
bool ReadP2PPacket(byte[] pubDest, uint cubDest, out uint pcubMsgSize, out CSteamID psteamIDRemote, int nChannel = 0)
```

<para>读取通过 SendP2PPacket() 从其他用户发送的数据包</para> <para>在最后两个参数中返回消息的大小及发送该消息的用户 SteamID</para> <para>如果传入的缓冲区过小，消息将被截断</para> <para>此调用为非阻塞操作，若无可用数据则返回 false</para>

**参数:**

- `pubDest` (`byte[]`)
- `cubDest` (`uint`)
- `pcubMsgSize` (`out uint`)
- `psteamIDRemote` (`out CSteamID`)
- `nChannel` (`int`) = `0`

**返回值:** `bool`

**用法示例:**
```csharp
uint msgSize; CSteamID remoteId; bool ok = SteamGameServerNetworking.ReadP2PPacket(buffer, (uint)buffer.Length, out msgSize, out remoteId, 0);
```

### AcceptP2PSessionWithUser (静态)

```csharp
bool AcceptP2PSessionWithUser(CSteamID steamIDRemote)
```

AcceptP2PSessionWithUser() 仅应在响应 P2PSessionRequest_t 回调时调用。当其他用户尝试向您发送尚未建立通信的数据包时，将发布 P2PSessionRequest_t 事件。如果您不希望与该用户通信，可直接忽略该请求。若该用户继续向您发送数据包，系统将周期性发布新的 P2PSessionRequest_t 事件。此方法可能针对同一用户被多次调用。（若您已对该用户调用 SendP2PPacket()，则隐式接受了对方的会话请求。）

**参数:**

- `steamIDRemote` (`CSteamID`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworking.AcceptP2PSessionWithUser(steamIdRemote);
```

### CloseP2PSessionWithUser (静态)

```csharp
bool CloseP2PSessionWithUser(CSteamID steamIDRemote)
```

在结束与某用户的通信后调用 CloseP2PSessionWithUser()，该操作将在底层释放相关资源。如果远程用户再次尝试向您发送数据，将触发另一个 P2PSessionRequest_t 回调。

**参数:**

- `steamIDRemote` (`CSteamID`)

**返回值:** `bool`

**用法示例:**
```csharp
bool closed = SteamGameServerNetworking.CloseP2PSessionWithUser(remoteSteamId);
```

### CloseP2PChannelWithUser (静态)

```csharp
bool CloseP2PChannelWithUser(CSteamID steamIDRemote, int nChannel)
```

调用 CloseP2PChannelWithUser() 以结束与特定用户在某个通道上的通信。一旦所有对该用户的开放通道均已关闭，则与该用户的会话将被终止，此后来自该用户的新数据将触发 P2PSessionRequest_t 回调。

**参数:**

- `steamIDRemote` (`CSteamID`)
- `nChannel` (`int`)

**返回值:** `bool`

**用法示例:**
```csharp
bool closed = SteamGameServerNetworking.CloseP2PChannelWithUser(steamIDRemote, 1);
```

### GetP2PSessionState (静态)

```csharp
bool GetP2PSessionState(CSteamID steamIDRemote, out P2PSessionState_t pConnectionState)
```

<para>使用关于该用户底层连接的详细信息填充 P2PSessionState_t 结构体</para> <para>仅用于调试目的时所需</para> <para>若不存在与指定用户的连接，则返回 false</para>

**参数:**

- `steamIDRemote` (`CSteamID`)
- `pConnectionState` (`out P2PSessionState_t`)

**返回值:** `bool`

**用法示例:**
```csharp
P2PSessionState_t state; bool hasState = SteamGameServerNetworking.GetP2PSessionState(steamIDRemote, out state);
```

### AllowP2PPacketRelay (静态)

```csharp
bool AllowP2PPacketRelay(bool bAllow)
```

<para>允许 P2P 连接在无法建立直接连接或 NAT 穿透时，回退为通过 Steam 服务器进行中继。</para> <para>该设置仅适用于设置此值后创建的连接，或在设置此值后需要自动重连的现有连接。</para> <para>P2P 数据包中继默认处于允许状态。</para> <para>注意：此函数已被弃用，并可能在 SDK 的未来版本中被移除。出于安全考虑，即使您向此函数传入 false，我们仍可能决定将某些对等节点的流量进行中继，以防止客户端 IP 地址泄露给其他对等节点。</para>

**参数:**

- `bAllow` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
bool enabled = SteamGameServerNetworking.AllowP2PPacketRelay(true);
```

### CreateListenSocket (静态)

```csharp
SNetListenSocket_t CreateListenSocket(int nVirtualP2PPort, SteamIPAddress_t nIP, ushort nPort, bool bAllowUseOfPacketRelay)
```

<para> </para> <para> LISTEN / CONNECT 面向连接的接口函数</para> <para> 这些函数的行为类似于客户端 - 服务器 TCP API。一端作为“服务器”监听传入的连接，随后必须将其“接受”。“客户端”则通过“连接”来发起通信。数据的发送和接收通过连接句柄进行。</para> <para> 如果您需要一种更类似 UDP 的接口（即不跟踪连接句柄，而是直接向 SteamID 发送消息），请使用上方的 UDP 风格函数。</para> <para> 两种方法均支持可靠传输和非可靠传输。</para> <para> 这些 API 已弃用，并可能在未来的 Steamworks SDK 版本中被移除。请参阅 ISteamNetworkingSockets。</para> <para> </para> <para> 创建一个套接字并监听其他客户端的连接请求</para> <para> 当有其他客户端连接时，将触发 SocketStatusCallback_t 回调</para> <para> nVirtualP2PPort 是客户端连接的目标唯一标识符。如果您需要多个端口，可设置此值；通常设为 0 即可，除非您需要多组独立的连接。</para> <para> unIP 是要绑定的本地 IP 地址。</para> <para> 若希望使用默认本地 IP，请传入 0。</para> <para> unPort 是要使用的端口号。</para> <para> 若您不希望用户能通过 IP/端口进行连接，而仅期望建立点对点（Peer-to-Peer）连接，请传入 0。</para>

**参数:**

- `nVirtualP2PPort` (`int`)
- `nIP` (`SteamIPAddress_t`)
- `nPort` (`ushort`)
- `bAllowUseOfPacketRelay` (`bool`)

**返回值:** `SNetListenSocket_t`

**用法示例:**
```csharp
var listenSocket = SteamGameServerNetworking.CreateListenSocket(0, default, 0, true);
```

### CreateP2PConnectionSocket (静态)

```csharp
SNetSocket_t CreateP2PConnectionSocket(CSteamID steamIDTarget, int nVirtualPort, int nTimeoutSec, bool bAllowUseOfPacketRelay)
```

<para>创建套接字并开始连接到远程目标</para><para>可通过已知的 SteamID（客户端或游戏服务器）或直接通过 IP 地址进行连接</para><para>若连接成功，将触发 SocketStatusCallback_t 回调</para><para>若连接失败或超时，将触发 SocketStatusCallback_t 回调，并在 m_eSNetSocketState 中返回错误代码</para>

**参数:**

- `steamIDTarget` (`CSteamID`)
- `nVirtualPort` (`int`)
- `nTimeoutSec` (`int`)
- `bAllowUseOfPacketRelay` (`bool`)

**返回值:** `SNetSocket_t`

**用法示例:**
```csharp
SNetSocket_t socket = SteamGameServerNetworking.CreateP2PConnectionSocket(targetSteamId, 0, 10, true);
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
SteamIPAddress_t ip = default;
SNetSocket_t socket = SteamGameServerNetworking.CreateConnectionSocket(ip, 27015, 10);
```

### DestroySocket (静态)

```csharp
bool DestroySocket(SNetSocket_t hSocket, bool bNotifyRemoteEnd)
```

断开与套接字的连接（如果存在），并使句柄无效。  
套接字上任何未读取的数据都将被丢弃。  
如果设置了 bNotifyRemoteEnd，则套接字不会完全销毁，直到远程端确认断开连接。

**参数:**

- `hSocket` (`SNetSocket_t`)
- `bNotifyRemoteEnd` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerNetworking.DestroySocket(hSocket, true);
```

### DestroyListenSocket (静态)

```csharp
bool DestroyListenSocket(SNetListenSocket_t hSocket, bool bNotifyRemoteEnd)
```

销毁监听套接字将自动终止由此生成的所有常规套接字。

**参数:**

- `hSocket` (`SNetListenSocket_t`)
- `bNotifyRemoteEnd` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
SNetListenSocket_t hSocket = default;
SteamGameServerNetworking.DestroyListenSocket(hSocket, true);
```

### SendDataOnSocket (静态)

```csharp
bool SendDataOnSocket(SNetSocket_t hSocket, byte[] pubData, uint cubData, bool bReliable)
```

<para>发送数据</para><para>必须是已连接套接字的句柄</para><para>所有数据均通过 UDP 发送，因此发送大小限制为 1200 字节；超过此值后，许多路由器将开始丢弃数据包</para><para>谨慎使用可靠标志；尽管重传速率相当激进，</para><para>但仍可能导致数据接收阻塞（类似于 TCP）</para>

**参数:**

- `hSocket` (`SNetSocket_t`)
- `pubData` (`byte[]`)
- `cubData` (`uint`)
- `bReliable` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerNetworking.SendDataOnSocket(hSocket, payload, (uint)payload.Length, true);
```

### IsDataAvailableOnSocket (静态)

```csharp
bool IsDataAvailableOnSocket(SNetSocket_t hSocket, out uint pcubMsgSize)
```

接收数据
若剩余数据为空则返回 false
将下一个消息的大小（以字节为单位）填充至 *pcubMsgSize

**参数:**

- `hSocket` (`SNetSocket_t`)
- `pcubMsgSize` (`out uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint msgSize; bool hasData = SteamGameServerNetworking.IsDataAvailableOnSocket(hSocket, out msgSize);
```

### RetrieveDataFromSocket (静态)

```csharp
bool RetrieveDataFromSocket(SNetSocket_t hSocket, byte[] pubDest, uint cubDest, out uint pcubMsgSize)
```

将消息内容填充到 pubDest 中。
消息始终是完整的，其大小与发送时相同（即采用分组方式传输，而非流式传输）。
如果 *pcubMsgSize < cubDest，则仅写入部分数据。
如果没有可用数据，则返回 false。

**参数:**

- `hSocket` (`SNetSocket_t`)
- `pubDest` (`byte[]`)
- `cubDest` (`uint`)
- `pcubMsgSize` (`out uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint msgSize; bool ok = SteamGameServerNetworking.RetrieveDataFromSocket(hSocket, buffer, (uint)buffer.Length, out msgSize);
```

### IsDataAvailable (静态)

```csharp
bool IsDataAvailable(SNetListenSocket_t hListenSocket, out uint pcubMsgSize, out SNetSocket_t phSocket)
```

检查从此监听套接字连接的任意套接字上的数据。
若没有剩余数据则返回 false。
通过 *pcubMsgSize 填充下一条消息的大小（以字节为单位）。
通过 *phSocket 填充有可用数据的套接字。

**参数:**

- `hListenSocket` (`SNetListenSocket_t`)
- `pcubMsgSize` (`out uint`)
- `phSocket` (`out SNetSocket_t`)

**返回值:** `bool`

**用法示例:**
```csharp
uint msgSize; SNetSocket_t socket; if (SteamGameServerNetworking.IsDataAvailable(listenSocket, out msgSize, out socket)) ProcessMessage(socket, msgSize);
```

### RetrieveData (静态)

```csharp
bool RetrieveData(SNetListenSocket_t hListenSocket, byte[] pubDest, uint cubDest, out uint pcubMsgSize, out SNetSocket_t phSocket)
```

从与该监听套接字关联连接的任意套接字中检索数据。  
将消息内容填充至 pubDest 参数。  
消息始终为完整数据包，其大小与发送时一致（即按包处理，而非流式传输）。  
若 *pcubMsgSize < cubDest，则仅写入部分数据。  
若无可用数据，则返回 false。  
将提供数据的套接字地址填充至 *phSocket 参数。

**参数:**

- `hListenSocket` (`SNetListenSocket_t`)
- `pubDest` (`byte[]`)
- `cubDest` (`uint`)
- `pcubMsgSize` (`out uint`)
- `phSocket` (`out SNetSocket_t`)

**返回值:** `bool`

**用法示例:**
```csharp
if (SteamGameServerNetworking.RetrieveData(listenSocket, destBuffer, (uint)destBuffer.Length, out uint msgSize, out SNetSocket_t socket)) { /* 处理 msgSize 和 socket */ }
```

### GetSocketInfo (静态)

```csharp
bool GetSocketInfo(SNetSocket_t hSocket, out CSteamID pSteamIDRemote, out int peSocketStatus, out SteamIPAddress_t punIPRemote, out ushort punPortRemote)
```

返回指定套接字的信息，并填充指针所指向的内容。

**参数:**

- `hSocket` (`SNetSocket_t`)
- `pSteamIDRemote` (`out CSteamID`)
- `peSocketStatus` (`out int`)
- `punIPRemote` (`out SteamIPAddress_t`)
- `punPortRemote` (`out ushort`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerNetworking.GetSocketInfo(hSocket, out CSteamID remoteId, out int socketStatus, out SteamIPAddress_t ipRemote, out ushort portRemote);
```

### GetListenSocketInfo (静态)

```csharp
bool GetListenSocketInfo(SNetListenSocket_t hListenSocket, out SteamIPAddress_t pnIP, out ushort pnPort)
```

<para>返回监听套接字绑定的本地端口</para> <para>*pnIP 和 *pnPort 若套接字仅设置为监听 P2P 连接，则均为 0</para>

**参数:**

- `hListenSocket` (`SNetListenSocket_t`)
- `pnIP` (`out SteamIPAddress_t`)
- `pnPort` (`out ushort`)

**返回值:** `bool`

**用法示例:**
```csharp
SNetListenSocket_t listenSocket = default;
bool ok = SteamGameServerNetworking.GetListenSocketInfo(listenSocket, out SteamIPAddress_t ip, out ushort port);
```

### GetSocketConnectionType (静态)

```csharp
ESNetSocketConnectionType GetSocketConnectionType(SNetSocket_t hSocket)
```

<para>返回 true 以描述连接是如何建立的</para>

**参数:**

- `hSocket` (`SNetSocket_t`)

**返回值:** `ESNetSocketConnectionType`

**用法示例:**
```csharp
var connectionType = SteamGameServerNetworking.GetSocketConnectionType(hSocket);
```

### GetMaxPacketSize (静态)

```csharp
int GetMaxPacketSize(SNetSocket_t hSocket)
```

最大数据包大小，单位为字节

**参数:**

- `hSocket` (`SNetSocket_t`)

**返回值:** `int`

**用法示例:**
```csharp
int maxPacketSize = SteamGameServerNetworking.GetMaxPacketSize(socketHandle);
Console.WriteLine(maxPacketSize);
```

