# 📦 ConVar

**命名空间:** `SwiftlyS2.Core.Convars`

**类型:** `class`

**继承:** `ConVar`

**实现接口:** `IConVar\<T\>`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `MinValue` | `T` | get, set | - |
| `MaxValue` | `T` | get, set | - |
| `DefaultValue` | `T` | get, set | - |
| `Value` | `T` | get, set | - |

## ⚙️ 方法

### ValidateType

```csharp
void ValidateType()
```

### ReplicateToClient

```csharp
void ReplicateToClient(int clientId, T value)
```

**参数:**

- `clientId` (`int`)
- `value` (`T`)

### GetValue

```csharp
T GetValue()
```

**返回值:** `T`

### SetValue

```csharp
void SetValue(T value)
```

**参数:**

- `value` (`T`)

### SetInternal

```csharp
void SetInternal(T value)
```

**参数:**

- `value` (`T`)

### GetMinValue

```csharp
T GetMinValue()
```

**返回值:** `T`

### GetMaxValue

```csharp
T GetMaxValue()
```

**返回值:** `T`

### SetMinValue

```csharp
void SetMinValue(T minValue)
```

**参数:**

- `minValue` (`T`)

### SetMaxValue

```csharp
void SetMaxValue(T maxValue)
```

**参数:**

- `maxValue` (`T`)

### GetDefaultValue

```csharp
T GetDefaultValue()
```

**返回值:** `T`

### SetDefaultValue

```csharp
void SetDefaultValue(T defaultValue)
```

**参数:**

- `defaultValue` (`T`)

### TryGetMinValue

```csharp
bool TryGetMinValue(out T minValue)
```

**参数:**

- `minValue` (`out T`)

**返回值:** `bool`

### TryGetMaxValue

```csharp
bool TryGetMaxValue(out T maxValue)
```

**参数:**

- `maxValue` (`out T`)

**返回值:** `bool`

### TryGetDefaultValue

```csharp
bool TryGetDefaultValue(out T defaultValue)
```

**参数:**

- `defaultValue` (`out T`)

**返回值:** `bool`

