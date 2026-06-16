<a id="hsteamnetconnection"></a>

# 🏗️ HSteamNetConnection

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<HSteamNetConnection\>`

**实现接口:** `System.IComparable\<HSteamNetConnection\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_HSteamNetConnection` | `uint` | - | - |

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

### uint (静态)

```csharp
operator uint(HSteamNetConnection that)
```

**参数:**

- `that` (`HSteamNetConnection`)

**返回值:** `operator`

**用法示例:**
```csharp
uint connectionId = (uint)existingConnection;
```

### Equals

```csharp
bool Equals(HSteamNetConnection other)
```

**参数:**

- `other` (`HSteamNetConnection`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(HSteamNetConnection other)
```

**参数:**

- `other` (`HSteamNetConnection`)

**返回值:** `int`

**用法示例:**
```csharp
int result = connection.CompareTo(otherConnection);
```

