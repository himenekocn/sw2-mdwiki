# 🔌 EventHltvChase

事件 "hltv_chase" 对单个实体的拍摄

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvChase\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Target1Controller` | `CCSPlayerController` | get | 主要目标索引 <br/> 类型：玩家控制器 |
| `Target1Pawn` | `CCSPlayerPawn` | get | 主要目标索引 <br/> 类型：玩家控制器 |
| `Target1` | `int` | get, set | 主要目标索引 <br/> 类型：玩家控制器 |
| `Target2Controller` | `CCSPlayerController` | get | 次要目标索引或 0 <br/> 类型：玩家控制器 |
| `Target2Pawn` | `CCSPlayerPawn` | get | 次要目标索引或 0 <br/> 类型：玩家控制器 |
| `Target2` | `int` | get, set | 次要目标索引或 0 <br/> 类型：玩家控制器 |
| `Distance` | `short` | get, set | 相机距离 <br/> 类型：短整型 |
| `Theta` | `short` | get, set | 视角水平 <br/> 类型：短整型 |
| `Phi` | `short` | get, set | 视角垂直 <br/> 类型：短整型 |
| `Inertia` | `byte` | get, set | 相机惯性 <br/> 类型：字节 |
| `InEye` | `byte` | get, set | diretcor 建议显示 ineye <br/> 类型：字节 |

