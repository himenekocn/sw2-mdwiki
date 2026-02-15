# 🔌 EventHltvRankEntity

事件 "hltv_rank_entity" 一个实体排名

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvRankEntity\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 玩家槽位 <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 玩家槽位 <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 玩家槽位 <br/> 类型：玩家控制器 |
| `Rank` | `float` | get, set | 排名，此实体被查看的有趣程度 <br/> 类型：浮点数 |
| `TargetController` | `CCSPlayerController` | get | 最佳/最近的目标实体 <br/> 类型：玩家控制器 |
| `TargetPawn` | `CCSPlayerPawn` | get | 最佳/最近的目标实体 <br/> 类型：玩家控制器 |
| `Target` | `int` | get, set | 最佳/最近的目标实体 <br/> 类型：玩家控制器 |

