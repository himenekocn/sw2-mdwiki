# 🏗️ QAngle

QAngle 是一种包含 3 个 float 的类型，用于表示角度。欧拉角（度）。俯仰角、偏航角、滚转角。

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `Pitch` | `float` | - | - |
| `Yaw` | `float` | - | - |
| `Roll` | `float` | - | - |

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `X` | `float` | - | Pitch旋转（上下）的X轴访问器。 |
| `Y` | `float` | - | 偏航旋转（左右）的Y轴访问器。 |
| `Z` | `float` | - | 用于滚转（roll/tilt）旋转的Z轴访问器。 |
| `Zero` | `QAngle` | - | - |

## ⚙️ 方法

### ToDirectionVectors

```csharp
void ToDirectionVectors(out Vector forward, out Vector right, out Vector up)
```

计算与此角度相对应的前向、右向和上向基向量。用法：<c>angle.ToDirectionVectors(out var forward, out var right, out var up);</c>

**参数:**

- `forward` (`out Vector`) - 前进方向 (X: 北, Z: 上)。
- `right` (`out Vector`) - 正确的方向。
- `up` (`out Vector`) - 向上方向。

**用法示例:**
```csharp
QAngle angle = new QAngle(0, 90, 0);  
angle.ToDirectionVectors(out var forward, out var right, out var up);
```

### Serialize

```csharp
string Serialize(IFormatProvider? formatProvider = null)
```

将qangle序列化为字符串。示例返回值："100 200 300"

**参数:**

- `formatProvider` (`IFormatProvider?`) = `null` - 用于字符串的格式提供程序。若为 null，则使用默认提供程序。

**返回值:** `string` - 序列化后的四元数角度值（以字符串形式）。

**用法示例:**
```csharp
QAngle angle = new QAngle(100, 200, 300);
string result = angle.Serialize(null);
```

### Deserialize (静态)

```csharp
QAngle Deserialize(string input, IFormatProvider? formatProvider = null)
```

从字符串反序列化qangle。示例输入："100 200 300"

**参数:**

- `input` (`string`) - 序列化后的四元数角度值（以字符串形式）。
- `formatProvider` (`IFormatProvider?`) = `null` - 用于字符串的格式提供程序。若为 null，则使用默认提供程序。

**返回值:** `QAngle` - 反序列化后的q角。

**用法示例:**
```csharp
QAngle angle = QAngle.Deserialize("100 200 300", null);
```

### TryDeserialize (静态)

```csharp
bool TryDeserialize([NotNullWhen(true )
```

尝试从字符串反序列化一个qangle。示例输入："100 200 300"

**参数:**

- `` (`[NotNullWhen(true`)

**返回值:** `bool` - 如果反序列化成功，则为 true；否则为 false。

**用法示例:**
```csharp
bool success = QAngle.TryDeserialize("100 200 300", out var angle);
```

### TryDeserialize (静态)

```csharp
bool TryDeserialize([NotNullWhen(true )
```

尝试从字符串反序列化一个qangle。示例输入："100 200 300"

**参数:**

- `` (`[NotNullWhen(true`)

**返回值:** `bool` - 如果反序列化成功，则为 true；否则为 false。

**用法示例:**
```csharp
bool success = QAngle.TryDeserialize("100 200 300", out var angle);
```

