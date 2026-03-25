<a id="iplayer"></a>

# 🔌 IPlayer

**命名空间:** `SwiftlyS2.Shared.Players`

**类型:** `interface`

**继承:** `IEquatable\<IPlayer\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlayerID` | `int` | get | 获取玩家的唯一标识符。 |
| `SessionId` | `ulong` | get | 获取玩家的会话 ID。 |
| `UserID` | `int` | get | 获取玩家的用户 ID。 |
| `Slot` | `int` | get | 获取玩家的槽位。等同于玩家 ID。 |
| `Name` | `string` | get | 获取玩家的名称。 |
| `IsFakeClient` | `bool` | get | 该客户端是否为机器人。 |
| `IsAuthorized` | `bool` | get | 当前用户是否已通过 Steam 授权。 |
| `ConnectedTime` | `uint` | get | 获取连接处于活动状态的总时间（以秒为单位）。 |
| `SteamID` | `ulong` | get | 获取与该用户关联的唯一 Steam 标识符。 |
| `UnauthorizedSteamID` | `ulong` | get | 获取尚未验证的 Steam ID。 |
| `IsAlive` | `bool` | get | 获取一个值，指示玩家当前是否存活。 |
| `Controller` | `CCSPlayerController` | get | 获取与玩家关联的玩家控制器。 |
| `RequiredController` | `CCSPlayerController` | get | 获取与该玩家关联的玩家控制器。要求该控制器必须有效。<exception cref="InvalidOperationException">当控制器无效时抛出此异常。</exception> |
| `Pawn` | `CBasePlayerPawn?` | get | 获取与该玩家关联的棋子。 |
| `RequiredPawn` | `CBasePlayerPawn` | get | 获取与该玩家关联的棋子。要求该棋子必须有效。<exception cref="InvalidOperationException">当棋子无效时抛出此异常。</exception> |
| `PlayerPawn` | `CCSPlayerPawn?` | get | 获取与该玩家关联的玩家Pawn。 |
| `RequiredPlayerPawn` | `CCSPlayerPawn` | get | 获取与该玩家关联的玩家 Pawn。要求该玩家 Pawn 必须有效。<exception cref="InvalidOperationException">当玩家 Pawn 无效时抛出此异常。</exception> |
| `PressedButtons` | `GameButtonFlags` | get | 获取当前按下的游戏按键集合。 |
| `IPAddress` | `string` | get | 获取与玩家关联的 IP 地址。 |
| `VoiceFlags` | `VoiceFlagValue` | get, set | 获取或设置指定要应用的语音选项或功能的标志集。 |
| `PlayerLanguage` | `Language` | get | 获取玩家的语言设置。 |
| `IsFirstSpawn` | `bool` | get | 指示这是否为玩家的首次出生。 |
| `IsValid` | `bool` | get | 检查玩家是否有效（拥有控制器、非 HLTV 用户、已连接且存在游戏角色）。 |

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
player.SendMessage(MessageType.Chat, "Hello, world!");
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
player.SendMessage(MessageType.Chat, "Hello World!", 5);
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
await player.SendMessageAsync(MessageType.Chat, "Hello, player!");
```

### SendMessageAsync

```csharp
Task SendMessageAsync(MessageType kind, string message, int htmlDuration = 5000)
```

异步向玩家发送指定类型的消息，并附带自定义的 HTML 持续时间。

**参数:**

- `kind` (`MessageType`) - 要发送的消息类型。决定消息的处理方式或显示方式。
- `message` (`string`) - 要发送的消息内容。不能为 null。
- `htmlDuration` (`int`) = `5000` - 消息以 HTML 格式显示的持续时间（单位：毫秒）。

**返回值:** `Task`

**用法示例:**
```csharp
await player.SendMessageAsync(MessageType.Chat, "Hello!", 5000);
```

### SendNotify

```csharp
void SendNotify(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
player.SendNotify("Hello, player!");
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
await player.SendNotifyAsync("Server is restarting in 5 minutes!");
```

### SendConsole

```csharp
void SendConsole(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
player.SendConsole("sv_cheats 1");
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
await player.SendConsoleAsync("Server restarting in 5 minutes.");
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

异步向玩家发送聊天消息。

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
player.SendCenter("Welcome to the server!");
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
await player.SendCenterAsync("Welcome to the server!");
```

### SendAlert

```csharp
void SendAlert(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
player.SendAlert("Warning: Unauthorized access detected!");
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
await player.SendAlertAsync("警告：检测到异常行为！");
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
player.SendCenterHTML("<font color='red'>Hello!</font>", 5);
```

### SendCenterHTMLAsync

```csharp
Task SendCenterHTMLAsync(string message, int duration = 5000)
```

异步向玩家发送一个中心位置的 HTML 消息。

**参数:**

- `message` (`string`) - 要发送的消息内容。不能为 null。
- `duration` (`int`) = `5000` - 消息以 HTML 格式显示的持续时间（单位：毫秒）。

**返回值:** `Task`

**用法示例:**
```csharp
await player.SendCenterHTMLAsync("<font color='red'>Hello</font>", 5);
```

### SendChatEOT

```csharp
void SendChatEOT(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
player.SendChatEOT("Hello, world!");
```

### SendChatEOTAsync

```csharp
Task SendChatEOTAsync(string message)
```

异步向玩家发送一条结尾的聊天消息。

**参数:**

- `message` (`string`) - 要发送的消息内容。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await player.SendChatEOTAsync("游戏结束！");
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
player.Kick("违规操作", ENetworkDisconnectionReason.Banned);
```

### KickAsync

```csharp
Task KickAsync(string reason, ENetworkDisconnectionReason gameReason)
```

异步断开用户与网络会话的连接，并提供指定的原因和断开类型。

**参数:**

- `reason` (`string`) - 描述断开连接原因的字符串消息。此消息可能会显示给用户。不能为 null 或空。
- `gameReason` (`ENetworkDisconnectionReason`) - 指示要执行的断开网络连接类型的断开连接原因代码。

**返回值:** `Task`

**用法示例:**
```csharp
await player.KickAsync("违规操作", ENetworkDisconnectionReason.Value);
```

### ShouldBlockTransmitEntity

```csharp
void ShouldBlockTransmitEntity(int entityid, bool shouldBlockTransmit)
```

设置是否应阻止指定实体的传输。

**参数:**

- `entityid` (`int`) - 要更新其传输状态实体的唯一标识符。
- `shouldBlockTransmit` (`bool`) - 指示是否应阻止该实体的传输的值。指定 <see langword="true"/> 以阻止传输；否则，指定 <see langword="false"/>。

**用法示例:**
```csharp
player.ShouldBlockTransmitEntity(1024, true);
```

### IsTransmitEntityBlocked

```csharp
bool IsTransmitEntityBlocked(int entityid)
```

确定指定的实体当前是否被阻止传输数据。

**参数:**

- `entityid` (`int`) - 待检查传输阻塞实体的唯一标识符。必须为有效的实体 ID。

**返回值:** `bool` - 如果实体被阻止传输，则为 true；否则为 false。

**用法示例:**
```csharp
bool isBlocked = player.IsTransmitEntityBlocked(entityId);
```

### ClearTransmitEntityBlocks

```csharp
void ClearTransmitEntityBlocks()
```

从发送缓冲区中移除所有实体块，并丢弃任何已排期待发送的待定数据。

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

- `player` (`int`) - 要更新其监听覆盖设置的玩家标识符。必须是有效的玩家索引。
- `listenOverride` (`ListenOverride`) - 应用于指定玩家的监听覆盖值。

**用法示例:**
```csharp
player.SetListenOverride(0, ListenOverride.Value);
```

### GetListenOverride

```csharp
ListenOverride GetListenOverride(int player)
```

获取指定玩家的监听覆盖设置。

**参数:**

- `player` (`int`) - 待获取监听覆盖设置的目标玩家标识符。必须是有效的玩家索引。

**返回值:** `ListenOverride` - 包含指定玩家的监听覆盖设置的 ListenOverride 对象。

**用法示例:**
```csharp
var overrideSettings = player.GetListenOverride(playerIndex);
```

### GetClientConvarValue

```csharp
string GetClientConvarValue(string convarName)
```

获取 convars 的用户信息值，例如：m_yaw、sensitivity。

**参数:**

- `convarName` (`string`)

**返回值:** `string`

**用法示例:**
```csharp
string yawValue = player.GetClientConvarValue("m_yaw");
```

### TakeDamage

```csharp
void TakeDamage(CTakeDamageInfo damageInfo)
```

**参数:**

- `damageInfo` (`CTakeDamageInfo`)

**用法示例:**
```csharp
player.TakeDamage(damageInfo);
```

### TakeDamageAsync

```csharp
Task TakeDamageAsync(CTakeDamageInfo damageInfo)
```

根据指定的伤害信息，异步地对实体施加伤害。

**参数:**

- `damageInfo` (`CTakeDamageInfo`) - 一个包含待施加伤害详细信息的对象，包括伤害数值、类型和来源。该对象不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await player.TakeDamageAsync(damageInfo);
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
player.TakeDamage(50.0f, DamageTypes_t.DMG_BULLET, null, attackerEntity, null);
```

### TakeDamageAsync

```csharp
Task TakeDamageAsync(float damage, DamageTypes_t damageType, CBaseEntity? inflictor = null, CBaseEntity? attacker = null, CBaseEntity? ability = null)
```

根据指定的伤害信息，异步地对实体施加伤害。

**参数:**

- `damage` (`float`) - 要施加的伤害量。
- `damageType` (`DamageTypes_t`) - 要应用伤害的类型。
- `inflictor` (`CBaseEntity?`) = `null` - 造成伤害的实体。可能为 null。
- `attacker` (`CBaseEntity?`) = `null` - 发起攻击的实体。可能为空。
- `ability` (`CBaseEntity?`) = `null` - 造成伤害的技能。可能为空。

**返回值:** `Task`

**用法示例:**
```csharp
await player.TakeDamageAsync(25.0f, DamageTypes_t.Value, null, attackerEntity, null);
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
player.Teleport(new Vector(0, 0, 0), new QAngle(0, 0, 0), new Vector(0, 0, 0));
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
player.Teleport(new Vector(100, 200, 50), null, null);
```

### TeleportAsync

```csharp
Task TeleportAsync(Vector pos, QAngle angle, Vector velocity)
```

异步将实体传送至指定的位置、朝向和速度。

**参数:**

- `pos` (`Vector`) - 实体传送的目标位置，表示为<see cref="Vector"/>。
- `angle` (`QAngle`) - 传送后应用于实体的朝向，表示为<see cref="QAngle"/>。
- `velocity` (`Vector`) - 实体到达时被赋予的速度，以 <see cref="Vector"/> 表示。

**返回值:** `Task`

**用法示例:**
```csharp
await player.TeleportAsync(new Vector(0, 0, 100), new QAngle(0, 90, 0), new Vector(0, 0, 0));
```

### TeleportAsync

```csharp
Task TeleportAsync(Vector? pos = null, QAngle? angle = null, Vector? velocity = null)
```

异步将实体传送至指定的位置、朝向和速度。

**参数:**

- `pos` (`Vector?`) = `null` - 实体传送的目标位置，表示为<see cref="Vector"/>。
- `angle` (`QAngle?`) = `null` - 传送后应用于实体的朝向，表示为<see cref="QAngle"/>。
- `velocity` (`Vector?`) = `null` - 实体到达时被赋予的速度，以 <see cref="Vector"/> 表示。

**返回值:** `Task`

**用法示例:**
```csharp
await player.TeleportAsync(new Vector(100, 200, 50), new QAngle(0, 90, 0), new Vector(0, 0, 0));
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

异步切换玩家所属的队伍。

**参数:**

- `team` (`Team`) - 要切换到的队伍。不能为 null。

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
player.ChangeTeam(Team.Terrorist);
```

### ChangeTeamAsync

```csharp
Task ChangeTeamAsync(Team team)
```

异步更改玩家的队伍。此操作同时会杀死该玩家。

**参数:**

- `team` (`Team`) - 待分配的队伍。不能为空。

**返回值:** `Task`

**用法示例:**
```csharp
await player.ChangeTeamAsync(Team.T);
```

### Respawn

```csharp
void Respawn()
```

使玩家重生。

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
player.ExecuteCommand("say Hello");
```

### ExecuteCommandAsync

```csharp
Task ExecuteCommandAsync(string command)
```

异步代表玩家执行命令。

**参数:**

- `command` (`string`) - 要执行的命令。不得为 null 或空。

**返回值:** `Task`

**用法示例:**
```csharp
await player.ExecuteCommandAsync("say Hello");
```

