# 🔌 IPlayerManagerService

**命名空间:** `SwiftlyS2.Shared.Players`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlayerCount` | `int` | get | 获取当前游戏中玩家的数量。 |
| `PlayerCap` | `int` | get | 获取引擎允许的最大玩家数量。 |

## ⚙️ 方法

### IsPlayerOnline

```csharp
bool IsPlayerOnline(int playerid)
```

检查指定玩家当前是否在线并连接到服务器。

**参数:**

- `playerid` (`int`)

**返回值:** `bool` - 如果玩家在线则为 true，否则为 false。

**用法示例:**
```csharp
bool isOnline = playerManager.IsPlayerOnline(12345);
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
manager.SendMessage(MessageType.Chat, "Hello World");
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
manager.SendMessage(MessageType.Value, "Hello", 5000);
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
manager.SendMessage(MessageType.Chat, (player, localizer) => localizer.Get("greeting"));
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
manager.SendMessage(MessageType.Chat, (player, localizer) => "Hello", 5000);
```

### SendMessageAsync

```csharp
Task SendMessageAsync(MessageType kind, string message)
```

异步向玩家发送指定类型的消息。

**参数:**

- `kind` (`MessageType`) - 要发送的消息类型。决定消息的处理方式或显示方式。
- `message` (`string`) - 要发送的消息内容。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await playerManager.SendMessageAsync(MessageType.Chat, "Hello Player!");
```

### SendMessageAsync

```csharp
Task SendMessageAsync(MessageType kind, string message, int htmlDuration = 5000)
```

异步地向玩家发送指定类型的消息，并附带自定义的 HTML 持续时间。

**参数:**

- `kind` (`MessageType`) - 要发送的消息类型。决定消息的处理方式或显示方式。
- `message` (`string`) - 要发送的消息内容。不能为 null。
- `htmlDuration` (`int`) = `5000` - 消息以 HTML 格式显示的持续时间（单位：毫秒）。

**返回值:** `Task`

**用法示例:**
```csharp
await playerManager.SendMessageAsync(MessageType.Value, "Hello World", 5000);
```

### SendMessageAsync

```csharp
Task SendMessageAsync(MessageType kind, Func<IPlayer, ILocalizer, string> messageCallback)
```

根据消息类型使用不同的显示方法向玩家广播消息。非线程安全，在非主线程上下文中请使用异步变体。

**参数:**

- `kind` (`MessageType`) - 消息显示的类型。
- `messageCallback` (`Func\<IPlayer, ILocalizer, string\>`) - 发送给玩家的通知回调。

**返回值:** `Task`

**用法示例:**
```csharp
await manager.SendMessageAsync(MessageType.Chat, (player, localizer) => "Hello");
```

### SendMessageAsync

```csharp
Task SendMessageAsync(MessageType kind, Func<IPlayer, ILocalizer, string> messageCallback, int htmlDuration = 5000)
```

将指定类型的消息发送给玩家，并附带自定义的 HTML 持续时长。此方法非线程安全，在非主线程上下文中请使用异步变体。

**参数:**

- `kind` (`MessageType`) - 要发送的消息类型。决定消息的处理方式或显示方式。
- `messageCallback` (`Func\<IPlayer, ILocalizer, string\>`) - 发送消息的回调函数。不能为 null。
- `htmlDuration` (`int`) = `5000` - 消息以 HTML 格式显示的持续时间（单位：毫秒）。

**返回值:** `Task`

**用法示例:**
```csharp
await manager.SendMessageAsync(MessageType.Chat, (p, l) => "Hello", 5000);
```

### SendNotify

```csharp
void SendNotify(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
playerManager.SendNotify("Server restarting in 5 minutes");
```

### SendNotifyAsync

```csharp
Task SendNotifyAsync(string message)
```

异步向玩家发送通知消息。

**参数:**

