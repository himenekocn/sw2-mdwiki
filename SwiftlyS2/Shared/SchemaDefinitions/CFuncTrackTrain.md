# 🔌 CFuncTrackTrain

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseModelEntity`

**实现接口:** `ISchemaClass\<CFuncTrackTrain\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Ppath` | `ref CHandle\<CPathTrack\>` | get | - |
| `Length` | `ref float` | get | - |
| `PosPrev` | `ref Vector` | get | - |
| `Prev` | `ref QAngle` | get | - |
| `ControlMins` | `ref Vector` | get | - |
| `ControlMaxs` | `ref Vector` | get | - |
| `LastBlockPos` | `ref Vector` | get | - |
| `LastBlockTick` | `ref int` | get | - |
| `Volume` | `ref float` | get | - |
| `Bank` | `ref float` | get | - |
| `OldSpeed` | `ref float` | get | - |
| `BlockDamage` | `ref float` | get | - |
| `Height` | `ref float` | get | - |
| `MaxSpeed` | `ref float` | get | - |
| `Dir` | `ref float` | get | - |
| `SoundMove` | `string` | get, set | - |
| `SoundMovePing` | `string` | get, set | - |
| `SoundStart` | `string` | get, set | - |
| `SoundStop` | `string` | get, set | - |
| `StrPathTarget` | `string` | get, set | - |
| `MoveSoundMinDuration` | `ref float` | get | - |
| `MoveSoundMaxDuration` | `ref float` | get | - |
| `NextMoveSoundTime` | `GameTime_t` | get | - |
| `MoveSoundMinPitch` | `ref float` | get | - |
| `MoveSoundMaxPitch` | `ref float` | get | - |
| `OrientationType` | `ref TrainOrientationType_t` | get | - |
| `VelocityType` | `ref TrainVelocityType_t` | get | - |
| `OnStart` | `ref CEntityIOOutput` | get | - |
| `OnNext` | `ref CEntityIOOutput` | get | - |
| `OnArrivedAtDestinationNode` | `ref CEntityIOOutput` | get | - |
| `ManualSpeedChanges` | `ref bool` | get | - |
| `DesiredSpeed` | `ref float` | get | - |
| `SpeedChangeTime` | `GameTime_t` | get | - |
| `AccelSpeed` | `ref float` | get | - |
| `DecelSpeed` | `ref float` | get | - |
| `AccelToSpeed` | `ref bool` | get | - |
| `NextMPSoundTime` | `GameTime_t` | get | - |

