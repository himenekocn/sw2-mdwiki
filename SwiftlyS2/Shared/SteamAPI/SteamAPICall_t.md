# 🏗️ SteamAPICall_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<SteamAPICall_t\>`

**实现接口:** `System.IComparable\<SteamAPICall_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_SteamAPICall` | `ulong` | - | - |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

**用法示例:**
```csharp
SteamAPICall_t call = default;
string result = call.ToString();
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
operator ulong(SteamAPICall_t that)
```

**参数:**

- `that` (`SteamAPICall_t`)

**返回值:** `operator`

**用法示例:**
```csharp
SteamAPICall_t call = (SteamAPICall_t)12345UL;
```

### Equals

```csharp
bool Equals(SteamAPICall_t other)
```

**参数:**

- `other` (`SteamAPICall_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(SteamAPICall_t other)
```

**参数:**

- `other` (`SteamAPICall_t`)

**返回值:** `int`

**用法示例:**
```csharp
SteamAPICall_t call1 = default;  
int result = call1.CompareTo(default);
```

