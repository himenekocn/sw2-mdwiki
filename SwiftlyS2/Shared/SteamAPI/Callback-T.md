# 📦 Callback<T>

表示一个自动管理其生命周期的 Steam 回调

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

**继承:** `ICallbackHandler\<T\>`

**实现接口:** `IDisposable where T : struct`

## ⚙️ 方法

### Create (静态)

```csharp
Callback<T> Create(Action<T> callback)
```

创建并注册一个新回调

**参数:**

- `callback` (`Action\<T\>`)

**返回值:** `Callback\<T\>`

**用法示例:**
```csharp
Callback<int> cb = Callback.Create((int value) => Console.WriteLine(value));
```

### Dispose

```csharp
void Dispose()
```

