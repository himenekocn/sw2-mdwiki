# 📦 SteamGameServerNetworkingSockets

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### CreateListenSocketIP (静态)

```csharp
HSteamListenSocket CreateListenSocketIP(ref SteamNetworkingIPAddr localAddress, int nOptions, SteamNetworkingConfigValue_t[] pOptions)
```

<para>/ 创建一个“服务器”套接字，用于通过调用 ConnectByIPAddress 来监听客户端连接，使用普通的 UDP（IPv4 或 IPv6）。</para> <para>/</para> <para>/ 您必须选择一个特定的本地端口进行监听，并将其设置在本地地址的端口字段中。</para> <para>/</para> <para>/ 通常，您会将地址的 IP 部分设置为零（SteamNetworkingIPAddr::Clear()）。这意味着您不会绑定到任何特定的本地接口（即与普通套接字代码中的 INADDR_ANY 相同）。此外，如果可能，套接字将以“双栈”模式绑定，这意味着它可以接受 IPv4 和 IPv6 客户端连接。</para> <para>/ 如果您确实希望绑定到特定接口，则将本地地址设置为相应的 IPv4 或 IPv6 IP。</para> <para>/</para> <para>/ 如果您需要设置任何初始配置选项，请在此处传递。有关为什么这比在创建后“立即”设置选项更可取的详细信息，请参阅 SteamNetworkingConfigValue_t。</para> <para>/</para> <para>/ 当客户端尝试连接时，将发布一个 SteamNetConnectionStatusChangedCallback_t。</para> <para>/ 连接将处于连接中状态。</para>

**参数:**

- `localAddress` (`ref SteamNetworkingIPAddr`)
- `nOptions` (`int`)
- `pOptions` (`SteamNetworkingConfigValue_t[]`)

**返回值:** `HSteamListenSocket`

**用法示例:**
```csharp
SteamNetworkingIPAddr addr = default;
addr.m_ip[0] = 0; // 绑定所有接口
addr.m_port = 27015;
var socket = SteamGameServerNetworkingSockets.CreateListenSocketIP(ref addr, 0, null);
```

### ConnectByIPAddress (静态)

```csharp
HSteamNetConnection ConnectByIPAddress(ref SteamNetworkingIPAddr address, int nOptions, SteamNetworkingConfigValue_t[] pOptions)
```

<para>/ 创建一个连接，并开始通过 UDP 与指定 IPv4 或 IPv6 地址上的“服务器”进行通信。远程主机必须使用匹配的 CreateListenSocketIP 调用，在指定端口上监听。</para> <para>/</para> <para>/ 当我们开始连接时，将触发一个 SteamNetConnectionStatusChangedCallback_t 回调，然后在超时或成功连接时再触发另一个回调。</para> <para>/</para> <para>/ 如果服务器未配置任何身份，则其网络地址将是唯一使用的身份。或者，网络主机可以提供带有或不带有有效证书的平台特定身份来验证该身份。（这些详细信息将包含在 SteamNetConnectionStatusChangedCallback_t 中。）是否允许连接由您的应用程序决定。</para> <para>/</para> <para>/ 默认情况下，所有连接都将获得足以防止 casual eavesdropping（ casual 窃听）的基本加密。但请注意，如果没有证书（或通过其他带外机制分发的共享密钥），您将无法知道另一端究竟是谁，因此容易受到中间人攻击。</para> <para>/</para> <para>/ 如果您需要设置任何初始配置选项，请在此处传递。有关为什么这比在创建后“立即”设置选项更可取，请参阅 SteamNetworkingConfigValue_t。</para>

**参数:**

- `address` (`ref SteamNetworkingIPAddr`)
- `nOptions` (`int`)
- `pOptions` (`SteamNetworkingConfigValue_t[]`)

**返回值:** `HSteamNetConnection`

**用法示例:**
```csharp
SteamNetworkingIPAddr addr = new SteamNetworkingIPAddr();
addr.SetIP(127, 0, 0, 1);
SteamGameServerNetworkingSockets.ConnectByIPAddress(ref addr, 0, null);
```

### CreateListenSocketP2P (静态)

```csharp
HSteamListenSocket CreateListenSocketP2P(int nLocalVirtualPort, int nOptions, SteamNetworkingConfigValue_t[] pOptions)
```

<para>/ 与 CreateListenSocketIP 类似，但客户端将使用 ConnectP2P 进行连接。</para> <para>/</para> <para>/ nLocalVirtualPort 指定了客户端如何使用 ConnectP2P 连接到此套接字。应用程序通常只有一个监听套接字；</para> <para>/ 在这种情况下，使用零。如果您需要打开多个监听套接字并让客户端能够连接到其中一个，</para> <para>/ 那么 nLocalVirtualPort 应该是一个较小的整数 (&lt;1000)，并且对您创建的每个监听套接字都是唯一的。</para> <para>/</para> <para>/ 如果您使用此功能，您可能希望在应用程序初始化时调用 ISteamNetworkingUtils::InitRelayNetworkAccess()</para> <para>/。</para> <para>/</para> <para>/ 如果您在已知数据中心中的专用服务器上进行监听，</para> <para>/ 那么您可以使用此函数代替 CreateHostedDedicatedServerListenSocket 来监听，</para> <para>/ 以允许客户端无需凭据即可连接。任何拥有该应用并已登录 Steam 的用户</para> <para>/ 都可以尝试连接到您的服务器。此外，连接尝试可能要求客户端</para> <para>/ 连接到 Steam，这是另一个可能出错的环节。当使用凭据时，一旦获得凭据，</para> <para>/ 即使客户端与 Steam 断开连接或 Steam 离线，客户端也可以连接到您的服务器。</para> <para>/</para> <para>/ 如果您需要设置任何初始配置选项，请在此处传递。有关为什么这比</para> <para>/ 在创建后“立即”设置选项更可取的详细信息，请参阅</para> <para>/ SteamNetworkingConfigValue_t。</para>

**参数:**

- `nLocalVirtualPort` (`int`)
- `nOptions` (`int`)
- `pOptions` (`SteamNetworkingConfigValue_t[]`)

**返回值:** `HSteamListenSocket`

**用法示例:**
```csharp
var listenSocket = SteamGameServerNetworkingSockets.CreateListenSocketP2P(0, 1, null);
```

### ConnectP2P (静态)

```csharp
HSteamNetConnection ConnectP2P(ref SteamNetworkingIdentity identityRemote, int nRemoteVirtualPort, int nOptions, SteamNetworkingConfigValue_t[] pOptions)
```

<para>/ 开始连接到一个使用平台特定标识符标识的对等方。</para> <para>/ 这使用默认的会合服务，该服务取决于平台和库</para> <para>/ 配置。(例如，在 Steam 上，它通过 Steam 后端进行。)</para> <para>/</para> <para>/ 如果需要设置任何初始配置选项，请在此处传递。有关为何这比</para> <para>/ 在创建后“立即”设置选项更可取的详细信息，请参阅</para> <para>/ SteamNetworkingConfigValue_t。</para> <para>/</para> <para>/ 若要使用您自己的信令服务，请参阅：</para> <para>/ - ConnectP2PCustomSignaling</para> <para>/ - k_ESteamNetworkingConfig_Callback_CreateConnectionSignaling</para>

**参数:**

- `identityRemote` (`ref SteamNetworkingIdentity`)
- `nRemoteVirtualPort` (`int`)
- `nOptions` (`int`)
- `pOptions` (`SteamNetworkingConfigValue_t[]`)

**返回值:** `HSteamNetConnection`

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.ConnectP2P(ref identityRemote, 12345, 0, null);
```

### AcceptConnection (静态)

```csharp
EResult AcceptConnection(HSteamNetConnection hConn)
```

<para>/ 接受在监听套接字上收到的传入连接。</para> <para>/</para> <para>/ 当收到连接尝试（可能在交换了一些基本的握手数据包以防止简单的欺骗之后），将创建一个处于 k_ESteamNetworkingConnectionState_Connecting 状态的连接接口对象，并发布一个 SteamNetConnectionStatusChangedCallback_t 回调。此时，您的应用程序必须接受或关闭该连接。（不能忽略它。）</para> <para>/ 接受连接将根据连接类型将其转换为已连接状态或查找路由状态。</para> <para>/</para> <para>/ 您应该在一两秒内采取行动，因为接受连接实际上是向客户端发送回复，通知其已连接。如果您延迟采取行动，从客户端的角度来看，这与网络无响应是一样的，客户端可能会超时连接尝试。换句话说，客户端无法区分由网络问题引起的延迟和由应用程序引起的延迟。</para> <para>/</para> <para>/ 这意味着如果您的应用程序在几秒钟内没有处理回调（例如，在加载地图时），那么在此期间客户端可能会尝试连接并因超时而失败。</para> <para>/</para> <para>/ 如果应用程序没有及时响应连接尝试，并且我们停止接收来自客户端的通信，连接尝试将在本地超时，将连接状态转换为 k_ESteamNetworkingConnectionState_ProblemDetectedLocally。客户端也可能在连接被接受之前关闭连接，并且根据确切的事件序列，也可能转换为 k_ESteamNetworkingConnectionState_ClosedByPeer。</para> <para>/</para> <para>/ 如果句柄无效，则返回 k_EResultInvalidParam。</para> <para>/ 如果连接未处于适当状态，则返回 k_EResultInvalidState。</para> <para>/ （请记住，连接状态可能在通知被发布到队列与被应用程序接收之间发生变化。）</para> <para>/</para> <para>/ 关于连接配置选项的说明。如果您需要设置通过特定监听套接字接受的所有连接通用的任何配置选项，请考虑在监听套接字上设置这些选项，因为此类选项会自动继承。如果您确实需要设置特定于连接的选项，可以在接受连接之前在连接上安全地设置它们。</para>

**参数:**

- `hConn` (`HSteamNetConnection`)

**返回值:** `EResult`

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.AcceptConnection(hConn);
```

