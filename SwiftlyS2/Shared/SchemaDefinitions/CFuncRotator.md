# 🔌 CFuncRotator

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseModelEntity`

**实现接口:** `ISchemaClass\<CFuncRotator\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `RotatorTarget` | `ref CHandle\<CBaseEntity\>` | get | - |
| `IsRotating` | `ref bool` | get | - |
| `IsReversing` | `ref bool` | get | - |
| `TimeToReachMaxSpeed` | `ref float` | get | - |
| `TimeToReachZeroSpeed` | `ref float` | get | - |
| `DistanceAlongArcTraveled` | `ref float` | get | - |
| `TimeToWaitOscillate` | `ref float` | get | - |
| `TimeRotationStart` | `GameTime_t` | get | - |
| `LSPrevChange` | `ref Quaternion` | get | - |
| `WSPrev` | `ref Quaternion` | get | - |
| `WSInit` | `ref Quaternion` | get | - |
| `LSInit` | `ref Quaternion` | get | - |
| `LSOrientation` | `ref Quaternion` | get | - |
| `OnRotationStarted` | `ref CEntityIOOutput` | get | - |
| `OnRotationCompleted` | `ref CEntityIOOutput` | get | - |
| `OnOscillate` | `ref CEntityIOOutput` | get | - |
| `OnOscillateStartArrive` | `ref CEntityIOOutput` | get | - |
| `OnOscillateStartDepart` | `ref CEntityIOOutput` | get | - |
| `OnOscillateEndArrive` | `ref CEntityIOOutput` | get | - |
| `OnOscillateEndDepart` | `ref CEntityIOOutput` | get | - |
| `OscillateDepart` | `ref bool` | get | - |
| `OscillateCount` | `ref int` | get | - |
| `RotateType` | `ref CFuncRotator__Rotate_t` | get | - |
| `PrevRotateType` | `ref CFuncRotator__Rotate_t` | get | - |
| `HasTargetOverride` | `ref bool` | get | - |
| `OrientationOverride` | `ref Quaternion` | get | - |
| `SpaceOverride` | `ref RotatorTargetSpace_t` | get | - |
| `AngularVelocity` | `ref QAngle` | get | - |
| `LookAtForcedUp` | `ref Vector` | get | - |
| `StrRotatorTarget` | `string` | get, set | - |
| `RecordHistory` | `ref bool` | get | - |
| `RotatorHistory` | `ref CUtlVector\<RotatorHistoryEntry_t\>` | get | - |
| `ReturningToPreviousOrientation` | `ref bool` | get | - |
| `RotatorQueue` | `ref CUtlVector\<RotatorQueueEntry_t\>` | get | - |
| `RotatorQueueHistory` | `ref CUtlVector\<RotatorHistoryEntry_t\>` | get | - |
| `SolidType` | `ref SolidType_t` | get | - |
| `SpeedFromMover` | `ref CHandle\<CFuncMover\>` | get | - |
| `SpeedFromMover1` | `string` | get, set | - |
| `SpeedScale` | `ref float` | get | - |
| `MinYawRotation` | `ref float` | get | - |
| `MaxYawRotation` | `ref float` | get | - |

