# 🏗️ CMoveData

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `OutWishVel` | `Vector` | - | - |
| `OldAngles` | `QAngle` | - | - |
| `InputRotated` | `Vector` | - | 世界空间输入向量。用于与移动服务的前一旋转进行对比，以处理地面移动相关逻辑。 |
| `ContinuousAcceleration` | `Vector` | - | 每秒平方单位的连续加速度（单位：u/s²）。 |
| `FrameVelocityDelta` | `Vector` | - | 瞬时间隔的 u/s 变化。空中加速度绕过每秒加速度限制，将其冲量的一半施加到速度上，其余部分直接计入此项。 |
| `MaxSpeed` | `float` | - | - |
| `ClientMaxSpeed` | `float` | - | - |
| `FrictionDecel` | `float` | - | - |
| `InAir` | `bool` | - | - |

