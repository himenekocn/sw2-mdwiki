# 🏗️ Vector2D

2-Dimensional vector for source 2.

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `X` | `float` | - | - |
| `Y` | `float` | - | - |

## ⚙️ 方法

### ToBuiltin

```csharp
System.Numerics.Vector2 ToBuiltin()
```

**返回值:** `System.Numerics.Vector2`

### FromBuiltin (静态)

```csharp
Vector2D FromBuiltin(System.Numerics.Vector2 vector)
```

**参数:**

- `vector` (`System.Numerics.Vector2`)

**返回值:** `Vector2D`

### Normalize

```csharp
void Normalize()
```

### Normalized

```csharp
Vector2D Normalized()
```

**返回值:** `Vector2D`

### Deconstruct

```csharp
void Deconstruct(out float x, out float y)
```

**参数:**

- `x` (`out float`)
- `y` (`out float`)

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

