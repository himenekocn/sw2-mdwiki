# 🔌 EventPlayerHurt

事件 "player_hurt"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerHurt\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 受伤的玩家 <br/> 类型：玩家控制器与模型 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 受伤的玩家 <br/> 类型：玩家控制器与模型 |
| `UserId` | `int` | get, set | 受伤的玩家 <br/> 类型：玩家控制器与模型 |
| `AttackerController` | `CCSPlayerController` | get | 攻击的玩家 <br/> 类型：玩家控制器与模型 |
| `AttackerPawn` | `CCSPlayerPawn` | get | 攻击的玩家 <br/> 类型：玩家控制器与模型 |
| `Attacker` | `int` | get, set | 攻击的玩家 <br/> 类型：玩家控制器与模型 |
| `Health` | `byte` | get, set | 剩余生命值 <br/> 类型：字节 |
| `Armor` | `byte` | get, set | 剩余护甲值 <br/> 类型：字节 |
| `Weapon` | `string` | get, set | 攻击者使用的武器名称，若未使用则为“world”<br/>类型：字符串 |
| `DmgHealth` | `short` | get, set | 对健康造成的伤害 <br/> 类型：short |
| `DmgArmor` | `byte` | get, set | 对护甲造成的伤害 <br/> 类型: 字节 |
| `HitGroup` | `byte` | get, set | 被损坏的命中组 <br/> 类型：字节 |

