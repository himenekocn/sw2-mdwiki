<a id="steamgameservernetworkingsockets"></a>

# 📦 SteamGameServerNetworkingSockets

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### CreateListenSocketIP (静态)

```csharp
HSteamListenSocket CreateListenSocketIP(ref SteamNetworkingIPAddr localAddress, int nOptions, SteamNetworkingConfigValue_t[] pOptions)
```

<para>/ 创建一个"服务端"套接字，用于通过普通UDP（IPv4或IPv6）监听客户端调用ConnectByIPAddress进行连接</para>  
<para>/</para>  
<para>/ 您必须选择要监听的特定本地端口，并在本地地址的端口字段中设置它。</para>  
<para>/</para>  
<para>/ 通常您会将地址的IP部分设置为零（SteamNetworkingIPAddr::Clear()）。</para>  
<para>/ 这意味着您不会绑定到任何特定的本地接口（即与普通套接字代码中的INADDR_ANY相同）。</para>  
<para>/ 此外，如果可能，套接字将以"双栈"模式绑定，这意味着它可以同时接受IPv4和IPv6客户端连接。</para>  
<para>/ 如果您确实希望绑定特定接口，则将本地地址设置为相应的IPv4或IPv6 IP。</para>  
<para>/</para>  
<para>/ 如果您需要设置任何初始配置选项，请在此处传递它们。关于为什么这比创建后"立即"设置选项更可取，请参阅SteamNetworkingConfigValue_t。</para>  
<para>/</para>  
<para>/ 当客户端尝试连接时，将发布SteamNetConnectionStatusChangedCallback_t。</para>  
<para>/ 连接将处于连接中状态。</para>

**参数:**

- `localAddress` (`ref SteamNetworkingIPAddr`)
- `nOptions` (`int`)
- `pOptions` (`SteamNetworkingConfigValue_t[]`)

**返回值:** `HSteamListenSocket`

**用法示例:**
```csharp
var addr = SteamNetworkingIPAddr.Any;
var socket = SteamGameServerNetworkingSockets.CreateListenSocketIP(ref addr, 0, null);
```

### ConnectByIPAddress (静态)

```csharp
HSteamNetConnection ConnectByIPAddress(ref SteamNetworkingIPAddr address, int nOptions, SteamNetworkingConfigValue_t[] pOptions)
```

<para>/ 创建一个连接，通过UDP在指定的IPv4或IPv6地址上开始与"服务器"通信。远程主机必须正在监听，且在该端口上使用匹配的CreateListenSocketIP调用。</para> <para>/</para> <para>/ 当开始连接时，将触发一个SteamNetConnectionStatusChangedCallback_t回调，随后在超时或成功连接时再次触发。</para> <para>/</para> <para>/ 如果服务器未配置任何身份标识，则其网络地址将成为唯一的身份标识。或者，网络主机可能提供平台特定的身份标识，带或不带有效证书以验证该身份。 （这些详细信息将包含在SteamNetConnectionStatusChangedCallback_t中。）由您的应用程序决定是否允许该连接。</para> <para>/</para> <para>/ 默认情况下，所有连接都将获得足以防止随意窃听的基本加密。但请注意，如果没有证书（或通过某些其他带外机制分发的共享密钥），您将无法知道另一端的真实身份，因此容易受到中间人攻击。</para> <para>/</para> <para>/ 如果您需要设置任何初始配置选项，请在此处传递。有关为何这优于在创建后"立即"设置选项的更多信息，请参阅SteamNetworkingConfigValue_t。</para>

**参数:**

- `address` (`ref SteamNetworkingIPAddr`)
- `nOptions` (`int`)
- `pOptions` (`SteamNetworkingConfigValue_t[]`)

**返回值:** `HSteamNetConnection`

**用法示例:**
```csharp
var addr = default(SteamNetworkingIPAddr);
var conn = SteamGameServerNetworkingSockets.ConnectByIPAddress(ref addr, 0, null);
```

### CreateListenSocketP2P (静态)

```csharp
HSteamListenSocket CreateListenSocketP2P(int nLocalVirtualPort, int nOptions, SteamNetworkingConfigValue_t[] pOptions)
```

<para>/ 类似于 CreateListenSocketIP，但客户端将使用 ConnectP2P 进行连接。</para> <para>/</para> <para>/ nLocalVirtualPort 指定客户端如何通过 ConnectP2P 连接到此套接字。</para> <para>/ 通常应用程序只有一个监听套接字；</para> <para>/ 此时使用零即可。如果需要打开多个监听套接字并允许客户端</para> <para>/ 连接到其中任意一个，则 nLocalVirtualPort 应为较小的整数</para> <para>/（<1000），且对创建的每个监听套接字唯一。</para> <para>/</para> <para>/ 如果使用此功能，建议在应用初始化时调用 ISteamNetworkingUtils::InitRelayNetworkAccess()。</para> <para>/</para> <para>/ 如果您在已知数据中心内的专用服务器上进行监听，</para> <para>/ 可以使用此函数代替 CreateHostedDedicatedServerListenSocket，</para> <para>/ 以允许客户端无需票据即可连接。任何拥有该应用</para> <para>/ 并登录 Steam 的用户均可尝试连接到您的服务器。</para> <para>/ 此外，连接尝试可能需要客户端连接到 Steam，</para> <para/> 这增加了可能的故障点。当使用票据时，</para> <para>/ 客户端获取票据后，即使与 Steam 断开连接或 Steam 离线，</para> <para>/ 也能连接到您的服务器。</para> <para>/</para> <para>/ 如果需要设置任何初始配置选项，请在此处传递。有关为何这比</para> <para>/ 创建后“立即”设置选项更优，请参阅 SteamNetworkingConfigValue_t。</para>

**参数:**

- `nLocalVirtualPort` (`int`)
- `nOptions` (`int`)
- `pOptions` (`SteamNetworkingConfigValue_t[]`)

**返回值:** `HSteamListenSocket`

**用法示例:**
```csharp
var socket = SteamGameServerNetworkingSockets.CreateListenSocketP2P(0, 0, null);
```

### ConnectP2P (静态)

```csharp
HSteamNetConnection ConnectP2P(ref SteamNetworkingIdentity identityRemote, int nRemoteVirtualPort, int nOptions, SteamNetworkingConfigValue_t[] pOptions)
```

<para>/ 开始连接一个使用特定平台标识符识别的对等端。</para>
<para>/ 这会使用默认的会合服务，该服务取决于平台和库的配置。</para>
<para>/ （例如，在Steam上，它通过Steam后端进行。）</para>
<para>/</para>
<para>/ 如果需要设置任何初始配置选项，请在此处传递。请参阅</para>
<para>/ SteamNetworkingConfigValue_t 了解为何这比在创建后"立即"设置选项更可取。</para>
<para>/</para>
<para>/ 如需使用您自己的信令服务，请参阅：</para>
<para>/ - ConnectP2PCustomSignaling</para>
<para>/ - k_ESteamNetworkingConfig_Callback_CreateConnectionSignaling</para>

**参数:**

- `identityRemote` (`ref SteamNetworkingIdentity`)
- `nRemoteVirtualPort` (`int`)
- `nOptions` (`int`)
- `pOptions` (`SteamNetworkingConfigValue_t[]`)

**返回值:** `HSteamNetConnection`

**用法示例:**
```csharp
var identity = SteamNetworkingIdentity.CreateFromSteamId(76561198000000000);
var connection = SteamGameServerNetworkingSockets.ConnectP2P(ref identity, 0, 0, null);
```

### AcceptConnection (静态)

```csharp
EResult AcceptConnection(HSteamNetConnection hConn)
```

