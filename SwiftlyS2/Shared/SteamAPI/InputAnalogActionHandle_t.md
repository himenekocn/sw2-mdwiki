# 🏗️ InputAnalogActionHandle_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<InputAnalogActionHandle_t\>`

**实现接口:** `System.IComparable\<InputAnalogActionHandle_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_InputAnalogActionHandle` | `ulong` | - | - |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

**用法示例:**
```csharp
InputAnalogActionHandle_t handle = default;
string result = handle.ToString();
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
operator ulong(InputAnalogActionHandle_t that)
```

**参数:**

- `that` (`InputAnalogActionHandle_t`)

**返回值:** `operator`

**用法示例:**
```csharp
InputAnalogActionHandle_t handle = InputAnalogActionHandle_t.ulong(12345);
```

### Equals

```csharp
bool Equals(InputAnalogActionHandle_t other)
```

**参数:**

- `other` (`InputAnalogActionHandle_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(InputAnalogActionHandle_t other)
```

**参数:**

- `other` (`InputAnalogActionHandle_t`)

**返回值:** `int`

**用法示例:**
```csharp
InputAnalogActionHandle_t handle1 = InputAnalogActionHandle_t.SomeValue;  
int result = handle1.CompareTo(InputAnalogActionHandle_t.OtherValue);
```

