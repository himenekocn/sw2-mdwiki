# 🔌 EventGameMessage

事件 "game_message" 是由游戏逻辑向所有人发送的一条消息

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGameMessage\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Target` | `byte` | get, set | 0 = 控制台, 1 = HUD <br/> 类型: 字节 |
| `Text` | `string` | get, set | 消息文本 <br/> 类型：字符串 |

