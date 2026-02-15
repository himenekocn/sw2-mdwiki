# 🔌 IPlayer

**命名空间:** `SwiftlyS2.Shared.Players`

**类型:** `interface`

**继承:** `IEquatable\<IPlayer\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlayerID` | `int` | get | 获取玩家的唯一标识符。 |
| `SessionId` | `ulong` | get | 获取玩家的会话 ID。 |
| `UserID` | `int` | get | 获取玩家的用户ID。 |
| `Slot` | `int` | get | 获取玩家的槽位。等同于玩家ID。 |
| `Name` | `string` | get | 获取玩家的名称。 |
| `IsFakeClient` | `bool` | get | 客户端是否为机器人。 |
| `IsAuthorized` | `bool` | get | 当前用户是否已通过 Steam 授权。 |
| `ConnectedTime` | `uint` | get | 获取连接处于活动状态的总时间（以秒为单位）。 |
| `SteamID` | `ulong` | get | 获取与用户关联的唯一 Steam 标识符。 |
| `UnauthorizedSteamID` | `ulong` | get | 获取尚未验证的 Steam ID。 |
| `IsAlive` | `bool` | get | 获取一个值，该值指示玩家当前是否存活。 |
| `Controller` | `CCSPlayerController` | get | 获取与玩家关联的玩家控制器。 |
| `RequiredController` | `CCSPlayerController` | get | 获取与玩家关联的玩家控制器。要求控制器必须有效。 <exception cref="InvalidOperationException">当控制器无效时抛出。</exception> |
| `Pawn` | `CBasePlayerPawn?` | get | 获取与玩家关联的棋子。 |
| `RequiredPawn` | `CBasePlayerPawn` | get | 获取与玩家关联的棋子。要求棋子必须有效。 <exception cref="InvalidOperationException">当棋子无效时抛出。</exception> |
| `PlayerPawn` | `CCSPlayerPawn?` | get | 获取与该玩家关联的玩家棋子。 |
| `RequiredPlayerPawn` | `CCSPlayerPawn` | get | 获取与玩家关联的玩家 pawn。要求玩家 pawn 必须有效。 <exception cref="InvalidOperationException">当玩家 pawn 无效时抛出。</exception> |
| `PressedButtons` | `GameButtonFlags` | get | 获取当前处于按下状态的按键集合。 |
| `IPAddress` | `string` | get | 获取与玩家关联的IP地址。 |
| `VoiceFlags` | `VoiceFlagValue` | get, set | 获取或设置指定要应用的语音选项或功能的标志集。 |
| `PlayerLanguage` | `Language` | get | 获取玩家的语言。 |
| `IsFirstSpawn` | `bool` | get | 指示这是否是玩家的首次生成。 |
| `IsValid` | `bool` | get | 检查玩家是否有效（拥有控制器、不是HLTV、已连接且拥有棋子）。 |

## ⚙️ 方法

### SendMessage

```csharp
void SendMessage(MessageType kind, string message)
```

**参数:**

- `kind` (`MessageType`)
- `message` (`string`)

**用法示例:**
```csharp
player.SendMessage(MessageType.Info, "Hello");
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
player.SendMessage(MessageType.Info, "Hello World", 3000);
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
await player.SendMessageAsync(MessageType.Value, "Hello");
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
await player.SendMessageAsync(MessageType.Info, "Hello World", 3000);
```

### SendNotify

```csharp
void SendNotify(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
player.SendNotify("Game started");
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
await player.SendNotifyAsync("Hello, player!");
```

### SendConsole

```csharp
void SendConsole(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
player.SendConsole("Hello World");
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
await player.SendConsoleAsync("Hello, console!");
```

### SendChat

```csharp
void SendChat(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
player.SendChat("Hello, world!");
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
await player.SendChatAsync("Hello, world!");
```

### SendCenter

```csharp
void SendCenter(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
player.SendCenter("Hello from center");
```

### SendCenterAsync

```csharp
Task SendCenterAsync(string message)
```

异步地向玩家发送一条中心消息。

**参数:**

