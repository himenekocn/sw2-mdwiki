# 📦 UnmanagedMemory

**命名空间:** `SwiftlyS2.Core.Memory`

**类型:** `class`

**继承:** `NativeHandle`

**实现接口:** `IUnmanagedMemory`, `IDisposable`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `Address` | `nint` | get, set | - |
| `Hooks` | `List\<Guid\>` | get | - |

## ⚙️ 方法

### AddHook

```csharp
Guid AddHook(MidHookDelegate callback)
```

**参数:**

- `callback` (`MidHookDelegate`)

**返回值:** `Guid`

### Dispose

```csharp
void Dispose()
```

### RemoveHook

```csharp
void RemoveHook(Guid id)
```

**参数:**

- `id` (`Guid`)

