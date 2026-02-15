# 📦 SteamGameServerClient

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### CreateSteamPipe (静态)

```csharp
HSteamPipe CreateSteamPipe()
```

<para> Creates a communication pipe to the Steam client.</para> <para> NOT THREADSAFE - ensure that no other threads are accessing Steamworks API when calling</para>

**返回值:** `HSteamPipe`

### BReleaseSteamPipe (静态)

```csharp
bool BReleaseSteamPipe(HSteamPipe hSteamPipe)
```

<para> Releases a previously created communications pipe</para> <para> NOT THREADSAFE - ensure that no other threads are accessing Steamworks API when calling</para>

**参数:**

- `hSteamPipe` (`HSteamPipe`)

**返回值:** `bool`

### ConnectToGlobalUser (静态)

```csharp
HSteamUser ConnectToGlobalUser(HSteamPipe hSteamPipe)
```

<para> connects to an existing global user, failing if none exists</para> <para> used by the game to coordinate with the steamUI</para> <para> NOT THREADSAFE - ensure that no other threads are accessing Steamworks API when calling</para>

**参数:**

- `hSteamPipe` (`HSteamPipe`)

**返回值:** `HSteamUser`

### CreateLocalUser (静态)

```csharp
HSteamUser CreateLocalUser(out HSteamPipe phSteamPipe, EAccountType eAccountType)
```

<para> used by game servers, create a steam user that won't be shared with anyone else</para> <para> NOT THREADSAFE - ensure that no other threads are accessing Steamworks API when calling</para>

**参数:**

- `phSteamPipe` (`out HSteamPipe`)
- `eAccountType` (`EAccountType`)

**返回值:** `HSteamUser`

### ReleaseUser (静态)

```csharp
void ReleaseUser(HSteamPipe hSteamPipe, HSteamUser hUser)
```

<para> removes an allocated user</para> <para> NOT THREADSAFE - ensure that no other threads are accessing Steamworks API when calling</para>

**参数:**

- `hSteamPipe` (`HSteamPipe`)
- `hUser` (`HSteamUser`)

### GetISteamUser (静态)

```csharp
IntPtr GetISteamUser(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> retrieves the ISteamUser interface associated with the handle</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

### GetISteamGameServer (静态)

```csharp
IntPtr GetISteamGameServer(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> retrieves the ISteamGameServer interface associated with the handle</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

### SetLocalIPBinding (静态)

```csharp
void SetLocalIPBinding(ref SteamIPAddress_t unIP, ushort usPort)
```

<para> set the local IP and Port to bind to</para> <para> this must be set before CreateLocalUser()</para>

**参数:**

- `unIP` (`ref SteamIPAddress_t`)
- `usPort` (`ushort`)

### GetISteamFriends (静态)

```csharp
IntPtr GetISteamFriends(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> returns the ISteamFriends interface</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

### GetISteamUtils (静态)

```csharp
IntPtr GetISteamUtils(HSteamPipe hSteamPipe, string pchVersion)
```

<para> returns the ISteamUtils interface</para>

**参数:**

- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

### GetISteamMatchmaking (静态)

```csharp
IntPtr GetISteamMatchmaking(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> returns the ISteamMatchmaking interface</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

### GetISteamMatchmakingServers (静态)

```csharp
IntPtr GetISteamMatchmakingServers(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> returns the ISteamMatchmakingServers interface</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

### GetISteamGenericInterface (静态)

```csharp
IntPtr GetISteamGenericInterface(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> returns the a generic interface</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

### GetISteamUserStats (静态)

```csharp
IntPtr GetISteamUserStats(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> returns the ISteamUserStats interface</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

### GetISteamGameServerStats (静态)

```csharp
IntPtr GetISteamGameServerStats(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> returns the ISteamGameServerStats interface</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

### GetISteamApps (静态)

```csharp
IntPtr GetISteamApps(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> returns apps interface</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

### GetISteamNetworking (静态)

```csharp
IntPtr GetISteamNetworking(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> networking</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

### GetISteamRemoteStorage (静态)

```csharp
IntPtr GetISteamRemoteStorage(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> remote storage</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

### GetISteamScreenshots (静态)

```csharp
IntPtr GetISteamScreenshots(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> user screenshots</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

### GetISteamGameSearch (静态)

```csharp
IntPtr GetISteamGameSearch(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> game search</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

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

<para> API warning handling</para> <para> 'int' is the severity; 0 for msg, 1 for warning</para> <para> 'const char *' is the text of the message</para> <para> callbacks will occur directly after the API function is called that generated the warning or message.</para>

**参数:**

- `pFunction` (`SteamAPIWarningMessageHook_t`)

### BShutdownIfAllPipesClosed (静态)

```csharp
bool BShutdownIfAllPipesClosed()
```

<para> Trigger global shutdown for the DLL</para>

**返回值:** `bool`

### GetISteamHTTP (静态)

```csharp
IntPtr GetISteamHTTP(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> Expose HTTP interface</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

### GetISteamController (静态)

```csharp
IntPtr GetISteamController(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> Exposes the ISteamController interface - deprecated in favor of Steam Input</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

### GetISteamUGC (静态)

```csharp
IntPtr GetISteamUGC(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> Exposes the ISteamUGC interface</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

### GetISteamMusic (静态)

```csharp
IntPtr GetISteamMusic(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> Music Player</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

### GetISteamMusicRemote (静态)

```csharp
IntPtr GetISteamMusicRemote(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> Music Player Remote</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

### GetISteamHTMLSurface (静态)

```csharp
IntPtr GetISteamHTMLSurface(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> html page display</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

### GetISteamInventory (静态)

```csharp
IntPtr GetISteamInventory(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> inventory</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

### GetISteamVideo (静态)

```csharp
IntPtr GetISteamVideo(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> Video</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

### GetISteamParentalSettings (静态)

```csharp
IntPtr GetISteamParentalSettings(HSteamUser hSteamuser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> Parental controls</para>

**参数:**

- `hSteamuser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

### GetISteamInput (静态)

```csharp
IntPtr GetISteamInput(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> Exposes the Steam Input interface for controller support</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

### GetISteamParties (静态)

```csharp
IntPtr GetISteamParties(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> Steam Parties interface</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

### GetISteamRemotePlay (静态)

```csharp
IntPtr GetISteamRemotePlay(HSteamUser hSteamUser, HSteamPipe hSteamPipe, string pchVersion)
```

<para> Steam Remote Play interface</para>

**参数:**

- `hSteamUser` (`HSteamUser`)
- `hSteamPipe` (`HSteamPipe`)
- `pchVersion` (`string`)

**返回值:** `IntPtr`