<para>/ 接受已在监听套接字上接收到的传入连接。</para> <para>/</para> <para>/ 当接收到连接尝试时（可能是在交换了几个基本握手数据包以防止简单欺骗之后），</para> <para>/ 会在 k_ESteamNetworkingConnectionState_Connecting 状态下创建一个连接接口</para> <para>/ 对象，并发布 SteamNetConnectionStatusChangedCallback_t 回调。此时，您的</para> <para>/ 应用必须接受或关闭该连接。（不得忽略它。）</para> <para>/ 接受连接将使其转换到已连接状态或路由查找状态，具体取决于连接类型。</para> <para>/</para> <para>/ 您应在一两秒内采取行动，因为接受连接实际上会发送回复通知客户端已连接。如果您</para> <para>/ 延迟采取行动，从客户端的角度来看，这等同于网络无响应，客户端可能会超时连接尝试。换句话说，</para> <para>/ 客户端无法区分由网络问题引起的延迟和应用导致的延迟。</para> <para>/</para> <para>/ 这意味着，如果您的应用在数秒内未处理回调（例如，在加载地图期间），则客户端</para> <para>/ 可能在该时间间隔内尝试连接并因超时而失败。</para> <para>/</para> <para>/ 如果应用未及时响应连接尝试，且我们停止接收来自客户端的通信，则连接尝试将</para> <para>/ 在本地超时，连接将转换到</para> <para>/ k_ESteamNetworkingConnectionState_ProblemDetectedLocally 状态。客户端也可能</para> <para>/ 在接受连接之前关闭连接，根据具体事件序列，</para> <para>/ 也可能转换到 k_ESteamNetworkingConnectionState_ClosedByPeer 状态。</para> <para>/</para> <para>/ 如果句柄无效，则返回 k_EResultInvalidParam。</para> <para>/ 如果连接未处于适当状态，则返回 k_EResultInvalidState。</para> <para>/ （请注意，连接状态可能在通知发布到队列与应用接收通知之间发生变化。）</para> <para>/</para> <para>/ 关于连接配置选项的注意事项。如果您需要设置通过特定监听</para> <para>/ 套接字接受的所有连接共有的配置选项，请考虑在监听套接字上设置这些选项，</para> <para>/ 因为此类选项会自动继承。如果您确实需要设置连接特定的选项，</para> <para>/ 则在接受连接之前设置这些选项是安全的。</para>

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

<para>/ 断开与远程主机的连接并使连接句柄失效。</para>
<para>/ 连接上所有未读取的数据将被丢弃。</para>
<para>/</para>
<para>/ nReason 是一个应用程序定义的代码，将在另一端被接收，并（在可能的情况下）记录在后端分析中。</para>
<para>/ 该值应来自受限范围。（参见 ESteamNetConnectionEnd。）如果您不需要向远程主机</para>
<para>/ 传递任何信息，并且不希望分析能够区分“正常”连接终止与“异常”连接终止，</para>
<para>/ 您可以传递零，此时将使用通用值</para>
<para>/ k_ESteamNetConnectionEnd_App_Generic。</para>
<para>/</para>
<para>/ pszDebug 是一个可选的人类可读诊断字符串，将由远程主机接收，并（在可能的情况下）记录在后端分析中。</para>
<para>/</para>
<para>/ 如果您希望将套接字置于“延迟关闭”状态，尝试刷新任何剩余的已发送数据，请使用 bEnableLinger=true。</para>
<para>/ 否则，可靠数据将不会被刷新。</para>
<para>/</para>
<para>/ 如果连接已经结束，您只是释放连接接口，则原因代码、调试字符串和延迟关闭标志将被忽略。</para>

**参数:**

- `hPeer` (`HSteamNetConnection`)
- `nReason` (`int`)
- `pszDebug` (`string`)
- `bEnableLinger` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.CloseConnection(hPeer, 0, "User disconnected", false);
```

### CloseListenSocket (静态)

```csharp
bool CloseListenSocket(HSteamListenSocket hSocket)
```

<para>/ 销毁监听套接字。所有在该监听套接字上接受</para> <para>/ 的连接将被强制关闭。</para>

**参数:**

- `hSocket` (`HSteamListenSocket`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.CloseListenSocket(listenSocketHandle);
```

### SetConnectionUserData (静态)

```csharp
bool SetConnectionUserData(HSteamNetConnection hPeer, long nUserData)
```

<para>/ 设置连接用户数据。该数据将在以下位置返回</para>
<para>/ - 您可以使用 GetConnectionUserData 查询该数据。</para>
<para>/ - SteamNetworkingmessage_t 结构体。</para>
<para>/ - SteamNetConnectionInfo_t 结构体。</para>
<para>/ （该结构体是 SteamNetConnectionStatusChangedCallback_t 的成员——但请注意下方警告!!!!）</para>
<para>/</para>
<para>/ 是否需要在连接创建时原子性地设置该数据？</para>
<para>/ 请参阅 k_ESteamNetworkingConfig_ConnectionUserData。</para>
<para>/</para>
<para>/ 警告：在回调结构体中使用该值时请*极其谨慎*。</para>
<para>/ 回调被排入队列，您在回调中接收到的值</para>
<para>/ 是回调被排入队列时生效的用户数据。</para>
<para>/ 如果您不理解这一点，可能会发生微妙的竞态条件！</para>
<para>/</para>
<para>/ 如果该连接有任何入站消息被排入队列，用户数据</para>
<para>/ 字段会被更新，因此当您接收消息时（例如使用</para>
<para>/ ReceiveMessagesOnConnection），它们始终包含最新的</para>
<para>/ 用户数据。因此，回调中可能发生的复杂竞态条件</para>
<para>/ 不适用于消息检索。</para>
<para>/</para>
<para>/ 如果句柄无效，则返回 false。</para>

**参数:**

