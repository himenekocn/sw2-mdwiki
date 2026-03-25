<a id="steaminventoryupdatehandle_t"></a>

# 🏗️ SteamInventoryUpdateHandle_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<SteamInventoryUpdateHandle_t\>`

**实现接口:** `System.IComparable\<SteamInventoryUpdateHandle_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_SteamInventoryUpdateHandle` | `ulong` | - | - |

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

### ulong (静态)

```csharp
operator ulong(SteamInventoryUpdateHandle_t that)
```

**参数:**

- `that` (`SteamInventoryUpdateHandle_t`)

**返回值:** `operator`

**用法示例:**
```csharp
ulong handleValue = SteamInventoryUpdateHandle_t.ulong(existingHandle);
```

### Equals

```csharp
bool Equals(SteamInventoryUpdateHandle_t other)
```

**参数:**

- `other` (`SteamInventoryUpdateHandle_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(SteamInventoryUpdateHandle_t other)
```

**参数:**

- `other` (`SteamInventoryUpdateHandle_t`)

**返回值:** `int`

**用法示例:**
```csharp
int result = handle.CompareTo(otherHandle);
```

