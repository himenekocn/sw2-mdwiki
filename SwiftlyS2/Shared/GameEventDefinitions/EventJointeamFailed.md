# 🔌 EventJointeamFailed

事件 "jointeam_failed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventJointeamFailed\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Reason` | `byte` | get, set | 0 = team_full <br/> 类型：字节 |

