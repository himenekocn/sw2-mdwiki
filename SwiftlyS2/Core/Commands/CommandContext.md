# 📦 CommandContext

**命名空间:** `SwiftlyS2.Core.Commands`

**类型:** `class`

**继承:** `ICommandContext`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `IsSentByPlayer` | `bool` | get | - |
| `Sender` | `IPlayer?` | get | - |
| `Prefix` | `string` | get | - |
| `IsSlient` | `bool` | get | - |
| `CommandName` | `string` | get | - |
| `Args` | `string[]` | get | - |

## ⚙️ 方法

### Reply

```csharp
void Reply(string message)
```

**参数:**

- `message` (`string`)

### ReplyAsync

```csharp
Task ReplyAsync(string message)
```

**参数:**

- `message` (`string`)

**返回值:** `Task`

### ToString

```csharp
string ToString()
```

**返回值:** `string`

