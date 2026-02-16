# 🏗️ CUtlRBTree<TValue, TKey>

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
CUtlRBTree.LessFunc(ref lhsValue, ref rhsValue);
```

### EnsureCapacity

```csharp
void EnsureCapacity(TKey num)
```

**参数:**

- `num` (`TKey`)

**用法示例:**
```csharp
CUtlRBTree<int> tree;  
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
bool valid = manager.IsValidIndex(0);
```

### NewNode

```csharp
TKey NewNode()
```

**返回值:** `TKey`

**用法示例:**
```csharp
CUtlRBTree<int> tree;  
int node = tree.NewNode();
```

### FreeNode

```csharp
void FreeNode(TKey i)
```

**参数:**

- `i` (`TKey`)

**用法示例:**
```csharp
CUtlRBTree<int> tree;
tree.FreeNode(42);
```

### RotateLeft

```csharp
void RotateLeft(TKey elem)
```

**参数:**

- `elem` (`TKey`)

**用法示例:**
```csharp
// 假设已存在 CUtlRBTree 实例 tree 和元素 elem  
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
CUtlRBTree tree = GetExistingTree();  
tree.RotateRight(someKey);
```

### InsertRebalance

```csharp
void InsertRebalance(TKey elem)
```

**参数:**

- `elem` (`TKey`)

**用法示例:**
```csharp
// 假设已存在 CUtlRBTree 实例 tree 和 TKey 类型的 elem 变量  
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
// 假设已存在 CUtlRBTree 实例 tree 和有效键值 i、parent
tree.LinkToParent(i, parent, true);
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
// 假设已存在 CUtlRBTree 实例 tree 和有效 parent 节点引用
tree.InsertAt(parentNode, true);
```

### RemoveRebalance

```csharp
void RemoveRebalance(TKey elem)
```

**参数:**

- `elem` (`TKey`)

**用法示例:**
```csharp
// 假设已存在 CUtlRBTree 实例 tree 和元素 elem
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
CUtlRBTree<int> tree = GetExistingTree();  
tree.Unlink(42);
```

### Link

```csharp
void Link(TKey elem)
```

**参数:**

- `elem` (`TKey`)

**用法示例:**
```csharp
CUtlRBTree tree;
tree.Link(someKey);
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
CUtlRBTree<int, string> tree;  
tree.FindInsertionPosition(42, out int parent, out bool leftchild);
```

### RemoveAt

```csharp
void RemoveAt(TKey elem)
```

**参数:**

- `elem` (`TKey`)

**用法示例:**
```csharp
CUtlRBTree<int> tree;
tree.RemoveAt(42);
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
CUtlRBTree<int> tree = GetExistingTree();  
tree.Remove(42);
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
// 假设已存在 CUtlRBTree 实例 tree 和 TValue 类型的 value 变量  
TKey key = tree.Find(value);
```

### RemoveAll

```csharp
void RemoveAll()
```

**用法示例:**
```csharp
CUtlRBTree<int> tree;
tree.RemoveAll();
```

### Purge

```csharp
void Purge()
```

**用法示例:**
```csharp
CUtlRBTree<int> tree = default;
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
var first = myTree.FirstInorder();
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
TKey next = tree.NextInorder(currentKey);
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
var prev = tree.PrevInorder(currentKey);
```

### LastInorder

```csharp
TKey LastInorder()
```

**返回值:** `TKey`

**用法示例:**
```csharp
var last = tree.LastInorder();
```

### FirstPreorder

```csharp
TKey FirstPreorder()
```

**返回值:** `TKey`

**用法示例:**
```csharp
TKey first = tree.FirstPreorder();
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
TKey next = tree.NextPreorder(currentKey);
```

### LastPreorder

```csharp
TKey LastPreorder()
```

**返回值:** `TKey`

**用法示例:**
```csharp
// 假设 tree 是 CUtlRBTree 的一个实例  
var last = tree.LastPreorder();
```

### FirstPostorder

```csharp
TKey FirstPostorder()
```

**返回值:** `TKey`

**用法示例:**
```csharp
TKey first = tree.FirstPostorder();
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
TKey next = tree.NextPostorder(currentKey);
```

### Reinsert

```csharp
void Reinsert(TKey i)
```

**参数:**

- `i` (`TKey`)

**用法示例:**
```csharp
manager.Reinsert(xxx);
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
void SetLessFunc(LessFunc func) { /* 示例：manager.SetLessFunc(CompareScores); */ }
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
CUtlRBTree<int, string> tree;
tree.Insert("hello");
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
CUtlRBTree<int, string> tree;
tree.InsertIfNotFound("hello");
```

