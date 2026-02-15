# 🔌 IPlayerManagerService

**命名空间:** `SwiftlyS2.Shared.Players`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlayerCount` | `int` | get | 获取当前游戏中的玩家数量。 |
| `PlayerCap` | `int` | get | 获取引擎允许的最大玩家数量。 |

## ⚙️ 方法

### IsPlayerOnline

```csharp
bool IsPlayerOnline(int playerid)
```

检查特定玩家是否当前在线并已连接到服务器。

**参数:**

- `playerid` (`int`)

**返回值:** `bool` - 如果玩家在线，则为 true，否则为 false。

**用法示例:**
```csharp
bool online = manager.IsPlayerOnline(123);
```

### SendMessage

```csharp
void SendMessage(MessageType kind, string message)
```

**参数:**

- `kind` (`MessageType`)
- `message` (`string`)

**用法示例:**
```csharp
manager.SendMessage(MessageType.Info, "Hello, world!");
```

### SendMessage

```csharp
void SendMessage(MessageType kind, string message, int htmlDuration = 5000)
```

**参数:**

- `kind` (`MessageType`)
- `message` (`string`)
- `htmlDuration` (`int`) = `5000`

**用法示例:**
```csharp
manager.SendMessage(MessageType.Info, "Hello World", 3000);
```

### SendMessage

```csharp
void SendMessage(MessageType kind, Func<IPlayer, ILocalizer, string> messageCallback)
```

**参数:**

- `kind` (`MessageType`)
- `messageCallback` (`Func\<IPlayer, ILocalizer, string\>`)

**用法示例:**
```csharp
manager.SendMessage(MessageType.Info, (player, localizer) => localizer["Hello, {0}!", player.Name]);
```

### SendMessage

```csharp
void SendMessage(MessageType kind, Func<IPlayer, ILocalizer, string> messageCallback, int htmlDuration = 5000)
```

**参数:**

- `kind` (`MessageType`)
- `messageCallback` (`Func\<IPlayer, ILocalizer, string\>`)
- `htmlDuration` (`int`) = `5000`

**用法示例:**
```csharp
manager.SendMessage(MessageType.Info, (p, l) => l.Get("PlayerJoined"), 5000);
```

### SendMessageAsync

```csharp
Task SendMessageAsync(MessageType kind, string message)
```

异步地向玩家发送指定类型的消息。

**参数:**

- `kind` (`MessageType`) - 要发送的消息类型。决定消息的处理或显示方式。
- `message` (`string`) - 要发送的消息内容。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await manager.SendMessageAsync(MessageType.Error, "连接失败");
```

### SendMessageAsync

```csharp
Task SendMessageAsync(MessageType kind, string message, int htmlDuration = 5000)
```

以自定义的 HTML 持续时间，异步地向玩家发送指定类型的消息。

**参数:**

- `kind` (`MessageType`) - 要发送的消息类型。决定消息的处理或显示方式。
- `message` (`string`) - 要发送的消息内容。不能为 null。
- `htmlDuration` (`int`) = `5000` - 消息应以HTML格式显示的持续时间（以毫秒为单位）。

**返回值:** `Task`

**用法示例:**
```csharp
await manager.SendMessageAsync(MessageType.Info, "Hello World", 5000);
```

### SendMessageAsync

```csharp
Task SendMessageAsync(MessageType kind, Func<IPlayer, ILocalizer, string> messageCallback)
```

根据消息类型，使用不同的显示方式向玩家广播消息。线程不安全，在非主线程上下文中请改用异步变体。

**参数:**

- `kind` (`MessageType`) - 消息显示的类型。
- `messageCallback` (`Func\<IPlayer, ILocalizer, string\>`) - 要发送给玩家的文本回调。

**返回值:** `Task`

**用法示例:**
```csharp
manager.SendMessageAsync(MessageType.Info, (player, localizer) => localizer["Hello, {0}!", player.Name]);
```

### SendMessageAsync

```csharp
Task SendMessageAsync(MessageType kind, Func<IPlayer, ILocalizer, string> messageCallback, int htmlDuration = 5000)
```

向玩家发送指定类型的消息，并附带自定义的HTML持续时间。线程不安全，在非主线程上下文中请改用异步变体。

**参数:**

- `kind` (`MessageType`) - 要发送的消息类型。决定消息的处理或显示方式。
- `messageCallback` (`Func\<IPlayer, ILocalizer, string\>`) - 要发送的消息的回调。不能为 null。
- `htmlDuration` (`int`) = `5000` - 消息应以HTML格式显示的持续时间（以毫秒为单位）。

**返回值:** `Task`

**用法示例:**
```csharp
await manager.SendMessageAsync(MessageType.Info, (p, l) => l["Hello"], 3000);
```

### SendNotify

```csharp
void SendNotify(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
manager.SendNotify("Game started");
```

### SendNotifyAsync

```csharp
Task SendNotifyAsync(string message)
```

异步地向玩家发送通知消息。

**参数:**

