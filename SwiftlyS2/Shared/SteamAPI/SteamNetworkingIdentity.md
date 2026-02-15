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
SteamNetworkingIdentity identity;
identity.Clear();
```

### IsInvalid

```csharp
bool IsInvalid()
```

**返回值:** `bool`

**用法示例:**
```csharp
SteamNetworkingIdentity identity;  
bool invalid = identity.IsInvalid();
```

### SetSteamID

```csharp
void SetSteamID(CSteamID steamID)
```

**参数:**

- `steamID` (`CSteamID`)

**用法示例:**
```csharp
SteamNetworkingIdentity identity;  
identity.SetSteamID(CSteamID(12345));
```

### GetSteamID

```csharp
CSteamID GetSteamID()
```

**返回值:** `CSteamID`

**用法示例:**
```csharp
SteamNetworkingIdentity identity;  
CSteamID id = identity.GetSteamID();
```

### SetSteamID64

```csharp
void SetSteamID64(ulong steamID)
```

**参数:**

- `steamID` (`ulong`)

**用法示例:**
```csharp
SteamNetworkingIdentity identity;  
identity.SetSteamID64(123456789UL);
```

### GetSteamID64

```csharp
ulong GetSteamID64()
```

**返回值:** `ulong`

**用法示例:**
```csharp
SteamNetworkingIdentity identity = SteamGameServer.GetPlayerIdentity(playerIndex);
ulong steamID64 = identity.GetSteamID64();
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
SteamNetworkingIdentity identity;  
identity.SetXboxPairwiseID("123456789");
```

### GetXboxPairwiseID

```csharp
string GetXboxPairwiseID()
```

**返回值:** `string`

**用法示例:**
```csharp
string pairId = SteamNetworkingIdentity.GetXboxPairwiseID();
```

### SetPSNID

```csharp
void SetPSNID(ulong id)
```

**参数:**

- `id` (`ulong`)

**用法示例:**
```csharp
SteamNetworkingIdentity identity;  
identity.SetPSNID(1234567890UL);
```

### GetPSNID

```csharp
ulong GetPSNID()
```

**返回值:** `ulong`

**用法示例:**
```csharp
ulong psnId = SteamNetworkingIdentity.GetPSNID();
```

### SetStadiaID

```csharp
void SetStadiaID(ulong id)
```

**参数:**

- `id` (`ulong`)

**用法示例:**
```csharp
SteamNetworkingIdentity identity;  
identity.SetStadiaID(123456789);
```

### GetStadiaID

```csharp
ulong GetStadiaID()
```

**返回值:** `ulong`

**用法示例:**
```csharp
ulong stadiaId = someSteamNetworkingIdentity.GetStadiaID();
```

### SetIPAddr

```csharp
void SetIPAddr(SteamNetworkingIPAddr addr)
```

**参数:**

- `addr` (`SteamNetworkingIPAddr`)

**用法示例:**
```csharp
SteamNetworkingIdentity identity;  
identity.SetIPAddr(default(SteamNetworkingIPAddr));
```

### GetIPAddr

```csharp
SteamNetworkingIPAddr GetIPAddr()
```

**返回值:** `SteamNetworkingIPAddr`

**用法示例:**
```csharp
SteamNetworkingIPAddr ip = identity.GetIPAddr();
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
SteamNetworkingIdentity identity;  
identity.SetIPv4Addr(0x7F000001, 8080);
```

### GetIPv4

```csharp
uint GetIPv4()
```

**返回值:** `uint`

**用法示例:**
```csharp
uint ip = SteamNetworkingIdentity.GetIPv4();
```

### GetFakeIPType

```csharp
ESteamNetworkingFakeIPType GetFakeIPType()
```

**返回值:** `ESteamNetworkingFakeIPType`

**用法示例:**
```csharp
SteamNetworkingFakeIPType fakeIPType = identity.GetFakeIPType();
```

### IsFakeIP

```csharp
bool IsFakeIP()
```

**返回值:** `bool`

**用法示例:**
```csharp
SteamNetworkingIdentity identity = SteamClient.GetLocalPlayer().GetSteamId();  
bool isFake = identity.IsFakeIP();
```

### SetLocalHost

```csharp
void SetLocalHost()
```

**用法示例:**
```csharp
SteamNetworkingIdentity identity = default;
identity.SetLocalHost();
```

### IsLocalHost

```csharp
bool IsLocalHost()
```

**返回值:** `bool`

**用法示例:**
```csharp
SteamNetworkingIdentity identity = SteamNetworkingMessages.GetIdentity();  
bool isLocalHost = identity.IsLocalHost();
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
SteamNetworkingIdentity id;  
id.SetGenericString("player123");
```

### GetGenericString

```csharp
string GetGenericString()
```

**返回值:** `string`

**用法示例:**
```csharp
string idStr = SteamNetworkingIdentity.GetGenericString();
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
SteamNetworkingIdentity identity;  
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
SteamNetworkingIdentity identity; // 已有实例  
byte[] bytes = identity.GetGenericBytes(out int len);
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

**用法示例:**
```csharp
string buf;
SteamNetworkingIdentity identity = SteamNetworkingIdentity.GetLocal();
identity.ToString(out buf);
```

### ParseString

```csharp
bool ParseString(string pszStr)
```

**参数:**

- `pszStr` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamNetworkingIdentity id;  
id.ParseString("steam:123456789");
```

