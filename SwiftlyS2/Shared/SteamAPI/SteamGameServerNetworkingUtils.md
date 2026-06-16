<a id="steamgameservernetworkingutils"></a>

# 📦 SteamGameServerNetworkingUtils

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### AllocateMessage (静态)

```csharp
IntPtr AllocateMessage(int cbAllocateBuffer)
```

<para> 高效消息发送</para> <para>/ 分配并初始化一个消息对象。通常调用此方法</para> <para>/ 的目的是将其传递给 ISteamNetworkingSockets::SendMessages。</para> <para>/ 返回的对象会将所有相关字段清零。</para> <para>/</para> <para>/ 可选地，你也可以请求系统分配空间来</para> <para>/ 容纳有效载荷本身。如果 cbAllocateBuffer 非零，系统</para> <para>/ 将分配至少 cbAllocateBuffer 字节的内存来容纳有效载荷。</para> <para>/ m_pData 将指向分配的缓冲区，m_cbSize 将被设置为该</para> <para>/ 大小，m_pfnFreeData 将被设置为释放缓冲区的正确函数。</para> <para>/</para> <para>/ 如果 cbAllocateBuffer=0，则不分配缓冲区。m_pData 将为 NULL，</para> <para>/ m_cbSize 为零，m_pfnFreeData 将为 NULL。你需要手动设置这些字段。</para>

**参数:**

