# 🏗️ SteamNetworkingPOPID

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<SteamNetworkingPOPID\>`

**实现接口:** `System.IComparable\<SteamNetworkingPOPID\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_SteamNetworkingPOPID` | `uint` | - | - |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

**用法示例:**
```csharp
SteamNetworkingPOPID popid = SteamNetworkingPOPID.Invalid;
string result = popid.ToString();
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

### uint (静态)

```csharp
operator uint(SteamNetworkingPOPID that)
```

**参数:**

- `that` (`SteamNetworkingPOPID`)

**返回值:** `operator`

**用法示例:**
```csharp
uint id = (uint)SteamNetworkingPOPID.k_ESteamNetworkingPOPID_Invalid;
```

### Equals

```csharp
bool Equals(SteamNetworkingPOPID other)
```

**参数:**

- `other` (`SteamNetworkingPOPID`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(SteamNetworkingPOPID other)
```

**参数:**

- `other` (`SteamNetworkingPOPID`)

**返回值:** `int`

**用法示例:**
```csharp
SteamNetworkingPOPID popid1 = SteamNetworkingPOPID.Invalid;  
int result = popid1.CompareTo(SteamNetworkingPOPID.LocalHost);
```

