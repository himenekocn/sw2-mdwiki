# 🏗️ SteamLeaderboardEntries_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<SteamLeaderboardEntries_t\>`

**实现接口:** `System.IComparable\<SteamLeaderboardEntries_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_SteamLeaderboardEntries` | `ulong` | - | - |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

**用法示例:**
```csharp
string result = SteamLeaderboardEntries_t.ToString();
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
operator ulong(SteamLeaderboardEntries_t that)
```

**参数:**

- `that` (`SteamLeaderboardEntries_t`)

**返回值:** `operator`

**用法示例:**
```csharp
SteamLeaderboardEntries_t.operator_ulong(leaderboardEntries);
```

### Equals

```csharp
bool Equals(SteamLeaderboardEntries_t other)
```

**参数:**

- `other` (`SteamLeaderboardEntries_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(SteamLeaderboardEntries_t other)
```

**参数:**

- `other` (`SteamLeaderboardEntries_t`)

**返回值:** `int`

**用法示例:**
```csharp
SteamLeaderboardEntries_t a = default; SteamLeaderboardEntries_t b = default; int result = a.CompareTo(b);
```