- `cbAllocateBuffer` (`int`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr message = SteamGameServerNetworkingUtils.AllocateMessage(1024);
```

### InitRelayNetworkAccess (静态)

```csharp
void InitRelayNetworkAccess()
```

<para> 访问 Steam 数据报中继 (SDR) 网络</para>
<para> 初始化与状态检查</para>
<para>/ 如果你已知将使用中继网络（例如，</para>
<para>/ 因为预计会建立 P2P 连接），请调用此方法初始化</para>
<para>/ 中继网络。若不调用此方法，初始化将</para>
<para>/ 延迟至首次使用需要访问中继网络的功能时，</para>
<para>/ 从而导致首次访问延迟。</para>
<para>/</para>
<para>/ 若先前尝试失败，你也可以调用此方法强制重试。</para>
<para>/ 执行任何需要访问中继网络的操作也会</para>
<para>/ 触发重试，因此调用此函数并非严格必要，</para>
<para>/ 但若预计需要使用中继网络，</para>
<para>/ 在程序启动时调用它可能很有用。</para>
<para>/</para>
<para>/ 使用 GetRelayNetworkStatus 或监听 SteamRelayNetworkStatus_t</para>
<para>/ 回调以了解初始化何时完成。</para>
<para>/ 通常初始化会在几秒内完成。</para>
<para>/</para>
<para>/ 注意：位于已知数据中心的专用服务器*无需*</para>
<para>/ 调用此方法，因为它们不进行路由决策。然而，如果</para>
<para>/ 专用服务器将使用 P2P 功能，它将充当</para>
<para>/ “客户端”，此时应调用此方法。</para>

**用法示例:**
```csharp
SteamGameServerNetworkingUtils.InitRelayNetworkAccess();
```

### GetRelayNetworkStatus (静态)

```csharp
ESteamNetworkingAvailability GetRelayNetworkStatus(out SteamRelayNetworkStatus_t pDetails)
```

<para>/ 获取中继网络的当前状态。</para> <para>/</para> <para>/ SteamRelayNetworkStatus_t 也是一个回调。当状态发生变化，</para> <para>/ 或 ping 测量开始/停止时，它会在用户和游戏服务器接口上触发。</para> <para>/</para> <para>/ 返回 SteamRelayNetworkStatus_t::m_eAvail。如果你需要</para> <para>/ 更多详细信息，可以传入非 NULL 值。</para>

**参数:**

- `pDetails` (`out SteamRelayNetworkStatus_t`)

**返回值:** `ESteamNetworkingAvailability`

**用法示例:**
```csharp
SteamRelayNetworkStatus_t status;
var availability = SteamGameServerNetworkingUtils.GetRelayNetworkStatus(out status);
```

### GetLocalPingLocation (静态)

```csharp
float GetLocalPingLocation(out SteamNetworkPingLocation_t result)
```

<para>“Ping 定位”功能</para>
<para>我们利用全球各地 Valve 中继服务器的 ping 时间，</para>
<para>生成一个用于描述互联网主机位置的“标记”。</para>
<para>给定两个这样的标记，我们可以在不发送任何数据包的情况下，</para>
<para>估算出两台主机之间的网络延迟。该估算基于通过 Valve 网络</para>
<para>找到的最优路由。如果您正在使用 Valve 网络传输流量，</para>
<para>这恰恰就是您需要的 ping 值。即使未使用，该 ping 时间</para>
<para>通常也能提供合理的估算。</para>
<para>这在匹配系统中选择对等节点时极为有用！</para>
<para>这些标记也可以转换为字符串，以便进行传输。</para>
<para>我们提供了一个独立的库，供您在应用程序的匹配/协调服务器上</para>
<para>操作这些对象。（参见 steamdatagram_gamecoordinator.h）</para>
<para>/ 返回当前主机的定位信息。返回数据的近似年龄（以秒为单位），</para>
<para>/ 如果没有可用数据则返回 -1。</para>
<para>/</para>
<para>/ 初始化中继网络访问需要几秒钟时间。如果您在调用</para>
<para>/ InitRelayNetworkAccess 后立即调用此函数，数据可能尚未可用。</para>
<para>/</para>
<para>/ 即使我们正在重新计算 ping 时间，此函数始终返回当前</para>
<para>/ 可用的最新信息。</para>

**参数:**

- `result` (`out SteamNetworkPingLocation_t`)

**返回值:** `float`

**用法示例:**
```csharp
SteamNetworkPingLocation_t location;
float age = SteamGameServerNetworkingUtils.GetLocalPingLocation(out location);
```

### EstimatePingTimeBetweenTwoLocations (静态)

```csharp
int EstimatePingTimeBetweenTwoLocations(ref SteamNetworkPingLocation_t location1, ref SteamNetworkPingLocation_t location2)
```

<para>/ 估算任意两个位置之间的往返延迟，单位为毫秒。</para> <para>/ 这是一个基于通过中继网络路由的保守估算。</para> <para>/ 对于大多数基本中继连接，此ping时间将相当准确，</para> <para>/ 因为它基于可能实际使用的路由。</para> <para>/</para> <para>/ 如果使用了直接IP路由（例如通过NAT穿透），</para> <para>/ 则路由会不同，ping时间可能会更好，</para> <para>/ 但也可能实际上更差！标准的IP路由通常并非最优！</para> <para>/</para> <para>/ 但即使在这种情况下，使用此方法获得的估算值</para> <para>/ 也是ping时间的一个合理上限。</para> <para>/ （同时它还具有立即返回且不发送任何数据包的优势。）</para> <para>/</para> <para>/ 在少数情况下，我们可能无法估算路由。</para> <para>/ 此时将返回负值。k_nSteamNetworkingPing_Failed</para> <para>/ 表示原因是由于某些网络困难（如ping失败等）。</para> <para>/ 如果由于其他原因当前无法回答该问题，</para> <para>/ 则返回 k_nSteamNetworkingPing_Unknown。</para> <para>/</para> <para>/ 您是否需要从后端/匹配服务器执行此操作？</para> <para>/ 您正在寻找的是“游戏协调器”库。</para>

**参数:**

- `location1` (`ref SteamNetworkPingLocation_t`)
- `location2` (`ref SteamNetworkPingLocation_t`)

**返回值:** `int`

**用法示例:**
```csharp
int ping = SteamGameServerNetworkingUtils.EstimatePingTimeBetweenTwoLocations(ref location1, ref location2);
```

### EstimatePingTimeFromLocalHost (静态)

```csharp
int EstimatePingTimeFromLocalHost(ref SteamNetworkPingLocation_t remoteLocation)
```

<para>与 EstimatePingTime 相同，但假定其中一个位置为本地主机。</para>
<para>此方法速度略快，尤其当您需要在循环中计算多个此类值以找出最快的一个时。</para>
<para></para>
<para>在极少数情况下，此方法返回的估算值可能与组合使用 GetLocalPingLocation 和 EstimatePingTimeBetweenTwoLocations 的结果略有不同。这是因为该函数使用了关于所采用路由的略微更完整的信息集。</para>

**参数:**

- `remoteLocation` (`ref SteamNetworkPingLocation_t`)

**返回值:** `int`

**用法示例:**
```csharp
var ping = SteamGameServerNetworkingUtils.EstimatePingTimeFromLocalHost(ref remoteLocation);
```

### ConvertPingLocationToString (静态)

```csharp
void ConvertPingLocationToString(ref SteamNetworkPingLocation_t location, out string pszBuf, int cchBufSize)
```

<para>/ 将ping位置转换为适合通过网络传输的文本格式。</para>
<para>/ 该格式紧凑且可读性强。但未来可能发生变化，</para>
<para>/ 因此请勿自行解析。您的缓冲区至少需要</para>
<para>/ k_cchMaxSteamNetworkingPingLocationString 字节。</para>

**参数:**

- `location` (`ref SteamNetworkPingLocation_t`)
- `pszBuf` (`out string`)
- `cchBufSize` (`int`)

**用法示例:**
```csharp
SteamNetworkPingLocation_t location = default;
SteamGameServerNetworkingUtils.ConvertPingLocationToString(ref location, out string result, 1024);
```

### ParsePingLocationString (静态)

```csharp
bool ParsePingLocationString(string pszString, out SteamNetworkPingLocation_t result)
```

<para>/ 解析回 SteamNetworkPingLocation_t 字符串。如果无法理解该字符串则返回 false。</para>
<para>/</para>

**参数:**

- `pszString` (`string`)
- `result` (`out SteamNetworkPingLocation_t`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerNetworkingUtils.ParsePingLocationString("1.2.3.4:80", out SteamNetworkPingLocation_t location);
```

### CheckPingDataUpToDate (静态)

```csharp
bool CheckPingDataUpToDate(float flMaxAgeSeconds)
```

<para>/ 检查是否存在足够新的Ping数据，若数据过旧则启动刷新。</para>
<para>/</para>
<para>/ 请仅在*确实*需要强制立即刷新数据时调用此函数。</para>
<para>/ （例如，响应用户主动刷新该信息的操作）。请勿"以防万一"地调用，</para>
<para>/ 或在每次连接前调用，否则将无谓增加网络流量。</para>
<para>/ 库会根据需要自动刷新该信息。</para>
<para>/</para>
<para>/ 若已存在足够新的数据，返回True。</para>
<para>/</para>
<para>/ 若不存在足够新的数据，返回False。此时将启动Ping测量</para>
<para>/ （若尚未进行中的测量）。不能重新启动已在进行的测量。</para>
<para>/</para>
<para>/ 可通过GetRelayNetworkStatus或监听SteamRelayNetworkStatus_t</para>
<para>/ 了解Ping测量何时完成。</para>

**参数:**

- `flMaxAgeSeconds` (`float`)

**返回值:** `bool`

**用法示例:**
```csharp
bool isUpToDate = SteamGameServerNetworkingUtils.CheckPingDataUpToDate(5.0f);
```

### GetPingToDataCenter (静态)

```csharp
int GetPingToDataCenter(SteamNetworkingPOPID popID, out SteamNetworkingPOPID pViaRelayPoP)
```

<para> Valve数据中心列表及其延迟时间。</para> <para> 如果您正在使用我们的托管服务，或需要测量我们运行中继的云数据中心延迟，</para> <para> 这可能会对您有所帮助。</para> <para>/ 获取从此主机到指定数据中心的最佳可用中继路径的延迟时间。</para>

**参数:**

- `popID` (`SteamNetworkingPOPID`)
- `pViaRelayPoP` (`out SteamNetworkingPOPID`)

**返回值:** `int`

**用法示例:**
```csharp
int ping = SteamGameServerNetworkingUtils.GetPingToDataCenter(SteamNetworkingPOPID.iad, out SteamNetworkingPOPID viaRelay);
```

### GetDirectPingToPOP (静态)

```csharp
int GetDirectPingToPOP(SteamNetworkingPOPID popID)
```

<para>/ 获取与数据中心中继服务器的*直接* ping 时间。</para>

**参数:**

- `popID` (`SteamNetworkingPOPID`)

**返回值:** `int`

**用法示例:**
```csharp
int ping = SteamGameServerNetworkingUtils.GetDirectPingToPOP(SteamNetworkingPOPID.iad);
```

### GetPOPCount (静态)

```csharp
int GetPOPCount()
```

<para>/ 获取配置中的网络接入点数量</para>

**返回值:** `int`

**用法示例:**
```csharp
int popCount = SteamGameServerNetworkingUtils.GetPOPCount();
```

### GetPOPList (静态)

```csharp
int GetPOPList(out SteamNetworkingPOPID list, int nListSz)
```

<para>获取所有POP ID的列表。返回已填入您列表的条目数量。</para>

**参数:**

- `list` (`out SteamNetworkingPOPID`)
- `nListSz` (`int`)

**返回值:** `int`

**用法示例:**
```csharp
SteamNetworkingPOPID[] popList = new SteamNetworkingPOPID[10];
int count = SteamGameServerNetworkingUtils.GetPOPList(out popList[0], popList.Length);
```

### GetLocalTimestamp (静态)

```csharp
SteamNetworkingMicroseconds GetLocalTimestamp()
```

<para> 杂项</para>
<para> / 获取当前时间戳。该计时器具有以下属性：</para>
<para> /</para>
<para> / - 保证单调性。</para>
<para> / - 初始值至少为24*3600*30*1e6，即大约30天的微秒数。通过这种方式，时间戳值0将始终表示“至少30天前”。此外，永远不会返回负数。</para>
<para> / - 回绕/溢出不是实际需要考虑的问题。</para>
<para> /</para>
<para> / 如果在调试器下运行并停止进程，时钟可能不会按两次调用之间流逝的实际挂钟时间推进。如果进程未因正常操作而阻塞，即使不频繁调用该函数，时间戳值也会跟踪挂钟时间。</para>
<para> /</para>
<para> / 该值仅对本次进程运行有意义。不要将其与在其他计算机上或同一进程的其他运行中获取的值进行比较。</para>

**返回值:** `SteamNetworkingMicroseconds`

**用法示例:**
```csharp
var timestamp = SteamGameServerNetworkingUtils.GetLocalTimestamp();
```

### SetDebugOutputFunction (静态)

```csharp
void SetDebugOutputFunction(ESteamNetworkingSocketsDebugOutputType eDetailLevel, FSteamNetworkingSocketsDebugOutput pfnFunc)
```

<para>/ 设置一个函数以接收对调试有用的网络相关信息。</para> <para>/ 这在开发期间非常有用，但对于与技术熟练的最终用户进行故障排除也同样有用。</para> <para>/ 如果您有控制台或其他可供客户检查的日志，这些日志消息通常有助于排查网络问题。</para> <para>/ （特别是任何警告/错误消息。）</para> <para>/</para> <para>/ 详细程度指示在何种消息上调用您的回调。数值越低表示越重要，</para> <para>/ 您传递的值是希望接收回调的最低优先级（最高数值）。</para> <para>/</para> <para>/ 此处的值控制大多数消息的详细程度。您可以通过调整配置值</para> <para>/ k_ESteamNetworkingConfig_LogLevel_Xxxxx 来控制各个子系统</para> <para>/（可能仅针对某些连接）的详细程度。</para> <para>/</para> <para>/ 除调试外，您应仅使用 k_ESteamNetworkingSocketsDebugOutputType_Msg</para> <para>/ 或 k_ESteamNetworkingSocketsDebugOutputType_Warning。为获得最佳性能，请勿</para> <para>/ 请求高详细级别然后在回调中过滤掉消息。这会承担格式化消息的所有开销，</para> <para>/ 而这些消息随后会被丢弃。在此处设置高优先级值（低数值）允许库避免执行此工作。</para> <para>/</para> <para>/ 重要提示：此函数可能从服务线程调用，同时我们持有互斥锁等。</para> <para>/ 您的输出函数必须是线程安全的且速度快！不要在处理器内进行任何其他</para> <para>/ Steamworks 调用。</para>

**参数:**

- `eDetailLevel` (`ESteamNetworkingSocketsDebugOutputType`)
- `pfnFunc` (`FSteamNetworkingSocketsDebugOutput`)

**用法示例:**
```csharp
SteamGameServerNetworkingUtils.SetDebugOutputFunction(ESteamNetworkingSocketsDebugOutputType.Warning, MyDebugOutputFunction);
```

### IsFakeIPv4 (静态)

```csharp
bool IsFakeIPv4(uint nIPv4)
```

<para> 虚拟IP</para>
<para> 适用于与假设对等节点使用IPv4地址标识的代码交互</para>
<para>/ 若IPv4地址可能是用作"虚拟"地址则返回true。</para>
<para>/ 此函数速度较快；仅对IP执行逻辑判断，</para>
<para>/ 无需执行任何查询操作。</para>

**参数:**

- `nIPv4` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
bool isFake = SteamGameServerNetworkingUtils.IsFakeIPv4(0x7F000001);
```

### GetIPv4FakeIPType (静态)

```csharp
ESteamNetworkingFakeIPType GetIPv4FakeIPType(uint nIPv4)
```

**参数:**

- `nIPv4` (`uint`)

**返回值:** `ESteamNetworkingFakeIPType`

**用法示例:**
```csharp
uint ipv4 = 0xC0A80001;
ESteamNetworkingFakeIPType type = SteamGameServerNetworkingUtils.GetIPv4FakeIPType(ipv4);
```

### GetRealIdentityForFakeIP (静态)

```csharp
EResult GetRealIdentityForFakeIP(ref SteamNetworkingIPAddr fakeIP, out SteamNetworkingIdentity pOutRealIdentity)
```

<para>/ 获取与给定FakeIP关联的真实身份。</para> <para>/</para> <para>/ 失败时返回：</para> <para>/ - k_EResultInvalidParam：该IP不是FakeIP。</para> <para>/ - k_EResultNoMatch：无法识别该FakeIP，且不知道对应的身份。</para> <para>/</para> <para>/ 活跃连接使用的FakeIP，或分配给本地身份的FakeIP，</para> <para>/ 将始终有效。最近销毁的连接的FakeIP会在短时间内</para> <para>/ 继续返回结果，但不会永久有效。为节省空间，我们最终</para> <para>/ 会遗忘这些FakeIP。可以合理假设，在连接销毁后不久</para> <para>/ 您即可读回该连接的真实身份。但请不要无限期等待。</para>

**参数:**

- `fakeIP` (`ref SteamNetworkingIPAddr`)
- `pOutRealIdentity` (`out SteamNetworkingIdentity`)

**返回值:** `EResult`

**用法示例:**
```csharp
SteamNetworkingIPAddr fakeIP = default;
EResult result = SteamGameServerNetworkingUtils.GetRealIdentityForFakeIP(ref fakeIP, out SteamNetworkingIdentity realIdentity);
```

### SetConfigValue (静态)

```csharp
bool SetConfigValue(ESteamNetworkingConfigValue eValue, ESteamNetworkingConfigScope eScopeType, IntPtr scopeObj, ESteamNetworkingConfigDataType eDataType, IntPtr pArg)
```

<para> 设置和获取配置值，具体描述请参见 ESteamNetworkingConfigValue。</para>
<para> 常见情况的快捷方式。（以下作为内联函数实现）</para>
<para> 设置全局回调。如果您不想使用 Steam 的回调分发机制，并且</para>
<para> 希望在所有（或大多数）监听套接字和连接上使用相同的回调，那么</para>
<para> 只需首先安装这些回调，即可正常使用。</para>
<para> 参见 ISteamNetworkingSockets::RunCallbacks</para>
<para>/ 设置一个配置值。</para>
<para>/ - eValue：要设置哪个值</para>
<para>/ - eScope：将设置应用于何种类型的对象？</para>
<para>/ - scopeArg：您想要更改哪个对象？（对于全局范围则忽略）。例如连接句柄、监听套接字句柄、接口指针等。</para>
<para>/ - eDataType：pValue 缓冲区中的数据类型是什么？必须与变量的类型完全匹配！</para>
<para>/ - pArg：要设置的值。您可以传递 NULL 来移除该作用域下的非全局设置，</para>
<para>/ 使得该对象的值使用全局默认值。或者在全局作用域下，传递 NULL</para>
<para>/ 将重置任何自定义值并恢复为系统默认值。</para>
<para>/ 注意：设置指针（如回调函数）时，请勿直接传递函数指针。</para>
<para>/ 您的参数应指向一个函数指针的指针。</para>

**参数:**

- `eValue` (`ESteamNetworkingConfigValue`)
- `eScopeType` (`ESteamNetworkingConfigScope`)
- `scopeObj` (`IntPtr`)
- `eDataType` (`ESteamNetworkingConfigDataType`)
- `pArg` (`IntPtr`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = SteamGameServerNetworkingUtils.SetConfigValue(ESteamNetworkingConfigValue.k_ESteamNetworkingConfig_RecvBufferSize, ESteamNetworkingConfigScope.k_ESteamNetworkingConfig_Global, IntPtr.Zero, ESteamNetworkingConfigDataType.k_ESteamNetworkingConfig_Int32, IntPtr.Zero);
```

### GetConfigValue (静态)

```csharp
ESteamNetworkingGetConfigValueResult GetConfigValue(ESteamNetworkingConfigValue eValue, ESteamNetworkingConfigScope eScopeType, IntPtr scopeObj, out ESteamNetworkingConfigDataType pOutDataType, IntPtr pResult, ref ulong cbResult)
```

<para>/ 使用结构体传递值来设置配置值。</para>
<para>/ （这是一个便捷快捷方式；有关实现以及在监听套接字和连接创建期间设置配置选项时如何使用SteamNetworkingConfigValue_t的详细说明，请参见下文。）</para>
<para>/ 获取配置值。</para>
<para>/ - eValue：要获取的值</para>
<para>/ - eScopeType：在何种类型的对象上查询设置</para>
<para>/ - eScopeArg：要查询设置的对象</para>
<para>/ - pOutDataType：如果非NULL，则返回值的数据类型。</para>
<para>/ - pResult：结果放置的位置。传入NULL以查询所需的缓冲区大小。（将返回k_ESteamNetworkingGetConfigValue_BufferTooSmall。）</para>
<para>/ - cbResult：IN：缓冲区的大小。OUT：填充或所需的字节数。</para>

**参数:**

- `eValue` (`ESteamNetworkingConfigValue`)
- `eScopeType` (`ESteamNetworkingConfigScope`)
- `scopeObj` (`IntPtr`)
- `pOutDataType` (`out ESteamNetworkingConfigDataType`)
- `pResult` (`IntPtr`)
- `cbResult` (`ref ulong`)

**返回值:** `ESteamNetworkingGetConfigValueResult`

**用法示例:**
```csharp
ulong cbResult = 4;
SteamGameServerNetworkingUtils.GetConfigValue(ESteamNetworkingConfigValue.k_ESteamNetworkingConfig_ConnectionTimeout, ESteamNetworkingConfigScope.k_ESteamNetworkingConfig_ScopeGlobal, IntPtr.Zero, out var dataType, IntPtr.Zero, ref cbResult);
```

### GetConfigValueInfo (静态)

```csharp
string GetConfigValueInfo(ESteamNetworkingConfigValue eValue, out ESteamNetworkingConfigDataType pOutDataType, out ESteamNetworkingConfigScope pOutScope)
```

<para>获取配置值的信息。返回值名称，</para> <para>如果值不存在则返回NULL。其他输出参数可为NULL</para> <para>如果不需要它们的话。</para>

**参数:**

- `eValue` (`ESteamNetworkingConfigValue`)
- `pOutDataType` (`out ESteamNetworkingConfigDataType`)
- `pOutScope` (`out ESteamNetworkingConfigScope`)

**返回值:** `string`

**用法示例:**
```csharp
string name = SteamGameServerNetworkingUtils.GetConfigValueInfo(ESteamNetworkingConfigValue.TimeoutInitial, out ESteamNetworkingConfigDataType dataType, out ESteamNetworkingConfigScope scope);
```

### IterateGenericEditableConfigValues (静态)

```csharp
ESteamNetworkingConfigValue IterateGenericEditableConfigValues(ESteamNetworkingConfigValue eCurrent, bool bEnumerateDevVars)
```

<para>/ 遍历当前环境中所有可能通过通用UI显示或编辑的配置值列表。</para> <para>/ 要获取第一个可迭代值，请传递 k_ESteamNetworkingConfig_Invalid。</para> <para>/ 返回 k_ESteamNetworkingConfig_Invalid 表示列表结束。</para> <para>/</para> <para>/ bEnumerateDevVars 参数可用于包含“开发”变量。</para> <para>/ 这些变量建议仅在“调试”或“开发”模式下编辑，</para> <para>/ 在零售环境中通常不应显示，以防止恶意本地用户利用其作弊。</para>

**参数:**

- `eCurrent` (`ESteamNetworkingConfigValue`)
- `bEnumerateDevVars` (`bool`)

**返回值:** `ESteamNetworkingConfigValue`

**用法示例:**
```csharp
var firstValue = SteamGameServerNetworkingUtils.IterateGenericEditableConfigValues(ESteamNetworkingConfigValue.Invalid, false);
```

### SteamNetworkingIPAddr_ToString (静态)

```csharp
void SteamNetworkingIPAddr_ToString(ref SteamNetworkingIPAddr addr, out string buf, uint cbBuf, bool bWithPort)
```

<para> 字符串转换。通常应通过相应的</para> <para> 内联方法进行访问。</para>

**参数:**

- `addr` (`ref SteamNetworkingIPAddr`)
- `buf` (`out string`)
- `cbBuf` (`uint`)
- `bWithPort` (`bool`)

**用法示例:**
```csharp
SteamNetworkingIPAddr addr = default;
SteamGameServerNetworkingUtils.SteamNetworkingIPAddr_ToString(ref addr, out string buf, 256, true);
```

### SteamNetworkingIPAddr_ParseString (静态)

```csharp
bool SteamNetworkingIPAddr_ParseString(out SteamNetworkingIPAddr pAddr, string pszStr)
```

**参数:**

- `pAddr` (`out SteamNetworkingIPAddr`)
- `pszStr` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworkingUtils.SteamNetworkingIPAddr_ParseString(out var addr, "127.0.0.1:8080");
```

### SteamNetworkingIPAddr_GetFakeIPType (静态)

```csharp
ESteamNetworkingFakeIPType SteamNetworkingIPAddr_GetFakeIPType(ref SteamNetworkingIPAddr addr)
```

**参数:**

- `addr` (`ref SteamNetworkingIPAddr`)

**返回值:** `ESteamNetworkingFakeIPType`

**用法示例:**
```csharp
SteamNetworkingIPAddr addr = default;
ESteamNetworkingFakeIPType type = SteamGameServerNetworkingUtils.SteamNetworkingIPAddr_GetFakeIPType(ref addr);
```

### SteamNetworkingIdentity_ToString (静态)

```csharp
void SteamNetworkingIdentity_ToString(ref SteamNetworkingIdentity identity, out string buf, uint cbBuf)
```

**参数:**

- `identity` (`ref SteamNetworkingIdentity`)
- `buf` (`out string`)
- `cbBuf` (`uint`)

**用法示例:**
```csharp
SteamNetworkingIdentity identity = default;
SteamGameServerNetworkingUtils.SteamNetworkingIdentity_ToString(ref identity, out string buf, 1024);
```

### SteamNetworkingIdentity_ParseString (静态)

```csharp
bool SteamNetworkingIdentity_ParseString(out SteamNetworkingIdentity pIdentity, string pszStr)
```

**参数:**

- `pIdentity` (`out SteamNetworkingIdentity`)
- `pszStr` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworkingUtils.SteamNetworkingIdentity_ParseString(out var identity, "ip:127.0.0.1:27015");
```

