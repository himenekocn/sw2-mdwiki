# 🏗️ CUtlMap<TKey, TValue, TIndex>

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

**继承:** `IDisposable
    where TIndex : unmanaged`

**实现接口:** `IBinaryInteger\<TIndex\>`, `IMinMaxValue\<TIndex\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `MaxElement` | `TIndex` | - | - |

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `this[TIndex idx]` | `ref TValue` | - | - |
| `Count` | `int` | - | - |
| `MaxElement` | `TIndex` | - | - |

## ⚙️ 方法

### EnsureCapacity

```csharp
void EnsureCapacity(TIndex num)
```

**参数:**

- `num` (`TIndex`)

**用法示例:**
```csharp
map.EnsureCapacity(10);
```

### Find

```csharp
TIndex Find(TKey key)
```

**参数:**

- `key` (`TKey`)

**返回值:** `TIndex`

**用法示例:**
```csharp
var index = existingUtlMap.Find(existingKey);
```

### Remove

```csharp
bool Remove(TKey key)
```

**参数:**

- `key` (`TKey`)

**返回值:** `bool`

**用法示例:**
```csharp
bool removed = map.Remove(key);
```

### Reinsert

```csharp
void Reinsert(TKey key, TIndex idx)
```

**参数:**

- `key` (`TKey`)
- `idx` (`TIndex`)

**用法示例:**
```csharp
map.Reinsert(key, idx);
```

### InsertOrReplace

```csharp
TIndex InsertOrReplace(TKey key, TValue element)
```

**参数:**

- `key` (`TKey`)
- `element` (`TValue`)

**返回值:** `TIndex`

**用法示例:**
```csharp
TIndex index = existingMap.InsertOrReplace(existingKey, existingValue);
```

### Dispose

```csharp
void Dispose()
```

