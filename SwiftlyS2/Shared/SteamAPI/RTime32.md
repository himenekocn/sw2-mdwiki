# 🏗️ RTime32

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<RTime32\>`

**实现接口:** `System.IComparable\<RTime32\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_RTime32` | `uint` | - | - |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

**用法示例:**
```csharp
string timeStr = RTime32.ToString();
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
operator uint(RTime32 that)
```

**参数:**

- `that` (`RTime32`)

**返回值:** `operator`

**用法示例:**
```csharp
uint val = (uint)RTime32.someInstance;
```

### Equals

```csharp
bool Equals(RTime32 other)
```

**参数:**

- `other` (`RTime32`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(RTime32 other)
```

**参数:**

- `other` (`RTime32`)

**返回值:** `int`

**用法示例:**
```csharp
RTime32 time1 = RTime32.Now;  
int result = time1.CompareTo(RTime32.Zero);
```

