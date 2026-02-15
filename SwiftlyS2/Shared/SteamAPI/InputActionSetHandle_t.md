# 🏗️ InputActionSetHandle_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<InputActionSetHandle_t\>`

**实现接口:** `System.IComparable\<InputActionSetHandle_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_InputActionSetHandle` | `ulong` | - | - |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

**用法示例:**
```csharp
string result = InputActionSetHandle_t.Default.ToString();
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

### ulong (静态)

```csharp
operator ulong(InputActionSetHandle_t that)
```

**参数:**

- `that` (`InputActionSetHandle_t`)

**返回值:** `operator`

**用法示例:**
```csharp
InputActionSetHandle_t handle = (ulong)someHandle;
```

### Equals

```csharp
bool Equals(InputActionSetHandle_t other)
```

**参数:**

- `other` (`InputActionSetHandle_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(InputActionSetHandle_t other)
```

**参数:**

- `other` (`InputActionSetHandle_t`)

**返回值:** `int`

**用法示例:**
```csharp
InputActionSetHandle_t handle1 = InputActionSetHandle_t.SomeValue;  
int result = handle1.CompareTo(handle2);
```

