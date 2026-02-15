# 📦 SteamGameServerUtils

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### GetSecondsSinceAppActive (静态)

```csharp
uint GetSecondsSinceAppActive()
```

<para> 返回自用户以来经过的秒数</para>

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

<para>此客户端正在连接的宇宙</para>

**返回值:** `EUniverse`

**用法示例:**
```csharp
EUniverse universe = SteamGameServerUtils.GetConnectedUniverse();
```

### GetServerRealTime (静态)

```csharp
uint GetServerRealTime()
```

Steam服务器时间。自1970年1月1日以来的秒数，格林尼治标准时间（即Unix时间）。

**返回值:** `uint`

**用法示例:**
```csharp
uint serverTime = SteamGameServerUtils.GetServerRealTime();
```

### GetIPCountry (静态)

```csharp
string GetIPCountry()
```

<para> 返回此客户端所在国家的两位数 ISO 3166-1-alpha-2 格式国家代码（通过 IP 到地理位置数据库查询获取）。</para> <para> 例如 "US" 或 "UK"。</para>

**返回值:** `string`

**用法示例:**
```csharp
string country = SteamGameServerUtils.GetIPCountry();
```

### GetImageSize (静态)

```csharp
bool GetImageSize(int iImage, out uint pnWidth, out uint pnHeight)
```

<para>如果图像存在，并且有效的大小已填写，则返回 true</para>

**参数:**

