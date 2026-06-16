<a id="steamnetworkingidentity"></a>

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

**用法示例:**
```csharp
identity.Clear();
```

### IsInvalid

```csharp
bool IsInvalid()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isInvalid = identity.IsInvalid();
```

### SetSteamID

```csharp
void SetSteamID(CSteamID steamID)
```

**参数:**

- `steamID` (`CSteamID`)

**用法示例:**
```csharp
identity.SetSteamID(steamID);
```

### GetSteamID

```csharp
CSteamID GetSteamID()
```

**返回值:** `CSteamID`

**用法示例:**
```csharp
CSteamID steamId = identity.GetSteamID();
```

### SetSteamID64

```csharp
void SetSteamID64(ulong steamID)
```

**参数:**

- `steamID` (`ulong`)

**用法示例:**
```csharp
identity.SetSteamID64(76561198000000000UL);
```

### GetSteamID64

```csharp
ulong GetSteamID64()
```

**返回值:** `ulong`

**用法示例:**
```csharp
ulong steamId = identity.GetSteamID64();
```

### SetXboxPairwiseID

```csharp
bool SetXboxPairwiseID(string pszString)
```

**参数:**

- `pszString` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
identity.SetXboxPairwiseID("xbox_pairwise_id_string");
```

### GetXboxPairwiseID

```csharp
string GetXboxPairwiseID()
```

**返回值:** `string`

**用法示例:**
```csharp
string xboxId = identity.GetXboxPairwiseID();
```

### SetPSNID

```csharp
void SetPSNID(ulong id)
```

**参数:**

- `id` (`ulong`)

**用法示例:**
```csharp
identity.SetPSNID(12345678901234567890);
```

### GetPSNID

```csharp
ulong GetPSNID()
```

**返回值:** `ulong`

**用法示例:**
```csharp
ulong psnId = identity.GetPSNID();
```

### SetStadiaID

```csharp
void SetStadiaID(ulong id)
```

**参数:**

- `id` (`ulong`)

**用法示例:**
```csharp
identity.SetStadiaID(1234567890UL);
```

### GetStadiaID

```csharp
ulong GetStadiaID()
```

**返回值:** `ulong`

**用法示例:**
```csharp
ulong stadiaId = identity.GetStadiaID();
```

### SetIPAddr

```csharp
void SetIPAddr(SteamNetworkingIPAddr addr)
```

**参数:**

- `addr` (`SteamNetworkingIPAddr`)

**用法示例:**
```csharp
identity.SetIPAddr(addr);
```

### GetIPAddr

```csharp
SteamNetworkingIPAddr GetIPAddr()
```

**返回值:** `SteamNetworkingIPAddr`

**用法示例:**
```csharp
var ipAddr = identity.GetIPAddr();
```

### SetIPv4Addr

```csharp
void SetIPv4Addr(uint nIPv4, ushort nPort)
```

**参数:**

- `nIPv4` (`uint`)
- `nPort` (`ushort`)

**用法示例:**
```csharp
identity.SetIPv4Addr(0x7F000001, 27015);
```

### GetIPv4

```csharp
uint GetIPv4()
```

**返回值:** `uint`

**用法示例:**
```csharp
uint ip = identity.GetIPv4();
```

### GetFakeIPType

```csharp
ESteamNetworkingFakeIPType GetFakeIPType()
```

**返回值:** `ESteamNetworkingFakeIPType`

**用法示例:**
```csharp
ESteamNetworkingFakeIPType type = identity.GetFakeIPType();
```

### IsFakeIP

```csharp
bool IsFakeIP()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isFake = identity.IsFakeIP();
```

### SetLocalHost

```csharp
void SetLocalHost()
```

**用法示例:**
```csharp
identity.SetLocalHost();
```

### IsLocalHost

```csharp
bool IsLocalHost()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isLocal = identity.IsLocalHost();
```

### SetGenericString

```csharp
bool SetGenericString(string pszString)
```

**参数:**

- `pszString` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
identity.SetGenericString("MyCustomIdentity");
```

### GetGenericString

```csharp
string GetGenericString()
```

**返回值:** `string`

**用法示例:**
```csharp
string identityString = existingIdentity.GetGenericString();
```

### SetGenericBytes

```csharp
bool SetGenericBytes(byte[] data, uint cbLen)
```

**参数:**

- `data` (`byte[]`)
- `cbLen` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
identity.SetGenericBytes(new byte[] { 1, 2, 3 }, 3);
```

### GetGenericBytes

```csharp
byte[] GetGenericBytes(out int cbLen)
```

**参数:**

- `cbLen` (`out int`)

**返回值:** `byte[]`

**用法示例:**
```csharp
byte[] data = identity.GetGenericBytes(out int cbLen);
```

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

**用法示例:**
```csharp
identity.ParseString("[U:1:123456]");
```

