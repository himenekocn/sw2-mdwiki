# 📦 EngineService

**命名空间:** `SwiftlyS2.Core.Services`

**类型:** `class`

**继承:** `IEngineService`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `Map` | `string` | - | - |
| `MaxPlayers` | `int` | - | - |
| `CurrentTime` | `float` | - | - |
| `TickCount` | `int` | - | - |

## ⚙️ 方法

### ExecuteCommand

```csharp
void ExecuteCommand(string command)
```

**参数:**

- `command` (`string`)

### ExecuteCommandAsync

```csharp
Task ExecuteCommandAsync(string command)
```

**参数:**

- `command` (`string`)

**返回值:** `Task`

### ExecuteCommandWithBuffer

```csharp
void ExecuteCommandWithBuffer(string command, Action<string> bufferCallback)
```

**参数:**

- `command` (`string`)
- `bufferCallback` (`Action\<string\>`)

### ExecuteCommandWithBufferAsync

```csharp
Task ExecuteCommandWithBufferAsync(string command, Action<string> bufferCallback)
```

**参数:**

- `command` (`string`)
- `bufferCallback` (`Action\<string\>`)

**返回值:** `Task`

### IsMapValid

```csharp
bool IsMapValid(string map)
```

**参数:**

- `map` (`string`)

**返回值:** `bool`

### FindGameSystemByName

```csharp
nint? FindGameSystemByName(string name)
```

**参数:**

- `name` (`string`)

**返回值:** `nint?`

