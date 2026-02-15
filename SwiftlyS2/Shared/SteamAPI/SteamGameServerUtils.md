# 📦 SteamGameServerUtils

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### GetSecondsSinceAppActive (静态)

```csharp
uint GetSecondsSinceAppActive()
```

<para> return the number of seconds since the user</para>

**返回值:** `uint`

### GetSecondsSinceComputerActive (静态)

```csharp
uint GetSecondsSinceComputerActive()
```

**返回值:** `uint`

### GetConnectedUniverse (静态)

```csharp
EUniverse GetConnectedUniverse()
```

<para> the universe this client is connecting to</para>

**返回值:** `EUniverse`

### GetServerRealTime (静态)

```csharp
uint GetServerRealTime()
```

<para> Steam server time. Number of seconds since January 1, 1970, GMT (i.e unix time)</para>

**返回值:** `uint`

### GetIPCountry (静态)

```csharp
string GetIPCountry()
```

<para> returns the 2 digit ISO 3166-1-alpha-2 format country code this client is running in (as looked up via an IP-to-location database)</para> <para> e.g "US" or "UK".</para>

**返回值:** `string`

### GetImageSize (静态)

```csharp
bool GetImageSize(int iImage, out uint pnWidth, out uint pnHeight)
```

<para> returns true if the image exists, and valid sizes were filled out</para>

**参数:**

- `iImage` (`int`)
- `pnWidth` (`out uint`)
- `pnHeight` (`out uint`)

**返回值:** `bool`

### GetImageRGBA (静态)

```csharp
bool GetImageRGBA(int iImage, byte[] pubDest, int nDestBufferSize)
```

<para> returns true if the image exists, and the buffer was successfully filled out</para> <para> results are returned in RGBA format</para> <para> the destination buffer size should be 4 * height * width * sizeof(char)</para>

**参数:**

- `iImage` (`int`)
- `pubDest` (`byte[]`)
- `nDestBufferSize` (`int`)

**返回值:** `bool`

### GetCurrentBatteryPower (静态)

```csharp
byte GetCurrentBatteryPower()
```

<para> return the amount of battery power left in the current system in % [0..100], 255 for being on AC power</para>

**返回值:** `byte`

### GetAppID (静态)

```csharp
AppId_t GetAppID()
```

<para> returns the appID of the current process</para>

**返回值:** `AppId_t`

### SetOverlayNotificationPosition (静态)

```csharp
void SetOverlayNotificationPosition(ENotificationPosition eNotificationPosition)
```

<para> Sets the position where the overlay instance for the currently calling game should show notifications.</para> <para> This position is per-game and if this function is called from outside of a game context it will do nothing.</para>

**参数:**

- `eNotificationPosition` (`ENotificationPosition`)

### IsAPICallCompleted (静态)

```csharp
bool IsAPICallCompleted(SteamAPICall_t hSteamAPICall, out bool pbFailed)
```

<para> API asynchronous call results</para> <para> can be used directly, but more commonly used via the callback dispatch API (see steam_api.h)</para>

**参数:**

- `hSteamAPICall` (`SteamAPICall_t`)
- `pbFailed` (`out bool`)

**返回值:** `bool`

### GetAPICallFailureReason (静态)

```csharp
ESteamAPICallFailure GetAPICallFailureReason(SteamAPICall_t hSteamAPICall)
```

**参数:**

- `hSteamAPICall` (`SteamAPICall_t`)

**返回值:** `ESteamAPICallFailure`

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

### GetIPCCallCount (静态)

```csharp
uint GetIPCCallCount()
```

<para> returns the number of IPC calls made since the last time this function was called</para> <para> Used for perf debugging so you can understand how many IPC calls your game makes per frame</para> <para> Every IPC call is at minimum a thread context switch if not a process one so you want to rate</para> <para> control how often you do them.</para>

**返回值:** `uint`

### SetWarningMessageHook (静态)

```csharp
void SetWarningMessageHook(SteamAPIWarningMessageHook_t pFunction)
```

<para> API warning handling</para> <para> 'int' is the severity; 0 for msg, 1 for warning</para> <para> 'const char *' is the text of the message</para> <para> callbacks will occur directly after the API function is called that generated the warning or message</para>

**参数:**

- `pFunction` (`SteamAPIWarningMessageHook_t`)

### IsOverlayEnabled (静态)

```csharp
bool IsOverlayEnabled()
```

<para> Returns true if the overlay is running &amp; the user can access it. The overlay process could take a few seconds to</para> <para> start &amp; hook the game process, so this function will initially return false while the overlay is loading.</para>

**返回值:** `bool`

### BOverlayNeedsPresent (静态)

