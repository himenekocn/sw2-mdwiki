# 🏗️ HTTPRequestHandle

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<HTTPRequestHandle\>`

**实现接口:** `System.IComparable\<HTTPRequestHandle\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_HTTPRequestHandle` | `uint` | - | - |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

**用法示例:**
```csharp
string result = HTTPRequestHandle.ToString();
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
operator uint(HTTPRequestHandle that)
```

**参数:**

- `that` (`HTTPRequestHandle`)

**返回值:** `operator`

**用法示例:**
```csharp
uint handle = (uint)HTTPRequestHandle.someInstance;
```

### Equals

```csharp
bool Equals(HTTPRequestHandle other)
```

**参数:**

- `other` (`HTTPRequestHandle`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(HTTPRequestHandle other)
```

**参数:**

- `other` (`HTTPRequestHandle`)

**返回值:** `int`

**用法示例:**
```csharp
HTTPRequestHandle h1 = HTTPRequestHandle.Default;  
int result = h1.CompareTo(other);
```

