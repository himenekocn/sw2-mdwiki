# 🏗️ ScreenshotHandle

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<ScreenshotHandle\>`

**实现接口:** `System.IComparable\<ScreenshotHandle\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_ScreenshotHandle` | `uint` | - | - |

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
operator uint(ScreenshotHandle that)
```

**参数:**

- `that` (`ScreenshotHandle`)

**返回值:** `operator`

**用法示例:**
```csharp
uint handleValue = ScreenshotHandle.uint(existingHandle);
```

### Equals

```csharp
bool Equals(ScreenshotHandle other)
```

**参数:**

- `other` (`ScreenshotHandle`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(ScreenshotHandle other)
```

**参数:**

- `other` (`ScreenshotHandle`)

**返回值:** `int`

**用法示例:**
```csharp
int result = existingHandle.CompareTo(otherHandle);
```