```csharp
bool BOverlayNeedsPresent()
```

<para> Normally this call is unneeded if your game has a constantly running frame loop that calls the</para> <para> D3D Present API, or OGL SwapBuffers API every frame.</para> <para> However, if you have a game that only refreshes the screen on an event driven basis then that can break</para> <para> the overlay, as it uses your Present/SwapBuffers calls to drive it's internal frame loop and it may also</para> <para> need to Present() to the screen any time an even needing a notification happens or when the overlay is</para> <para> brought up over the game by a user. You can use this API to ask the overlay if it currently need a present</para> <para> in that case, and then you can check for this periodically (roughly 33hz is desirable) and make sure you</para> <para> refresh the screen with Present or SwapBuffers to allow the overlay to do it's work.</para>

**返回值:** `bool`

### CheckFileSignature (静态)

```csharp
SteamAPICall_t CheckFileSignature(string szFileName)
```

<para> Asynchronous call to check if an executable file has been signed using the public key set on the signing tab</para> <para> of the partner site, for example to refuse to load modified executable files.</para> <para> The result is returned in CheckFileSignature_t.</para> <para> k_ECheckFileSignatureNoSignaturesFoundForThisApp - This app has not been configured on the signing tab of the partner site to enable this function.</para> <para> k_ECheckFileSignatureNoSignaturesFoundForThisFile - This file is not listed on the signing tab for the partner site.</para> <para> k_ECheckFileSignatureFileNotFound - The file does not exist on disk.</para> <para> k_ECheckFileSignatureInvalidSignature - The file exists, and the signing tab has been set for this file, but the file is either not signed or the signature does not match.</para> <para> k_ECheckFileSignatureValidSignature - The file is signed and the signature is valid.</para>

**参数:**

- `szFileName` (`string`)

**返回值:** `SteamAPICall_t`

### ShowGamepadTextInput (静态)

```csharp
bool ShowGamepadTextInput(EGamepadTextInputMode eInputMode, EGamepadTextInputLineMode eLineInputMode, string pchDescription, uint unCharMax, string pchExistingText)
```

<para> Activates the full-screen text input dialog which takes a initial text string and returns the text the user has typed</para>

**参数:**

- `eInputMode` (`EGamepadTextInputMode`)
- `eLineInputMode` (`EGamepadTextInputLineMode`)
- `pchDescription` (`string`)
- `unCharMax` (`uint`)
- `pchExistingText` (`string`)

**返回值:** `bool`

### GetEnteredGamepadTextLength (静态)

```csharp
uint GetEnteredGamepadTextLength()
```

<para> Returns previously entered text &amp; length</para>

**返回值:** `uint`

### GetEnteredGamepadTextInput (静态)

```csharp
bool GetEnteredGamepadTextInput(out string pchText, uint cchText)
```

**参数:**

- `pchText` (`out string`)
- `cchText` (`uint`)

**返回值:** `bool`

### GetSteamUILanguage (静态)

```csharp
string GetSteamUILanguage()
```

<para> returns the language the steam client is running in, you probably want ISteamApps::GetCurrentGameLanguage instead, this is for very special usage cases</para>

**返回值:** `string`

### IsSteamRunningInVR (静态)

```csharp
bool IsSteamRunningInVR()
```

<para> returns true if Steam itself is running in VR mode</para>

**返回值:** `bool`

### SetOverlayNotificationInset (静态)

```csharp
void SetOverlayNotificationInset(int nHorizontalInset, int nVerticalInset)
```

<para> Sets the inset of the overlay notification from the corner specified by SetOverlayNotificationPosition.</para>

**参数:**

- `nHorizontalInset` (`int`)
- `nVerticalInset` (`int`)

### IsSteamInBigPictureMode (静态)

```csharp
bool IsSteamInBigPictureMode()
```

<para> returns true if Steam &amp; the Steam Overlay are running in Big Picture mode</para> <para> Games much be launched through the Steam client to enable the Big Picture overlay. During development,</para> <para> a game can be added as a non-steam game to the developers library to test this feature</para>

**返回值:** `bool`

### StartVRDashboard (静态)

```csharp
void StartVRDashboard()
```

<para> ask SteamUI to create and render its OpenVR dashboard</para>

### IsVRHeadsetStreamingEnabled (静态)

```csharp
bool IsVRHeadsetStreamingEnabled()
```

<para> Returns true if the HMD content will be streamed via Steam Remote Play</para>

**返回值:** `bool`

### SetVRHeadsetStreamingEnabled (静态)

```csharp
void SetVRHeadsetStreamingEnabled(bool bEnabled)
```

