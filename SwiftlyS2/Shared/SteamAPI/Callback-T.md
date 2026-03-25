<a id="callback-t"></a>

# 📦 Callback&lt;T&gt;

表示一个自动管理其生命周期的 Steam 回调。

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

**继承:** `ICallbackHandler\<T\>`

**实现接口:** `IDisposable where T : struct`

## ⚙️ 方法

### Create (静态)

```csharp
Callback<T> Create(Action<T> callback)
```

创建并注册一个新的回调

**参数:**

- `callback` (`Action\<T\>`)

**返回值:** `Callback\<T\>`

**用法示例:**
```csharp
var callback = Callback.Create<string>(msg => Console.WriteLine(msg));
```

### Dispose

```csharp
void Dispose()
```

