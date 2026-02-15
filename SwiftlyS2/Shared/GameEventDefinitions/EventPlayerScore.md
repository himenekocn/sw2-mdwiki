# 🔌 EventPlayerScore

事件 "player_score" 玩家分数已更改

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerScore\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户ID <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户ID <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 服务器上的用户ID <br/> 类型：玩家控制器 |
| `Kills` | `short` | get, set | 击杀数 <br/> 类型：短整型 |
| `Deaths` | `short` | get, set | 死亡人数 <br/> 类型：短整型 |
| `Score` | `short` | get, set | 总游戏分数 <br/> 类型：短整型 |

