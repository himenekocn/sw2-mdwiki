# 🏗️ HSteamPipe

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<HSteamPipe\>`

**实现接口:** `System.IComparable\<HSteamPipe\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_HSteamPipe` | `int` | - | - |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

**用法示例:**
```csharp
HSteamPipe pipe = default;
string result = pipe.ToString();
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

### int (静态)

```csharp
operator int(HSteamPipe that)
```

**参数:**

- `that` (`HSteamPipe`)

**返回值:** `operator`

**用法示例:**
```csharp
int pipe = (int)HSteamPipe.myPipe;
```

### Equals

```csharp
bool Equals(HSteamPipe other)
```

**参数:**

- `other` (`HSteamPipe`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(HSteamPipe other)
```

**参数:**

- `other` (`HSteamPipe`)

**返回值:** `int`

**用法示例:**
```csharp
HSteamPipe pipe1 = SteamAPI.GetHSteamPipe();  
int result = pipe1.CompareTo(pipe2);
```

