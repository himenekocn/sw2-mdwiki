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

在指定地址使用托管回调钩取原生函数。回调接收一个上下文结构体，允许读取和修改CPU寄存器。

**参数:**

- `callback` (`MidHookDelegate`) - 代码到达该地址时要调用的回调。

**返回值:** `Guid`

**用法示例:**
```csharp
var hookId = memory.AddHook(ctx => { ctx.Rax = 0; });
```

### RemoveHook

```csharp
void RemoveHook(Guid id)
```

根据其ID取消挂钩。

**参数:**

- `id` (`Guid`) - 要解除挂钩的挂钩ID。

**用法示例:**
```csharp
IUnmanagedMemory memory;
memory.RemoveHook(Guid.Empty);
```

