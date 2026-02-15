# 🏗️ CUtlMap

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

**继承:** `IDisposable
    where TIndex : unmanaged`

**实现接口:** `IBinaryInteger\<TIndex\>`, `IMinMaxValue\<TIndex\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `MaxElement` | `TIndex` | - | - |

## ⚙️ 方法

### EnsureCapacity

```csharp
void EnsureCapacity(TIndex num)
```

**参数:**

- `num` (`TIndex`)

### SetLessFunc

```csharp
void SetLessFunc(CUtlRBTree<CUtlMapTreeNode<TKey, TValue>, TIndex>.LessFunc func)
```

**参数:**

- `func` (`CUtlRBTree\<CUtlMapTreeNode\<TKey, TValue\>, TIndex\>.LessFunc`)

### Insert

```csharp
TIndex Insert(TKey key, TValue element)
```

**参数:**

- `key` (`TKey`)
- `element` (`TValue`)

**返回值:** `TIndex`

### Insert

```csharp
TIndex Insert(TKey key)
```

**参数:**

- `key` (`TKey`)

**返回值:** `TIndex`

### Find

```csharp
TIndex Find(TKey key)
```

**参数:**

- `key` (`TKey`)

**返回值:** `TIndex`

### Remove

```csharp
bool Remove(TKey key)
```

**参数:**

- `key` (`TKey`)

**返回值:** `bool`

### Reinsert

```csharp
void Reinsert(TKey key, TIndex idx)
```

**参数:**

- `key` (`TKey`)
- `idx` (`TIndex`)

### InsertOrReplace

```csharp
TIndex InsertOrReplace(TKey key, TValue element)
```

**参数:**

- `key` (`TKey`)
- `element` (`TValue`)

**返回值:** `TIndex`

### Dispose

```csharp
void Dispose()
```

