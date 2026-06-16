<a id="snetsocket_t"></a>

# 🏗️ SNetSocket_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<SNetSocket_t\>`

**实现接口:** `System.IComparable\<SNetSocket_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_SNetSocket` | `uint` | - | - |

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
operator uint(SNetSocket_t that)
```

**参数:**

- `that` (`SNetSocket_t`)

**返回值:** `operator`

**用法示例:**
```csharp
uint socketId = (uint)existingSocket;
```

### Equals

```csharp
bool Equals(SNetSocket_t other)
```

**参数:**

- `other` (`SNetSocket_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(SNetSocket_t other)
```

**参数:**

- `other` (`SNetSocket_t`)

**返回值:** `int`

**用法示例:**
```csharp
int result = socket.CompareTo(otherSocket);
```

