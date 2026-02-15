# 🏗️ UGCQueryHandle_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<UGCQueryHandle_t\>`

**实现接口:** `System.IComparable\<UGCQueryHandle_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_UGCQueryHandle` | `ulong` | - | - |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

**用法示例:**
```csharp
string result = UGCQueryHandle_t.Invalid.ToString();
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
operator ulong(UGCQueryHandle_t that)
```

**参数:**

- `that` (`UGCQueryHandle_t`)

**返回值:** `operator`

**用法示例:**
```csharp
ulong handle = (UGCQueryHandle_t)someUGCQueryHandle;
```

### Equals

```csharp
bool Equals(UGCQueryHandle_t other)
```

**参数:**

- `other` (`UGCQueryHandle_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(UGCQueryHandle_t other)
```

**参数:**

- `other` (`UGCQueryHandle_t`)

**返回值:** `int`

**用法示例:**
```csharp
UGCQueryHandle_t handle1 = UGCQueryHandle_t.Invalid;  
UGCQueryHandle_t handle2 = UGCQueryHandle_t.Invalid;  
int result = handle1.CompareTo(handle2);
```

