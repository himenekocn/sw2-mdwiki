# 🔌 EventGgKilledEnemy

事件 "gg_killed_enemy"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGgKilledEnemy\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `VictimIDController` | `CCSPlayerController` | get | 已死亡的用户ID <br/> 类型：玩家控制器 |
| `VictimIDPawn` | `CCSPlayerPawn` | get | 已死亡的用户ID <br/> 类型：玩家控制器 |
| `VictimID` | `int` | get, set | 已死亡的用户ID <br/> 类型：玩家控制器 |
| `AttackerIDController` | `CCSPlayerController` | get | 击杀者用户ID <br/> 类型：玩家控制器 |
| `AttackerIDPawn` | `CCSPlayerPawn` | get | 击杀者用户ID <br/> 类型：玩家控制器 |
| `AttackerID` | `int` | get, set | 击杀者用户ID <br/> 类型：玩家控制器 |
| `Dominated` | `short` | get, set | 凶手是否通过此击杀压制了受害者 <br/> 类型：简短 |
| `Revenge` | `short` | get, set | 凶手是否通过此次击杀向受害者复仇 <br/> 类型：简短 |
| `Bonus` | `bool` | get, set | 杀手是否使用奖励武器杀人？<br/>类型：布尔值 |

