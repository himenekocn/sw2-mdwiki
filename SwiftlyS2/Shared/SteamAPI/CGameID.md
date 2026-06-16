<a id="cgameid"></a>

# 🏗️ CGameID

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<CGameID\>`

**实现接口:** `System.IComparable\<CGameID\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_GameID` | `ulong` | - | - |

## ⚙️ 方法

### IsSteamApp

```csharp
bool IsSteamApp()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isApp = gameID.IsSteamApp();
```

### IsMod

```csharp
bool IsMod()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isMod = gameID.IsMod();
```

### IsShortcut

```csharp
bool IsShortcut()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isShortcut = gameID.IsShortcut();
```

### IsP2PFile

```csharp
bool IsP2PFile()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isP2P = gameID.IsP2PFile();
```

### AppID

```csharp
AppId_t AppID()
```

**返回值:** `AppId_t`

**用法示例:**
```csharp
AppId_t appId = gameID.AppID();
```

### Type

```csharp
EGameIDType Type()
```

**返回值:** `EGameIDType`

**用法示例:**
```csharp
var type = gameID.Type();
```

### ModID

```csharp
uint ModID()
```

**返回值:** `uint`

**用法示例:**
```csharp
uint modId = gameID.ModID();
```

### IsValid

```csharp
bool IsValid()
```

**返回值:** `bool`

### Reset

```csharp
void Reset()
```

**用法示例:**
```csharp
gameID.Reset();
```

### Set

```csharp
void Set(ulong GameID)
```

**参数:**

- `GameID` (`ulong`)

**用法示例:**
```csharp
gameID.Set(730);
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
operator ulong(CGameID that)
```

**参数:**

- `that` (`CGameID`)

**返回值:** `operator`

**用法示例:**
```csharp
ulong id = (ulong)gameId;
```

### Equals

```csharp
bool Equals(CGameID other)
```

**参数:**

- `other` (`CGameID`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(CGameID other)
```

**参数:**

- `other` (`CGameID`)

**返回值:** `int`

**用法示例:**
```csharp
int result = gameID.CompareTo(otherGameID);
```

