# 🔌 CPhysHinge

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CPhysConstraint`

**实现接口:** `ISchemaClass\<CPhysHinge\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SoundInfo` | `ConstraintSoundInfo` | get | - |
| `NotifyMinLimitReached` | `ref CEntityIOOutput` | get | - |
| `NotifyMaxLimitReached` | `ref CEntityIOOutput` | get | - |
| `AtMinLimit` | `ref bool` | get | - |
| `AtMaxLimit` | `ref bool` | get | - |
| `Hinge` | `constraint_hingeparams_t` | get | - |
| `HingeFriction` | `ref float` | get | - |
| `SystemLoadScale` | `ref float` | get | - |
| `IsAxisLocal` | `ref bool` | get | - |
| `MinRotation` | `ref float` | get | - |
| `MaxRotation` | `ref float` | get | - |
| `InitialRotation` | `ref float` | get | - |
| `MotorFrequency` | `ref float` | get | - |
| `MotorDampingRatio` | `ref float` | get | - |
| `AngleSpeed` | `ref float` | get | - |
| `AngleSpeedThreshold` | `ref float` | get | - |
| `LimitsDebugVisRotation` | `ref float` | get | - |
| `OnStartMoving` | `ref CEntityIOOutput` | get | - |
| `OnStopMoving` | `ref CEntityIOOutput` | get | - |