- `iImage` (`int`)
- `pnWidth` (`out uint`)
- `pnHeight` (`out uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint width, height;
bool result = SteamGameServerUtils.GetImageSize(0, out width, out height);
```

### GetImageRGBA (静态)

```csharp
bool GetImageRGBA(int iImage, byte[] pubDest, int nDestBufferSize)
```

<para>如果图像存在且缓冲区已成功填充，则返回 true</para> <para>结果以 RGBA 格式返回</para> <para>目标缓冲区大小应为 4 * height * width * sizeof(char)</para>

**参数:**

- `iImage` (`int`)
- `pubDest` (`byte[]`)
- `nDestBufferSize` (`int`)

**返回值:** `bool`

**用法示例:**
```csharp
byte[] dest = new byte[4 * 1024 * 1024]; // 假设图像尺寸为1024x1024
bool success = SteamGameServerUtils.GetImageRGBA(0, dest, dest.Length);
```

### GetCurrentBatteryPower (静态)

```csharp
byte GetCurrentBatteryPower()
```

返回当前系统中剩余的电池电量百分比 [0..100]，若使用交流电源则返回 255。

**返回值:** `byte`

**用法示例:**
```csharp
byte battery = SteamGameServerUtils.GetCurrentBatteryPower();
```

### GetAppID (静态)

```csharp
AppId_t GetAppID()
```

<para> 返回当前进程的应用程序标识符（appID）</para>

**返回值:** `AppId_t`

**用法示例:**
```csharp
AppId_t appid = SteamGameServerUtils.GetAppID();
```

### SetOverlayNotificationPosition (静态)

```csharp
void SetOverlayNotificationPosition(ENotificationPosition eNotificationPosition)
```

<para>设置当前调用游戏的通知叠加层实例应显示的位置。</para> <para>此位置是每个游戏独有的，如果从游戏上下文外部调用此函数，则不会执行任何操作。</para>

**参数:**

- `eNotificationPosition` (`ENotificationPosition`)

**用法示例:**
```csharp
SteamGameServerUtils.SetOverlayNotificationPosition(ENotificationPosition.k_ENotificationPosition_TopLeft);
```

### IsAPICallCompleted (静态)

```csharp
bool IsAPICallCompleted(SteamAPICall_t hSteamAPICall, out bool pbFailed)
```

<para> API 异步调用结果</para> <para> 可以直接使用，但更常见的是通过回调分发 API 使用（请参阅 steam_api.h）</para>

**参数:**

- `hSteamAPICall` (`SteamAPICall_t`)
- `pbFailed` (`out bool`)

**返回值:** `bool`

**用法示例:**
```csharp
bool failed;
bool result = SteamGameServerUtils.IsAPICallCompleted(mySteamAPICall, out failed);
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
SteamAPICall_t call = default;
ESteamAPICallFailure result = SteamGameServerUtils.GetAPICallFailureReason(call);
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
bool result = SteamGameServerUtils.GetAPICallResult(callHandle, callbackPtr, 4, expectedCallbackId, out bool failed);
```

### GetIPCCallCount (静态)

```csharp
uint GetIPCCallCount()
```

<para>返回自上次调用此函数以来所进行的 IPC 调用次数。</para> <para>用于性能调试，以便了解您的游戏每帧执行多少次 IPC 调用。</para> <para>每次 IPC 调用至少会导致一次线程上下文切换，甚至可能是进程上下文切换，因此您需要控制执行它们的频率。</para>

**返回值:** `uint`

**用法示例:**
```csharp
uint ipcCalls = SteamGameServerUtils.GetIPCCallCount();
```

### SetWarningMessageHook (静态)

```csharp
void SetWarningMessageHook(SteamAPIWarningMessageHook_t pFunction)
```

<para> API 警告处理</para> <para> 'int' 是严重性等级；0 表示消息，1 表示警告</para> <para> 'const char *' 是消息的文本内容</para> <para> 回调函数将在产生警告或消息的 API 函数被调用后立即执行</para>

**参数:**

- `pFunction` (`SteamAPIWarningMessageHook_t`)

**用法示例:**
```csharp
SteamGameServerUtils.SetWarningMessageHook((severity, msg) => Console.WriteLine($"[{severity}] {msg}"));
```

### IsOverlayEnabled (静态)

```csharp
bool IsOverlayEnabled()
```

<para>如果覆盖层正在运行且用户可以访问它，则返回 true。覆盖层进程可能需要几秒钟来启动并挂钩游戏进程，因此在此覆盖层加载期间，此函数将初始返回 false。</para> <para></para>

**返回值:** `bool`

**用法示例:**
```csharp
bool overlayEnabled = SteamGameServerUtils.IsOverlayEnabled();
```

### BOverlayNeedsPresent (静态)

```csharp
bool BOverlayNeedsPresent()
```

<para> 通常，如果你的游戏有一个持续运行的帧循环，该循环每帧都会调用 D3D Present API 或 OGL SwapBuffers API，那么这个调用是不需要的。</para> <para> 但是，如果你的游戏仅在事件驱动的基础上刷新屏幕，这可能会破坏覆盖层，因为它使用你的 Present/SwapBuffers 调用来驱动其内部帧循环，并且它也可能需要在发生需要通知的事件时或当用户将覆盖层置于游戏之上时，随时向屏幕 Present()。在这种情况下，你可以使用此 API 来询问覆盖层是否当前需要一次 Present，然后你可以定期（大约 33Hz 是理想的）检查这一点，并确保你使用 Present 或 SwapBuffers 刷新屏幕，以允许覆盖层完成其工作。</para>

**返回值:** `bool`

**用法示例:**
```csharp
if (SteamGameServerUtils.BOverlayNeedsPresent()) { /* 调用 Present 或 SwapBuffers */ }
```

### CheckFileSignature (静态)

```csharp
SteamAPICall_t CheckFileSignature(string szFileName)
```

<para> 异步调用，用于检查可执行文件是否使用合作伙伴网站签名选项卡上设置的公钥进行了签名，例如以拒绝加载已修改的可执行文件。</para> <para> 结果通过 CheckFileSignature_t 返回。</para> <para> k_ECheckFileSignatureNoSignaturesFoundForThisApp - 此应用程序未在合作伙伴网站的签名选项卡上进行配置以启用此功能。</para> <para> k_ECheckFileSignatureNoSignaturesFoundForThisFile - 此文件未在合作伙伴网站的签名选项卡上列出。</para> <para> k_ECheckFileSignatureFileNotFound - 该文件在磁盘上不存在。</para> <para> k_ECheckFileSignatureInvalidSignature - 文件存在，并且已为该文件设置了签名选项卡，但文件要么未签名，要么签名不匹配。</para> <para> k_ECheckFileSignatureValidSignature - 文件已签名且签名有效。</para>

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

<para> 激活全屏文本输入对话框，该对话框接收一个初始文本字符串，并返回用户输入的文本</para>

**参数:**

- `eInputMode` (`EGamepadTextInputMode`)
- `eLineInputMode` (`EGamepadTextInputLineMode`)
- `pchDescription` (`string`)
- `unCharMax` (`uint`)
- `pchExistingText` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = SteamGameServerUtils.ShowGamepadTextInput(EGamepadTextInputMode.k_EGamepadTextInputModeNormal, EGamepadTextInputLineMode.k_EGamepadTextInputLineModeSingleLine, "Enter your name:", 32, "");
```

### GetEnteredGamepadTextLength (静态)

```csharp
uint GetEnteredGamepadTextLength()
```

<para> 返回先前输入的文本及其长度</para>

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
SteamGameServerUtils.GetEnteredGamepadTextInput(out text, 256);
```

### GetSteamUILanguage (静态)

```csharp
string GetSteamUILanguage()
```

<para> 返回 Steam 客户端正在运行的语言，你可能更想要使用 ISteamApps::GetCurrentGameLanguage，此函数用于非常特殊的用例场景。</para>

**返回值:** `string`

**用法示例:**
```csharp
string lang = SteamGameServerUtils.GetSteamUILanguage();
```

### IsSteamRunningInVR (静态)

```csharp
bool IsSteamRunningInVR()
```

<para> 如果 Steam 本身正在 VR 模式下运行，则返回 true</para>

**返回值:** `bool`

**用法示例:**
```csharp
bool isVrMode = SteamGameServerUtils.IsSteamRunningInVR();
```

### SetOverlayNotificationInset (静态)

```csharp
void SetOverlayNotificationInset(int nHorizontalInset, int nVerticalInset)
```

<para>设置叠加通知相对于 SetOverlayNotificationPosition 指定的角的偏移量。</para>

**参数:**

- `nHorizontalInset` (`int`)
- `nVerticalInset` (`int`)

**用法示例:**
```csharp
SteamGameServerUtils.SetOverlayNotificationInset(10, 20);
```

### IsSteamInBigPictureMode (静态)

```csharp
bool IsSteamInBigPictureMode()
```

<para>如果 Steam 和 Steam 覆盖层正在以大屏幕模式运行，则返回 true。</para> <para>游戏必须通过 Steam 客户端启动，才能启用大屏幕覆盖层。在开发期间，</para> <para>可以将游戏作为非 Steam 游戏添加到开发者的库中以测试此功能。</para>

**返回值:** `bool`

**用法示例:**
```csharp
if (SteamGameServerUtils.IsSteamInBigPictureMode())
{
    // 处理大屏幕模式逻辑
}
```

### StartVRDashboard (静态)

```csharp
void StartVRDashboard()
```

<para> 请求 SteamUI 创建并渲染其 OpenVR 仪表盘 </para>

**用法示例:**
```csharp
SteamGameServerUtils.StartVRDashboard();
```

### IsVRHeadsetStreamingEnabled (静态)

```csharp
bool IsVRHeadsetStreamingEnabled()
```

<para>如果 HMD 内容将通过 Steam 远程播放进行流式传输，则返回 true</para>

**返回值:** `bool`

**用法示例:**
```csharp
bool isStreaming = SteamGameServerUtils.IsVRHeadsetStreamingEnabled();
```

### SetVRHeadsetStreamingEnabled (静态)

```csharp
void SetVRHeadsetStreamingEnabled(bool bEnabled)
```

<para> 设置是否通过 Steam 远程播放功能来流式传输 HMD 内容。</para> <para> 如果设置为 true，则将流式传输 HMD 头显中的场景，并且不允许远程输入。</para> <para> 如果设置为 false，则将流式传输应用程序窗口，并且允许远程输入。</para> <para> 默认值为 true，除非游戏在扩展的 appinfo 中包含 "VRHeadsetStreaming" "0"。</para> <para> （这对于具有非对称多人游戏玩法的游戏很有用）</para>

**参数:**

- `bEnabled` (`bool`)

**用法示例:**
```csharp
SteamGameServerUtils.SetVRHeadheadsetStreamingEnabled(true);
```

### IsSteamChinaLauncher (静态)

```csharp
bool IsSteamChinaLauncher()
```

<para> 返回此 Steam 客户端是否为 Steam 中国专用客户端，而非全球客户端。</para>

**返回值:** `bool`

**用法示例:**
```csharp
bool isChina = SteamGameServerUtils.IsSteamChinaLauncher();
```

### InitFilterText (静态)

```csharp
bool InitFilterText(uint unFilterOptions = 0)
```

<para>初始化文本过滤，为游戏运行的语言加载字典。</para> <para>unFilterOptions 预留用于未来功能，应将其设置为 0。</para> <para>如果游戏语言不支持过滤，则返回 false，此时 FilterText() 将作为直通函数。</para> <para>用户可以在其 Steam 账户设置中自定义文本过滤行为：</para> <para>https://store.steampowered.com/account/preferences#CommunityContentPreferences</para>

**参数:**

- `unFilterOptions` (`uint`) = `0`

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUtils.InitFilterText(0u);
```

### FilterText (静态)

```csharp
int FilterText(ETextFilteringContext eContext, CSteamID sourceSteamID, string pchInputMessage, out string pchOutFilteredText, uint nByteSizeOutFilteredText)
```

<para> 对提供的输入消息进行过滤，并将过滤后的结果放入 pchOutFilteredText 中，使用法律要求的过滤以及基于上下文和用户设置的额外过滤</para> <para> eContext 是输入字符串中内容的类型</para> <para> sourceSteamID 是输入字符串来源的 Steam ID（例如，拥有该名称的玩家，或说出聊天文本的人）</para> <para> pchInputText 是应被过滤的输入字符串，可以是 ASCII 或 UTF-8</para> <para> pchOutFilteredText 是输出将被放置的位置，即使未执行任何过滤</para> <para> nByteSizeOutFilteredText 是 pchOutFilteredText 的大小（以字节为单位），应至少为 strlen(pchInputText)+1</para> <para> 返回被过滤的字符数（而非字节数）</para>

**参数:**

- `eContext` (`ETextFilteringContext`)
- `sourceSteamID` (`CSteamID`)
- `pchInputMessage` (`string`)
- `pchOutFilteredText` (`out string`)
- `nByteSizeOutFilteredText` (`uint`)

**返回值:** `int`

**用法示例:**
```csharp
string filteredText = "";
int result = SteamGameServerUtils.FilterText(ETextFilteringContext.Chat, new CSteamID(123456789), "Hello @#$%^&*", out filteredText, (uint)(filteredText.Length + 1));
```

### GetIPv6ConnectivityState (静态)

```csharp
ESteamIPv6ConnectivityState GetIPv6ConnectivityState(ESteamIPv6ConnectivityProtocol eProtocol)
```

<para> 返回我们认为您在指定协议上，对“互联网”的当前 IPv6 连接状态。</para> <para> 这并不会告知您 Steam 客户端当前是否通过 IPv6 连接到 Steam。</para>

**参数:**

- `eProtocol` (`ESteamIPv6ConnectivityProtocol`)

**返回值:** `ESteamIPv6ConnectivityState`

**用法示例:**
```csharp
ESteamIPv6ConnectivityState state = SteamGameServerUtils.GetIPv6ConnectivityState(ESteamIPv6ConnectivityProtocol.TCP);
```

### IsSteamRunningOnSteamDeck (静态)

```csharp
bool IsSteamRunningOnSteamDeck()
```

<para> 如果当前正在 Steam Deck 设备上运行，则返回 true </para>

**返回值:** `bool`

**用法示例:**
```csharp
bool isDeck = SteamGameServerUtils.IsSteamRunningOnSteamDeck();
```

### ShowFloatingGamepadTextInput (静态)

```csharp
bool ShowFloatingGamepadTextInput(EFloatingGamepadTextInputMode eKeyboardMode, int nTextFieldXPosition, int nTextFieldYPosition, int nTextFieldWidth, int nTextFieldHeight)
```

<para>在游戏内容上方打开一个浮动键盘，并将操作系统键盘按键直接发送给游戏。</para> <para>文本字段的位置以像素为单位，相对于游戏窗口的原点进行指定，用于将浮动键盘定位在不会遮挡文本字段的位置。</para>

**参数:**

- `eKeyboardMode` (`EFloatingGamepadTextInputMode`)
- `nTextFieldXPosition` (`int`)
- `nTextFieldYPosition` (`int`)
- `nTextFieldWidth` (`int`)
- `nTextFieldHeight` (`int`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUtils.ShowFloatingGamepadTextInput(EFloatingGamepadTextInputMode.Value, 100, 200, 300, 50);
```

### SetGameLauncherMode (静态)

```csharp
void SetGameLauncherMode(bool bLauncherMode)
```

在那些不支持手柄的游戏启动器中，你可以调用此方法，让 Steam Input 将手柄输入转换为鼠标/键盘输入，以导航启动器。

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

<para> 关闭浮动键盘。</para>

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUtils.DismissFloatingGamepadTextInput();
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

