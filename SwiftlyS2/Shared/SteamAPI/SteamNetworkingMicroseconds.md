# 🏗️ SteamNetworkingMicroseconds

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<SteamNetworkingMicroseconds\>`

**实现接口:** `System.IComparable\<SteamNetworkingMicroseconds\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_SteamNetworkingMicroseconds` | `long` | - | - |

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

### long (静态)

```csharp
operator long(SteamNetworkingMicroseconds that)
```

**参数:**

- `that` (`SteamNetworkingMicroseconds`)

**返回值:** `operator`

**用法示例:**
```csharp
long microseconds = (long)SteamNetworkingMicroseconds.FromSeconds(1.5);
```

### Equals

```csharp
bool Equals(SteamNetworkingMicroseconds other)
```

**参数:**

- `other` (`SteamNetworkingMicroseconds`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(SteamNetworkingMicroseconds other)
```

**参数:**

- `other` (`SteamNetworkingMicroseconds`)

**返回值:** `int`

**用法示例:**
```csharp
int result = existingMicroseconds.CompareTo(otherMicroseconds);
```

