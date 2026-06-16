<a id="steamgameserverclient"></a>

# 📦 SteamGameServerClient

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### CreateSteamPipe (静态)

```csharp
HSteamPipe CreateSteamPipe()
```

<para> 创建与Steam客户端的通信管道。</para> <para> 非线程安全 - 调用时请确保没有其他线程正在访问Steamworks API</para>

**返回值:** `HSteamPipe`

**用法示例:**
```csharp
HSteamPipe pipe = SteamGameServerClient.CreateSteamPipe();
```

### BReleaseSteamPipe (静态)

```csharp
bool BReleaseSteamPipe(HSteamPipe hSteamPipe)
```

<para> 释放先前创建的通信管道</para>
<para> 非线程安全 - 调用时请确保没有其他线程正在访问Steamworks API</para>

**参数:**

- `hSteamPipe` (`HSteamPipe`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = SteamGameServerClient.BReleaseSteamPipe(hSteamPipe);
```

### ConnectToGlobalUser (静态)

```csharp
HSteamUser ConnectToGlobalUser(HSteamPipe hSteamPipe)
```

<para> 连接到现有全局用户，若不存在则失败</para>
<para> 游戏用于与SteamUI协调</para>
<para> 非线程安全 - 调用时需确保没有其他线程正在访问Steamworks API</para>

**参数:**

- `hSteamPipe` (`HSteamPipe`)

**返回值:** `HSteamUser`

**用法示例:**
```csharp
HSteamPipe pipe = SteamAPI.GetHSteamPipe();
HSteamUser user = SteamGameServerClient.ConnectToGlobalUser(pipe);
```

### CreateLocalUser (静态)

```csharp
HSteamUser CreateLocalUser(out HSteamPipe phSteamPipe, EAccountType eAccountType)
```

<para> 由游戏服务器使用，创建一个不会与任何其他人共享的Steam用户</para> <para> 非线程安全 - 调用时确保没有其他线程正在访问Steamworks API</para>

**参数:**

- `phSteamPipe` (`out HSteamPipe`)
- `eAccountType` (`EAccountType`)

**返回值:** `HSteamUser`

**用法示例:**
```csharp
HSteamPipe pipe;
var user = SteamGameServerClient.CreateLocalUser(out pipe, EAccountType.Individual);
```

### ReleaseUser (静态)

```csharp
void ReleaseUser(HSteamPipe hSteamPipe, HSteamUser hUser)
```

<para> 移除已分配的用户</para> <para> 非线程安全 - 调用时确保没有其他线程在访问Steamworks API</para>

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
IntPtr steamUserInterface = SteamGameServerClient.GetISteamUser(HSteamUser.Default, HSteamPipe.Default, "SteamUser021");
```

### GetISteamGameServer (静态)

```csharp
IntPtr GetISteamGameServer(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 获取与该句柄关联的 ISteamGameServer 接口 </para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr serverInterface = SteamGameServerClient.GetISteamGameServer(HSteamUser.Null, HSteamPipe.Null, "SteamGameServer013");
```

### SetLocalIPBinding (静态)

```csharp
void SetLocalIPBinding(ref SteamIPAddress_t unIP, ushort usPort)
```

<para> 设置要绑定的本地IP和端口</para> <para> 必须在CreateLocalUser()之前设置此项</para>

**参数:**

- `unIP` (`ref SteamIPAddress_t`)
- `usPort` (`ushort`)

**用法示例:**
```csharp
var ip = SteamIPAddress_t.Parse("0.0.0.0");
SteamGameServerClient.SetLocalIPBinding(ref ip, 27015);
```

### GetISteamFriends (静态)

```csharp
IntPtr GetISteamFriends(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>返回ISteamFriends接口</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr friendsInterface = SteamGameServerClient.GetISteamFriends(HSteamUser.Invalid, HSteamPipe.Invalid, "SteamFriends015");
```

### GetISteamUtils (静态)

```csharp
IntPtr GetISteamUtils(HSteamPipe hSteamPipe, string pchVersion)
```

<para>返回ISteamUtils接口</para>

**参数:**

- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr utilsInterface = SteamGameServerClient.GetISteamUtils(0, "SteamUtils005");
```

### GetISteamMatchmaking (静态)

```csharp
IntPtr GetISteamMatchmaking(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>返回ISteamMatchmaking接口</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr matchmakingInterface = SteamGameServerClient.GetISteamMatchmaking(HSteamUser.Nil, HSteamPipe.Nil, "SteamMatchMaking002");
```

### GetISteamMatchmakingServers (静态)

```csharp
IntPtr GetISteamMatchmakingServers(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>返回ISteamMatchmakingServers接口</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr interfacePtr = SteamGameServerClient.GetISteamMatchmakingServers(hSteamUser, hSteamPipe, "SteamMatchMakingServers002");
```

### GetISteamGenericInterface (静态)

```csharp
IntPtr GetISteamGenericInterface(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 返回一个通用接口</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr interfacePtr = SteamGameServerClient.GetISteamGenericInterface(hSteamUser, hSteamPipe, "SteamGameServer012");
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
IntPtr statsInterface = SteamGameServerClient.GetISteamUserStats(HSteamUser.Invalid, HSteamPipe.Invalid, "STEAMUSERSTATS_INTERFACE_VERSION012");
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
IntPtr statsInterface = SteamGameServerClient.GetISteamGameServerStats(hSteamUser, hSteamPipe, "STEAMGAMESERVERSTATS_INTERFACE_VERSION001");
```

### GetISteamApps (静态)

```csharp
IntPtr GetISteamApps(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>返回应用程序接口</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr appsInterface = SteamGameServerClient.GetISteamApps(HSteamUser.Default, HSteamPipe.Default, "STEAMAPPS_INTERFACE_VERSION008");
```

### GetISteamNetworking (静态)

```csharp
IntPtr GetISteamNetworking(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>网络通信</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr networking = SteamGameServerClient.GetISteamNetworking(HSteamUser.Nil, HSteamPipe.Nil, "SteamNetworking001");
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
IntPtr remoteStorage = SteamGameServerClient.GetISteamRemoteStorage(hSteamUser, hSteamPipe, "STEAMREMOTESTORAGE_INTERFACE_VERSION014");
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
var hUser = HSteamUser.Invalid; var hPipe = HSteamPipe.Invalid; IntPtr ptr = SteamGameServerClient.GetISteamScreenshots(hUser, hPipe, "STEAMSCREENSHOTS_INTERFACE_VERSION003");
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
var hUser = HSteamUser.Invalid; var hPipe = HSteamPipe.Invalid; IntPtr searchInterface = SteamGameServerClient.GetISteamGameSearch(hUser, hPipe, "STEAMGAMESEARCH_INTERFACE_VERSION001");
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
uint ipcCalls = SteamGameServerClient.GetIPCCallCount();
```

### SetWarningMessageHook (静态)

```csharp
void SetWarningMessageHook(SteamAPIWarningMessageHook_t pFunction)
```

<para> API 警告处理</para>  
<para> 'int' 表示严重性；0 表示消息，1 表示警告</para>  
<para> 'const char *' 是消息的文本内容</para>  
<para> 回调将在生成警告或消息的 API 函数被调用后立即发生。</para>

**参数:**

- `pFunction` (`SteamAPIWarningMessageHook_t`)

**用法示例:**
```csharp
SteamGameServerClient.SetWarningMessageHook((severity, message) => System.Console.WriteLine($"[{severity}] {message}"));
```

### BShutdownIfAllPipesClosed (静态)

```csharp
bool BShutdownIfAllPipesClosed()
```

<para> 触发该DLL的全局关闭</para>

**返回值:** `bool`

**用法示例:**
```csharp
bool shouldShutdown = SteamGameServerClient.BShutdownIfAllPipesClosed();
```

### GetISteamHTTP (静态)

```csharp
IntPtr GetISteamHTTP(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 公开HTTP接口</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
var httpInterface = SteamGameServerClient.GetISteamHTTP(HSteamUser.Invalid, HSteamPipe.Invalid, "STEAMHTTP_INTERFACE_VERSION002");
```

### GetISteamController (静态)

```csharp
IntPtr GetISteamController(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 公开 ISteamController 接口 - 已弃用，建议使用 Steam Input</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr controllerInterface = SteamGameServerClient.GetISteamController(HSteamUser.Invalid, HSteamPipe.Invalid, "SteamController008");
```

### GetISteamUGC (静态)

```csharp
IntPtr GetISteamUGC(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 公开 ISteamUGC 接口</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr ugcInterface = SteamGameServerClient.GetISteamUGC(HSteamUser.Invalid, HSteamPipe.Invalid, "SteamUGC009");
```

### GetISteamMusic (静态)

```csharp
IntPtr GetISteamMusic(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 音乐播放器</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
var musicInterface = SteamGameServerClient.GetISteamMusic(HSteamUser.Invalid, HSteamPipe.Invalid, "STEAMMUSIC_INTERFACE_VERSION001");
```

### GetISteamMusicRemote (静态)

```csharp
IntPtr GetISteamMusicRemote(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>音乐播放器远程控制</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr remote = SteamGameServerClient.GetISteamMusicRemote(HSteamUser.Invalid, HSteamPipe.Invalid, "V001");
```

### GetISteamHTMLSurface (静态)

```csharp
IntPtr GetISteamHTMLSurface(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 网页页面显示</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr surface = SteamGameServerClient.GetISteamHTMLSurface(HSteamUser.Default, HSteamPipe.Default, "STEAMHTMLSURFACE_INTERFACE_VERSION_005");
```

### GetISteamInventory (静态)

```csharp
IntPtr GetISteamInventory(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para>库存</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr inventoryInterface = SteamGameServerClient.GetISteamInventory(HSteamUser.Default, HSteamPipe.Default, "STEAMINVENTORY_INTERFACE_V003");
```

### GetISteamVideo (静态)

```csharp
IntPtr GetISteamVideo(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 视频 </para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr videoInterface = SteamGameServerClient.GetISteamVideo(HSteamUser.Invalid, HSteamPipe.Invalid, "STEAMVIDEO_INTERFACE_V002");
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
IntPtr settingsPtr = SteamGameServerClient.GetISteamParentalSettings(HSteamUser.Current, HSteamPipe.Current, "STEAMPARENTALSETTINGS_INTERFACE_VERSION001");
```

### GetISteamInput (静态)

```csharp
IntPtr GetISteamInput(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> 暴露用于控制器支持的 Steam 输入接口</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
var inputInterface = SteamGameServerClient.GetISteamInput(HSteamUser.Nil, HSteamPipe.Nil, "SteamInput001");
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
var hUser = new HSteamUser(0);
var hPipe = new HSteamPipe(0);
var interfacePtr = SteamGameServerClient.GetISteamParties(hUser, hPipe, "STEAMPARTIES_INTERFACE_VERSION001");
```

### GetISteamRemotePlay (静态)

```csharp
IntPtr GetISteamRemotePlay(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> Steam远程同乐接口</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
IntPtr remotePlayInterface = SteamGameServerClient.GetISteamRemotePlay(HSteamUser.Invalid, HSteamPipe.Invalid, "STEAMREMOTEPLAY_INTERFACE_VERSION001");
```

