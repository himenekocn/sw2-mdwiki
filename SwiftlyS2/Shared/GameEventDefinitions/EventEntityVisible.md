# 🔌 EventEntityVisible

事件 "entity_visible"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventEntityVisible\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 看到该实体的玩家 <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 看到该实体的玩家 <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 看到该实体的玩家 <br/> 类型：玩家控制器 |
| `Subject` | `int` | get, set | 他们所看到的实体的实体索引 <br/> 类型：长整型 |
| `ClassName` | `string` | get, set | 他们所看到实体的类名 <br/> 类型：字符串 |
| `EntityName` | `string` | get, set | 他们所看到的实体的名称 <br/> 类型：字符串 |

