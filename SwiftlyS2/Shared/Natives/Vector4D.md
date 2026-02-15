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

## ⚙️ 方法

### ToBuiltin

```csharp
System.Numerics.Vector4 ToBuiltin()
```

**返回值:** `System.Numerics.Vector4`

### FromBuiltin (静态)

```csharp
Vector4D FromBuiltin(System.Numerics.Vector4 vector)
```

**参数:**

- `vector` (`System.Numerics.Vector4`)

**返回值:** `Vector4D`

### GetHashCode

```csharp
int GetHashCode()
```

**返回值:** `int`

### ToString

```csharp
string ToString()
```

**返回值:** `string`

### Normalize

```csharp
void Normalize()
```

### Normalized

```csharp
Vector4D Normalized()
```

**返回值:** `Vector4D`

### Deconstruct

```csharp
void Deconstruct(out float x, out float y, out float z, out float w)
```

**参数:**

- `x` (`out float`)
- `y` (`out float`)
- `z` (`out float`)
- `w` (`out float`)

