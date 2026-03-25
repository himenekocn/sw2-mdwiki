# 📦 SteamGameServerNetworkingSockets

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### CreateListenSocketIP (静态)

```csharp
HSteamListenSocket CreateListenSocketIP(ref SteamNetworkingIPAddr localAddress, int nOptions, SteamNetworkingConfigValue_t[] pOptions)
```

<para>/ 创建一个“服务器”套接字，通过普通的 UDP（IPv4 或 IPv6）监听客户端连接请求，</para> <para>/ 客户端需调用 ConnectByIPAddress 进行连接。</para> <para>/</para> <para>/ 必须选择一个特定的本地端口用于监听，并将其设置到本地地址的 port 字段中。</para> <para>/</para> <para>/ 通常应将地址的 IP 部分设置为零（SteamNetworkingIPAddr::Clear()）。</para> <para>/ 这表示不会绑定到任何特定的本地接口（即与纯 Socket 代码中的 INADDR_ANY 相同）。此外，如果可能，该套接字将以“双栈”模式绑定，这意味着它可以同时接受 IPv4 和 IPv6 客户端连接。</para> <para>/ 若确实需要绑定特定接口，则将本地地址设置为相应的 IPv4 或 IPv6 地址即可。</para> <para>/</para> <para>/ 如需设置任何初始配置选项，请在此处传入。有关为何此方式优于在创建后“立即”设置选项的说明，请参阅 SteamNetworkingConfigValue_t。</para> <para>/</para> <para>/ 当客户端尝试连接时，将发布一个 SteamNetConnectionStatusChangedCallback_t 回调。此时连接状态为“正在连接”。</para>

**参数:**

- `localAddress` (`ref SteamNetworkingIPAddr`)
- `nOptions` (`int`)
- `pOptions` (`SteamNetworkingConfigValue_t[]`)

**返回值:** `HSteamListenSocket`

**用法示例:**
```csharp
SteamNetworkingIPAddr addr = default; addr.Clear(); addr.port = 27015;
HSteamListenSocket listenSocket = SteamGameServerNetworkingSockets.CreateListenSocketIP(ref addr, 0, null);
```

### ConnectByIPAddress (静态)

```csharp
HSteamNetConnection ConnectByIPAddress(ref SteamNetworkingIPAddr address, int nOptions, SteamNetworkingConfigValue_t[] pOptions)
```

<para>/ 在指定的 IPv4 或 IPv6 地址上创建连接，并通过 UDP 开始与"服务器"通信。</para> <para>/ 远程主机必须在指定端口上使用匹配的 CreateListenSocketIP 调用进行监听。</para> <para>/</para> <para>/ 当开始连接时，将触发一个 SteamNetConnectionStatusChangedCallback_t 回调；随后在超时或连接成功时，将触发另一个回调。</para> <para>/</para> <para>/ 如果服务器未配置任何身份标识，则其网络地址将是唯一使用的身份。或者，网络主机可提供平台特定的身份标识，并可选择附带有效证书以验证该身份。（这些详细信息将包含在 SteamNetConnectionStatusChangedCallback_t 中。）是否允许该连接由您的应用程序自行决定。</para> <para>/</para> <para>/ 默认情况下，所有连接都将获得基本加密，足以防止非专业窃听。但请注意，如果没有证书（或通过其他带外机制分发的共享密钥），您无法确认另一端实际是谁，因此容易受到中间人攻击。</para> <para>/</para> <para>/ 如需设置任何初始配置选项，请在此处传递它们。有关为何优于在创建后“立即”设置选项的更多信息，请参阅 SteamNetworkingConfigValue_t。</para>

**参数:**

- `address` (`ref SteamNetworkingIPAddr`)
- `nOptions` (`int`)
- `pOptions` (`SteamNetworkingConfigValue_t[]`)

**返回值:** `HSteamNetConnection`

**用法示例:**
```csharp
SteamNetworkingIPAddr address = default;
HSteamNetConnection conn = SteamGameServerNetworkingSockets.ConnectByIPAddress(ref address, 0, null);
```

### CreateListenSocketP2P (静态)

```csharp
HSteamListenSocket CreateListenSocketP2P(int nLocalVirtualPort, int nOptions, SteamNetworkingConfigValue_t[] pOptions)
```

<para>/ 与 CreateListenSocketIP 类似，但客户端将通过 ConnectP2P 进行连接。</para> <para>/</para> <para>/ nLocalVirtualPort 指定客户端如何使用 ConnectP2P 连接到该套接字。对于仅拥有一个监听套接字的应用程序而言，这是非常常见的情况；此时应使用零。如果您需要打开多个监听套接字，并允许客户端连接到其中任意一个，则 nLocalVirtualPort 应为每个创建的监听套接字分配一个唯一的小整数（<1000）。</para> <para>/</para> <para>/ 若使用此方法，您的应用在初始化时可能还需要调用 ISteamNetworkingUtils::InitRelayNetworkAccess()。</para> <para>/</para> <para>/ 如果您在已知数据中心的专用服务器上监听，可以使用本函数替代 CreateHostedDedicatedServerListenSocket，从而允许客户端无需票据即可连接。任何拥有该应用并已登录 Steam 的用户均可尝试连接至您的服务器。此外，连接请求可能需要客户端保持与 Steam 的连接，这增加了潜在的失败点。而在使用票据的情况下，一旦获取了票据，即使客户端从 Steam 断开或 Steam 处于离线状态，仍可连接至您的服务器。</para> <para>/</para> <para>/ 如需设置任何初始配置选项，请在此处传递它们。有关为何此方式优于在创建后立即设置这些选项的详细信息，请参阅 SteamNetworkingConfigValue_t。</para>

**参数:**

- `nLocalVirtualPort` (`int`)
- `nOptions` (`int`)
- `pOptions` (`SteamNetworkingConfigValue_t[]`)

**返回值:** `HSteamListenSocket`

**用法示例:**
```csharp
HSteamListenSocket listenSocket = SteamGameServerNetworkingSockets.CreateListenSocketP2P(0, 0, null);
```

### ConnectP2P (静态)

```csharp
HSteamNetConnection ConnectP2P(ref SteamNetworkingIdentity identityRemote, int nRemoteVirtualPort, int nOptions, SteamNetworkingConfigValue_t[] pOptions)
```

<para>/ 开始连接使用平台特定标识符识别的对等节点。</para> <para>/ 此方法使用默认的会合服务，其具体实现取决于平台和库配置。（例如在 Steam 上，通信将通过 Steam 后端进行。）</para> <para>/</para> <para>/ 如需设置任何初始配置选项，请在此处传入。请参阅</para> <para>/ SteamNetworkingConfigValue_t 以了解为何这种方式优于在创建后立即设置选项。</para> <para>/</para> <para>/ 若要使用自定义信令服务，请参见：</para> <para>/ - ConnectP2PCustomSignaling</para> <para>/ - k_ESteamNetworkingConfig_Callback_CreateConnectionSignaling</para>

**参数:**

- `identityRemote` (`ref SteamNetworkingIdentity`)
- `nRemoteVirtualPort` (`int`)
- `nOptions` (`int`)
- `pOptions` (`SteamNetworkingConfigValue_t[]`)

**返回值:** `HSteamNetConnection`

**用法示例:**
```csharp
var conn = SteamGameServerNetworkingSockets.ConnectP2P(ref identityRemote, 0, 0, null);
```

### AcceptConnection (静态)

```csharp
EResult AcceptConnection(HSteamNetConnection hConn)
```

