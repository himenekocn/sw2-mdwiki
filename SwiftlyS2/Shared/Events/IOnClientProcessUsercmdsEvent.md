<a id="ionclientprocessusercmdsevent"></a>

# 🔌 IOnClientProcessUsercmdsEvent

当客户端处理用户命令时调用。此回调是热点路径，请谨慎处理，避免执行任何高开销操作。

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlayerId` | `int` | get | 处理用户命令的客户端的玩家ID |
| `Usercmds` | `List\<CSGOUserCmdPB\>` | get | 客户端处理的用户指令。 |
| `Paused` | `bool` | get | 客户端是否已暂停。 |
| `Margin` | `float` | get | 客户端的余量，单位为毫秒。 |

