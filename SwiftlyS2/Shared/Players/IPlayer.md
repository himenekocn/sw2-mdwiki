<a id="iplayer"></a>

# 🔌 IPlayer

**命名空间:** `SwiftlyS2.Shared.Players`

**类型:** `interface`

**继承:** `IEquatable\<IPlayer\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlayerID` | `int` | get | 获取玩家的唯一标识符。 |
| `SessionId` | `ulong` | get | 获取玩家的会话ID。 |
| `UserID` | `int` | get | 获取该玩家的用户ID。 |
| `Slot` | `int` | get | 获取玩家的槽位。等于玩家ID。 |
| `Name` | `string` | get, set | 获取玩家名称。 |
| `ServerSideClient` | `IServerSideClient` | get | 获取与玩家关联的服务端客户端。 |
| `IsFakeClient` | `bool` | get | 客户端是否为机器人。 |
| `IsAuthorized` | `bool` | get | 当前用户是否已通过Steam授权。 |
| `ConnectedTime` | `uint` | get | 获取连接处于活动状态的总时间（以秒为单位）。 |
| `SteamID` | `ulong` | get | 获取与该用户关联的唯一Steam标识符。 |
| `UnauthorizedSteamID` | `ulong` | get | 获取尚未验证的Steam ID。 |
| `IsAlive` | `bool` | get | 获取一个值，该值指示玩家当前是否存活。 |
| `Controller` | `CCSPlayerController` | get | 获取与玩家关联的玩家控制器。 |
| `RequiredController` | `CCSPlayerController` | get | 获取与玩家关联的玩家控制器。要求控制器有效。<exception cref="InvalidOperationException">当控制器无效时抛出。</exception> |
| `Pawn` | `CBasePlayerPawn?` | get | 获取与该玩家关联的棋子。 |
| `RequiredPawn` | `CBasePlayerPawn` | get | 获取与该玩家关联的棋子。要求棋子有效。 <exception cref="InvalidOperationException">当棋子无效时抛出。</exception> |
| `PlayerPawn` | `CCSPlayerPawn?` | get | 获取与玩家关联的玩家棋子。 |
| `RequiredPlayerPawn` | `CCSPlayerPawn` | get | 获取与该玩家关联的玩家Pawn。要求玩家Pawn必须有效。<exception cref="InvalidOperationException">当玩家Pawn无效时抛出。</exception> |
| `PressedButtons` | `GameButtonFlags` | get | 获取当前按下的游戏按键集合。 |
| `IPAddress` | `string` | get | 获取与该玩家关联的IP地址。 |
| `VoiceFlags` | `VoiceFlagValue` | get, set | 获取或设置指定语音选项或功能的标志集。 |
| `PlayerLanguage` | `Language` | get | 获取玩家的语言。 |
| `IsFirstSpawn` | `bool` | get | 指示这是否为玩家的首次出生。 |
| `IsValid` | `bool` | get | 检查玩家是否有效（拥有控制器、不是HLTV、已连接并有Pawn）。 |

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
player.SendMessage(MessageType.Chat, "Hello World");
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
player.SendMessage(MessageType.Value, "Hello World", 5);
```

### SendMessageAsync

```csharp
Task SendMessageAsync(MessageType kind, string message)
```

异步向玩家发送指定类型的消息。

**参数:**

- `kind` (`MessageType`) - 要发送的消息类型。决定消息的处理或显示方式。
- `message` (`string`) - 要发送的消息内容。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await player.SendMessageAsync(MessageType.Chat, "Hello World");
```

### SendMessageAsync

```csharp
Task SendMessageAsync(MessageType kind, string message, int htmlDuration = 5000)
```

以自定义 HTML 持续时间异步向玩家发送指定类型的消息。

**参数:**

- `kind` (`MessageType`) - 要发送的消息类型。决定消息的处理或显示方式。
- `message` (`string`) - 要发送的消息内容。不能为 null。
- `htmlDuration` (`int`) = `5000` - 该消息应以HTML格式显示的持续时间，单位毫秒。

**返回值:** `Task`

**用法示例:**
```csharp
await player.SendMessageAsync(MessageType.Value, "Hello World", 5000);
```

### SendNotify

```csharp
void SendNotify(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
player.SendNotify("Hello, World!");
```

### SendNotifyAsync

```csharp
Task SendNotifyAsync(string message)
```

向玩家异步发送通知消息。

**参数:**

