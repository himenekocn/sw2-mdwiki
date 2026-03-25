# 🏗️ PartyBeaconID_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<PartyBeaconID_t\>`

**实现接口:** `System.IComparable\<PartyBeaconID_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_PartyBeaconID` | `ulong` | - | - |

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

### ulong (静态)

```csharp
operator ulong(PartyBeaconID_t that)
```

**参数:**

- `that` (`PartyBeaconID_t`)

**返回值:** `operator`

**用法示例:**
```csharp
ulong id = PartyBeaconID_t.operator ulong(existingBeacon);
```

### Equals

```csharp
bool Equals(PartyBeaconID_t other)
```

**参数:**

- `other` (`PartyBeaconID_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(PartyBeaconID_t other)
```

**参数:**

- `other` (`PartyBeaconID_t`)

**返回值:** `int`

**用法示例:**
```csharp
int result = existingBeaconID.CompareTo(otherBeaconID);
```

