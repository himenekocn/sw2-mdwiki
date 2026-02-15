# 🏗️ CUtlLeanVector

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

### SetExternalBuffer

```csharp
void SetExternalBuffer(nint memory, I allocationCount, I numElements)
```

**参数:**

- `memory` (`nint`)
- `allocationCount` (`I`)
- `numElements` (`I`)

### AssumeMemory

```csharp
void AssumeMemory(nint memory, I allocationCount, I numElements)
```

**参数:**

- `memory` (`nint`)
- `allocationCount` (`I`)
- `numElements` (`I`)

### DetachMemory

```csharp
nint DetachMemory()
```

**返回值:** `nint`

### RemoveAll

```csharp
void RemoveAll()
```

### Purge

```csharp
void Purge()
```

### AddToTail

```csharp
I AddToTail()
```

**返回值:** `I`

### AddToTail

```csharp
I AddToTail(T element)
```

**参数:**

- `element` (`T`)

**返回值:** `I`

### SetCount

```csharp
void SetCount(I count)
```

**参数:**

- `count` (`I`)

### Find

```csharp
I Find(T element)
```

**参数:**

- `element` (`T`)

**返回值:** `I`

### FastRemove

```csharp
void FastRemove(I elem)
```

**参数:**

- `elem` (`I`)

### Remove

```csharp
void Remove(I elem)
```

**参数:**

- `elem` (`I`)

### RemoveMultiple

```csharp
void RemoveMultiple(I idx, I count)
```

**参数:**

- `idx` (`I`)
- `count` (`I`)

### RemoveMultipleFromHead

```csharp
void RemoveMultipleFromHead(I count)
```

**参数:**

- `count` (`I`)

### RemoveMultipleFromTail

```csharp
void RemoveMultipleFromTail(I count)
```

**参数:**

- `count` (`I`)

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

### Dispose

```csharp
void Dispose()
```

### GetEnumerator

```csharp
IEnumerator<T> GetEnumerator()
```

**返回值:** `IEnumerator\<T\>`

