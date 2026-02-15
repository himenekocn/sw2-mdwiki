# 📦 SteamGameServerClient

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### CreateSteamPipe (静态)

```csharp
HSteamPipe CreateSteamPipe()
```

<para>创建与 Steam 客户端的通信管道。</para> <para>非线程安全 - 调用时请确保没有其他线程正在访问 Steamworks API。</para>

**返回值:** `HSteamPipe`

**用法示例:**
```csharp
HSteamPipe pipe = SteamGameServerClient.CreateSteamPipe();
```

### BReleaseSteamPipe (静态)

```csharp
bool BReleaseSteamPipe(HSteamPipe hSteamPipe)
```

<para> 释放先前创建的通信管道</para> <para> 非线程安全 - 调用时请确保没有其他线程正在访问 Steamworks API</para>

**参数:**

- `hSteamPipe` (`HSteamPipe`)

**返回值:** `bool`

**用法示例:**
```csharp
bool released = SteamGameServerClient.BReleaseSteamPipe(hSteamPipe);
if (released) { /* handle success */ }
```

### ConnectToGlobalUser (静态)

```csharp
HSteamUser ConnectToGlobalUser(HSteamPipe hSteamPipe)
```

<para>连接到一个已存在的全局用户，如果不存在则失败</para> <para>游戏用于与SteamUI进行协调</para> <para>非线程安全 - 调用时请确保没有其他线程正在访问Steamworks API</para>

**参数:**

- `hSteamPipe` (`HSteamPipe`)

**返回值:** `HSteamUser`

**用法示例:**
```csharp
HSteamPipe pipe = SteamGameServer.CreateSteamPipe();
HSteamUser user = SteamGameServerClient.ConnectToGlobalUser(pipe);
```

### CreateLocalUser (静态)

```csharp
HSteamUser CreateLocalUser(out HSteamPipe phSteamPipe, EAccountType eAccountType)
```

<para>供游戏服务器使用，创建一个不会与其他任何人共享的 Steam 用户</para> <para>非线程安全 - 调用时请确保没有其他线程正在访问 Steamworks API</para>

**参数:**

- `phSteamPipe` (`out HSteamPipe`)
- `eAccountType` (`EAccountType`)

**返回值:** `HSteamUser`

**用法示例:**
```csharp
HSteamPipe pipe;
HSteamUser user = SteamGameServerClient.CreateLocalUser(out pipe, EAccountType.Value);
```

### ReleaseUser (静态)

```csharp
void ReleaseUser(HSteamPipe hSteamPipe, HSteamUser hUser)
```

<para>移除一个已分配的用户</para> <para>非线程安全 - 调用时请确保没有其他线程正在访问 Steamworks API</para>

**参数:**

- `hSteamPipe` (`HSteamPipe`)
- `hUser` (`HSteamUser`)

**用法示例:**
```csharp
SteamGameServerClient.ReleaseUser(hSteamPipe, hUser);
```

### GetISteamUser (静态)

```csharp
IntPtr GetISteamUser(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>检索与该句柄关联的 ISteamUser 接口</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr pSteamUser = SteamGameServerClient.GetISteamUser(hSteamUser, hSteamPipe, "STEAM_USER_VERSION");
```

### GetISteamGameServer (静态)

```csharp
IntPtr GetISteamGameServer(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>检索与该句柄关联的 ISteamGameServer 接口</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr steamServer = SteamGameServerClient.GetISteamGameServer(hSteamUser, hSteamPipe, "STEAM_GAMESERVER_API_VERSION");
```

### SetLocalIPBinding (静态)

```csharp
void SetLocalIPBinding(ref SteamIPAddress_t unIP, ushort usPort)
```

<para>设置要绑定的本地IP和端口</para> <para>必须在调用CreateLocalUser()之前设置此属性</para>

**参数:**

- `unIP` (`ref SteamIPAddress_t`)
- `usPort` (`ushort`)

**用法示例:**
```csharp
SteamIPAddress_t ip = new SteamIPAddress_t { IPv4 = 0x7F000001 }; // 127.0.0.1
SteamGameServerClient.SetLocalIPBinding(ref ip, 27015);
```

### GetISteamFriends (静态)

```csharp
IntPtr GetISteamFriends(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 返回 ISteamFriends 接口</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr friendsPtr = SteamGameServerClient.GetISteamFriends(hSteamUser, hSteamPipe, "SteamFriends012");
```

