# 📦 NativeEngineHelpers

**命名空间:** `SwiftlyS2.Core.Natives`

**类型:** `class`

## ⚙️ 方法

### GetIP (静态)

```csharp
string GetIP()
```

**返回值:** `string`

### IsMapValid (静态)

```csharp
bool IsMapValid(string map_name)
```

it can be map name, or workshop id

**参数:**

- `map_name` (`string`)

**返回值:** `bool`

### ExecuteCommand (静态)

```csharp
void ExecuteCommand(string command)
```

**参数:**

- `command` (`string`)

### FindGameSystemByName (静态)

```csharp
nint FindGameSystemByName(string name)
```

**参数:**

- `name` (`string`)

**返回值:** `nint`

### SendMessageToConsole (静态)

```csharp
void SendMessageToConsole(string msg)
```

**参数:**

- `msg` (`string`)

### GetTraceManager (静态)

```csharp
nint GetTraceManager()
```

**返回值:** `nint`

### GetCurrentGame (静态)

```csharp
string GetCurrentGame()
```

**返回值:** `string`

### GetNativeVersion (静态)

```csharp
string GetNativeVersion()
```

**返回值:** `string`

### GetMenuSettings (静态)

```csharp
string GetMenuSettings()
```

**返回值:** `string`

### GetGlobalVars (静态)

```csharp
nint GetGlobalVars()
```

**返回值:** `nint`

### GetNetworkGameServer (静态)

```csharp
nint GetNetworkGameServer()
```

**返回值:** `nint`

### GetCSGODirectoryPath (静态)

```csharp
string GetCSGODirectoryPath()
```

**返回值:** `string`

### GetGameDirectoryPath (静态)

```csharp
string GetGameDirectoryPath()
```

**返回值:** `string`

### GetWorkshopId (静态)

```csharp
string GetWorkshopId()
```

**返回值:** `string`

### DispatchParticleEffect (静态)

```csharp
void DispatchParticleEffect(string particleName, uint attachmentType, nint entity, byte attachmentPoint, nint attachmentName, bool resetAllParticlesOnEntity, int splitScreenSlot, ulong filtermask)
```

**参数:**

- `particleName` (`string`)
- `attachmentType` (`uint`)
- `entity` (`nint`)
- `attachmentPoint` (`byte`)
- `attachmentName` (`nint`)
- `resetAllParticlesOnEntity` (`bool`)
- `splitScreenSlot` (`int`)
- `filtermask` (`ulong`)

