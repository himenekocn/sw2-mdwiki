# 📦 SteamGameServerNetworkingUtils

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### AllocateMessage (静态)

```csharp
IntPtr AllocateMessage(int cbAllocateBuffer)
```

<para>高效的消息发送</para> <para>/ 分配并初始化一个消息对象。通常调用此方法的目的是将其传递给 ISteamNetworkingSockets::SendMessages。</para> <para>/ 返回的对象中所有相关字段将被初始化为零。</para> <para>/</para> <para>/ 可选地，您还可以请求系统分配用于存储有效负载（payload）的空间。如果 cbAllocateBuffer 为非零值，系统将分配至少 cbAllocateBuffer 字节的内存以容纳有效负载。</para> <para>/ 此时，m_pData 将指向分配的缓冲区，m_cbSize 将被设置为该大小，而 m_pfnFreeData 将被设置为释放该缓冲区的正确函数。</para> <para>/</para> <para>/ 如果 cbAllocateBuffer 为 0，则不分配任何缓冲区。m_pData 将为 NULL，m_cbSize 为零，m_pfnFreeData 也为 NULL。您需要手动设置这些成员。</para>

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

访问 Steam 数据报中继（SDR）网络。初始化与状态检查。如果您确定将使用中继网络（例如，预期会建立 P2P 连接），请调用此函数以初始化中继网络。若不调用此函数，初始化将延迟至首次使用需要访问中继网络的功能时进行，从而导致该首次访问出现延迟。您也可调用此函数在先前尝试失败后强制重试。任何需要访问中继网络的操作也会触发重试，因此严格来说调用此函数并非必需；但若预期会使用中继网络，在游戏启动时调用此函数仍具实用价值。请使用 GetRelayNetworkStatus 或监听 SteamRelayNetworkStatus_t 回调以确认初始化是否完成。通常初始化会在几秒内完成。注意：托管于已知数据中心的专用服务器*无需*调用此函数，因为它们不进行路由决策。然而，如果该专用服务器将使用 P2P 功能，它将作为“客户端”运行，此时应调用此函数。

**用法示例:**
```csharp
SteamGameServerNetworkingUtils.InitRelayNetworkAccess();
```

### GetRelayNetworkStatus (静态)

```csharp
ESteamNetworkingAvailability GetRelayNetworkStatus(out SteamRelayNetworkStatus_t pDetails)
```

<para>/ 获取中继网络的当前状态。</para> <para>/</para> <para>/ SteamRelayNetworkStatus_t 也是一个回调。当状态发生变化，或开始/停止 Ping 测量时，该回调将在用户接口和游戏服务器接口上被触发。</para> <para>/</para> <para>/ 返回 SteamRelayNetworkStatus_t::m_eAvail。如需更多详细信息，可传入非 NULL 值。</para>

**参数:**

- `pDetails` (`out SteamRelayNetworkStatus_t`)

**返回值:** `ESteamNetworkingAvailability`

**用法示例:**
```csharp
SteamRelayNetworkStatus_t details;
ESteamNetworkingAvailability availability = SteamGameServerNetworkingUtils.GetRelayNetworkStatus(out details);
```

### GetLocalPingLocation (静态)

```csharp
float GetLocalPingLocation(out SteamNetworkPingLocation_t result)
```

<para>“Ping 位置”相关功能</para> <para>我们利用遍布全球的 Valve 中继节点的 Ping 时间，</para> <para>生成一个描述互联网主机位置的“标记（marker）”。</para> <para>给定两个此类标记，我们可以在不发送任何数据包的情况下，</para> <para>估算两台主机之间的网络延迟。该估算基于通过 Valve 网络发现的最优路径。</para> <para>如果您正使用 Valve 网络承载流量，则此值即为您所需的 Ping 值。</para> <para>如果您未使用 Valve 网络，则该 Ping 时间通常仍是一个合理的估算值。</para> <para>这对于为匹配系统选择对等节点极为有用！</para> <para>这些标记也可转换为字符串，以便进行传输。</para> <para>我们提供了一个独立的库，供您在应用的匹配/协调服务器上用于操作这些对象。（参见 steamdatagram_gamecoordinator.h）</para> <para>/ 返回当前主机的位置信息。返回数据的近似年龄（单位：秒），若无可用的数据则返回 -1。</para> <para>/</para> <para>/ 访问中继网络需要数秒进行初始化。若您在调用 InitRelayNetworkAccess 后不久立即调用此函数，</para> <para>/ 可能尚无法获取数据。</para> <para>/</para> <para>/ 无论我们是否正在重新计算 Ping 时间，此函数始终返回当前可用的最新信息。</para>

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

