# 📦 ConsoleOutputService

**命名空间:** `SwiftlyS2.Core.ConsoleOutput`

**类型:** `class`

**继承:** `IConsoleOutputService`

**实现接口:** `IDisposable`

## ⚙️ 方法

### IsFilterEnabled

```csharp
bool IsFilterEnabled()
```

**返回值:** `bool`

### ToggleFilter

```csharp
void ToggleFilter()
```

### ReloadFilterConfiguration

```csharp
void ReloadFilterConfiguration()
```

### NeedsFiltering

```csharp
bool NeedsFiltering(string message)
```

**参数:**

- `message` (`string`)

**返回值:** `bool`

### GetCounterText

```csharp
string GetCounterText()
```

**返回值:** `string`

### WriteToServerConsole

```csharp
void WriteToServerConsole(string message)
```

**参数:**

- `message` (`string`)

### Dispose

```csharp
void Dispose()
```

