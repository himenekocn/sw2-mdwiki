# 🔌 EventShowDeathpanel

事件 "show_deathpanel"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventShowDeathpanel\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `VictimController` | `CCSPlayerController` | get | 被击杀者的结束索引 <br/> 类型：玩家控制器与Pawn |
| `VictimPawn` | `CCSPlayerPawn` | get | 被击杀者的结束索引 <br/> 类型：玩家控制器与Pawn |
| `Victim` | `int` | get, set | 被击杀者的结束索引 <br/> 类型：玩家控制器与Pawn |
| `Killer` | `nint` | get, set | 杀手实体的实体索引 <br/> 类型：ehandle |
| `KillerControllerController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `KillerControllerPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `KillerController` | `int` | get, set | 类型：玩家控制器 |
| `HitsTaken` | `short` | get, set | 类型：短整型 |
| `DamageTaken` | `short` | get, set | 类型：短整型 |
| `HitsGiven` | `short` | get, set | 类型：短整型 |
| `DamageGiven` | `short` | get, set | 类型：短整型 |

