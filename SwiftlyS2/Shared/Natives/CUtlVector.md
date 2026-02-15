# 🏗️ CUtlVector

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

**继承:** `IEnumerable\<T\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `Base` | `nint` | - | - |
| `Count` | `int` | - | - |
| `Capacity` | `int` | - | - |

## ⚙️ 方法

### Purge

```csharp
void Purge()
```

### EnsureCapacity

```csharp
void EnsureCapacity(int num)
```

**参数:**

- `num` (`int`)

### SetExternalBuffer

```csharp
void SetExternalBuffer(nint memory, int allocationCount, int numELements, bool readOnly)
```

**参数:**

- `memory` (`nint`)
- `allocationCount` (`int`)
- `numELements` (`int`)
- `readOnly` (`bool`)

### AssumeMemory

```csharp
void AssumeMemory(nint memory, int allocationCount, int numElements)
```

**参数:**

- `memory` (`nint`)
- `allocationCount` (`int`)
- `numElements` (`int`)

### DetachMemory

```csharp
nint DetachMemory()
```

**返回值:** `nint`

### IsValidIndex

```csharp
bool IsValidIndex(int index)
```

**参数:**

- `index` (`int`)

**返回值:** `bool`

### GrowVector

```csharp
void GrowVector(int count)
```

**参数:**

- `count` (`int`)

### InsertBeforeIdx

```csharp
int InsertBeforeIdx(int elem)
```

**参数:**

- `elem` (`int`)

**返回值:** `int`

### InsertAfterIdx

```csharp
int InsertAfterIdx(int elem)
```

**参数:**

- `elem` (`int`)

**返回值:** `int`

### InsertBefore

```csharp
int InsertBefore(int idx, T value)
```

**参数:**

- `idx` (`int`)
- `value` (`T`)

**返回值:** `int`

### InsertAfter

```csharp
int InsertAfter(int idx, T value)
```

**参数:**

- `idx` (`int`)
- `value` (`T`)

**返回值:** `int`

### AddToHead

```csharp
int AddToHead(T value)
```

**参数:**

- `value` (`T`)

**返回值:** `int`

### AddToTail

```csharp
int AddToTail(T value)
```

**参数:**

- `value` (`T`)

**返回值:** `int`

### AddVectorToTail

```csharp
int AddVectorToTail(CUtlVector<T> other)
```

**参数:**

- `other` (`CUtlVector\<T\>`)

**返回值:** `int`

### Find

```csharp
int Find(T value)
```

**参数:**

- `value` (`T`)

**返回值:** `int`

### FillWithValue

```csharp
void FillWithValue(T value)
```

**参数:**

- `value` (`T`)

### HasElement

```csharp
bool HasElement(T value)
```

**参数:**

- `value` (`T`)

**返回值:** `bool`

### FastRemove

```csharp
void FastRemove(int elem)
```

**参数:**

- `elem` (`int`)

### FindAndRemove

```csharp
bool FindAndRemove(T value)
```

**参数:**

- `value` (`T`)

**返回值:** `bool`

### FindAndFastRemove

```csharp
bool FindAndFastRemove(T value)
```

**参数:**

- `value` (`T`)

**返回值:** `bool`

### RemoveMultiple

```csharp
void RemoveMultiple(int idx, int count)
```

**参数:**

- `idx` (`int`)
- `count` (`int`)

### RemoveMultipleFromHead

```csharp
void RemoveMultipleFromHead(int count)
```

**参数:**

- `count` (`int`)

### RemoveMultipleFromTail

```csharp
void RemoveMultipleFromTail(int count)
```

**参数:**

- `count` (`int`)

### Remove

```csharp
void Remove(int elem)
```

**参数:**

- `elem` (`int`)

### RemoveAll

```csharp
void RemoveAll()
```

### GetEnumerator

```csharp
IEnumerator<T> GetEnumerator()
```

**返回值:** `IEnumerator\<T\>`

