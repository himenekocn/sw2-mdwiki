# 📦 SteamAPI

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### Init (静态)

```csharp
bool Init()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamAPI.Init();
```

### Shutdown (静态)

```csharp
void Shutdown()
```

**用法示例:**
```csharp
SteamAPI.Shutdown();
```

### RestartAppIfNecessary (静态)

```csharp
bool RestartAppIfNecessary(AppId_t unOwnAppID)
```

**参数:**

- `unOwnAppID` (`AppId_t`)

**返回值:** `bool`

**用法示例:**
```csharp
bool needsRestart = SteamAPI.RestartAppIfNecessary(123456);
```

### ReleaseCurrentThreadMemory (静态)

```csharp
void ReleaseCurrentThreadMemory()
```

**用法示例:**
```csharp
SteamAPI.ReleaseCurrentThreadMemory();
```

### RunCallbacks (静态)

```csharp
void RunCallbacks()
```

**用法示例:**
```csharp
SteamAPI.RunCallbacks();
```

### IsSteamRunning (静态)

```csharp
bool IsSteamRunning()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isRunning = SteamAPI.IsSteamRunning();
```

### GetHSteamPipe (静态)

```csharp
HSteamPipe GetHSteamPipe()
```

**返回值:** `HSteamPipe`

**用法示例:**
```csharp
HSteamPipe pipe = SteamAPI.GetHSteamPipe();
```

### GetHSteamUser (静态)

```csharp
HSteamUser GetHSteamUser()
```

**返回值:** `HSteamUser`

**用法示例:**
```csharp
HSteamUser user = SteamAPI.GetHSteamUser();
```

