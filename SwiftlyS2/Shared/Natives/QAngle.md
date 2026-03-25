<a id="qangle"></a>

# 🏗️ QAngle

QAngle 是一个包含三个 float 的类型，用于表示角度。采用度数制欧拉角，依次为：俯仰（Pitch）、偏航（Yaw）和翻滚（Roll）。

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
| `X` | `float` | - | 俯仰旋转（上下）的 X 轴访问器。 |
| `Y` | `float` | - | 用于偏航旋转（左右）的 Y 轴访问器。 |
| `Z` | `float` | - | 用于 Roll 旋转（翻滚/倾斜）的 Z 轴访问器。 |
| `Zero` | `QAngle` | - | - |

## ⚙️ 方法

### ToDirectionVectors

```csharp
void ToDirectionVectors(out Vector forward, out Vector right, out Vector up)
```

计算与该角度对应的正向、右侧和上向基向量。用法：<c>angle.ToDirectionVectors(out var forward, out var right, out var up);</c>

**参数:**

- `forward` (`out Vector`) - 前向方向（X：北，Z：上）。
- `right` (`out Vector`) - 方向正确。
- `up` (`out Vector`) - 向上方向。

**用法示例:**
```csharp
QAngle angle = default; angle.ToDirectionVectors(out var forward, out var right, out var up);
```

### Serialize

```csharp
string Serialize(IFormatProvider? formatProvider = null)
```

将角度向量序列化为字符串。示例返回："100 200 300"

**参数:**

- `formatProvider` (`IFormatProvider?`) = `null` - 要使用的字符串格式提供程序。为 null 时，使用默认提供程序。

**返回值:** `string` - 以字符串形式序列化的角度值（qangle）。

**用法示例:**
```csharp
string result = existingQAngle.Serialize(null);
```

### Deserialize (静态)

```csharp
QAngle Deserialize(string input, IFormatProvider? formatProvider = null)
```

将 qangle 从字符串反序列化。示例输入："100 200 300"

**参数:**

- `input` (`string`) - 以字符串形式序列化的角度值（qangle）。
- `formatProvider` (`IFormatProvider?`) = `null` - 要使用的字符串格式提供程序。为 null 时，使用默认提供程序。

**返回值:** `QAngle` - 反序列化后的角度值。

**用法示例:**
```csharp
var angle = QAngle.Deserialize("100 200 300", null);
```

### TryDeserialize (静态)

```csharp
bool TryDeserialize([NotNullWhen(true )
```

尝试从字符串反序列化 qangle。示例输入："100 200 300"

**参数:**

- `` (`[NotNullWhen(true`)

**返回值:** `bool` - 若反序列化成功则为 true，否则为 false。

**用法示例:**
```csharp
string input = "100 200 300";
bool success = QAngle.TryDeserialize(input, out var angle);
```

### TryDeserialize (静态)

```csharp
bool TryDeserialize([NotNullWhen(true )
```

尝试从字符串反序列化 qangle。示例输入："100 200 300"

**参数:**

- `` (`[NotNullWhen(true`)

**返回值:** `bool` - 若反序列化成功则为 true，否则为 false。

**用法示例:**
```csharp
string input = "100 200 300";
bool success = QAngle.TryDeserialize(input, out var angle);
```

