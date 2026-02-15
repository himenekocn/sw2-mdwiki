# 🏗️ SteamInventoryResult_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<SteamInventoryResult_t\>`

**实现接口:** `System.IComparable\<SteamInventoryResult_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_SteamInventoryResult` | `int` | - | - |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

**用法示例:**
```csharp
string result = inventoryResult.ToString();
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
operator int(SteamInventoryResult_t that)
```

**参数:**

- `that` (`SteamInventoryResult_t`)

**返回值:** `operator`

**用法示例:**
```csharp
int result = SteamInventoryResult_t(someInstance);
```

### Equals

```csharp
bool Equals(SteamInventoryResult_t other)
```

**参数:**

- `other` (`SteamInventoryResult_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(SteamInventoryResult_t other)
```

**参数:**

- `other` (`SteamInventoryResult_t`)

**返回值:** `int`

**用法示例:**
```csharp
SteamInventoryResult_t result1 = SteamInventoryResult_t.Success;  
SteamInventoryResult_t result2 = SteamInventoryResult_t.NoInv;  
int comparison = result1.CompareTo(result2);
```

