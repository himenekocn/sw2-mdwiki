<a id="iplayermanagerservice"></a>

# 🔌 IPlayerManagerService

**命名空间:** `SwiftlyS2.Shared.Players`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlayerCount` | `int` | get | 获取当前游戏中的玩家数量。 |
| `PlayerCap` | `int` | get | 获取引擎允许的最大玩家数量。 |
| `MaxPlayers` | `int` | get | 获取服务器配置允许的最大玩家数量。 |

## ⚙️ 方法

### IsPlayerOnline

```csharp
bool IsPlayerOnline(int playerid)
```

检查特定玩家当前是否在线并连接到服务器。

**参数:**

- `playerid` (`int`)

**返回值:** `bool` - 如果玩家在线则为真，否则为假。

**用法示例:**
```csharp
bool isOnline = playerManager.IsPlayerOnline(1);
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
playerManager.SendMessage(MessageType.Chat, "Hello World");
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
playerManagerService.SendMessage(MessageType.Value, "Hello", 5);
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
manager.SendMessage(MessageType.Chat, (player, localizer) => "Hello");
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
manager.SendMessage(MessageType.Value, (player, localizer) => "Hello", 5);
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
await playerManager.SendMessageAsync(MessageType.Info, "Hello Player");
```

### SendMessageAsync

```csharp
Task SendMessageAsync(MessageType kind, string message, int htmlDuration = 5000)
```

以自定义HTML持续时间异步向玩家发送指定类型的消息。

**参数:**

- `kind` (`MessageType`) - 要发送的消息类型。决定消息的处理或显示方式。
- `message` (`string`) - 要发送的消息内容。不能为 null。
- `htmlDuration` (`int`) = `5000` - 该消息应以HTML格式显示的持续时间，单位毫秒。

**返回值:** `Task`

**用法示例:**
```csharp
await playerManager.SendMessageAsync(MessageType.Chat, "Hello World", 5000);
```

### SendMessageAsync

```csharp
Task SendMessageAsync(MessageType kind, Func<IPlayer, ILocalizer, string> messageCallback)
```

根据消息类型使用不同的显示方法向玩家广播消息。非线程安全，在非主线程上下文中请改用异步变体。

**参数:**

- `kind` (`MessageType`) - 消息显示的类型。
- `messageCallback` (`Func\<IPlayer, ILocalizer, string\>`) - 发送给玩家的文本回调。

**返回值:** `Task`

**用法示例:**
```csharp
await playerManager.SendMessageAsync(MessageType.Chat, (p, l) => "Hello");
```

### SendMessageAsync

```csharp
Task SendMessageAsync(MessageType kind, Func<IPlayer, ILocalizer, string> messageCallback, int htmlDuration = 5000)
```

向指定类型的玩家发送一条带有自定义HTML持续时间的消息。线程不安全，非主线程上下文中请改用异步变体。

**参数:**

- `kind` (`MessageType`) - 要发送的消息类型。决定消息的处理或显示方式。
- `messageCallback` (`Func\<IPlayer, ILocalizer, string\>`) - 要发送的消息的回调。不能为 null。
- `htmlDuration` (`int`) = `5000` - 该消息应以HTML格式显示的持续时间，单位毫秒。

**返回值:** `Task`

**用法示例:**
```csharp
await playerManager.SendMessageAsync(MessageType.Chat, (player, localizer) => "Hello", 5);
```

### SendNotify

```csharp
void SendNotify(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
playerManager.SendNotify("Hello World");
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
await playerManagerService.SendNotifyAsync("Welcome to the game!");
```

### SendConsole

```csharp
void SendConsole(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
playerManagerService.SendConsole("status");
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
await manager.SendConsoleAsync("Hello World");
```

### SendChat

```csharp
void SendChat(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
playerManager.SendChat("Hello World");
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
await playerManager.SendChatAsync("Hello World");
```

### SendCenter

```csharp
void SendCenter(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
manager.SendCenter("Hello World");
```

### SendCenterAsync

```csharp
Task SendCenterAsync(string message)
```

异步向玩家发送中心消息。

**参数:**

- `message` (`string`) - 要发送的消息内容。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await playerManager.SendCenterAsync("Welcome to the game!");
```

### SendAlert

```csharp
void SendAlert(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
manager.SendAlert("Hello, Player!");
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
await manager.SendAlertAsync("服务器即将重启");
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
playerManagerService.SendCenterHTML("<font color='red'>Hello World</font>", 5);
```

### SendCenterHTMLAsync

```csharp
Task SendCenterHTMLAsync(string message, int duration = 5000)
```

向玩家异步发送居中HTML消息。

**参数:**

- `message` (`string`) - 要发送的消息内容。不能为 null。
- `duration` (`int`) = `5000` - 该消息应以HTML格式显示的持续时间，单位毫秒。

**返回值:** `Task`

**用法示例:**
```csharp
await playerManager.SendCenterHTMLAsync("<font color='red'>Welcome!</font>", 5);
```

### SendChatEOT

```csharp
void SendChatEOT(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
playerManager.SendChatEOT("Hello World");
```

### SendChatEOTAsync

```csharp
Task SendChatEOTAsync(string message)
```

异步向玩家发送一条文本结束聊天消息。

**参数:**

- `message` (`string`) - 要发送的消息内容。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await playerManagerService.SendChatEOTAsync("聊天结束");
```

### ShouldBlockTransmitEntity

```csharp
void ShouldBlockTransmitEntity(int entityid, bool shouldBlockTransmit)
```

控制特定实体是否应被阻止传输/同步至客户端。

**参数:**

- `entityid` (`int`)
- `shouldBlockTransmit` (`bool`)

**用法示例:**
```csharp
playerManager.ShouldBlockTransmitEntity(1001, true);
```

### ClearAllBlockedTransmitEntities

```csharp
void ClearAllBlockedTransmitEntities()
```

移除所有实体传输阻止，使所有先前被阻止的实体能够再次传输到客户端。

**用法示例:**
```csharp
manager.ClearAllBlockedTransmitEntities();
```

### GetPlayer

```csharp
IPlayer? GetPlayer(int playerid)
```

获取与指定玩家ID关联的玩家对象。

**参数:**

- `playerid` (`int`) - 要检索的玩家的唯一标识符。必须是一个有效的玩家ID。

**返回值:** `IPlayer?` - 一个表示具有指定ID的玩家的<see cref="IPlayer"/>实例，如果该玩家不存在则为<c>null</c>。

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

- `controller` (`CBasePlayerController`) - 用于从中获取玩家角色的控制器。

**返回值:** `IPlayer?` - 一个表示具有指定控制器的玩家的 <see cref="IPlayer"/> 实例，如果不存在这样的玩家，则为 <c>null</c>。

**用法示例:**
```csharp
IPlayer? player = manager.GetPlayerFromController(controller);
```

### GetPlayerFromPawn

```csharp
IPlayer? GetPlayerFromPawn(CBasePlayerPawn pawn)
```

检索与指定棋子关联的玩家。

**参数:**

- `pawn` (`CBasePlayerPawn`) - 从中检索玩家的棋子。

**返回值:** `IPlayer?` - 表示具有指定棋子的玩家的 <see cref="IPlayer"/> 实例，如果不存在这样的玩家，则为 <c>null</c>。

**用法示例:**
```csharp
IPlayer? player = manager.GetPlayerFromPawn(pawn);
```

### GetAllPlayers

```csharp
IEnumerable<IPlayer> GetAllPlayers()
```

检索当前在线的所有玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 表示所有在线玩家的 <see cref="IPlayer"/> 实例的可枚举集合。

**用法示例:**
```csharp
var players = manager.GetAllPlayers();
```

### GetAllValidPlayers

```csharp
IEnumerable<IPlayer> GetAllValidPlayers()
```

获取当前在线所有有效玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 表示所有在线玩家的 <see cref="IPlayer"/> 实例的可枚举集合。

**用法示例:**
```csharp
var players = manager.GetAllValidPlayers();
```

### GetBots

```csharp
IEnumerable<IPlayer> GetBots()
```

获取当前在线的所有机器人玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 表示所有在线机器人玩家的 <see cref="IPlayer"/> 实例的可枚举集合。

**用法示例:**
```csharp
var bots = playerManager.GetBots();
```

### GetAlive

```csharp
IEnumerable<IPlayer> GetAlive()
```

获取当前在线的所有存活玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 一个可枚举的<see cref="IPlayer"/>实例集合，表示当前在线且存活的全部玩家。

**用法示例:**
```csharp
var alivePlayers = manager.GetAlive();
```

### GetCT

```csharp
IEnumerable<IPlayer> GetCT()
```

检索当前在线的所有CT玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 一个可枚举的集合，包含当前在线所有CT玩家的<see cref="IPlayer"/>实例。

**用法示例:**
```csharp
var ctPlayers = playerManager.GetCT();
```

### GetT

```csharp
IEnumerable<IPlayer> GetT()
```

获取当前在线的所有T阵营玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 表示当前在线所有T阵营玩家的 <see cref="IPlayer"/> 实例的可枚举集合。

**用法示例:**
```csharp
var tPlayers = playerManager.GetT();
```

### GetSpectators

```csharp
IEnumerable<IPlayer> GetSpectators()
```

获取当前所有在线观战玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 表示当前在线所有观察者玩家的 <see cref="IPlayer"/> 实例的可枚举集合。

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

- `team` (`Team`) - 要检索玩家的队伍。

**返回值:** `IEnumerable\<IPlayer\>` - 表示指定队伍中所有玩家的<see cref="IPlayer"/>实例的可枚举集合。

**用法示例:**
```csharp
var players = manager.GetInTeam(Team.Red);
```

### GetTAlive

```csharp
IEnumerable<IPlayer> GetTAlive()
```

检索当前在线所有存活T阵营玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 一个可枚举的集合，包含当前在线所有存活的T方玩家的 <see cref="IPlayer"/> 实例。

**用法示例:**
```csharp
var aliveTPlayers = playerManager.GetTAlive();
```

### GetCTAlive

```csharp
IEnumerable<IPlayer> GetCTAlive()
```

获取所有当前在线的存活CT玩家。

**返回值:** `IEnumerable\<IPlayer\>` - 一个可枚举的集合，包含当前在线的所有存活CT玩家的<see cref="IPlayer"/>实例。

**用法示例:**
```csharp
var ctAlivePlayers = playerManager.GetCTAlive();
```

### IsSessionIdValid

```csharp
bool IsSessionIdValid(ulong sessionId)
```

检查特定会话ID是否有效。当关联玩家断开连接或不存在时，会话ID将无效。

**参数:**

- `sessionId` (`ulong`) - 要检查的会话ID。

**返回值:** `bool` - 如果会话ID有效则为真，否则为假。

**用法示例:**
```csharp
bool isValid = playerManager.IsSessionIdValid(123456789UL);
```

### GetPlayerFromSessionId

```csharp
IPlayer? GetPlayerFromSessionId(ulong sessionId)
```

获取与指定会话ID关联的玩家。

**参数:**

- `sessionId` (`ulong`) - 用于从中检索玩家的会话ID。

**返回值:** `IPlayer?` - 一个 <see cref="IPlayer"/> 实例，表示具有指定会话ID的玩家，如果会话ID已释放或无效，则为 <c>null</c>。玩家存在。

**用法示例:**
```csharp
var player = manager.GetPlayerFromSessionId(sessionId);
```

### GetPlayerFromSteamId

```csharp
IPlayer? GetPlayerFromSteamId(ulong steamId, bool allowUnauthorized = true)
```

获取与指定Steam ID关联的玩家。

**参数:**

- `steamId` (`ulong`) - 用于检索玩家的Steam ID。
- `allowUnauthorized` (`bool`) = `true` - 是否允许未授权的玩家。

**返回值:** `IPlayer?` - 表示具有指定Steam ID的玩家的<see cref="IPlayer"/>实例，如果该玩家不存在则为<c>null</c>。

**用法示例:**
```csharp
var player = playerManager.GetPlayerFromSteamId(76561198000000000, false);
```

