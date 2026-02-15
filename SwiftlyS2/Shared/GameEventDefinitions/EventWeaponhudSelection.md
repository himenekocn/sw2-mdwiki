# 🔌 EventWeaponhudSelection

事件 "weaponhud_selection"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventWeaponhudSelection\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 此事件所适用的玩家 <br/> 类型：玩家控制器与载具 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 此事件所适用的玩家 <br/> 类型：玩家控制器与载具 |
| `UserId` | `int` | get, set | 此事件所适用的玩家 <br/> 类型：玩家控制器与载具 |
| `Mode` | `byte` | get, set | EWeaponHudSelectionMode (切换 / 拾取 / 丢弃) <br/> 类型: 字节 |
| `EntIndex` | `int` | get, set | 武器实体索引 <br/> 类型：长整型 |

