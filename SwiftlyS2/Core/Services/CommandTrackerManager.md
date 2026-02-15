# 📦 CommandTrackerManager

**命名空间:** `SwiftlyS2.Core.Services`

**类型:** `class`

**继承:** `IDisposable`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `Output` | `ConcurrentQueue\<string\>` | get | - |
| `Created` | `DateTime` | get | - |

## ⚙️ 方法

### Dispose

```csharp
void Dispose()
```

### EnqueueCommand

```csharp
void EnqueueCommand(Action<string> callback)
```

**参数:**

- `callback` (`Action\<string\>`)

### ProcessCommand

```csharp
void ProcessCommand(IOnCommandExecuteHookEvent @event)
```

**参数:**

- `@event` (`IOnCommandExecuteHookEvent`)

### ProcessOutput

```csharp
void ProcessOutput(IOnConsoleOutputEvent @event)
```

**参数:**

- `@event` (`IOnConsoleOutputEvent`)

