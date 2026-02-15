# 🔌 EventPlayerTeam

事件 "player_team"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerTeam\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 玩家 <br/> 类型：玩家控制器与 pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 玩家 <br/> 类型：玩家控制器与 pawn |
| `UserId` | `int` | get, set | 玩家 <br/> 类型：玩家控制器与 pawn |
| `Team` | `byte` | get, set | 团队标识 <br/> 类型：字节 |
| `OldTeam` | `byte` | get, set | 旧团队 ID <br/> 类型：字节 |
| `Disconnect` | `bool` | get, set | 团队变更，因为玩家断开连接 <br/> 类型：布尔值 |
| `Silent` | `bool` | get, set | 类型：布尔值 |
| `Name` | `string` | get, set | 类型：字符串 |
| `IsBot` | `bool` | get, set | 如果玩家是机器人则为 true <br/> 类型：布尔值 |

