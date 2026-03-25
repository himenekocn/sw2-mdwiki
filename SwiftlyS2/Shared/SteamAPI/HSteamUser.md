# 🏗️ HSteamUser

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<HSteamUser\>`

**实现接口:** `System.IComparable\<HSteamUser\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_HSteamUser` | `int` | - | - |

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

### int (静态)

```csharp
operator int(HSteamUser that)
```

**参数:**

- `that` (`HSteamUser`)

**返回值:** `operator`

**用法示例:**
```csharp
int userId = HSteamUser.int(existingUser);
```

### Equals

```csharp
bool Equals(HSteamUser other)
```

**参数:**

- `other` (`HSteamUser`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(HSteamUser other)
```

**参数:**

- `other` (`HSteamUser`)

**返回值:** `int`

**用法示例:**
```csharp
int result = user.CompareTo(otherUser);
```

