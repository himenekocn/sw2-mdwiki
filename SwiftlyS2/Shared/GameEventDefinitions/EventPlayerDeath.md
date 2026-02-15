# 🔌 EventPlayerDeath

事件 "player_death" 是一个游戏事件，名称最长可为 32 个字符。

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerDeath\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 已死亡的用户ID <br/> 类型：玩家控制器与载具 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 已死亡的用户ID <br/> 类型：玩家控制器与载具 |
| `UserId` | `int` | get, set | 已死亡的用户ID <br/> 类型：玩家控制器与载具 |
| `AttackerController` | `CCSPlayerController` | get | 杀死该实体的用户ID <br/> 类型：玩家控制器与载具 |
| `AttackerPawn` | `CCSPlayerPawn` | get | 杀死该实体的用户ID <br/> 类型：玩家控制器与载具 |
| `Attacker` | `int` | get, set | 杀死该实体的用户ID <br/> 类型：玩家控制器与载具 |
| `AssisterController` | `CCSPlayerController` | get | 参与击杀的玩家 <br/> 类型：玩家控制器与游戏体 |
| `AssisterPawn` | `CCSPlayerPawn` | get | 参与击杀的玩家 <br/> 类型：玩家控制器与游戏体 |
| `Assister` | `int` | get, set | 参与击杀的玩家 <br/> 类型：玩家控制器与游戏体 |
| `AssistedFlash` | `bool` | get, set | 助手协助了闪存 <br/> 类型：布尔值 |
| `Weapon` | `string` | get, set | 武器名称 杀手使用 <br/> 类型：字符串 |
| `WeaponItemid` | `string` | get, set | 武器杀手使用的物品ID <br/> 类型：字符串 |
| `WeaponFauxitemid` | `string` | get, set | 武器杀手使用的伪物品ID <br/> 类型：字符串 |
| `WeaponOriginalownerXuid` | `string` | get, set | 类型：字符串 |
| `Headshot` | `bool` | get, set | 表示爆头 <br/> 类型：布尔值 |
| `Dominated` | `short` | get, set | 凶手是否通过此击杀压制了受害者 <br/> 类型：简短 |
| `Revenge` | `short` | get, set | 凶手是否通过此次击杀向受害者复仇 <br/> 类型：简短 |
| `Wipe` | `short` | get, set | 是否导致小队全灭 <br/> 类型：short |
| `Penetrated` | `short` | get, set | 击杀目标前穿透的物体数量 <br/> 类型：short |
| `NoReplay` | `bool` | get, set | 如果重播数据不可用，则此属性将存在并设置为 false <br/> 类型：布尔值 |
| `NoScope` | `bool` | get, set | 击杀发生时未处于瞄准状态，用于死亡通知图标 <br/> 类型：布尔值 |
| `ThruSmoke` | `bool` | get, set | 射线武器穿透烟雾弹 <br/> 类型：布尔值 |
| `AttackerBlind` | `bool` | get, set | 攻击者因闪光弹致盲 <br/> 类型：布尔值 |
| `Distance` | `float` | get, set | 与受害者的距离（单位：米）<br/>类型：浮点数 |
| `DmgHealth` | `short` | get, set | 对健康造成的伤害 <br/> 类型：short |
| `DmgArmor` | `byte` | get, set | 对护甲造成的伤害 <br/> 类型: 字节 |
| `HitGroup` | `byte` | get, set | 被损坏的命中组 <br/> 类型：字节 |
| `AttackerInAir` | `bool` | get, set | 攻击者处于空中 <br/> 类型：布尔值 |

