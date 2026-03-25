# 🔌 ICommandContext

**命名空间:** `SwiftlyS2.Shared.Commands`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `IsSentByPlayer` | `bool` | get | 获取一个值，指示该命令是否由玩家发送。 |
| `Sender` | `IPlayer?` | get | 获取发送该命令的玩家，若命令并非由玩家发送则返回 null。 |
| `Prefix` | `string` | get | 获取命令前缀。 |
| `IsSlient` | `bool` | get | 获取一个值，指示该命令是否应静默执行且不向其他玩家广播。 |
| `CommandName` | `string` | get | 获取命令名称本身。 |
| `Args` | `string[]` | get | 获取与命令一同传递的参数数组。 |

## ⚙️ 方法

### Reply

```csharp
void Reply(string message)
```

向命令发送者回复一条消息。

**参数:**

- `message` (`string`) - 作为回复要发送的消息。

**用法示例:**
```csharp
context.Reply("Command received successfully.");
```

### ReplyAsync

```csharp
Task ReplyAsync(string message)
```

异步向命令发送者发送回复消息。

**参数:**

- `message` (`string`) - 作为回复要发送的消息。

**返回值:** `Task`

**用法示例:**
```csharp
await context.ReplyAsync("Command executed successfully.");
```

