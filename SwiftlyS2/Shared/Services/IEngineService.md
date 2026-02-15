# 🔌 IEngineService

**命名空间:** `SwiftlyS2.Shared.Services`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ServerIP` | `string?` | get | 服务器的IP地址。 |
| `WorkshopId` | `string` | get | 获取当前地图的工作坊ID。 |
| `GlobalVars` | `ref CGlobalVars` | get | 获取对全局变量结构的引用。 |

## ⚙️ 方法

### IsMapValid

```csharp
bool IsMapValid(string map)
```

判断指定的地图字符串是否代表服务器文件中的一个有效地图。

**参数:**

- `map` (`string`) - 要验证的地图字符串。同时也支持创意工坊 ID。

**返回值:** `bool` - 如果地图有效，则为 true；否则为 false。

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

- `command` (`string`) - 要执行的命令。不能为 null 或空。

**用法示例:**
```csharp
engineService.ExecuteCommand("start");
```

### ExecuteCommandAsync

```csharp
Task ExecuteCommandAsync(string command)
```

在当前上下文中异步执行指定的命令字符串。

**参数:**

- `command` (`string`) - 要执行的命令。不能为 null 或空。

**返回值:** `Task`

**用法示例:**
```csharp
await engineService.ExecuteCommandAsync("start_game");
```

### ExecuteCommandWithBuffer

```csharp
void ExecuteCommandWithBuffer(string command, Action<string> bufferCallback)
```

在当前上下文中执行指定的命令字符串。

**参数:**

- `command` (`string`) - 要执行的命令。不能为 null 或空。
- `bufferCallback` (`Action\<string\>`) - 用于接收命令输出的回调。

**用法示例:**
```csharp
engineService.ExecuteCommandWithBuffer("echo Hello", Console.WriteLine);
```

### ExecuteCommandWithBufferAsync

```csharp
Task ExecuteCommandWithBufferAsync(string command, Action<string> bufferCallback)
```

在当前上下文中，使用缓冲回调异步执行指定的命令字符串。

**参数:**

- `command` (`string`) - 要执行的命令。不能为 null 或空。
- `bufferCallback` (`Action\<string\>`) - 用于接收命令输出的回调。

**返回值:** `Task`

**用法示例:**
```csharp
await engineService.ExecuteCommandWithBufferAsync("status", Console.WriteLine);
```

### FindGameSystemByName

```csharp
nint? FindGameSystemByName(string name)
```

按名称查找游戏系统。

**参数:**

- `name` (`string`) - 游戏系统的名称。

**返回值:** `nint?` - 游戏系统句柄。如果未找到则为 null。

**用法示例:**
```csharp
nint? result = engineService.FindGameSystemByName("Unity");
```

