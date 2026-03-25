<a id="vector4d"></a>

# 🏗️ Vector4D

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `X` | `float` | - | - |
| `Y` | `float` | - | - |
| `Z` | `float` | - | - |
| `W` | `float` | - | - |

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Zero` | `Vector4D` | - | - |
| `One` | `Vector4D` | - | - |

## ⚙️ 方法

### ToBuiltin

```csharp
System.Numerics.Vector4 ToBuiltin()
```

**返回值:** `System.Numerics.Vector4`

**用法示例:**
```csharp
System.Numerics.Vector4 builtin = vector4D.ToBuiltin();
```

### FromBuiltin (静态)

```csharp
Vector4D FromBuiltin(System.Numerics.Vector4 vector)
```

**参数:**

- `vector` (`System.Numerics.Vector4`)

**返回值:** `Vector4D`

**用法示例:**
```csharp
var result = Vector4D.FromBuiltin(new System.Numerics.Vector4(1, 2, 3, 4));
```

### Normalize

```csharp
void Normalize()
```

**用法示例:**
```csharp
Vector4D v = default;
v.Normalize();
```

### Normalized

```csharp
Vector4D Normalized()
```

**返回值:** `Vector4D`

**用法示例:**
```csharp
Vector4D result = existingVector.Normalized();
```

### Deconstruct

```csharp
void Deconstruct(out float x, out float y, out float z, out float w)
```

**参数:**

- `x` (`out float`)
- `y` (`out float`)
- `z` (`out float`)
- `w` (`out float`)

**用法示例:**
```csharp
Vector4D vec = Vector4D.UnitW; vec.Deconstruct(out float x, out float y, out float z, out float w);
```

