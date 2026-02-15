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

**用法示例:**
```csharp
string idStr = AppId_t.Dota2.ToString();
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

### uint (静态)

```csharp
operator uint(AppId_t that)
```

**参数:**

- `that` (`AppId_t`)

**返回值:** `operator`

**用法示例:**
```csharp
uint id = (uint)AppId_t.SomeValue;
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
AppId_t id1 = AppId_t.SomeValue;  
int result = id1.CompareTo(AppId_t.OtherValue);
```

