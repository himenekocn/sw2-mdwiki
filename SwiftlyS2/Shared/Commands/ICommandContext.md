# 🔌 ICommandContext

**命名空间:** `SwiftlyS2.Shared.Commands`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `IsSentByPlayer` | `bool` | get | Gets a value indicating whether the command was sent by a player. |
| `Sender` | `IPlayer?` | get | Gets the player who sent the command, or null if the command was not sent by a player. |
| `Prefix` | `string` | get | Gets the command prefix. |
| `IsSlient` | `bool` | get | Gets a value indicating whether the command should be executed silently without broadcasting to other players. |
| `CommandName` | `string` | get | Gets the command name itself. |
| `Args` | `string[]` | get | Gets the array of arguments passed with the command. |

