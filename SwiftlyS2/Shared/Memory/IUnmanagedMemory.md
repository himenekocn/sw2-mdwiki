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

在指定地址挂钩一个原生函数，并使用托管回调。该回调会接收一个上下文结构，该结构允许读取和修改CPU寄存器。

**参数:**

- `callback` (`MidHookDelegate`) - 当代码执行到该地址时调用的回调。

**返回值:** `Guid`

**用法示例:**
```csharp
Guid hookId = IUnmanagedMemory.AddHook((ctx) => { /* 修改 ctx 寄存器 */ });
```

### RemoveHook

```csharp
void RemoveHook(Guid id)
```

根据指定的ID取消挂钩。

**参数:**

- `id` (`Guid`) - 要取消挂钩的钩子的 ID。

**用法示例:**
```csharp
IUnmanagedMemory.RemoveHook(someId);
```

