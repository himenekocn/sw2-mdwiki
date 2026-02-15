# 🏗️ CUtlRBTree

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

**继承:** `IDisposable
    where TKey : unmanaged`

**实现接口:** `IBinaryInteger\<TKey\>`, `IMinMaxValue\<TKey\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `LFunc` | `nint` | - | - |
| `Root` | `TKey` | - | - |
| `NumElements` | `TKey` | - | - |
| `FirstFree` | `TKey` | - | - |

## ⚙️ 方法

### EnsureCapacity

```csharp
void EnsureCapacity(TKey num)
```

**参数:**

- `num` (`TKey`)

### IsValidIndex

```csharp
bool IsValidIndex(TKey i)
```

**参数:**

- `i` (`TKey`)

**返回值:** `bool`

### NewNode

```csharp
TKey NewNode()
```

**返回值:** `TKey`

### FreeNode

```csharp
void FreeNode(TKey i)
```

**参数:**

- `i` (`TKey`)

### RotateLeft

```csharp
void RotateLeft(TKey elem)
```

**参数:**

- `elem` (`TKey`)

### RotateRight

```csharp
void RotateRight(TKey elem)
```

**参数:**

- `elem` (`TKey`)

### InsertRebalance

```csharp
void InsertRebalance(TKey elem)
```

**参数:**

- `elem` (`TKey`)

### LinkToParent

```csharp
void LinkToParent(TKey i, TKey parent, bool isLeft)
```

**参数:**

- `i` (`TKey`)
- `parent` (`TKey`)
- `isLeft` (`bool`)

### InsertAt

```csharp
TKey InsertAt(TKey parent, bool leftchild)
```

**参数:**

- `parent` (`TKey`)
- `leftchild` (`bool`)

**返回值:** `TKey`

### RemoveRebalance

```csharp
void RemoveRebalance(TKey elem)
```

**参数:**

- `elem` (`TKey`)

### Unlink

```csharp
void Unlink(TKey elem)
```

**参数:**

- `elem` (`TKey`)

### Link

```csharp
void Link(TKey elem)
```

**参数:**

- `elem` (`TKey`)

### FindInsertionPosition

```csharp
void FindInsertionPosition(TValue val, out TKey parent, out bool leftchild)
```

**参数:**

- `val` (`TValue`)
- `parent` (`out TKey`)
- `leftchild` (`out bool`)

### RemoveAt

```csharp
void RemoveAt(TKey elem)
```

**参数:**

- `elem` (`TKey`)

### Remove

```csharp
bool Remove(TValue value)
```

**参数:**

- `value` (`TValue`)

**返回值:** `bool`

### Find

```csharp
TKey Find(TValue value)
```

**参数:**

- `value` (`TValue`)

**返回值:** `TKey`

### RemoveAll

```csharp
void RemoveAll()
```

### Purge

```csharp
void Purge()
```

### Dispose

```csharp
void Dispose()
```

### FirstInorder

```csharp
TKey FirstInorder()
```

**返回值:** `TKey`

### NextInorder

```csharp
TKey NextInorder(TKey i)
```

**参数:**

- `i` (`TKey`)

**返回值:** `TKey`

### PrevInorder

```csharp
TKey PrevInorder(TKey i)
```

**参数:**

- `i` (`TKey`)

**返回值:** `TKey`

### LastInorder

```csharp
TKey LastInorder()
```

**返回值:** `TKey`

### FirstPreorder

```csharp
TKey FirstPreorder()
```

**返回值:** `TKey`

### NextPreorder

```csharp
TKey NextPreorder(TKey i)
```

**参数:**

- `i` (`TKey`)

**返回值:** `TKey`

### LastPreorder

```csharp
TKey LastPreorder()
```

**返回值:** `TKey`

### FirstPostorder

```csharp
TKey FirstPostorder()
```

**返回值:** `TKey`

### NextPostorder

```csharp
TKey NextPostorder(TKey i)
```

**参数:**

- `i` (`TKey`)

**返回值:** `TKey`

### Reinsert

```csharp
void Reinsert(TKey i)
```

**参数:**

- `i` (`TKey`)

### IsValid

```csharp
bool IsValid()
```

**返回值:** `bool`

### SetLessFunc

```csharp
void SetLessFunc(LessFunc func)
```

**参数:**

- `func` (`LessFunc`)

### Insert

```csharp
TKey Insert(TValue val)
```

**参数:**

- `val` (`TValue`)

**返回值:** `TKey`

### InsertIfNotFound

```csharp
TKey InsertIfNotFound(TValue val)
```

**参数:**

- `val` (`TValue`)

**返回值:** `TKey`

