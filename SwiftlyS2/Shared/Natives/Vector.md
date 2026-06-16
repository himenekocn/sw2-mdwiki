<a id="vector"></a>

# 🏗️ Vector

用于 Source 2 的三维向量。告别 CSSSharp 的混乱。

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
Vector3 builtinVec = vector.ToBuiltin();
```

### Normalize

```csharp
void Normalize()
```

**用法示例:**
```csharp
vec.Normalize();
```

### Normalized

```csharp
Vector Normalized()
```

**返回值:** `Vector`

**用法示例:**
```csharp
Vector normalizedVec = existingVector.Normalized();
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
var (x, y, z) = vector;
```

### ToQAngles

```csharp
QAngle ToQAngles()
```

将此前向向量转换为欧拉QAngle（俯仰角、偏航角、滚转角）。用法：<c>forward.ToQAngles(out var angles);</c>

**返回值:** `QAngle` - 结果 <see cref="QAngle"/>。

**用法示例:**
```csharp
var angles = forward.ToQAngles();
```

### Serialize

```csharp
string Serialize(IFormatProvider? formatProvider = null)
```

将向量序列化为字符串。返回示例："100 200 300"

**参数:**

- `formatProvider` (`IFormatProvider?`) = `null` - 用于字符串的格式提供程序。为null则使用默认提供程序。

**返回值:** `string` - 以字符串形式序列化后的向量。

**用法示例:**
```csharp
string result = vector.Serialize(null);
```

### Deserialize (静态)

```csharp
Vector Deserialize(string input, IFormatProvider? formatProvider = null)
```

从字符串反序列化向量。示例输入："100 200 300"

**参数:**

- `input` (`string`) - 以字符串形式序列化后的向量。
- `formatProvider` (`IFormatProvider?`) = `null` - 用于字符串的格式提供程序。为null则使用默认提供程序。

**返回值:** `Vector` - 反序列化后的向量。

**用法示例:**
```csharp
var vector = Vector.Deserialize("100 200 300", null);
```

### TryDeserialize (静态)

```csharp
bool TryDeserialize([NotNullWhen(true )
```

尝试从字符串反序列化向量。示例输入："100 200 300"

**参数:**

- `` (`[NotNullWhen(true`)

**返回值:** `bool` - 如果反序列化成功则为 true，否则为 false。

**用法示例:**
```csharp
if (Vector.TryDeserialize("100 200 300", out var vector)) { }
```

### TryDeserialize (静态)

```csharp
bool TryDeserialize([NotNullWhen(true )
```

尝试从字符串反序列化向量。示例输入："100 200 300"

**参数:**

- `` (`[NotNullWhen(true`)

**返回值:** `bool` - 如果反序列化成功则为 true，否则为 false。

**用法示例:**
```csharp
if (Vector.TryDeserialize("100 200 300", out var vector)) { }
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
float distSq = player.Location.Distance2DSquared(target.Location);
```

### Length2D

```csharp
float Length2D()
```

**返回值:** `float`

**用法示例:**
```csharp
float len = vector.Length2D();
```

### Length2DSquared

```csharp
float Length2DSquared()
```

**返回值:** `float`

**用法示例:**
```csharp
float lenSq = vector.Length2DSquared();
```

### Normalize2D

```csharp
void Normalize2D()
```

**用法示例:**
```csharp
vector.Normalize2D();
```

### Normalized2D

```csharp
Vector Normalized2D()
```

**返回值:** `Vector`

**用法示例:**
```csharp
var normalized = player.Location.Normalized2D();
```

