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

### Set

```csharp
void Set(AccountID_t unAccountID, EUniverse eUniverse, EAccountType eAccountType)
```

**参数:**

- `unAccountID` (`AccountID_t`)
- `eUniverse` (`EUniverse`)
- `eAccountType` (`EAccountType`)

### InstancedSet

```csharp
void InstancedSet(AccountID_t unAccountID, uint unInstance, EUniverse eUniverse, EAccountType eAccountType)
```

**参数:**

- `unAccountID` (`AccountID_t`)
- `unInstance` (`uint`)
- `eUniverse` (`EUniverse`)
- `eAccountType` (`EAccountType`)

### Clear

```csharp
void Clear()
```

### CreateBlankAnonLogon

```csharp
void CreateBlankAnonLogon(EUniverse eUniverse)
```

**参数:**

- `eUniverse` (`EUniverse`)

### CreateBlankAnonUserLogon

```csharp
void CreateBlankAnonUserLogon(EUniverse eUniverse)
```

**参数:**

- `eUniverse` (`EUniverse`)

### BBlankAnonAccount

```csharp
bool BBlankAnonAccount()
```

**返回值:** `bool`

### BGameServerAccount

```csharp
bool BGameServerAccount()
```

**返回值:** `bool`

### BPersistentGameServerAccount

```csharp
bool BPersistentGameServerAccount()
```

**返回值:** `bool`

### BAnonGameServerAccount

```csharp
bool BAnonGameServerAccount()
```

**返回值:** `bool`

### BContentServerAccount

```csharp
bool BContentServerAccount()
```

**返回值:** `bool`

### BClanAccount

```csharp
bool BClanAccount()
```

**返回值:** `bool`

### BChatAccount

```csharp
bool BChatAccount()
```

**返回值:** `bool`

### IsLobby

```csharp
bool IsLobby()
```

**返回值:** `bool`

### BIndividualAccount

```csharp
bool BIndividualAccount()
```

**返回值:** `bool`

### BAnonAccount

```csharp
bool BAnonAccount()
```

**返回值:** `bool`

### BAnonUserAccount

```csharp
bool BAnonUserAccount()
```

**返回值:** `bool`

### BConsoleUserAccount

```csharp
bool BConsoleUserAccount()
```

**返回值:** `bool`

### SetAccountID

```csharp
void SetAccountID(AccountID_t other)
```

**参数:**

- `other` (`AccountID_t`)

### SetAccountInstance

```csharp
void SetAccountInstance(uint other)
```

**参数:**

- `other` (`uint`)

### SetEAccountType

```csharp
void SetEAccountType(EAccountType other)
```

**参数:**

- `other` (`EAccountType`)

### SetEUniverse

```csharp
void SetEUniverse(EUniverse other)
```

**参数:**

- `other` (`EUniverse`)

### GetAccountID

```csharp
AccountID_t GetAccountID()
```

**返回值:** `AccountID_t`

### GetUnAccountInstance

```csharp
uint GetUnAccountInstance()
```

**返回值:** `uint`

### GetEAccountType

```csharp
EAccountType GetEAccountType()
```

**返回值:** `EAccountType`

### GetEUniverse

```csharp
EUniverse GetEUniverse()
```

**返回值:** `EUniverse`

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

### GetSteamID

```csharp
string GetSteamID()
```

**返回值:** `string`

### GetSteamID3

```csharp
string GetSteamID3()
```

**返回值:** `string`

### GetSteamID32

```csharp
uint GetSteamID32()
```

**返回值:** `uint`

### GetSteamIDOnline

```csharp
string GetSteamIDOnline()
```

**返回值:** `string`

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