/ 估算两个任意位置之间的往返延迟（单位：毫秒）。此估算是保守的，基于通过中继网络的路线。对于大多数基本的中继连接，该 Ping 值将相当准确，因为它基于实际可能使用的路线。
/
/ 如果使用直接 IP 路由（例如通过 NAT 穿透），则路线会有所不同，Ping 值可能会更好。但也可能实际上略差！标准 IP 路由经常不是最优的！
/
/ 即使在这种情况下，使用此方法获得的估计值仍然是 Ping 时间的合理上限。（此外，它的优势在于能够立即返回且无需发送任何数据包。）
/
/ 在某些情况下，我们可能无法估算路线。此时将返回负值。若原因是某些网络困难（如无法 Ping 通等），则返回 k_nSteamNetworkingPing_Failed；若因其他原因目前无法回答该问题，则返回 k_nSteamNetworkingPing_Unknown。
/
/ 您是否需要在后端/匹配服务器上进行此类操作？您需要使用的是“游戏协调器”库。

**参数:**

- `location1` (`ref SteamNetworkPingLocation_t`)
- `location2` (`ref SteamNetworkPingLocation_t`)

**返回值:** `int`

**用法示例:**
```csharp
int pingMs = SteamGameServerNetworkingUtils.EstimatePingTimeBetweenTwoLocations(ref loc1, ref loc2);
```

### EstimatePingTimeFromLocalHost (静态)

```csharp
int EstimatePingTimeFromLocalHost(ref SteamNetworkPingLocation_t remoteLocation)
```

/// 与 EstimatePingTime 相同，但假设其中一个位置为本机。
/// 此方法速度更快，特别是在需要在循环中计算大量此类值以找出最快位置时。
///
/// 在极少数情况下，此方法返回的估算值可能与结合使用 GetLocalPingLocation 和 EstimatePingTimeBetweenTwoLocations 得到的结果略有不同。这是因为本函数使用了关于路由选择更完整的信息集。

**参数:**

- `remoteLocation` (`ref SteamNetworkPingLocation_t`)

**返回值:** `int`

**用法示例:**
```csharp
int pingMs = SteamGameServerNetworkingUtils.EstimatePingTimeFromLocalHost(ref remoteLocation);
```

### ConvertPingLocationToString (静态)

```csharp
void ConvertPingLocationToString(ref SteamNetworkPingLocation_t location, out string pszBuf, int cchBufSize)
```

<para>/ 将 ping 位置转换为适合通过网络传输的文本格式。</para> <para>/ 该格式紧凑且易于人类阅读，但可能发生变化，</para> <para>/ 因此请勿自行解析。您的缓冲区大小必须至少为</para> <para>/ k_cchMaxSteamNetworkingPingLocationString 字节。</para>

**参数:**

- `location` (`ref SteamNetworkPingLocation_t`)
- `pszBuf` (`out string`)
- `cchBufSize` (`int`)

**用法示例:**
```csharp
SteamNetworkPingLocation_t location = default;
SteamGameServerNetworkingUtils.ConvertPingLocationToString(ref location, out string pszBuf, 1024);
```

### ParsePingLocationString (静态)

```csharp
bool ParsePingLocationString(string pszString, out SteamNetworkPingLocation_t result)
```

// 解析返回的 SteamNetworkPingLocation_t 字符串。如果无法理解该字符串，则返回 false。

**参数:**