- `message` (`string`) - 要发送的消息内容。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await player.SendNotifyAsync("Welcome to the game!");
```

### SendConsole

```csharp
void SendConsole(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
player.SendConsole("say Hello World");
```

### SendConsoleAsync

```csharp
Task SendConsoleAsync(string message)
```

向玩家异步发送控制台消息。

**参数:**

- `message` (`string`) - 要发送的消息内容。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await player.SendConsoleAsync("Hello World");
```

### SendChat

```csharp
void SendChat(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
player.SendChat("Hello World");
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
await player.SendChatAsync("Hello World");
```

### SendCenter

```csharp
void SendCenter(string message)
```

**参数:**

- `message` (`string`)

**用法示例:**
```csharp
player.SendCenter("Hello World");
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
player.SendAlert("Warning: Restricted area!");
```

### SendAlertAsync

```csharp
Task SendAlertAsync(string message)
```

向玩家异步发送警报消息。

**参数:**

- `message` (`string`) - 要发送的消息内容。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await player.SendAlertAsync("警告：检测到异常行为");
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
player.SendCenterHTML("<font color='red'>Hello World</font>", 5);
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
player.SendChatEOT("Hello World");
```

### SendChatEOTAsync

```csharp
Task SendChatEOTAsync(string message)
```

异步向玩家发送一条文本结束的聊天消息。

**参数:**

- `message` (`string`) - 要发送的消息内容。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await player.SendChatEOTAsync("Hello World");
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
player.Kick("违规操作", ENetworkDisconnectionReason.KICKED_BY_SERVER);
```

### KickAsync

```csharp
Task KickAsync(string reason, ENetworkDisconnectionReason gameReason)
```

以指定的原因和断开连接类型，将用户从网络会话中断开，异步执行。

**参数:**

- `reason` (`string`) - 描述断开连接原因的消息。此消息可能会显示给用户。不能为 null 或为空。
- `gameReason` (`ENetworkDisconnectionReason`) - 指示要执行的网络断开连接类型的断开原因代码。

**返回值:** `Task`

**用法示例:**
```csharp
await player.KickAsync("违规操作", ENetworkDisconnectionReason.Banned);
```

### ShouldBlockTransmitEntity

```csharp
void ShouldBlockTransmitEntity(int entityid, bool shouldBlockTransmit)
```

设置是否应阻止指定实体的传输。

**参数:**

- `entityid` (`int`) - 要更新传输状态的实体的唯一标识符。
- `shouldBlockTransmit` (`bool`) - 一个指示是否应阻止该实体传输的值。指定 <see langword="true"/> 以阻止传输；否则指定 <see langword="false"/>。

**用法示例:**
```csharp
player.ShouldBlockTransmitEntity(1024, true);
```

### IsTransmitEntityBlocked

```csharp
bool IsTransmitEntityBlocked(int entityid)
```

确定指定实体当前是否被阻止传输数据。

**参数:**

- `entityid` (`int`) - 要检查传输阻塞的实体的唯一标识符。必须是有效的实体ID。

**返回值:** `bool` - 如果该实体被阻止传输则为 true；否则为 false。

**用法示例:**
```csharp
bool isBlocked = player.IsTransmitEntityBlocked(123);
```

### ClearTransmitEntityBlocks

```csharp
void ClearTransmitEntityBlocks()
```

从传输缓冲区中移除所有实体块，丢弃所有计划传输的待处理数据。

**用法示例:**
```csharp
player.ClearTransmitEntityBlocks();
```

### SetListenOverride

```csharp
void SetListenOverride(int player, ListenOverride listenOverride)
```

为指定的玩家设置自定义监听覆盖。

**参数:**

- `player` (`int`) - 将要更新其“监听覆盖”设置的玩家标识符。必须是一个有效的玩家索引。
- `listenOverride` (`ListenOverride`) - 要应用于指定玩家的监听覆盖值。

**用法示例:**
```csharp
player.SetListenOverride(targetPlayer, ListenOverride.Yes);
```

### GetListenOverride

```csharp
ListenOverride GetListenOverride(int player)
```

获取指定玩家的监听覆盖设置。

**参数:**

- `player` (`int`) - 要检索其监听覆盖设置的玩家标识符，必须为有效的玩家索引。

**返回值:** `ListenOverride` - 包含指定玩家监听覆盖设置的监听覆盖对象。

**用法示例:**
```csharp
var overrideSetting = player.GetListenOverride(player.Index);
```

### GetClientConvarValue

```csharp
string GetClientConvarValue(string convarName)
```

检索用户信息值，用于诸如 m_yaw、sensitivity 等控制台变量。

**参数:**

- `convarName` (`string`)

**返回值:** `string`

**用法示例:**
```csharp
string yaw = player.GetClientConvarValue("m_yaw");
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

根据指定的伤害信息异步对实体施加伤害。

**参数:**

- `damageInfo` (`CTakeDamageInfo`) - 一个包含所受伤害详细信息的对象，包括伤害值、类型和来源。不能为null。

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
player.TakeDamage(50.0f, DamageTypes_t.DMG_BULLET, null, attacker, null);
```

### TakeDamageAsync

```csharp
Task TakeDamageAsync(float damage, DamageTypes_t damageType, CBaseEntity? inflictor = null, CBaseEntity? attacker = null, CBaseEntity? ability = null)
```

根据指定的伤害信息异步对实体施加伤害。

**参数:**

- `damage` (`float`) - 要应用的伤害数值。
- `damageType` (`DamageTypes_t`) - 要应用伤害的类型。
- `inflictor` (`CBaseEntity?`) = `null` - 造成伤害的实体。可以为 null。
- `attacker` (`CBaseEntity?`) = `null` - 正在攻击的实体。可为空。
- `ability` (`CBaseEntity?`) = `null` - 造成伤害的能力。可以为空。

**返回值:** `Task`

**用法示例:**
```csharp
await player.TakeDamageAsync(25.0f, DamageTypes_t.DMG_BULLET, null, attackerEntity, null);
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
player.Teleport(new Vector(0, 0, 0), new QAngle(0, 0, 0), new Vector(0, 0, 0));
```

### TeleportAsync

```csharp
Task TeleportAsync(Vector pos, QAngle angle, Vector velocity)
```

异步将实体传送至指定位置、朝向和速度。

**参数:**

- `pos` (`Vector`) - 将实体传送至的目标位置，表示为 <see cref="Vector"/>。
- `angle` (`QAngle`) - 传送后应用于实体的朝向，以 <see cref="QAngle"/> 表示。
- `velocity` (`Vector`) - 抵达时分配给实体的速度，表示为<see cref="Vector"/>。

**返回值:** `Task`

**用法示例:**
```csharp
await player.TeleportAsync(new Vector(0, 0, 0), QAngle.Zero, Vector.Zero);
```

### TeleportAsync

```csharp
Task TeleportAsync(Vector? pos = null, QAngle? angle = null, Vector? velocity = null)
```

异步将实体传送至指定位置、朝向和速度。

**参数:**

- `pos` (`Vector?`) = `null` - 将实体传送至的目标位置，表示为 <see cref="Vector"/>。
- `angle` (`QAngle?`) = `null` - 传送后应用于实体的朝向，以 <see cref="QAngle"/> 表示。
- `velocity` (`Vector?`) = `null` - 抵达时分配给实体的速度，表示为<see cref="Vector"/>。

**返回值:** `Task`

**用法示例:**
```csharp
await player.TeleportAsync(new Vector(0, 0, 0), new QAngle(0, 90, 0), Vector.Zero);
```

### SwitchTeam

```csharp
void SwitchTeam(Team team)
```

**参数:**

- `team` (`Team`)

**用法示例:**
```csharp
player.SwitchTeam(Team.CounterTerrorist);
```

### SwitchTeamAsync

```csharp
Task SwitchTeamAsync(Team team)
```

异步切换玩家所属队伍。

**参数:**

- `team` (`Team`) - 要切换到的队伍。不能为 null。

**返回值:** `Task`

**用法示例:**
```csharp
await player.SwitchTeamAsync(Team.CounterTerrorist);
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

异步更改玩家所在队伍。此操作也会击杀该玩家。

**参数:**

- `team` (`Team`) - 要分配的队伍。不能为空。

**返回值:** `Task`

**用法示例:**
```csharp
await player.ChangeTeamAsync(Team.T);
```

### Respawn

```csharp
void Respawn()
```

重新生成玩家。

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
player.ExecuteCommand("say Hello World");
```

### ExecuteCommandAsync

```csharp
Task ExecuteCommandAsync(string command)
```

异步代表玩家执行一条命令。

**参数:**

- `command` (`string`) - 要执行的命令。不能为空或空字符串。

**返回值:** `Task`

**用法示例:**
```csharp
await player.ExecuteCommandAsync("say Hello");
```

