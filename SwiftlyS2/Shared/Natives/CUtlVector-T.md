# 🏗️ CUtlVector<T>

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
CUtlVector<int> vector;
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
CUtlVector<int> vec;
vec.EnsureCapacity(10);
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
CUtlVector.SetExternalBuffer(bufferPtr, 10, 5, false);
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
CUtlVector vector;
vector.AssumeMemory(IntPtr.Zero, 0, 0);
```

### DetachMemory

```csharp
nint DetachMemory()
```

**返回值:** `nint`

**用法示例:**
```csharp
CUtlVector vector = default;
nint memory = vector.DetachMemory();
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
CUtlVector<int> vec = GetVector();  
bool valid = vec.IsValidIndex(0);
```

### GrowVector

```csharp
void GrowVector(int count)
```

**参数:**

- `count` (`int`)

**用法示例:**
```csharp
CUtlVector vector;
vector.GrowVector(10);
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
CUtlVector vector = GetExistingVector();  
vector.InsertBeforeIdx(5);
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
CUtlVector vector = GetExistingVector();  
vector.InsertAfterIdx(5);
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
CUtlVector<int> vector = default;
vector.InsertBefore(0, 42);
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
CUtlVector<int> vec;
vec.InsertAfter(0, 42);
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
CUtlVector<int> vec;
vec.AddToHead(42);
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
CUtlVector<int> vec;
vec.AddToTail(42);
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
CUtlVector<int> a, b;
a.AddVectorToTail(b);
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
int index = vector.Find(value);
```

### FillWithValue

```csharp
void FillWithValue(T value)
```

**参数:**

- `value` (`T`)

**用法示例:**
```csharp
CUtlVector<int> vec;
vec.FillWithValue(42);
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
CUtlVector<T> vector = GetExistingVector();  
bool exists = vector.HasElement(someValue);
```

### FastRemove

```csharp
void FastRemove(int elem)
```

**参数:**

- `elem` (`int`)

**用法示例:**
```csharp
CUtlVector vector = GetExistingVector();  
vector.FastRemove(5);
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
CUtlVector<int> vec = {1, 2, 3};
vec.FindAndRemove(2);
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
CUtlVector<int> vec = GetExistingVector();  
vec.FindAndFastRemove(42);
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
CUtlVector vector = ...; // 假设已初始化  
vector.RemoveMultiple(2, 3);
```

### RemoveMultipleFromHead

```csharp
void RemoveMultipleFromHead(int count)
```

**参数:**

- `count` (`int`)

**用法示例:**
```csharp
CUtlVector vec = someExistingVector;
vec.RemoveMultipleFromHead(3);
```

### RemoveMultipleFromTail

```csharp
void RemoveMultipleFromTail(int count)
```

**参数:**

- `count` (`int`)

**用法示例:**
```csharp
CUtlVector vec;  
vec.RemoveMultipleFromTail(3);
```

### Remove

```csharp
void Remove(int elem)
```

**参数:**

- `elem` (`int`)

**用法示例:**
```csharp
CUtlVector vector = ...; // 已有实例
vector.Remove(0);
```

### RemoveAll

```csharp
void RemoveAll()
```

**用法示例:**
```csharp
CUtlVector vector;
vector.RemoveAll();
```

### GetEnumerator

```csharp
IEnumerator<T> GetEnumerator()
```

**返回值:** `IEnumerator\<T\>`

**用法示例:**
```csharp
foreach (var item in someUtlVector) { Console.WriteLine(item); }
```

