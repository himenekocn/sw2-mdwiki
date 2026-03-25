# 📦 SteamGameServerUtils

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### GetSecondsSinceAppActive (静态)

```csharp
uint GetSecondsSinceAppActive()
```

<para>返回自用户登录以来经过的秒数</para>

**返回值:** `uint`

**用法示例:**
```csharp
uint secondsSinceAppActive = SteamGameServerUtils.GetSecondsSinceAppActive();
```

### GetSecondsSinceComputerActive (静态)

```csharp
uint GetSecondsSinceComputerActive()
```

**返回值:** `uint`

**用法示例:**
```csharp
uint secondsSinceActive = SteamGameServerUtils.GetSecondsSinceComputerActive();
```

### GetConnectedUniverse (静态)

```csharp
EUniverse GetConnectedUniverse()
```

客户端正在连接的宇宙

**返回值:** `EUniverse`

**用法示例:**
```csharp
EUniverse universe = SteamGameServerUtils.GetConnectedUniverse();
Console.WriteLine(universe);
```

### GetServerRealTime (静态)

```csharp
uint GetServerRealTime()
```

Steam 服务器时间。自格林威治标准时间（GMT）1970 年 1 月 1 日起的秒数（即 Unix 时间戳）。

**返回值:** `uint`

**用法示例:**
```csharp
uint serverTime = SteamGameServerUtils.GetServerRealTime();
Console.WriteLine(serverTime);
```

### GetIPCountry (静态)

```csharp
string GetIPCountry()
```

返回该客户端所在国家的两位 ISO 3166-1-alpha-2 格式国家代码（通过 IP 到地理位置数据库查询获得），例如"US"或"UK"。

**返回值:** `string`

**用法示例:**
```csharp
string countryCode = SteamGameServerUtils.GetIPCountry();
Console.WriteLine(countryCode);
```

### GetImageSize (静态)

```csharp
bool GetImageSize(int iImage, out uint pnWidth, out uint pnHeight)
```

<para>如果图像存在且有效尺寸已填写，则返回 true</para>

**参数:**

