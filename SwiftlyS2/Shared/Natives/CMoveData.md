# 🏗️ CMoveData

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `OutWishVel` | `Vector` | - | - |
| `OldAngles` | `QAngle` | - | - |
| `InputRotated` | `Vector` | - | World space input vector. Used to compare against the movement services' previous rotation for ground movement stuff. |
| `ContinuousAcceleration` | `Vector` | - | Continuous acceleration in units per second squared (u/s²). |
| `FrameVelocityDelta` | `Vector` | - | Immediate delta in u/s. Air acceleration bypasses per second acceleration, applies up to half of its impulse to the velocity and the rest goes straight into this. |
| `MaxSpeed` | `float` | - | - |
| `ClientMaxSpeed` | `float` | - | - |
| `FrictionDecel` | `float` | - | - |
| `InAir` | `bool` | - | - |

