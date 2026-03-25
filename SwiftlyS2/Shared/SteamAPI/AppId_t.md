<a id="appid_t"></a>

# 🏗️ AppId_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<AppId_t\>`

**实现接口:** `System.IComparable\<AppId_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_AppId` | `uint` | - | - |

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
operator uint(AppId_t that)
```

**参数:**

- `that` (`AppId_t`)

**返回值:** `operator`

**用法示例:**
```csharp
uint appIdValue = (uint)existingAppId;
```

### Equals

```csharp
bool Equals(AppId_t other)
```

**参数:**

- `other` (`AppId_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(AppId_t other)
```

**参数:**

- `other` (`AppId_t`)

**返回值:** `int`

**用法示例:**
```csharp
int result = existingAppId.CompareTo(otherAppId);
```

