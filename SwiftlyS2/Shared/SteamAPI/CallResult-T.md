<a id="callresult-t"></a>

# 📦 CallResult&lt;T&gt;

表示一个自动管理其生命周期的 Steam 调用结果。

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

**继承:** `ICallResultHandler\<T\>`

**实现接口:** `IDisposable where T : struct`

## ⚙️ 方法

### Create (静态)

```csharp
CallResult<T> Create(ulong hAPICall, Action<T, bool> callback)
```

创建并注册一个新的调用结果

**参数:**

- `hAPICall` (`ulong`)
- `callback` (`Action\<T, bool\>`)

**返回值:** `CallResult\<T\>`

**用法示例:**
```csharp
CallResult<MyResponse> result = CallResult<MyResponse>.Create(12345, (response, success) => { });
```

### Set

```csharp
void Set(ulong hAPICall)
```

设置或更改 API 调用以等待

**参数:**

- `hAPICall` (`ulong`)

**用法示例:**
```csharp
callResult.Set(1234567890UL);
```

### Dispose

```csharp
void Dispose()
```

