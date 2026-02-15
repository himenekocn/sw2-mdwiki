# 🏗️ CMoveData

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `OutWishVel` | `Vector` | - | - |
| `OldAngles` | `QAngle` | - | - |
| `InputRotated` | `Vector` | - | 世界空间输入向量。用于与移动服务的先前旋转进行比较，以处理地面移动相关逻辑。 |
| `ContinuousAcceleration` | `Vector` | - | 连续加速度，单位为每秒平方单位 (u/s²)。 |
| `FrameVelocityDelta` | `Vector` | - | 瞬时速度变化量。空气加速度会绕过每秒加速度，将其冲量的一半应用于速度，其余部分则直接作用于此。 |
| `MaxSpeed` | `float` | - | - |
| `ClientMaxSpeed` | `float` | - | - |
| `FrictionDecel` | `float` | - | - |
| `InAir` | `bool` | - | - |

