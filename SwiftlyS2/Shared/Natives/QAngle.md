<a id="qangle"></a>

# 🏗️ QAngle

QAngle 是一个包含三个浮点数的类型，表示一个角度。度制欧拉角。俯仰角、偏航角、翻滚角

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
| `X` | `float` | - | 俯仰旋转（上下）的X轴访问器 |
| `Y` | `float` | - | Y轴访问器，用于偏航旋转（左/右）。 |
| `Z` | `float` | - | 滚转角（Roll/Tilt）的Z轴访问器。 |
| `Zero` | `QAngle` | - | - |

## ⚙️ 方法

### ToDirectionVectors

```csharp
void ToDirectionVectors(out Vector forward, out Vector right, out Vector up)
```

计算与该角度对应的前向、右向和上向基向量。用法：<c>angle.ToDirectionVectors(out var forward, out var right, out var up);</c>

**参数:**

- `forward` (`out Vector`) - 前向方向（X：北，Z：上）。
- `right` (`out Vector`) - 右方向。
- `up` (`out Vector`) - 向上方向。

**用法示例:**
```csharp
angle.ToDirectionVectors(out var forward, out var right, out var up);
```

### Serialize

```csharp
string Serialize(IFormatProvider? formatProvider = null)
```

将qangle序列化为字符串。返回示例："100 200 300"

**参数:**

- `formatProvider` (`IFormatProvider?`) = `null` - 用于字符串的格式提供程序。为null则使用默认提供程序。

**返回值:** `string` - 序列化后的qangle字符串。

**用法示例:**
```csharp
string result = qangle.Serialize(null);
```

### Deserialize (静态)

```csharp
QAngle Deserialize(string input, IFormatProvider? formatProvider = null)
```

从字符串反序列化四元组角度。示例输入："100 200 300"

**参数:**

- `input` (`string`) - 序列化后的qangle字符串。
- `formatProvider` (`IFormatProvider?`) = `null` - 用于字符串的格式提供程序。为null则使用默认提供程序。

**返回值:** `QAngle` - 已反序列化的视角角度。

**用法示例:**
```csharp
var angle = QAngle.Deserialize("100 200 300", null);
```

### TryDeserialize (静态)

```csharp
bool TryDeserialize([NotNullWhen(true )
```

尝试从字符串反序列化qangle。示例输入："100 200 300"

**参数:**

- `` (`[NotNullWhen(true`)

**返回值:** `bool` - 如果反序列化成功则为 true，否则为 false。

**用法示例:**
```csharp
bool success = QAngle.TryDeserialize("100 200 300", out QAngle angle);
```

### TryDeserialize (静态)

```csharp
bool TryDeserialize([NotNullWhen(true )
```

尝试从字符串反序列化qangle。示例输入："100 200 300"

**参数:**

- `` (`[NotNullWhen(true`)

**返回值:** `bool` - 如果反序列化成功则为 true，否则为 false。

**用法示例:**
```csharp
bool success = QAngle.TryDeserialize("100 200 300", out QAngle angle);
```

