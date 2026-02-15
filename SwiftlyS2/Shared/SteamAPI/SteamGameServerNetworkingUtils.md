# 📦 SteamGameServerNetworkingUtils

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### AllocateMessage (静态)

```csharp
IntPtr AllocateMessage(int cbAllocateBuffer)
```

<para> 高效的消息发送</para> <para>/ 分配并初始化一个消息对象。通常调用此函数的原因</para> <para>/ 是为了将其传递给 ISteamNetworkingSockets::SendMessages。</para> <para>/ 返回的对象会将所有相关字段清零。</para> <para>/</para> <para>/ 也可以选择性地请求系统分配空间来</para> <para>/ 存储有效载荷本身。如果 cbAllocateBuffer 不为零，系统</para> <para>/ 将分配内存以容纳至少 cbAllocateBuffer 字节的有效载荷。</para> <para>/ m_pData 将指向已分配的缓冲区，m_cbSize 将被设置为</para> <para>/ 该大小，m_pfnFreeData 将被设置为正确的函数以释放</para> <para>/ 该缓冲区。</para> <para>/</para> <para>/ 如果 cbAllocateBuffer=0，则不分配缓冲区。m_pData 将为 NULL，</para> <para>/ m_cbSize 将为零，m_pfnFreeData 将为 NULL。您需要</para> <para>/ 设置这些字段中的每一个。</para>

**参数:**

