# 📦 CBitVecOperations

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `class`

## ⚙️ 方法

### ClearAll (静态)

```csharp
void ClearAll(uint* buffer, int intCount)
```

**参数:**

- `buffer` (`uint*`)
- `intCount` (`int`)

**用法示例:**
```csharp
unsafe { uint[] buffer = new uint[10]; fixed (uint* ptr = buffer) CBitVecOperations.ClearAll(ptr, 10); }
```

### SetAll (静态)

```csharp
void SetAll(uint* buffer, int intCount)
```

**参数:**

- `buffer` (`uint*`)
- `intCount` (`int`)

**用法示例:**
```csharp
uint[] data = new uint[10]; fixed (uint* ptr = data) CBitVecOperations.SetAll(ptr, 10);
```

### Set (静态)

```csharp
void Set(uint* buffer, uint index, uint maxBits)
```

**参数:**

- `buffer` (`uint*`)
- `index` (`uint`)
- `maxBits` (`uint`)

**用法示例:**
```csharp
unsafe { fixed (uint* ptr = buffer) CBitVecOperations.Set(ptr, index, maxBits); }
```

### Set (静态)

```csharp
void Set(uint* buffer, int index, uint maxBits)
```

**参数:**

- `buffer` (`uint*`)
- `index` (`int`)
- `maxBits` (`uint`)

**用法示例:**
```csharp
unsafe { uint[] data = new uint[1]; fixed (uint* ptr = data) CBitVecOperations.Set(ptr, 5, 32); }
```

### Clear (静态)

```csharp
void Clear(uint* buffer, uint index, uint maxBits)
```

**参数:**

- `buffer` (`uint*`)
- `index` (`uint`)
- `maxBits` (`uint`)

**用法示例:**
```csharp
uint* buffer = stackalloc uint[10]; CBitVecOperations.Clear(buffer, 0, 32);
```

### Clear (静态)

```csharp
void Clear(uint* buffer, int index, uint maxBits)
```

**参数:**

- `buffer` (`uint*`)
- `index` (`int`)
- `maxBits` (`uint`)

**用法示例:**
```csharp
uint* buffer = stackalloc uint[10]; CBitVecOperations.Clear(buffer, 0, 32);
```

### IsSet (静态)

```csharp
bool IsSet(uint* buffer, uint index, uint maxBits)
```

**参数:**

- `buffer` (`uint*`)
- `index` (`uint`)
- `maxBits` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint[] data = new uint[10]; bool result = CBitVecOperations.IsSet((uint*)System.Runtime.InteropServices.Marshal.UnsafeAddrOfPinnedArrayElement(data, 0), 5, 64);
```

### IsSet (静态)

```csharp
bool IsSet(uint* buffer, int index, uint maxBits)
```

**参数:**

- `buffer` (`uint*`)
- `index` (`int`)
- `maxBits` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
unsafe { bool result = CBitVecOperations.IsSet(buffer, 5, 32); }
```

### Count (静态)

```csharp
int Count(uint* buffer, int intCount)
```

**参数:**

- `buffer` (`uint*`)
- `intCount` (`int`)

**返回值:** `int`

**用法示例:**
```csharp
uint[] data = new uint[10]; int result; unsafe { fixed (uint* ptr = data) { result = CBitVecOperations.Count(ptr, 10); } }
```

### IsAllClear (静态)

```csharp
bool IsAllClear(uint* buffer, int intCount)
```

**参数:**

- `buffer` (`uint*`)
- `intCount` (`int`)

**返回值:** `bool`

**用法示例:**
```csharp
unsafe { bool result = CBitVecOperations.IsAllClear(null, 0); }
```

