# 🔌 CBtActionAim

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBtNode`

**实现接口:** `ISchemaClass\<CBtActionAim\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SensorInputKey` | `string` | get, set | - |
| `AimReadyKey` | `string` | get, set | - |
| `ZoomCooldownTimestamp` | `ref float` | get | - |
| `DoneAiming` | `ref bool` | get | - |
| `LerpStartTime` | `ref float` | get | - |
| `NextLookTargetLerpTime` | `ref float` | get | - |
| `PenaltyReductionRatio` | `ref float` | get | - |
| `NextLookTarget` | `ref QAngle` | get | - |
| `AimTimer` | `CountdownTimer` | get | - |
| `SniperHoldTimer` | `CountdownTimer` | get | - |
| `FocusIntervalTimer` | `CountdownTimer` | get | - |
| `Acquired` | `ref bool` | get | - |

