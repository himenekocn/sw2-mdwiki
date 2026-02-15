# 🏗️ SteamNetworkingIPAddr

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<SteamNetworkingIPAddr\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_ipv6` | `byte[]` | - | - |
| `m_port` | `ushort` | - | - |
| `k_cchMaxString` | `int` | const | - |

## ⚙️ 方法

### Clear

```csharp
void Clear()
```

### IsIPv6AllZeros

```csharp
bool IsIPv6AllZeros()
```

**返回值:** `bool`

### SetIPv6

```csharp
void SetIPv6(byte[] ipv6, ushort nPort)
```

**参数:**

- `ipv6` (`byte[]`)
- `nPort` (`ushort`)

### SetIPv4

```csharp
void SetIPv4(uint nIP, ushort nPort)
```

**参数:**

- `nIP` (`uint`)
- `nPort` (`ushort`)

### IsIPv4

```csharp
bool IsIPv4()
```

**返回值:** `bool`

### GetIPv4

```csharp
uint GetIPv4()
```

**返回值:** `uint`

### SetIPv6LocalHost

```csharp
void SetIPv6LocalHost(ushort nPort = 0)
```

**参数:**

- `nPort` (`ushort`) = `0`

### IsLocalHost

```csharp
bool IsLocalHost()
```

**返回值:** `bool`

### ToString

```csharp
void ToString(out string buf, bool bWithPort)
```

**参数:**

- `buf` (`out string`)
- `bWithPort` (`bool`)

### ParseString

```csharp
bool ParseString(string pszStr)
```

**参数:**

- `pszStr` (`string`)

**返回值:** `bool`

### Equals

```csharp
bool Equals(SteamNetworkingIPAddr x)
```

**参数:**

- `x` (`SteamNetworkingIPAddr`)

**返回值:** `bool`

### GetFakeIPType

```csharp
ESteamNetworkingFakeIPType GetFakeIPType()
```

**返回值:** `ESteamNetworkingFakeIPType`

### IsFakeIP

```csharp
bool IsFakeIP()
```

**返回值:** `bool`

