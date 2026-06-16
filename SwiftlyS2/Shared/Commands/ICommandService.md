<a id="icommandservice"></a>

# 🔌 ICommandService

**命名空间:** `SwiftlyS2.Shared.Commands`

**类型:** `interface`

## ⚙️ 方法

### CommandListener

```csharp
void CommandListener(ICommandContext context)
```

命令的侦听器。

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

- `playerId` (`int`) - 玩家ID。
- `commandLine` (`string`) - 命令行。

**返回值:** `HookResult` - 命令是否应继续发送。

**用法示例:**
```csharp
HookResult result = commandService.ClientCommandHandler(playerId, "say hello");
```

### ClientChatHandler

```csharp
HookResult ClientChatHandler(int playerId, string text, bool teamonly)
```

客户端聊天钩子的处理器。

**参数:**

- `playerId` (`int`) - 玩家ID。
- `text` (`string`) - The text.
- `teamonly` (`bool`) - 文本是否仅限队伍可见。

**返回值:** `HookResult` - 文本是否应继续发送。

**用法示例:**
```csharp
HookResult result = commandService.ClientChatHandler(playerId, text, teamonly);
```

### RegisterCommand

```csharp
Guid RegisterCommand(string commandName, CommandListener handler, bool registerRaw, string permission)
```

注册一个命令（向后兼容性重载）。

**参数:**

- `commandName` (`string`) - 命令名称。
- `handler` (`CommandListener`) - 命令的处理程序回调。
- `registerRaw` (`bool`) - 如果设为 true，该命令将不会以 `sw_` 前缀开头。
- `permission` (`string`) - 使用命令所需的权限。

**返回值:** `Guid` - 命令的GUID。

**用法示例:**
```csharp
Guid cmdId = commandService.RegisterCommand("test_cmd", (player, args) => { }, false, "generic");
```

### RegisterCommand

```csharp
Guid RegisterCommand(string commandName, CommandListener handler, bool registerRaw = false, string permission = "", string helpText = "SwiftlyS2 registered command")
```

注册一个命令。

**参数:**

- `commandName` (`string`) - 命令名称。
- `handler` (`CommandListener`) - 命令的处理程序回调。
- `registerRaw` (`bool`) = `false` - 如果设为 true，该命令将不会以 `sw_` 前缀开头。
- `permission` (`string`) = `""` - 使用命令所需的权限。
- `helpText` (`string`) = `"SwiftlyS2 registered command"` - 命令的帮助文本。

**返回值:** `Guid` - 命令的GUID。

**用法示例:**
```csharp
Guid cmdId = commandService.RegisterCommand("test", OnTestCommand, false, "admin", "Test command");
```

### RegisterCommandAlias

```csharp
void RegisterCommandAlias(string commandName, string alias, bool registerRaw = false)
```

注册命令别名。

**参数:**

- `commandName` (`string`) - 命令名称。
- `alias` (`string`) - 别名。
- `registerRaw` (`bool`) = `false` - 如果设置为 true，别名将不会以 `sw_` 前缀开头。

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

- `guid` (`Guid`) - 命令的GUID。

**用法示例:**
```csharp
commandService.UnregisterCommand(commandGuid);
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
commandService.UnregisterCommand("say");
```

### IsCommandRegistered

```csharp
bool IsCommandRegistered(string commandName)
```

检查命令是否已注册。

**参数:**

- `commandName` (`string`) - 命令名称。

**返回值:** `bool` - 是否已注册该命令。

**用法示例:**
```csharp
bool isRegistered = commandService.IsCommandRegistered("my_command");
```

### HookClientCommand

```csharp
Guid HookClientCommand(ClientCommandHandler handler)
```

挂钩客户端指令，将在玩家发送任何指令时触发。

**参数:**

- `handler` (`ClientCommandHandler`) - 客户端命令的处理程序回调。

**返回值:** `Guid`

**用法示例:**
```csharp
var hookId = commandService.HookClientCommand(OnClientCommand);
```

### UnhookClientCommand

```csharp
void UnhookClientCommand(Guid guid)
```

取消挂接客户端命令。

**参数:**

- `guid` (`Guid`) - 客户端命令的GUID。

**用法示例:**
```csharp
commandService.UnhookClientCommand(clientGuid);
```

### HookClientChat

```csharp
Guid HookClientChat(ClientChatHandler handler)
```

钩子客户端聊天，当玩家发送任何聊天消息时将触发。

**参数:**

- `handler` (`ClientChatHandler`) - 客户端聊天的处理程序回调。

**返回值:** `Guid`

**用法示例:**
```csharp
Guid hookId = commandService.HookClientChat(OnClientChat);
```

### UnhookClientChat

```csharp
void UnhookClientChat(Guid guid)
```

取消挂钩客户端聊天。

**参数:**

- `guid` (`Guid`) - 客户端聊天的GUID。

**用法示例:**
```csharp
commandService.UnhookClientChat(clientGuid);
```

### GetAllCommands

```csharp
List<string> GetAllCommands()
```

获取所有由插件注册的命令。

**返回值:** `List\<string\>`

**用法示例:**
```csharp
var commands = commandService.GetAllCommands();
```

### GetCommandsByPlugin

```csharp
List<CommandInfo> GetCommandsByPlugin(string pluginName)
```

获取特定插件注册的所有命令。

**参数:**

- `pluginName` (`string`) - 插件的名称。

**返回值:** `List\<CommandInfo\>` - 插件注册的命令信息列表。

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

获取由插件注册的所有命令信息。

**返回值:** `List\<CommandInfo\>` - 插件注册的命令信息列表。

**用法示例:**
```csharp
var commands = commandService.GetAllCommandsInfo();
```

