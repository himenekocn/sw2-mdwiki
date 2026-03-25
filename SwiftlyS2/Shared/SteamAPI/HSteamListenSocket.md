# 🏗️ HSteamListenSocket

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<HSteamListenSocket\>`

**实现接口:** `System.IComparable\<HSteamListenSocket\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_HSteamListenSocket` | `uint` | - | - |

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
operator uint(HSteamListenSocket that)
```

**参数:**

- `that` (`HSteamListenSocket`)

**返回值:** `operator`

**用法示例:**
```csharp
uint socketId = HSteamListenSocket.uint(existingSocket);
```

### Equals

```csharp
bool Equals(HSteamListenSocket other)
```

**参数:**

- `other` (`HSteamListenSocket`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(HSteamListenSocket other)
```

**参数:**

- `other` (`HSteamListenSocket`)

**返回值:** `int`

**用法示例:**
```csharp
int result = existingSocket.CompareTo(otherSocket);
```

