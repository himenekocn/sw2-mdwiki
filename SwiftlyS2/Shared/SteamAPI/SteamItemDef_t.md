# 🏗️ SteamItemDef_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<SteamItemDef_t\>`

**实现接口:** `System.IComparable\<SteamItemDef_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_SteamItemDef` | `int` | - | - |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

**用法示例:**
```csharp
string result = steamItemDef.ToString();
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
operator int(SteamItemDef_t that)
```

**参数:**

- `that` (`SteamItemDef_t`)

**返回值:** `operator`

**用法示例:**
```csharp
int result = (int)SteamItemDef_t.SomeItemDef;
```

### Equals

```csharp
bool Equals(SteamItemDef_t other)
```

**参数:**

- `other` (`SteamItemDef_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(SteamItemDef_t other)
```

**参数:**

- `other` (`SteamItemDef_t`)

**返回值:** `int`

**用法示例:**
```csharp
SteamItemDef_t item1 = SteamItemDef_t.DefinitionA;
SteamItemDef_t item2 = SteamItemDef_t.DefinitionB;
int result = item1.CompareTo(item2);
```

