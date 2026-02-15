# 📦 Callback

Represents a Steam callback that automatically manages its lifecycle

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

**继承:** `ICallbackHandler\<T\>`

**实现接口:** `IDisposable where T : struct`

## ⚙️ 方法

### Create (静态)

```csharp
Callback<T> Create(Action<T> callback)
```

Create and register a new callback

**参数:**

- `callback` (`Action\<T\>`)

**返回值:** `Callback\<T\>`

### Dispose

```csharp
void Dispose()
```

