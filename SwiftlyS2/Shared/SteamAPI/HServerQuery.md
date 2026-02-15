# 🏗️ HServerQuery

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<HServerQuery\>`

**实现接口:** `System.IComparable\<HServerQuery\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_HServerQuery` | `int` | - | - |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

**用法示例:**
```csharp
string result = HServerQuery.ToString();
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
operator int(HServerQuery that)
```

**参数:**

- `that` (`HServerQuery`)

**返回值:** `operator`

**用法示例:**
```csharp
int result = (int)HServerQuery.someInstance;
```

### Equals

```csharp
bool Equals(HServerQuery other)
```

**参数:**

- `other` (`HServerQuery`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(HServerQuery other)
```

**参数:**

- `other` (`HServerQuery`)

**返回值:** `int`

**用法示例:**
```csharp
HServerQuery a = HServerQuery.Default;  
int result = a.CompareTo(HServerQuery.Empty);
```