<para>/ 接收监听套接字上收到的传入连接。</para> <para>/</para> <para>/ 当收到连接请求时（可能在交换了少量基本握手数据包以防止简单伪造后），会创建一个处于 k_ESteamNetworkingConnectionState_Connecting 状态的连接接口对象，并发布 SteamNetConnectionStatusChangedCallback_t 回调。此时，您的应用程序必须选择接受或关闭该连接（不得忽略它）。接受连接后，根据连接类型，连接状态将转换至已连接状态（Connected）或正在寻找路由状态（Finding Route）。</para> <para>/</para> <para>/ 您应在一两秒内采取行动，因为接受连接是实际发送响应通知客户端已建立连接的操作。如果延迟处理，从客户端视角来看，等同于网络无响应，客户端可能会因超时而放弃连接尝试。换言之，客户端无法区分延迟是由网络问题引起还是由应用程序处理缓慢导致。</para> <para>/</para> <para>/ 这意味着，如果您的应用程序超过数秒未处理回调（例如在加载地图期间），则在此期间可能有客户端发起连接尝试，但因超时而失败。</para> <para>/</para> <para>/ 如果应用程序未及时响应连接请求，且我们停止收到来自客户端的通信，则该连接尝试将在本地超时，并将连接状态转换为 k_ESteamNetworkingConnectionState_ProblemDetectedLocally。客户端也可能在接受前主动关闭连接，具体事件序列不同，也可能触发转换至 k_ESteamNetworkingConnectionState_ClosedByPeer 状态。</para> <para>/</para> <para>/ 若句柄无效，返回 k_EResultInvalidParam。</para> <para>/ 若连接当前不在合适的状态，返回 k_EResultInvalidState。（请注意，从回调被加入队列到应用程序接收到该回调之间，连接状态可能发生变化。）</para> <para>/</para> <para>/ 关于连接配置选项的说明：如果您需要为通过特定监听套接字接受的所有连接设置通用配置选项，建议直接在监听套接字上设置这些选项，因为它们会自动继承。若您确实需要设置仅针对单个连接的选项，在调用接受操作之前对连接设置这些选项也是安全的。</para>

**参数:**

- `hConn` (`HSteamNetConnection`)

**返回值:** `EResult`

**用法示例:**
```csharp
EResult result = SteamGameServerNetworkingSockets.AcceptConnection(hConn);
```

### CloseConnection (静态)

```csharp
bool CloseConnection(HSteamNetConnection hPeer, int nReason, string pszDebug, bool bEnableLinger)
```

<para>/ 断开与远程主机的连接并使连接句柄失效。</para> <para>/ 连接上任何未读取的数据将被丢弃。</para> <para>/</para> <para>/ nReason 是一个由应用程序定义的错误代码，将在另一端接收（在可能时）记录到后端分析系统中。该值应取自受限范围。（参见 ESteamNetConnectionEnd。）如果您不需要向远程主机传递任何信息，且不希望分析系统区分“正常”连接终止与“异常”终止，则可以传入零；此时将使用通用值 k_ESteamNetConnectionEnd_App_Generic。</para> <para>/</para> <para>/ pszDebug 是一个可选的人类可读诊断字符串，将被远程主机接收（在可能时）记录到后端分析系统中。</para> <para>/</para> <para>/ 如果您希望将套接字置于“ linger"状态（即尝试刷新任何待发送的剩余数据），请使用 bEnableLinger=true。否则，可靠数据不会被刷新。</para> <para>/</para> <para>/ 如果连接已经结束，您仅是释放连接接口，则原因代码、调试字符串和 linger 标志将被忽略。</para>

**参数:**

- `hPeer` (`HSteamNetConnection`)
- `nReason` (`int`)
- `pszDebug` (`string`)
- `bEnableLinger` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
bool closed = SteamGameServerNetworkingSockets.CloseConnection(hPeer, 1001, "Server shutting down", false);
```

### CloseListenSocket (静态)

```csharp
bool CloseListenSocket(HSteamListenSocket hSocket)
```

<para>/ 销毁监听套接字。所有通过该监听套接字接受连接的连接都将非优雅地关闭。</para>

**参数:**

- `hSocket` (`HSteamListenSocket`)

**返回值:** `bool`

**用法示例:**
```csharp
bool closed = SteamGameServerNetworkingSockets.CloseListenSocket(hListenSocket);
```

### SetConnectionUserData (静态)

```csharp
bool SetConnectionUserData(HSteamNetConnection hPeer, long nUserData)
```

<para>/ 设置连接用户数据。该数据将在以下位置返回：</para> <para>/ - 可使用 GetConnectionUserData 进行查询。</para> <para>/ - SteamNetworkingmessage_t 结构体中。</para> <para>/ - SteamNetConnectionInfo_t 结构体中。</para> <para>/ （其为 SteamNetConnectionStatusChangedCallback_t 的成员，但请参见下方的警告!!!!）</para> <para>/</para> <para>/ 您是否需要在创建连接时原子地设置此值？</para> <para>/ 请参阅 k_ESteamNetworkingConfig_ConnectionUserData。</para> <para>/</para> <para>/ 警告：在使用回调结构体中提供的值时必须 *格外小心*。</para> <para>/ 回调是队列化的，您在回调中接收到的 userdata 值是回调入队时刻有效的 userdata。若您未理解这一点，可能会引发微妙的竞态条件！</para> <para>/</para> <para>/ 若该连接的任意传入消息已入队，则 userdata 字段将被更新，因此当您接收消息（例如通过 ReceiveMessagesOnConnection）时，它们将始终携带最新的 userdata。因此，与回调相关的棘手竞态条件不适用于消息检索操作。</para> <para>/</para> <para>/ 若句柄无效，则返回 false。</para>

**参数:**

- `hPeer` (`HSteamNetConnection`)
- `nUserData` (`long`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerNetworkingSockets.SetConnectionUserData(hPeer, 123456789L);
```

### GetConnectionUserData (静态)

```csharp
long GetConnectionUserData(HSteamNetConnection hPeer)
```

<para>/ 获取连接用户数据。如果句柄无效，或者尚未为连接设置任何用户数据，则返回 -1。</para>

**参数:**

- `hPeer` (`HSteamNetConnection`)

**返回值:** `long`

**用法示例:**
```csharp
long userData = SteamGameServerNetworkingSockets.GetConnectionUserData(hPeer);
```

### SetConnectionName (静态)

```csharp
void SetConnectionName(HSteamNetConnection hPeer, string pszName)
```

<para>/ 为连接设置名称，主要用于调试</para>

**参数:**

- `hPeer` (`HSteamNetConnection`)
- `pszName` (`string`)

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.SetConnectionName(hPeer, "LobbyPeer");
```

### GetConnectionName (静态)

```csharp
bool GetConnectionName(HSteamNetConnection hPeer, out string pszName, int nMaxLen)
```

<para>/ 获取连接名称。如果句柄无效则返回 false</para>

**参数:**

- `hPeer` (`HSteamNetConnection`)
- `pszName` (`out string`)
- `nMaxLen` (`int`)

**返回值:** `bool`

**用法示例:**
```csharp
string name;
bool ok = SteamGameServerNetworkingSockets.GetConnectionName(hPeer, out name, 64);
```

### SendMessageToConnection (静态)

```csharp
EResult SendMessageToConnection(HSteamNetConnection hConn, IntPtr pData, uint cbData, int nSendFlags, out long pOutMessageNumber)
```

<para>/ 向指定连接上的远程主机发送消息。</para> <para>/</para> <para>/ nSendFlags 决定将提供的交付保证、数据缓冲时机等。例如 k_nSteamNetworkingSend_Unreliable。</para> <para>/</para> <para>/ 请注意，此处使用的消息语义与标准“流式”套接字（SOCK_STREAM）的语义并不完全相同。</para> <para>/ 对于普通流式套接字，数据块之间的边界被视为无关紧要，写入的数据块大小不一定与另一端读取操作返回的数据块大小匹配。远程主机可能会读取部分数据块，或者多个数据块可能会被合并。然而，对于此处使用的消息语义，数据块大小将会严格匹配。每次发送调用将一对一地对应远程主机上的一次成功读取调用。如果您正在将现有的面向流的代码移植到可靠消息语义，您的代码应能正常工作，因为可靠消息语义比流式语义更为严格。唯一的注意事项涉及性能：为了保留消息大小，每条消息都会产生额外开销，因此如果您的代码发送大量小块数据，性能将会下降。任何基于流式套接字且不频繁写入极小数据块的代码均可无需任何修改即可工作。</para> <para>/</para> <para>/ pOutMessageNumber 是一个可选指针，用于接收分配给该消息的消息编号（仅在发送成功时有效）。</para> <para>/</para> <para>/ 返回值：</para> <para>/ - k_EResultInvalidParam：连接句柄无效，或单个消息过大。（参见 k_cbMaxSteamNetworkingSocketsMessageSizeSend）</para> <para>/ - k_EResultInvalidState：连接处于无效状态</para> <para>/ - k_EResultNoConnection：连接已终止</para> <para>/ - k_EResultIgnored：您使用了 k_nSteamNetworkingSend_NoDelay，但由于尚未准备好发送，导致消息被丢弃。</para> <para>/ - k_EResultLimitExceeded：待发送队列中的数据量已超过上限。（参见 k_ESteamNetworkingConfig_SendBufferSize）</para>

**参数:**

- `hConn` (`HSteamNetConnection`)
- `pData` (`IntPtr`)
- `cbData` (`uint`)
- `nSendFlags` (`int`)
- `pOutMessageNumber` (`out long`)

**返回值:** `EResult`

**用法示例:**
```csharp
long messageNumber; var result = SteamGameServerNetworkingSockets.SendMessageToConnection(hConn, dataPtr, cbData, k_nSteamNetworkingSend_Unreliable, out messageNumber);
```

### SendMessages (静态)

```csharp
void SendMessages(int nMessages, SteamNetworkingMessage_t[] pMessages, long[] pOutMessageNumberOrResult)
```

<para>/ 发送一个或多个消息，且不复制消息负载。</para> <para>/ 这是发送消息最高效的方式。要使用此</para> <para>/ 函数，您必须首先使用</para> <para>/ ISteamNetworkingUtils::AllocateMessage 分配一个消息对象。（请勿在栈上声明或自行分配。）</para> <para>/</para> <para>/ 您应填充消息负载。您可以让系统为您分配缓冲区并随后填充负载，</para> <para>/ 或者如果您已拥有分配的缓冲区，只需将 m_pData 指向您的缓冲区，并将回调设置为相应的释放函数。</para> <para>/ 请注意，若使用您自己的缓冲区，该缓冲区必须在回调执行前始终保持有效。同时请注意，您的回调可能在任意时刻从任意线程被调用（甚至可能在 SendMessages 返回之前），因此它必须是快速且线程安全的。</para> <para>/</para> <para>/ 您还必须填写以下字段：</para> <para>/ - m_conn：要发送消息的目标连接的句柄。</para> <para>/ - m_nFlags：k_nSteamNetworkingSend_xxx 标志的位掩码。</para> <para>/</para> <para>/ 所有其他字段当前保留，不应修改。</para> <para>/</para> <para>/ 库将接管这些消息结构的所有权。它们可能随时被修改或变为无效，因此在将它们传递给此函数后，不得再读取它们。</para> <para>/</para> <para>/ pOutMessageNumberOrResult 是一个可选数组，用于接收每条消息的消息编号（如果发送成功）。如果发送失败，则向数组中写入负的 EResult 值。例如，若连接处于无效状态，数组中将保存 -k_EResultInvalidState。</para> <para>/ 有关可能的失败代码，请参阅 ISteamNetworkingSockets::SendMessageToConnection。</para>

**参数:**

- `nMessages` (`int`)
- `pMessages` (`SteamNetworkingMessage_t[]`)
- `pOutMessageNumberOrResult` (`long[]`)

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.SendMessages(messages.Length, messages, results);
```