- `message` (`string`) - 要发送的消息内容。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await playerManagerService.SendNotifyAsync("Welcome to the server!");
```

### SendConsole

```csharp
void SendConsole(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
playerManagerService.SendConsole("sv_restart 1");
```

### SendConsoleAsync

```csharp
Task SendConsoleAsync(string message)
```

异步向玩家发送控制台消息。

**参数:**

- `message` (`string`) - 要发送的消息内容。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await manager.SendConsoleAsync("Server restarting in 5 seconds.");
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

异步向玩家发送聊天消息。

**参数:**

- `message` (`string`) - 要发送的消息内容。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await playerManagerService.SendChatAsync("Hello, players!");
```

### SendCenter

```csharp
void SendCenter(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
manager.SendCenter("Server restarting in 5 minutes!");
```

### SendCenterAsync

```csharp
Task SendCenterAsync(string message)
```

异步向玩家发送一条居中消息。

**参数:**

- `message` (`string`) - 要发送的消息内容。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await playerManager.SendCenterAsync("比赛即将开始");
```

### SendAlert

```csharp
void SendAlert(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
manager.SendAlert("Server is restarting in 5 minutes!");
```

### SendAlertAsync

```csharp
Task SendAlertAsync(string message)
```

异步向玩家发送警报消息。

**参数:**

- `message` (`string`) - 要发送的消息内容。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await playerManagerService.SendAlertAsync("Server restarting in 5 minutes!");
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
playerManagerService.SendCenterHTML("<font color='red'>重要通知</font>", 5);
```

### SendCenterHTMLAsync

```csharp
Task SendCenterHTMLAsync(string message, int duration = 5000)
```

异步向玩家发送中心 HTML 消息。

**参数:**

- `message` (`string`) - 要发送的消息内容。不能为 null。
- `duration` (`int`) = `5000` - 消息以 HTML 格式显示的持续时间（单位：毫秒）。

**返回值:** `Task`

**用法示例:**
```csharp
await playerManagerService.SendCenterHTMLAsync("<font color='red'>Hello</font>", 5);
```

### SendChatEOT

```csharp
void SendChatEOT(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
manager.SendChatEOT("Hello, world!");
```

### SendChatEOTAsync

```csharp
Task SendChatEOTAsync(string message)
```

异步向玩家发送文本聊天消息。

**参数:**

- `message` (`string`) - 要发送的消息内容。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await playerManagerService.SendChatEOTAsync("Hello, players!");
```

### ShouldBlockTransmitEntity

```csharp
void ShouldBlockTransmitEntity(int entityid, bool shouldBlockTransmit)
```

控制是否应阻止特定实体向客户端进行传输/同步。

**参数:**

- `entityid` (`int`)
- `shouldBlockTransmit` (`bool`)

**用法示例:**
```csharp
manager.ShouldBlockTransmitEntity(1024, true);
```

### ClearAllBlockedTransmitEntities

```csharp
void ClearAllBlockedTransmitEntities()
```

移除所有实体传输块，使所有先前被阻止的实体能够再次向客户端进行传输。

**用法示例:**
```csharp
manager.ClearAllBlockedTransmitEntities();
```

### GetPlayer

```csharp
IPlayer? GetPlayer(int playerid)
```

获取与指定玩家 ID 关联的玩家。

**参数:**

- `playerid` (`int`) - 待检索玩家的唯一标识符。必须为有效的玩家 ID。

**返回值:** `IPlayer?` - 表示指定 ID 玩家的 <see cref="IPlayer"/> 实例，若不存在该玩家则为 <c>null</c>。

**用法示例:**
```csharp
IPlayer? player = manager.GetPlayer(1);
```

### GetPlayerFromController

```csharp
IPlayer? GetPlayerFromController(CBasePlayerController controller)
```

获取与指定控制器关联的玩家。

**参数:**

- `controller` (`CBasePlayerController`) - 获取玩家的控制器。

**返回值:** `IPlayer?` - 一个代表指定控制器的玩家的 <see cref="IPlayer"/> 实例，如果不存在此类玩家，则为 <c>null</c>。

**用法示例:**
```csharp
IPlayer? player = manager.GetPlayerFromController(controller);
```

### GetPlayerFromPawn

```csharp
IPlayer? GetPlayerFromPawn(CBasePlayerPawn pawn)
```

获取与指定棋子关联的玩家。

**参数:**

- `pawn` (`CBasePlayerPawn`) - 用于从玩家处检索棋子。

**返回值:** `IPlayer?` - 一个表示拥有指定棋子玩家的 <see cref="IPlayer"/> 实例；若不存在此类玩家，则为 <c>null</c>。

**用法示例:**
```csharp
IPlayer? player = manager.GetPlayerFromPawn(pawn);
```

### GetAllPlayers

```csharp
IEnumerable<IPlayer> GetAllPlayers()
```

获取当前所有在线玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 表示所有在线玩家的 IPlayer 实例的可枚举集合。

**用法示例:**
```csharp
var players = manager.GetAllPlayers();
```

### GetAllValidPlayers

```csharp
IEnumerable<IPlayer> GetAllValidPlayers()
```

获取当前在线的所有有效玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 表示所有在线玩家的 IPlayer 实例的可枚举集合。

**用法示例:**
```csharp
var players = manager.GetAllValidPlayers();
```

### GetBots

```csharp
IEnumerable<IPlayer> GetBots()
```

检索当前在线的所有机器人玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 一个包含所有在线机器人玩家实例的 <see cref="IPlayer"/> 可枚举集合。

**用法示例:**
```csharp
var bots = manager.GetBots();
```

### GetAlive

```csharp
IEnumerable<IPlayer> GetAlive()
```

获取当前在线的所有存活玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 一个可枚举集合，包含代表当前在线所有存活玩家的 <see cref="IPlayer"/> 实例。

**用法示例:**
```csharp
var alivePlayers = manager.GetAlive();
```

### GetCT

```csharp
IEnumerable<IPlayer> GetCT()
```

获取当前所有在线的 CT 玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 一个可枚举集合，包含所有当前在线的 CT 玩家实例。

**用法示例:**
```csharp
var ctPlayers = manager.GetCT();
```

### GetT

```csharp
IEnumerable<IPlayer> GetT()
```

获取当前在线的所有 T 玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 一个包含 <see cref="IPlayer"/> 实例的可枚举集合，代表当前在线的所有 T 方玩家。

**用法示例:**
```csharp
var tPlayers = manager.GetT();
```

### GetSpectators

```csharp
IEnumerable<IPlayer> GetSpectators()
```

获取当前在线的所有观战玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 一个表示当前在线的所有观战玩家的 `IPlayer` 实例的可枚举集合。

**用法示例:**
```csharp
var spectators = playerManager.GetSpectators();
```

### GetInTeam

```csharp
IEnumerable<IPlayer> GetInTeam(Team team)
```

获取指定队伍中的所有玩家。

**参数:**

- `team` (`Team`) - 要检索玩家所属的队伍。

**返回值:** `IEnumerable\<IPlayer\>` - 一个包含指定队伍中所有玩家实例的 IPlayer 枚举集合。

**用法示例:**
```csharp
var players = manager.GetInTeam(Team.Value);
```

### GetTAlive

```csharp
IEnumerable<IPlayer> GetTAlive()
```

检索当前在线的所有存活 T 方玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 表示当前在线的所有存活恐怖分子（T）玩家的 <see cref="IPlayer"/> 实例的可枚举集合。

**用法示例:**
```csharp
var aliveTPlayers = manager.GetTAlive();
```

### GetCTAlive

```csharp
IEnumerable<IPlayer> GetCTAlive()
```

获取当前在线的所有存活反恐精英（CT）玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 一个包含当前在线的所有存活 CT 玩家实例的 IPlayer 可枚举集合。

**用法示例:**
```csharp
var ctPlayers = manager.GetCTAlive();
```

### IsSessionIdValid

```csharp
bool IsSessionIdValid(ulong sessionId)
```

检查特定会话 ID 是否有效。当关联的玩家已断开连接或不存在时，该会话 ID 将无效。

**参数:**

- `sessionId` (`ulong`) - 要检查的会话 ID。

**返回值:** `bool` - 若会话 ID 有效则为 true，否则为 false。

**用法示例:**
```csharp
bool isValid = playerManager.IsSessionIdValid(sessionId);
```

### GetPlayerFromSessionId

```csharp
IPlayer? GetPlayerFromSessionId(ulong sessionId)
```

检索与指定会话 ID 关联的玩家。

**参数:**

- `sessionId` (`ulong`) - 用于检索玩家的会话 ID。

**返回值:** `IPlayer?` - 一个表示具有指定会话 ID 的玩家的 <see cref="IPlayer"/> 实例；若会话 ID 已释放或无效，则为 <c>null</c>。

**用法示例:**
```csharp
var player = manager.GetPlayerFromSessionId(sessionId);
```

### GetPlayerFromSteamId

```csharp
IPlayer? GetPlayerFromSteamId(ulong steamId, bool allowUnauthorized = true)
```

获取与指定 Steam ID 关联的玩家。

**参数:**

- `steamId` (`ulong`) - 用于检索玩家的 Steam ID。
- `allowUnauthorized` (`bool`) = `true` - 是否允许未授权玩家加入。

**返回值:** `IPlayer?` - 一个表示具有指定 Steam ID 的玩家实例，若该玩家不存在则返回 null。

**用法示例:**
```csharp
var player = manager.GetPlayerFromSteamId(76561198000000000, false);
```

