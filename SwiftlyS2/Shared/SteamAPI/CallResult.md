# 📦 CallResult

Represents a Steam call result that automatically manages its lifecycle

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

**继承:** `ICallResultHandler\<T\>`

**实现接口:** `IDisposable where T : struct`

## ⚙️ 方法

### Create (静态)

```csharp
CallResult<T> Create(ulong hAPICall, Action<T, bool> callback)
```

Create and register a new call result

**参数:**

- `hAPICall` (`ulong`)
- `callback` (`Action\<T, bool\>`)

**返回值:** `CallResult\<T\>`

### Set

```csharp
void Set(ulong hAPICall)
```

Set or change the API call to wait for

**参数:**

- `hAPICall` (`ulong`)

### Dispose

```csharp
void Dispose()
```