### CloseConnection (静态)

```csharp
bool CloseConnection(HSteamNetConnection hPeer, int nReason, string pszDebug, bool bEnableLinger)
```

<para>/ 断开与远程主机的连接并使连接句柄失效。</para> <para>/ 连接上任何未读取的数据都将被丢弃。</para> <para>/</para> <para>/ nReason 是一个应用程序定义的代码，它将在另一端被接收，并（在可能的情况下）记录在后端分析中。该值应来自一个受限范围。（请参阅 ESteamNetConnectionEnd。）如果您不需要向远程主机传达任何信息，并且不希望分析能够区分“正常”连接终止与“异常”终止，您可以传入零，在这种情况下将使用 k_ESteamNetConnectionEnd_App_Generic 的通用值。</para> <para>/</para> <para>/ pszDebug 是一个可选的人类可读诊断字符串，它将在远程主机上被接收，并（在可能的情况下）记录在后端分析中。</para> <para>/</para> <para>/ 如果您希望将套接字置于“延迟关闭”状态，即尝试刷新任何剩余的已发送数据，请使用 bEnableLinger=true。否则，可靠数据不会被刷新。</para> <para>/</para> <para>/ 如果连接已经结束，而您只是要释放连接接口，则原因代码、调试字符串和延迟关闭标志将被忽略。</para>

**参数:**

- `hPeer` (`HSteamNetConnection`)
- `nReason` (`int`)
- `pszDebug` (`string`)
- `bEnableLinger` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.CloseConnection(hPeer, 0, "Graceful shutdown", false);
```

### CloseListenSocket (静态)

```csharp
bool CloseListenSocket(HSteamListenSocket hSocket)
```

<para>/ 销毁一个监听套接字。所有在该监听套接字上等待连接的连接都将被非正常关闭。</para> <para>/</para>

**参数:**

- `hSocket` (`HSteamListenSocket`)

**返回值:** `bool`

**用法示例:**
```csharp
HSteamListenSocket listenSocket = 12345;
bool result = SteamGameServerNetworkingSockets.CloseListenSocket(listenSocket);
```

### SetConnectionUserData (静态)

```csharp
bool SetConnectionUserData(HSteamNetConnection hPeer, long nUserData)
```

<para>/ 设置连接的用户数据。该数据会在以下位置返回</para> <para>/ - 您可以使用 GetConnectionUserData 进行查询。</para> <para>/ - SteamNetworkingmessage_t 结构体中。</para> <para>/ - SteamNetConnectionInfo_t 结构体中。</para> <para>/ (该结构体是 SteamNetConnectionStatusChangedCallback_t 的一个成员 -- 但请参阅下方的警告!!!!)</para> <para>/</para> <para>/ 当连接创建时，是否需要原子性地设置此值？</para> <para>/ 请参阅 k_ESteamNetworkingConfig_ConnectionUserData。</para> <para>/</para> <para>/ 警告：在使用回调结构体中提供的值时，请务必*非常小心*。</para> <para>/ 回调会被排队，您在回调中收到的值是回调被排队时生效的用户数据。</para> <para>/ 如果您不理解这一点，可能会发生微妙的竞态条件！</para> <para>/</para> <para>/ 如果此连接的任何传入消息被排队，用户数据字段会被更新，因此当您接收消息时（例如使用</para> <para>/ ReceiveMessagesOnConnection），它们将始终包含最新的用户数据。因此，与回调相关的棘手竞态条件</para> <para>/ 并不适用于检索消息。</para> <para>/</para> <para>/ 如果句柄无效，则返回 false。</para>

**参数:**

- `hPeer` (`HSteamNetConnection`)
- `nUserData` (`long`)

**返回值:** `bool`

**用法示例:**
```csharp
long userData = 12345;
SteamGameServerNetworkingSockets.SetConnectionUserData(hPeer, userData);
```

### GetConnectionUserData (静态)

```csharp
long GetConnectionUserData(HSteamNetConnection hPeer)
```

<para>/ 获取连接的用户数据。如果句柄无效，</para> <para>/ 或者您未在连接上设置任何用户数据，则返回 -1。</para>

**参数:**

- `hPeer` (`HSteamNetConnection`)

**返回值:** `long`

**用法示例:**
```csharp
long userData = SteamGameServerNetworkingSockets.GetConnectionUserData(hPeer);
Console.WriteLine($"User data: {userData}");
```

### SetConnectionName (静态)

```csharp
void SetConnectionName(HSteamNetConnection hPeer, string pszName)
```

<para>设置连接的名称，主要用于调试</para>

**参数:**

- `hPeer` (`HSteamNetConnection`)
- `pszName` (`string`)

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.SetConnectionName(hPeer, "Player1");
```

### GetConnectionName (静态)

```csharp
bool GetConnectionName(HSteamNetConnection hPeer, out string pszName, int nMaxLen)
```

<para>/ 获取连接名称。如果句柄无效，则返回 false</para>

**参数:**

- `hPeer` (`HSteamNetConnection`)
- `pszName` (`out string`)
- `nMaxLen` (`int`)

**返回值:** `bool`

**用法示例:**
```csharp
string name;
bool result = SteamGameServerNetworkingSockets.GetConnectionName(hPeer, out name, 256);
Console.WriteLine($"Connection name: {name}");
```

### SendMessageToConnection (静态)

```csharp
EResult SendMessageToConnection(HSteamNetConnection hConn, IntPtr pData, uint cbData, int nSendFlags, out long pOutMessageNumber)
```

<para>/ 向指定连接的远程主机发送一条消息。</para> <para>/</para> <para>/ nSendFlags 参数决定了将提供的交付保证、数据应何时被缓冲等。例如 k_nSteamNetworkingSend_Unreliable。</para> <para>/</para> <para>/ 请注意，我们在此处使用的消息语义与标准“流”套接字（SOCK_STREAM）的语义并不完全相同。</para> <para>/ 对于普通的流套接字，数据块之间的边界被认为无关紧要，写入的数据块大小与另一端读取返回的数据块大小不一定匹配。</para> <para>/ 远程主机可能会读取部分数据块，或者数据块可能会被合并。然而，对于此处使用的消息语义，大小将完全匹配。</para> <para>/ 每次发送调用都会与远程主机上的一次成功读取调用一一对应。如果您正在将现有的面向流的代码移植到可靠消息的语义，</para> <para>/ 您的代码应该能正常工作，因为可靠消息的语义比流语义更严格。唯一的注意事项与性能有关：保留消息大小会产生每条消息的开销，</para> <para>/ 因此如果您的代码发送许多小块数据，性能将会受到影响。任何基于流套接字且不写入过小数据块的代码无需任何更改即可正常工作。</para> <para>/</para> <para>/ pOutMessageNumber 是一个可选指针，用于接收分配给消息的消息编号（如果发送成功）。</para> <para>/</para> <para>/ 返回值：</para> <para>/ - k_EResultInvalidParam: 无效的连接句柄，或单个消息过大。</para> <para>/ (请参阅 k_cbMaxSteamNetworkingSocketsMessageSizeSend)</para> <para>/ - k_EResultInvalidState: 连接处于无效状态</para> <para>/ - k_EResultNoConnection: 连接已结束</para> <para>/ - k_EResultIgnored: 您使用了 k_nSteamNetworkingSend_NoDelay，但由于我们尚未准备好发送，消息被丢弃。</para> <para>/ - k_EResultLimitExceeded: 已有太多数据排队等待发送。</para> <para>/ (请参阅 k_ESteamNetworkingConfig_SendBufferSize)</para>

**参数:**

- `hConn` (`HSteamNetConnection`)
- `pData` (`IntPtr`)
- `cbData` (`uint`)
- `nSendFlags` (`int`)
- `pOutMessageNumber` (`out long`)

