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

### IsMod

```csharp
bool IsMod()
```

**返回值:** `bool`

### IsShortcut

```csharp
bool IsShortcut()
```

**返回值:** `bool`

### IsP2PFile

```csharp
bool IsP2PFile()
```

**返回值:** `bool`

### AppID

```csharp
AppId_t AppID()
```

**返回值:** `AppId_t`

### Type

```csharp
EGameIDType Type()
```

**返回值:** `EGameIDType`

### ModID

```csharp
uint ModID()
```

**返回值:** `uint`

### IsValid

```csharp
bool IsValid()
```

**返回值:** `bool`

### Reset

```csharp
void Reset()
```

### Set

```csharp
void Set(ulong GameID)
```

**参数:**

- `GameID` (`ulong`)

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

