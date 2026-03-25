# 🏗️ Quaternion

四元数，本质上由 4 个浮点数构成。

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
var builtin = quaternion.ToBuiltin();
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
var builtin = new System.Numerics.Quaternion(0, 0, 0, 1);
var swiftlyQuat = Quaternion.FromBuiltin(builtin);
```