**返回值:** `EResult`

**用法示例:**
```csharp
long msgNum;
EResult result = SteamGameServerNetworkingSockets.SendMessageToConnection(hConn, dataPtr, (uint)data.Length, k_nSteamNetworkingSend_Unreliable, out msgNum);
```

### SendMessages (静态)

```csharp
void SendMessages(int nMessages, SteamNetworkingMessage_t[] pMessages, long[] pOutMessageNumberOrResult)
```

<para>/ 发送一条或多条消息，且不复制消息负载。</para> <para>/ 这是发送消息最高效的方式。要使用此</para> <para>/ 函数，您必须首先使用</para> <para>/ ISteamNetworkingUtils::AllocateMessage 分配一个消息对象。(不要在栈上声明或自行分配。)</para> <para>/</para> <para>/ 您应该填充消息负载。您可以让它为您分配缓冲区，然后填充负载，</para> <para>/ 或者如果您已经分配了缓冲区，您可以将 m_pData 指向您的缓冲区，并将回调设置为适当的函数</para> <para>/ 来释放它。请注意，如果您使用自己的缓冲区，它必须在回调执行期间保持有效。</para> <para>/ 同时请注意，您的回调可能从任何线程在任何时间被调用（甚至可能在 SendMessages</para> <para>/ 返回之前！），因此它必须是快速且线程安全的。</para> <para>/</para> <para>/ 您还必须填写：</para> <para>/ - m_conn - 要发送消息的连接句柄</para> <para>/ - m_nFlags - k_nSteamNetworkingSend_xxx 标志的位掩码。</para> <para>/</para> <para>/ 所有其他字段目前为保留字段，不应修改。</para> <para>/</para> <para>/ 库将拥有消息结构的所有权。它们可能</para> <para>/ 在任何时候被修改或变为无效，因此您在将它们传递给此函数后</para> <para>/ 不得再读取它们。</para> <para>/</para> <para>/ pOutMessageNumberOrResult 是一个可选数组，它将接收</para> <para>/ 每条消息被分配的消息编号（如果发送成功）。如果发送失败，则将一个负的 EResult</para> <para>/ 值放入数组中。例如，数组将包含</para> <para>/ -k_EResultInvalidState（如果连接处于无效状态）。</para> <para>/ 有关可能的失败代码，请参阅 ISteamNetworkingSockets::SendMessageToConnection。</para>

**参数:**

- `nMessages` (`int`)
- `pMessages` (`SteamNetworkingMessage_t[]`)
- `pOutMessageNumberOrResult` (`long[]`)

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.SendMessages(1, messages, outMessageNumbers);
```

### FlushMessagesOnConnection (静态)

```csharp
EResult FlushMessagesOnConnection(HSteamNetConnection hConn)
```

<para>/ 刷新所有等待 Nagle 计时器的消息并将其发送</para> <para>/ 在下一次传输机会时（通常意味着立即）。</para> <para>/</para> <para>/ 如果 Nagle 已启用（默认开启），则在调用</para> <para>/ SendMessageToConnection 时，消息将被缓冲，在发送前最多等待 Nagle 时间，</para> <para>/ 以将小消息合并到同一个数据包中。</para> <para>/ (参见 k_ESteamNetworkingConfig_NagleTime)</para> <para>/</para> <para>/ 返回值：</para> <para>/ k_EResultInvalidParam: 无效的连接句柄</para> <para>/ k_EResultInvalidState: 连接处于无效状态</para> <para>/ k_EResultNoConnection: 连接已结束</para> <para>/ k_EResultIgnored: 我们尚未连接，因此此操作无效。</para>

**参数:**

- `hConn` (`HSteamNetConnection`)

**返回值:** `EResult`

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.FlushMessagesOnConnection(hConn);
```

### ReceiveMessagesOnConnection (静态)

```csharp
int ReceiveMessagesOnConnection(HSteamNetConnection hConn, IntPtr[] ppOutMessages, int nMaxMessages)
```

<para>/ 从连接中获取下一个可用的消息（如果有的话）。</para> <para>/ 返回返回到数组中的消息数量，最多为 nMaxMessages。</para> <para>/ 如果连接句柄无效，则返回 -1。</para> <para>/</para> <para>/ 数组中返回的消息顺序是相关的。</para> <para>/ 可靠消息将按照其发送的顺序接收（并且具有相同的尺寸——有关此与流套接字的细微差异，请参阅 SendMessageToConnection）。</para> <para>/</para> <para>/ 不可靠消息可能会被丢弃，或者相对于彼此或相对于可靠消息乱序交付。同一条不可靠消息可能会被多次接收。</para> <para>/</para> <para>/ 如果有任何消息被返回，您必须在处理完它们后对每个消息调用 SteamNetworkingMessage_t::Release() 以释放资源。将对象保持存活一小段时间（例如将其放入某个队列等）是安全的，并且您可以从任何线程调用 Release()。</para>

**参数:**

- `hConn` (`HSteamNetConnection`)
- `ppOutMessages` (`IntPtr[]`)
- `nMaxMessages` (`int`)

**返回值:** `int`

**用法示例:**
```csharp
IntPtr[] messages = new IntPtr[10];
int count = SteamGameServerNetworkingSockets.ReceiveMessagesOnConnection(hConn, messages, 10);
for (int i = 0; i < count; i++) { messages[i].Release(); }
```

### GetConnectionInfo (静态)

```csharp
bool GetConnectionInfo(HSteamNetConnection hConn, out SteamNetConnectionInfo_t pInfo)
```

<para>/ 返回有关连接高级状态的基本信息。</para>

**参数:**

