# 🏗️ Quaternion

四元数，基本上是4个浮点数。

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
| `Zero` | `Quaternion` | - | - |
| `One` | `Quaternion` | - | - |

## ⚙️ 方法

### ToBuiltin

```csharp
System.Numerics.Quaternion ToBuiltin()
```

**返回值:** `System.Numerics.Quaternion`

**用法示例:**
```csharp
Quaternion q = Quaternion.Identity;
Quaternion builtin = q.ToBuiltin();
```

### FromBuiltin (静态)

```csharp
Quaternion FromBuiltin(System.Numerics.Quaternion quaternion)
```

**参数:**

- `quaternion` (`System.Numerics.Quaternion`)

**返回值:** `Quaternion`

**用法示例:**
```csharp
Quaternion q = Quaternion.FromBuiltin(new System.Numerics.Quaternion(1, 2, 3, 4));
```

