<a id="steamgameserverclient"></a>

# 📦 SteamGameServerClient

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### CreateSteamPipe (静态)

```csharp
HSteamPipe CreateSteamPipe()
```

<para>创建一个通往 Steam 客户端的通信管道。</para><para>非线程安全——调用时请确保没有其他线程正在访问 Steamworks API。</para>

**返回值:** `HSteamPipe`

**用法示例:**
```csharp
HSteamPipe pipe = SteamGameServerClient.CreateSteamPipe();
```

### BReleaseSteamPipe (静态)

```csharp
bool BReleaseSteamPipe(HSteamPipe hSteamPipe)
```

释放之前创建的通信管道。  
非线程安全——调用时请确保没有其他线程正在访问 Steamworks API。

**参数:**

- `hSteamPipe` (`HSteamPipe`)

**返回值:** `bool`

**用法示例:**
```csharp
bool released = SteamGameServerClient.BReleaseSteamPipe(hSteamPipe);
```

### ConnectToGlobalUser (静态)

```csharp
HSteamUser ConnectToGlobalUser(HSteamPipe hSteamPipe)
```

连接到现有的全局用户，若不存在则失败。游戏用于与 SteamUI 进行协调。非线程安全——调用时请确保没有其他线程正在访问 Steamworks API。

**参数:**

- `hSteamPipe` (`HSteamPipe`)

**返回值:** `HSteamUser`

**用法示例:**
```csharp
var hSteamUser = SteamGameServerClient.ConnectToGlobalUser(hSteamPipe);
```

### CreateLocalUser (静态)

```csharp
HSteamUser CreateLocalUser(out HSteamPipe phSteamPipe, EAccountType eAccountType)
```

用于游戏服务器，创建一个不会与他人共享的 Steam 用户。  
非线程安全——调用时请确保没有其他线程正在访问 Steamworks API。

**参数:**

- `phSteamPipe` (`out HSteamPipe`)
- `eAccountType` (`EAccountType`)

**返回值:** `HSteamUser`

**用法示例:**
```csharp
HSteamPipe pipe;
HSteamUser user = SteamGameServerClient.CreateLocalUser(out pipe, EAccountType.GameServer);
```

### ReleaseUser (静态)

```csharp
void ReleaseUser(HSteamPipe hSteamPipe, HSteamUser hUser)
```

<para>移除已分配的用户</para> <para>非线程安全 - 调用时请确保没有其他线程正在访问 Steamworks API</para>

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

