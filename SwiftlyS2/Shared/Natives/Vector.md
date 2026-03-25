# 🏗️ Vector

Source 2 的三维向量。不再有 CSHARP 混乱。

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `X` | `float` | - | - |
| `Y` | `float` | - | - |
| `Z` | `float` | - | - |

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Zero` | `Vector` | - | - |
| `One` | `Vector` | - | - |

## ⚙️ 方法

### ToBuiltin

```csharp
Vector3 ToBuiltin()
```

**返回值:** `Vector3`

**用法示例:**
```csharp
Vector3 builtin = vector.ToBuiltin();
```

### Normalize

```csharp
void Normalize()
```

**用法示例:**
```csharp
var vec = Vector.Zero; vec.Normalize();
```

### Normalized

```csharp
Vector Normalized()
```

**返回值:** `Vector`

**用法示例:**
```csharp
Vector normalizedVec = someVector.Normalized();
```

### Deconstruct

```csharp
void Deconstruct(out float x, out float y, out float z)
```

**参数:**

- `x` (`out float`)
- `y` (`out float`)
- `z` (`out float`)

**用法示例:**
```csharp
Vector v = default; v.Deconstruct(out float x, out float y, out float z);
```

### ToQAngles

```csharp
QAngle ToQAngles()
```

将此前方向向量转换为欧拉 Q 角度（俯仰角、偏航角、翻滚角）。用法：<c>forward.ToQAngles(out var angles);</c>

**返回值:** `QAngle` - 结果 <see cref="QAngle"/>。

**用法示例:**
```csharp
QAngle angles = forward.ToQAngles();
```

### Serialize

```csharp
string Serialize(IFormatProvider? formatProvider = null)
```

将向量序列化为字符串。示例返回值："100 200 300"

**参数:**

- `formatProvider` (`IFormatProvider?`) = `null` - 要使用的字符串格式提供程序。为 null 时，使用默认提供程序。

**返回值:** `string` - 序列化的向量，以字符串形式存储。

**用法示例:**
```csharp
string serialized = vector.Serialize(null);
```

### Deserialize (静态)

```csharp
Vector Deserialize(string input, IFormatProvider? formatProvider = null)
```

从字符串反序列化向量。示例输入："100 200 300"

**参数:**

- `input` (`string`) - 序列化的向量，以字符串形式存储。
- `formatProvider` (`IFormatProvider?`) = `null` - 要使用的字符串格式提供程序。为 null 时，使用默认提供程序。

**返回值:** `Vector` - 反序列化的向量。

**用法示例:**
```csharp
var vector = Vector.Deserialize("100 200 300", null);
```

### TryDeserialize (静态)

```csharp
bool TryDeserialize([NotNullWhen(true )
```

尝试将向量从字符串反序列化。示例输入："100 200 300"

**参数:**

- `` (`[NotNullWhen(true`)

**返回值:** `bool` - 若反序列化成功则为 true，否则为 false。

**用法示例:**
```csharp
string input = "100 200 300"; if (Vector.TryDeserialize(input, out var vector)) { }
```

### TryDeserialize (静态)

```csharp
bool TryDeserialize([NotNullWhen(true )
```

尝试将向量从字符串反序列化。示例输入："100 200 300"

**参数:**

- `` (`[NotNullWhen(true`)

**返回值:** `bool` - 若反序列化成功则为 true，否则为 false。

**用法示例:**
```csharp
string input = "100 200 300"; if (Vector.TryDeserialize(input, out var vector)) { }
```

### Distance2D

```csharp
float Distance2D(Vector other)
```

**参数:**

- `other` (`Vector`)

**返回值:** `float`

**用法示例:**
```csharp
float dist = player.Position.Distance2D(target.Position);
```

### Distance2DSquared

```csharp
float Distance2DSquared(Vector other)
```

**参数:**

- `other` (`Vector`)

**返回值:** `float`

**用法示例:**
```csharp
float distSq = myVector.Distance2DSquared(targetVector);
```

### Length2D

```csharp
float Length2D()
```

**返回值:** `float`

**用法示例:**
```csharp
float len = player.Position.Length2D();
```

### Length2DSquared

```csharp
float Length2DSquared()
```

**返回值:** `float`

**用法示例:**
```csharp
float lengthSq = vector.Length2DSquared();
```

### Normalize2D

```csharp
void Normalize2D()
```

**用法示例:**
```csharp
var v = Vector.Zero; v.Normalize2D();
```

### Normalized2D

```csharp
Vector Normalized2D()
```

**返回值:** `Vector`

**用法示例:**
```csharp
Vector normalized = player.Position.Normalized2D();
```

