# 🏗️ PublishedFileId_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<PublishedFileId_t\>`

**实现接口:** `System.IComparable\<PublishedFileId_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_PublishedFileId` | `ulong` | - | - |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

**用法示例:**
```csharp
PublishedFileId_t id = PublishedFileId_t.Invalid;  
string str = id.ToString();
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
operator ulong(PublishedFileId_t that)
```

**参数:**

- `that` (`PublishedFileId_t`)

**返回值:** `operator`

**用法示例:**
```csharp
PublishedFileId_t file = (PublishedFileId_t)12345UL;
```

### Equals

```csharp
bool Equals(PublishedFileId_t other)
```

**参数:**

- `other` (`PublishedFileId_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(PublishedFileId_t other)
```

**参数:**

- `other` (`PublishedFileId_t`)

**返回值:** `int`

**用法示例:**
```csharp
PublishedFileId_t id1 = PublishedFileId_t.Invalid;  
int result = id1.CompareTo(PublishedFileId_t.Invalid);
```

