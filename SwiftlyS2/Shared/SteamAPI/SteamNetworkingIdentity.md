# 🏗️ SteamNetworkingIdentity

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<SteamNetworkingIdentity\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_eType` | `ESteamNetworkingIdentityType` | - | - |
| `k_cchMaxString` | `int` | const | - |
| `k_cchMaxGenericString` | `int` | const | - |
| `k_cchMaxXboxPairwiseID` | `int` | const | - |
| `k_cbMaxGenericBytes` | `int` | const | - |

## ⚙️ 方法

### Clear

```csharp
void Clear()
```

### IsInvalid

```csharp
bool IsInvalid()
```

**返回值:** `bool`

### SetSteamID

```csharp
void SetSteamID(CSteamID steamID)
```

**参数:**

- `steamID` (`CSteamID`)

### GetSteamID

```csharp
CSteamID GetSteamID()
```

**返回值:** `CSteamID`

### SetSteamID64

```csharp
void SetSteamID64(ulong steamID)
```

**参数:**

- `steamID` (`ulong`)

### GetSteamID64

```csharp
ulong GetSteamID64()
```

**返回值:** `ulong`

### SetXboxPairwiseID

```csharp
bool SetXboxPairwiseID(string pszString)
```

**参数:**

- `pszString` (`string`)

**返回值:** `bool`

### GetXboxPairwiseID

```csharp
string GetXboxPairwiseID()
```

**返回值:** `string`

### SetPSNID

```csharp
void SetPSNID(ulong id)
```

**参数:**

- `id` (`ulong`)

### GetPSNID

```csharp
ulong GetPSNID()
```

**返回值:** `ulong`

### SetStadiaID

```csharp
void SetStadiaID(ulong id)
```

**参数:**

- `id` (`ulong`)

### GetStadiaID

```csharp
ulong GetStadiaID()
```

**返回值:** `ulong`

### SetIPAddr

```csharp
void SetIPAddr(SteamNetworkingIPAddr addr)
```

**参数:**

- `addr` (`SteamNetworkingIPAddr`)

### GetIPAddr

```csharp
SteamNetworkingIPAddr GetIPAddr()
```

**返回值:** `SteamNetworkingIPAddr`

### SetIPv4Addr

```csharp
void SetIPv4Addr(uint nIPv4, ushort nPort)
```

**参数:**

- `nIPv4` (`uint`)
- `nPort` (`ushort`)

### GetIPv4

```csharp
uint GetIPv4()
```

**返回值:** `uint`

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

### SetLocalHost

```csharp
void SetLocalHost()
```

### IsLocalHost

```csharp
bool IsLocalHost()
```

**返回值:** `bool`

### SetGenericString

```csharp
bool SetGenericString(string pszString)
```

**参数:**

- `pszString` (`string`)

**返回值:** `bool`

### GetGenericString

```csharp
string GetGenericString()
```

**返回值:** `string`

### SetGenericBytes

```csharp
bool SetGenericBytes(byte[] data, uint cbLen)
```

**参数:**

- `data` (`byte[]`)
- `cbLen` (`uint`)

**返回值:** `bool`

### GetGenericBytes

```csharp
byte[] GetGenericBytes(out int cbLen)
```

**参数:**

- `cbLen` (`out int`)

**返回值:** `byte[]`

### Equals

```csharp
bool Equals(SteamNetworkingIdentity x)
```

**参数:**

- `x` (`SteamNetworkingIdentity`)

**返回值:** `bool`

### ToString

```csharp
void ToString(out string buf)
```

**参数:**

- `buf` (`out string`)

### ParseString

```csharp
bool ParseString(string pszStr)
```

**参数:**

- `pszStr` (`string`)

**返回值:** `bool`

