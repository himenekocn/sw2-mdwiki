<a id="quaternion"></a>

# 🏗️ Quaternion

四元数，本质上由4个浮点数组成。

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
System.Numerics.Quaternion builtin = quaternion.ToBuiltin();
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
var builtinQuat = System.Numerics.Quaternion.Identity;
var result = Quaternion.FromBuiltin(builtinQuat);
```

