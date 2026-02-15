# 🔌 CBaseUserCmdPB

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CBaseUserCmdPB\>`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `LegacyCommandNumber` | `int` | get, set | - |
| `ClientTick` | `int` | get, set | - |
| `PredictionOffsetTicksX256` | `uint` | get, set | - |
| `ButtonsPb` | `CInButtonStatePB` | get, set | - |
| `Viewangles` | `QAngle` | get, set | - |
| `Forwardmove` | `float` | get, set | - |
| `Leftmove` | `float` | get, set | - |
| `Upmove` | `float` | get, set | - |
| `Impulse` | `int` | get, set | - |
| `Weaponselect` | `int` | get, set | - |
| `RandomSeed` | `int` | get, set | - |
| `Mousedx` | `int` | get, set | - |
| `Mousedy` | `int` | get, set | - |
| `PawnEntityHandle` | `uint` | get, set | - |
| `SubtickMoves` | `IProtobufRepeatedFieldSubMessageType\<CSubtickMoveStep\>` | get, set | - |
| `MoveCrc` | `byte[]` | get, set | - |
| `ConsumedServerAngleChanges` | `uint` | get, set | - |
| `CmdFlags` | `int` | get, set | - |
| `ExecutionNotes` | `CBaseUserCmdExecutionNotes` | get | - |