- `hConn` (`HSteamNetConnection`)
- `pInfo` (`out SteamNetConnectionInfo_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.GetConnectionInfo(hConn, out var pInfo);
Console.WriteLine($"Connection state: {pInfo.m_eState}");
```

### GetConnectionRealTimeStatus (静态)

```csharp
EResult GetConnectionRealTimeStatus(HSteamNetConnection hConn, ref SteamNetConnectionRealTimeStatus_t pStatus, int nLanes, ref SteamNetConnectionRealTimeLaneStatus_t pLanes)
```

<para>/ 返回有关连接实时状态和每个车道队列状态的一小部分信息。</para> <para>/</para> <para>/ - 如果不需要该信息（例如，您只对车道信息感兴趣），则 pStatus 可能为 NULL。</para> <para>/ - 在入口处，nLanes 指定 pLanes 数组的长度。如果不需要接收任何车道数据，则可以为 0。</para> <para>/ 这可以小于已配置车道的总数。</para> <para>/ - pLanes 指向一个将接收特定车道信息的数组。如果不需要此信息，则可以为 NULL。</para> <para>/</para> <para>/ 返回值：</para> <para>/ - k_EResultNoConnection - 连接句柄无效或连接已关闭。</para> <para>/ - k_EResultInvalidParam - nLanes 参数无效</para>

**参数:**

- `hConn` (`HSteamNetConnection`)
- `pStatus` (`ref SteamNetConnectionRealTimeStatus_t`)
- `nLanes` (`int`)
- `pLanes` (`ref SteamNetConnectionRealTimeLaneStatus_t`)

**返回值:** `EResult`

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.GetConnectionRealTimeStatus(hConn, ref status, 1, ref laneStatus);
```

### GetDetailedConnectionStatus (静态)

```csharp
int GetDetailedConnectionStatus(HSteamNetConnection hConn, out string pszBuf, int cbBuf)
```

<para>/ 以文本格式返回详细的连接统计信息。可用于</para> <para>/ 转储到日志等场景。</para> <para>/</para> <para>/ 返回值：</para> <para>/ -1 失败（连接句柄无效）</para> <para>/ 0 成功，您的缓冲区已填充并以 '\0' 结尾</para> <para>/ &gt;0 您的缓冲区为 nullptr，或者缓冲区太小导致文本被截断。</para> <para>/ 请尝试使用至少 N 字节大小的缓冲区再次调用。</para>

**参数:**

- `hConn` (`HSteamNetConnection`)
- `pszBuf` (`out string`)
- `cbBuf` (`int`)

**返回值:** `int`

**用法示例:**
```csharp
string status;
int result = SteamGameServerNetworkingSockets.GetDetailedConnectionStatus(hConn, out status, 256);
```

### GetListenSocketAddress (静态)

```csharp
bool GetListenSocketAddress(HSteamListenSocket hSocket, out SteamNetworkingIPAddr address)
```

<para>/ 返回使用 CreateListenSocketIP 创建的监听套接字所绑定的本地 IP 和端口。</para> <para>/</para> <para>/ IPv6 地址 ::0 表示“任意 IPv4 或 IPv6”</para> <para>/ IPv6 地址 ::ffff:0000:0000 表示“任意 IPv4”</para>

**参数:**

- `hSocket` (`HSteamListenSocket`)
- `address` (`out SteamNetworkingIPAddr`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.GetListenSocketAddress(hSocket, out var address);
```

### CreateSocketPair (静态)

```csharp
bool CreateSocketPair(out HSteamNetConnection pOutConnection1, out HSteamNetConnection pOutConnection2, bool bUseNetworkLoopback, ref SteamNetworkingIdentity pIdentity1, ref SteamNetworkingIdentity pIdentity2)
```

<para>/ 创建一对相互通信的连接，例如回环连接。</para> <para>/ 这对于测试非常有用，或者即使您正在运行本地“服务器”，也能使您的客户端/服务器代码正常工作。</para> <para>/</para> <para>/ 这两个连接将立即进入已连接状态，并且不会立即发布任何回调。此后，如果您关闭任一连接，另一连接</para> <para>/ 将收到一个回调，就像它们通过网络通信一样。您必须</para> <para>/ 关闭*两端*才能完全清理资源！</para> <para>/</para> <para>/ 默认情况下，使用内部缓冲区，完全绕过网络、将消息拆分为数据包、加密、复制有效载荷等。这意味着默认情况下，</para> <para>/ 回环数据包不会模拟延迟或丢包。如果为 bUseNetworkLoopback 传入 true，</para> <para>/ 将导致套接字对通过本地网络回环设备（127.0.0.1）</para> <para>/ 在临时端口上发送数据包。在这种情况下，支持模拟延迟和丢包，并且会消耗 CPU 时间</para> <para>/ 来进行加密和解密。</para> <para>/</para> <para>/ 如果您希望为任一连接分配特定身份，可以传入特定</para> <para>/ 身份。否则，如果传入 nullptr，相应的连接将采用通用的</para> <para>/ “localhost”身份。如果使用真实的网络回环，这可能会被转换为</para> <para>/ 实际绑定的回环端口。否则，端口将为零。</para>

**参数:**

- `pOutConnection1` (`out HSteamNetConnection`)
- `pOutConnection2` (`out HSteamNetConnection`)
- `bUseNetworkLoopback` (`bool`)
- `pIdentity1` (`ref SteamNetworkingIdentity`)
- `pIdentity2` (`ref SteamNetworkingIdentity`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.CreateSocketPair(out HSteamNetConnection conn1, out HSteamNetConnection conn2, false, ref identity1, ref identity2);
```

### ConfigureConnectionLanes (静态)

```csharp
EResult ConfigureConnectionLanes(HSteamNetConnection hConn, int nNumLanes, out int pLanePriorities, out ushort pLaneWeights)
```

<para>/ 在连接上配置多个出站消息流（“通道”），并</para> <para>/ 控制它们之间的队头阻塞。给定通道内的消息</para> <para>/ 始终按照其排队顺序发送，但来自不同</para> <para>/ 通道的消息可能以乱序发送。每个通道都有其自己的消息编号</para> <para>/ 序列。每个通道上发送的第一条消息将被分配数字 1。</para> <para>/</para> <para>/ 每个通道都有一个“优先级”。优先级数值更高的通道</para> <para>/ 仅在所有优先级数值更低的通道都为空时才会被处理。优先级</para> <para>/ 值的大小并不重要，只有它们的排序顺序重要。</para> <para>/</para> <para>/ 每个通道还被分配一个权重，该权重控制该通道相对于其他相同优先级</para> <para>/ 通道所消耗的带宽的大致比例。（这是假设通道保持繁忙。空闲的通道</para> <para>/ 不会累积“信用”以在消息排队后使用。）</para> <para>/ 该值仅在与具有相同优先级的其他通道进行比较时才有意义。对于不同优先级的通道，</para> <para>/ 严格的优先级顺序将占主导地位，它们之间的权重相对值则无关紧要。</para> <para>/ 因此，如果一个通道具有唯一的优先级值，则该通道的权重值</para> <para>/ 就无关紧要。</para> <para>/</para> <para>/ 示例：3 个通道，优先级为 [ 0, 10, 10 ]，权重为 [ (NA), 20, 5 ]。</para> <para>/ 在第一个通道上发送的消息将始终在其他两个通道的消息之前发送。</para> <para>/ 其权重值无关紧要，因为没有其他优先级为 0 的通道。其他两个通道将共享带宽，</para> <para>/ 第二个和第三个通道将以大约 4:1 的比例共享带宽。</para> <para>/ （权重 [ NA, 4, 1 ] 是等效的。）</para> <para>/</para> <para>/ 注意事项：</para> <para>/ - 在撰写本文时，一些代码的性能成本与通道数量成正比，</para> <para>/ 因此请将通道数量保持在绝对最小值。3 个左右是合适的；</para> <para>/ &gt;8 就很多了。Steam 上的最大通道数为 255，</para> <para>/ 这是一个非常大的数字，不推荐！如果您正在从源代码编译此</para> <para>/ 库，请参阅 STEAMNETWORKINGSOCKETS_MAX_LANES。）</para> <para>/ - 通道优先级值可以是任何整数。其绝对值无关紧要，</para> <para>/ 只有顺序重要。</para> <para>/ - 权重必须为正数，并且由于实现细节，它们被限制</para> <para>/ 为 16 位值。绝对大小无关紧要，只要比例正确即可。</para> <para>/ - 在非 0 的通道索引上发送的消息在网络上会有少量开销，</para> <para>/ 因此为了实现最大的网络效率，通道 0 应该是“最常用”的通道，</para> <para>/ 无论优先级或权重如何。</para> <para>/ - 连接默认只有一个通道。使用 nNumLanes=1 调用此函数是合法的，</para> <para>/ 但没有意义，因为在这种情况下优先级和权重值都无关紧要。</para> <para>/ - 您可以随时重新配置连接通道，但不允许减少通道数量。</para> <para>/ - 重新配置通道可能会重启任何带宽共享平衡。通常您</para> <para>/ 会在连接开始时调用此函数一次，可能在交换了几条消息之后。</para> <para>/ - 若要为所有通道分配相同的优先级，您可以使用 pLanePriorities=NULL。</para> <para>/ - 如果您希望所有具有相同优先级的通道平等共享带宽（或</para> <para>/ 如果没有两个通道具有相同的优先级值，因此优先级值</para> <para>/ 无关紧要），您可以使用 pLaneWeights=NULL</para> <para>/ - 优先级和权重决定了消息在网络上发送的顺序。</para> <para>/ 消息接收的顺序没有任何保证！由于数据包</para> <para>/ 丢失、乱序交付以及数据包序列化的微妙细节，消息</para> <para>/ 仍可能以轻微的乱序接收！唯一的强保证是</para> <para>/

**参数:**

- `hConn` (`HSteamNetConnection`)
- `nNumLanes` (`int`)
- `pLanePriorities` (`out int`)
- `pLaneWeights` (`out ushort`)

**返回值:** `EResult`

**用法示例:**
```csharp
int[] priorities = { 0, 10, 10 };
ushort[] weights = { 0, 20, 5 };
SteamGameServerNetworkingSockets.ConfigureConnectionLanes(hConn, 3, out int pLanePriorities, out ushort pLaneWeights);
```

### GetIdentity (静态)

```csharp
bool GetIdentity(out SteamNetworkingIdentity pIdentity)
```

<para> 身份与认证</para> <para>/ 获取分配给此接口的身份。</para> <para>/ 例如，在 Steam 上，这是用户的 SteamID；对于游戏服务器接口，则是分配给</para> <para>/ 游戏服务器的 SteamID。如果尚未知晓我们的身份，则返回 false 并将结果设置为无效身份。</para> <para>/（例如，GameServer 尚未登录。在 Steam 上，即使用户未登录 Steam，他们也会知道自己的 SteamID。）</para>

**参数:**

- `pIdentity` (`out SteamNetworkingIdentity`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.GetIdentity(out var identity);
Console.WriteLine(identity);
```

### InitAuthentication (静态)

```csharp
ESteamNetworkingAvailability InitAuthentication()
```

<para>/ 指示我们希望准备好参与经过身份验证的通信。</para> <para>/ 如果我们当前尚未准备就绪，则会采取措施获取必要的</para> <para>/ 证书。（这包括我们自己的证书，以及用于验证对等方的任何 CA 证书</para> <para>/ 所需的证书。）</para> <para>/</para> <para>/ 如果您知道将要建立经过身份验证的连接，可以在程序初始化时调用此函数，</para> <para>/ 以便在尝试这些连接时我们能立即准备就绪。（请注意，几乎所有连接都需要</para> <para>/ 身份验证，除非通过 k_ESteamNetworkingConfig_IP_AllowWithoutAuth 禁用了</para> <para>/ 身份验证的普通 UDP 连接。）如果您不调用此函数，我们将等到需要这些</para> <para>/ 资源的功能被使用时再进行准备。</para> <para>/</para> <para>/ 如果发生失败，您也可以调用此函数以强制重试。</para> <para>/ 一旦我们尝试并失败，将不会自动重试。</para> <para>/ 在这方面，系统在尝试失败后的行为与第一次尝试前相同：</para> <para>/ 尝试进行经过身份验证的通信或调用此函数将促使系统尝试获取必要的资源。</para> <para>/</para> <para>/ 您可以使用 GetAuthenticationStatus 或监听 SteamNetAuthenticationStatus_t</para> <para>/ 来监控状态。</para> <para>/</para> <para>/ 返回 GetAuthenticationStatus 将返回的当前值。</para>

**返回值:** `ESteamNetworkingAvailability`

**用法示例:**
```csharp
ESteamNetworkingAvailability status = SteamGameServerNetworkingSockets.InitAuthentication();
```

### GetAuthenticationStatus (静态)

```csharp
ESteamNetworkingAvailability GetAuthenticationStatus(out SteamNetAuthenticationStatus_t pDetails)
```

<para>/ 查询我们参与身份验证通信的准备状态。当此状态发生任何变化时，</para> <para>/ 都会发布一个 SteamNetAuthenticationStatus_t 回调，</para> <para>/ 但您可以使用此函数随时查询它。</para> <para>/</para> <para>/ 返回 SteamNetAuthenticationStatus_t::m_eAvail 的值。如果您只需要</para> <para>/ 这个高级别状态，可以将 pDetails 传入 NULL。如果您需要更详细的</para> <para>/ 信息，请传入非 NULL 以接收它们。</para>

**参数:**

- `pDetails` (`out SteamNetAuthenticationStatus_t`)

**返回值:** `ESteamNetworkingAvailability`

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.GetAuthenticationStatus(out var status);
Console.WriteLine($"Auth status: {status.m_eAvail}");
```

### CreatePollGroup (静态)

```csharp
HSteamNetPollGroup CreatePollGroup()
```

<para>轮询组。轮询组是一组可以高效轮询的连接。</para> <para>（在我们的API中，“轮询”一个连接意味着检索所有待处理的消息。实际上，我们没有用于“轮询”连接*状态*的API，例如BSD套接字。）</para> <para>/ 创建一个新的轮询组。</para> <para>/</para> <para>/ 当您使用完轮询组后，应通过 DestroyPollGroup 销毁它。</para>

**返回值:** `HSteamNetPollGroup`

**用法示例:**
```csharp
HSteamNetPollGroup pollGroup = SteamGameServerNetworkingSockets.CreatePollGroup();
```

### DestroyPollGroup (静态)

```csharp
bool DestroyPollGroup(HSteamNetPollGroup hPollGroup)
```

<para>/ 销毁通过 CreatePollGroup() 创建的轮询组。</para> <para>/</para> <para>/ 如果轮询组中存在任何连接，它们将被从该组中移除，</para> <para>/ 并处于不属于任何轮询组的状态。</para> <para>/ 如果传入无效的轮询组句柄，则返回 false。</para>

**参数:**

- `hPollGroup` (`HSteamNetPollGroup`)

**返回值:** `bool`

**用法示例:**
```csharp
HSteamNetPollGroup pollGroup = ...; // 假设已通过 CreatePollGroup 创建
bool result = SteamGameServerNetworkingSockets.DestroyPollGroup(pollGroup);
```

### SetConnectionPollGroup (静态)

```csharp
bool SetConnectionPollGroup(HSteamNetConnection hConn, HSteamNetPollGroup hPollGroup)
```

<para>/ 将一个连接分配到一个轮询组。请注意，一个连接只能属于一个</para> <para>/ 轮询组。将一个连接添加到轮询组会隐式地将其从</para> <para>/ 它所属的任何其他轮询组中移除。</para> <para>/</para> <para>/ 你可以传入 k_HSteamNetPollGroup_Invalid 来将一个连接从其当前</para> <para>/ 轮询组中移除，而不将其添加到新的轮询组。</para> <para>/</para> <para>/ 如果连接上当前有待处理的已接收消息，则会尝试将它们添加到轮询组的</para> <para>/ 消息队列中，顺序大致与如果连接在接收消息时已经属于该轮询组</para> <para>/ 时所适用的顺序相同。</para> <para>/</para> <para>/ 如果连接句柄无效，或者轮询组句柄</para> <para>/ 无效（且不是 k_HSteamNetPollGroup_Invalid），则返回 false。</para>

**参数:**

- `hConn` (`HSteamNetConnection`)
- `hPollGroup` (`HSteamNetPollGroup`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.SetConnectionPollGroup(hConn, k_HSteamNetPollGroup_Invalid);
```

### ReceiveMessagesOnPollGroup (静态)

```csharp
int ReceiveMessagesOnPollGroup(HSteamNetPollGroup hPollGroup, IntPtr[] ppOutMessages, int nMaxMessages)
```

<para>/ 与 ReceiveMessagesOnConnection 类似，但会返回轮询组中任意连接上可用的下一条消息。</para> <para>/ 通过检查 SteamNetworkingMessage_t::m_conn 来确定是哪个连接。</para> <para>/ (SteamNetworkingMessage_t::m_nConnUserData 也可能有用。)</para> <para>/</para> <para>/ 不同连接之间消息的投递顺序通常与完成消息的最后一个数据包的接收顺序相匹配。</para> <para>/ 但这并非强保证，尤其是在连接被分配到轮询组时立即接收数据包的情况下。</para> <para>/</para> <para>/ 同一连接上消息的投递顺序是明确定义的，并且与 ReceiveMessagesOnConnection 中提到的保证相同。</para> <para>/ (但消息不会按连接分组，因此它们在列表中不一定会连续出现；可能会与其他连接的消息交错。)</para>

**参数:**

- `hPollGroup` (`HSteamNetPollGroup`)
- `ppOutMessages` (`IntPtr[]`)
- `nMaxMessages` (`int`)

**返回值:** `int`

**用法示例:**
```csharp
IntPtr[] messages = new IntPtr[10];
int count = SteamGameServerNetworkingSockets.ReceiveMessagesOnPollGroup(hPollGroup, messages, 10);
```

### ReceivedRelayAuthTicket (静态)

```csharp
bool ReceivedRelayAuthTicket(IntPtr pvTicket, int cbTicket, out SteamDatagramRelayAuthTicket pOutParsedTicket)
```

<para> 客户端通过游戏协调器（Game Coordinator）颁发的票据连接到数据中心托管的专用服务器。</para> <para> 如果您不颁发自己的票据来限制谁能尝试连接到您的服务器，那么您将不会使用这些函数。</para> <para>/ 当您从后端/匹配系统接收到票据时调用此函数。将票据存入持久缓存，并可选择返回已解析的票据。</para> <para>/</para> <para>/ 更多详情请参阅 stamdatagram_ticketgen.h。</para>

**参数:**

- `pvTicket` (`IntPtr`)
- `cbTicket` (`int`)
- `pOutParsedTicket` (`out SteamDatagramRelayAuthTicket`)

**返回值:** `bool`

**用法示例:**
```csharp
IntPtr ticketPtr = Marshal.AllocHGlobal(1024); // 假设票据数据已填充
SteamGameServerNetworkingSockets.ReceivedRelayAuthTicket(ticketPtr, 1024, out var parsedTicket);
```

### FindRelayAuthTicketForServer (静态)

```csharp
int FindRelayAuthTicketForServer(ref SteamNetworkingIdentity identityGameServer, int nRemoteVirtualPort, out SteamDatagramRelayAuthTicket pOutParsedTicket)
```

<para>/ 在缓存中搜索用于与指定虚拟端口上的服务器通信的票据。</para> <para>/ 如果找到，则返回票据到期前的秒数，并可选择性地</para> <para>/ 返回完整的破解票据。如果没有票据，则返回 0。</para> <para>/</para> <para>/ 通常，在调用 ConnectToHostedDedicatedServer 连接到服务器之前，</para> <para>/ 使用此方法确认您拥有票据是很有用的。</para>

**参数:**

- `identityGameServer` (`ref SteamNetworkingIdentity`)
- `nRemoteVirtualPort` (`int`)
- `pOutParsedTicket` (`out SteamDatagramRelayAuthTicket`)

**返回值:** `int`

**用法示例:**
```csharp
int secondsLeft = SteamGameServerNetworkingSockets.FindRelayAuthTicketForServer(ref identityGameServer, 27015, out SteamDatagramRelayAuthTicket ticket);
```

### ConnectToHostedDedicatedServer (静态)

```csharp
HSteamNetConnection ConnectToHostedDedicatedServer(ref SteamNetworkingIdentity identityTarget, int nRemoteVirtualPort, int nOptions, SteamNetworkingConfigValue_t[] pOptions)
```

<para>/ 客户端调用，用于连接到托管在 Valve 数据中心的指定虚拟端口上的服务器。</para> <para>/ 您必须已将此服务器的票证放入缓存，否则此连接尝试将失败！如果您不自行发放票证，</para> <para>/ 则要通过 SDR 在自动票证模式下连接到专用服务器，请使用 ConnectP2P。（服务器必须</para> <para>/ 通过使用 CreateListenSocketP2P 进行监听来配置为允许此类型的连接。）</para> <para>/</para> <para>/ 您可能会疑惑为什么票证存储在缓存中，而不是直接作为参数传递。原因是为了</para> <para>/ 使与游戏服务器的重新连接更加健壮，即使客户端计算机与 Steam 或中央后端断开</para> <para>/ 连接，或应用程序重新启动或崩溃等。</para> <para>/</para> <para>/ 如果您使用此功能，您可能希望在应用程序初始化时调用 ISteamNetworkingUtils::InitRelayNetworkAccess()</para> <para>/</para> <para>/ 如果需要设置任何初始配置选项，请在此处传递。有关为何这比在创建后</para> <para>/ “立即”设置选项更可取的详细信息，请参阅 SteamNetworkingConfigValue_t。</para>

**参数:**

- `identityTarget` (`ref SteamNetworkingIdentity`)
- `nRemoteVirtualPort` (`int`)
- `nOptions` (`int`)
- `pOptions` (`SteamNetworkingConfigValue_t[]`)

**返回值:** `HSteamNetConnection`

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.ConnectToHostedDedicatedServer(ref identityTarget, 12345, 0, null);
```

### GetHostedDedicatedServerPort (静态)

```csharp
ushort GetHostedDedicatedServerPort()
```

<para>由 Valve 中继网络已知的数据中心托管的服务器</para> <para>/ 返回 SDR_LISTEN_PORT 环境变量的值。这是</para> <para>/ 你的服务器将监听的 UDP 服务器。这将在</para> <para>/ 生产环境中为你自动配置。</para> <para>/</para> <para>/ 在开发环境中，你需要自行设置。请参阅</para> <para>/ https://partner.steamgames.com/doc/api/ISteamNetworkingSockets</para> <para>/ 了解有关如何配置开发环境的更多信息。</para>

**返回值:** `ushort`

**用法示例:**
```csharp
ushort port = SteamGameServerNetworkingSockets.GetHostedDedicatedServerPort();
Console.WriteLine($"Hosted server port: {port}");
```

### GetHostedDedicatedServerPOPID (静态)

```csharp
SteamNetworkingPOPID GetHostedDedicatedServerPOPID()
```

<para>/ 如果未设置 SDR_LISTEN_PORT，则返回 0。否则，返回服务器运行的数据中心。</para> <para>/ 在非生产环境中，此值将为 k_SteamDatagramPOPID_dev。</para>

**返回值:** `SteamNetworkingPOPID`

**用法示例:**
```csharp
var popid = SteamGameServerNetworkingSockets.GetHostedDedicatedServerPOPID();
```

### GetHostedDedicatedServerAddress (静态)

```csharp
EResult GetHostedDedicatedServerAddress(out SteamDatagramHostedAddress pRouting)
```

<para>/ 返回有关托管服务器的信息。此信息包含服务器的 PoPID，</para> <para>/ 以及中继可用于将流量发送到您服务器的透明路由信息。</para> <para>/</para> <para>/ 您需要将此信息发送到您的后端，并将其放入票据中，</para> <para>/ 以便中继知道如何将客户端的流量转发到您的服务器。有关更多信息，请参阅 SteamDatagramRelayAuthTicket。</para> <para>/</para> <para>/ 另外，请注意路由信息包含在 SteamDatagramGameCoordinatorServerLogin 中，</para> <para>/ 因此如果可能，建议使用 GetGameCoordinatorServerLogin 将此信息</para> <para>/ 发送到您的游戏协调器服务，并同时进行安全登录。</para> <para>/</para> <para>/ 成功退出时，返回 k_EResultOK。</para> <para>/</para> <para>/ 非成功退出：</para> <para>/ - 返回除 k_EResultOK 之外的值。</para> <para>/ - k_EResultInvalidState：我们未配置为侦听 SDR（SDR_LISTEN_SOCKET</para> <para>/ 未设置。）</para> <para>/ - k_EResultPending：我们尚未（尚未）拥有所需的身份验证信息。</para> <para>/ （请参阅 GetAuthenticationStatus。）如果您使用环境变量预取</para> <para>/ 网络配置，此数据应始终立即可用。</para> <para>/ - 一个非本地化的诊断调试消息将被放置在 m_data 中，描述</para> <para>/ 失败的原因。</para> <para>/</para> <para>/ 注意：返回的 blob 未加密。请将其发送到您的后端，但不要</para> <para>/ 直接与客户端共享。</para>

**参数:**

- `pRouting` (`out SteamDatagramHostedAddress`)

**返回值:** `EResult`

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.GetHostedDedicatedServerAddress(out var routing);
```

### CreateHostedDedicatedServerListenSocket (静态)

```csharp
HSteamListenSocket CreateHostedDedicatedServerListenSocket(int nLocalVirtualPort, int nOptions, SteamNetworkingConfigValue_t[] pOptions)
```

<para>/ 在指定的虚拟端口上创建一个监听套接字。要使用的物理 UDP 端口将由 SDR_LISTEN_PORT 环境变量决定。如果未配置 UDP 端口，此调用将失败。</para> <para>/</para> <para>/ 此调用必须通过 SteamGameServerNetworkingSockets() 接口进行。</para> <para>/</para> <para>/ 当您使用票证生成器库来发放自己的票证时，应使用此函数。连接到此虚拟端口的客户端将需要一张票证，并且他们必须使用 ConnectToHostedDedicatedServer 进行连接。</para> <para>/</para> <para>/ 如果需要设置任何初始配置选项，请在此处传入。有关为何这比在创建后“立即”设置选项更可取，请参阅 SteamNetworkingConfigValue_t。</para>

**参数:**

- `nLocalVirtualPort` (`int`)
- `nOptions` (`int`)
- `pOptions` (`SteamNetworkingConfigValue_t[]`)

**返回值:** `HSteamListenSocket`

**用法示例:**
```csharp
var listenSocket = SteamGameServerNetworkingSockets.CreateHostedDedicatedServerListenSocket(27015, 0, null);
```

### GetGameCoordinatorServerLogin (静态)

```csharp
EResult GetGameCoordinatorServerLogin(IntPtr pLoginInfo, out int pcbSignedBlob, IntPtr pBlob)
```

<para>/ 生成一个身份验证 blob，可用于通过 SteamDatagram_ParseHostedServerLogin 安全登录</para> <para>/ 到您的后端。(请参阅 steamdatagram_gamecoordinator.h)</para> <para>/</para> <para>/ 在调用此函数前：</para> <para>/ - 在 pLoginInfo 中填充应用数据 (m_cbAppData 和 m_appData)。您可以将其</para> <para>/ 他所有字段留空。</para> <para>/ - *pcbSignedBlob 包含 pBlob 缓冲区的大小。(它应至少为</para> <para>/ k_cbMaxSteamDatagramGameCoordinatorServerLoginSerialized。)</para> <para>/</para> <para>/ 成功退出时：</para> <para>/ - 返回 k_EResultOK</para> <para>/ - pLoginInfo 的所有其他字段将被填充。</para> <para>/ - *pcbSignedBlob 包含已放入 pBlob 的序列化 blob 的大小。</para> <para>/</para> <para>/ 失败退出时：</para> <para>/ - 返回除 k_EResultOK 以外的值。</para> <para>/ - k_EResultNotLoggedOn：您尚未登录</para> <para>/ - 有关更多可能的失败返回值，请参阅 GetHostedDedicatedServerAddress。</para> <para>/ - pBlob 中将放置一条非本地化的诊断调试消息，描述</para> <para>/ 失败的原因。</para> <para>/</para> <para>/ 此函数通过使用颁发给此服务器的证书对 SteamDatagramGameCoordinatorServerLogin</para> <para>/ 的内容进行签名来工作。在开发环境中，如果没有证书也可以。</para> <para>/ (您需要在 SteamDatagram_ParseHostedServerLogin 中启用不安全的开发登录。)</para> <para>/ 否则，您将需要一个已签名的证书。</para> <para>/</para> <para>/ 注意：此处返回的路由 blob 未加密。请将其发送到您的后端</para> <para>/，不要直接与客户端共享。</para>

**参数:**

- `pLoginInfo` (`IntPtr`)
- `pcbSignedBlob` (`out int`)
- `pBlob` (`IntPtr`)

**返回值:** `EResult`

**用法示例:**
```csharp
IntPtr loginInfo = Marshal.AllocHGlobal(Marshal.SizeOf<SteamDatagramGameCoordinatorServerLogin>());
int blobSize = 1024;
IntPtr blob = Marshal.AllocHGlobal(blobSize);
EResult result = SteamGameServerNetworkingSockets.GetGameCoordinatorServerLogin(loginInfo, out blobSize, blob);
```

### ConnectP2PCustomSignaling (静态)

```csharp
HSteamNetConnection ConnectP2PCustomSignaling(out ISteamNetworkingConnectionSignaling pSignaling, ref SteamNetworkingIdentity pPeerIdentity, int nRemoteVirtualPort, int nOptions, SteamNetworkingConfigValue_t[] pOptions)
```

<para> 使用自定义信令协议的转发连接</para> <para> 如果您有自己的方法，可以通过一个相互信任的通道发送带外</para> <para> 信令/会合消息，则使用此方法。</para> <para>/ 创建一个 P2P“客户端”连接，该连接通过自定义</para> <para>/ 会合/信令通道进行信令。</para> <para>/</para> <para>/ pSignaling 指向您为此连接新创建的对象。</para> <para>/ 在调用 Release() 之前，该对象必须保持有效。一旦您将</para> <para>/ 该对象传递给此函数，它就会假定所有权。如果调用失败，</para> <para>/ 函数内部将调用 Release()。此外，在调用 Release() 之前，</para> <para>/ 您应准备好从任何线程调用您对象上的方法！您需要确保您的对象是线程安全的！</para> <para>/ 此外，您应确保尽快分派这些方法。</para> <para>/</para> <para>/ 此函数将立即构造一个处于“连接中”状态的连接。</para> <para>/ 不久之后（可能在函数返回之前，也可能在另一个线程中），</para> <para>/ 连接将通过调用 ISteamNetworkingConnectionSignaling::SendSignal</para> <para>/ 开始发送信令消息。</para> <para>/</para> <para>/ 当远程对等方接受连接时（请参阅</para> <para>/ ISteamNetworkingSignalingRecvContext::OnConnectRequest），</para> <para>/ 它将开始发送信令消息。当收到这些消息时，</para> <para>/ 您可以使用 ReceivedP2PCustomSignal 将其传递给连接。</para> <para>/</para> <para>/ 如果您知道预期在另一端的对等方的身份，</para> <para>/ 您可以传递其身份以改进调试输出或仅用于检测错误。</para> <para>/ 如果您还不知道他们的身份，可以传递 NULL，他们的</para> <para>/ 身份将在连接握手过程中确定。</para> <para>/</para> <para>/ 如果您使用此功能，可能希望在应用程序初始化时</para> <para>/ 调用 ISteamNetworkingUtils::InitRelayNetworkAccess()</para> <para>/</para> <para>/ 如果需要设置任何初始配置选项，请在此处传递。有关</para> <para>/ 为何这比在创建后“立即”设置选项更可取的详细信息，</para> <para>/ 请参阅 SteamNetworkingConfigValue_t。</para>

**参数:**

- `pSignaling` (`out ISteamNetworkingConnectionSignaling`)
- `pPeerIdentity` (`ref SteamNetworkingIdentity`)
- `nRemoteVirtualPort` (`int`)
- `nOptions` (`int`)
- `pOptions` (`SteamNetworkingConfigValue_t[]`)

**返回值:** `HSteamNetConnection`

**用法示例:**
```csharp
// 注意：此方法需要实现 ISteamNetworkingConnectionSignaling 接口并管理其生命周期  
// 示例仅展示调用方式（实际需自行实现 pSignaling 对象）  
SteamGameServerNetworkingSockets.ConnectP2PCustomSignaling(out pSignaling, ref peerIdentity, 12345, 0, null);
```

### ReceivedP2PCustomSignal (静态)

```csharp
bool ReceivedP2PCustomSignal(IntPtr pMsg, int cbMsg, out ISteamNetworkingSignalingRecvContext pContext)
```

<para>/ 当自定义信令接收到消息时调用。当您的</para> <para>/ 信令通道接收到消息时，应将信封中的任何</para> <para>/ 路由信息保存到上下文对象中，</para> <para>/ 然后将有效载荷传递给此函数。</para> <para>/</para> <para>/ 接下来可能会发生几种不同的情况，具体取决于消息：</para> <para>/</para> <para>/ - 如果信号与现有连接关联，则立即处理。</para> <para>/ 如果需要发送任何回复，它们将通过</para> <para>/ 与该连接关联的 ISteamNetworkingConnectionSignaling</para> <para>/ 进行分发。</para> <para>/ - 如果消息代表一个连接请求（并且该请求</para> <para>/ 对现有连接而言并非冗余），则会创建一个新连接，</para> <para>/ 并在您的上下文对象上调用 ReceivedConnectRequest</para> <para>/ 以确定如何继续。</para> <para>/ - 否则，该消息是针对一个不存在（或已不存在）的连接。</para> <para>/ 在这种情况下，我们*可能*会在您的上下文对象上调用 SendRejectionReply。</para> <para>/</para> <para>/ 在任何情况下，我们都不会在函数返回后保存或访问 pContext。</para> <para>/</para> <para>/ 如果消息被解析并分发，且未发生任何异常或可疑情况，则返回 true。</para> <para>/ 如果消息存在问题，导致无法进行常规处理，则返回 false。（调试输出通常</para> <para>/ 会提供更多信息。）</para> <para>/</para> <para>/ 如果您打算使用中继连接，那么在应用程序初始化时，</para> <para>/ 您可能需要调用 ISteamNetworkingUtils::InitRelayNetworkAccess()。</para>

**参数:**

- `pMsg` (`IntPtr`)
- `cbMsg` (`int`)
- `pContext` (`out ISteamNetworkingSignalingRecvContext`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.ReceivedP2PCustomSignal(msgBuffer, msgSize, out context);
```

### GetCertificateRequest (静态)

```csharp
bool GetCertificateRequest(out int pcbBlob, IntPtr pBlob, out SteamNetworkingErrMsg errMsg)
```

<para>由应用程序提供证书。在 Steam 上，我们通常会自动处理所有这些操作</para> <para>因此您无需使用这些高级功能。</para> <para>/ 获取描述证书请求的 blob。您可以将此发送给您的游戏协调器。</para> <para>/ 进入时，*pcbBlob 应包含缓冲区的大小。成功退出时，它将</para> <para>/ 返回已填充的字节数。您可以传递 pBlob=NULL 来查询所需</para> <para>/ 的大小。（512 字节是一个保守的估计。）</para> <para>/</para> <para>/ 将此 blob 传递给您的游戏协调器并调用 SteamDatagram_CreateCert。</para>

**参数:**

- `pcbBlob` (`out int`)
- `pBlob` (`IntPtr`)
- `errMsg` (`out SteamNetworkingErrMsg`)

**返回值:** `bool`

**用法示例:**
```csharp
int pcbBlob;  
SteamGameServerNetworkingSockets.GetCertificateRequest(out pcbBlob, IntPtr.Zero, out var errMsg);
```

### SetCertificate (静态)

```csharp
bool SetCertificate(IntPtr pCertificate, int cbCertificate, out SteamNetworkingErrMsg errMsg)
```

<para>/ 设置证书。证书 blob 应为 SteamDatagram_CreateCert 的输出。</para> <para>/</para>

**参数:**

- `pCertificate` (`IntPtr`)
- `cbCertificate` (`int`)
- `errMsg` (`out SteamNetworkingErrMsg`)

**返回值:** `bool`

**用法示例:**
```csharp
IntPtr certPtr = Marshal.AllocHGlobal(1024); // 假设已填充证书数据
SteamGameServerNetworkingSockets.SetCertificate(certPtr, 1024, out SteamNetworkingErrMsg errMsg);
Marshal.FreeHGlobal(certPtr);
```

### ResetIdentity (静态)

```csharp
void ResetIdentity(ref SteamNetworkingIdentity pIdentity)
```

<para>/ 重置与此实例关联的身份。</para> <para>/ 任何已打开的连接都将被关闭。任何先前的证书等都将被丢弃。</para> <para>/ 您可以传入您想要使用的特定身份，也可以传入 NULL，</para> <para>/ 在这种情况下，身份将无效，直到您使用 SetCertificate 设置它。</para> <para>/</para> <para>/ 注意：此功能实际上在 Steam 上不受支持！它被包含</para> <para>/ 在其中是为了在其他平台上的使用，在这些平台上，当前用户可以注销，</para> <para>/ 而新用户可以登录。</para>

**参数:**

- `pIdentity` (`ref SteamNetworkingIdentity`)

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.ResetIdentity(ref identity);
```

### RunCallbacks (静态)

```csharp
void RunCallbacks()
```

<para> 杂项 </para> <para>/ 为此接口调用所有已排队的回调函数。</para> <para>/ 参见 k_ESteamNetworkingConfig_Callback_ConnectionStatusChanged 等。</para> <para>/</para> <para>/ 如果您正在使用 Steam 的回调分发机制（SteamAPI_RunCallbacks 和 SteamGameserver_RunCallbacks），则无需调用此函数。</para>

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.RunCallbacks();
```

### BeginAsyncRequestFakeIP (静态)

```csharp
bool BeginAsyncRequestFakeIP(int nNumPorts)
```

<para> "FakeIP" 系统。</para> <para> FakeIP 本质上是一个临时的、任意的标识符，碰巧是一个有效的 IPv4 地址。此系统的目的是使其易于与使用 IPv4 地址标识主机的现有代码集成。</para> <para> FakeIP 地址永远不会真正用于在互联网上发送或接收任何数据包，它严格来说只是一个标识符。</para> <para> FakeIP 地址的设计目标是（希望）能尽可能透明地通过现有代码，同时与在同一代码中使用的“真实”地址（可能存在于互联网和局域网中）的冲突尽可能少。在撰写此注释时，它们来自 169.254.0.0/16 范围，且端口号始终大于 1024。但是，这可能会发生变化！不要对这些地址做任何假设，否则您的代码将来可能会损坏。特别是，您应该使用 ISteamNetworkingUtils::IsFakeIP 等函数来确定一个 IP 地址是否是此系统使用的“虚假”地址。</para> <para>/ 开始分配一个虚假的 IPv4 地址的异步过程，其他对等方可以使用该地址通过 P2P 联系我们。此函数返回的 IP 地址对于给定的 appid 是全局唯一的。</para> <para>/</para> <para>/ nNumPorts 是您希望保留的端口号。这与监听多个 UDP 端口对不同类型流量的作用相同。因为这些分配来自全局命名空间，因此您可请求的端口数量有相对严格的限制。（在撰写本文时，限制为 4。）</para> <para>/ 端口分配*不*保证有任何特定的顺序或关系！*不要*假设它们是连续的，尽管在实践中经常如此。</para> <para>/</para> <para>/ 如果请求已在进行中，则返回 false；如果启动了新请求，则返回 true。请求完成后将发布一个 SteamNetworkingFakeIPResult_t。</para> <para>/</para> <para>/ 对于游戏服务器，您*必须*在初始化 SDK 后但在开始登录前调用此函数。Steam 需要提前知道将使用 FakeIP。</para> <para>/ 通常显示公共 IP 的任何地方（例如服务器浏览器）都将被 FakeIP 和索引 0 处的虚假端口替换。请求实际上被排队，直到登录完成，因此您必须在分配完成前登录。除了可以本地检测到的简单故障（例如无效参数）外，SteamNetworkingFakeIPResult_t 回调（无论成功或失败）都不会在登录后发布。此外，假设 FakeIP 分配对您的应用程序功能至关重要，因此只有在*多次*重试后才会报告失败。此过程可能持续几分钟。强烈建议将失败视为致命错误。</para> <para>/</para> <para>/ 要使用面向连接的（TCP 风格）API 进行通信：</para> <para>/ - 服务器使用 CreateListenSocketP2PFakeIP 创建一个监听套接字</para> <para>/ - 客户端使用 ConnectByIPAddress 进行连接，传入 FakeIP 地址。</para> <para>/ - 连接的行为大多像 P2P 连接。SteamNetConnectionInfo_t 中出现的身份在知道真实身份之前将是 FakeIP 身份。然后它将是真实身份。如果 SteamNetConnectionInfo_t::m_addrRemote 有效，它将是一个 NAT 打洞连接的真实 IPv4 地址。否则，它将无效。</para> <para>/</para> <para>/ 要使用即席的 sendto/recvfrom（UDP 风格）API 进行通信，</para> <para>/ 请使用 CreateFakeUDPPort。</para>

**参数:**

- `nNumPorts` (`int`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerNetworkingSockets.BeginAsyncRequestFakeIP(1);
```

### GetFakeIP (静态)

```csharp
void GetFakeIP(int idxFirstPort, out SteamNetworkingFakeIPResult_t pInfo)
```

<para>/ 返回我们被分配的伪造IP和端口信息，</para> <para>/ 如果有的话。idxFirstPort目前为保留字段，必须为零。</para> <para>/ 请务必检查 SteamNetworkingFakeIPResult_t::m_eResult</para>

**参数:**

- `idxFirstPort` (`int`)
- `pInfo` (`out SteamNetworkingFakeIPResult_t`)

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.GetFakeIP(0, out var result);
Console.WriteLine($"Result: {result.m_eResult}, IP: {result.m_nIP}, Port: {result.m_nPort}");
```

### CreateListenSocketP2PFakeIP (静态)

```csharp
HSteamListenSocket CreateListenSocketP2PFakeIP(int idxFakePort, int nOptions, SteamNetworkingConfigValue_t[] pOptions)
```

<para>/ 创建一个监听套接字，用于监听发送到我们伪造IP的P2P连接。</para> <para>/ 对等方可以通过调用ConnectByIPAddress来向此监听套接字发起连接。</para> <para>/</para> <para>/ idxFakePort 指的是所请求的伪造端口的*索引*，</para> <para>/ 而不是实际的端口号。例如，传入0以引用保留中的第一个端口。</para> <para>/ 你必须在调用BeginAsyncRequestFakeIP之后才能调用此方法。</para> <para>/ 但是，你无需等待请求完成即可创建监听套接字。</para>

**参数:**

- `idxFakePort` (`int`)
- `nOptions` (`int`)
- `pOptions` (`SteamNetworkingConfigValue_t[]`)

**返回值:** `HSteamListenSocket`

**用法示例:**
```csharp
var listenSocket = SteamGameServerNetworkingSockets.CreateListenSocketP2PFakeIP(0, 0, null);
```

### GetRemoteFakeIPForConnection (静态)

```csharp
EResult GetRemoteFakeIPForConnection(HSteamNetConnection hConn, out SteamNetworkingIPAddr pOutAddr)
```

<para>/ 如果连接是通过“FakeIP”系统发起的，那么我们可以</para> <para>/ 获取远程主机的IP地址。如果在建立连接时远程主机</para> <para>/ 拥有一个全局的FakeIP，则此函数将返回该全局IP。</para> <para>/ 否则，将从本地的FakeIP地址空间中分配一个</para> <para>/ 本地唯一的FakeIP，并返回该地址。</para> <para>/</para> <para>/ 本地FakeIP的分配会尝试以一致的方式分配地址。</para> <para>/ 如果对同一远程主机建立了多个连接，它们*很可能*会</para> <para>/ 返回相同的FakeIP。但是，由于命名空间有限，</para> <para>/ 这无法得到保证。</para> <para>/</para> <para>/ 失败时返回：</para> <para>/ - k_EResultInvalidParam: 无效的连接句柄</para> <para>/ - k_EResultIPNotFound: 此连接未使用FakeIP系统建立</para>

**参数:**

- `hConn` (`HSteamNetConnection`)
- `pOutAddr` (`out SteamNetworkingIPAddr`)

**返回值:** `EResult`

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.GetRemoteFakeIPForConnection(hConn, out var fakeAddr);
Console.WriteLine($"Fake IP: {fakeAddr}");
```

### CreateFakeUDPPort (静态)

```csharp
IntPtr CreateFakeUDPPort(int idxFakeServerPort)
```

<para>/ 获取一个接口，该接口可以像 UDP 端口一样用于向 FakeIP 地址发送/接收</para> <para>/ 数据报。此功能旨在简化将现有的基于 UDP 的代码移植以利用 SDR。</para> <para>/</para> <para>/ idxFakeServerPort 指的是使用 BeginAsyncRequestFakeIP 分配的端口的 *索引*，</para> <para>/ 用于创建“服务器”端口。您可以在分配完成之前调用此函数。</para> <para>/ 但是，在分配成功之前，任何发送数据包的尝试都将失败。</para> <para>/ 当对等方接收到从此接口发送的数据包时，数据包的源地址</para> <para>/ 将是全局唯一的 FakeIP。如果您多次调用此函数并传递相同的（非负）</para> <para>/ 伪端口索引，将返回同一个对象，并且该对象不进行引用计数。</para> <para>/</para> <para>/ 要创建“客户端”端口（例如，相当于临时 UDP 端口），</para> <para>/ 请传递 -1。在这种情况下，每次调用都会返回一个不同的对象。</para> <para>/ 当对等方接收到从此接口发送的数据包时，对等方将</para> <para>/ 从其自身本地控制的命名空间中分配一个 FakeIP。</para>

**参数:**

- `idxFakeServerPort` (`int`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr fakePort = SteamGameServerNetworkingSockets.CreateFakeUDPPort(0); // 创建服务器端口（索引为0）  
IntPtr clientPort = SteamGameServerNetworkingSockets.CreateFakeUDPPort(-1); // 创建客户端端口
```

