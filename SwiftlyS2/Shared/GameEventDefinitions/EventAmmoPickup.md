# 🔌 EventAmmoPickup

事件 "ammo_pickup"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAmmoPickup\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Item` | `string` | get, set | 要么是像 'tmp' 或 'hegrenade' 这样的武器，要么是像 'nvgs' 这样的物品 <br/> 类型：字符串 |
| `Index` | `int` | get, set | 武器实体索引 <br/> 类型：长整型 |

