<a id="cutlrbtree-tvalue-tkey"></a>

# 🏗️ CUtlRBTree&lt;TValue, TKey&gt;

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

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `this[TKey i]` | `ref TValue` | - | - |
| `Count` | `uint` | - | - |
| `MaxElement` | `TKey` | - | - |

## ⚙️ 方法

### LessFunc

```csharp
bool LessFunc(ref TValue lhs, ref TValue rhs)
```

**参数:**

- `lhs` (`ref TValue`)
- `rhs` (`ref TValue`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = tree.LessFunc(ref itemA, ref itemB);
```

### EnsureCapacity

```csharp
void EnsureCapacity(TKey num)
```

**参数:**

- `num` (`TKey`)

**用法示例:**
```csharp
tree.EnsureCapacity(10);
```

### IsValidIndex

```csharp
bool IsValidIndex(TKey i)
```

**参数:**

- `i` (`TKey`)

**返回值:** `bool`

**用法示例:**
```csharp
bool isValid = tree.IsValidIndex(5);
```

### NewNode

```csharp
TKey NewNode()
```

**返回值:** `TKey`

**用法示例:**
```csharp
var newNodeKey = rbTree.NewNode();
```

### FreeNode

```csharp
void FreeNode(TKey i)
```

**参数:**

- `i` (`TKey`)

**用法示例:**
```csharp
tree.FreeNode(key);
```

### RotateLeft

```csharp
void RotateLeft(TKey elem)
```

**参数:**

- `elem` (`TKey`)

**用法示例:**
```csharp
tree.RotateLeft(elem);
```

### RotateRight

```csharp
void RotateRight(TKey elem)
```

**参数:**

- `elem` (`TKey`)

**用法示例:**
```csharp
tree.RotateRight(elem);
```

### InsertRebalance

```csharp
void InsertRebalance(TKey elem)
```

**参数:**

- `elem` (`TKey`)

**用法示例:**
```csharp
tree.InsertRebalance(elem);
```

### LinkToParent

```csharp
void LinkToParent(TKey i, TKey parent, bool isLeft)
```

**参数:**

- `i` (`TKey`)
- `parent` (`TKey`)
- `isLeft` (`bool`)

**用法示例:**
```csharp
tree.LinkToParent(childKey, parentKey, true);
```

### InsertAt

```csharp
TKey InsertAt(TKey parent, bool leftchild)
```

**参数:**

- `parent` (`TKey`)
- `leftchild` (`bool`)

**返回值:** `TKey`

**用法示例:**
```csharp
var newNode = rbTree.InsertAt(existingKey, true);
```

### RemoveRebalance

```csharp
void RemoveRebalance(TKey elem)
```

**参数:**

- `elem` (`TKey`)

**用法示例:**
```csharp
tree.RemoveRebalance(elem);
```

### Unlink

```csharp
void Unlink(TKey elem)
```

**参数:**

- `elem` (`TKey`)

**用法示例:**
```csharp
tree.Unlink(elem);
```

### Link

```csharp
void Link(TKey elem)
```

**参数:**

- `elem` (`TKey`)

**用法示例:**
```csharp
tree.Link(elem);
```

### FindInsertionPosition

```csharp
void FindInsertionPosition(TValue val, out TKey parent, out bool leftchild)
```

**参数:**

- `val` (`TValue`)
- `parent` (`out TKey`)
- `leftchild` (`out bool`)

**用法示例:**
```csharp
tree.FindInsertionPosition(val, out parent, out leftchild);
```

### RemoveAt

```csharp
void RemoveAt(TKey elem)
```

**参数:**

- `elem` (`TKey`)

**用法示例:**
```csharp
tree.RemoveAt(elem);
```

### Remove

```csharp
bool Remove(TValue value)
```

**参数:**

- `value` (`TValue`)

**返回值:** `bool`

**用法示例:**
```csharp
tree.Remove(value);
```

### Find

```csharp
TKey Find(TValue value)
```

**参数:**

- `value` (`TValue`)

**返回值:** `TKey`

**用法示例:**
```csharp
var key = tree.Find(value);
```

### RemoveAll

```csharp
void RemoveAll()
```

**用法示例:**
```csharp
existingTree.RemoveAll();
```

### Purge

```csharp
void Purge()
```

**用法示例:**
```csharp
tree.Purge();
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

**用法示例:**
```csharp
TKey firstKey = rbTree.FirstInorder();
```

### NextInorder

```csharp
TKey NextInorder(TKey i)
```

**参数:**

- `i` (`TKey`)

**返回值:** `TKey`

**用法示例:**
```csharp
var nextKey = rbTree.NextInorder(currentKey);
```

### PrevInorder

```csharp
TKey PrevInorder(TKey i)
```

**参数:**

- `i` (`TKey`)

**返回值:** `TKey`

**用法示例:**
```csharp
TKey previous = rbTree.PrevInorder(currentKey);
```

### LastInorder

```csharp
TKey LastInorder()
```

**返回值:** `TKey`

**用法示例:**
```csharp
TKey lastKey = rbTree.LastInorder();
```

### FirstPreorder

```csharp
TKey FirstPreorder()
```

**返回值:** `TKey`

**用法示例:**
```csharp
var firstKey = rbTree.FirstPreorder();
```

### NextPreorder

```csharp
TKey NextPreorder(TKey i)
```

**参数:**

- `i` (`TKey`)

**返回值:** `TKey`

**用法示例:**
```csharp
TKey nextNode = rbTree.NextPreorder(currentNode);
```

### LastPreorder

```csharp
TKey LastPreorder()
```

**返回值:** `TKey`

**用法示例:**
```csharp
var lastKey = rbTree.LastPreorder();
```

### FirstPostorder

```csharp
TKey FirstPostorder()
```

**返回值:** `TKey`

**用法示例:**
```csharp
var first = rbTree.FirstPostorder();
```

### NextPostorder

```csharp
TKey NextPostorder(TKey i)
```

**参数:**

- `i` (`TKey`)

**返回值:** `TKey`

**用法示例:**
```csharp
TKey nextNode = rbTree.NextPostorder(currentNode);
```

### Reinsert

```csharp
void Reinsert(TKey i)
```

**参数:**

- `i` (`TKey`)

**用法示例:**
```csharp
tree.Reinsert(i);
```

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

**用法示例:**
```csharp
tree.SetLessFunc((x, y) => x < y);
```

### Insert

```csharp
TKey Insert(TValue val)
```

**参数:**

- `val` (`TValue`)

**返回值:** `TKey`

**用法示例:**
```csharp
TKey key = rbTree.Insert(val);
```

### InsertIfNotFound

```csharp
TKey InsertIfNotFound(TValue val)
```

**参数:**

- `val` (`TValue`)

**返回值:** `TKey`

**用法示例:**
```csharp
TKey key = tree.InsertIfNotFound(val);
```

