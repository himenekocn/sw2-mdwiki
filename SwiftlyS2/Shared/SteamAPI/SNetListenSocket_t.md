# 🏗️ SNetListenSocket_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<SNetListenSocket_t\>`

**实现接口:** `System.IComparable\<SNetListenSocket_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_SNetListenSocket` | `uint` | - | - |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

**用法示例:**
```csharp
string result = listenSocket.ToString();
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
operator uint(SNetListenSocket_t that)
```

**参数:**

- `that` (`SNetListenSocket_t`)

**返回值:** `operator`

**用法示例:**
```csharp
uint socketId = (uint)someListenSocket;
```

### Equals

```csharp
bool Equals(SNetListenSocket_t other)
```

**参数:**

- `other` (`SNetListenSocket_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(SNetListenSocket_t other)
```

**参数:**

- `other` (`SNetListenSocket_t`)

**返回值:** `int`

**用法示例:**
```csharp
SNetListenSocket_t socket1 = default;  
int result = socket1.CompareTo(default);
```

