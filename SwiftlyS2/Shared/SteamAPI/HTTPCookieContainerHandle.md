<a id="httpcookiecontainerhandle"></a>

# 🏗️ HTTPCookieContainerHandle

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<HTTPCookieContainerHandle\>`

**实现接口:** `System.IComparable\<HTTPCookieContainerHandle\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_HTTPCookieContainerHandle` | `uint` | - | - |

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
operator uint(HTTPCookieContainerHandle that)
```

**参数:**

- `that` (`HTTPCookieContainerHandle`)

**返回值:** `operator`

**用法示例:**
```csharp
uint handleValue = (uint)existingCookieContainerHandle;
```

### Equals

```csharp
bool Equals(HTTPCookieContainerHandle other)
```

**参数:**

- `other` (`HTTPCookieContainerHandle`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(HTTPCookieContainerHandle other)
```

**参数:**

- `other` (`HTTPCookieContainerHandle`)

**返回值:** `int`

**用法示例:**
```csharp
int result = existingHandle.CompareTo(otherHandle);
```