- `iImage` (`int`)
- `pnWidth` (`out uint`)
- `pnHeight` (`out uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint width, height;
bool ok = SteamGameServerUtils.GetImageSize(imageId, out width, out height);
```

### GetImageRGBA (静态)

```csharp
bool GetImageRGBA(int iImage, byte[] pubDest, int nDestBufferSize)
```

<para>若图像存在且缓冲区填充成功，则返回 true</para> <para>结果以 RGBA 格式返回</para> <para>目标缓冲区大小应为 4 * height * width * sizeof(char)</para>

**参数:**

- `iImage` (`int`)
- `pubDest` (`byte[]`)
- `nDestBufferSize` (`int`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerUtils.GetImageRGBA(imageId, imageRgbaBuffer, imageRgbaBuffer.Length);
if (ok) { /* imageRgbaBuffer contains RGBA data */ }
```

### GetCurrentBatteryPower (静态)

```csharp
byte GetCurrentBatteryPower()
```

返回当前系统中剩余的电池电量百分比（范围：0..100），若接市电供电则返回 255。

**返回值:** `byte`

**用法示例:**
```csharp
byte battery = SteamGameServerUtils.GetCurrentBatteryPower();
```

### GetAppID (静态)

```csharp
AppId_t GetAppID()
```

<para>返回当前进程的 AppID</para>

**返回值:** `AppId_t`

**用法示例:**
```csharp
var appId = SteamGameServerUtils.GetAppID();
Console.WriteLine(appId);
```

### SetOverlayNotificationPosition (静态)

```csharp
void SetOverlayNotificationPosition(ENotificationPosition eNotificationPosition)
```

<para>设置当前调用游戏所对应的叠加层实例显示通知的位置。</para> <para>此位置按游戏区分，若在游戏上下文之外调用此函数，则不会产生任何效果。</para>

**参数:**

- `eNotificationPosition` (`ENotificationPosition`)

**用法示例:**
```csharp
SteamGameServerUtils.SetOverlayNotificationPosition(ENotificationPosition.TopRight);
```

### IsAPICallCompleted (静态)

```csharp
bool IsAPICallCompleted(SteamAPICall_t hSteamAPICall, out bool pbFailed)
```

<para> API 异步调用结果</para> <para> 可直接使用，但更常通过回调分发 API 使用（参见 steam_api.h）</para>

**参数:**

- `hSteamAPICall` (`SteamAPICall_t`)
- `pbFailed` (`out bool`)

**返回值:** `bool`

**用法示例:**
```csharp
bool failed;
bool completed = SteamGameServerUtils.IsAPICallCompleted(hSteamAPICall, out failed);
```

### GetAPICallFailureReason (静态)

```csharp
ESteamAPICallFailure GetAPICallFailureReason(SteamAPICall_t hSteamAPICall)
```

**参数:**

- `hSteamAPICall` (`SteamAPICall_t`)

**返回值:** `ESteamAPICallFailure`

**用法示例:**
```csharp
var failureReason = SteamGameServerUtils.GetAPICallFailureReason(apiCall);
```

### GetAPICallResult (静态)

```csharp
bool GetAPICallResult(SteamAPICall_t hSteamAPICall, IntPtr pCallback, int cubCallback, int iCallbackExpected, out bool pbFailed)
```

**参数:**

- `hSteamAPICall` (`SteamAPICall_t`)
- `pCallback` (`IntPtr`)
- `cubCallback` (`int`)
- `iCallbackExpected` (`int`)
- `pbFailed` (`out bool`)

**返回值:** `bool`

**用法示例:**
```csharp
bool failed;
bool ok = SteamGameServerUtils.GetAPICallResult(hSteamAPICall, callbackPtr, callbackSize, callbackId, out failed);
```

### GetIPCCallCount (静态)

```csharp
uint GetIPCCallCount()
```

返回自上次调用此函数以来所执行的 IPC 调用次数。  
用于性能调试，以便了解每帧中游戏发起的 IPC 调用数量。  
每次 IPC 调用至少涉及一次线程上下文切换，若跨越进程则更为昂贵，因此需控制其执行频率。

**返回值:** `uint`

**用法示例:**
```csharp
uint ipcCount = SteamGameServerUtils.GetIPCCallCount();
Console.WriteLine($"IPC calls since last check: {ipcCount}");
```

### SetWarningMessageHook (静态)

```csharp
void SetWarningMessageHook(SteamAPIWarningMessageHook_t pFunction)
```

<para>API 警告处理</para> <para>'int'表示严重程度；0 代表消息，1 代表警告</para> <para>'const char *'为消息文本</para> <para>回调将在生成该警告或消息的 API 函数调用后立即发生</para>

**参数:**

- `pFunction` (`SteamAPIWarningMessageHook_t`)

**用法示例:**
```csharp
SteamGameServerUtils.SetWarningMessageHook((severity, message) => Console.WriteLine($"[SteamAPI {severity}] {message}"));
```

### IsOverlayEnabled (静态)

```csharp
bool IsOverlayEnabled()
```

返回 true 表示覆盖层正在运行且用户可访问。覆盖层进程可能需要数秒才能启动并挂钩游戏进程，因此在该函数调用初期，当覆盖层处于加载状态时，将返回 false。

**返回值:** `bool`

**用法示例:**
```csharp
bool overlayEnabled = SteamGameServerUtils.IsOverlayEnabled();
if (overlayEnabled) Console.WriteLine("Overlay is available.");
```

### BOverlayNeedsPresent (静态)

```csharp
bool BOverlayNeedsPresent()
```

通常，如果您的游戏拥有持续运行的帧循环并在每帧调用 D3D Present API 或 OGL SwapBuffers API，则无需此调用。然而，如果您的游戏仅在事件触发时刷新屏幕，则可能会破坏覆盖层（overlay），因为覆盖层依赖您的 Present/SwapBuffers 调用来驱动其内部帧循环。此外，当发生需要通知的事件或用户将覆盖层唤出至游戏上方时，覆盖层也可能需要执行 Present() 操作以渲染到屏幕。在这种情况下，您可以使用此 API 查询覆盖层当前是否需要执行 Present 操作；随后建议定期检查（频率约为 33Hz）并务必通过 Present 或 SwapBuffers 刷新屏幕，以确保覆盖层能够正常执行其工作。

**返回值:** `bool`

**用法示例:**
```csharp
if (SteamGameServerUtils.BOverlayNeedsPresent()) RenderFrame();
```

### CheckFileSignature (静态)

```csharp
SteamAPICall_t CheckFileSignature(string szFileName)
```

异步调用，用于检查可执行文件是否使用合作伙伴站点“签名”选项卡中设置的公钥进行了签名，例如拒绝加载被篡改的可执行文件。结果将通过 CheckFileSignature_t 结构体返回。k_ECheckFileSignatureNoSignaturesFoundForThisApp - 该应用程序未在合作伙伴站点的“签名”选项卡上配置以启用此功能。k_ECheckFileSignatureNoSignaturesFoundForThisFile - 该文件未列在合作伙伴站点的“签名”选项卡中。k_ECheckFileSignatureFileNotFound - 该文件在磁盘上不存在。k_ECheckFileSignatureInvalidSignature - 该文件存在，且其“签名”选项卡已设置，但该文件未被签名或签名不匹配。k_ECheckFileSignatureValidSignature - 该文件已签名且签名有效。

**参数:**

- `szFileName` (`string`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServerUtils.CheckFileSignature("game.exe");
```

### ShowGamepadTextInput (静态)

```csharp
bool ShowGamepadTextInput(EGamepadTextInputMode eInputMode, EGamepadTextInputLineMode eLineInputMode, string pchDescription, uint unCharMax, string pchExistingText)
```

<para>激活全屏文本输入对话框，该对话框接收一个初始文本字符串，并返回用户输入的文本。</para>

**参数:**

- `eInputMode` (`EGamepadTextInputMode`)
- `eLineInputMode` (`EGamepadTextInputLineMode`)
- `pchDescription` (`string`)
- `unCharMax` (`uint`)
- `pchExistingText` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUtils.ShowGamepadTextInput(EGamepadTextInputMode.Normal, EGamepadTextInputLineMode.SingleLine, "请输入名称", 32, "Player1");
```

### GetEnteredGamepadTextLength (静态)

```csharp
uint GetEnteredGamepadTextLength()
```

返回先前输入的文本及其长度

**返回值:** `uint`

**用法示例:**
```csharp
uint length = SteamGameServerUtils.GetEnteredGamepadTextLength();
```

### GetEnteredGamepadTextInput (静态)

```csharp
bool GetEnteredGamepadTextInput(out string pchText, uint cchText)
```

**参数:**

- `pchText` (`out string`)
- `cchText` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
string text;
bool hasText = SteamGameServerUtils.GetEnteredGamepadTextInput(out text, 256u);
```

### GetSteamUILanguage (静态)

```csharp
string GetSteamUILanguage()
```

返回 Steam 客户端当前运行的语言，通常您应使用 ISteamApps::GetCurrentGameLanguage；本接口仅适用于极少数特殊用例。

**返回值:** `string`

**用法示例:**
```csharp
string uiLanguage = SteamGameServerUtils.GetSteamUILanguage();
Console.WriteLine(uiLanguage);
```

### IsSteamRunningInVR (静态)

```csharp
bool IsSteamRunningInVR()
```

<para>如果 Steam 本身处于 VR 模式运行，则返回 true</para>

**返回值:** `bool`

**用法示例:**
```csharp
Console.WriteLine(SteamGameServerUtils.IsSteamRunningInVR() ? "Steam 正在 VR 模式运行" : "Steam 未在 VR 模式运行");
```

### SetOverlayNotificationInset (静态)

```csharp
void SetOverlayNotificationInset(int nHorizontalInset, int nVerticalInset)
```

<para>设置叠加层通知相对于 SetOverlayNotificationPosition 指定的角落的内边距。</para>

**参数:**

- `nHorizontalInset` (`int`)
- `nVerticalInset` (`int`)

**用法示例:**
```csharp
SteamGameServerUtils.SetOverlayNotificationInset(20, 10);
```

### IsSteamInBigPictureMode (静态)

```csharp
bool IsSteamInBigPictureMode()
```

<para>当 Steam 和 Steam 覆盖层正在以大屏幕模式运行时返回 true</para> <para>游戏必须通过 Steam 客户端启动才能启用大屏幕覆盖层。在开发过程中，可以将游戏作为非 Steam 游戏添加到开发者库中以测试此功能。</para>

**返回值:** `bool`

**用法示例:**
```csharp
bool isBigPictureMode = SteamGameServerUtils.IsSteamInBigPictureMode();
if (isBigPictureMode) Console.WriteLine("Steam is running in Big Picture mode.");
```

### StartVRDashboard (静态)

```csharp
void StartVRDashboard()
```

请求 SteamUI 创建并渲染其 OpenVR 仪表盘

**用法示例:**
```csharp
SteamGameServerUtils.StartVRDashboard();
```

### IsVRHeadsetStreamingEnabled (静态)

```csharp
bool IsVRHeadsetStreamingEnabled()
```

<para>如果 HMD 内容将通过 Steam 远程播放进行流式传输，则返回 true。</para>

**返回值:** `bool`

**用法示例:**
```csharp
bool isStreaming = SteamGameServerUtils.IsVRHeadsetStreamingEnabled();
if (isStreaming) { }
```

### SetVRHeadsetStreamingEnabled (静态)

```csharp
void SetVRHeadsetStreamingEnabled(bool bEnabled)
```

<para>设置是否通过 Steam 远程游玩流式传输 HMD（头戴式显示器）内容。</para> <para>如果设置为 true，则头显中的场景将被流式传输，且不允许远程输入。</para> <para>如果设置为 false，则应用程序窗口将被流式传输，并允许远程输入。</para> <para>默认值为 true，除非游戏的扩展应用信息中包含 "VRHeadsetStreaming" "0"。</para> <para>（这对于具有非对称多人游戏模式的游戏非常有用。）</para>

**参数:**

- `bEnabled` (`bool`)

**用法示例:**
```csharp
SteamGameServerUtils.SetVRHeadsetStreamingEnabled(true);
```

### IsSteamChinaLauncher (静态)

```csharp
bool IsSteamChinaLauncher()
```

<para>返回此 Steam 客户端是否为专为中国市场设计的 Steam 中国客户端，而非全球通用客户端。</para>

**返回值:** `bool`

**用法示例:**
```csharp
bool isChinaLauncher = SteamGameServerUtils.IsSteamChinaLauncher();
if (isChinaLauncher) Console.WriteLine("Steam China launcher");
```

### InitFilterText (静态)

```csharp
bool InitFilterText(uint unFilterOptions = 0)
```

<para> 初始化文本过滤功能，加载游戏当前运行语言对应的词典。</para><para> unFilterOptions 保留供将来使用，应设置为 0。</para><para> 如果游戏的语言不支持过滤功能，则返回 false；此时 FilterText() 将作为直通处理（即原样返回）。</para><para> 用户可在其 Steam 账户偏好设置中自定义文本过滤行为：</para><para> https://store.steampowered.com/account/preferences#CommunityContentPreferences</para>

**参数:**

- `unFilterOptions` (`uint`) = `0`

**返回值:** `bool`

**用法示例:**
```csharp
bool filterSupported = SteamGameServerUtils.InitFilterText(0);
```

### FilterText (静态)

```csharp
int FilterText(ETextFilteringContext eContext, CSteamID sourceSteamID, string pchInputMessage, out string pchOutFilteredText, uint nByteSizeOutFilteredText)
```

<para>根据法律要求的过滤规则，并结合上下文与用户设置进行额外过滤，将提供的输入消息处理后结果写入 pchOutFilteredText。</para><para>eContext 表示输入字符串中的内容类型。</para><para>sourceSteamID 为输入字符串来源的 Steam ID（例如：显示该名称的玩家或发送聊天文本的用户）。</para><para>pchInputText 是需要被过滤的输入字符串，可为 ASCII 或 UTF-8 编码。</para><para>pchOutFilteredText 是输出结果的存放位置，即使未执行任何过滤操作也会写入数据。</para><para>nByteSizeOutFilteredText 是 pchOutFilteredText 的大小（以字节计），应至少为 strlen(pchInputText)+1。</para><para>返回被过滤的字符数量（非字节数）。</para>

**参数:**

- `eContext` (`ETextFilteringContext`)
- `sourceSteamID` (`CSteamID`)
- `pchInputMessage` (`string`)
- `pchOutFilteredText` (`out string`)
- `nByteSizeOutFilteredText` (`uint`)

**返回值:** `int`

**用法示例:**
```csharp
string filteredText; int filteredCount = SteamGameServerUtils.FilterText(ETextFilteringContext.Chat, sourceSteamID, inputMessage, out filteredText, 1024);
```

### GetIPv6ConnectivityState (静态)

```csharp
ESteamIPv6ConnectivityState GetIPv6ConnectivityState(ESteamIPv6ConnectivityProtocol eProtocol)
```

<para>返回我们认为您当前通过指定协议对“互联网”的 IPv6 连接状态。</para><para>此方法并不表示 Steam 客户端当前是否已通过 IPv6 连接到 Steam。</para>

**参数:**

- `eProtocol` (`ESteamIPv6ConnectivityProtocol`)

**返回值:** `ESteamIPv6ConnectivityState`

**用法示例:**
```csharp
var ipv6State = SteamGameServerUtils.GetIPv6ConnectivityState(ESteamIPv6ConnectivityProtocol.HTTP);
```

### IsSteamRunningOnSteamDeck (静态)

```csharp
bool IsSteamRunningOnSteamDeck()
```

<para>如果当前在 Steam Deck 设备上运行则返回 true</para>

**返回值:** `bool`

**用法示例:**
```csharp
if (SteamGameServerUtils.IsSteamRunningOnSteamDeck()) Console.WriteLine("Running on Steam Deck");
```

### ShowFloatingGamepadTextInput (静态)

```csharp
bool ShowFloatingGamepadTextInput(EFloatingGamepadTextInputMode eKeyboardMode, int nTextFieldXPosition, int nTextFieldYPosition, int nTextFieldWidth, int nTextFieldHeight)
```

<para>在游戏内容上方打开浮动键盘，并将操作系统的键盘按键直接发送至游戏。</para><para>文本字段的位置以相对于游戏窗口原点的像素值指定，用于定位浮动键盘，使其不遮挡该文本字段。</para>

**参数:**

- `eKeyboardMode` (`EFloatingGamepadTextInputMode`)
- `nTextFieldXPosition` (`int`)
- `nTextFieldYPosition` (`int`)
- `nTextFieldWidth` (`int`)
- `nTextFieldHeight` (`int`)

**返回值:** `bool`

**用法示例:**
```csharp
bool shown = SteamGameServerUtils.ShowFloatingGamepadTextInput(EFloatingGamepadTextInputMode.SingleLine, 100, 200, 300, 40);
```

### SetGameLauncherMode (静态)

```csharp
void SetGameLauncherMode(bool bLauncherMode)
```

对于不支持控制器的游戏启动器，您可以调用此接口，使 Steam Input 将控制器输入转换为鼠标/键盘输入，以便导航该启动器。

**参数:**

- `bLauncherMode` (`bool`)

**用法示例:**
```csharp
SteamGameServerUtils.SetGameLauncherMode(true);
```

### DismissFloatingGamepadTextInput (静态)

```csharp
bool DismissFloatingGamepadTextInput()
```

<para>隐藏浮动键盘。</para>

**返回值:** `bool`

**用法示例:**
```csharp
bool hidden = SteamGameServerUtils.DismissFloatingGamepadTextInput();
```

### DismissGamepadTextInput (静态)

```csharp
bool DismissGamepadTextInput()
```

<para>关闭全屏文本输入对话框。</para>

**返回值:** `bool`

**用法示例:**
```csharp
bool dismissed = SteamGameServerUtils.DismissGamepadTextInput();
```

