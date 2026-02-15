# 🔌 EventPlayerSpawned

事件 "player_spawned"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerSpawned\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `InRestart` | `bool` | get, set | 如果存在待重启的情况，则为 true <br/> 类型：布尔值 |