### FlushMessagesOnConnection (静态)

```csharp
EResult FlushMessagesOnConnection(HSteamNetConnection hConn)
```

<para>/ 刷新任何等待在 Nagle 定时器上的消息并立即发送它们。</para> <para>/ （通常意味着现在立即发送。）</para> <para>/</para> <para>/ 如果启用了 Nagle 算法（默认启用），则在调用 SendMessageToConnection 时，</para> <para>/ 消息将被缓冲，直到达到 Nagle 时间限制后再发送，以便将小消息合并到同一个数据包中。</para> <para>/（参见 k_ESteamNetworkingConfig_NagleTime）</para> <para>/</para> <para>/ 返回值：</para> <para>/ k_EResultInvalidParam：无效的连接句柄</para> <para>/ k_EResultInvalidState：连接处于无效状态</para> <para>/ k_EResultNoConnection：连接已终止</para> <para>/ k_EResultIgnored：我们尚未（当前）建立连接，因此此操作无效果。</para>

**参数:**

- `hConn` (`HSteamNetConnection`)

**返回值:** `EResult`

**用法示例:**
```csharp
EResult result = SteamGameServerNetworkingSockets.FlushMessagesOnConnection(hConn);
if (result != EResult.OK) Console.WriteLine(result);
```

### ReceiveMessagesOnConnection (静态)

```csharp
int ReceiveMessagesOnConnection(HSteamNetConnection hConn, IntPtr[] ppOutMessages, int nMaxMessages)
```

<para>/ 从连接中获取下一个可用的消息（若存在）。</para> <para>/ 返回放入您数组中的消息数量，最多为 nMaxMessages 条。</para> <para>/ 如果连接句柄无效，则返回 -1。</para> <para>/</para> <para>/ 数组中返回的消息顺序是重要的。</para> <para>/ 可靠消息将按发送顺序接收（且大小相同——关于这一与流式套接字的细微差别，请参阅 SendMessageToConnection）。</para> <para>/</para> <para>/ 不可靠消息可能会被丢弃，或在彼此之间或与可靠消息之间乱序交付。同一条不可靠消息可能被多次接收。</para> <para>/</para> <para>/ 如果返回了任何消息，您在完成使用后必须对每条消息调用 SteamNetworkingMessage_t::Release() 以释放资源。将该对象保留一段时间（例如放入队列等）是安全的，并且您可以从任意线程调用 Release()。</para>

**参数:**

- `hConn` (`HSteamNetConnection`)
- `ppOutMessages` (`IntPtr[]`)
- `nMaxMessages` (`int`)

**返回值:** `int`

**用法示例:**
```csharp
int received = SteamGameServerNetworkingSockets.ReceiveMessagesOnConnection(hConn, outMessages, 8);
for (int i = 0; i < received; i++) SteamNetworkingMessage_t.Release(outMessages[i]);
```

### GetConnectionInfo (静态)

```csharp
bool GetConnectionInfo(HSteamNetConnection hConn, out SteamNetConnectionInfo_t pInfo)
```

<para>/ 返回连接高级状态的简要信息。</para>

**参数:**

