# 📦 GameServer

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### Init (静态)

```csharp
bool Init(uint unIP, ushort usGamePort, ushort usQueryPort, EServerMode eServerMode, string pchVersionString)
```

**参数:**

- `unIP` (`uint`)
- `usGamePort` (`ushort`)
- `usQueryPort` (`ushort`)
- `eServerMode` (`EServerMode`)
- `pchVersionString` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = GameServer.Init(0x7F000001, 27015, 27016, EServerMode.Value, "1.0.0");
```

### Shutdown (静态)

```csharp
void Shutdown()
```

**用法示例:**
```csharp
GameServer.Shutdown();
```

### RunCallbacks (静态)

```csharp
void RunCallbacks()
```

**用法示例:**
```csharp
GameServer.RunCallbacks();
```

### ReleaseCurrentThreadMemory (静态)

```csharp
void ReleaseCurrentThreadMemory()
```

**用法示例:**
```csharp
GameServer.ReleaseCurrentThreadMemory();
```

### BSecure (静态)

```csharp
bool BSecure()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isSecure = GameServer.BSecure();
```

### GetSteamID (静态)

```csharp
CSteamID GetSteamID()
```

**返回值:** `CSteamID`

**用法示例:**
```csharp
CSteamID serverId = GameServer.GetSteamID();
```

### GetHSteamPipe (静态)

```csharp
HSteamPipe GetHSteamPipe()
```

**返回值:** `HSteamPipe`

**用法示例:**
```csharp
HSteamPipe pipe = GameServer.GetHSteamPipe();
```

### GetHSteamUser (静态)

```csharp
HSteamUser GetHSteamUser()
```

**返回值:** `HSteamUser`

**用法示例:**
```csharp
HSteamUser user = GameServer.GetHSteamUser();
```

