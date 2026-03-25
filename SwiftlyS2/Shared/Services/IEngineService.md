<a id="iengineservice"></a>

# 🔌 IEngineService

**命名空间:** `SwiftlyS2.Shared.Services`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ServerIP` | `string?` | get | 服务器的 IP 地址。 |
| `WorkshopId` | `string` | get | 获取当前地图的创意工坊 ID。 |
| `GlobalVars` | `ref CGlobalVars` | get | 获取全局变量结构的引用。 |

## ⚙️ 方法

### IsMapValid

```csharp
bool IsMapValid(string map)
```

确定指定的地图字符串是否在服务器文件中代表一个有效的地图。

**参数:**

- `map` (`string`) - 待验证的地图字符串。它同时也支持创意工坊 ID。

**返回值:** `bool` - 如果地图有效则为 true；否则为 false。

**用法示例:**
```csharp
bool isValid = engineService.IsMapValid("de_dust2");
```

### ExecuteCommand

```csharp
void ExecuteCommand(string command)
```

在当前上下文中执行指定的命令字符串。

**参数:**

- `command` (`string`) - 要执行的命令。不得为 null 或空。

**用法示例:**
```csharp
IEngineService engine;
engine.ExecuteCommand("sv_restart 1");
```

### ExecuteCommandAsync

```csharp
Task ExecuteCommandAsync(string command)
```

在当前上下文中异步执行指定的命令字符串。

**参数:**

- `command` (`string`) - 要执行的命令。不得为 null 或空。

**返回值:** `Task`

**用法示例:**
```csharp
await engineService.ExecuteCommandAsync("sv_restart 1");
```

### ExecuteCommandWithBuffer

```csharp
void ExecuteCommandWithBuffer(string command, Action<string> bufferCallback)
```

在当前上下文中执行指定的命令字符串。

**参数:**

- `command` (`string`) - 要执行的命令。不得为 null 或空。
- `bufferCallback` (`Action\<string\>`) - 用于接收命令输出的回调。

**用法示例:**
```csharp
engineService.ExecuteCommandWithBuffer("status", msg => Console.WriteLine(msg));
```

### ExecuteCommandWithBufferAsync

```csharp
Task ExecuteCommandWithBufferAsync(string command, Action<string> bufferCallback)
```

在当前上下文中异步执行指定的命令字符串，并采用缓冲区回调。

**参数:**

- `command` (`string`) - 要执行的命令。不得为 null 或空。
- `bufferCallback` (`Action\<string\>`) - 用于接收命令输出的回调。

**返回值:** `Task`

**用法示例:**
```csharp
await engineService.ExecuteCommandWithBufferAsync("status", msg => Console.WriteLine(msg));
```

### FindGameSystemByName

```csharp
nint? FindGameSystemByName(string name)
```

根据名称查找游戏系统。

**参数:**

- `name` (`string`) - 游戏系统的名称。

**返回值:** `nint?` - 游戏系统句柄。若未找到则为 null。

**用法示例:**
```csharp
nint? systemId = engineService.FindGameSystemByName("Physics");
```

