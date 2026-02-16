# 🏗️ FourVectors

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `X` | `fltx4` | - | - |
| `Y` | `fltx4` | - | - |
| `Z` | `fltx4` | - | - |

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `this[int index]` | `Vector` | - | - |

## ⚙️ 方法

### GetVector

```csharp
Vector GetVector(int index)
```

**参数:**

- `index` (`int`)

**返回值:** `Vector`

**用法示例:**
```csharp
Vector v = convar.GetVector(0);
```

### SetVector

```csharp
void SetVector(int index, Vector vector)
```

**参数:**

- `index` (`int`)
- `vector` (`Vector`)

**用法示例:**
```csharp
convar.SetVector(0, Vector.Forward);
```

