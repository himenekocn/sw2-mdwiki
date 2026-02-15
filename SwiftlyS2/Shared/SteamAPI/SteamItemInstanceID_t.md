# 🏗️ SteamItemInstanceID_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<SteamItemInstanceID_t\>`

**实现接口:** `System.IComparable\<SteamItemInstanceID_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_SteamItemInstanceID` | `ulong` | - | - |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

**用法示例:**
```csharp
SteamItemInstanceID_t id = SteamInventory.GetNextItemInstanceID();  
Console.WriteLine(id.ToString());
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

### ulong (静态)

```csharp
operator ulong(SteamItemInstanceID_t that)
```

**参数:**

- `that` (`SteamItemInstanceID_t`)

**返回值:** `operator`

**用法示例:**
```csharp
SteamItemInstanceID_t instance = default;
ulong id = (ulong)instance;
```

### Equals

```csharp
bool Equals(SteamItemInstanceID_t other)
```

**参数:**

- `other` (`SteamItemInstanceID_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(SteamItemInstanceID_t other)
```

**参数:**

- `other` (`SteamItemInstanceID_t`)

**返回值:** `int`

**用法示例:**
```csharp
SteamItemInstanceID_t id1 = default; SteamItemInstanceID_t id2 = default; int result = id1.CompareTo(id2);
```

