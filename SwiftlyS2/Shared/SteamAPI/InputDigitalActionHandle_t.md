# 🏗️ InputDigitalActionHandle_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<InputDigitalActionHandle_t\>`

**实现接口:** `System.IComparable\<InputDigitalActionHandle_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_InputDigitalActionHandle` | `ulong` | - | - |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

**用法示例:**
```csharp
InputDigitalActionHandle_t handle = InputManager.GetAction("jump");  
Console.WriteLine(handle.ToString());
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
operator ulong(InputDigitalActionHandle_t that)
```

**参数:**

- `that` (`InputDigitalActionHandle_t`)

**返回值:** `operator`

**用法示例:**
```csharp
InputDigitalActionHandle_t handle = (InputDigitalActionHandle_t)12345UL;
```

### Equals

```csharp
bool Equals(InputDigitalActionHandle_t other)
```

**参数:**

- `other` (`InputDigitalActionHandle_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(InputDigitalActionHandle_t other)
```

**参数:**

- `other` (`InputDigitalActionHandle_t`)

**返回值:** `int`

**用法示例:**
```csharp
int result = handle1.CompareTo(handle2);
```