- `hConn` (`HSteamNetConnection`)
- `pInfo` (`out SteamNetConnectionInfo_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamNetConnectionInfo_t info;
bool ok = SteamGameServerNetworkingSockets.GetConnectionInfo(hConn, out info);
```

### GetConnectionRealTimeStatus (静态)

```csharp
EResult GetConnectionRealTimeStatus(HSteamNetConnection hConn, ref SteamNetConnectionRealTimeStatus_t pStatus, int nLanes, ref SteamNetConnectionRealTimeLaneStatus_t pLanes)
```

<para>/ 返回有关连接实时状态及每个通道队列状态的一组少量信息。</para> <para>/</para> <para>/ - 若不需要状态信息，pStatus 可为 NULL（例如：仅关注通道信息）。</para> <para>/ - 调用前，nLanes 指定 pLanes 数组的长度。若不希望接收任何通道数据，该值可设为 0。此值小于配置的总通道数是可以接受的。</para> <para>/ - pLanes 指向一个用于接收通道特定信息的数组。若不需要此类信息，可设为 NULL。</para> <para>/</para> <para>/ 返回值：</para> <para>/ - k_EResultNoConnection：连接句柄无效或连接已关闭。</para> <para>/ - k_EResultInvalidParam：nLanes 参数无效。</para>

**参数:**

- `hConn` (`HSteamNetConnection`)
- `pStatus` (`ref SteamNetConnectionRealTimeStatus_t`)
- `nLanes` (`int`)
- `pLanes` (`ref SteamNetConnectionRealTimeLaneStatus_t`)

**返回值:** `EResult`

**用法示例:**
```csharp
var result = SteamGameServerNetworkingSockets.GetConnectionRealTimeStatus(hConn, ref status, 0, ref laneStatus);
```

### GetDetailedConnectionStatus (静态)

```csharp
int GetDetailedConnectionStatus(HSteamNetConnection hConn, out string pszBuf, int cbBuf)
```

<para>/ 以文本格式返回详细的连接统计信息。适用于</para> <para>/ 导出到日志等用途。</para> <para>/</para> <para>/ 返回值：</para> <para>/ -1：失败（无效的连接句柄）</para> <para>/ 0：成功，已填充缓冲区并以'\0'终止</para> <para>/ >0：缓冲区为 nullptr，或缓冲区过小导致文本被截断。</para> <para>/ 请尝试使用至少 N 字节的缓冲区重试。</para>

**参数:**

- `hConn` (`HSteamNetConnection`)
- `pszBuf` (`out string`)
- `cbBuf` (`int`)

**返回值:** `int`

**用法示例:**
```csharp
string status; int result = SteamGameServerNetworkingSockets.GetDetailedConnectionStatus(hConn, out status, 1024);
Console.WriteLine(status);
```

### GetListenSocketAddress (静态)

```csharp
bool GetListenSocketAddress(HSteamListenSocket hSocket, out SteamNetworkingIPAddr address)
```

<para>/ 返回使用 CreateListenSocketIP 创建的监听套接字所绑定的本地 IP 和端口。</para> <para>/</para> <para>/ IPv6 地址 ::0 表示“任何 IPv4 或 IPv6"</para> <para>/ IPv6 地址 ::ffff:0000:0000 表示“任何 IPv4"</para>

**参数:**

- `hSocket` (`HSteamListenSocket`)
- `address` (`out SteamNetworkingIPAddr`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamNetworkingIPAddr address;
bool ok = SteamGameServerNetworkingSockets.GetListenSocketAddress(hSocket, out address);
```

### CreateSocketPair (静态)

```csharp
bool CreateSocketPair(out HSteamNetConnection pOutConnection1, out HSteamNetConnection pOutConnection2, bool bUseNetworkLoopback, ref SteamNetworkingIdentity pIdentity1, ref SteamNetworkingIdentity pIdentity2)
```

<para>/ 创建一对相互通信的连接，例如环回连接。</para> <para>/ 这对测试非常有用，或者可以让您的客户端/服务器代码在运行本地“服务器”时保持一致的行为。</para> <para>/</para> <para>/ 两个连接将立即进入已连接状态，且不会立即触发任何回调。此后，如果您关闭任一连接，另一个连接将收到回调，其表现与实际通过网络通信完全相同。您必须关闭 *两侧* 才能彻底清理资源！</para> <para>/</para> <para>/ 默认情况下，使用内部缓冲区，完全绕过网络、消息分包、加密、载荷复制等操作。这意味着默认情况下环回数据包不会模拟延迟或丢包。若将 `bUseNetworkLoopback` 参数设为 true，则套接字对将通过本地网络环回设备（127.0.0.1）上的临时端口发送数据包。在此模式下支持模拟延迟和丢包，但需要消耗 CPU 时间进行加解密操作。</para> <para>/</para> <para>/ 如果您希望为任一连接分配特定的身份标识，可传入相应的标识；否则，若传入 `nullptr`，对应连接将采用通用的"localhost"身份。若使用真实网络环回，该身份可能会被解析为实际绑定的环回端口；否则，端口号将为零。</para>

**参数:**

- `pOutConnection1` (`out HSteamNetConnection`)
- `pOutConnection2` (`out HSteamNetConnection`)
- `bUseNetworkLoopback` (`bool`)
- `pIdentity1` (`ref SteamNetworkingIdentity`)
- `pIdentity2` (`ref SteamNetworkingIdentity`)

**返回值:** `bool`

**用法示例:**
```csharp
HSteamNetConnection c1, c2; SteamNetworkingIdentity id1 = default, id2 = default; SteamGameServerNetworkingSockets.CreateSocketPair(out c1, out c2, false, ref id1, ref id2);
```

### ConfigureConnectionLanes (静态)

```csharp
EResult ConfigureConnectionLanes(HSteamNetConnection hConn, int nNumLanes, out int pLanePriorities, out ushort pLaneWeights)
```

/ 在连接上配置多个出站消息流（称为“通道”），并控制它们之间的队头阻塞。同一通道内的消息始终按照入队顺序发送，但不同通道的消息可能以乱序方式发出。每个通道拥有独立的消息编号序列。每条通道发送的第一条消息将被分配编号 1。
/
/ 每个通道都拥有一个“优先级”。数值较高的通道仅在所有数值较低的通道为空时才会被处理。优先级的具体数值大小无关紧要，仅其排序顺序有意义。
/
/ 每个通道还被分配一个权重，该权重控制该通道相对于其他同优先级通道所消耗的带宽的大致比例。（此假设前提是通道处于忙碌状态。空闲的通道不会积累“信用”，以便在后续消息入队时使用。）该值仅在与其他同优先级通道比较时才具有比例意义。对于不同优先级的通道，严格的优先级顺序将生效，它们之间的相对权重无关紧要。因此，若某通道拥有唯一的优先级值，则该通道的权重值无实际意义。
/
/ 示例：3 个通道，优先级分别为 [0, 10, 10]，权重分别为 [(NA), 20, 5]。
/ 发送到第一个通道的消息将总是优先于其他两个通道中的消息发送。由于没有其他优先级为 0 的通道，其权重值无关紧要。其余两个通道将共享带宽，第二个和第三个通道将以大约 4:1 的比例共享带宽。
/ （权重 [NA, 4, 1] 也是等效的。）
/
/ 注意事项：
/ - 撰写本文时，部分代码的性能开销与通道数量呈线性关系，因此请将通道数量保持在绝对最低水平。3 左右是可以接受的；超过 8 则过多。Steam 上的最大通道数为 255，这是一个非常大的数字，并不推荐！如果您是从源代码编译此库，请参阅 STEAMNETWORKINGSOCKETS_MAX_LANES。)
/ - 通道优先级可以是任意整数。其绝对值无关紧要，仅顺序重要。
/ - 权重必须为正数，且由于实现细节的限制，它们被限制为 16 位值。绝对数值大小不重要，仅比例有意义。
/ - 除索引 0 以外的通道发送的消息在传输线上会有少量额外开销，因此为了获得最大的传输效率，无论优先级或权重如何，通道 0 都应作为使用最频繁的通道。
/ - 连接默认只有一个通道。调用此函数并设置 nNumLanes=1 是合法的，但没有意义，因为在这种情况下优先级和权重值均无关紧要。
/ - 您可以随时重新配置连接通道，但不允许减少通道数量。
/ - 重新配置通道可能会重启带宽共享平衡机制。通常您只需在连接初期调用一次此函数，或许在交换几条消息之后即可。
/ - 若要为所有通道分配相同的优先级，可使用 pLanePriorities=NULL。
/ - 若您希望相同优先级的所有通道平均共享带宽（或者没有任何两个通道的优先级值相同，从而使得优先级值无关紧要），可使用 pLaneWeights=NULL。
/ - 优先级和权重决定了消息在传输线上的发送顺序。对消息接收顺序**没有任何保证**！由于丢包、乱序交付以及数据包序列化的细微细节，消息仍可能以轻微乱序的方式被接收！**唯一**的强保证是：**同一通道**上的**可靠**消息将按发送顺序交付。
/ - 每个主机仅为其发送的数据包配置通道；一个方向的通道与该方向相反的通道完全无关。
/
/ 返回值：
/ - k_EResultNoConnection：无效的 hConn
/ - k_EResultInvalidParam：无效的通道数量、权重错误，或尝试减少通道数量
/ - k_EResultInvalidState：连接已断开等
/
/ 另见：
/ SteamNetworkingMessage_t::m_idxLane

**参数:**

- `hConn` (`HSteamNetConnection`)
- `nNumLanes` (`int`)
- `pLanePriorities` (`out int`)
- `pLaneWeights` (`out ushort`)

**返回值:** `EResult`

**用法示例:**
```csharp
int lanePriority; ushort laneWeight; EResult result = SteamGameServerNetworkingSockets.ConfigureConnectionLanes(hConn, 3, out lanePriority, out laneWeight);
```

### GetIdentity (静态)

```csharp
bool GetIdentity(out SteamNetworkingIdentity pIdentity)
```

<para>身份与认证</para> <para>/ 获取分配给此接口的身份。</para> <para>/ 例如，在 Steam 上，这是用户的 SteamID；对于游戏服务器接口，则是分配给该游戏服务器的 SteamID。</para> <para>/ 如果我们尚不知道自身身份（例如游戏服务器尚未登录），则返回 false 并将结果设置为无效身份。（注：在 Steam 上，即使用户未登录 Steam，他们仍知晓自己的 SteamID。）</para>

**参数:**

- `pIdentity` (`out SteamNetworkingIdentity`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamNetworkingIdentity identity;
bool ok = SteamGameServerNetworkingSockets.GetIdentity(out identity);
```

### InitAuthentication (静态)

```csharp
ESteamNetworkingAvailability InitAuthentication()
```

<para>/ 表明我们准备参与经过身份验证的通信。</para> <para>/ 如果我们当前尚未就绪，系统将采取步骤获取必要的</para> <para>/ 证书（包括我方所需的证书以及用于对等方身份验证所需的任何 CA 证书）。</para> <para>/</para> <para>/ 若在程序初始化阶段已知将建立经过身份验证的连接，可在此时调用此函数，以便在尝试建立连接时立即就绪。（请注意，除使用 k_ESteamNetworkingConfig_IP_AllowWithoutAuth 禁用身份验证的普通 UDP 连接外，几乎所有连接都需要身份验证。）若不调用此函数，系统将延迟到实际使用需要这些资源的特性时再进行处理。</para> <para>/</para> <para>/ 若此前尝试失败，也可调用此函数强制重试。一旦尝试并失败，系统不会自动重试。</para> <para>/ 在此方面，系统在首次尝试失败后的行为与首次尝试前相同：无论是尝试进行身份验证通信还是调用此函数，都会触发系统尝试获取必要资源。</para> <para>/</para> <para>/ 可使用 GetAuthenticationStatus 或监听 SteamNetAuthenticationStatus_t 事件以监控状态。</para> <para>/</para> <para>/ 返回 GetAuthenticationStatus 当前将返回的值。</para>

**返回值:** `ESteamNetworkingAvailability`

**用法示例:**
```csharp
ESteamNetworkingAvailability authStatus = SteamGameServerNetworkingSockets.InitAuthentication();
```

### GetAuthenticationStatus (静态)

```csharp
ESteamNetworkingAvailability GetAuthenticationStatus(out SteamNetAuthenticationStatus_t pDetails)
```

<para>/ 查询我们参与认证通信的准备状态。每当此状态发生变化时，都会发布一个 SteamNetAuthenticationStatus_t 回调，</para> <para>/ 但您也可以随时使用此函数进行查询。</para> <para>/</para> <para>/ 返回 SteamNetAuthenticationStatus_t::m_eAvail 的值。如果您仅需此高级别状态，可将 pDetails 传为 NULL；如需获取详细信息，请传入非空指针以接收。</para>

**参数:**

- `pDetails` (`out SteamNetAuthenticationStatus_t`)

**返回值:** `ESteamNetworkingAvailability`

**用法示例:**
```csharp
SteamNetAuthenticationStatus_t details;
var avail = SteamGameServerNetworkingSockets.GetAuthenticationStatus(out details);
```

### CreatePollGroup (静态)

```csharp
HSteamNetPollGroup CreatePollGroup()
```

<para>轮询组。轮询组是一组连接，可被高效地轮询。</para><para>（在我们的 API 中，“轮询”一个连接意味着获取所有待处理的消息。我们实际上没有针对连接*状态*进行“轮询”的 API，如 BSD 套接字所示。）</para><para>/ 创建一个新的轮询组。</para><para>/</para><para>/ 当不再需要使用时，应使用 DestroyPollGroup 销毁该轮询组。</para>

**返回值:** `HSteamNetPollGroup`

**用法示例:**
```csharp
HSteamNetPollGroup pollGroup = SteamGameServerNetworkingSockets.CreatePollGroup();
```

### DestroyPollGroup (静态)

```csharp
bool DestroyPollGroup(HSteamNetPollGroup hPollGroup)
```

<para>/ 销毁通过 CreatePollGroup() 创建的投票组。</para> <para>/</para> <para>/ 如果投票组中存在任何连接，它们将从该组中移除，</para> <para>/ 并处于不再属于任何投票组的状态。</para> <para>/ 若传入无效的投票组句柄，则返回 false。</para>

**参数:**

- `hPollGroup` (`HSteamNetPollGroup`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerNetworkingSockets.DestroyPollGroup(pollGroup);
```

### SetConnectionPollGroup (静态)

```csharp
bool SetConnectionPollGroup(HSteamNetConnection hConn, HSteamNetPollGroup hPollGroup)
```

<para>/ 将连接分配至轮询组。注意，一个连接只能属于单个轮询组。</para> <para>/ 将连接添加至轮询组时，会自动将其从该连接当前所属的任何其他轮询组中移除。</para> <para>/</para> <para>/ 可传入 k_HSteamNetPollGroup_Invalid 以将连接从其当前轮询组中移除，且不将其加入新的轮询组。</para> <para>/</para> <para>/ 若该连接上存在当前待处理的接收消息，系统将尝试按大致符合以下规则的顺序将这些消息添加至该轮询组的待处理消息队列：即假设在收到这些消息时，该连接已是该轮询组成员时所适用的顺序。</para> <para>/</para> <para>/ 如果连接句柄无效，或轮询组句柄无效（且非 k_HSteamNetPollGroup_Invalid），则返回 false。</para>

**参数:**

- `hConn` (`HSteamNetConnection`)
- `hPollGroup` (`HSteamNetPollGroup`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerNetworkingSockets.SetConnectionPollGroup(hConn, hPollGroup);
```

### ReceiveMessagesOnPollGroup (静态)

```csharp
int ReceiveMessagesOnPollGroup(HSteamNetPollGroup hPollGroup, IntPtr[] ppOutMessages, int nMaxMessages)
```

<para>/ 与 ReceiveMessagesOnConnection 相同，但将返回轮询组中任意连接上可用的下一条消息。</para> <para>/ 请检查 SteamNetworkingMessage_t::m_conn 以确认所属连接。（SteamNetworkingMessage_t::m_nConnUserData 也可能有用。）</para> <para>/</para> <para>/ 不同连接间消息的交付顺序通常与完成该消息的最后一次数据包接收顺序一致。但这并非严格保证，特别是在连接被分配至轮询组的同时收到数据包的情况下。</para> <para>/</para> <para>/ 同一连接上的消息交付顺序定义明确，并遵循 ReceiveMessagesOnConnection 中所述相同的保证。</para> <para>/（但消息未按连接分组，因此它们不一定在列表中连续出现；它们可能会与其他连接的消息交错排列。）</para>

**参数:**

- `hPollGroup` (`HSteamNetPollGroup`)
- `ppOutMessages` (`IntPtr[]`)
- `nMaxMessages` (`int`)

**返回值:** `int`

**用法示例:**
```csharp
int msgCount = SteamGameServerNetworkingSockets.ReceiveMessagesOnPollGroup(pollGroup, msgs, msgs.Length);
for (int i = 0; i < msgCount; i++) { /* 处理 msgs[i] */ }
```

### ReceivedRelayAuthTicket (静态)

```csharp
bool ReceivedRelayAuthTicket(IntPtr pvTicket, int cbTicket, out SteamDatagramRelayAuthTicket pOutParsedTicket)
```

连接到托管在数据中心内的专用服务器的客户端，使用由游戏协调器签发的票证。如果您不自行签发票证以限制可尝试连接您服务器的用户，则无需使用这些函数。  
/ 当从后端匹配系统接收到票证时调用此函数。将票证存入持久缓存，并可选择返回解析后的票证内容。  
/  
/ 更多详情请参见 stamdatagram_ticketgen.h。

**参数:**

- `pvTicket` (`IntPtr`)
- `cbTicket` (`int`)
- `pOutParsedTicket` (`out SteamDatagramRelayAuthTicket`)

**返回值:** `bool`

**用法示例:**
```csharp
IntPtr pvTicket = IntPtr.Zero; SteamDatagramRelayAuthTicket parsedTicket;
bool ok = SteamGameServerNetworkingSockets.ReceivedRelayAuthTicket(pvTicket, cbTicket, out parsedTicket);
```

### FindRelayAuthTicketForServer (静态)

```csharp
int FindRelayAuthTicketForServer(ref SteamNetworkingIdentity identityGameServer, int nRemoteVirtualPort, out SteamDatagramRelayAuthTicket pOutParsedTicket)
```

<para>/ 在缓存中搜索用于在指定虚拟端口与服务器通信的票据。</para> <para>/ 若找到，则返回票据过期前的剩余秒数，并可选择性地返回完整的已破解票据。若没有票据则返回 0。</para> <para>/</para> <para>/ 通常，此方法主要用于在调用 ConnectToHostedDedicatedServer 连接托管专用服务器之前，确认是否持有有效票据。</para>

**参数:**

- `identityGameServer` (`ref SteamNetworkingIdentity`)
- `nRemoteVirtualPort` (`int`)
- `pOutParsedTicket` (`out SteamDatagramRelayAuthTicket`)

**返回值:** `int`

**用法示例:**
```csharp
SteamDatagramRelayAuthTicket ticket;
int secondsLeft = SteamGameServerNetworkingSockets.FindRelayAuthTicketForServer(ref identityGameServer, nRemoteVirtualPort, out ticket);
```

### ConnectToHostedDedicatedServer (静态)

```csharp
HSteamNetConnection ConnectToHostedDedicatedServer(ref SteamNetworkingIdentity identityTarget, int nRemoteVirtualPort, int nOptions, SteamNetworkingConfigValue_t[] pOptions)
```

/ 客户端调用此方法以连接托管在 Valve 数据中心指定虚拟端口上的服务器。您必须已将该服务器的票据放入缓存，否则连接尝试将失败！如果您不自行签发票据，则通过 SDR 以自动票据模式连接专用服务器时，请使用 ConnectP2P。（该服务器必须通过调用 CreateListenSocketP2P 进行监听，以便允许此类连接。）
/
/ 您可能会好奇：为何票据存储在缓存中，而不是直接作为参数传入此处？原因是为了增强游戏服务器重连的鲁棒性，即使客户端计算机与 Steam 或中央后端失去连接、应用程序重启或崩溃等情况下也能正常重连。
/
/ 若使用本接口，建议在应用程序初始化时调用 ISteamNetworkingUtils::InitRelayNetworkAccess()。
/
/ 如需设置任何初始配置选项，请在此处传递。有关为何此举优于在创建后立即设置选项的说明，请参阅 SteamNetworkingConfigValue_t。

**参数:**

- `identityTarget` (`ref SteamNetworkingIdentity`)
- `nRemoteVirtualPort` (`int`)
- `nOptions` (`int`)
- `pOptions` (`SteamNetworkingConfigValue_t[]`)

**返回值:** `HSteamNetConnection`

**用法示例:**
```csharp
SteamNetworkingIdentity identityTarget = default;
HSteamNetConnection conn = SteamGameServerNetworkingSockets.ConnectToHostedDedicatedServer(ref identityTarget, 0, 0, null);
```

### GetHostedDedicatedServerPort (静态)

```csharp
ushort GetHostedDedicatedServerPort()
```

<para>托管在 Valve 中继网络已知数据中心内的服务器</para> <para>/ 返回 SDR_LISTEN_PORT 环境变量的值。该端口是您的服务器将监听的 UDP 服务器端口。在生产环境中，此设置将由系统自动为您配置。</para> <para>/</para> <para>/ 在开发环境中，您需要自行设置该变量。有关如何配置开发环境的详细信息，请参阅：</para> <para>/ https://partner.steamgames.com/doc/api/ISteamNetworkingSockets</para>

**返回值:** `ushort`

**用法示例:**
```csharp
ushort listenPort = SteamGameServerNetworkingSockets.GetHostedDedicatedServerPort();
Console.WriteLine(listenPort);
```

### GetHostedDedicatedServerPOPID (静态)

```csharp
SteamNetworkingPOPID GetHostedDedicatedServerPOPID()
```

<para>/ 如果未设置 SDR_LISTEN_PORT，则返回 0。否则，返回服务器运行的数据中心。</para> <para>/ 在非生产环境中，此值将为 k_SteamDatagramPOPID_dev。</para>

**返回值:** `SteamNetworkingPOPID`

**用法示例:**
```csharp
SteamNetworkingPOPID popid = SteamGameServerNetworkingSockets.GetHostedDedicatedServerPOPID();
Console.WriteLine(popid);
```

### GetHostedDedicatedServerAddress (静态)

```csharp
EResult GetHostedDedicatedServerAddress(out SteamDatagramHostedAddress pRouting)
```

<para>/ 返回托管服务器的信息。此信息包含服务器的 PoPID，</para> <para>/ 以及供中继系统用于将流量转发至您服务器的不透明路由信息。</para> <para>/</para> <para>/ 您需要将此信息发送至您的后端服务，并将其嵌入票证（tickets）中，</para> <para>/ 以便中继系统知晓如何将从客户端发出的流量转发到您的服务器。有关详细信息，请参阅 SteamDatagramRelayAuthTicket。</para> <para>/</para> <para>/ 此外请注意，路由信息已包含在 SteamDatagramGameCoordinatorServerLogin 结构中，</para> <para>/ 因此如果可行，建议优先使用 GetGameCoordinatorServerLogin 方法将该信息发送至您的游戏协调器服务，</para> <para>/ 并同时完成安全登录。</para> <para>/</para> <para>/ 成功退出时，返回 k_EResultOK。</para> <para>/</para> <para>/ 失败退出情形：</para> <para>/ - 返回除 k_EResultOK 以外的其他值。</para> <para>/ - k_EResultInvalidState：未配置为监听 SDR（未设置 SDR_LISTEN_SOCKET。）</para> <para>/ - k_EResultPending：尚未获取所需的认证信息。</para> <para>/ （请参见 GetAuthenticationStatus。）如果您通过环境变量预先获取网络配置，则该数据应立即可用。</para> <para>/ - m_data 中将放置一条非本地化的诊断调试消息，说明失败原因。</para> <para>/</para> <para>/ 注意：返回的字节流未经加密。请将其发送至您的后端服务，但切勿直接将其共享给客户端。</para>

**参数:**

- `pRouting` (`out SteamDatagramHostedAddress`)

**返回值:** `EResult`

**用法示例:**
```csharp
EResult result = SteamGameServerNetworkingSockets.GetHostedDedicatedServerAddress(out SteamDatagramHostedAddress routing);
if (result == EResult.OK) Console.WriteLine(routing);
```

### CreateHostedDedicatedServerListenSocket (静态)

```csharp
HSteamListenSocket CreateHostedDedicatedServerListenSocket(int nLocalVirtualPort, int nOptions, SteamNetworkingConfigValue_t[] pOptions)
```

<para>/ 在指定的虚拟端口上创建一个监听套接字。所使用的物理 UDP 端口将由 SDR_LISTEN_PORT 环境变量决定。若未配置 UDP 端口，此调用将失败。</para> <para>/</para> <para>/ 此调用必须通过 SteamGameServerNetworkingSockets() 接口执行。</para> <para>/</para> <para>/ 当您使用票据生成库自行签发票据时，应使用此函数。连接到该虚拟端口的客户端需要一张票据，并且必须使用 ConnectToHostedDedicatedServer 进行连接。</para> <para>/</para> <para>/ 如需设置任何初始配置选项，请在此处传递它们。有关为何优先采用此方式而非在创建后立即设置这些选项，请参阅 SteamNetworkingConfigValue_t。</para>

**参数:**

- `nLocalVirtualPort` (`int`)
- `nOptions` (`int`)
- `pOptions` (`SteamNetworkingConfigValue_t[]`)

**返回值:** `HSteamListenSocket`

**用法示例:**
```csharp
HSteamListenSocket listenSocket = SteamGameServerNetworkingSockets.CreateHostedDedicatedServerListenSocket(7777, 0, null);
```

### GetGameCoordinatorServerLogin (静态)

```csharp
EResult GetGameCoordinatorServerLogin(IntPtr pLoginInfo, out int pcbSignedBlob, IntPtr pBlob)
```

<para>/ 生成一个认证数据块（blob），用于通过 SteamDatagram_ParseHostedServerLogin 函数安全地登录到您的后端服务器。（请参阅</para> <para>/ steamdatagram_gamecoordinator.h）</para> <para>/</para> <para>/ 调用本函数前：</para> <para>/ - 请在 pLoginInfo 中填充应用数据（m_cbAppData 和 m_appData）。其余字段可保持未初始化状态。</para> <para>/ - *pcbSignedBlob 包含 pBlob 指向的缓冲区大小。（该值应至少为 k_cbMaxSteamDatagramGameCoordinatorServerLoginSerialized。）</para> <para>/</para> <para>/ 成功退出时：</para> <para>/ - 返回 k_EResultOK。</para> <para>/ - pLoginInfo 的所有剩余字段均会被填充。</para> <para>/ - *pcbSignedBlob 包含已序列化并写入 pBlob 的数据块的字节数。</para> <para>/</para> <para>/ 失败退出时：</para> <para>/ - 返回非 k_EResultOK 的结果码。</para> <para>/ - k_EResultNotLoggedOn：表示尚未登录。</para> <para>/ - 有关更多可能的失败返回值，请参见 GetHostedDedicatedServerAddress。</para> <para>/ - 将在 pBlob 中放置一条非本地化的诊断调试消息，说明失败原因。</para> <para>/</para> <para>/ 该机制通过使用颁发给当前服务器的证书对 SteamDatagramGameCoordinatorServerLogin 的内容进行签名实现。在开发环境中，若暂无证书亦可正常运作（此时需在 SteamDatagram_ParseHostedServerLogin 中启用不安全的开发登录模式）。否则，必须提供已签名的证书。</para> <para>/</para> <para>/ 注意：此处返回的路由数据块未加密。请将其发送至您的后端服务，切勿直接向客户端分发。</para>

**参数:**

- `pLoginInfo` (`IntPtr`)
- `pcbSignedBlob` (`out int`)
- `pBlob` (`IntPtr`)

**返回值:** `EResult`

**用法示例:**
```csharp
int blobSize = 8192; IntPtr loginInfo = Marshal.AllocHGlobal(256), blob = Marshal.AllocHGlobal(blobSize); EResult result = SteamGameServerNetworkingSockets.GetGameCoordinatorServerLogin(loginInfo, out blobSize, blob);
```

### ConnectP2PCustomSignaling (静态)

```csharp
HSteamNetConnection ConnectP2PCustomSignaling(out ISteamNetworkingConnectionSignaling pSignaling, ref SteamNetworkingIdentity pPeerIdentity, int nRemoteVirtualPort, int nOptions, SteamNetworkingConfigValue_t[] pOptions)
```

<para>使用自定义信令协议转发的连接</para><para>此方法适用于您拥有自己的带外信令/ rendezvous（会合）消息发送方式，且通过双方互信的通道进行传输的场景。</para><para>/ 创建一个 P2P“客户端”连接，该连接通过自定义的会合/信令通道执行信令交互。</para><para>/</para><para>/ pSignaling 指向一个为您此次连接专门创建的新对象。</para><para>/ 该对象必须在使用 Release() 调用前保持有效。一旦您将此对象传递给本函数，所有权即转移至该函数。若函数调用失败，将在函数内部调用 Release()。此外，在调用 Release() 之前，您需要准备好您的对象可能从任何线程被调用！务必确保您的对象是线程安全的！</para><para>/ 同时，请确保方法的调度尽可能迅速执行。</para><para>/</para><para>/ 本函数将立即构造一个处于"connecting"（连接中）状态的连接。随后（可能在当前函数返回前，也可能在另一个线程中），连接将通过调用 ISteamNetworkingConnectionSignaling::SendSignal 开始发送信令消息。</para><para>/</para><para>/ 当远端对等体接受连接时（参见 ISteamNetworkingSignalingRecvContext::OnConnectRequest），它将开始发送信令消息。收到这些消息后，您可以使用 ReceivedP2PCustomSignal 将其传递至该连接。</para><para>/</para><para>/ 如果您已知预期另一端对等体的身份，可将该身份传入以改善调试输出或用于检测错误。若您尚不知晓其身份，可传入 NULL，其身份将在连接握手过程中确立。</para><para>/</para><para>/ 若您使用此功能，很可能需要在应用初始化时调用 ISteamNetworkingUtils::InitRelayNetworkAccess()</para><para>/</para><para>/ 如需设置任何初始配置选项，请在此处传入。有关为何优于在创建后立即设置这些选项的更多信息，请参阅 SteamNetworkingConfigValue_t。</para>

**参数:**

- `pSignaling` (`out ISteamNetworkingConnectionSignaling`)
- `pPeerIdentity` (`ref SteamNetworkingIdentity`)
- `nRemoteVirtualPort` (`int`)
- `nOptions` (`int`)
- `pOptions` (`SteamNetworkingConfigValue_t[]`)

**返回值:** `HSteamNetConnection`

**用法示例:**
```csharp
ISteamNetworkingConnectionSignaling signaling; SteamNetworkingIdentity peerIdentity = default; HSteamNetConnection conn = SteamGameServerNetworkingSockets.ConnectP2PCustomSignaling(out signaling, ref peerIdentity, 0, 0, null);
```

### ReceivedP2PCustomSignal (静态)

```csharp
bool ReceivedP2PCustomSignal(IntPtr pMsg, int cbMsg, out ISteamNetworkingSignalingRecvContext pContext)
```

<para>/ 当自定义信令收到消息时调用。当您的信令通道接收到消息时，应将信封中的任何路由信息保存到上下文对象中，然后将有效载荷传递给此函数。</para> <para>/</para> <para>/ 接下来可能发生几种不同的情况，具体取决于消息类型：</para> <para>/</para> <para>/ - 如果该信号与现有连接关联，则立即处理该信号。如果需要发送任何回复，将通过与该连接关联的 ISteamNetworkingConnectionSignaling 进行分发。</para> <para>/ - 如果该消息代表连接请求（且该请求对于现有连接不是冗余的），则将创建新连接，并调用您上下文对象上的 ReceivedConnectRequest 以确定后续操作。</para> <para>/ - 否则，该消息指向一个不存在（或不再存在）的连接。在此情况下，我们*可能*会调用您上下文对象上的 SendRejectionReply。</para> <para>/</para> <para>/ 无论何种情况，在此函数返回后，我们将不再保存 pContext 或访问它。</para> <para>/</para> <para>/ 如果消息被解析并正常分发，未发生任何异常或可疑情况，则返回 true。如果消息存在问题导致无法正常处理，则返回 false。（调试输出通常包含更多信息。）</para> <para>/</para> <para>/ 如果您预期使用中继连接，则在应用初始化时，您可能需要调用 ISteamNetworkingUtils::InitRelayNetworkAccess()。</para>

**参数:**

- `pMsg` (`IntPtr`)
- `cbMsg` (`int`)
- `pContext` (`out ISteamNetworkingSignalingRecvContext`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerNetworkingSockets.ReceivedP2PCustomSignal(IntPtr.Zero, 0, out var context);
```

### GetCertificateRequest (静态)

```csharp
bool GetCertificateRequest(out int pcbBlob, IntPtr pBlob, out SteamNetworkingErrMsg errMsg)
```

由应用程序提供证书。在 Steam 平台上，我们通常会自动处理所有相关事宜，因此您无需使用这些高级功能。<para>/ 获取描述证书请求的字节数组（blob）。您可以将其发送给游戏协调器。</para><para>/ 调用时，*pcbBlob 应包含缓冲区的大小。成功返回后，它将填入已填充的字节数。您可以传入 pBlob=NULL 以查询所需大小。（保守估计为 512 字节。）</para><para>/</para><para>/ 将该字节数组传递给你的游戏协调器，并调用 SteamDatagram_CreateCert。</para>

**参数:**

- `pcbBlob` (`out int`)
- `pBlob` (`IntPtr`)
- `errMsg` (`out SteamNetworkingErrMsg`)

**返回值:** `bool`

**用法示例:**
```csharp
int pcbBlob; SteamNetworkingErrMsg errMsg; SteamGameServerNetworkingSockets.GetCertificateRequest(out pcbBlob, IntPtr.Zero, out errMsg);
```

### SetCertificate (静态)

```csharp
bool SetCertificate(IntPtr pCertificate, int cbCertificate, out SteamNetworkingErrMsg errMsg)
```

<para>/ 设置证书。证书二进制数据块应为</para> <para>/ SteamDatagram_CreateCert函数的输出。</para>

**参数:**

- `pCertificate` (`IntPtr`)
- `cbCertificate` (`int`)
- `errMsg` (`out SteamNetworkingErrMsg`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamNetworkingErrMsg errMsg;
bool ok = SteamGameServerNetworkingSockets.SetCertificate(certPtr, certSize, out errMsg);
```

### ResetIdentity (静态)

```csharp
void ResetIdentity(ref SteamNetworkingIdentity pIdentity)
```

<para>/ 重置与此实例关联的身份。</para> <para>/ 所有打开的连接都将关闭。任何先前的证书等都将被丢弃。</para> <para>/ 您可以传入希望使用的特定身份，也可以传入 NULL，</para> <para>/ 此时该身份将无效，直到您使用 SetCertificate 设置它。</para> <para>/</para> <para>/ 注意：此功能在 Steam 上实际上不受支持！它被包含在内是为了在其他平台上使用，在这些平台上当前用户可以登出，新用户可以登录。</para>

**参数:**

- `pIdentity` (`ref SteamNetworkingIdentity`)

**用法示例:**
```csharp
SteamNetworkingIdentity identity = default; SteamGameServerNetworkingSockets.ResetIdentity(ref identity);
```

### RunCallbacks (静态)

```csharp
void RunCallbacks()
```

<para>杂项</para> <para>/ 调用为此接口排队的所有回调函数。</para> <para>/ 参见 k_ESteamNetworkingConfig_Callback_ConnectionStatusChanged 等。</para> <para>/</para> <para>/ 如果您正在使用 Steam 的回调分发机制（SteamAPI_RunCallbacks 和 SteamGameserver_RunCallbacks），则无需调用此方法。</para>

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.RunCallbacks();
```

### BeginAsyncRequestFakeIP (静态)

```csharp
bool BeginAsyncRequestFakeIP(int nNumPorts)
```

<para> "FakeIP" 系统。</para> <para> FakeIP 本质上是一个临时的、任意的标识符，碰巧也是一个有效的 IPv4 地址。该系统的目的是便于与现有代码集成，这些代码使用 IPv4 地址来识别主机。</para> <para> FakeIP 地址永远不会实际用于在互联网上发送或接收任何数据包；它纯粹是一个标识符。</para> <para> 设计 FakeIP 地址的目标是（希望）尽可能透明地通过现有代码，同时尽量减少与同一代码中网络（包括互联网和局域网）上可能正在使用的“真实”地址发生冲突的可能性。在撰写此注释时，它们来自 169.254.0.0/16 范围，且端口号始终大于 1024。然而，这可能会发生变化！切勿对这类地址做出假设，否则您的代码未来可能会出错。特别是，您应使用如 ISteamNetworkingUtils::IsFakeIP 之类的函数来判断 IP 地址是否为该系统所使用的“伪造”地址。</para> <para>/ 开始异步分配一个伪 IPv4 地址的过程，其他对等节点可通过该地址通过 P2P 方式联系我们。由此函数返回的 IP 地址对于给定的应用 ID 是全球唯一的。</para> <para>/ nNumPorts 是您希望预留的端口数量。这与为不同类型的流量监听多个 UDP 端口具有相同的作用。由于这些分配来自全局命名空间，因此对您可请求的最大端口数有相对严格的限制。（截至撰写本文时，该限制为 4。）端口分配*不*保证具有任何特定顺序或关系！请勿假设它们是连续的，尽管在实践中这种情况经常发生。</para> <para>/ 如果已有请求正在进行，则返回 false；如果启动了新请求，则返回 true。当请求完成时，将发布一个 SteamNetworkingFakeIPResult_t。</para> <para>/ 对于游戏服务器，您*必须*在初始化 SDK 之后但在开始登录之前调用此函数。Steam 需要提前知晓将使用 FakeIP。在公共 IP 通常出现的所有位置（例如服务器浏览器），都将被 FakeIP 以及索引为 0 的伪端口所替换。该请求实际上会被排队，直到登录完成为止，因此您不能在等待分配完成后再进行登录。除了可以本地检测到的微小失败（例如无效参数）之外，SteamNetworkingFakeIPResult_t 回调（无论成功还是失败）将在我们登录后才会发布。此外，假定 FakeIP 分配对于您的应用程序运行至关重要，因此只有在尝试了*多次*重试后才会报告失败。此过程可能需要几分钟时间。强烈建议将失败视为致命错误。</para> <para>/ 若使用面向连接的（类 TCP）API 进行通信：</para> <para>/ - 服务器使用 CreateListenSocketP2PFakeIP 创建侦听套接字</para> <para>/ - 客户端使用 ConnectByIPAddress 进行连接，并传入 FakeIP 地址。</para> <para>/ - 该连接的行为将主要类似于 P2P 连接。SteamNetConnectionInfo_t 中显示的标识将是 FakeIP 标识，直到我们获知真实身份。随后将显示真实身份。如果 SteamNetConnectionInfo_t::m_addrRemote 有效，则它将是一个经过 NAT 穿透的真实 IPv4 地址；否则将无效。</para> <para>/ 若使用临时的 sendto/recvfrom（类 UDP）API 进行通信，请使用 CreateFakeUDPPort。</para>

**参数:**

- `nNumPorts` (`int`)

**返回值:** `bool`

**用法示例:**
```csharp
bool started = SteamGameServerNetworkingSockets.BeginAsyncRequestFakeIP(2);
if (!started) Console.WriteLine("FakeIP request already in progress or failed to start.");
```

### GetFakeIP (静态)

```csharp
void GetFakeIP(int idxFirstPort, out SteamNetworkingFakeIPResult_t pInfo)
```

/ 返回我们已分配的 FakeIP 和端口（如有）的相关信息，
/ idxFirstPort 当前保留且必须为零。
/ 请务必检查 SteamNetworkingFakeIPResult_t::m_eResult

**参数:**

- `idxFirstPort` (`int`)
- `pInfo` (`out SteamNetworkingFakeIPResult_t`)

**用法示例:**
```csharp
SteamNetworkingFakeIPResult_t info; SteamGameServerNetworkingSockets.GetFakeIP(0, out info); if (info.m_eResult == EResult.k_EResultOK) { }
```

### CreateListenSocketP2PFakeIP (静态)

```csharp
HSteamListenSocket CreateListenSocketP2PFakeIP(int idxFakePort, int nOptions, SteamNetworkingConfigValue_t[] pOptions)
```

<para>/ 创建一个监听套接字，用于侦听发送至我们虚拟 IP (FakeIP) 的对等 (P2P) 连接。</para> <para>/ 对等节点可通过调用 ConnectByIPAddress 向此监听套接字发起连接。</para> <para>/</para> <para>/ idxFakePort 指的是所请求的虚拟端口的*索引*，而非实际端口号。例如，传递 0 以引用预留中的第一个端口。必须在调用 BeginAsyncRequestFakeIP 之后才能调用本方法。但在创建监听套接字之前，无需等待该请求完成。</para>

**参数:**

- `idxFakePort` (`int`)
- `nOptions` (`int`)
- `pOptions` (`SteamNetworkingConfigValue_t[]`)

**返回值:** `HSteamListenSocket`

**用法示例:**
```csharp
HSteamListenSocket listenSocket = SteamGameServerNetworkingSockets.CreateListenSocketP2PFakeIP(0, 0, null);
```

### GetRemoteFakeIPForConnection (静态)

```csharp
EResult GetRemoteFakeIPForConnection(HSteamNetConnection hConn, out SteamNetworkingIPAddr pOutAddr)
```

<para>/ 如果连接是通过"FakeIP"系统发起的，则我们可以获取远程主机的 IP 地址。若该远程主机在建立连接时拥有全局 FakeIP，</para> <para>/ 此函数将返回该全局 IP。否则，将从本地 FakeIP 地址空间中分配一个仅在本局域内唯一的 FakeIP，并予以返回。</para> <para>/</para> <para>/ 本地 FakeIP 的分配策略力求保持一致性。若多次连接到同一远程主机，它们*很可能*返回相同的 FakeIP。</para> <para>/ 但由于命名空间容量有限，此行为无法得到保证。</para> <para>/</para> <para>/ 发生失败时，返回：</para> <para>/ - k_EResultInvalidParam：无效的连接句柄</para> <para>/ - k_EResultIPNotFound：该连接未使用 FakeIP 系统建立</para>

**参数:**

- `hConn` (`HSteamNetConnection`)
- `pOutAddr` (`out SteamNetworkingIPAddr`)

**返回值:** `EResult`

**用法示例:**
```csharp
EResult result = SteamGameServerNetworkingSockets.GetRemoteFakeIPForConnection(hConn, out SteamNetworkingIPAddr remoteAddr);
if (result == EResult.k_EResultOK) Console.WriteLine(remoteAddr);
```

### CreateFakeUDPPort (静态)

```csharp
IntPtr CreateFakeUDPPort(int idxFakeServerPort)
```

<para>/ 获取一个可用作 UDP 端口的接口，用于向 FakeIP 地址发送/接收</para> <para>/ 数据报。此设计旨在便于将现有的基于 UDP 的代码移植到 SDR（安全数据路由）架构。</para> <para>/</para> <para>/ idxFakeServerPort 指通过 BeginAsyncRequestFakeIP 分配的端口索引，用于创建“服务器”端口。您可以在分配完成前调用此函数。然而，在分配成功之前，任何尝试发送数据包的操作都将失败。当对等端收到从此接口发出的数据包时，数据包的源地址将为全局唯一的 FakeIP。如果您多次调用此函数并传入相同的（非负）假端口索引，则返回的是同一个对象；该对象未进行引用计数管理。</para> <para>/</para> <para>/ 若要创建“客户端”端口（例如等效于临时 UDP 端口），请传入 -1。在此情况下，每次调用将返回一个独立的对象。当对等端收到从此接口发出的数据包时，将对等端将从其本地控制的命名空间中为其分配一个 FakeIP。</para>

**参数:**

- `idxFakeServerPort` (`int`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr fakeUdpPort = SteamGameServerNetworkingSockets.CreateFakeUDPPort(-1);
```

