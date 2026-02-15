# 🏗️ UGCUpdateHandle_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<UGCUpdateHandle_t\>`

**实现接口:** `System.IComparable\<UGCUpdateHandle_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_UGCUpdateHandle` | `ulong` | - | - |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

**用法示例:**
```csharp
string result = UGCUpdateHandle_t.Invalid.ToString();
```

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
operator ulong(UGCUpdateHandle_t that)
```

**参数:**

- `that` (`UGCUpdateHandle_t`)

**返回值:** `operator`

**用法示例:**
```csharp
ulong handle = UGCUpdateHandle_t.operator_ulong(existingHandle);
```

### Equals

```csharp
bool Equals(UGCUpdateHandle_t other)
```

**参数:**

- `other` (`UGCUpdateHandle_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(UGCUpdateHandle_t other)
```

**参数:**

- `other` (`UGCUpdateHandle_t`)

**返回值:** `int`

**用法示例:**
```csharp
int result = handle1.CompareTo(handle2);
```

