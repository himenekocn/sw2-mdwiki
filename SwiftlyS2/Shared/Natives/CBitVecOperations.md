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
uint buffer[10]; CBitVecOperations::ClearAll(buffer, 10);
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
uint buffer[10]; CBitVecOperations::SetAll(buffer, 10);
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
uint buffer[10]; CBitVecOperations.Set(buffer, 5u, 32u);
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
uint buffer[10]; CBitVecOperations::Set(buffer, 5, 32);
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
CBitVecOperations::Clear(buffer, 32u, 1024u);
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
CBitVecOperations::Clear(buffer, 32u, 1024u);
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
uint buffer[10] = {0};  
bool result = CBitVecOperations.IsSet(buffer, 5u, 32u);
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
bool result = CBitVecOperations.IsSet(myBuffer, 5, 32);
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
int count = CBitVecOperations.Count(buffer, 10);
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
uint buffer[4] = {0};  
bool result = CBitVecOperations::IsAllClear(buffer, 4);
```

