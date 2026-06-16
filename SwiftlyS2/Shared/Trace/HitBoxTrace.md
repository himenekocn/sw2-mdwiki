<a id="hitboxtrace"></a>

# 🏗️ HitBoxTrace

**命名空间:** `SwiftlyS2.Shared.Trace`

**类型:** `struct`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | get, set | 命中盒的名称。 |
| `SurfaceProperty` | `string` | get, set | 与此碰撞体关联的表面属性名称。 |
| `BoneName` | `string` | get, set | 此命中框所附加到的骨骼名称。 |
| `MinBounds` | `Vector` | get, set | 命中框在三维空间中的最小边界。 |
| `MaxBounds` | `Vector` | get, set | 3D空间中碰撞箱的最大边界。 |
| `ShapeRadius` | `float` | get, set | 此碰撞箱所用形状的半径。 |
| `BoneNameHash` | `CUtlStringToken` | get, set | 用于加速查找的骨骼名称哈希令牌。 |
| `GroupId` | `HitGroup_t` | get, set | 与此命中框关联的命中组ID，用于决定伤害行为。 |
| `ShapeType` | `byte` | get, set | 此命中框使用的形状类型。 |
| `TranslationOnly` | `bool` | get, set | 指示此命中框是否仅使用平移，不包含旋转。 |
| `CRC` | `uint` | get, set | 命中框数据的CRC校验和。 |
| `RenderColor` | `Color` | get, set | 击中箱的渲染颜色，通常用于调试可视化。 |
| `HitBoxIndex` | `ushort` | get, set | 该命中盒在实体命中盒列表中的索引。 |
| `ForcedTransform` | `bool` | get, set | 指示此命中框是否应用了强制变换。 |
| `ForcedTransformObject` | `CTransform` | get, set | 定义此碰撞箱额外位置或旋转的强制变换对象。 |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

