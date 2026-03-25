<a id="remoteplaycursorid_t"></a>

# 🏗️ RemotePlayCursorID_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<RemotePlayCursorID_t\>`

**实现接口:** `System.IComparable\<RemotePlayCursorID_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_RemotePlayCursorID` | `uint` | - | - |

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
operator uint(RemotePlayCursorID_t that)
```

**参数:**

- `that` (`RemotePlayCursorID_t`)

**返回值:** `operator`

**用法示例:**
```csharp
uint id = RemotePlayCursorID_t.uint(existingCursorID);
```

### Equals

```csharp
bool Equals(RemotePlayCursorID_t other)
```

**参数:**

- `other` (`RemotePlayCursorID_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(RemotePlayCursorID_t other)
```

**参数:**

- `other` (`RemotePlayCursorID_t`)

**返回值:** `int`

**用法示例:**
```csharp
int result = existingCursor.CompareTo(otherCursor);
```

