<a id="iunmanagedmemory"></a>

# 🔌 IUnmanagedMemory

**命名空间:** `SwiftlyS2.Shared.Memory`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Address` | `nint` | get | 非托管指针的地址。 |

## ⚙️ 方法

### AddHook

```csharp
Guid AddHook(MidHookDelegate callback)
```

在指定地址挂钩一个原生函数，并使用托管回调。该回调接收一个上下文结构，允许读取和修改 CPU 寄存器。

**参数:**

- `callback` (`MidHookDelegate`) - 当代码到达该地址时调用的回调函数。

**返回值:** `Guid`

**用法示例:**
```csharp
var hookId = unmanagedMemory.AddHook((ctx) => { ctx.Rax = 0; });
```

### RemoveHook

```csharp
void RemoveHook(Guid id)
```

根据其 ID 移除钩子。

**参数:**

- `id` (`Guid`) - 要解除挂钩的钩子 ID。

**用法示例:**
```csharp
manager.RemoveHook(Guid.Parse("00000000-0000-0000-0000-000000000001"));
```

