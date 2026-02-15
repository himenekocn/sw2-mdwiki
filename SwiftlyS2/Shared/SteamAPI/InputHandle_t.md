# 🏗️ InputHandle_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<InputHandle_t\>`

**实现接口:** `System.IComparable\<InputHandle_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_InputHandle` | `ulong` | - | - |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

**用法示例:**
```csharp
InputHandle_t handle = InputManager.GetLastInput();  
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
operator ulong(InputHandle_t that)
```

**参数:**

- `that` (`InputHandle_t`)

**返回值:** `operator`

**用法示例:**
```csharp
InputHandle_t.ulong(handle);
```

### Equals

```csharp
bool Equals(InputHandle_t other)
```

**参数:**

- `other` (`InputHandle_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(InputHandle_t other)
```

**参数:**

- `other` (`InputHandle_t`)

**返回值:** `int`

**用法示例:**
```csharp
InputHandle_t handle1 = InputManager.GetHandle();  
int result = handle1.CompareTo(handle2);
```

