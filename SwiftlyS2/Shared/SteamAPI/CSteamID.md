<a id="csteamid"></a>

# 🏗️ CSteamID

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `IEquatable\<CSteamID\>`

**实现接口:** `IComparable\<CSteamID\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_SteamID` | `ulong` | - | - |

## ⚙️ 方法

### AccountID_t (静态)

```csharp
new AccountID_t( 0)
```

**参数:**

- `0` (``)

**返回值:** `new`

**用法示例:**
```csharp
var accountId = new AccountID_t(0);
```

### AccountID_t (静态)

```csharp
new AccountID_t( 0)
```

**参数:**

- `0` (``)

**返回值:** `new`

**用法示例:**
```csharp
var accountId = new AccountID_t(0);
```

### AccountID_t (静态)

```csharp
new AccountID_t( 1)
```

**参数:**

- `1` (``)

**返回值:** `new`

**用法示例:**
```csharp
var accountId = CSteamID.AccountID_t(1);
```

### AccountID_t (静态)

```csharp
new AccountID_t( 2)
```

**参数:**

- `2` (``)

**返回值:** `new`

**用法示例:**
```csharp
var accountId = CSteamID.AccountID_t(2);
```

### Set

```csharp
void Set(AccountID_t unAccountID, EUniverse eUniverse, EAccountType eAccountType)
```

**参数:**

- `unAccountID` (`AccountID_t`)
- `eUniverse` (`EUniverse`)
- `eAccountType` (`EAccountType`)

**用法示例:**
```csharp
steamID.Set(new AccountID_t(12345), EUniverse.Public, EAccountType.Individual);
```

### InstancedSet

```csharp
void InstancedSet(AccountID_t unAccountID, uint unInstance, EUniverse eUniverse, EAccountType eAccountType)
```

**参数:**

- `unAccountID` (`AccountID_t`)
- `unInstance` (`uint`)
- `eUniverse` (`EUniverse`)
- `eAccountType` (`EAccountType`)

**用法示例:**
```csharp
steamId.InstancedSet(new AccountID_t(12345), 1, EUniverse.Public, EAccountType.Individual);
```

### Clear

```csharp
void Clear()
```

**用法示例:**
```csharp
steamId.Clear();
```

### CreateBlankAnonLogon

```csharp
void CreateBlankAnonLogon(EUniverse eUniverse)
```

**参数:**

- `eUniverse` (`EUniverse`)

**用法示例:**
```csharp
steamID.CreateBlankAnonLogon(EUniverse.Public);
```

### CreateBlankAnonUserLogon

```csharp
void CreateBlankAnonUserLogon(EUniverse eUniverse)
```

**参数:**

- `eUniverse` (`EUniverse`)

**用法示例:**
```csharp
steamID.CreateBlankAnonUserLogon(EUniverse.Public);
```

### BBlankAnonAccount

```csharp
bool BBlankAnonAccount()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isBlank = steamId.BBlankAnonAccount();
```

### BGameServerAccount

```csharp
bool BGameServerAccount()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isGameServer = steamID.BGameServerAccount();
```

### BPersistentGameServerAccount

```csharp
bool BPersistentGameServerAccount()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isPersistent = steamID.BPersistentGameServerAccount();
```

### BAnonGameServerAccount

```csharp
bool BAnonGameServerAccount()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isAnon = steamID.BAnonGameServerAccount();
```

### BContentServerAccount

```csharp
bool BContentServerAccount()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isContentServer = steamID.BContentServerAccount();
```

### BClanAccount

```csharp
bool BClanAccount()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isClan = steamId.BClanAccount();
```

### BChatAccount

```csharp
bool BChatAccount()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isChat = steamID.BChatAccount();
```

### IsLobby

```csharp
bool IsLobby()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isLobby = steamID.IsLobby();
```

### BIndividualAccount

```csharp
bool BIndividualAccount()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isIndividual = steamID.BIndividualAccount();
```

### BAnonAccount

```csharp
bool BAnonAccount()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isAnon = steamID.BAnonAccount();
```

### BAnonUserAccount

```csharp
bool BAnonUserAccount()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isAnon = steamID.BAnonUserAccount();
```

### BConsoleUserAccount

```csharp
bool BConsoleUserAccount()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isConsole = steamID.BConsoleUserAccount();
```

### SetAccountID

```csharp
void SetAccountID(AccountID_t other)
```

**参数:**

- `other` (`AccountID_t`)

**用法示例:**
```csharp
steamID.SetAccountID(new AccountID_t(12345));
```

### SetAccountInstance

```csharp
void SetAccountInstance(uint other)
```

**参数:**

- `other` (`uint`)

**用法示例:**
```csharp
CSteamID steamID;
steamID.SetAccountInstance(1);
```

### SetEAccountType

```csharp
void SetEAccountType(EAccountType other)
```

**参数:**

- `other` (`EAccountType`)

**用法示例:**
```csharp
CSteamID steamId = new CSteamID();
steamId.SetEAccountType(EAccountType.Individual);
```

### SetEUniverse

```csharp
void SetEUniverse(EUniverse other)
```

**参数:**

- `other` (`EUniverse`)

**用法示例:**
```csharp
CSteamID steamId = CSteamID.Nil;
steamId.SetEUniverse(EUniverse.Public);
```

### GetAccountID

```csharp
AccountID_t GetAccountID()
```

**返回值:** `AccountID_t`

**用法示例:**
```csharp
AccountID_t accountId = steamId.GetAccountID();
```

### GetUnAccountInstance

```csharp
uint GetUnAccountInstance()
```

**返回值:** `uint`

**用法示例:**
```csharp
uint instance = steamID.GetUnAccountInstance();
```

### GetEAccountType

```csharp
EAccountType GetEAccountType()
```

**返回值:** `EAccountType`

**用法示例:**
```csharp
EAccountType accountType = steamID.GetEAccountType();
```

### GetEUniverse

```csharp
EUniverse GetEUniverse()
```

**返回值:** `EUniverse`

**用法示例:**
```csharp
EUniverse universe = steamID.GetEUniverse();
```

### IsValid

```csharp
bool IsValid()
```

**返回值:** `bool`

### GetSteamID64

```csharp
ulong GetSteamID64()
```

**返回值:** `ulong`

**用法示例:**
```csharp
ulong steamId64 = player.GetSteamID64();
```

### GetSteamID

```csharp
string GetSteamID()
```

**返回值:** `string`

**用法示例:**
```csharp
string steamId = player.GetSteamID();
```

### GetSteamID3

```csharp
string GetSteamID3()
```

**返回值:** `string`

**用法示例:**
```csharp
string steamId3 = player.GetSteamID3();
```

### GetSteamID32

```csharp
uint GetSteamID32()
```

**返回值:** `uint`

**用法示例:**
```csharp
uint steamId32 = player.GetSteamID32();
```

### GetSteamIDOnline

```csharp
string GetSteamIDOnline()
```

**返回值:** `string`

**用法示例:**
```csharp
string steamId = player.GetSteamIDOnline();
```

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
operator ulong(CSteamID that)
```

**参数:**

- `that` (`CSteamID`)

**返回值:** `operator`

**用法示例:**
```csharp
ulong steamId = (ulong)player.SteamID;
```

### Equals

```csharp
bool Equals(CSteamID other)
```

**参数:**

- `other` (`CSteamID`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(CSteamID other)
```

**参数:**

- `other` (`CSteamID`)

**返回值:** `int`

**用法示例:**
```csharp
int result = steamId.CompareTo(otherSteamId);
```

