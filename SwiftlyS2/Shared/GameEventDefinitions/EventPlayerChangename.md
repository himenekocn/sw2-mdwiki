# 🔌 EventPlayerChangename

事件 "player_changename"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerChangename\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户ID <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户ID <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 服务器上的用户ID <br/> 类型：玩家控制器 |
| `OldName` | `string` | get, set | 玩家旧（当前）名称 <br/> 类型：字符串 |
| `NewName` | `string` | get, set | 玩家新名称 <br/> 类型：字符串 |

