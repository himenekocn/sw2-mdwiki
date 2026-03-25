# 🔌 IOnClientProcessUsercmdsEvent

当客户端处理用户命令时调用。此回调为热点路径，请谨慎使用，避免执行任何高开销操作。

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlayerId` | `int` | get | 处理用户命令的客户端的玩家 ID。 |
| `Usercmds` | `List\<CSGOUserCmdPB\>` | get | 用户向客户端发送的指令。 |
| `Paused` | `bool` | get | 客户端是否处于暂停状态。 |
| `Margin` | `float` | get | 客户端的边距，单位：毫秒。 |

