<a id="ugcfilewritestreamhandle_t"></a>

# 🏗️ UGCFileWriteStreamHandle_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<UGCFileWriteStreamHandle_t\>`

**实现接口:** `System.IComparable\<UGCFileWriteStreamHandle_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_UGCFileWriteStreamHandle` | `ulong` | - | - |

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
operator ulong(UGCFileWriteStreamHandle_t that)
```

**参数:**

- `that` (`UGCFileWriteStreamHandle_t`)

**返回值:** `operator`

**用法示例:**
```csharp
ulong handleValue = (ulong)existingStreamHandle;
```

### Equals

```csharp
bool Equals(UGCFileWriteStreamHandle_t other)
```

**参数:**

- `other` (`UGCFileWriteStreamHandle_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(UGCFileWriteStreamHandle_t other)
```

**参数:**

- `other` (`UGCFileWriteStreamHandle_t`)

**返回值:** `int`

**用法示例:**
```csharp
int result = handle.CompareTo(otherHandle);
```

