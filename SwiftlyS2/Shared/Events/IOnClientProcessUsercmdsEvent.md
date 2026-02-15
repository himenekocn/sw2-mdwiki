# 🔌 IOnClientProcessUsercmdsEvent

Called when a client processes user commands. This callback is a hot path, be careful with it and don't do anything expensive.

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `PlayerId` | `int` | get | The player ID of the client that processed the user commands. |
| `Usercmds` | `List\<CSGOUserCmdPB\>` | get | The user commands that the client processed. |
| `Paused` | `bool` | get | Whether the client is paused. |
| `Margin` | `float` | get | The margin of the client, milliseconds. |

