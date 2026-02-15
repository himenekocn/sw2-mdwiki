# 🏗️ QAngle

QAngle is a type that contains 3 float, representing an angle. Degree Euler. Pitch, Yaw, Roll

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `Pitch` | `float` | - | - |
| `Yaw` | `float` | - | - |
| `Roll` | `float` | - | - |

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `X` | `float` | - | X-axis accessor for Pitch rotation (up/down). |
| `Y` | `float` | - | Y-axis accessor for Yaw rotation (left/right). |
| `Z` | `float` | - | Z-axis accessor for Roll rotation (roll/tilt). |

## ⚙️ 方法

### Deserialize (静态)

```csharp
QAngle Deserialize(string input, IFormatProvider? formatProvider = null)
```

Deserializes the qangle from a string. Example input: "100 200 300"

**参数:**

- `input` (`string`) - Serialized qangle in string.
- `formatProvider` (`IFormatProvider?`) = `null` - Format provider to use for the string. Null for default provider.

**返回值:** `QAngle` - Deserialized qangle.

### TryDeserialize (静态)

```csharp
bool TryDeserialize([NotNullWhen(true )
```

Tries to deserialize the qangle from a string. Example input: "100 200 300"

**参数:**

- `` (`[NotNullWhen(true`)

**返回值:** `bool` - True if the deserialization was successful, false otherwise.

### TryDeserialize (静态)

```csharp
bool TryDeserialize([NotNullWhen(true )
```

Tries to deserialize the qangle from a string. Example input: "100 200 300"

**参数:**

- `` (`[NotNullWhen(true`)

**返回值:** `bool` - True if the deserialization was successful, false otherwise.

