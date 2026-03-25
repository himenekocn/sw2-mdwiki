# 🏗️ UGCHandle_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<UGCHandle_t\>`

**实现接口:** `System.IComparable\<UGCHandle_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_UGCHandle` | `ulong` | - | - |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

### Equals

```csharp
bool Equals(object other)
```

**参数:**

- `other` (`object`)

**返回值:** `bool`

### GetHashCode

```csharp
int GetHashCode()
```

**返回值:** `int`

### ulong (静态)

```csharp
operator ulong(UGCHandle_t that)
```

**参数:**

- `that` (`UGCHandle_t`)

**返回值:** `operator`

**用法示例:**
```csharp
ulong handleValue = UGCHandle_t.operator ulong(existingHandle);
```

### Equals

```csharp
bool Equals(UGCHandle_t other)
```

**参数:**

- `other` (`UGCHandle_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(UGCHandle_t other)
```

**参数:**

- `other` (`UGCHandle_t`)

**返回值:** `int`

**用法示例:**
```csharp
int result = handleA.CompareTo(handleB);
```

