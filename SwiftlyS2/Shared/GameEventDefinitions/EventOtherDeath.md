# 🔌 EventOtherDeath

事件 "other_death"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventOtherDeath\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `OtherID` | `short` | get, set | 其他已死亡的实体ID <br/> 类型：short |
| `OtherType` | `string` | get, set | 其他实体类型 <br/> 类型：字符串 |
| `Attacker` | `short` | get, set | 击杀者的用户ID <br/> 类型：短整型 |
| `Weapon` | `string` | get, set | 武器名称 杀手使用 <br/> 类型：字符串 |
| `WeaponItemid` | `string` | get, set | 武器杀手使用的物品ID <br/> 类型：字符串 |
| `WeaponFauxitemid` | `string` | get, set | 武器杀手使用的伪物品ID <br/> 类型：字符串 |
| `WeaponOriginalownerXuid` | `string` | get, set | 类型：字符串 |
| `Headshot` | `bool` | get, set | 表示爆头 <br/> 类型：布尔值 |
| `Penetrated` | `short` | get, set | 击杀目标前穿透的物体数量 <br/> 类型：short |
| `NoScope` | `bool` | get, set | 击杀发生时未处于瞄准状态，用于死亡通知图标 <br/> 类型：布尔值 |
| `ThruSmoke` | `bool` | get, set | 射线武器穿透烟雾弹 <br/> 类型：布尔值 |
| `AttackerBlind` | `bool` | get, set | 攻击者因闪光弹致盲 <br/> 类型：布尔值 |

