# 🔌 EventPlayerChat

事件 "player_chat" 公共玩家聊天

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerChat\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TeamOnly` | `bool` | get, set | 如果团队仅聊天则为 true <br/> 类型：布尔值 |
| `UserIdController` | `CCSPlayerController` | get | 聊天玩家 <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 聊天玩家 <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 聊天玩家 <br/> 类型：玩家控制器 |
| `Playerid` | `short` | get, set | 聊天玩家ID <br/> 类型：short |
| `Text` | `string` | get, set | 聊天文本 <br/> 类型：字符串 |

