# 🔌 IVariantAllocator

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `interface`

## ⚙️ 方法

### Alloc (静态)

```csharp
nint Alloc(ulong size)
```

**参数:**

- `size` (`ulong`)

**返回值:** `nint`

**用法示例:**
```csharp
nint ptr = IVariantAllocator.Alloc(1024);
```

### Free (静态)

```csharp
void Free(nint ptr)
```

**参数:**

- `ptr` (`nint`)

**用法示例:**
```csharp
IVariantAllocator.Free(ptr);
```