- `message` (`string`) - 要发送的消息内容。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await manager.SendNotifyAsync("Game started!");
```

### SendConsole

```csharp
void SendConsole(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
manager.SendConsole("Hello World");
```

### SendConsoleAsync

```csharp
Task SendConsoleAsync(string message)
```

异步地向玩家发送控制台消息。

**参数:**

- `message` (`string`) - 要发送的消息内容。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await manager.SendConsoleAsync("Hello, player!");
```

### SendChat

```csharp
void SendChat(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
manager.SendChat("Hello, world!");
```

### SendChatAsync

```csharp
Task SendChatAsync(string message)
```

异步地向玩家发送聊天消息。

**参数:**

- `message` (`string`) - 要发送的消息内容。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await manager.SendChatAsync("Hello, world!");
```

### SendCenter

```csharp
void SendCenter(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
manager.SendCenter("Hello from center");
```

### SendCenterAsync

```csharp
Task SendCenterAsync(string message)
```

异步地向玩家发送中心消息。

**参数:**

- `message` (`string`) - 要发送的消息内容。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await manager.SendCenterAsync("Hello, player!");
```

### SendAlert

```csharp
void SendAlert(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
manager.SendAlert("Player disconnected");
```

### SendAlertAsync

```csharp
Task SendAlertAsync(string message)
```

异步地向玩家发送警报消息。

**参数:**

- `message` (`string`) - 要发送的消息内容。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await manager.SendAlertAsync("Game starting in 30 seconds!");
```

### SendCenterHTML

```csharp
void SendCenterHTML(string message, int duration = 5000)
```

**参数:**

- `message` (`string`)
- `duration` (`int`) = `5000`

**用法示例:**
```csharp
manager.SendCenterHTML("Hello World", 5);
```

### SendCenterHTMLAsync

```csharp
Task SendCenterHTMLAsync(string message, int duration = 5000)
```

异步地向玩家发送居中的 HTML 消息。

**参数:**

- `message` (`string`) - 要发送的消息内容。不能为 null。
- `duration` (`int`) = `5000` - 消息应以HTML格式显示的持续时间（以毫秒为单位）。

**返回值:** `Task`

**用法示例:**
```csharp
await manager.SendCenterHTMLAsync("<color=red>Game Started!</color>", 5);
```

### SendChatEOT

```csharp
void SendChatEOT(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
manager.SendChatEOT("Game ended");
```

### SendChatEOTAsync

```csharp
Task SendChatEOTAsync(string message)
```

异步地向玩家发送文本聊天消息的结束。

**参数:**

- `message` (`string`) - 要发送的消息内容。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await manager.SendChatEOTAsync("Hello World");
```

### ShouldBlockTransmitEntity

```csharp
void ShouldBlockTransmitEntity(int entityid, bool shouldBlockTransmit)
```

控制是否应阻止特定实体被传输/同步到客户端。

**参数:**

- `entityid` (`int`)
- `shouldBlockTransmit` (`bool`)

**用法示例:**
```csharp
manager.ShouldBlockTransmitEntity(entityId, true);
```

### ClearAllBlockedTransmitEntities

```csharp
void ClearAllBlockedTransmitEntities()
```

移除所有实体传输区块，使所有先前被阻止的实体能够再次传输给客户端。

**用法示例:**
```csharp
manager.ClearAllBlockedTransmitEntities();
```

### GetPlayer

```csharp
IPlayer? GetPlayer(int playerid)
```

根据指定的玩家ID获取关联的玩家。

**参数:**

- `playerid` (`int`) - 要检索的玩家的唯一标识符。必须是有效的玩家ID。

**返回值:** `IPlayer?` - 一个表示具有指定ID的玩家的 <see cref="IPlayer"/> 实例，如果不存在这样的玩家，则为 <c>null</c>。

**用法示例:**
```csharp
IPlayer? player = manager.GetPlayer(123);
```

### GetPlayerFromController

```csharp
IPlayer? GetPlayerFromController(CBasePlayerController controller)
```

获取与指定控制器关联的玩家。

**参数:**

- `controller` (`CBasePlayerController`) - 用于检索玩家的控制器。

**返回值:** `IPlayer?` - 一个表示具有指定控制器的玩家的 <see cref="IPlayer"/> 实例，如果不存在这样的玩家，则为 <c>null</c>。

**用法示例:**
```csharp
IPlayer? player = manager.GetPlayerFromController(controller);
```

### GetPlayerFromPawn

```csharp
IPlayer? GetPlayerFromPawn(CBasePlayerPawn pawn)
```

获取与指定Pawn关联的玩家。

**参数:**

- `pawn` (`CBasePlayerPawn`) - 要从中获取玩家的Pawn。

**返回值:** `IPlayer?` - 一个表示拥有指定Pawn的玩家的 <see cref="IPlayer"/> 实例，如果不存在这样的玩家，则为 <c>null</c>。

**用法示例:**
```csharp
IPlayer? player = manager.GetPlayerFromPawn(pawn);
```

### GetAllPlayers

```csharp
IEnumerable<IPlayer> GetAllPlayers()
```

获取所有当前在线的玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 一个可枚举的 <see cref="IPlayer"/> 实例集合，代表所有在线玩家。

**用法示例:**
```csharp
IEnumerable<IPlayer> players = manager.GetAllPlayers();
```

### GetAllValidPlayers

```csharp
IEnumerable<IPlayer> GetAllValidPlayers()
```

获取所有当前在线的有效玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 一个可枚举的 <see cref="IPlayer"/> 实例集合，代表所有在线玩家。

**用法示例:**
```csharp
IPlayerManagerService manager = PlayerManager.Instance;
foreach (var player in manager.GetAllValidPlayers())
{
    Console.WriteLine(player.Name);
}
```

### GetBots

```csharp
IEnumerable<IPlayer> GetBots()
```

获取当前在线的所有机器人玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 一个可枚举的 <see cref="IPlayer"/> 实例集合，代表所有在线的机器人玩家。

**用法示例:**
```csharp
foreach (var bot in manager.GetBots()) Console.WriteLine(bot.Name);
```

### GetAlive

```csharp
IEnumerable<IPlayer> GetAlive()
```

获取当前在线的所有存活玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 一个可枚举的集合，包含代表当前在线的所有存活玩家的 <see cref="IPlayer"/> 实例。

**用法示例:**
```csharp
var alivePlayers = manager.GetAlive();
```

### GetCT

```csharp
IEnumerable<IPlayer> GetCT()
```

获取所有当前在线的CT玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 一个可枚举的集合，包含代表当前在线的所有CT玩家的 <see cref="IPlayer"/> 实例。

**用法示例:**
```csharp
var ctPlayers = manager.GetCT();
```

### GetT

```csharp
IEnumerable<IPlayer> GetT()
```

获取所有当前在线的 T 玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 一个可枚举的集合，包含代表当前在线的所有T玩家的 <see cref="IPlayer"/> 实例。

**用法示例:**
```csharp
IEnumerable<IPlayer> onlineTPlayers = manager.GetT();
```

### GetSpectators

```csharp
IEnumerable<IPlayer> GetSpectators()
```

获取当前在线的所有观战玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 一个可枚举的集合，包含表示当前在线的所有观赛玩家的 <see cref="IPlayer"/> 实例。

**用法示例:**
```csharp
foreach (var spectator in manager.GetSpectators()) { Console.WriteLine(spectator.Name); }
```

### GetInTeam

```csharp
IEnumerable<IPlayer> GetInTeam(Team team)
```

获取指定团队中的所有玩家。

**参数:**

- `team` (`Team`) - 要检索其玩家的团队。

**返回值:** `IEnumerable\<IPlayer\>` - 一个可枚举的 <see cref="IPlayer"/> 实例集合，代表指定团队中的所有玩家。

**用法示例:**
```csharp
manager.GetInTeam(Team.T);
```

### GetTAlive

```csharp
IEnumerable<IPlayer> GetTAlive()
```

检索所有当前在线的存活 T 玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 一个可枚举的集合，包含代表当前在线的所有存活T阵营玩家的 <see cref="IPlayer"/> 实例。

**用法示例:**
```csharp
var aliveTPlayers = manager.GetTAlive();
```

### GetCTAlive

```csharp
IEnumerable<IPlayer> GetCTAlive()
```

获取当前在线的所有存活的CT玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 一个可枚举的集合，包含表示当前在线的所有存活CT玩家的 <see cref="IPlayer"/> 实例。

**用法示例:**
```csharp
manager.GetCTAlive();
```

### IsSessionIdValid

```csharp
bool IsSessionIdValid(ulong sessionId)
```

检查特定的会话 ID 是否有效。当关联的玩家断开连接或不存在时，会话 ID 将变为无效。

**参数:**

- `sessionId` (`ulong`) - 要检查的会话 ID。

**返回值:** `bool` - 如果会话 ID 有效，则为 true，否则为 false。

**用法示例:**
```csharp
bool valid = manager.IsSessionIdValid(12345UL);
```

### GetPlayerFromSessionId

```csharp
IPlayer? GetPlayerFromSessionId(ulong sessionId)
```

根据指定的会话 ID 获取关联的玩家。

**参数:**

- `sessionId` (`ulong`) - 用于检索玩家的会话 ID。

**返回值:** `IPlayer?` - 一个表示具有指定会话 ID 的玩家的 <see cref="IPlayer"/> 实例，如果会话 ID 已释放或无效，则返回 <c>null</c>。玩家存在。

**用法示例:**
```csharp
IPlayer? player = manager.GetPlayerFromSessionId(12345);
```

### GetPlayerFromSteamId

```csharp
IPlayer? GetPlayerFromSteamId(ulong steamId, bool allowUnauthorized = true)
```

根据指定的 Steam ID 获取关联的玩家。

**参数:**

- `steamId` (`ulong`) - 要检索的玩家的 Steam ID。
- `allowUnauthorized` (`bool`) = `true` - 是否允许未经授权的玩家。

**返回值:** `IPlayer?` - 一个表示具有指定 Steam ID 的玩家的 <see cref="IPlayer"/> 实例，如果不存在这样的玩家，则为 <c>null</c>。

**用法示例:**
```csharp
IPlayer? player = manager.GetPlayerFromSteamId(123456789, false);
```

