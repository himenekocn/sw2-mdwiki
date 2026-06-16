<a id="igamehookmovement"></a>

# 🔌 IGameHookMovement

**命名空间:** `SwiftlyS2.Shared.GameHooks`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `RunCommand` | `IRunCommandMovementHook` | get | 当玩家移动tick被处理时触发Hook。 |
| `SetupMove` | `ISetupMoveMovementHook` | get | 当玩家移动数据设置完成时触发的钩子。 |
| `ProcessMovement` | `IProcessMovementMovementHook` | get | 当玩家移动数据正在处理时触发的钩子。 |
| `CheckFalling` | `ICheckFallingMovementHook` | get | 当执行玩家下落检查时触发的钩子。 |
| `CategorizePosition` | `ICategorizePositionMovementHook` | get | 当玩家位置被分类时触发的钩子。 |
| `TryPlayerMove` | `ITryPlayerMoveMovementHook` | get | 当玩家尝试移动时触发的钩子。 |
| `WalkMove` | `IWalkMoveMovementHook` | get | 当玩家执行行走移动时触发的钩子。 |
| `Friction` | `IFrictionMovementHook` | get | 当摩擦应用于玩家时触发的钩子。 |
| `AirAccelerate` | `IAirAccelerateMovementHook` | get | 当玩家执行空中加速时触发的钩子。 |
| `AirMove` | `IAirMoveMovementHook` | get | 当玩家执行空中移动时触发的钩子。 |
| `OnJumpModern` | `IOnJumpModernMovementHook` | get | 当玩家执行现代跳跃时触发的钩子。 |
| `OnJumpLegacy` | `IOnJumpLegacyMovementHook` | get | 当玩家执行传统跳跃时触发的钩子。 |
| `CheckJumpButtonModern` | `ICheckJumpButtonModernMovementHook` | get | 当检查现代跳跃按钮时触发的钩子。 |
| `CheckJumpButtonLegacy` | `ICheckJumpButtonLegacyMovementHook` | get | 当检测到旧版跳跃按钮时触发的钩子。 |
| `LadderMove` | `ILadderMoveMovementHook` | get | 当玩家执行梯子移动时触发的钩子。 |
| `CanUnduck` | `ICanUnduckMovementHook` | get | 当执行玩家解除蹲伏检查时触发的钩子。 |
| `Duck` | `IDuckMovementHook` | get | 当玩家执行蹲下操作时触发的钩子。 |
| `CheckVelocity` | `ICheckVelocityMovementHook` | get | 当检测玩家速度时触发的钩子。 |
| `WaterMove` | `IWaterMoveMovementHook` | get | 当玩家执行水上移动时触发的钩子。 |
| `CheckWater` | `ICheckWaterMovementHook` | get | 当执行玩家水检测时触发的钩子。 |
| `MoveInit` | `IMoveInitMovementHook` | get | 当玩家移动初始化时触发的钩子。 |
| `FullWalkMove` | `IFullWalkMoveMovementHook` | get | 当玩家执行完整行走移动时触发的钩子。 |
| `CheckParameters` | `ICheckParametersMovementHook` | get | 当玩家移动参数被检查时触发的钩子。 |
| `PlayerMove` | `IPlayerMoveMovementHook` | get | 当玩家移动被处理时触发的钩子。 |
| `GroundAccelerate` | `IGroundAccelerateMovementHook` | get | 当向玩家施加地面加速度时触发的钩子。 |

