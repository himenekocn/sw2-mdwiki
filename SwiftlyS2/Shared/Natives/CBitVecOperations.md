<a id="cbitvecoperations"></a>

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
unsafe { CBitVecOperations.ClearAll(buffer, intCount); }
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
unsafe { fixed (uint* ptr = buffer) CBitVecOperations.SetAll(ptr, count); }
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
uint[] buffer = new uint[1]; fixed (uint* ptr = buffer) { CBitVecOperations.Set(ptr, 0, 32); }
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
CBitVecOperations.Set(buffer, 0, 32);
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
unsafe { fixed (uint* ptr = new uint[1]) { CBitVecOperations.Clear(ptr, 0, 32); } }
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
unsafe { CBitVecOperations.Clear(buffer, 0, 32); }
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
bool isSet = CBitVecOperations.IsSet(buffer, 0, 32);
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
unsafe { bool result = CBitVecOperations.IsSet(buffer, 0, 32); }
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
unsafe { uint[] data = new uint[10]; fixed (uint* ptr = data) { int count = CBitVecOperations.Count(ptr, 10); } }
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
unsafe { bool result = CBitVecOperations.IsAllClear(stackalloc uint[10], 10); }
```

