<a id="cutlleanvector-t-i"></a>

# 🏗️ CUtlLeanVector&lt;T, I&gt;

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

**继承:** `IDisposable`

**实现接口:** `IEnumerable\<T\>
    where I : unmanaged`, `IBinaryInteger\<I\>`, `IMinMaxValue\<I\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `Count` | `I` | - | - |
| `Allocated` | `I` | - | - |
| `Elements` | `nint` | - | - |
| `Index` | `I` | - | - |
| `Base` | `nint` | - | - |

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ElementSize` | `int` | - | - |
| `NumAllocated` | `int` | - | - |
| `ExternallyAllocated` | `bool` | - | - |
| `Base` | `nint` | - | - |
| `this[I index]` | `ref T` | - | - |

## ⚙️ 方法

### Equals

```csharp
bool Equals(object? obj)
```

**参数:**

- `obj` (`object?`)

**返回值:** `bool`

### GetHashCode

```csharp
int GetHashCode()
```

**返回值:** `int`

### EnsureCapacity

```csharp
void EnsureCapacity(int num, bool force)
```

**参数:**

- `num` (`int`)
- `force` (`bool`)

**用法示例:**
```csharp
vector.EnsureCapacity(10, true);
```

### SetExternalBuffer

```csharp
void SetExternalBuffer(nint memory, I allocationCount, I numElements)
```

**参数:**

- `memory` (`nint`)
- `allocationCount` (`I`)
- `numElements` (`I`)

**用法示例:**
```csharp
vector.SetExternalBuffer(memoryPtr, 10, 5);
```

### AssumeMemory

```csharp
void AssumeMemory(nint memory, I allocationCount, I numElements)
```

**参数:**

- `memory` (`nint`)
- `allocationCount` (`I`)
- `numElements` (`I`)

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

### RemoveAll

```csharp
void RemoveAll()
```

**用法示例:**
```csharp
vector.RemoveAll();
```

### Purge

```csharp
void Purge()
```

**用法示例:**
```csharp
vector.Purge();
```

### Element

```csharp
T Element(I idx)
```

**参数:**

- `idx` (`I`)

**返回值:** `T`

**用法示例:**
```csharp
var element = vector.Element(0);
```

### AddToTail

```csharp
I AddToTail()
```

**返回值:** `I`

**用法示例:**
```csharp
CUtlLeanVector vector; var item = vector.AddToTail();
```

### AddToTail

```csharp
I AddToTail(T element)
```

**参数:**

- `element` (`T`)

**返回值:** `I`

**用法示例:**
```csharp
CUtlLeanVector vector;
vector.AddToTail(default(T));
```

### SetCount

```csharp
void SetCount(I count)
```

**参数:**

- `count` (`I`)

**用法示例:**
```csharp
vector.SetCount(10);
```

### Find

```csharp
I Find(T element)
```

**参数:**

- `element` (`T`)

**返回值:** `I`

**用法示例:**
```csharp
var index = leanVector.Find(targetElement);
```

### FastRemove

```csharp
void FastRemove(I elem)
```

**参数:**

- `elem` (`I`)

**用法示例:**
```csharp
vector.FastRemove(element);
```

### Remove

```csharp
void Remove(I elem)
```

**参数:**

- `elem` (`I`)

**用法示例:**
```csharp
vector.Remove(elem);
```

### RemoveMultiple

```csharp
void RemoveMultiple(I idx, I count)
```

**参数:**

- `idx` (`I`)
- `count` (`I`)

**用法示例:**
```csharp
vector.RemoveMultiple(0, 5);
```

### RemoveMultipleFromHead

```csharp
void RemoveMultipleFromHead(I count)
```

**参数:**

- `count` (`I`)

**用法示例:**
```csharp
vector.RemoveMultipleFromHead(5);
```

### RemoveMultipleFromTail

```csharp
void RemoveMultipleFromTail(I count)
```

**参数:**

- `count` (`I`)

**用法示例:**
```csharp
vector.RemoveMultipleFromTail(3);
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
vector.FindAndRemove(value);
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

### Dispose

```csharp
void Dispose()
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

