# 🏗️ RemotePlaySessionID_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<RemotePlaySessionID_t\>`

**实现接口:** `System.IComparable\<RemotePlaySessionID_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_RemotePlaySessionID` | `uint` | - | - |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

**用法示例:**
```csharp
string idStr = sessionID.ToString();
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
operator uint(RemotePlaySessionID_t that)
```

**参数:**

- `that` (`RemotePlaySessionID_t`)

**返回值:** `operator`

**用法示例:**
```csharp
uint sessionId = (uint)RemotePlaySessionID_t.someInstance;
```

### Equals

```csharp
bool Equals(RemotePlaySessionID_t other)
```

**参数:**

- `other` (`RemotePlaySessionID_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(RemotePlaySessionID_t other)
```

**参数:**

- `other` (`RemotePlaySessionID_t`)

**返回值:** `int`

**用法示例:**
```csharp
RemotePlaySessionID_t id1 = RemotePlaySessionID_t.Default;
RemotePlaySessionID_t id2 = RemotePlaySessionID_t.Default;
int result = id1.CompareTo(id2);
```