### GetISteamUtils (静态)

```csharp
IntPtr GetISteamUtils(HSteamPipe hSteamPipe, string pchVersion)
```

<para> 返回 ISteamUtils 接口</para>

**参数:**

- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr utilsPtr = SteamGameServerClient.GetISteamUtils(hSteamPipe, "SteamUtils001");
```

### GetISteamMatchmaking (静态)

```csharp
IntPtr GetISteamMatchmaking(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 返回 ISteamMatchmaking 接口</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr matchMakingPtr = SteamGameServerClient.GetISteamMatchmaking(hSteamUser, hSteamPipe, "STEAM_MATCHMAKING_INTERFACE_VERSION_001");
if (matchMakingPtr != IntPtr.Zero) { /* 使用接口 */ }
```

### GetISteamMatchmakingServers (静态)

```csharp
IntPtr GetISteamMatchmakingServers(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 返回 ISteamMatchmakingServers 接口</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr serverInterface = SteamGameServerClient.GetISteamMatchmakingServers(hSteamUser, hSteamPipe, "STEAM_MATCHMAKING_V1");
```

### GetISteamGenericInterface (静态)

```csharp
IntPtr GetISteamGenericInterface(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 返回一个泛型接口 </para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr steamInterface = SteamGameServerClient.GetISteamGenericInterface(hSteamUser, hSteamPipe, "SteamGameServer012");
```

### GetISteamUserStats (静态)

```csharp
IntPtr GetISteamUserStats(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 返回 ISteamUserStats 接口</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr statsPtr = SteamGameServerClient.GetISteamUserStats(hSteamUser, hSteamPipe, "STEAM_USER_STATS_V001");
if (statsPtr != IntPtr.Zero) { /* 使用 statsPtr */ }
```

### GetISteamGameServerStats (静态)

```csharp
IntPtr GetISteamGameServerStats(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 返回 ISteamGameServerStats 接口</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr stats = SteamGameServerClient.GetISteamGameServerStats(hSteamUser, hSteamPipe, "STEAMGAMESERVERSTATS001");
if (stats != IntPtr.Zero)
{
    // 使用 stats 指针进行后续操作
}
```

### GetISteamApps (静态)

```csharp
IntPtr GetISteamApps(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 返回应用程序接口 </para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr appsInterface = SteamGameServerClient.GetISteamApps(hSteamUser, hSteamPipe, "STEAMAPPS_INTERFACE_VERSION001");
```

### GetISteamNetworking (静态)

```csharp
IntPtr GetISteamNetworking(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>网络</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr networkInterface = SteamGameServerClient.GetISteamNetworking(hSteamUser, hSteamPipe, "STEAM_GAME_SERVER_NETWORKING_VERSION_1");
```

### GetISteamRemoteStorage (静态)

```csharp
IntPtr GetISteamRemoteStorage(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 远程存储 </para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr storage = SteamGameServerClient.GetISteamRemoteStorage(hSteamUser, hSteamPipe, "STEAMREMOTESTORE_INTERFACE_VERSION001");
```

### GetISteamScreenshots (静态)

```csharp
IntPtr GetISteamScreenshots(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

用户截图

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr ptr = SteamGameServerClient.GetISteamScreenshots(hSteamUser, hSteamPipe, "STEAMSCREENSHOTS_INTERFACE_VERSION_1");
```

### GetISteamGameSearch (静态)

```csharp
IntPtr GetISteamGameSearch(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>游戏搜索</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr p = SteamGameServerClient.GetISteamGameSearch(hSteamUser, hSteamPipe, "SteamGameSearch001");
```

### GetIPCCallCount (静态)

```csharp
uint GetIPCCallCount()
```

<para>返回自上次调用此函数以来所进行的 IPC 调用次数。</para> <para>用于性能调试，以便了解您的游戏每帧执行多少次 IPC 调用。</para> <para>每次 IPC 调用至少会导致一次线程上下文切换，甚至可能是进程上下文切换，因此您需要控制执行它们的频率。</para>

**返回值:** `uint`

**用法示例:**
```csharp
uint calls = SteamGameServerClient.GetIPCCallCount();
```

### SetWarningMessageHook (静态)

```csharp
void SetWarningMessageHook(SteamAPIWarningMessageHook_t pFunction)
```

<para> API 警告处理</para> <para> 'int' 是严重级别；0 表示消息，1 表示警告</para> <para> 'const char *' 是消息的文本内容</para> <para> 回调函数将在生成警告或消息的 API 函数被调用后立即执行。</para>

**参数:**

- `pFunction` (`SteamAPIWarningMessageHook_t`)

**用法示例:**
```csharp
SteamGameServerClient.SetWarningMessageHook((severity, message) => Console.WriteLine($"[{severity}] {message}"));
```

### BShutdownIfAllPipesClosed (静态)

```csharp
bool BShutdownIfAllPipesClosed()
```

<para> 触发 DLL 的全局关闭</para>

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerClient.BShutdownIfAllPipesClosed();
```

### GetISteamHTTP (静态)

```csharp
IntPtr GetISteamHTTP(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 暴露 HTTP 接口 </para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr httpInterface = SteamGameServerClient.GetISteamHTTP(hSteamUser, hSteamPipe, "HTTP_002");
```

### GetISteamController (静态)

```csharp
IntPtr GetISteamController(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 暴露 ISteamController 接口 - 已弃用，推荐使用 Steam Input</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr controller = SteamGameServerClient.GetISteamController(0, 1, "STEAM_CONTROLLER_API_VERSION001");
```

### GetISteamUGC (静态)

```csharp
IntPtr GetISteamUGC(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 暴露 ISteamUGC 接口</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr pUGC = SteamGameServerClient.GetISteamUGC(hUser, hPipe, "STEAMUGC_INTERFACE_VERSION001");
```

### GetISteamMusic (静态)

```csharp
IntPtr GetISteamMusic(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 音乐播放器 </para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr musicInterface = SteamGameServerClient.GetISteamMusic(hSteamUser, hSteamPipe, "IVoiceUI_001");
```

### GetISteamMusicRemote (静态)

```csharp
IntPtr GetISteamMusicRemote(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 音乐播放器远程控制 </para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr musicRemote = SteamGameServerClient.GetISteamMusicRemote(hSteamUser, hSteamPipe, "IVersion_1");
```

### GetISteamHTMLSurface (静态)

```csharp
IntPtr GetISteamHTMLSurface(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> HTML 页面显示</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr surface = SteamGameServerClient.GetISteamHTMLSurface(hSteamUser, hSteamPipe, "1.0");
```

### GetISteamInventory (静态)

```csharp
IntPtr GetISteamInventory(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 库存 </para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr inventoryPtr = SteamGameServerClient.GetISteamInventory(hSteamUser, hSteamPipe, "STEAM_INVENTORY_API_V001");
if (inventoryPtr != IntPtr.Zero) { /* 使用 inventoryPtr */ }
```

### GetISteamVideo (静态)

```csharp
IntPtr GetISteamVideo(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 视频</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr video = SteamGameServerClient.GetISteamVideo(0, 0, "STEAM_GAMESERVER_VIDEO_INTERFACE");
Console.WriteLine(video);
```

### GetISteamParentalSettings (静态)

```csharp
IntPtr GetISteamParentalSettings(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 家长控制 </para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr ptr = SteamGameServerClient.GetISteamParentalSettings(hSteamUser, hSteamPipe, "parental_settings_v1");
```

### GetISteamInput (静态)

```csharp
IntPtr GetISteamInput(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 暴露 Steam Input 接口以支持控制器</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr inputPtr = SteamGameServerClient.GetISteamInput(hSteamUser, hSteamPipe, "STEAM_INPUT_INTERFACE_VERSION_001");
```

### GetISteamParties (静态)

```csharp
IntPtr GetISteamParties(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> Steam 聚会界面</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr partiesPtr = SteamGameServerClient.GetISteamParties(hSteamUser, hSteamPipe, "SteamParties001");
if (partiesPtr != IntPtr.Zero) { /* 使用 partiesPtr */ }
```

### GetISteamRemotePlay (静态)

```csharp
IntPtr GetISteamRemotePlay(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> Steam 远程游玩接口</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr remotePlay = SteamGameServerClient.GetISteamRemotePlay(0, 1, "STEAM_GAME_SERVER_REMOTE_PLAY_INTERFACE");
Console.WriteLine(remotePlay);
```