- `cbAllocateBuffer` (`int`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr msgPtr = SteamGameServerNetworkingUtils.AllocateMessage(1024);
SteamGameServerNetworkingUtils.FreeMessage(msgPtr);
```

### InitRelayNetworkAccess (静态)

```csharp
void InitRelayNetworkAccess()
```

<para> 访问 Steam 数据报中继 (SDR) 网络</para> <para> 初始化和状态检查</para> <para>/ 如果您知道将要使用中继网络（例如，</para> <para>/ 因为您预计将建立 P2P 连接），请调用此方法来初始化</para> <para>/ 中继网络。如果您不调用此方法，初始化将会</para> <para>/ 延迟到您首次使用需要访问</para> <para>/ 中继网络的功能时，这会延迟首次访问。</para> <para>/</para> <para>/ 如果之前的尝试失败，您也可以调用此方法来强制重试。</para> <para>/ 执行任何需要访问中继网络的操作也会</para> <para>/ 触发重试，因此调用此函数并非严格必要，</para> <para>/ 但如果预计在程序启动时需要访问</para> <para>/ 中继网络，调用它可能会有用。</para> <para>/</para> <para>/ 使用 GetRelayNetworkStatus 或监听 SteamRelayNetworkStatus_t</para> <para>/ 回调来了解初始化何时完成。</para> <para>/ 通常初始化在几秒钟内完成。</para> <para>/</para> <para>/ 注意：托管在已知数据中心的专业服务器*不需要*</para> <para>/ 调用此方法，因为它们不进行路由决策。但是，如果</para> <para>/ 专业服务器将使用 P2P 功能，它将作为</para> <para>/ 一个“客户端”，则应调用此方法。</para>

**用法示例:**
```csharp
SteamGameServerNetworkingUtils.InitRelayNetworkAccess();
```

### GetRelayNetworkStatus (静态)

```csharp
ESteamNetworkingAvailability GetRelayNetworkStatus(out SteamRelayNetworkStatus_t pDetails)
```

<para>/ 获取中继网络的当前状态。</para> <para>/</para> <para>/ SteamRelayNetworkStatus_t 也是一个回调函数。当状态发生变化，或</para> <para>/ Ping 测量开始或停止时，它将在用户和游戏服务器接口上被触发。</para> <para>/</para> <para>/ 返回 SteamRelayNetworkStatus_t::m_eAvail。如果您需要</para> <para>/ 更多详细信息，可以传入一个非 NULL 的值。</para>

**参数:**

- `pDetails` (`out SteamRelayNetworkStatus_t`)

**返回值:** `ESteamNetworkingAvailability`

**用法示例:**
```csharp
SteamRelayNetworkStatus_t status;
var result = SteamGameServerNetworkingUtils.GetRelayNetworkStatus(out status);
```

### GetLocalPingLocation (静态)

```csharp
float GetLocalPingLocation(out SteamNetworkPingLocation_t result)
```

<para>“Ping 位置”功能</para> <para>我们使用全球部署的阀门中继（valve relays）的 Ping 时间来</para> <para>生成一个“标记”（marker），用于描述一个互联网主机的位置。</para> <para>给定两个这样的标记，我们可以在不发送任何数据包的情况下，估算</para> <para>两个主机之间的网络延迟。该估算基于通过 Valve 网络找到的最优</para> <para>路由。如果您正在使用 Valve 网络来承载流量，那么这就是您想要</para> <para>的 Ping 值。如果您没有使用，那么 Ping 时间可能仍然是一个</para> <para>合理的估算值。</para> <para>这对于为匹配（matchmaking）选择对等节点非常有用！</para> <para>这些标记也可以转换为字符串，以便进行传输。</para> <para>我们有一个独立的库，您可以在应用程序的匹配/协调</para> <para>服务器上使用它来操作这些对象。（请参阅 steamdatagram_gamecoordinator.h）</para> <para>/ 返回当前主机的位置信息。返回数据的近似</para> <para>/ 年龄（以秒为单位），如果数据不可用则返回 -1。</para> <para>/</para> <para>/ 初始化对中继网络的访问需要几秒钟。如果您在调用</para> <para>/ InitRelayNetworkAccess 后立即调用此函数，</para> <para>/ 数据可能尚未可用。</para> <para>/</para> <para>/ 此函数始终返回我们当前可用的最新信息，</para> <para>/ 即使我们正在重新计算 Ping 时间的过程中也是如此。</para>

**参数:**

- `result` (`out SteamNetworkPingLocation_t`)

**返回值:** `float`

**用法示例:**
```csharp
float age = SteamGameServerNetworkingUtils.GetLocalPingLocation(out var location);
```

### EstimatePingTimeBetweenTwoLocations (静态)

```csharp
int EstimatePingTimeBetweenTwoLocations(ref SteamNetworkPingLocation_t location1, ref SteamNetworkPingLocation_t location2)
```

<para>/ 估算两个任意位置之间的往返延迟，单位为毫秒。这是一个保守的估计，</para> <para>/ 基于通过中继网络的路由。对于大多数基本的中继连接，此ping时间</para> <para>/ 将相当准确，因为它将基于可能实际使用的路由。</para> <para>/</para> <para>/ 如果使用直接IP路由（可能通过NAT穿透），则路由</para> <para>/ 将不同，ping时间可能会更好。或者它实际上</para> <para>/ 可能会更差一些！标准的IP路由通常不是最优的！</para> <para>/</para> <para>/ 但即使在这种情况下，使用此方法获得的估计值也是ping时间</para> <para>/ 的合理上限。（此外，它还具有立即返回且不发送任何数据包的优势。）</para> <para>/</para> <para>/ 在少数情况下，我们可能无法估计路由。在这种情况下</para> <para>/ 返回一个负值。k_nSteamNetworkingPing_Failed表示</para> <para>/ 原因是由于某些网络困难。（ping失败等）如果由于其他原因</para> <para>/ 我们目前无法回答该问题，则返回k_nSteamNetworkingPing_Unknown。</para> <para>/</para> <para>/ 您是否需要从后端/匹配服务器执行此操作？</para> <para>/ 您正在寻找“游戏协调器”库。</para>

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

<para>/ 与 EstimatePingTime 类似，但假定其中一个位置是本地主机。</para> <para>/ 此方法速度更快，尤其是在循环中需要计算大量</para> <para>/ 这些值以找到最快的一个时。</para> <para>/</para> <para>/ 在极少数情况下，此方法返回的估算值可能与结合</para> <para>/ GetLocalPingLocation 和 EstimatePingTimeBetweenTwoLocations 的结果略有不同。这是因为</para> <para>/ 此函数使用了关于路由路径的更完整信息集。</para>

**参数:**

- `remoteLocation` (`ref SteamNetworkPingLocation_t`)

**返回值:** `int`

**用法示例:**
```csharp
int ping = SteamGameServerNetworkingUtils.EstimatePingTimeFromLocalLocation(ref remoteLocation);
```

### ConvertPingLocationToString (静态)

```csharp
void ConvertPingLocationToString(ref SteamNetworkPingLocation_t location, out string pszBuf, int cchBufSize)
```

<para>/ 将一个ping位置转换为适合通过网络发送的文本格式。</para> <para>/ 该格式是紧凑且人类可读的。但是，它可能会发生变化</para> <para>/，因此请不要自行解析。您的缓冲区大小必须至少为</para> <para>/ k_cchMaxSteamNetworkingPingLocationString 字节。</para>

**参数:**

- `location` (`ref SteamNetworkPingLocation_t`)
- `pszBuf` (`out string`)
- `cchBufSize` (`int`)

**用法示例:**
```csharp
string result;
SteamGameServerNetworkingUtils.ConvertPingLocationToString(ref location, out result, 256);
```

### ParsePingLocationString (静态)

```csharp
bool ParsePingLocationString(string pszString, out SteamNetworkPingLocation_t result)
```

<para>/ 解析 SteamNetworkPingLocation_t 字符串。如果无法理解该字符串，则返回 false。</para> <para>/ 该字符串。</para>

**参数:**

- `pszString` (`string`)
- `result` (`out SteamNetworkPingLocation_t`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerNetworkingUtils.ParsePingLocationString("us-east-1", out var location);
```

### CheckPingDataUpToDate (静态)

```csharp
bool CheckPingDataUpToDate(float flMaxAgeSeconds)
```

<para>/ 检查是否可用足够新近的ping数据，如果数据过旧，则开始刷新。</para> <para>/</para> <para>/ 请仅在您*确实*需要强制立即刷新数据时调用此函数。（例如，响应用户刷新此信息的特定输入。）不要“以防万一”调用它，</para> <para>/ 不要在每次连接前等场景下调用。这会导致发送不必要的额外流量。</para> <para>/ 库会根据需要自动刷新信息。</para> <para>/</para> <para>/ 如果已有足够新近的数据可用，则返回true。</para> <para>/</para> <para>/ 如果没有足够新近的数据可用，则返回false。在这种情况下，如果测量尚未进行，则会启动ping测量。</para> <para>/（您无法重新启动已进行的测量。）</para> <para>/</para> <para>/ 您可以使用GetRelayNetworkStatus或监听SteamRelayNetworkStatus_t</para> <para>/ 来了解ping测量何时完成。</para>

**参数:**

- `flMaxAgeSeconds` (`float`)

**返回值:** `bool`

**用法示例:**
```csharp
bool isReady = SteamGameServerNetworkingUtils.CheckPingDataUpToDate(5.0f);
if (!isReady)
{
    // 监听SteamRelayNetworkStatus_t以获取测量完成通知
}
```

### GetPingToDataCenter (静态)

```csharp
int GetPingToDataCenter(SteamNetworkingPOPID popID, out SteamNetworkingPOPID pViaRelayPoP)
```

<para> Valve 数据中心列表，以及到它们的 ping 延迟时间。如果您正在使用我们的托管服务，或者只是需要测量到我们运行中继服务的云数据中心的延迟，这些信息可能对您有用。</para> <para>/ 获取从本主机到指定数据中心的最佳可用中继路由的 ping 延迟时间。</para>

**参数:**

- `popID` (`SteamNetworkingPOPID`)
- `pViaRelayPoP` (`out SteamNetworkingPOPID`)

**返回值:** `int`

**用法示例:**
```csharp
int ping = SteamGameServerNetworkingUtils.GetPingToDataCenter(SteamNetworkingPOPID.k_ESteamNetworkingPOPID_UseRelay, out var viaRelayPoP);
Console.WriteLine($"Ping to data center: {ping}, via relay PoP: {viaRelayPoP}");
```

### GetDirectPingToPOP (静态)

```csharp
int GetDirectPingToPOP(SteamNetworkingPOPID popID)
```

<para>// 获取到数据中心中继节点的*直接*ping时间。</para>

**参数:**

- `popID` (`SteamNetworkingPOPID`)

**返回值:** `int`

**用法示例:**
```csharp
int ping = SteamGameServerNetworkingUtils.GetDirectPingToPOP(SteamNetworkingPOPID.Singapore);
```

### GetPOPCount (静态)

```csharp
int GetPOPCount()
```

<para>获取配置中的网络存在点数量</para>

**返回值:** `int`

**用法示例:**
```csharp
int popCount = SteamGameServerNetworkingUtils.GetPOPCount();
```

### GetPOPList (静态)

```csharp
int GetPOPList(out SteamNetworkingPOPID list, int nListSz)
```

<para>/ 获取所有POP ID的列表。返回填充到</para> <para>/ 您列表中的条目数量。</para>

**参数:**

- `list` (`out SteamNetworkingPOPID`)
- `nListSz` (`int`)

**返回值:** `int`

**用法示例:**
```csharp
SteamNetworkingPOPID[] popIds = new SteamNetworkingPOPID[10];
int count = SteamGameServerNetworkingUtils.GetPOPList(out popIds, popIds.Length);
```

### GetLocalTimestamp (静态)

```csharp
SteamNetworkingMicroseconds GetLocalTimestamp()
```

<para> 杂项</para> <para>/ 获取当前时间戳。此计时器具有以下特性：</para> <para>/</para> <para>/ - 保证单调性。</para> <para>/ - 初始值至少为 24*3600*30*1e6，即大约</para> <para>/ 30 天的微秒数。这样，时间戳值 0 将永远至少是“30 天前”。此外，绝不会返回负数。</para> <para>/ - 溢出问题在实际上无需考虑。</para> <para>/</para> <para>/ 如果在调试器下运行并停止进程，时钟</para> <para>/ 可能无法在两次调用之间推进完整的挂钟时间。如果进程未被阻止正常运行，则</para> <para>/ 即使不频繁调用该函数，时间戳值也会跟踪挂钟时间。</para> <para>/</para> <para>/ 该值仅对本次进程运行有意义。不要将其与在其他计算机上或同一进程的其他运行中获取的值进行比较。</para>

**返回值:** `SteamNetworkingMicroseconds`

**用法示例:**
```csharp
SteamGameServerNetworkingUtils.GetLocalTimestamp();
```

### SetDebugOutputFunction (静态)

```csharp
void SetDebugOutputFunction(ESteamNetworkingSocketsDebugOutputType eDetailLevel, FSteamNetworkingSocketsDebugOutput pfnFunc)
```

<para>/ 设置一个函数来接收与网络相关的信息，这些信息对于调试很有用。</para> <para>/ 这在开发过程中可能非常有用，但对于与技术相关的终端用户排查问题也可能有用。如果您有一个控制台或其他日志可供客户检查，这些日志消息通常有助于排查网络问题。</para> <para>/ (尤其是任何警告/错误消息。)</para> <para>/</para> <para>/ 详细级别指示要调用回调函数的消息类型。数值越小表示越重要，您传入的值是您希望接收回调的最低优先级（最高数值）。</para> <para>/</para> <para>/ 此处的值控制大多数消息的详细级别。您可以通过调整配置值 k_ESteamNetworkingConfig_LogLevel_Xxxxx 来控制各种子系统的详细级别（可能仅针对某些连接）。</para> <para>/</para> <para>/ 除非在调试时，否则您应仅使用 k_ESteamNetworkingSocketsDebugOutputType_Msg 或 k_ESteamNetworkingSocketsDebugOutputType_Warning。为了获得最佳性能，请不要请求高详细级别，然后在回调中过滤掉消息。这会导致所有格式化消息的开销，而这些消息随后被丢弃。在此处设置高优先级值（低数值）允许库避免执行此工作。</para> <para>/</para> <para>/ 重要提示：此函数可能从服务线程中调用，同时我们持有互斥锁等。</para> <para>/ 您的输出函数必须是线程安全的且快速的！请勿在处理程序中调用任何其他 Steamworks 函数。</para>

**参数:**

- `eDetailLevel` (`ESteamNetworkingSocketsDebugOutputType`)
- `pfnFunc` (`FSteamNetworkingSocketsDebugOutput`)

**用法示例:**
```csharp
SteamGameServerNetworkingUtils.SetDebugOutputFunction(ESteamNetworkingSocketsDebugOutputType.Msg, MyDebugOutputCallback);
```

### IsFakeIPv4 (静态)

```csharp
bool IsFakeIPv4(uint nIPv4)
```

<para> 伪造IP</para> <para> 用于与假设对等方使用IPv4地址进行标识的代码进行交互</para> <para>/ 如果IPv4地址可能是“伪造”地址，则返回true。</para> <para>/ 此函数执行速度快；它仅对IP执行一些逻辑测试，</para> <para>/ 无需执行任何查找操作。</para>

**参数:**

- `nIPv4` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
bool isFake = SteamGameServerNetworkingUtils.IsFakeIPv4(0x7F000001); // 127.0.0.1
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
uint fakeIPType = SteamGameServerNetworkingUtils.GetIPv4FakeIPType(0x01020304);
Console.WriteLine($"Fake IP type: {fakeIPType}");
```

### GetRealIdentityForFakeIP (静态)

```csharp
EResult GetRealIdentityForFakeIP(ref SteamNetworkingIPAddr fakeIP, out SteamNetworkingIdentity pOutRealIdentity)
```

<para>/ 获取与给定虚拟IP关联的真实身份。</para> <para>/</para> <para>/ 如果失败，将返回：</para> <para>/ - k_EResultInvalidParam：该IP不是虚拟IP。</para> <para>/ - k_EResultNoMatch：我们不识别该虚拟IP，也不知道其对应的身份。</para> <para>/</para> <para>/ 活动连接使用的虚拟IP，或分配给本地身份的虚拟IP，</para> <para>/ 总是能正常工作。最近已断开连接的虚拟IP，在一段时间内</para> <para>/ 仍会返回结果，但并非永久有效。在某个时刻，为了节省空间，我们将</para> <para>/ 忘记这些虚拟IP。可以合理地假设，在连接断开后不久，你仍能读取其</para> <para>/ 真实身份。但不要无限期地等待。</para>

**参数:**

- `fakeIP` (`ref SteamNetworkingIPAddr`)
- `pOutRealIdentity` (`out SteamNetworkingIdentity`)

**返回值:** `EResult`

**用法示例:**
```csharp
SteamNetworkingIPAddr fakeIP = new SteamNetworkingIPAddr();
SteamNetworkingIdentity identity;
EResult result = SteamGameServerNetworkingUtils.GetRealIdentityForFakeIP(ref fakeIP, out identity);
Console.WriteLine($"Result: {result}, Identity: {identity}");
```

### SetConfigValue (静态)

```csharp
bool SetConfigValue(ESteamNetworkingConfigValue eValue, ESteamNetworkingConfigScope eScopeType, IntPtr scopeObj, ESteamNetworkingConfigDataType eDataType, IntPtr pArg)
```

<para> 设置和获取配置值，有关各个配置项的详细说明，请参阅 ESteamNetworkingConfigValue。</para> <para> 常见用例的快捷方式。(以下以内联函数形式实现)</para> <para> 设置全局回调。如果您不想使用 Steam 的回调分发机制，并且希望</para> <para> 在所有（或大多数）监听套接字和连接上使用相同的回调，那么</para> <para> 只需在开始时首先安装这些回调，即可正常使用。</para> <para> 参见 ISteamNetworkingSockets::RunCallbacks</para> <para>/ 设置一个配置值。</para> <para>/ - eValue: 要设置的配置项</para> <para>/ - eScope: 将设置应用于何种类型的对象？</para> <para>/ - scopeArg: 要更改哪个对象？(全局作用域下忽略此参数)。例如连接句柄、监听套接字句柄、接口指针等。</para> <para>/ - eDataType: pValue 缓冲区中的数据类型。此类型必须与变量的类型完全匹配！</para> <para>/ - pArg: 要设置的值。对于非全局作用域，可以传入 NULL 以移除该作用域下的非全局设置，</para> <para>/ 从而使该对象的值使用全局默认值。对于全局作用域，传入 NULL</para> <para>/ 将重置任何自定义值，并将其恢复为系统默认值。</para> <para>/ 注意：在设置指针（例如回调函数）时，请不要直接传递函数指针。</para> <para>/ 您的参数应为一个指向函数指针的指针。</para>

**参数:**

- `eValue` (`ESteamNetworkingConfigValue`)
- `eScopeType` (`ESteamNetworkingConfigScope`)
- `scopeObj` (`IntPtr`)
- `eDataType` (`ESteamNetworkingConfigDataType`)
- `pArg` (`IntPtr`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworkingUtils.SetConfigValue(ESteamNetworkingConfigValue.MaxMessageSize, ESteamNetworkingConfigScope.Global, IntPtr.Zero, ESteamNetworkingConfigDataType.Int32, Marshal.SizeOf(typeof(int)).ToIntPtr());
```

### GetConfigValue (静态)

```csharp
ESteamNetworkingGetConfigValueResult GetConfigValue(ESteamNetworkingConfigValue eValue, ESteamNetworkingConfigScope eScopeType, IntPtr scopeObj, out ESteamNetworkingConfigDataType pOutDataType, IntPtr pResult, ref ulong cbResult)
```

<para>/ 设置一个配置值，使用一个结构体来传递该值。</para> <para>/ (这只是一个便捷的快捷方式；请参见下方了解其实现，</para> <para>/ 以及在监听套接字和连接创建期间设置配置选项时，</para> <para>/ SteamNetworkingConfigValue_t 是如何被使用的相关见解。)</para> <para>/ 获取一个配置值。</para> <para>/ - eValue: 要获取的值</para> <para>/ - eScopeType: 查询设置的对象类型</para> <para>/ - eScopeArg: 要查询设置的对象</para> <para>/ - pOutDataType: 如果非 NULL，则返回该值的数据类型。</para> <para>/ - pResult: 用于存放结果的位置。传入 NULL 以查询所需的缓冲区大小。（将返回 k_ESteamNetworkingGetConfigValue_BufferTooSmall。）</para> <para>/ - cbResult: IN: 您缓冲区的大小。OUT: 已填充的字节数或所需字节数。</para>

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
ulong size = 0;  
ESteamNetworkingGetConfigValueResult result = SteamGameServerNetworkingUtils.GetConfigValue(ESteamNetworkingConfigValue.Value, ESteamNetworkingConfigScope.Global, IntPtr.Zero, out _, IntPtr.Zero, ref size);
```

### GetConfigValueInfo (静态)

```csharp
string GetConfigValueInfo(ESteamNetworkingConfigValue eValue, out ESteamNetworkingConfigDataType pOutDataType, out ESteamNetworkingConfigScope pOutScope)
```

<para>/ 获取配置值的信息。返回该值的名称，</para> <para>/ 如果该值不存在则返回 NULL。其他输出参数可以为 NULL</para> <para>/ 如果您不需要它们。</para>

**参数:**

- `eValue` (`ESteamNetworkingConfigValue`)
- `pOutDataType` (`out ESteamNetworkingConfigDataType`)
- `pOutScope` (`out ESteamNetworkingConfigScope`)

**返回值:** `string`

**用法示例:**
```csharp
string name = SteamGameServerNetworkingUtils.GetConfigValueInfo(ESteamNetworkingConfigValue.Value, out _, out _);
Console.WriteLine(name);
```

### IterateGenericEditableConfigValues (静态)

```csharp
ESteamNetworkingConfigValue IterateGenericEditableConfigValues(ESteamNetworkingConfigValue eCurrent, bool bEnumerateDevVars)
```

<para>/ 遍历当前环境中所有可能通过通用UI显示或编辑的配置值列表。要获取第一个可迭代值，</para> <para>/ 请传入 k_ESteamNetworkingConfig_Invalid。当返回 k_ESteamNetworkingConfig_Invalid 时，</para> <para>/ 表示列表已结束。</para> <para>/</para> <para>/ bEnumerateDevVars 参数可用于包含 "dev" 变量。这些变量建议仅在 "debug" 或 "dev" 模式下</para> <para>/ 可编辑，通常不应在零售环境中显示，因为恶意本地用户可能利用此功能作弊。</para>

**参数:**

- `eCurrent` (`ESteamNetworkingConfigValue`)
- `bEnumerateDevVars` (`bool`)

**返回值:** `ESteamNetworkingConfigValue`

**用法示例:**
```csharp
ESteamNetworkingConfigValue val = ESteamNetworkingConfigValue.Value;
while (val != ESteamNetworkingConfigValue.Invalid)
{
    val = SteamGameServerNetworkingUtils.IterateGenericEditableConfigValues(val, false);
}
Console.WriteLine("遍历完成");
```

### SteamNetworkingIPAddr_ToString (静态)

```csharp
void SteamNetworkingIPAddr_ToString(ref SteamNetworkingIPAddr addr, out string buf, uint cbBuf, bool bWithPort)
```

<para>字符串转换。通常您会通过相应的</para> <para>内联方法来访问这些功能。</para>

**参数:**

- `addr` (`ref SteamNetworkingIPAddr`)
- `buf` (`out string`)
- `cbBuf` (`uint`)
- `bWithPort` (`bool`)

**用法示例:**
```csharp
SteamGameServerNetworkingUtils.SteamNetworkingIPAddr_ToString(ref addr, out string buf, (uint)256, true);
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
SteamGameServerNetworkingUtils.SteamNetworkingIPAddr_ParseString(out var addr, "127.0.0.1:27015");
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
var fakeIPType = SteamGameServerNetworkingUtils.SteamNetworkingIPAddr_GetFakeIPType(ref someAddr);
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
SteamNetworkingIdentity_ToString(ref identity, out string buf, 0);
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
SteamGameServerNetworkingUtils.SteamNetworkingIdentity_ParseString(out var identity, "123456789");
```

