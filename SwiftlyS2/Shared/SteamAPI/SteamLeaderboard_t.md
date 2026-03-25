<a id="steamleaderboard_t"></a>

# 🏗️ SteamLeaderboard_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<SteamLeaderboard_t\>`

**实现接口:** `System.IComparable\<SteamLeaderboard_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_SteamLeaderboard` | `ulong` | - | - |

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
operator ulong(SteamLeaderboard_t that)
```

**参数:**

- `that` (`SteamLeaderboard_t`)

**返回值:** `operator`

**用法示例:**
```csharp
ulong leaderboardId = (ulong)existingLeaderboard;
```

### Equals

```csharp
bool Equals(SteamLeaderboard_t other)
```

**参数:**

- `other` (`SteamLeaderboard_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(SteamLeaderboard_t other)
```

**参数:**

- `other` (`SteamLeaderboard_t`)

**返回值:** `int`

**用法示例:**
```csharp
int result = leaderboard.CompareTo(otherLeaderboard);
```

