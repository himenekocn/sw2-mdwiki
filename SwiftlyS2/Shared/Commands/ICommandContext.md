<a id="icommandcontext"></a>

# 🔌 ICommandContext

**命名空间:** `SwiftlyS2.Shared.Commands`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `IsSentByPlayer` | `bool` | get | 获取一个值，指示该命令是否由玩家发送。 |
| `Sender` | `IPlayer?` | get | 获取发送该命令的玩家，如果命令并非由玩家发送，则返回 null。 |
| `Prefix` | `string` | get | 获取命令前缀。 |
| `IsSlient` | `bool` | get | 获取一个值，指示该命令是否应在不向其他玩家广播的情况下静默执行。 |
| `CommandName` | `string` | get | 获取命令名称本身。 |
| `Args` | `string[]` | get | 获取命令传入的参数数组。 |

## ⚙️ 方法

### Reply

```csharp
void Reply(string message)
```

向命令发送者发送回复消息。

**参数:**

- `message` (`string`) - 作为回复发送的消息。

**用法示例:**
```csharp
context.Reply("Command executed successfully.");
```

### ReplyAsync

```csharp
Task ReplyAsync(string message)
```

异步向命令发送者发送回复消息。

**参数:**

- `message` (`string`) - 作为回复发送的消息。

**返回值:** `Task`

**用法示例:**
```csharp
await commandContext.ReplyAsync("Command executed successfully.");
```

