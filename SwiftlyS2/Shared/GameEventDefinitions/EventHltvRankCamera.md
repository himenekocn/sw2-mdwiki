# 🔌 EventHltvRankCamera

事件 "hltv_rank_camera" 一个相机排名

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvRankCamera\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Index` | `byte` | get, set | 固定摄像机索引 <br/> 类型：字节 |
| `Rank` | `float` | get, set | 排名，此摄像头视图的有趣程度 <br/> 类型：浮点数 |
| `TargetController` | `CCSPlayerController` | get | 最佳/最近的目标实体 <br/> 类型：玩家控制器 |
| `TargetPawn` | `CCSPlayerPawn` | get | 最佳/最近的目标实体 <br/> 类型：玩家控制器 |
| `Target` | `int` | get, set | 最佳/最近的目标实体 <br/> 类型：玩家控制器 |

