# 🏗️ PublishedFileUpdateHandle_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<PublishedFileUpdateHandle_t\>`

**实现接口:** `System.IComparable\<PublishedFileUpdateHandle_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_PublishedFileUpdateHandle` | `ulong` | - | - |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

**用法示例:**
```csharp
PublishedFileUpdateHandle_t handle = PublishedFileUpdateHandle_t.Invalid;  
Console.WriteLine(handle.ToString());
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
operator ulong(PublishedFileUpdateHandle_t that)
```

**参数:**

- `that` (`PublishedFileUpdateHandle_t`)

**返回值:** `operator`

**用法示例:**
```csharp
PublishedFileUpdateHandle_t handle = default;
ulong value = (ulong)handle;
```

### Equals

```csharp
bool Equals(PublishedFileUpdateHandle_t other)
```

**参数:**

- `other` (`PublishedFileUpdateHandle_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(PublishedFileUpdateHandle_t other)
```

**参数:**

- `other` (`PublishedFileUpdateHandle_t`)

**返回值:** `int`

**用法示例:**
```csharp
PublishedFileUpdateHandle_t handle1 = default;  
int result = handle1.CompareTo(handle2);
```

