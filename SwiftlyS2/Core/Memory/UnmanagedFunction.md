# 📦 UnmanagedFunction

**命名空间:** `SwiftlyS2.Core.Memory`

**类型:** `class`

**继承:** `UnmanagedFunction`

**实现接口:** `IUnmanagedFunction\<TDelegate\>`, `IDisposable where TDelegate : Delegate`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `Address` | `nint` | get, set | - |
| `CallOriginal` | `TDelegate` | get | - |
| `Call` | `TDelegate` | get, set | - |
| `Hooks` | `List\<Guid\>` | get, set | - |

## ⚙️ 方法

### AddHook

```csharp
Guid AddHook(Func<Func<TDelegate>, TDelegate> callbackBuilder)
```

**参数:**

- `callbackBuilder` (`Func\<Func\<TDelegate\>, TDelegate\>`)

**返回值:** `Guid`

### RemoveHook

```csharp
void RemoveHook(Guid id)
```

**参数:**

- `id` (`Guid`)

### Dispose

```csharp
void Dispose()
```

