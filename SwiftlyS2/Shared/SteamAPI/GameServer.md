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

### Shutdown (静态)

```csharp
void Shutdown()
```

### RunCallbacks (静态)

```csharp
void RunCallbacks()
```

### ReleaseCurrentThreadMemory (静态)

```csharp
void ReleaseCurrentThreadMemory()
```

### BSecure (静态)

```csharp
bool BSecure()
```

**返回值:** `bool`

### GetSteamID (静态)

```csharp
CSteamID GetSteamID()
```

**返回值:** `CSteamID`

### GetHSteamPipe (静态)

```csharp
HSteamPipe GetHSteamPipe()
```

**返回值:** `HSteamPipe`

### GetHSteamUser (静态)

```csharp
HSteamUser GetHSteamUser()
```

**返回值:** `HSteamUser`