<para> Set whether the HMD content will be streamed via Steam Remote Play</para> <para> If this is set to true, then the scene in the HMD headset will be streamed, and remote input will not be allowed.</para> <para> If this is set to false, then the application window will be streamed instead, and remote input will be allowed.</para> <para> The default is true unless "VRHeadsetStreaming" "0" is in the extended appinfo for a game.</para> <para> (this is useful for games that have asymmetric multiplayer gameplay)</para>

**参数:**

- `bEnabled` (`bool`)

### IsSteamChinaLauncher (静态)

```csharp
bool IsSteamChinaLauncher()
```

<para> Returns whether this steam client is a Steam China specific client, vs the global client.</para>

**返回值:** `bool`

### InitFilterText (静态)

```csharp
bool InitFilterText(uint unFilterOptions = 0)
```

<para> Initializes text filtering, loading dictionaries for the language the game is running in.</para> <para> unFilterOptions are reserved for future use and should be set to 0</para> <para> Returns false if filtering is unavailable for the game's language, in which case FilterText() will act as a passthrough.</para> <para> Users can customize the text filter behavior in their Steam Account preferences:</para> <para> https://store.steampowered.com/account/preferences#CommunityContentPreferences</para>

**参数:**

- `unFilterOptions` (`uint`) = `0`

**返回值:** `bool`

### FilterText (静态)

```csharp
int FilterText(ETextFilteringContext eContext, CSteamID sourceSteamID, string pchInputMessage, out string pchOutFilteredText, uint nByteSizeOutFilteredText)
```

<para> Filters the provided input message and places the filtered result into pchOutFilteredText, using legally required filtering and additional filtering based on the context and user settings</para> <para> eContext is the type of content in the input string</para> <para> sourceSteamID is the Steam ID that is the source of the input string (e.g. the player with the name, or who said the chat text)</para> <para> pchInputText is the input string that should be filtered, which can be ASCII or UTF-8</para> <para> pchOutFilteredText is where the output will be placed, even if no filtering is performed</para> <para> nByteSizeOutFilteredText is the size (in bytes) of pchOutFilteredText, should be at least strlen(pchInputText)+1</para> <para> Returns the number of characters (not bytes) filtered</para>

**参数:**

- `eContext` (`ETextFilteringContext`)
- `sourceSteamID` (`CSteamID`)
- `pchInputMessage` (`string`)
- `pchOutFilteredText` (`out string`)
- `nByteSizeOutFilteredText` (`uint`)

**返回值:** `int`

### GetIPv6ConnectivityState (静态)

```csharp
ESteamIPv6ConnectivityState GetIPv6ConnectivityState(ESteamIPv6ConnectivityProtocol eProtocol)
```

<para> Return what we believe your current ipv6 connectivity to "the internet" is on the specified protocol.</para> <para> This does NOT tell you if the Steam client is currently connected to Steam via ipv6.</para>

**参数:**

- `eProtocol` (`ESteamIPv6ConnectivityProtocol`)

**返回值:** `ESteamIPv6ConnectivityState`

### IsSteamRunningOnSteamDeck (静态)

```csharp
bool IsSteamRunningOnSteamDeck()
```

<para> returns true if currently running on the Steam Deck device</para>

**返回值:** `bool`

### ShowFloatingGamepadTextInput (静态)

```csharp
bool ShowFloatingGamepadTextInput(EFloatingGamepadTextInputMode eKeyboardMode, int nTextFieldXPosition, int nTextFieldYPosition, int nTextFieldWidth, int nTextFieldHeight)
```

<para> Opens a floating keyboard over the game content and sends OS keyboard keys directly to the game.</para> <para> The text field position is specified in pixels relative the origin of the game window and is used to position the floating keyboard in a way that doesn't cover the text field</para>

**参数:**

- `eKeyboardMode` (`EFloatingGamepadTextInputMode`)
- `nTextFieldXPosition` (`int`)
- `nTextFieldYPosition` (`int`)
- `nTextFieldWidth` (`int`)
- `nTextFieldHeight` (`int`)

**返回值:** `bool`

### SetGameLauncherMode (静态)

```csharp
void SetGameLauncherMode(bool bLauncherMode)
```

<para> In game launchers that don't have controller support you can call this to have Steam Input translate the controller input into mouse/kb to navigate the launcher</para>

**参数:**

- `bLauncherMode` (`bool`)

### DismissFloatingGamepadTextInput (静态)

```csharp
bool DismissFloatingGamepadTextInput()
```

<para> Dismisses the floating keyboard.</para>

**返回值:** `bool`

### DismissGamepadTextInput (静态)

```csharp
bool DismissGamepadTextInput()
```

<para> Dismisses the full-screen text input dialog.</para>

**返回值:** `bool`

