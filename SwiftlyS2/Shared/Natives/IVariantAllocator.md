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

**注意:** 此方法是抽象方法,需要在子类中实现 (override).

### Free (静态)

```csharp
void Free(nint ptr)
```

**参数:**

- `ptr` (`nint`)

**注意:** 此方法是抽象方法,需要在子类中实现 (override).

