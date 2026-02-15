# 🏗️ DepotId_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<DepotId_t\>`

**实现接口:** `System.IComparable\<DepotId_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_DepotId` | `uint` | - | - |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

**用法示例:**
```csharp
DepotId_t id = DepotId_t.SomeValue;
string str = id.ToString();
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
operator uint(DepotId_t that)
```

**参数:**

- `that` (`DepotId_t`)

**返回值:** `operator`

**用法示例:**
```csharp
uint id = (uint)DepotId_t.SomeValue;
```

### Equals

```csharp
bool Equals(DepotId_t other)
```

**参数:**

- `other` (`DepotId_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(DepotId_t other)
```

**参数:**

- `other` (`DepotId_t`)

**返回值:** `int`

**用法示例:**
```csharp
DepotId_t id1 = DepotId_t.A;  
int result = id1.CompareTo(DepotId_t.B);
```

