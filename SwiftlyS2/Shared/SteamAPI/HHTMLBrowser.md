# 🏗️ HHTMLBrowser

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<HHTMLBrowser\>`

**实现接口:** `System.IComparable\<HHTMLBrowser\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_HHTMLBrowser` | `uint` | - | - |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

**用法示例:**
```csharp
string result = HHTMLBrowser.ToString();
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
operator uint(HHTMLBrowser that)
```

**参数:**

- `that` (`HHTMLBrowser`)

**返回值:** `operator`

**用法示例:**
```csharp
uint value = (uint)HHTMLBrowser.someInstance;
```

### Equals

```csharp
bool Equals(HHTMLBrowser other)
```

**参数:**

- `other` (`HHTMLBrowser`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(HHTMLBrowser other)
```

**参数:**

- `other` (`HHTMLBrowser`)

**返回值:** `int`

**用法示例:**
```csharp
HHTMLBrowser a = HHTMLBrowser.Default;  
int result = a.CompareTo(HHTMLBrowser.Empty);
```

