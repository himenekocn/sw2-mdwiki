# 📦 MemoryHelpers

**命名空间:** `SwiftlyS2.Shared.Misc`

**类型:** `class`

## ⚙️ 方法

### CalcNewDoublingCount (静态)

```csharp
int CalcNewDoublingCount(int oldCount, int requestedCount, int minCount, int maxCount)
```

**参数:**

- `oldCount` (`int`)
- `requestedCount` (`int`)
- `minCount` (`int`)
- `maxCount` (`int`)

**返回值:** `int`

**用法示例:**
```csharp
int newCount = MemoryHelpers.CalcNewDoublingCount(4, 10, 2, 32);
```

### ShiftElementsRight (静态)

```csharp
void ShiftElementsRight(nint memory, int elem, int num, int size, int elementSize)
```

**参数:**

- `memory` (`nint`)
- `elem` (`int`)
- `num` (`int`)
- `size` (`int`)
- `elementSize` (`int`)

**用法示例:**
```csharp
MemoryHelpers.ShiftElementsRight(IntPtr.Zero, 0, 10, 4, 4);
```

### ShiftElementsLeft (静态)

```csharp
void ShiftElementsLeft(nint memory, int elem, int num, int size, int elementSize)
```

**参数:**

- `memory` (`nint`)
- `elem` (`int`)
- `num` (`int`)
- `size` (`int`)
- `elementSize` (`int`)

**用法示例:**
```csharp
MemoryHelpers.ShiftElementsLeft(IntPtr.Zero, 0, 10, sizeof(int), sizeof(int));
```

