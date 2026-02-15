# 🔌 EventPlayerInfo

事件 "player_info" 玩家更改了其名称

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerInfo\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | get, set | 玩家名称 <br/> 类型：字符串 |
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户ID（在服务器上唯一）<br/>类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户ID（在服务器上唯一）<br/>类型：玩家控制器 |
| `UserId` | `int` | get, set | 服务器上的用户ID（在服务器上唯一）<br/>类型：玩家控制器 |
| `SteamID` | `ulong` | get, set | 玩家网络（例如 Steam）ID <br/> 类型：uint64 |
| `Bot` | `bool` | get, set | 如果玩家是AI机器人则为true <br/> 类型：布尔值 |