<para>检索与句柄关联的 ISteamUser 接口</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr steamUser = SteamGameServerClient.GetISteamUser(hSteamUser, hSteamPipe, "SteamUser021");
```

### GetISteamGameServer (静态)

```csharp
IntPtr GetISteamGameServer(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>检索与句柄关联的 ISteamGameServer 接口</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr server = SteamGameServerClient.GetISteamGameServer(hSteamUser, hSteamPipe, "SteamGameServer012");
```

### SetLocalIPBinding (静态)

```csharp
void SetLocalIPBinding(ref SteamIPAddress_t unIP, ushort usPort)
```

<para>设置要绑定的本地 IP 地址和端口</para> <para>必须在调用 CreateLocalUser() 之前进行设置</para>

**参数:**

- `unIP` (`ref SteamIPAddress_t`)
- `usPort` (`ushort`)

**用法示例:**
```csharp
SteamIPAddress_t ip = default;
SteamGameServerClient.SetLocalIPBinding(ref ip, 27015);
```

### GetISteamFriends (静态)

```csharp
IntPtr GetISteamFriends(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>返回 ISteamFriends 接口</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr friends = SteamGameServerClient.GetISteamFriends(hSteamUser, hSteamPipe, "SteamFriends015");
```

### GetISteamUtils (静态)

```csharp
IntPtr GetISteamUtils(HSteamPipe hSteamPipe, string pchVersion)
```

返回 ISteamUtils 接口

**参数:**

- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr utils = SteamGameServerClient.GetISteamUtils(hSteamPipe, "SteamUtils009");
```

### GetISteamMatchmaking (静态)

```csharp
IntPtr GetISteamMatchmaking(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>返回 ISteamMatchmaking 接口</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr matchmaking = SteamGameServerClient.GetISteamMatchmaking(hSteamUser, hSteamPipe, "SteamMatchmaking009");
```

### GetISteamMatchmakingServers (静态)

```csharp
IntPtr GetISteamMatchmakingServers(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>返回 ISteamMatchmakingServers 接口</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr matchmakingServers = SteamGameServerClient.GetISteamMatchmakingServers(hSteamUser, hSteamPipe, "SteamMatchmakingServers001");
```

### GetISteamGenericInterface (静态)

```csharp
IntPtr GetISteamGenericInterface(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

返回一个通用接口

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr genericInterface = SteamGameServerClient.GetISteamGenericInterface(hSteamUser, hSteamPipe, "SteamGameServer012");
```

### GetISteamUserStats (静态)

```csharp
IntPtr GetISteamUserStats(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>返回 ISteamUserStats 接口</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr userStats = SteamGameServerClient.GetISteamUserStats(hSteamUser, hSteamPipe, "STEAMUSERSTATS_INTERFACE_VERSION001");
```

### GetISteamGameServerStats (静态)

```csharp
IntPtr GetISteamGameServerStats(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

返回 ISteamGameServerStats 接口

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr statsPtr = SteamGameServerClient.GetISteamGameServerStats(hSteamUser, hSteamPipe, "STEAMGAMESERVERSTATS_INTERFACE_VERSION001");
```

### GetISteamApps (静态)

```csharp
IntPtr GetISteamApps(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>返回应用接口</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr appsPtr = SteamGameServerClient.GetISteamApps(hSteamUser, hSteamPipe, "STEAMAPPS_INTERFACE_VERSION001");
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
IntPtr networking = SteamGameServerClient.GetISteamNetworking(user, pipe, "SteamNetworking001");
```

### GetISteamRemoteStorage (静态)

```csharp
IntPtr GetISteamRemoteStorage(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>远程存储</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
var remoteStoragePtr = SteamGameServerClient.GetISteamRemoteStorage(hSteamUser, hSteamPipe, "STEAMREMOTESTORAGE_INTERFACE_VERSION001");
```

### GetISteamScreenshots (静态)

```csharp
IntPtr GetISteamScreenshots(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>用户截图</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr screenshots = SteamGameServerClient.GetISteamScreenshots(hSteamuser, hSteamPipe, "STEAMSCREENSHOTS_INTERFACE_VERSION001");
```

### GetISteamGameSearch (静态)

```csharp
IntPtr GetISteamGameSearch(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 游戏搜索</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr gameSearch = SteamGameServerClient.GetISteamGameSearch(hSteamUser, hSteamPipe, "SteamGameSearch001");
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
uint ipcCount = SteamGameServerClient.GetIPCCallCount();
Console.WriteLine(ipcCount);
```

### SetWarningMessageHook (静态)

```csharp
void SetWarningMessageHook(SteamAPIWarningMessageHook_t pFunction)
```

<para>API 警告处理</para> <para>'int' 表示严重程度；0 代表消息，1 代表警告</para> <para>'const char *' 为消息文本</para> <para>回调将在生成该警告或消息的 API 函数调用后直接发生。</para>

**参数:**

- `pFunction` (`SteamAPIWarningMessageHook_t`)

**用法示例:**
```csharp
SteamGameServerClient.SetWarningMessageHook((severity, msg) => Console.WriteLine($"[{severity}] {msg}"));
```

### BShutdownIfAllPipesClosed (静态)

```csharp
bool BShutdownIfAllPipesClosed()
```

触发 DLL 的全局关闭

**返回值:** `bool`

**用法示例:**
```csharp
bool closed = SteamGameServerClient.BShutdownIfAllPipesClosed();
Console.WriteLine(closed);
```

### GetISteamHTTP (静态)

```csharp
IntPtr GetISteamHTTP(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>暴露 HTTP 接口</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr http = SteamGameServerClient.GetISteamHTTP(hSteamUser, hSteamPipe, "STEAMHTTP_INTERFACE_VERSION001");
```

### GetISteamController (静态)

```csharp
IntPtr GetISteamController(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>暴露 ISteamController 接口——该接口已被弃用，现推荐使用 Steam Input</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr controller = SteamGameServerClient.GetISteamController(hSteamUser, hSteamPipe, "SteamController001");
```

### GetISteamUGC (静态)

```csharp
IntPtr GetISteamUGC(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>暴露 ISteamUGC 接口</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr ugc = SteamGameServerClient.GetISteamUGC(hSteamUser, hSteamPipe, "STEAMUGC_INTERFACE_VERSION014");
```

### GetISteamMusic (静态)

```csharp
IntPtr GetISteamMusic(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>音乐播放器</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr music = SteamGameServerClient.GetISteamMusic(hSteamUser, hSteamPipe, "SteamMusic001");
```

### GetISteamMusicRemote (静态)

```csharp
IntPtr GetISteamMusicRemote(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

音乐播放器远程控制器

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr musicRemote = SteamGameServerClient.GetISteamMusicRemote(hSteamuser, hSteamPipe, "STEAMMUSICREMOTE_INTERFACE_VERSION001");
```

### GetISteamHTMLSurface (静态)

```csharp
IntPtr GetISteamHTMLSurface(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>HTML 页面显示</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr htmlSurface = SteamGameServerClient.GetISteamHTMLSurface(hSteamUser, hSteamPipe, "SteamHTMLSurface001");
```

### GetISteamInventory (静态)

```csharp
IntPtr GetISteamInventory(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 背包</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr inventory = SteamGameServerClient.GetISteamInventory(hSteamUser, hSteamPipe, "STEAMINVENTORY_INTERFACE_V001");
```

### GetISteamVideo (静态)

```csharp
IntPtr GetISteamVideo(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>视频</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr videoPtr = SteamGameServerClient.GetISteamVideo(hSteamUser, hSteamPipe, "SteamVideo001");
```

### GetISteamParentalSettings (静态)

```csharp
IntPtr GetISteamParentalSettings(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>家长控制</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr parentalSettings = SteamGameServerClient.GetISteamParentalSettings(hSteamUser, hSteamPipe, "SteamGameServerClient001");
```

### GetISteamInput (静态)

```csharp
IntPtr GetISteamInput(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>暴露 Steam Input 接口以支持手柄控制</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr inputPtr = SteamGameServerClient.GetISteamInput(hSteamUser, hSteamPipe, "SteamInput001");
```

### GetISteamParties (静态)

```csharp
IntPtr GetISteamParties(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>Steam 派对接口</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr steamParties = SteamGameServerClient.GetISteamParties(hSteamUser, hSteamPipe, "STEAMPARTIES_INTERFACE_VERSION");
```

### GetISteamRemotePlay (静态)

```csharp
IntPtr GetISteamRemotePlay(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>Steam远程游玩接口</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr remotePlay = SteamGameServerClient.GetISteamRemotePlay((HSteamUser)0, (HSteamPipe)0, "SteamRemotePlay001");
```

