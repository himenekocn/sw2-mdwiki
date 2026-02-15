# 🔌 ICommandService

**命名空间:** `SwiftlyS2.Shared.Commands`

**类型:** `interface`

## ⚙️ 方法

### CommandListener

```csharp
void CommandListener(ICommandContext context)
```

命令的监听器。

**参数:**

- `context` (`ICommandContext`) - 命令上下文。

**用法示例:**
```csharp
ICommandService.CommandListener(player.Context);
```

### ClientCommandHandler

```csharp
HookResult ClientCommandHandler(int playerId, string commandLine)
```

客户端命令钩子的处理程序。

**参数:**

- `playerId` (`int`) - 玩家ID。
- `commandLine` (`string`) - 命令行。

**返回值:** `HookResult` - 是否应继续发送该命令。

**用法示例:**
```csharp
ICommandService.ClientCommandHandler(player.Id, "say hello");
```

### ClientChatHandler

```csharp
HookResult ClientChatHandler(int playerId, string text, bool teamonly)
```

客户端聊天钩子的处理程序。

**参数:**

- `playerId` (`int`) - 玩家ID。
- `text` (`string`) - 好的，请提供需要翻译的C#代码注释。
- `teamonly` (`bool`) - 文本是否仅限团队可见。

**返回值:** `HookResult` - 是否应继续发送文本。

**用法示例:**
```csharp
HookResult result = commandService.ClientChatHandler(playerId: 1, text: "Hello", teamonly: false);
```

### RegisterCommand

```csharp
Guid RegisterCommand(string commandName, CommandListener handler, bool registerRaw, string permission)
```

注册一个命令（向后兼容重载）。

**参数:**

- `commandName` (`string`) - 命令名称。
- `handler` (`CommandListener`) - 命令的处理程序回调。
- `registerRaw` (`bool`) - 如果设置为 true，则该命令不会以 `sw_` 为前缀。
- `permission` (`string`) - 使用该命令所需的权限。

**返回值:** `Guid` - 命令的 GUID。

**用法示例:**
```csharp
manager.RegisterCommand("kick", OnKickCommand, false, "admin.kick");
```

### RegisterCommand

```csharp
Guid RegisterCommand(string commandName, CommandListener handler, bool registerRaw = false, string permission = "", string helpText = "SwiftlyS2 registered command")
```

注册一个命令。

**参数:**

- `commandName` (`string`) - 命令名称。
- `handler` (`CommandListener`) - 命令的处理程序回调。
- `registerRaw` (`bool`) = `false` - 如果设置为 true，则该命令不会以 `sw_` 为前缀。
- `permission` (`string`) = `""` - 使用该命令所需的权限。
- `helpText` (`string`) = `"SwiftlyS2 registered command"` - 命令的帮助文本。

**返回值:** `Guid` - 命令的 GUID。

**用法示例:**
```csharp
commandService.RegisterCommand("kick", OnKickCommand, false, "admin.kick", "Kicks a player from the server");
```

### RegisterCommandAlias

```csharp
void RegisterCommandAlias(string commandName, string alias, bool registerRaw = false)
```

注册一个命令别名。

**参数:**

- `commandName` (`string`) - 命令名称。
- `alias` (`string`) - 别名。
- `registerRaw` (`bool`) = `false` - 如果设置为 true，则别名不会以 `sw_` 为前缀。

**用法示例:**
```csharp
commandService.RegisterCommandAlias("kick", "k", true);
```

### UnregisterCommand

```csharp
void UnregisterCommand(Guid guid)
```

注销命令。

**参数:**

- `guid` (`Guid`) - 命令的 GUID。

**用法示例:**
```csharp
commandService.UnregisterCommand(Guid.NewGuid());
```

### UnregisterCommand

```csharp
void UnregisterCommand(string commandName)
```

注销所有具有指定命令名称的命令监听器。

**参数:**

- `commandName` (`string`) - 命令名称。

**用法示例:**
```csharp
commandService.UnregisterCommand("move");
```

### IsCommandRegistered

```csharp
bool IsCommandRegistered(string commandName)
```

检查命令是否已注册。

**参数:**

- `commandName` (`string`) - 命令名称。

**返回值:** `bool` - 命令是否已注册。

**用法示例:**
```csharp
bool isRegistered = commandService.IsCommandRegistered("myCommand");
```

### HookClientCommand

```csharp
Guid HookClientCommand(ClientCommandHandler handler)
```

挂钩客户端命令，当玩家发送任何命令时将被触发。

**参数:**

- `handler` (`ClientCommandHandler`) - 客户端命令的处理程序回调。

**返回值:** `Guid`

**用法示例:**
```csharp
Guid id = commandService.HookClientCommand((player, command) => Console.WriteLine($"Player {player.Name} used command: {command}"));
```

### UnhookClientCommand

```csharp
void UnhookClientCommand(Guid guid)
```

取消挂钩客户端命令。

**参数:**

- `guid` (`Guid`) - 客户端命令的 GUID。

**用法示例:**
```csharp
commandService.UnhookClientCommand(someGuid);
```

### HookClientChat

```csharp
Guid HookClientChat(ClientChatHandler handler)
```

挂钩客户端聊天，当玩家发送任何聊天消息时将触发。

**参数:**

- `handler` (`ClientChatHandler`) - 客户端聊天的事件处理回调。

**返回值:** `Guid`

**用法示例:**
```csharp
Guid hookId = commandService.HookClientChat((player, message) => Console.WriteLine($"{player.Name}: {message}"));
```

### UnhookClientChat

```csharp
void UnhookClientChat(Guid guid)
```

取消客户端聊天挂钩。

**参数:**

- `guid` (`Guid`) - 客户端聊天的 GUID。

**用法示例:**
```csharp
commandService.UnhookClientChat(playerGuid);
```