- `message` (`string`) - 要发送的消息内容。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await player.SendCenterAsync("Hello from center!");
```

### SendAlert

```csharp
void SendAlert(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
player.SendAlert("Game started!");
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
await player.SendAlertAsync("Game starting in 30 seconds!");
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
player.SendCenterHTML("Game Started!", 3);
```

### SendCenterHTMLAsync

```csharp
Task SendCenterHTMLAsync(string message, int duration = 5000)
```

异步地向玩家发送一个居中的HTML消息。

**参数:**

- `message` (`string`) - 要发送的消息内容。不能为 null。
- `duration` (`int`) = `5000` - 消息应以HTML格式显示的持续时间（以毫秒为单位）。

**返回值:** `Task`

**用法示例:**
```csharp
await player.SendCenterHTMLAsync("<color=red>Game Over</color>", 5);
```

### SendChatEOT

```csharp
void SendChatEOT(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
player.SendChatEOT("Hello");
```

### SendChatEOTAsync

```csharp
Task SendChatEOTAsync(string message)
```

异步地向玩家发送一条文本结束聊天消息。

**参数:**

- `message` (`string`) - 要发送的消息内容。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await player.SendChatEOTAsync("Game ended.");
```

### Kick

```csharp
void Kick(string reason, ENetworkDisconnectionReason gameReason)
```

**参数:**

- `reason` (`string`)
- `gameReason` (`ENetworkDisconnectionReason`)

**用法示例:**
```csharp
player.Kick("Connection lost", ENetworkDisconnectionReason.Timeout);
```

### KickAsync

```csharp
Task KickAsync(string reason, ENetworkDisconnectionReason gameReason)
```

异步断开用户与网络会话的连接，并提供指定的断开原因和断开类型。

**参数:**

- `reason` (`string`) - 描述断开连接原因的消息。此消息可能会显示给用户。不能为 null 或空。
- `gameReason` (`ENetworkDisconnectionReason`) - 断开连接原因代码，用于指示要执行的网络断开连接类型。

**返回值:** `Task`

**用法示例:**
```csharp
await player.KickAsync("玩家行为异常", ENetworkDisconnectionReason.Timeout);
```

### ShouldBlockTransmitEntity

```csharp
void ShouldBlockTransmitEntity(int entityid, bool shouldBlockTransmit)
```

设置是否应阻止指定实体的传输。

**参数:**

- `entityid` (`int`) - 要更新其传输状态的实体的唯一标识符。
- `shouldBlockTransmit` (`bool`) - 一个指示是否应阻止实体传输的值。指定 <see langword="true"/> 以阻止传输；否则，<see langword="false"/>。

**用法示例:**
```csharp
player.ShouldBlockTransmitEntity(123, true);
```

### IsTransmitEntityBlocked

```csharp
bool IsTransmitEntityBlocked(int entityid)
```

确定指定的实体当前是否被阻止传输数据。

**参数:**

- `entityid` (`int`) - 要检查其传输阻塞的实体的唯一标识符。必须是有效的实体ID。

**返回值:** `bool` - 如果实体被阻止传输，则为 true；否则为 false。

**用法示例:**
```csharp
bool blocked = player.IsTransmitEntityBlocked(123);
```

### ClearTransmitEntityBlocks

```csharp
void ClearTransmitEntityBlocks()
```

从传输缓冲区中移除所有实体块，丢弃所有已安排的待传输数据。

**用法示例:**
```csharp
player.ClearTransmitEntityBlocks();
```

### SetListenOverride

```csharp
void SetListenOverride(int player, ListenOverride listenOverride)
```

为指定玩家设置自定义监听覆盖。

**参数:**

- `player` (`int`) - 要更新其监听覆盖设置的玩家的标识符。必须是有效的玩家索引。
- `listenOverride` (`ListenOverride`) - 要应用于指定玩家的监听覆盖值。

**用法示例:**
```csharp
player.SetListenOverride(1, ListenOverride.Value);
```

### GetListenOverride

```csharp
ListenOverride GetListenOverride(int player)
```

获取指定玩家的监听覆盖设置。

**参数:**

- `player` (`int`) - 要检索其监听覆盖设置的玩家的标识符。必须是有效的玩家索引。

**返回值:** `ListenOverride` - 一个包含指定玩家监听覆盖设置的 ListenOverride 对象。

**用法示例:**
```csharp
ListenOverride override = IPlayer.GetListenOverride(1);
```

### TakeDamage

```csharp
void TakeDamage(CTakeDamageInfo damageInfo)
```

**参数:**

- `damageInfo` (`CTakeDamageInfo`)

**用法示例:**
```csharp
player.TakeDamage(CTakeDamageInfo.Create(10.0f, DMG_GENERIC, null));
```

### TakeDamageAsync

```csharp
Task TakeDamageAsync(CTakeDamageInfo damageInfo)
```

根据指定的伤害信息，异步地对实体造成伤害。

**参数:**

- `damageInfo` (`CTakeDamageInfo`) - 一个包含待应用伤害详情的对象，包括伤害值、类型和来源。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await player.TakeDamageAsync(new CTakeDamageInfo(10.0f, DMG_GENERIC, Vector.Zero, Vector.Zero));
```

### TakeDamage

```csharp
void TakeDamage(float damage, DamageTypes_t damageType, CBaseEntity? inflictor = null, CBaseEntity? attacker = null, CBaseEntity? ability = null)
```

**参数:**

- `damage` (`float`)
- `damageType` (`DamageTypes_t`)
- `inflictor` (`CBaseEntity?`) = `null`
- `attacker` (`CBaseEntity?`) = `null`
- `ability` (`CBaseEntity?`) = `null`

**用法示例:**
```csharp
player.TakeDamage(10.0f, DamageTypes_t.BULLET, null, attackerEntity, null);
```

### TakeDamageAsync

```csharp
Task TakeDamageAsync(float damage, DamageTypes_t damageType, CBaseEntity? inflictor = null, CBaseEntity? attacker = null, CBaseEntity? ability = null)
```

根据指定的伤害信息，异步地对实体造成伤害。

**参数:**

- `damage` (`float`) - 要应用的伤害量。
- `damageType` (`DamageTypes_t`) - 要应用的伤害类型。
- `inflictor` (`CBaseEntity?`) = `null` - 造成伤害的实体。可以为 null。
- `attacker` (`CBaseEntity?`) = `null` - 正在攻击的实体。可以为 null。
- `ability` (`CBaseEntity?`) = `null` - 造成伤害的能力。可以为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await player.TakeDamageAsync(10f, DamageTypes_t.BULLET, null, attackerEntity, null);
```

### Teleport

```csharp
void Teleport(Vector pos, QAngle angle, Vector velocity)
```

**参数:**

- `pos` (`Vector`)
- `angle` (`QAngle`)
- `velocity` (`Vector`)

**用法示例:**
```csharp
player.Teleport(Vector.Zero, QAngle.Zero, Vector.Zero);
```

### Teleport

```csharp
void Teleport(Vector? pos = null, QAngle? angle = null, Vector? velocity = null)
```

**参数:**

- `pos` (`Vector?`) = `null`
- `angle` (`QAngle?`) = `null`
- `velocity` (`Vector?`) = `null`

**用法示例:**
```csharp
player.Teleport(new Vector(0, 0, 0), new QAngle(0, 0, 0), new Vector(0, 0, 0));
```

### TeleportAsync

```csharp
Task TeleportAsync(Vector pos, QAngle angle, Vector velocity)
```

异步地将实体传送至指定的位置、朝向和速度。

**参数:**

- `pos` (`Vector`) - 要传送实体到的目标位置，以 <see cref="Vector"/> 表示。
- `angle` (`QAngle`) - 传送后应用于实体的朝向，以 <see cref="QAngle"/> 表示。
- `velocity` (`Vector`) - 实体到达时分配的速度，以 <see cref="Vector"/> 表示。

**返回值:** `Task`

**用法示例:**
```csharp
await player.TeleportAsync(new Vector(100, 200, 300), new QAngle(0, 90, 0), Vector.Zero);
```

### TeleportAsync

```csharp
Task TeleportAsync(Vector? pos = null, QAngle? angle = null, Vector? velocity = null)
```

异步地将实体传送至指定的位置、朝向和速度。

**参数:**

- `pos` (`Vector?`) = `null` - 要传送实体到的目标位置，以 <see cref="Vector"/> 表示。
- `angle` (`QAngle?`) = `null` - 传送后应用于实体的朝向，以 <see cref="QAngle"/> 表示。
- `velocity` (`Vector?`) = `null` - 实体到达时分配的速度，以 <see cref="Vector"/> 表示。

**返回值:** `Task`

**用法示例:**
```csharp
await player.TeleportAsync(new Vector(100, 200, 300), new QAngle(0, 90, 0), new Vector(50, 0, 0));
```

### SwitchTeam

```csharp
void SwitchTeam(Team team)
```

**参数:**

- `team` (`Team`)

**用法示例:**
```csharp
player.SwitchTeam(Team.T);
```

### SwitchTeamAsync

```csharp
Task SwitchTeamAsync(Team team)
```

异步切换玩家所属队伍。

**参数:**

- `team` (`Team`) - 要切换到的团队。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await player.SwitchTeamAsync(Team.T);
```

### ChangeTeam

```csharp
void ChangeTeam(Team team)
```

**参数:**

- `team` (`Team`)

**用法示例:**
```csharp
player.ChangeTeam(Team.T);
```

### ChangeTeamAsync

```csharp
Task ChangeTeamAsync(Team team)
```

异步更改玩家的队伍。此操作也会击杀该玩家。

**参数:**

- `team` (`Team`) - 要分配的团队。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await player.ChangeTeamAsync(Team.T);
```

### Respawn

```csharp
void Respawn()
```

重生玩家。

**用法示例:**
```csharp
player.Respawn();
```

### ExecuteCommand

```csharp
void ExecuteCommand(string command)
```

**参数:**

- `command` (`string`)

**用法示例:**
```csharp
player.ExecuteCommand("start_match");
```

### ExecuteCommandAsync

```csharp
Task ExecuteCommandAsync(string command)
```

以异步方式代表玩家执行命令。

**参数:**

- `command` (`string`) - 要执行的命令。不能为 null 或空。

**返回值:** `Task`

**用法示例:**
```csharp
await player.ExecuteCommandAsync("join_team T");
```

