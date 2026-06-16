<a id="vector2d"></a>

# 🏗️ Vector2D

用于Source 2的二维向量。

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `X` | `float` | - | - |
| `Y` | `float` | - | - |

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Zero` | `Vector2D` | - | - |
| `One` | `Vector2D` | - | - |

## ⚙️ 方法

### ToBuiltin

```csharp
System.Numerics.Vector2 ToBuiltin()
```

**返回值:** `System.Numerics.Vector2`

**用法示例:**
```csharp
System.Numerics.Vector2 builtin = vector.ToBuiltin();
```

### FromBuiltin (静态)

```csharp
Vector2D FromBuiltin(System.Numerics.Vector2 vector)
```

**参数:**

- `vector` (`System.Numerics.Vector2`)

**返回值:** `Vector2D`

**用法示例:**
```csharp
var builtinVec = new System.Numerics.Vector2(1.0f, 2.0f);
var vec2D = Vector2D.FromBuiltin(builtinVec);
```

### Normalize

```csharp
void Normalize()
```

**用法示例:**
```csharp
var v = Vector2D.Zero; v.Normalize();
```

### Normalized

```csharp
Vector2D Normalized()
```

**返回值:** `Vector2D`

**用法示例:**
```csharp
Vector2D normalizedVec = existingVector.Normalized();
```

### Deconstruct

```csharp
void Deconstruct(out float x, out float y)
```

**参数:**

- `x` (`out float`)
- `y` (`out float`)

**用法示例:**
```csharp
var v = Vector2D.Zero;
v.Deconstruct(out float x, out float y);
```

