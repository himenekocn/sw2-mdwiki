# 🔌 IConsoleOutputService

**命名空间:** `SwiftlyS2.Shared.ConsoleOutput`

**类型:** `interface`

## ⚙️ 方法

### ConsoleOutputHandler

```csharp
void ConsoleOutputHandler(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
consoleOutputService.ConsoleOutputHandler("Server started successfully");
```

### RegisterConsoleOutputListener

```csharp
Guid RegisterConsoleOutputListener(ConsoleOutputHandler handler)
```

**参数:**

- `handler` (`ConsoleOutputHandler`)

**返回值:** `Guid`

**用法示例:**
```csharp
Guid listenerId = consoleOutputService.RegisterConsoleOutputListener(handler);
```

### UnregisterConsoleOutputListener

```csharp
void UnregisterConsoleOutputListener(Guid guid)
```

**参数:**

- `guid` (`Guid`)

**用法示例:**
```csharp
convar.UnregisterConsoleOutputListener(existingGuid);
```

### IsFilterEnabled

```csharp
bool IsFilterEnabled()
```

获取控制台过滤功能是否已启用。

**返回值:** `bool` - 若启用了过滤功能则为 true，否则为 false。

**用法示例:**
```csharp
bool isEnabled = consoleOutputService.IsFilterEnabled();
```

### ToggleFilter

```csharp
void ToggleFilter()
```

切换控制台过滤器的开启/关闭状态。

**用法示例:**
```csharp
consoleOutputService.ToggleFilter();
```

### ReloadFilterConfiguration

```csharp
void ReloadFilterConfiguration()
```

从文件重新加载过滤器配置。

**用法示例:**
```csharp
consoleOutputService.ReloadFilterConfiguration();
```

### NeedsFiltering

```csharp
bool NeedsFiltering(string message)
```

检查消息是否需要过滤。

**参数:**

- `message` (`string`) - 待检查的消息。

**返回值:** `bool` - 若消息应被过滤，则为 true；否则为 false。

**用法示例:**
```csharp
bool shouldFilter = consoleOutputService.NeedsFiltering("Player joined the game");
```

### GetCounterText

```csharp
string GetCounterText()
```

获取显示已过滤消息数量的计数器文本。

**返回值:** `string` - 计数器文本。

**用法示例:**
```csharp
string counterText = consoleOutputService.GetCounterText();
```

### WriteToServerConsole

```csharp
void WriteToServerConsole(string message)
```

使用 tier0 日志系统向服务器控制台写入消息。

**参数:**

- `message` (`string`) - 该消息

**用法示例:**
```csharp
consoleOutputService.WriteToServerConsole("Server started successfully");
```

