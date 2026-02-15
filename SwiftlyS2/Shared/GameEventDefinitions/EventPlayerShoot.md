# 🔌 EventPlayerShoot

事件 "player_shoot" 玩家开火

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerShoot\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户ID <br/> 类型：玩家控制器与载具 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户ID <br/> 类型：玩家控制器与载具 |
| `UserId` | `int` | get, set | 服务器上的用户ID <br/> 类型：玩家控制器与载具 |
| `Weapon` | `byte` | get, set | 武器 ID <br/> 类型：字节 |
| `Mode` | `byte` | get, set | 武器模式 <br/> 类型：字节 |