- `pszString` (`string`)
- `result` (`out SteamNetworkPingLocation_t`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerNetworkingUtils.ParsePingLocationString("12345abc", out var pingLocation);
```

### CheckPingDataUpToDate (静态)

```csharp
bool CheckPingDataUpToDate(float flMaxAgeSeconds)
```

<para>/ 检查是否已有足够新的 Ping 数据可用；若数据已过时，则启动刷新。</para> <para>/</para> <para>/ 仅在您确实需要强制立即刷新数据时才调用此函数。（例如，响应特定的用户输入以刷新该信息。）切勿出于“以防万一”的考虑，或在每次连接前无条件调用。这会导致无谓地增加网络流量。本库将在需要时自动刷新相关数据。</para> <para>/</para> <para>/ 若已存在足够新的数据，则返回 true。</para> <para>/</para> <para>/ 若不存在足够新的数据，则返回 false。此时，若尚未开始 Ping 测量，将启动测量过程。（无法重启正在进行的测量。）</para> <para>/</para> <para>/ 可使用 GetRelayNetworkStatus 或监听 SteamRelayNetworkStatus_t 消息，以获知 Ping 测量何时完成。</para>

**参数:**

- `flMaxAgeSeconds` (`float`)

**返回值:** `bool`

**用法示例:**
```csharp
if (!SteamGameServerNetworkingUtils.CheckPingDataUpToDate(300f)) Console.WriteLine("Ping 数据已过期，正在刷新...");
```

### GetPingToDataCenter (静态)

```csharp
int GetPingToDataCenter(SteamNetworkingPOPID popID, out SteamNetworkingPOPID pViaRelayPoP)
```

<para>Valve 数据中心列表及其对应的延迟时间。如果您正在使用我们的托管服务，或仅需测量至我们运行中继的云端数据中心的延迟，此信息可能对您有所帮助。</para><para>/ 获取从当前主机到指定数据中心的最佳可用中继路径的延迟时间。</para>

**参数:**

- `popID` (`SteamNetworkingPOPID`)
- `pViaRelayPoP` (`out SteamNetworkingPOPID`)

**返回值:** `int`

**用法示例:**
```csharp
SteamNetworkingPOPID viaRelayPoP;
int ping = SteamGameServerNetworkingUtils.GetPingToDataCenter(popID, out viaRelayPoP);
```

### GetDirectPingToPOP (静态)

```csharp
int GetDirectPingToPOP(SteamNetworkingPOPID popID)
```

<para>/ 获取到数据中心中继的直接延迟时间。</para>

**参数:**

- `popID` (`SteamNetworkingPOPID`)

**返回值:** `int`

**用法示例:**
```csharp
SteamNetworkingPOPID popID = default;
int ping = SteamGameServerNetworkingUtils.GetDirectPingToPOP(popID);
```

### GetPOPCount (静态)

```csharp
int GetPOPCount()
```

<para>/ 获取配置中的网络存在点数量</para>

**返回值:** `int`

**用法示例:**
```csharp
int popCount = SteamGameServerNetworkingUtils.GetPOPCount();
```

### GetPOPList (静态)

```csharp
int GetPOPList(out SteamNetworkingPOPID list, int nListSz)
```

<para>/ 获取所有 POP ID 列表。返回已填充到</para> <para>/ 您列表中的条目数量。</para>

**参数:**

- `list` (`out SteamNetworkingPOPID`)
- `nListSz` (`int`)

**返回值:** `int`

**用法示例:**
```csharp
SteamNetworkingPOPID popId;
int count = SteamGameServerNetworkingUtils.GetPOPList(out popId, 1);
```

### GetLocalTimestamp (静态)

```csharp
SteamNetworkingMicroseconds GetLocalTimestamp()
```

<para>杂项</para> <para>/ 获取当前时间戳。该计时器具有以下属性：</para> <para>/</para> <para>/ - 保证单调性。</para> <para>/ - 初始值至少为 24*3600*30*1e6，即大约</para> <para>/ 30 天的微秒数。因此，时间戳值 0 始终代表“至少 30 天前”。此外，</para> <para>/ 永远不会返回负数。</para> <para>/ - 回绕/溢出在实际应用中无需担心。</para> <para>/</para> <para>/ 如果在调试器中运行并暂停进程，时钟可能不会推进两次调用之间经过的完整真实时间。如果进程未因正常操作受阻，</para> <para>/ 即使不频繁调用该函数，时间戳值仍会跟踪真实时间。</para> <para>/</para> <para>/ 该值仅对当前进程运行有意义。请勿将其与在其他计算机上或其他次同一进程运行中获得的值进行比较。</para>

**返回值:** `SteamNetworkingMicroseconds`

**用法示例:**
```csharp
var timestamp = SteamGameServerNetworkingUtils.GetLocalTimestamp();
Console.WriteLine(timestamp);
```

### SetDebugOutputFunction (静态)

```csharp
void SetDebugOutputFunction(ESteamNetworkingSocketsDebugOutputType eDetailLevel, FSteamNetworkingSocketsDebugOutput pfnFunc)
```

/ 设置一个函数以接收对调试有用的网络相关信息。
/ 这在开发过程中非常有用，对于协助技术熟练的终端用户排查问题也很有帮助。如果您有控制台或其他日志可供客户查看，这些日志消息通常有助于诊断网络问题。
/ （特别是任何警告或错误消息。）
/
/ 详细级别指示在何种消息级别调用您的回调函数。较低的数值代表更高级别（更重要），您传入的值是您希望接收回调的最高优先级（即最大数值）阈值。
/
/ 此处的值控制大多数消息的详细级别。您可以通过调整配置值 k_ESteamNetworkingConfig_LogLevel_Xxxxx，来控制各个子系统的详细级别（例如仅针对特定连接）。
/
/ 除非进行调试，否则应仅使用 k_ESteamNetworkingSocketsDebugOutputType_Msg 或 k_ESteamNetworkingSocketsDebugOutputType_Warning。为了获得最佳性能，请勿请求高详细级别然后在您的回调中过滤掉消息。这样做会导致产生格式化消息的所有开销，随后这些消息却被丢弃。在此处设置较高的优先级值（即较低的数值）可让库避免执行此类工作。
/
/ 重要提示：此函数可能由服务线程调用，且此时我们持有互斥锁等。您的输出函数必须是线程安全且高效的！切勿在处理器内调用任何其他 Steamworks 函数。

**参数:**

- `eDetailLevel` (`ESteamNetworkingSocketsDebugOutputType`)
- `pfnFunc` (`FSteamNetworkingSocketsDebugOutput`)

**用法示例:**
```csharp
SteamGameServerNetworkingUtils.SetDebugOutputFunction(ESteamNetworkingSocketsDebugOutputType.Warning, (type, msg) => Console.WriteLine(msg));
```

### IsFakeIPv4 (静态)

```csharp
bool IsFakeIPv4(uint nIPv4)
```

<para>虚假 IP</para> <para>适用于与假设对等体通过 IPv4 地址进行识别的代码进行接口交互。</para> <para>/ 如果某个 IPv4 地址可能是“虚假”地址，则返回 true。</para> <para>/ 此函数执行速度极快；它仅对 IP 地址执行逻辑测试，无需进行任何查找操作。</para>

**参数:**

- `nIPv4` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint ip = 0x7F000001;
bool isFake = SteamGameServerNetworkingUtils.IsFakeIPv4(ip);
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
uint ip = 0x7F000001;
ESteamNetworkingFakeIPType type = SteamGameServerNetworkingUtils.GetIPv4FakeIPType(ip);
```

### GetRealIdentityForFakeIP (静态)

```csharp
EResult GetRealIdentityForFakeIP(ref SteamNetworkingIPAddr fakeIP, out SteamNetworkingIdentity pOutRealIdentity)
```

<para>/ 获取与给定 FakeIP 关联的真实身份。</para> <para>/</para> <para>/ 若失败，返回：</para> <para>/ - k_EResultInvalidParam：该 IP 不是 FakeIP。</para> <para>/ - k_EResultNoMatch：我们未识别该 FakeIP，且不知其对应的身份。</para> <para>/</para> <para>/ 由活跃连接使用的 FakeIP，或分配给本地身份的 FakeIP，将始终有效。最近已销毁连接的 FakeIP 会在短时间内继续返回结果，但不会永久有效。某时刻，我们将遗忘部分 FakeIP 以节省空间。可以合理假设，在连接刚被销毁后不久，即可读取其真实身份。但请勿无限期等待。</para>

**参数:**

- `fakeIP` (`ref SteamNetworkingIPAddr`)
- `pOutRealIdentity` (`out SteamNetworkingIdentity`)

**返回值:** `EResult`

**用法示例:**
```csharp
SteamNetworkingIdentity realIdentity;
EResult result = SteamGameServerNetworkingUtils.GetRealIdentityForFakeIP(ref fakeIP, out realIdentity);
```

### SetConfigValue (静态)

```csharp
bool SetConfigValue(ESteamNetworkingConfigValue eValue, ESteamNetworkingConfigScope eScopeType, IntPtr scopeObj, ESteamNetworkingConfigDataType eDataType, IntPtr pArg)
```

<para>设置和获取配置值，请参阅 ESteamNetworkingConfigValue 以了解各值的详细说明。</para><para>针对常见情况的快捷方式。（以下作为内联函数实现）</para><para>设置全局回调。如果您不希望使用 Steam 的回调分发机制，且希望在所有（或大多数）监听套接字和连接上使用相同的回调，则只需首先安装这些回调即可开始使用。</para><para>请参见 ISteamNetworkingSockets::RunCallbacks</para><para>/ 设置一个配置值。</para><para>/ - eValue：正在设置的值类型</para><para>/ - eScope：该设置应用于何种类型的对象？</para><para>/ - scopeArg：您希望更改哪个对象？（对于全局作用域可忽略）。例如：连接句柄、监听套接字句柄、接口指针等。</para><para>/ - eDataType：pValue 缓冲区内数据的类型。必须与变量的类型完全匹配！</para><para>/ - pArg：要设置的值。您可以传递 NULL 以移除该作用域下的非全局设置，从而使该对象的值使用全局默认值。或者在全局作用域下，传递 NULL 将重置任何自定义值并恢复为系统默认值。</para><para>/ 注意：在设置指针（例如回调函数）时，请勿直接传递函数指针。</para><para>/ 您的参数应为一个指向函数指针的指针。</para>

**参数:**

- `eValue` (`ESteamNetworkingConfigValue`)
- `eScopeType` (`ESteamNetworkingConfigScope`)
- `scopeObj` (`IntPtr`)
- `eDataType` (`ESteamNetworkingConfigDataType`)
- `pArg` (`IntPtr`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerNetworkingUtils.SetConfigValue(ESteamNetworkingConfigValue.k_ESteamNetworkingConfig_TimeoutInitial.Value, ESteamNetworkingConfigScope.Global.Value, IntPtr.Zero, ESteamNetworkingConfigDataType.Int32.Value, IntPtr.Zero);
```

### GetConfigValue (静态)

```csharp
ESteamNetworkingGetConfigValueResult GetConfigValue(ESteamNetworkingConfigValue eValue, ESteamNetworkingConfigScope eScopeType, IntPtr scopeObj, out ESteamNetworkingConfigDataType pOutDataType, IntPtr pResult, ref ulong cbResult)
```

<para>/ 使用结构体设置配置值。</para> <para>/ （这仅是一个便捷的快捷方式；有关 SteamNetworkingConfigValue_t 在创建监听套接字和连接时用于设置配置选项的实现细节及工作原理，请参见下文。）</para> <para>/ 获取配置值。</para> <para>/ - eValue：要获取的配置项名称</para> <para>/ - eScopeType：查询设置所属的对象类型</para> <para>/ - eScopeArg：要查询设置的特定对象</para> <para>/ - pOutDataType：如果非 NULL，则返回该值的原始数据类型。</para> <para>/ - pResult：存放结果的缓冲区。若传入 NULL，则仅查询所需缓冲区大小（将返回 k_ESteamNetworkingGetConfigValue_BufferTooSmall 错误）。</para> <para>/ - cbResult：输入为缓冲区大小；输出为已填充的字节数或所需字节数。</para>

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
ulong cb = 0; ESteamNetworkingConfigDataType dataType; var result = SteamGameServerNetworkingUtils.GetConfigValue(ESteamNetworkingConfigValue.Value, ESteamNetworkingConfigScope.Value, IntPtr.Zero, out dataType, IntPtr.Zero, ref cb);
```

### GetConfigValueInfo (静态)

```csharp
string GetConfigValueInfo(ESteamNetworkingConfigValue eValue, out ESteamNetworkingConfigDataType pOutDataType, out ESteamNetworkingConfigScope pOutScope)
```

<para>/ 获取配置项的信息。返回该值的名称，</para> <para>/ 若该值不存在则返回 NULL。其他输出参数如无需使用，可为 NULL。</para>

**参数:**

- `eValue` (`ESteamNetworkingConfigValue`)
- `pOutDataType` (`out ESteamNetworkingConfigDataType`)
- `pOutScope` (`out ESteamNetworkingConfigScope`)

**返回值:** `string`

**用法示例:**
```csharp
ESteamNetworkingConfigDataType dataType; ESteamNetworkingConfigScope scope; string name = SteamGameServerNetworkingUtils.GetConfigValueInfo(ESteamNetworkingConfigValue.Value, out dataType, out scope);
```

### IterateGenericEditableConfigValues (静态)

```csharp
ESteamNetworkingConfigValue IterateGenericEditableConfigValues(ESteamNetworkingConfigValue eCurrent, bool bEnumerateDevVars)
```

<para>/ 遍历当前环境中所有可能通过通用 UI 显示或编辑的配置值列表。若要获取第一个可迭代值，请传入 k_ESteamNetworkingConfig_Invalid。返回 k_ESteamNetworkingConfig_Invalid 表示列表结束。</para> <para>/</para> <para>/ bEnumerateDevVars 参数可用于包含"dev"（开发）变量。这些变量建议在仅处于"debug"或"dev"模式时才可编辑，通常不应在零售环境中展示，以防恶意本地用户利用这些变量进行作弊。</para>

**参数:**

- `eCurrent` (`ESteamNetworkingConfigValue`)
- `bEnumerateDevVars` (`bool`)

**返回值:** `ESteamNetworkingConfigValue`

**用法示例:**
```csharp
ESteamNetworkingConfigValue cfg = ESteamNetworkingConfigValue.k_ESteamNetworkingConfig_Invalid;
while ((cfg = SteamGameServerNetworkingUtils.IterateGenericEditableConfigValues(cfg, false)) != ESteamNetworkingConfigValue.k_ESteamNetworkingConfig_Invalid) { }
```

### SteamNetworkingIPAddr_ToString (静态)

```csharp
void SteamNetworkingIPAddr_ToString(ref SteamNetworkingIPAddr addr, out string buf, uint cbBuf, bool bWithPort)
```

<para>字符串转换。通常可通过相应的</para> <para>内联方法访问这些功能。</para>

**参数:**

- `addr` (`ref SteamNetworkingIPAddr`)
- `buf` (`out string`)
- `cbBuf` (`uint`)
- `bWithPort` (`bool`)

**用法示例:**
```csharp
string ip;
SteamGameServerNetworkingUtils.SteamNetworkingIPAddr_ToString(ref addr, out ip, 64, true);
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
SteamNetworkingIPAddr addr;
bool ok = SteamGameServerNetworkingUtils.SteamNetworkingIPAddr_ParseString(out addr, "127.0.0.1:27015");
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
ESteamNetworkingFakeIPType fakeIpType = SteamGameServerNetworkingUtils.SteamNetworkingIPAddr_GetFakeIPType(ref addr);
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
SteamGameServerNetworkingUtils.SteamNetworkingIdentity_ToString(ref identity, out string buf, 256);
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
SteamNetworkingIdentity identity;
bool ok = SteamGameServerNetworkingUtils.SteamNetworkingIdentity_ParseString(out identity, "steamid:123456789");
```

