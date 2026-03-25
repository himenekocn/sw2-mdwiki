<a id="icommandservice"></a>

# 🔌 ICommandService

**命名空间:** `SwiftlyS2.Shared.Commands`

**类型:** `interface`

## ⚙️ 方法

### CommandListener

```csharp
void CommandListener(ICommandContext context)
```

命令监听器。

**参数:**

- `context` (`ICommandContext`) - 命令上下文。

**用法示例:**
```csharp
commandService.CommandListener(context);
```

### ClientCommandHandler

```csharp
HookResult ClientCommandHandler(int playerId, string commandLine)
```

客户端命令钩子的处理器。

**参数:**

- `playerId` (`int`) - 玩家 ID。
- `commandLine` (`string`) - 命令行。

**返回值:** `HookResult` - 是否应继续发送该命令。

**用法示例:**
```csharp
var result = commandService.ClientCommandHandler(playerId, "say Hello");
```

### ClientChatHandler

```csharp
HookResult ClientChatHandler(int playerId, string text, bool teamonly)
```

客户端聊天钩子的处理器。

**参数:**

- `playerId` (`int`) - 玩家 ID。
- `text` (`string`) - 文本。
- `teamonly` (`bool`) - 该文本是否仅用于团队内部。

**返回值:** `HookResult` - 是否应继续发送文本。

**用法示例:**
```csharp
var result = commandService.ClientChatHandler(playerId, "Hello", false);
```

### RegisterCommand

```csharp
Guid RegisterCommand(string commandName, CommandListener handler, bool registerRaw, string permission)
```

注册一个命令（向后兼容的重载）。

**参数:**

- `commandName` (`string`) - 命令名称。
- `handler` (`CommandListener`) - 该命令的处理器回调。
- `registerRaw` (`bool`) - 如果设置为 true，命令将不带 `sw_` 前缀。
- `permission` (`string`) - 使用该命令所需的权限。

**返回值:** `Guid` - 该命令的 GUID。

**用法示例:**
```csharp
var commandId = commandService.RegisterCommand("testcmd", HandleCommand, false, "admin.access");
```

### RegisterCommand

```csharp
Guid RegisterCommand(string commandName, CommandListener handler, bool registerRaw = false, string permission = "", string helpText = "SwiftlyS2 registered command")
```

注册一个命令。

**参数:**

- `commandName` (`string`) - 命令名称。
- `handler` (`CommandListener`) - 该命令的处理器回调。
- `registerRaw` (`bool`) = `false` - 如果设置为 true，命令将不带 `sw_` 前缀。
- `permission` (`string`) = `""` - 使用该命令所需的权限。
- `helpText` (`string`) = `"SwiftlyS2 registered command"` - 该命令的帮助文本。

**返回值:** `Guid` - 该命令的 GUID。

**用法示例:**
```csharp
Guid cmdId = commandService.RegisterCommand("teleport", OnTeleportCommand, false, "admin.teleport", "Teleports a player to spawn");
```

### RegisterCommandAlias

```csharp
void RegisterCommandAlias(string commandName, string alias, bool registerRaw = false)
```

注册命令别名。

**参数:**

- `commandName` (`string`) - 命令名称。
- `alias` (`string`) - 别名。
- `registerRaw` (`bool`) = `false` - 如果设置为 true，则别名将不以 `sw_` 前缀开头。

**用法示例:**
```csharp
commandService.RegisterCommandAlias("say", "s", false);
```

### UnregisterCommand

```csharp
void UnregisterCommand(Guid guid)
```

注销一个命令。

**参数:**

- `guid` (`Guid`) - 该命令的 GUID。

**用法示例:**
```csharp
commandService.UnregisterCommand(existingGuid);
```

### UnregisterCommand

```csharp
void UnregisterCommand(string commandName)
```

注销所有指定命令名称的命令监听器。

**参数:**

- `commandName` (`string`) - 命令名称。

**用法示例:**
```csharp
commandService.UnregisterCommand("say");
```

### IsCommandRegistered

```csharp
bool IsCommandRegistered(string commandName)
```

检查命令是否已注册。

**参数:**

- `commandName` (`string`) - 命令名称。

**返回值:** `bool` - 该命令是否已注册。

**用法示例:**
```csharp
bool isRegistered = commandService.IsCommandRegistered("say");
```

### HookClientCommand

```csharp
Guid HookClientCommand(ClientCommandHandler handler)
```

钩住客户端命令，当玩家发送任何命令时将被触发。

**参数:**

- `handler` (`ClientCommandHandler`) - 客户端命令的处理程序回调。

**返回值:** `Guid`

**用法示例:**
```csharp
Guid hookId = commandService.HookClientCommand(OnClientCommand);
```

### UnhookClientCommand

```csharp
void UnhookClientCommand(Guid guid)
```

解除绑定客户端命令。

**参数:**

- `guid` (`Guid`) - 客户端命令的 GUID。

**用法示例:**
```csharp
commandService.UnhookClientCommand(commandGuid);
```

### HookClientChat

```csharp
Guid HookClientChat(ClientChatHandler handler)
```

挂钩客户端聊天，当玩家发送任何聊天消息时将被触发。

**参数:**

- `handler` (`ClientChatHandler`) - 客户端聊天的处理器回调。

**返回值:** `Guid`

**用法示例:**
```csharp
Guid hookId = commandService.HookClientChat((player, message) => Console.WriteLine($"{player.Name}: {message}"));
```

### UnhookClientChat

```csharp
void UnhookClientChat(Guid guid)
```

解除客户端聊天的挂钩。

**参数:**

- `guid` (`Guid`) - 客户端聊天的 GUID。

**用法示例:**
```csharp
commandService.UnhookClientChat(clientGuid);
```

### GetAllCommands

```csharp
List<string> GetAllCommands()
```

获取插件注册的所有命令。

**返回值:** `List\<string\>`

**用法示例:**
```csharp
var commands = commandService.GetAllCommands();
```

### GetCommandsByPlugin

```csharp
List<CommandInfo> GetCommandsByPlugin(string pluginName)
```

获取由特定插件注册的所有命令。

**参数:**

- `pluginName` (`string`) - 插件的名称。

**返回值:** `List\<CommandInfo\>` - 由插件注册的玩家指令信息列表。

**用法示例:**
```csharp
var commands = commandService.GetCommandsByPlugin("MyPlugin");
```

### GetAllCommandsByPlugin

```csharp
List<CommandInfo>> GetAllCommandsByPlugin()
```

获取所有已注册命令的插件。

**返回值:** `List\<CommandInfo\>\>` - 将插件名称映射到其注册命令信息的字典。

**用法示例:**
```csharp
var commands = commandService.GetAllCommandsByPlugin();
```

### GetAllCommandsInfo

```csharp
List<CommandInfo> GetAllCommandsInfo()
```

获取由插件注册的所有命令的信息。

**返回值:** `List\<CommandInfo\>` - 由插件注册的玩家指令信息列表。

**用法示例:**
```csharp
var commands = commandService.GetAllCommandsInfo();
```