- `hPeer` (`HSteamNetConnection`)
- `nUserData` (`long`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerNetworkingSockets.SetConnectionUserData(hPeer, 12345L);
```

### GetConnectionUserData (静态)

```csharp
long GetConnectionUserData(HSteamNetConnection hPeer)
```

<para>/ 获取连接用户数据。如果句柄无效，返回 -1</para> <para>/ 或者未在连接上设置任何用户数据时，返回 -1。</para>

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

<para>/ 设置连接名称，主要用于调试</para>

**参数:**

- `hPeer` (`HSteamNetConnection`)
- `pszName` (`string`)

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.SetConnectionName(connectionHandle, "DebugClient");
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
bool result = SteamGameServerNetworkingSockets.GetConnectionName(hPeer, out string name, 256);
```

### SendMessageToConnection (静态)

```csharp
EResult SendMessageToConnection(HSteamNetConnection hConn, IntPtr pData, uint cbData, int nSendFlags, out long pOutMessageNumber)
```

<para>/ 在指定连接上向远程主机发送消息。</para> <para>/</para> <para>/ nSendFlags 决定了将提供的传递保证，</para> <para>/ 以及数据何时应被缓冲等。例如：k_nSteamNetworkingSend_Unreliable</para> <para>/</para> <para>/ 请注意，我们用于消息的语义与标准“流”套接字的语义</para> <para>/ 并不完全相同。（SOCK_STREAM）对于普通流套接字，</para> <para>/ 数据块之间的界限不被视为相关，写入数据块的大小</para> <para>/ 不一定与另一端读取返回的数据块大小相匹配。</para> <para>/ 远程主机可能读取部分数据块，或数据块可能被合并。</para> <para>/ 然而，对于此处使用的消息语义，大小将完全匹配。</para> <para>/ 每个发送调用将与远程主机上的成功读取调用一一对应。</para> <para>/ 如果您正在将现有的面向流代码移植到可靠消息的语义上，</para> <para>/ 您的代码应该能正常工作，因为可靠消息语义比流语义</para> <para>/ 更为严格。唯一的注意事项与性能相关：保留消息大小</para> <para/> 会产生每条消息的开销，因此如果您的代码发送许多小块数据，</para> <para>/ 性能将会下降。任何不写入过小数据块的基于流套接字的代码</para> <para>/ 无需任何更改即可正常工作。</para> <para>/</para> <para>/ pOutMessageNumber 是一个可选指针，用于接收分配给消息的</para> <para>/ 消息编号（如果发送成功）。</para> <para>/</para> <para>/ 返回值：</para> <para>/ - k_EResultInvalidParam：无效的连接句柄，或单条消息过大。</para> <para>/ （参见 k_cbMaxSteamNetworkingSocketsMessageSizeSend）</para> <para>/ - k_EResultInvalidState：连接处于无效状态</para> <para>/ - k_EResultNoConnection：连接已终止</para> <para>/ - k_EResultIgnored：您使用了 k_nSteamNetworkingSend_NoDelay，但消息被丢弃，因为</para> <para>/   我们尚未准备好发送。</para> <para>/ - k_EResultLimitExceeded：已有过多数据排队待发送。</para> <para>/ （参见 k_ESteamNetworkingConfig_SendBufferSize）</para>

**参数:**

- `hConn` (`HSteamNetConnection`)
- `pData` (`IntPtr`)
- `cbData` (`uint`)
- `nSendFlags` (`int`)
- `pOutMessageNumber` (`out long`)

**返回值:** `EResult`

**用法示例:**
```csharp
var result = SteamGameServerNetworkingSockets.SendMessageToConnection(hConn, pData, cbData, 0, out long messageNumber);
```

### SendMessages (静态)

```csharp
void SendMessages(int nMessages, SteamNetworkingMessage_t[] pMessages, long[] pOutMessageNumberOrResult)
```

<para>/ 发送一条或多条消息，无需复制消息负载。</para>  
<para>/ 这是发送消息的最高效方式。要使用此</para>  
<para>/ 函数，必须先通过 ISteamNetworkingUtils::AllocateMessage 分配一个消息对象。</para>  
<para>/ （请勿在栈上声明或自行分配。）</para>  
<para>/</para>  
<para>/ 您应填写消息负载。您既可以</para>  
<para>/ 让其为缓冲区分配内存并随后填充负载，</para>  
<para>/ 也可以若已分配缓冲区，直接让 m_pData 指向您的缓冲区，</para>  
<para>/ 并设置回调函数以释放该缓冲区。请注意，若使用自定义缓冲区，该缓冲区必须保持有效</para>  
<para>/ 直到回调执行完毕。同时还请注意，回调可能随时</para>  
<para>/ 从任何线程被调用（甚至可能在 SendMessages 返回之前！），</para>  
<para>/ 因此回调必须快速且线程安全。</para>  
<para>/</para>  
<para>/ 您还必须填写：</para>  
<para>/ - m_conn —— 接收消息的连接句柄</para>  
<para>/ - m_nFlags —— k_nSteamNetworkingSend_xxx 标志的位掩码</para>  
<para>/</para>  
<para>/ 所有其他字段当前均为保留字段，不应修改。</para>  
<para>/</para>  
<para>/ 库将取得消息结构体的所有权。它们可能</para>  
<para>/ 随时被修改或失效，因此传递给此函数后，</para>  
<para>/ 不得再读取它们。</para>  
<para>/</para>  
<para>/ pOutMessageNumberOrResult 是一个可选数组，用于接收</para>  
<para>/ 每条消息发送成功时分配的消息编号。</para>  
<para>/ 若发送失败，则数组中会存入负的 EResult 值。</para>  
<para>/ 例如，若连接处于无效状态，数组将包含 -k_EResultInvalidState。</para>  
<para>/ 可能的失败代码请参见 ISteamNetworkingSockets::SendMessageToConnection。</para>

**参数:**

- `nMessages` (`int`)
- `pMessages` (`SteamNetworkingMessage_t[]`)
- `pOutMessageNumberOrResult` (`long[]`)

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.SendMessages(1, messages, results);
```

### FlushMessagesOnConnection (静态)

```csharp
EResult FlushMessagesOnConnection(HSteamNetConnection hConn)
```

<para>/ 刷新任何在纳格尔计时器上等待的消息，并在下一次传输机会时发送它们（通常意味着立即发送）。</para>  
<para>/</para>  
<para>/ 如果启用了纳格尔算法（默认启用），则在调用</para>  
<para>/ SendMessageToConnection 时，消息将被缓冲，直到纳格尔时间到期</para>  
<para>/ 前才发送，以便将小消息合并到同一个数据包中。</para>  
<para>/ （参见 k_ESteamNetworkingConfig_NagleTime）</para>  
<para>/</para>  
<para>/ 返回值：</para>  
<para>/ k_EResultInvalidParam：无效的连接句柄</para>  
<para>/ k_EResultInvalidState：连接处于无效状态</para>  
<para>/ k_EResultNoConnection：连接已终止</para>  
<para>/ k_EResultIgnored：我们尚未（完全）连接，因此此操作无效。</para>

**参数:**

- `hConn` (`HSteamNetConnection`)

**返回值:** `EResult`

**用法示例:**
```csharp
EResult result = SteamGameServerNetworkingSockets.FlushMessagesOnConnection(hConn);
```

### ReceiveMessagesOnConnection (静态)

```csharp
int ReceiveMessagesOnConnection(HSteamNetConnection hConn, IntPtr[] ppOutMessages, int nMaxMessages)
```

<para>/ 从连接中获取下一个可用消息（如果有）。</para>  
<para>/ 返回放入数组中的消息数量，最多不超过 nMaxMessages。</para>  
<para>/ 如果连接句柄无效，则返回 -1。</para>  
<para>/</para>  
<para>/ 数组中返回消息的顺序是相关的。</para>  
<para>/ 可靠消息将按照发送顺序接收（且具有相同的大小——关于此点与流式套接字的细微区别，请参见 SendMessageToConnection）。</para>  
<para>/</para>  
<para>/ 不可靠消息可能被丢弃，或相对于彼此、相对于可靠消息乱序传递。同一不可靠消息可能被多次接收。</para>  
<para>/</para>  
<para>/ 如果返回任何消息，您必须在处理完每条消息后调用 SteamNetworkingMessage_t::Release() 以释放资源。将对象保留一段时间（放入某些队列等）是安全的，并且您可以从任何线程调用 Release()。</para>

**参数:**

- `hConn` (`HSteamNetConnection`)
- `ppOutMessages` (`IntPtr[]`)
- `nMaxMessages` (`int`)

**返回值:** `int`

**用法示例:**
```csharp
IntPtr[] messages = new IntPtr[10];
int count = SteamGameServerNetworkingSockets.ReceiveMessagesOnConnection(hConn, messages, 10);
```

### GetConnectionInfo (静态)

```csharp
bool GetConnectionInfo(HSteamNetConnection hConn, out SteamNetConnectionInfo_t pInfo)
```

<para>返回关于连接高级状态的基本信息。</para>

**参数:**

- `hConn` (`HSteamNetConnection`)
- `pInfo` (`out SteamNetConnectionInfo_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamNetConnectionInfo_t info;
bool success = SteamGameServerNetworkingSockets.GetConnectionInfo(hConn, out info);
```

### GetConnectionRealTimeStatus (静态)

```csharp
EResult GetConnectionRealTimeStatus(HSteamNetConnection hConn, ref SteamNetConnectionRealTimeStatus_t pStatus, int nLanes, ref SteamNetConnectionRealTimeLaneStatus_t pLanes)
```

<para>/ 返回关于连接实时状态以及每个通道队列状态的一小组信息</para>
<para>/</para>
<para>/ - 如果不需要该信息，pStatus 可为 NULL（例如，您只关心通道信息）</para>
<para>/ - 进入时，nLanes 指定 pLanes 数组的长度。如果您不希望接收任何通道数据，此值可为 0。该值小于已配置的通道总数是允许的。</para>
<para>/ - pLanes 指向一个将接收通道特定信息的数组。如果不需要，它可为 NULL</para>
<para>/</para>
<para>/ 返回值：</para>
<para>/ - k_EResultNoConnection - 连接句柄无效或连接已关闭</para>
<para>/ - k_EResultInvalidParam - nLanes 参数错误</para>

**参数:**

- `hConn` (`HSteamNetConnection`)
- `pStatus` (`ref SteamNetConnectionRealTimeStatus_t`)
- `nLanes` (`int`)
- `pLanes` (`ref SteamNetConnectionRealTimeLaneStatus_t`)

**返回值:** `EResult`

**用法示例:**
```csharp
var status = new SteamNetConnectionRealTimeStatus_t(); var laneStatus = new SteamNetConnectionRealTimeLaneStatus_t(); EResult result = SteamGameServerNetworkingSockets.GetConnectionRealTimeStatus(hConn, ref status, 1, ref laneStatus);
```

### GetDetailedConnectionStatus (静态)

```csharp
int GetDetailedConnectionStatus(HSteamNetConnection hConn, out string pszBuf, int cbBuf)
```

<para>/ 以文本格式返回详细的连接统计信息。适用于</para>
<para>/ 转储到日志等场景。</para>
<para>/</para>
<para>/ 返回值：</para>
<para>/ -1 失败（无效的连接句柄）</para>
<para>/ 0 成功，缓冲区已填充并以'\0'结尾</para>
<para>/ &gt;0 缓冲区为nullptr或空间过小导致文本被截断。</para>
<para>/ 请使用至少N字节的缓冲区重试。</para>

**参数:**

- `hConn` (`HSteamNetConnection`)
- `pszBuf` (`out string`)
- `cbBuf` (`int`)

**返回值:** `int`

**用法示例:**
```csharp
string statusBuf = new string('\0', 1024);
int result = SteamGameServerNetworkingSockets.GetDetailedConnectionStatus(hConn, out statusBuf, 1024);
```

### GetListenSocketAddress (静态)

```csharp
bool GetListenSocketAddress(HSteamListenSocket hSocket, out SteamNetworkingIPAddr address)
```

<para>/ 返回使用 CreateListenSocketIP 创建的监听套接字所绑定的本地 IP 和端口。</para>
<para>/</para>
<para>/ IPv6 地址 ::0 表示"任意 IPv4 或 IPv6"</para>
<para>/ IPv6 地址 ::ffff:0000:0000 表示"任意 IPv4"</para>

**参数:**

- `hSocket` (`HSteamListenSocket`)
- `address` (`out SteamNetworkingIPAddr`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamNetworkingIPAddr addr;
bool success = SteamGameServerNetworkingSockets.GetListenSocketAddress(listenSocket, out addr);
```

### CreateSocketPair (静态)

```csharp
bool CreateSocketPair(out HSteamNetConnection pOutConnection1, out HSteamNetConnection pOutConnection2, bool bUseNetworkLoopback, ref SteamNetworkingIdentity pIdentity1, ref SteamNetworkingIdentity pIdentity2)
```

<para>/ 创建一对相互通信的连接，例如回环连接。</para> <para>/ 这对于测试非常有用，或者使您的客户端/服务器代码在运行本地“服务器”时</para> <para>/ 也能以相同方式工作。</para> <para>/</para> <para>/ 这两个连接将立即进入已连接状态，并且不会立即触发任何回调。</para> <para>/ 之后，如果您关闭任一连接，另一个连接将收到回调，就像它们通过网络通信一样。</para> <para>/ 您必须关闭*两侧*连接才能完全清理资源！</para> <para>/</para> <para>/ 默认情况下，使用内部缓冲区，完全绕过网络、消息分片、加密、</para> <para>/ 有效载荷复制等操作。这意味着默认情况下，回环数据包不会模拟延迟或丢包。</para> <para>/ 将 bUseNetworkLoopback 设为 true 将使套接字对通过本地网络回环设备 (127.0.0.1)</para> <para>/ 在临时端口上发送数据包。在这种情况下支持模拟延迟和丢包，并且会消耗 CPU 时间</para> <para>/ 进行加密和解密。</para> <para>/</para> <para>/ 如果您希望为任一连接分配特定身份，可以传递特定的标识。</para> <para>/ 否则，如果传递 nullptr，相应的连接将采用通用的“localhost”身份。</para> <para>/ 如果使用真实的网络回环，这可能会被转换为实际绑定的回环端口。</para> <para>/ 否则，端口将为零。</para>

**参数:**

- `pOutConnection1` (`out HSteamNetConnection`)
- `pOutConnection2` (`out HSteamNetConnection`)
- `bUseNetworkLoopback` (`bool`)
- `pIdentity1` (`ref SteamNetworkingIdentity`)
- `pIdentity2` (`ref SteamNetworkingIdentity`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.CreateSocketPair(out var conn1, out var conn2, false, ref SteamNetworkingIdentity.Default, ref SteamNetworkingIdentity.Default);
```

### ConfigureConnectionLanes (静态)

```csharp
EResult ConfigureConnectionLanes(HSteamNetConnection hConn, int nNumLanes, out int pLanePriorities, out ushort pLaneWeights)
```

<para>/ 在连接上配置多个出站消息流（"车道"），并</para> <para>/ 控制它们之间的队头阻塞。同一车道内的消息</para> <para>/ 始终按入队顺序发送，但不同车道的消息</para> <para>/ 可能乱序发送。每个车道拥有独立的消息编号</para> <para>/ 序列。每个车道上发送的第一条消息将被分配编号 1。</para> <para>/</para> <para>/ 每个车道都有一个"优先级"。数值更高的车道仅会</para> <para>/ 在数值较低的所有车道清空时被处理。优先级数值的</para> <para>/ 大小关系无关紧要，仅排序顺序有意义。</para> <para>/</para> <para>/ 每个车道还被分配一个权重，用于控制该车道相对于</para> <para>/ 其他同优先级车道所消耗带宽的大致比例。（这假设</para> <para>/ 车道保持忙碌状态。空闲车道不会累积"信用额度"</para> <para>/ 以供消息入队后使用。）该值仅作为与其他同优先级</para> <para>/ 车道相比的比例有意义。对于不同优先级的车道，</para> <para>/ 严格的优先级顺序将生效，它们之间的相对权重无关。</para> <para>/ 因此，如果一个车道拥有唯一的优先级值，该车道的</para> <para>/ 权重值无关紧要。</para> <para>/</para> <para>/ 示例：3 个车道，优先级为 [ 0, 10, 10 ]，权重为 [ (不适用), 20, 5 ]。</para> <para>/ 第一个车道上发送的消息将始终优先于其他两个车道</para> <para>/ 发送。其权重值无关紧要，因为没有其他优先级=0 的车道。</para> <para>/ 另外两个车道将共享带宽，其中第二个和第三个车道</para> <para>/ 以约 4:1 的比例共享带宽。（权重 [ 不适用, 4, 1 ]</para> <para>/ 将等效。）</para> <para>/</para> <para>/ 注意：</para> <para>/ - 在编写本文时，部分代码的性能开销与车道数量成线性关系，</para> <para>/ 因此请将车道数量维持在绝对最小值。3 个左右即可；&gt;8 个就很多了。</para> <para>/ Steam 上最大车道数为 255，这是一个非常大的数字，不推荐！</para> <para>/ 如果您从源码编译此库，请参见 STEAMNETWORKINGSOCKETS_MAX_LANES。）</para> <para>/ - 车道优先级值可以是任意整数。其绝对值无关紧要，</para> <para>/ 仅顺序有意义。</para> <para>/ - 权重必须为正数，且由于实现细节，它们被限制为</para> <para>/ 16 位值。绝对大小不重要，仅比例有意义。</para> <para>/ - 在非 0 车道索引上发送的消息在线路上会有少量开销，</para> <para>/ 因此为最大化线路效率，车道 0 应作为"最常用"车道，</para> <para>/ 无论优先级或权重如何。</para> <para>/ - 连接默认只有一个车道。使用 nNumLanes=1 调用此函数</para> <para>/ 是合法的，但毫无意义，因为该情况下优先级和权重值无关。</para> <para>/ - 您可以随时重新配置连接的车道，但不允许减少车道数量。</para> <para>/ - 重新配置车道可能重启任何带宽共享均衡。通常您</para> <para>/ 会在连接初期调用此函数一次，可能是在交换几条消息之后。</para> <para>/ - 要为所有车道分配相同优先级，可使用 pLanePriorities=NULL。</para> <para>/ - 如果您希望所有同优先级车道均等共享带宽（或者</para> <para>/ 没有两个车道具有相同优先级值，因此优先级值无关），</para> <para>/ 可使用 pLaneWeights=NULL。</para> <para>/ - 优先级和权重决定了消息在线上发送的顺序。</para> <para>/ 不保证消息的接收顺序！由于丢包、</para> <para>/ 乱序交付以及数据包序列化的细微细节，消息</para> <para>/ 仍可能被轻微乱序接收！唯一强有力的保证是</para> <para>/ *同一车道*上的*可靠*消息将按发送顺序交付。</para> <para>/ - 每个主机配置其发送数据包的车

**参数:**

- `hConn` (`HSteamNetConnection`)
- `nNumLanes` (`int`)
- `pLanePriorities` (`out int`)
- `pLaneWeights` (`out ushort`)

**返回值:** `EResult`

**用法示例:**
```csharp
int[] priorities = { 0, 10, 10 }; ushort[] weights = { 1, 20, 5 }; SteamGameServerNetworkingSockets.ConfigureConnectionLanes(hConn, 3, out priorities[0], out weights[0]);
```

### GetIdentity (静态)

```csharp
bool GetIdentity(out SteamNetworkingIdentity pIdentity)
```

<para>身份与认证</para>
<para>/ 获取分配给此接口的身份标识。</para>
<para>/ 例如在Steam平台上，这是用户的SteamID；对于游戏服务器接口，则是分配给游戏服务器的SteamID。</para>
<para>/ 如果尚未获取到身份信息，则返回false并将结果设置为无效身份标识。</para>
<para>/ （例如：游戏服务器尚未登录。而在Steam平台上，即便用户未登录Steam，也能获知其SteamID。）</para>

**参数:**

- `pIdentity` (`out SteamNetworkingIdentity`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamNetworkingIdentity identity;
bool success = SteamGameServerNetworkingSockets.GetIdentity(out identity);
```

### InitAuthentication (静态)

```csharp
ESteamNetworkingAvailability InitAuthentication()
```

<para>/ 表明我们愿意准备好参与经过身份验证的通信。</para>
<para>/ 如果我们当前尚未就绪，则将采取必要步骤来获取所需的</para>
<para>/ 证书。（这包括我们自身的证书，以及任何用于验证对等方所需的</para>
<para>/ CA 证书。）</para>
<para>/</para>
<para>/ 如果您知道将要建立经过身份验证的连接，可以在程序初始化时调用此函数，</para>
<para>/ 以便在尝试这些连接时能立即就绪。（请注意，几乎所有连接都需要</para>
<para>/ 身份验证，除非是使用了 k_ESteamNetworkingConfig_IP_AllowWithoutAuth 禁用身份验证的</para>
<para>/ 普通 UDP 连接。）如果您不调用此函数，我们将等待需要使用这些资源的</para>
<para>/ 功能被启用。</para>
<para>/</para>
<para>/ 如果发生失败，您也可以调用此函数强制重试。</para>
<para>/ 一旦我们尝试并失败后，将不会自动重试。</para>
<para>/ 在这方面，系统在尝试并失败后的行为与首次尝试前相同：</para>
<para>/ 尝试经过身份验证的通信或调用此函数将触发系统尝试获取必要的资源。</para>
<para>/</para>
<para>/ 您可以使用 GetAuthenticationStatus 或监听 SteamNetAuthenticationStatus_t</para>
<para>/ 来监控状态。</para>
<para>/</para>
<para>/ 返回当前将从 GetAuthenticationStatus 获取的值。</para>

**返回值:** `ESteamNetworkingAvailability`

**用法示例:**
```csharp
ESteamNetworkingAvailability status = SteamGameServerNetworkingSockets.InitAuthentication();
```

### GetAuthenticationStatus (静态)

```csharp
ESteamNetworkingAvailability GetAuthenticationStatus(out SteamNetAuthenticationStatus_t pDetails)
```

<para>/ 查询我们参与认证通信的准备状态。当此状态发生任何变化时，会触发</para> <para>/ SteamNetAuthenticationStatus_t 回调，但您也可以随时使用此函数进行查询。</para> <para>/</para> <para>/ 返回 SteamNetAuthenticationStatus_t::m_eAvail 的值。如果您仅需要</para> <para>/ 这一高级状态，可将 pDetails 设为 NULL。若需获取进一步详情，</para> <para>/ 则传入非 NULL 值以接收它们。</para>

**参数:**

- `pDetails` (`out SteamNetAuthenticationStatus_t`)

**返回值:** `ESteamNetworkingAvailability`

**用法示例:**
```csharp
SteamNetAuthenticationStatus_t status;
var availability = SteamGameServerNetworkingSockets.GetAuthenticationStatus(out status);
```

### CreatePollGroup (静态)

```csharp
HSteamNetPollGroup CreatePollGroup()
```

<para> 轮询组。轮询组是一组可以高效轮询的连接。</para>
<para> （在我们的API中，“轮询”一个连接意味着检索所有待处理消息。我们</para>
<para> 实际上并没有像BSD套接字那样用于轮询连接*状态*的API。）</para>
<para>/ 创建一个新的轮询组。</para>
<para>/</para>
<para>/ 使用完毕后，应通过DestroyPollGroup销毁该轮询组。</para>

**返回值:** `HSteamNetPollGroup`

**用法示例:**
```csharp
HSteamNetPollGroup pollGroup = SteamGameServerNetworkingSockets.CreatePollGroup();
```

### DestroyPollGroup (静态)

```csharp
bool DestroyPollGroup(HSteamNetPollGroup hPollGroup)
```

<para>/ 销毁通过 CreatePollGroup() 创建的轮询组。</para>
<para>/</para>
<para>/ 如果轮询组中存在任何连接，这些连接将从组中移除，</para>
<para>/ 并置于不归属于任何轮询组的状态。</para>
<para>/ 若传入无效的轮询组句柄，则返回 false。</para>

**参数:**

- `hPollGroup` (`HSteamNetPollGroup`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerNetworkingSockets.DestroyPollGroup(pollGroupHandle);
```

### SetConnectionPollGroup (静态)

```csharp
bool SetConnectionPollGroup(HSteamNetConnection hConn, HSteamNetPollGroup hPollGroup)
```

<para>/ 将连接分配到一个轮询组。注意，一个连接仅可属于一个</para> <para>/ 轮询组。将连接添加到一个轮询组将隐式地将其从</para> <para>/ 任何其他所属的轮询组中移除。</para> <para>/</para> <para>/ 你可以传入 k_HSteamNetPollGroup_Invalid 以将连接从其当前</para> <para>/ 轮询组中移除，而不将其添加到新的轮询组。</para> <para>/</para> <para>/ 如果该连接上当前有待处理的已接收消息，系统将尝试</para> <para>/ 以大致上如果连接在消息接收时已属于该轮询组</para> <para>/ 所应具有的顺序，将这些消息添加到该轮询组的消息队列中。</para> <para>/</para> <para>/ 如果连接句柄无效，或轮询组句柄无效（且不等于 k_HSteamNetPollGroup_Invalid），</para> <para>/ 则返回 false。</para>

**参数:**

- `hConn` (`HSteamNetConnection`)
- `hPollGroup` (`HSteamNetPollGroup`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerNetworkingSockets.SetConnectionPollGroup(hConn, hPollGroup);
```

### ReceiveMessagesOnPollGroup (静态)

```csharp
int ReceiveMessagesOnPollGroup(HSteamNetPollGroup hPollGroup, IntPtr[] ppOutMessages, int nMaxMessages)
```

<para>与ReceiveMessagesOnConnection相同，但会返回轮询组中任何连接上可用的下一条消息。</para>  
<para>请检查SteamNetworkingMessage_t::m_conn以确定是哪个连接。（SteamNetworkingMessage_t::m_nConnUserData也可能有用。）</para>  
<para>/</para>  
<para>不同连接之间的消息投递顺序通常与完成消息的最后一个数据包的接收顺序一致。但这不是一个强保证，特别是当连接刚刚被分配到轮询组时收到的数据包。</para>  
<para>/</para>  
<para>同一连接上的消息投递顺序有明确的规定，并且与ReceiveMessagesOnConnection中提到的保证相同。</para>  
<para>（但消息不会按连接分组，因此它们不一定会连续出现在列表中；它们可能与其他连接的消息交错排列。）</para>

**参数:**

- `hPollGroup` (`HSteamNetPollGroup`)
- `ppOutMessages` (`IntPtr[]`)
- `nMaxMessages` (`int`)

**返回值:** `int`

**用法示例:**
```csharp
var messages = new IntPtr[10];
int count = SteamGameServerNetworkingSockets.ReceiveMessagesOnPollGroup(pollGroup, messages, 10);
```

### ReceivedRelayAuthTicket (静态)

```csharp
bool ReceivedRelayAuthTicket(IntPtr pvTicket, int cbTicket, out SteamDatagramRelayAuthTicket pOutParsedTicket)
```

<para> 连接至数据中心托管专用服务器的客户端，</para> <para> 使用由您的游戏协调器颁发的票据。如果您未自行</para> <para> 颁发票据以限制哪些玩家可以尝试连接</para> <para> 至您的服务器，则无需使用这些功能。</para> <para>/ 从后端/匹配系统收到票据时调用此函数。将票据</para> <para>/ 存入持久缓存，并可选返回已解析的票据。</para> <para>/</para> <para>/ 详见 stamdatagram_ticketgen.h。</para>

**参数:**

- `pvTicket` (`IntPtr`)
- `cbTicket` (`int`)
- `pOutParsedTicket` (`out SteamDatagramRelayAuthTicket`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.ReceivedRelayAuthTicket(ticketPtr, ticketLength, out SteamDatagramRelayAuthTicket parsedTicket);
```

### FindRelayAuthTicketForServer (静态)

```csharp
int FindRelayAuthTicketForServer(ref SteamNetworkingIdentity identityGameServer, int nRemoteVirtualPort, out SteamDatagramRelayAuthTicket pOutParsedTicket)
```

<para>在缓存中搜索与指定虚拟端口上的服务器通信的票证。</para>
<para>如果找到，返回票证过期前的剩余秒数，并可选择返回</para>
<para>完整的破解票证。如果没有票证则返回0。</para>
<para>/</para>
<para>通常，这仅用于确认您拥有票证，然后</para>
<para>调用ConnectToHostedDedicatedServer连接到服务器。</para>

**参数:**

- `identityGameServer` (`ref SteamNetworkingIdentity`)
- `nRemoteVirtualPort` (`int`)
- `pOutParsedTicket` (`out SteamDatagramRelayAuthTicket`)

**返回值:** `int`

**用法示例:**
```csharp
SteamNetworkingIdentity identity = default;
int seconds = SteamGameServerNetworkingSockets.FindRelayAuthTicketForServer(ref identity, 0, out SteamDatagramRelayAuthTicket ticket);
```

### ConnectToHostedDedicatedServer (静态)

```csharp
HSteamNetConnection ConnectToHostedDedicatedServer(ref SteamNetworkingIdentity identityTarget, int nRemoteVirtualPort, int nOptions, SteamNetworkingConfigValue_t[] pOptions)
```

<para>/ 客户端调用，用于连接到托管在Valve数据中心指定虚拟端口的服务器。</para> <para>/ 你必须已将此服务器的票据存入缓存，否则此连接</para> <para>/ 尝试将失败！如果你不自行签发票据，则要通过SDR以自动票据模式连接至专用</para> <para>/ 服务器，请使用ConnectP2P。（服务器必须通过使用CreateListenSocketP2P进行监听来配置为允许</para> <para>/ 此类连接。）</para> <para>/</para> <para>/ 你可能会疑惑为什么票据存储在缓存中，而不是直接作为参数传入</para> <para>/ 此处。原因是为了使游戏服务器的重新连接更加稳健，即使客户端计算机与</para> <para>/ Steam或中央后端断开连接，或应用重启、崩溃等。</para> <para>/</para> <para>/ 如果你使用此接口，可能需要在应用初始化时调用ISteamNetworkingUtils::InitRelayNetworkAccess()</para> <para>/</para> <para>/ 如果你需要设置任何初始配置选项，请在此处传入。参见</para> <para>/ SteamNetworkingConfigValue_t以了解为何这比</para> <para>/ 在创建后“立即”设置选项更优。</para>

**参数:**

- `identityTarget` (`ref SteamNetworkingIdentity`)
- `nRemoteVirtualPort` (`int`)
- `nOptions` (`int`)
- `pOptions` (`SteamNetworkingConfigValue_t[]`)

**返回值:** `HSteamNetConnection`

**用法示例:**
```csharp
SteamNetworkingIdentity identity = default;
var connection = SteamGameServerNetworkingSockets.ConnectToHostedDedicatedServer(ref identity, 0, 0, null);
```

### GetHostedDedicatedServerPort (静态)

```csharp
ushort GetHostedDedicatedServerPort()
```

<para> 托管在Valve中继网络已知的数据中心的服务器</para>  
<para>/ 返回SDR_LISTEN_PORT环境变量的值。此</para>  
<para>/ 端口为您的服务器将要监听的UDP服务器端口。在生产环境中，</para>  
<para>/ 此端口将自动为您配置。</para>  
<para>/</para>  
<para>/ 在开发环境中，您需要自行设置。请参阅</para>  
<para>/ https://partner.steamgames.com/doc/api/ISteamNetworkingSockets</para>  
<para>/ 了解有关如何配置开发环境的更多信息。</para>

**返回值:** `ushort`

**用法示例:**
```csharp
ushort port = SteamGameServerNetworkingSockets.GetHostedDedicatedServerPort();
```

### GetHostedDedicatedServerPOPID (静态)

```csharp
SteamNetworkingPOPID GetHostedDedicatedServerPOPID()
```

<para>/ 如果未设置 SDR_LISTEN_PORT，则返回 0。否则，返回服务器所在的数据中心。</para> <para>/ 在非生产环境中，这将返回 k_SteamDatagramPOPID_dev。</para>

**返回值:** `SteamNetworkingPOPID`

**用法示例:**
```csharp
var popid = SteamGameServerNetworkingSockets.GetHostedDedicatedServerPOPID();
```

### GetHostedDedicatedServerAddress (静态)

```csharp
EResult GetHostedDedicatedServerAddress(out SteamDatagramHostedAddress pRouting)
```

<para>/ 返回关于托管服务器的信息。这包含服务器的PoPID，</para> <para>/ 以及中继可用于将流量发送到您服务器的不透明路由信息。</para> <para>/</para> <para>/ 您需要将此信息发送至后端，并将其放入票据中，</para> <para>/ 以便中继知道如何将客户端的流量转发到您的服务器。</para> <para>/ 更多信息请参见SteamDatagramRelayAuthTicket。</para> <para>/</para> <para>/ 此外，请注意路由信息包含在SteamDatagramGameCoordinatorServerLogin中，</para> <para>/ 因此如果可能，建议使用GetGameCoordinatorServerLogin将此信息发送到您的</para> <para>/ 游戏协调服务，同时安全地完成登录。</para> <para>/</para> <para>/ 成功退出时，返回k_EResultOK</para> <para>/</para> <para>/ 不成功退出：</para> <para>/ - 返回k_EResultOK以外的值。</para> <para>/ - k_EResultInvalidState：未配置为监听SDR（未设置SDR_LISTEN_SOCKET）。</para> <para>/ - k_EResultPending：我们尚未（或尚未）拥有所需的身份验证信息。</para> <para>/ （参见GetAuthenticationStatus。）如果您使用环境变量预取网络配置，</para> <para>/ 这些数据应始终立即可用。</para> <para>/ - 描述失败原因的非本地化诊断调试消息将放入m_data中。</para> <para>/</para> <para>/ 注意：返回的数据块未加密。请将其发送到您的后端，但不要</para> <para>/ 直接与客户端共享。</para>

**参数:**

- `pRouting` (`out SteamDatagramHostedAddress`)

**返回值:** `EResult`

**用法示例:**
```csharp
SteamDatagramHostedAddress address;
EResult result = SteamGameServerNetworkingSockets.GetHostedDedicatedServerAddress(out address);
```

### CreateHostedDedicatedServerListenSocket (静态)

```csharp
HSteamListenSocket CreateHostedDedicatedServerListenSocket(int nLocalVirtualPort, int nOptions, SteamNetworkingConfigValue_t[] pOptions)
```

<para>/ 在指定虚拟端口上创建监听套接字。实际使用的UDP端口</para> <para>/ 将由SDR_LISTEN_PORT环境变量决定。若未配置UDP端口，</para> <para>/ 此调用将失败。</para> <para>/</para> <para>/ 此调用必须通过SteamGameServerNetworkingSockets()接口进行。</para> <para>/</para> <para>/ 当您使用票据生成器库签发自有票据时，应使用此函数。</para> <para>/ 连接到此虚拟端口服务器的客户端将需要一张票据，且必须使用</para> <para>/ ConnectToHostedDedicatedServer进行连接。</para> <para>/</para> <para>/ 如需设置任何初始配置选项，请在此处传入。参见</para> <para>/ SteamNetworkingConfigValue_t了解为何这优于在创建后</para> <para>/ "立即"设置选项。</para>

**参数:**

- `nLocalVirtualPort` (`int`)
- `nOptions` (`int`)
- `pOptions` (`SteamNetworkingConfigValue_t[]`)

**返回值:** `HSteamListenSocket`

**用法示例:**
```csharp
var socket = SteamGameServerNetworkingSockets.CreateHostedDedicatedServerListenSocket(0, 0, null);
```

### GetGameCoordinatorServerLogin (静态)

```csharp
EResult GetGameCoordinatorServerLogin(IntPtr pLoginInfo, out int pcbSignedBlob, IntPtr pBlob)
```

<para>/ 生成一个可用于通过 SteamDatagram_ParseHostedServerLogin 安全登录后端的身份验证数据块。（参见</para> <para>/ steamdatagram_gamecoordinator.h）</para> <para>/</para> <para>/ 调用函数前：</para> <para>/ - 填充 pLoginInfo 中的应用数据（m_cbAppData 和 m_appData）。你无需初始化</para> <para>/ 所有其他字段。</para> <para>/ - *pcbSignedBlob 包含 pBlob 指向的缓冲区大小（应至少为</para> <para>/ k_cbMaxSteamDatagramGameCoordinatorServerLoginSerialized）。</para> <para>/</para> <para>/ 成功退出时：</para> <para>/ - 返回 k_EResultOK</para> <para>/ - pLoginInfo 的所有剩余字段将被填充。</para> <para>/ - *pcbSignedBlob 包含已放入 pBlob 的序列化数据块大小。</para> <para>/</para> <para>/ 失败退出时：</para> <para>/ - 返回非 k_EResultOK 的值。</para> <para>/ - k_EResultNotLoggedOn：你尚未（或还未）登录</para> <para>/ - 更多可能的失败返回值请参见 GetHostedDedicatedServerAddress。</para> <para>/ - 描述失败原因的非本地化诊断调试信息将被放入 pBlob。</para> <para>/</para> <para>/ 此功能通过使用颁发给该服务器的证书对 SteamDatagramGameCoordinatorServerLogin 的内容进行签名来实现。</para> <para>/ 在开发环境中，没有证书也可以。（你需要先在 SteamDatagram_ParseHostedServerLogin 中启用不安全的开发登录。）</para> <para>/ 否则，你将需要一个已签名的证书。</para> <para>/</para> <para>/ 注意：此处返回的路由数据块未加密。请将其发送到你的后端，</para> <para>/ 不要直接与客户端共享。</para>

**参数:**

- `pLoginInfo` (`IntPtr`)
- `pcbSignedBlob` (`out int`)
- `pBlob` (`IntPtr`)

**返回值:** `EResult`

**用法示例:**
```csharp
var result = SteamGameServerNetworkingSockets.GetGameCoordinatorServerLogin(pLoginInfo, out int pcbSignedBlob, pBlob);
```

### ConnectP2PCustomSignaling (静态)

```csharp
HSteamNetConnection ConnectP2PCustomSignaling(out ISteamNetworkingConnectionSignaling pSignaling, ref SteamNetworkingIdentity pPeerIdentity, int nRemoteVirtualPort, int nOptions, SteamNetworkingConfigValue_t[] pOptions)
```

<para> 使用自定义信令协议的中继连接</para>
<para> 当您拥有通过相互信任的通道发送带外信令/会合消息的独立方法时使用</para>
<para> 创建通过自定义信令/会合通道进行信令的P2P“客户端”连接</para>
<para></para>
<para> pSignaling指向您为此连接创建的新对象</para>
<para> 该对象必须保持有效直到调用Release()。将对象传递给此函数后，</para>
<para> 所有权即转移。如果调用失败，Release()将从函数内部调用。此外，在Release()</para>
<para> 被调用之前，您需要准备好从任何线程调用该对象的方法！必须确保对象是线程安全的！</para>
<para> 并且应确保尽可能快速地调度这些方法。</para>
<para></para>
<para> 此函数将立即构建一个处于“连接中”状态的连接。不久之后（可能在此函数返回之前，也可能在另一个线程中），</para>
<para> 连接将通过调用ISteamNetworkingConnectionSignaling::SendSignal开始发送信令消息。</para>
<para></para>
<para> 当远程对等端接受连接时（参见ISteamNetworkingSignalingRecvContext::OnConnectRequest），</para>
<para> 它将开始发送信令消息。收到这些消息后，可以使用ReceivedP2PCustomSignal将其传递给连接。</para>
<para></para>
<para> 如果您知道预期对端身份，可以传递其身份以改进调试输出或检测错误。</para>
<para> 如果尚不知道其身份，可以传递NULL，身份将在连接握手过程中建立。</para>
<para></para>
<para> 如果使用此功能，建议在应用初始化时调用ISteamNetworkingUtils::InitRelayNetworkAccess()</para>
<para></para>
<para> 如果需要设置任何初始配置选项，请在此处传递。关于为何这优于创建后“立即”设置选项，</para>
<para> 请参阅SteamNetworkingConfigValue_t以获取更多信息。</para>

**参数:**

- `pSignaling` (`out ISteamNetworkingConnectionSignaling`)
- `pPeerIdentity` (`ref SteamNetworkingIdentity`)
- `nRemoteVirtualPort` (`int`)
- `nOptions` (`int`)
- `pOptions` (`SteamNetworkingConfigValue_t[]`)

**返回值:** `HSteamNetConnection`

**用法示例:**
```csharp
var conn = SteamGameServerNetworkingSockets.ConnectP2PCustomSignaling(out var signaling, ref peerIdentity, 0, 0, null);
```

### ReceivedP2PCustomSignal (静态)

```csharp
bool ReceivedP2PCustomSignal(IntPtr pMsg, int cbMsg, out ISteamNetworkingSignalingRecvContext pContext)
```

<para>/ 当自定义信令接收到消息时调用。当您的</para> <para>/ 信令通道收到消息时，应将信封中的任何</para> <para>/ 路由信息保存到上下文对象中，</para> <para>/ 然后将有效载荷传递给此函数。</para> <para>/</para> <para>/ 根据消息的不同，接下来可能发生几种情况：</para> <para>/</para> <para>/ - 如果信令与现有连接关联，则立即处理。</para> <para>/ 如果需要发送任何回复，将使用与该连接关联的</para> <para>/ ISteamNetworkingConnectionSignaling 进行分发。</para> <para>/ - 如果消息表示连接请求（且该请求</para> <para>/ 不是对现有连接的冗余请求），则将创建</para> <para>/ 新连接，并调用您的上下文对象上的 ReceivedConnectRequest</para> <para>/ 以确定后续操作。</para> <para>/ - 否则，该消息针对一个（已）不存在的</para> <para>/ 连接。在这种情况下，我们*可能*会调用您的</para> <para>/ 上下文对象上的 SendRejectionReply。</para> <para>/</para> <para>/ 无论何种情况，在此函数返回后，我们不会保存 pContext 或访问它。</para> <para>/</para> <para>/ 如果消息被解析并分发，且未发生任何异常或可疑情况，则返回 true。</para> <para>/ 如果消息存在某些问题导致无法正常处理，则返回 false。（调试输出中</para> <para>/ 通常会包含更多信息。）</para> <para>/</para> <para>/ 如果您期望使用中继连接，则可能需要在应用初始化时</para> <para>/ 调用 ISteamNetworkingUtils::InitRelayNetworkAccess()</para>

**参数:**

- `pMsg` (`IntPtr`)
- `cbMsg` (`int`)
- `pContext` (`out ISteamNetworkingSignalingRecvContext`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = SteamGameServerNetworkingSockets.ReceivedP2PCustomSignal(pMsg, cbMsg, out ISteamNetworkingSignalingRecvContext context);
```

### GetCertificateRequest (静态)

```csharp
bool GetCertificateRequest(out int pcbBlob, IntPtr pBlob, out SteamNetworkingErrMsg errMsg)
```

<para> 由应用程序提供证书。在Steam上，我们通常自动处理所有相关事项</para> <para> 您无需使用这些高级功能。</para> <para>/ 获取描述证书请求的数据块。您可以将此数据发送给您的游戏协调器。</para> <para>/ 输入时，*pcbBlob 应包含缓冲区的大小。成功退出时，它将</para> <para>/ 返回已填充的字节数。您可以传递 pBlob=NULL 来查询所需</para> <para>/ 的大小。（512字节是一个保守估计值。）</para> <para>/</para> <para>/ 将此数据块传递给您的游戏协调器并调用 SteamDatagram_CreateCert。</para>

**参数:**

- `pcbBlob` (`out int`)
- `pBlob` (`IntPtr`)
- `errMsg` (`out SteamNetworkingErrMsg`)

**返回值:** `bool`

**用法示例:**
```csharp
int blobSize = 512;
SteamGameServerNetworkingSockets.GetCertificateRequest(out blobSize, System.IntPtr.Zero, out var errMsg);
```

### SetCertificate (静态)

```csharp
bool SetCertificate(IntPtr pCertificate, int cbCertificate, out SteamNetworkingErrMsg errMsg)
```

<para>设置证书。证书数据块应为</para>
<para>SteamDatagram_CreateCert 的输出结果。</para>

**参数:**

- `pCertificate` (`IntPtr`)
- `cbCertificate` (`int`)
- `errMsg` (`out SteamNetworkingErrMsg`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamNetworkingErrMsg errMsg;
bool result = SteamGameServerNetworkingSockets.SetCertificate(certPtr, certSize, out errMsg);
```

### ResetIdentity (静态)

```csharp
void ResetIdentity(ref SteamNetworkingIdentity pIdentity)
```

<para>重置与此实例关联的身份标识。</para>
<para>所有打开的连接将被关闭。任何先前的证书等将被丢弃。</para>
<para>你可以传入一个想要使用的特定身份标识，也可以传入NULL，</para>
<para>在这种情况下，该身份标识将保持无效，直到你使用SetCertificate进行设置。</para>
<para></para>
<para>注意：此功能实际上在Steam上不受支持！</para>
<para>它被包含进来用于其他平台，在这些平台上活跃用户可以登出，</para>
<para>而新用户可以登入。</para>

**参数:**

- `pIdentity` (`ref SteamNetworkingIdentity`)

**用法示例:**
```csharp
SteamNetworkingIdentity identity = default;
SteamGameServerNetworkingSockets.ResetIdentity(ref identity);
```

### RunCallbacks (静态)

```csharp
void RunCallbacks()
```

<para> 杂项</para> <para>/ 调用为此接口排队的全部回调函数。</para> <para>/ 参见 k_ESteamNetworkingConfig_Callback_ConnectionStatusChanged 等。</para> <para>/</para> <para>/ 若您正在使用 Steam 的回调分发机制</para> <para>/ (SteamAPI_RunCallbacks 和 SteamGameserver_RunCallbacks)，则无需调用此方法。</para>

**用法示例:**
```csharp
SteamGameServerNetworkingSockets.RunCallbacks();
```

### BeginAsyncRequestFakeIP (静态)

```csharp
bool BeginAsyncRequestFakeIP(int nNumPorts)
```

<para> “假 IP”系统。</para>  
<para> 假 IP 本质上是一个临时性的、任意指定的标识符，</para>  
<para> 碰巧是一个有效的 IPv4 地址。该系统的目的是为了</para>  
<para> 便于与使用 IPv4 地址识别主机的现有代码进行集成。</para>  
<para> 该假 IP 地址永远不会实际用于在互联网上发送或接收任何数据包，</para>  
<para> 它严格来说只是一个标识符。</para>  
<para> 假 IP 地址的设计目标是（希望）尽可能透明地通过现有代码，</para>  
<para> 同时尽可能少地与网络中（包括互联网和局域网）实际使用的</para>  
<para> “真实”地址发生冲突。在编写此注释时，这些地址来自</para>  
<para> 169.254.0.0/16 范围，且端口号始终 >1024。然而，</para>  
<para> 这一点可能会发生变化！请勿对这些地址做出任何假设，</para>  
<para> 否则您的代码将来可能会出现问题。特别是，您应使用</para>  
<para> 诸如 ISteamNetworkingUtils::IsFakeIP 之类的函数来判断一个 IP</para>  
<para> 地址是否为此系统使用的“假”地址。</para>  
<para>/ 开始异步进程，分配一个假 IPv4 地址，以便其他</para>  
<para>/ 对等端可以通过 P2P 联系我们。此函数返回的 IP</para>  
<para>/ 地址对于给定的 appid 是全局唯一的。</para>  
<para>/</para>  
<para>/ nNumPorts 是您希望保留的端口数量。这对于</para>  
<para>/ 监听多个 UDP 端口以处理不同类型流量类似的原因很有用。</para>  
<para>/ 由于这些分配来自全局命名空间，因此您可请求的最大端口</para>  
<para>/ 数量有相对严格的限制。（在编写本文时，限制为 4。）</para>  
<para>/ 端口分配*不*保证具有任何特定的顺序或关系！</para>  
<para>/ *切勿*假设它们是连续的，即使在实践中可能经常如此。</para>  
<para>/</para>  
<para>/ 如果请求已在处理中，则返回 false；如果新请求已启动，</para>  
<para>/ 则返回 true。当请求完成时，将发布一个</para>  
<para>/ SteamNetworkingFakeIPResult_t 回调。</para>  
<para>/</para>  
<para>/ 对于游戏服务器，您*必须*在初始化 SDK 之后、开始登录之前</para>  
<para>/ 调用此函数。Steam 需要提前知道将使用假 IP。</para>  
<para>/ 通常显示您公共 IP 的所有位置（例如服务器浏览器）都将</para>  
<para>/ 被替换为假 IP 和索引 0 的假端口。该请求实际上会被排队</para>  
<para>/ 直到登录完成，因此您不能在分配完成之前等待并阻塞登录。</para>  
<para>/ 除了可以在本地检测到的简单故障（例如无效参数）外，</para>  
<para>/ SteamNetworkingFakeIPResult_t 回调（无论是成功还是失败）</para>  
<para>/ 将只在登录之后才会发布。此外，假 IP 分配被视为</para>  
<para>/ 应用程序正常运行所必需，因此在*多次*重试尝试后才会报告失败。</para>  
<para>/ 此过程可能持续数分钟。*强烈*建议将失败视为致命错误。</para>  
<para>/</para>  
<para>/ 要使用面向连接（TCP 风格）的 API 进行通信：</para>  
<para>/ - 服务器使用 CreateListenSocketP2PFakeIP 创建监听套接字</para>  
<para>/ - 客户端使用 ConnectByIPAddress 连接，传入假 IP 地址。</para>  
<para>/ - 该连接的行为将类似于 P2P 连接。在</para>  
<para>/ SteamNetConnectionInfo_t 中出现的身份将是假 IP 身份，直到</para>  
<para>/ 我们获知真实身份。之后将变为真实身份。如果</para>  
<para>/ SteamNetConnectionInfo_t::m_addrRemote 有效，则它将是</para>  
<para>/ NAT 打洞连接的真实 IPv4 地址。否则，它将无效。</para>  
<para>/</para>  
<para>/

**参数:**

- `nNumPorts` (`int`)

**返回值:** `bool`

**用法示例:**
```csharp
bool requested = SteamGameServerNetworkingSockets.BeginAsyncRequestFakeIP(1);
```

### GetFakeIP (静态)

```csharp
void GetFakeIP(int idxFirstPort, out SteamNetworkingFakeIPResult_t pInfo)
```

<para>/ 返回有关我们被分配的FakeIP和端口的信息，</para> <para>/ 如果有的话。idxFirstPort当前为保留字段且必须为零。</para> <para>/ 请务必检查SteamNetworkingFakeIPResult_t::m_eResult</para>

**参数:**

- `idxFirstPort` (`int`)
- `pInfo` (`out SteamNetworkingFakeIPResult_t`)

**用法示例:**
```csharp
SteamNetworkingFakeIPResult_t result;
SteamGameServerNetworkingSockets.GetFakeIP(0, out result);
```

### CreateListenSocketP2PFakeIP (静态)

```csharp
HSteamListenSocket CreateListenSocketP2PFakeIP(int idxFakePort, int nOptions, SteamNetworkingConfigValue_t[] pOptions)
```

<para>/ 创建一个监听套接字，用于监听发送到我们FakeIP的P2P连接。</para>
<para>/ 对等方可以通过调用ConnectByIPAddress来发起到此监听套接字的连接。</para>
<para>/</para>
<para>/ idxFakePort指的是所请求的**虚拟端口索引**，而非实际端口号。</para>
<para>/ 例如，传递0表示保留中的第一个端口。</para>
<para>/ 只有在调用BeginAsyncRequestFakeIP之后才能调用此方法。</para>
<para>/ 但是，在创建监听套接字之前无需等待请求完成。</para>

**参数:**

- `idxFakePort` (`int`)
- `nOptions` (`int`)
- `pOptions` (`SteamNetworkingConfigValue_t[]`)

**返回值:** `HSteamListenSocket`

**用法示例:**
```csharp
var socket = SteamGameServerNetworkingSockets.CreateListenSocketP2PFakeIP(0, 0, null);
```

### GetRemoteFakeIPForConnection (静态)

```csharp
EResult GetRemoteFakeIPForConnection(HSteamNetConnection hConn, out SteamNetworkingIPAddr pOutAddr)
```

<para>/ 如果连接是使用"FakeIP"系统发起的，那么</para> <para>/ 我们可以获取远程主机的IP地址。如果远程主机在</para> <para>/ 建立连接时拥有全局FakeIP，此函数将返回该全局IP。</para> <para>/ 否则，将从本地FakeIP地址空间中分配一个本地唯一的</para> <para>/ FakeIP，并将其返回。</para> <para>/</para> <para>/ 本地FakeIP的分配会尝试以一致的方式分配地址。</para> <para>/ 如果与同一远程主机建立了多个连接，它们*可能*会返回</para> <para>/ 相同的FakeIP。但由于命名空间有限，这无法保证。</para> <para>/</para> <para>/ 失败时返回：</para> <para>/ - k_EResultInvalidParam：无效的连接句柄</para> <para>/ - k_EResultIPNotFound：该连接未使用FakeIP系统建立</para>

**参数:**

- `hConn` (`HSteamNetConnection`)
- `pOutAddr` (`out SteamNetworkingIPAddr`)

**返回值:** `EResult`

**用法示例:**
```csharp
EResult result = SteamGameServerNetworkingSockets.GetRemoteFakeIPForConnection(hConn, out SteamNetworkingIPAddr addr);
```

### CreateFakeUDPPort (静态)

```csharp
IntPtr CreateFakeUDPPort(int idxFakeServerPort)
```

<para>获取一个可像UDP端口一样用于向FakeIP地址发送/接收数据报的接口。此接口旨在简化将现有基于UDP的代码移植以利用SDR的过程。</para>
<para>idxFakeServerPort指使用BeginAsyncRequestFakeIP分配的端口索引，用于创建“服务器”端口。你可以在分配完成前调用此方法。但在分配成功之前，任何发送数据包的尝试都将失败。当对端收到从此接口发送的数据包时，数据包的源地址将是全局唯一的FakeIP。如果你多次调用此函数并传入相同的（非负）虚拟端口索引，将返回同一对象，且该对象不进行引用计数。</para>
<para>要创建“客户端”端口（例如临时UDP端口的等效项），请传入-1。在这种情况下，每次调用都会返回一个不同的对象。当对端收到从此接口发送的数据包时，对端将从其本地控制的命名空间分配一个FakeIP。</para>

**参数:**

- `idxFakeServerPort` (`int`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
var serverPort = SteamGameServerNetworkingSockets.CreateFakeUDPPort(0);
var clientPort = SteamGameServerNetworkingSockets.CreateFakeUDPPort(-1);
```

