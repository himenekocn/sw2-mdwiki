# 🏗️ AccountID_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<AccountID_t\>`

**实现接口:** `System.IComparable\<AccountID_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_AccountID` | `uint` | - | - |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

**用法示例:**
```csharp
AccountID_t id = AccountID_t.Default;  
string str = id.ToString();
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
operator uint(AccountID_t that)
```

**参数:**

- `that` (`AccountID_t`)

**返回值:** `operator`

**用法示例:**
```csharp
uint id = (uint)AccountID_t.SomeValue;
```

### Equals

```csharp
bool Equals(AccountID_t other)
```

**参数:**

- `other` (`AccountID_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(AccountID_t other)
```

**参数:**

- `other` (`AccountID_t`)

**返回值:** `int`

**用法示例:**
```csharp
AccountID_t id1 = AccountID_t.Default;  
int result = id1.CompareTo(AccountID_t.Empty);
```

