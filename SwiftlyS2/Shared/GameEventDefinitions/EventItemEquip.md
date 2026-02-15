# 🔌 EventItemEquip

事件 "item_equip"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventItemEquip\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Item` | `string` | get, set | 要么是像 'tmp' 或 'hegrenade' 这样的武器，要么是像 'nvgs' 这样的物品 <br/> 类型：字符串 |
| `DefIndex` | `int` | get, set | 类型：长整型 |
| `CanZoom` | `bool` | get, set | 类型：布尔值 |
| `HasSilencer` | `bool` | get, set | 类型：布尔值 |
| `IsSilenced` | `bool` | get, set | 类型：布尔值 |
| `HasTracers` | `bool` | get, set | 类型：布尔值 |
| `WepType` | `short` | get, set | 类型：短整型 |
| `IsPainted` | `bool` | get, set | 类型：布尔值 |

