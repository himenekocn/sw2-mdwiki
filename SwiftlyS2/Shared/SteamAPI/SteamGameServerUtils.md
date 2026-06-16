<a id="steamgameserverutils"></a>

# 📦 SteamGameServerUtils

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### GetSecondsSinceAppActive (静态)

```csharp
uint GetSecondsSinceAppActive()
```

返回自用户以来的秒数

**返回值:** `uint`

**用法示例:**
```csharp
uint seconds = SteamGameServerUtils.GetSecondsSinceAppActive();
```

### GetSecondsSinceComputerActive (静态)

```csharp
uint GetSecondsSinceComputerActive()
```

**返回值:** `uint`

**用法示例:**
```csharp
uint seconds = SteamGameServerUtils.GetSecondsSinceComputerActive();
```

### GetConnectedUniverse (静态)

```csharp
EUniverse GetConnectedUniverse()
```

<para>此客户端正在连接的游戏世界</para>

**返回值:** `EUniverse`

**用法示例:**
```csharp
EUniverse universe = SteamGameServerUtils.GetConnectedUniverse();
```

### GetServerRealTime (静态)

```csharp
uint GetServerRealTime()
```

<para>Steam服务器时间。自1970年1月1日GMT（即Unix时间）以来的秒数</para>

**返回值:** `uint`

**用法示例:**
```csharp
uint serverTime = SteamGameServerUtils.GetServerRealTime();
```

### GetIPCountry (静态)

```csharp
string GetIPCountry()
```

<para>返回该客户端运行所在地的两位ISO 3166-1-alpha-2格式国家代码（通过IP地址地理位置数据库查询）</para> <para> 例如 "US" 或 "UK"。</para>

**返回值:** `string`

**用法示例:**
```csharp
string countryCode = SteamGameServerUtils.GetIPCountry();
```

### GetImageSize (静态)

```csharp
bool GetImageSize(int iImage, out uint pnWidth, out uint pnHeight)
```

<para> 如果图像存在且有效尺寸已填充，则返回 true</para>

**参数:**

