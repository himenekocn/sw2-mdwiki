<a id="hsteamnetpollgroup"></a>

# 🏗️ HSteamNetPollGroup

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<HSteamNetPollGroup\>`

**实现接口:** `System.IComparable\<HSteamNetPollGroup\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_HSteamNetPollGroup` | `uint` | - | - |

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

### uint (静态)

```csharp
operator uint(HSteamNetPollGroup that)
```

**参数:**

- `that` (`HSteamNetPollGroup`)

**返回值:** `operator`

**用法示例:**
```csharp
uint pollGroupValue = HSteamNetPollGroup.uint(existingPollGroup);
```

### Equals

```csharp
bool Equals(HSteamNetPollGroup other)
```

**参数:**

- `other` (`HSteamNetPollGroup`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(HSteamNetPollGroup other)
```

**参数:**

- `other` (`HSteamNetPollGroup`)

**返回值:** `int`

**用法示例:**
```csharp
int result = existingPollGroup.CompareTo(otherPollGroup);
```

