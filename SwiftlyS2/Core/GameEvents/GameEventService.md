# 📦 GameEventService

**命名空间:** `SwiftlyS2.Core.GameEvents`

**类型:** `class`

**继承:** `IGameEventService`

**实现接口:** `IDisposable`

## ⚙️ 方法

### Unhook

```csharp
void Unhook(Guid guid)
```

**参数:**

- `guid` (`Guid`)

### IsListeningToEvent

```csharp
bool IsListeningToEvent(int slot, string eventName)
```

**参数:**

- `slot` (`int`)
- `eventName` (`string`)

**返回值:** `bool`

### Dispose

```csharp
void Dispose()
```