- `iImage` (`int`)
- `pnWidth` (`out uint`)
- `pnHeight` (`out uint`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUtils.GetImageSize(0, out uint width, out uint height);
```

### GetImageRGBA (静态)

```csharp
bool GetImageRGBA(int iImage, byte[] pubDest, int nDestBufferSize)
```

<para> 如果图像存在且缓冲区成功填充，则返回 true</para>
<para> 结果以 RGBA 格式返回</para>
<para> 目标缓冲区大小应为 4 * 高度 * 宽度 * sizeof(char)</para>

**参数:**

- `iImage` (`int`)
- `pubDest` (`byte[]`)
- `nDestBufferSize` (`int`)

**返回值:** `bool`

**用法示例:**
```csharp
byte[] buffer = new byte[1024];
bool success = SteamGameServerUtils.GetImageRGBA(0, buffer, buffer.Length);
```

### GetCurrentBatteryPower (静态)

```csharp
byte GetCurrentBatteryPower()
```

<para> 返回当前系统中剩余电池电量的百分比 [0..100]，255 表示正在使用交流电源</para>

**返回值:** `byte`

**用法示例:**
```csharp
byte batteryLevel = SteamGameServerUtils.GetCurrentBatteryPower();
```

### GetAppID (静态)

```csharp
AppId_t GetAppID()
```

<para>返回当前进程的应用ID</para>

**返回值:** `AppId_t`

**用法示例:**
```csharp
AppId_t appId = SteamGameServerUtils.GetAppID();
```

### SetOverlayNotificationPosition (静态)

```csharp
void SetOverlayNotificationPosition(ENotificationPosition eNotificationPosition)
```

<para> 设置当前调用游戏的覆盖层实例应显示通知的位置。</para> <para> 此位置基于每个游戏独立设置，如果从游戏上下文之外调用此函数，则将不执行任何操作。</para>

**参数:**

- `eNotificationPosition` (`ENotificationPosition`)

**用法示例:**
```csharp
SteamGameServerUtils.SetOverlayNotificationPosition(ENotificationPosition.TopLeft);
```

### IsAPICallCompleted (静态)

```csharp
bool IsAPICallCompleted(SteamAPICall_t hSteamAPICall, out bool pbFailed)
```

<para> API 异步调用结果</para>
<para> 可直接使用，但更常见的是通过回调调度 API 使用（参见 steam_api.h）</para>

**参数:**

- `hSteamAPICall` (`SteamAPICall_t`)
- `pbFailed` (`out bool`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamAPICall_t callHandle = default;
bool result = SteamGameServerUtils.IsAPICallCompleted(callHandle, out bool pbFailed);
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
SteamAPICall_t callHandle = SteamGameServer.LogOnAnonymous();
ESteamAPICallFailure failureReason = SteamGameServerUtils.GetAPICallFailureReason(callHandle);
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
bool pbFailed;
bool result = SteamGameServerUtils.GetAPICallResult(hSteamAPICall, pCallback, cubCallback, iCallbackExpected, out pbFailed);
```

### GetIPCCallCount (静态)

```csharp
uint GetIPCCallCount()
```

<para> 返回自上次调用此函数以来所发出的IPC调用次数</para>
<para> 用于性能调试，以便了解您的游戏每帧进行了多少次IPC调用</para>
<para> 每次IPC调用至少是一次线程上下文切换，甚至可能是一次进程上下文切换，因此需要</para>
<para> 控制其执行频率。</para>

**返回值:** `uint`

**用法示例:**
```csharp
uint ipcCalls = SteamGameServerUtils.GetIPCCallCount();
System.Console.WriteLine($"IPC calls since last check: {ipcCalls}");
```

### SetWarningMessageHook (静态)

```csharp
void SetWarningMessageHook(SteamAPIWarningMessageHook_t pFunction)
```

<para> API 警告处理</para>  
<para> 'int' 表示严重程度；0 表示消息，1 表示警告</para>  
<para> 'const char *' 是消息文本</para>  
<para> 回调将在生成警告或消息的 API 函数被调用后立即发生</para>

**参数:**

- `pFunction` (`SteamAPIWarningMessageHook_t`)

**用法示例:**
```csharp
SteamGameServerUtils.SetWarningMessageHook((severity, message) => System.Console.WriteLine($"[{severity}] {message}"));
```

### IsOverlayEnabled (静态)

```csharp
bool IsOverlayEnabled()
```

<para> 如果叠加层正在运行且用户可以访问它，则返回 true。叠加层进程可能需要几秒钟才能</para> <para> 启动并挂钩游戏进程，因此在叠加层加载期间，此函数最初会返回 false。</para>

**返回值:** `bool`

**用法示例:**
```csharp
bool isEnabled = SteamGameServerUtils.IsOverlayEnabled();
```

### BOverlayNeedsPresent (静态)

```csharp
bool BOverlayNeedsPresent()
```

<para> 通常情况下，如果你的游戏有一个持续运行的帧循环，且每帧都会调用</para> <para> D3D Present API 或 OGL SwapBuffers API，则无需此调用。</para> <para> 然而，如果你的游戏仅在事件驱动的基础上刷新屏幕，这可能会破坏</para> <para> 覆盖层，因为它利用你的 Present/SwapBuffers 调用来驱动其内部帧循环，并且它可能还需要</para> <para> 在任何需要通知的事件发生时，或用户将覆盖层</para> <para> 唤起到游戏上方时，调用 Present() 来显示画面。在这种情况下，你可以使用此 API 询问覆盖层当前是否需要调用 Present，</para> <para> 然后你可以定期检查这一点（理想频率约为 33Hz），并确保</para> <para> 通过 Present 或 SwapBuffers 刷新屏幕，以允许覆盖层执行其工作。</para>

**返回值:** `bool`

**用法示例:**
```csharp
bool needsPresent = SteamGameServerUtils.BOverlayNeedsPresent();
if (needsPresent) SwapBuffers();
```

### CheckFileSignature (静态)

```csharp
SteamAPICall_t CheckFileSignature(string szFileName)
```

<para> 异步调用，用于检查可执行文件是否已使用合作伙伴网站签名选项卡上设置的公钥进行签名</para>
<para> 例如，拒绝加载修改过的可执行文件。</para>
<para> 结果在 CheckFileSignature_t 中返回。</para>
<para> k_ECheckFileSignatureNoSignaturesFoundForThisApp - 此应用尚未在合作伙伴网站的签名选项卡上配置以启用此功能。</para>
<para> k_ECheckFileSignatureNoSignaturesFoundForThisFile - 此文件未列在合作伙伴网站的签名选项卡上。</para>
<para> k_ECheckFileSignatureFileNotFound - 磁盘上不存在该文件。</para>
<para> k_ECheckFileSignatureInvalidSignature - 文件存在，且签名选项卡已为此文件设置，但文件未签名或签名不匹配。</para>
<para> k_ECheckFileSignatureValidSignature - 文件已签名且签名有效。</para>

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

<para> 激活全屏文本输入对话框，该对话框接收初始文本字符串并返回用户输入的文本</para>

**参数:**

- `eInputMode` (`EGamepadTextInputMode`)
- `eLineInputMode` (`EGamepadTextInputLineMode`)
- `pchDescription` (`string`)
- `unCharMax` (`uint`)
- `pchExistingText` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = SteamGameServerUtils.ShowGamepadTextInput(EGamepadTextInputMode.Normal, EGamepadTextInputLineMode.SingleLine, "Enter text", 100, "");
```

### GetEnteredGamepadTextLength (静态)

```csharp
uint GetEnteredGamepadTextLength()
```

<para> 返回先前输入的文本和长度</para>

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
bool success = SteamGameServerUtils.GetEnteredGamepadTextInput(out text, 256);
```

### GetSteamUILanguage (静态)

```csharp
string GetSteamUILanguage()
```

<para>返回Steam客户端当前运行的语言，通常情况下您应改用ISteamApps::GetCurrentGameLanguage，此接口仅适用于非常特殊的用例</para>

**返回值:** `string`

**用法示例:**
```csharp
string language = SteamGameServerUtils.GetSteamUILanguage();
```

### IsSteamRunningInVR (静态)

```csharp
bool IsSteamRunningInVR()
```

<para> 如果 Steam 本身以 VR 模式运行，则返回 true</para>

**返回值:** `bool`

**用法示例:**
```csharp
bool isVR = SteamGameServerUtils.IsSteamRunningInVR();
```

### SetOverlayNotificationInset (静态)

```csharp
void SetOverlayNotificationInset(int nHorizontalInset, int nVerticalInset)
```

<para> 设置叠加通知相对于由 SetOverlayNotificationPosition 指定的角落的边缘偏移。</para>

**参数:**

- `nHorizontalInset` (`int`)
- `nVerticalInset` (`int`)

**用法示例:**
```csharp
SteamGameServerUtils.SetOverlayNotificationInset(10, 10);
```

### IsSteamInBigPictureMode (静态)

```csharp
bool IsSteamInBigPictureMode()
```

<para> 如果 Steam 和 Steam 覆盖层正在大屏幕模式下运行，则返回 true</para>
<para> 游戏必须通过 Steam 客户端启动才能启用大屏幕覆盖层。在开发过程中，</para>
<para> 可以将游戏作为非 Steam 游戏添加到开发者的库中，以测试此功能</para>

**返回值:** `bool`

**用法示例:**
```csharp
bool isInBigPicture = SteamGameServerUtils.IsSteamInBigPictureMode();
```

### StartVRDashboard (静态)

```csharp
void StartVRDashboard()
```

<para> 请求SteamUI创建并渲染其OpenVR仪表盘</para>

**用法示例:**
```csharp
SteamGameServerUtils.StartVRDashboard();
```

### IsVRHeadsetStreamingEnabled (静态)

```csharp
bool IsVRHeadsetStreamingEnabled()
```

<para> 如果HMD内容将通过Steam远程同乐进行流式传输，则返回true</para>

**返回值:** `bool`

**用法示例:**
```csharp
bool isStreaming = SteamGameServerUtils.IsVRHeadsetStreamingEnabled();
```

### SetVRHeadsetStreamingEnabled (静态)

```csharp
void SetVRHeadsetStreamingEnabled(bool bEnabled)
```

<para> 设置是否通过 Steam 远程畅玩流式传输 HMD 内容</para>
<para> 如果设置为 true，则头戴式显示器中的场景将被流式传输，且不允许远程输入。</para>
<para> 如果设置为 false，则应用程序窗口将被流式传输，且允许远程输入。</para>
<para> 默认值为 true，除非游戏的扩展应用信息中包含 "VRHeadsetStreaming" "0"。</para>
<para> （这对于具有非对称多人游戏玩法的游戏很有用）</para>

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

<para> 返回此Steam客户端是否为Steam China特定客户端，而非全球客户端。</para>

**返回值:** `bool`

**用法示例:**
```csharp
bool isChinaLauncher = SteamGameServerUtils.IsSteamChinaLauncher();
```

### InitFilterText (静态)

```csharp
bool InitFilterText(uint unFilterOptions = 0)
```

<para> 初始化文本过滤功能，加载游戏当前运行语言的词典。</para> <para> unFilterOptions 参数保留供将来使用，应设置为 0。</para> <para> 如果游戏语言不支持过滤功能，则返回 false，此时 FilterText() 将作为直通函数运行。</para> <para> 用户可以在其 Steam 账户偏好设置中自定义文本过滤行为：</para> <para> https://store.steampowered.com/account/preferences#CommunityContentPreferences</para>

**参数:**

- `unFilterOptions` (`uint`) = `0`

**返回值:** `bool`

**用法示例:**
```csharp
bool isInitialized = SteamGameServerUtils.InitFilterText(0);
```

### FilterText (静态)

```csharp
int FilterText(ETextFilteringContext eContext, CSteamID sourceSteamID, string pchInputMessage, out string pchOutFilteredText, uint nByteSizeOutFilteredText)
```

<para> 根据法律要求的过滤以及基于上下文和用户设置的附加过滤，过滤提供的输入消息，并将过滤结果放入 pchOutFilteredText 中</para> <para> eContext 是输入字符串中内容的类型</para> <para> sourceSteamID 是输入字符串来源的 Steam ID（例如，拥有名称的玩家，或说出聊天文本的玩家）</para> <para> pchInputText 是应被过滤的输入字符串，可以是 ASCII 或 UTF-8 格式</para> <para> pchOutFilteredText 是输出存放的位置，即使未执行任何过滤也会放置输出</para> <para> nByteSizeOutFilteredText 是 pchOutFilteredText 的大小（以字节为单位），应至少为 strlen(pchInputText)+1</para> <para> 返回被过滤的字符数（而非字节数）</para>

**参数:**

- `eContext` (`ETextFilteringContext`)
- `sourceSteamID` (`CSteamID`)
- `pchInputMessage` (`string`)
- `pchOutFilteredText` (`out string`)
- `nByteSizeOutFilteredText` (`uint`)

**返回值:** `int`

**用法示例:**
```csharp
string input = "Hello World"; SteamGameServerUtils.FilterText(ETextFilteringContext.k_ETextFilteringContextGameContent, new CSteamID(76561197960287930), input, out string filtered, (uint)(input.Length + 1));
```

### GetIPv6ConnectivityState (静态)

```csharp
ESteamIPv6ConnectivityState GetIPv6ConnectivityState(ESteamIPv6ConnectivityProtocol eProtocol)
```

<para> 返回我们认为您在指定协议上当前与"互联网"的IPv6连接状况。</para> <para> 这并不告知您Steam客户端当前是否通过IPv6连接到Steam。</para>

**参数:**

- `eProtocol` (`ESteamIPv6ConnectivityProtocol`)

**返回值:** `ESteamIPv6ConnectivityState`

**用法示例:**
```csharp
var state = SteamGameServerUtils.GetIPv6ConnectivityState(ESteamIPv6ConnectivityProtocol.Value);
```

### IsSteamRunningOnSteamDeck (静态)

```csharp
bool IsSteamRunningOnSteamDeck()
```

<para> 如果当前在 Steam Deck 设备上运行，则返回 true</para>

**返回值:** `bool`

**用法示例:**
```csharp
bool isOnDeck = SteamGameServerUtils.IsSteamRunningOnSteamDeck();
```

### ShowFloatingGamepadTextInput (静态)

```csharp
bool ShowFloatingGamepadTextInput(EFloatingGamepadTextInputMode eKeyboardMode, int nTextFieldXPosition, int nTextFieldYPosition, int nTextFieldWidth, int nTextFieldHeight)
```

<para> 在游戏内容上方打开浮动键盘，并将操作系统键盘按键直接发送到游戏。</para> <para> 文本框位置以像素为单位指定，相对于游戏窗口的原点，用于定位浮动键盘，使其不会遮挡文本框。</para>

**参数:**

- `eKeyboardMode` (`EFloatingGamepadTextInputMode`)
- `nTextFieldXPosition` (`int`)
- `nTextFieldYPosition` (`int`)
- `nTextFieldWidth` (`int`)
- `nTextFieldHeight` (`int`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = SteamGameServerUtils.ShowFloatingGamepadTextInput(EFloatingGamepadTextInputMode.Value, 100, 100, 300, 50);
```

### SetGameLauncherMode (静态)

```csharp
void SetGameLauncherMode(bool bLauncherMode)
```

<para> 在不支持控制器的游戏启动器中，你可以调用此方法让 Steam Input 将控制器输入转换为鼠标/键盘操作以导航启动器</para>

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

<para>关闭浮动键盘。</para>

**返回值:** `bool`

**用法示例:**
```csharp
bool result = SteamGameServerUtils.DismissFloatingGamepadTextInput();
```

### DismissGamepadTextInput (静态)

```csharp
bool DismissGamepadTextInput()
```

<para> 关闭全屏文本输入对话框。</para>

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUtils.DismissGamepadTextInput();
```

