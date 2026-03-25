<a id="cutlvector-t"></a>

# 🏗️ CUtlVector&lt;T&gt;

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

**继承:** `IEnumerable\<T\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `Base` | `nint` | - | - |
| `Count` | `int` | - | - |
| `Capacity` | `int` | - | - |

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ElementSize` | `int` | - | - |
| `this[int index]` | `ref T` | - | - |
| `Base` | `nint` | - | - |
| `Count` | `int` | - | - |
| `Capacity` | `int` | - | - |

## ⚙️ 方法

### Purge

```csharp
void Purge()
```

**用法示例:**
```csharp
vector.Purge();
```

### EnsureCapacity

```csharp
void EnsureCapacity(int num)
```

**参数:**

- `num` (`int`)

**用法示例:**
```csharp
vector.EnsureCapacity(10);
```

### SetExternalBuffer

```csharp
void SetExternalBuffer(nint memory, int allocationCount, int numELements, bool readOnly)
```

**参数:**

- `memory` (`nint`)
- `allocationCount` (`int`)
- `numELements` (`int`)
- `readOnly` (`bool`)

**用法示例:**
```csharp
vector.SetExternalBuffer(memoryPtr, 100, 50, false);
```

### AssumeMemory

```csharp
void AssumeMemory(nint memory, int allocationCount, int numElements)
```

**参数:**

- `memory` (`nint`)
- `allocationCount` (`int`)
- `numElements` (`int`)

**用法示例:**
```csharp
vector.AssumeMemory(memoryPtr, 10, 5);
```

### DetachMemory

```csharp
nint DetachMemory()
```

**返回值:** `nint`

**用法示例:**
```csharp
nint ptr = vector.DetachMemory();
```

### IsValidIndex

```csharp
bool IsValidIndex(int index)
```

**参数:**

- `index` (`int`)

**返回值:** `bool`

**用法示例:**
```csharp
bool isValid = vector.IsValidIndex(0);
```

### GrowVector

```csharp
void GrowVector(int count)
```

**参数:**

- `count` (`int`)

**用法示例:**
```csharp
vector.GrowVector(5);
```

### InsertBeforeIdx

```csharp
int InsertBeforeIdx(int elem)
```

**参数:**

- `elem` (`int`)

**返回值:** `int`

**用法示例:**
```csharp
vector.InsertBeforeIdx(0);
```

### InsertAfterIdx

```csharp
int InsertAfterIdx(int elem)
```

**参数:**

- `elem` (`int`)

**返回值:** `int`

**用法示例:**
```csharp
int newIndex = vector.InsertAfterIdx(elem);
```

### InsertBefore

```csharp
int InsertBefore(int idx, T value)
```

**参数:**

- `idx` (`int`)
- `value` (`T`)

**返回值:** `int`

**用法示例:**
```csharp
var existingVector = GetExistingVector(); int newIndex = existingVector.InsertBefore(0, defaultValue);
```

### InsertAfter

```csharp
int InsertAfter(int idx, T value)
```

**参数:**

- `idx` (`int`)
- `value` (`T`)

**返回值:** `int`

**用法示例:**
```csharp
CUtlVector vector; vector.InsertAfter(0, default(T));
```

### AddToHead

```csharp
int AddToHead(T value)
```

**参数:**

- `value` (`T`)

**返回值:** `int`

**用法示例:**
```csharp
vector.AddToHead(value);
```

### AddToTail

```csharp
int AddToTail(T value)
```

**参数:**

- `value` (`T`)

**返回值:** `int`

**用法示例:**
```csharp
vector.AddToTail(value);
```

### AddVectorToTail

```csharp
int AddVectorToTail(CUtlVector<T> other)
```

**参数:**

- `other` (`CUtlVector\<T\>`)

**返回值:** `int`

**用法示例:**
```csharp
int count = existingVector.AddVectorToTail(otherVector);
```

### Find

```csharp
int Find(T value)
```

**参数:**

- `value` (`T`)

**返回值:** `int`

**用法示例:**
```csharp
int index = vector.Find(targetValue);
```

### FillWithValue

```csharp
void FillWithValue(T value)
```

**参数:**

- `value` (`T`)

**用法示例:**
```csharp
vector.FillWithValue(0);
```

### HasElement

```csharp
bool HasElement(T value)
```

**参数:**

- `value` (`T`)

**返回值:** `bool`

**用法示例:**
```csharp
bool exists = vector.HasElement(targetValue);
```

### FastRemove

```csharp
void FastRemove(int elem)
```

**参数:**

- `elem` (`int`)

**用法示例:**
```csharp
vector.FastRemove(0);
```

### FindAndRemove

```csharp
bool FindAndRemove(T value)
```

**参数:**

- `value` (`T`)

**返回值:** `bool`

**用法示例:**
```csharp
vector.FindAndRemove(targetValue);
```

### FindAndFastRemove

```csharp
bool FindAndFastRemove(T value)
```

**参数:**

- `value` (`T`)

**返回值:** `bool`

**用法示例:**
```csharp
vector.FindAndFastRemove(value);
```

### RemoveMultiple

```csharp
void RemoveMultiple(int idx, int count)
```

**参数:**

- `idx` (`int`)
- `count` (`int`)

**用法示例:**
```csharp
vector.RemoveMultiple(0, 5);
```

### RemoveMultipleFromHead

```csharp
void RemoveMultipleFromHead(int count)
```

**参数:**

- `count` (`int`)

**用法示例:**
```csharp
vector.RemoveMultipleFromHead(5);
```

### RemoveMultipleFromTail

```csharp
void RemoveMultipleFromTail(int count)
```

**参数:**

- `count` (`int`)

**用法示例:**
```csharp
vector.RemoveMultipleFromTail(3);
```

### Remove

```csharp
void Remove(int elem)
```

**参数:**

- `elem` (`int`)

**用法示例:**
```csharp
vector.Remove(0);
```

### RemoveAll

```csharp
void RemoveAll()
```

**用法示例:**
```csharp
myVector.RemoveAll();
```

### GetEnumerator

```csharp
IEnumerator<T> GetEnumerator()
```

**返回值:** `IEnumerator\<T\>`

**用法示例:**
```csharp
foreach (var item in vector) { }
```

