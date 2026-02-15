# 📦 Player

**命名空间:** `SwiftlyS2.Core.Players`

**类型:** `class`

**继承:** `IPlayer`

**实现接口:** `IDisposable`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `PlayerID` | `int` | - | - |
| `Pawn` | `CBasePlayerPawn?` | - | - |
| `PlayerPawn` | `CCSPlayerPawn?` | - | - |

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `SessionId` | `ulong` | get | - |
| `Slot` | `int` | get | - |
| `UserID` | `int` | get | - |
| `Name` | `string` | get | - |
| `IsFakeClient` | `bool` | get | - |
| `IsAuthorized` | `bool` | get | - |
| `ConnectedTime` | `uint` | get | - |
| `PlayerLanguage` | `Language` | get | - |
| `SteamID` | `ulong` | get | - |
| `UnauthorizedSteamID` | `ulong` | get | - |
| `Controller` | `CCSPlayerController` | get | - |
| `PressedButtons` | `GameButtonFlags` | get | - |
| `IPAddress` | `string` | get | - |
| `VoiceFlags` | `VoiceFlagValue` | get, set | - |
| `IsFirstSpawn` | `bool` | get | - |

## ⚙️ 方法

### ChangeTeam

```csharp
void ChangeTeam(Team team)
```

**参数:**

- `team` (`Team`)

### ChangeTeamAsync

```csharp
Task ChangeTeamAsync(Team team)
```

**参数:**

- `team` (`Team`)

**返回值:** `Task`

### ClearTransmitEntityBlocks

```csharp
void ClearTransmitEntityBlocks()
```

### GetListenOverride

```csharp
ListenOverride GetListenOverride(int player)
```

**参数:**

- `player` (`int`)

**返回值:** `ListenOverride`

### IsTransmitEntityBlocked

```csharp
bool IsTransmitEntityBlocked(int entityid)
```

**参数:**

- `entityid` (`int`)

**返回值:** `bool`

### Kick

```csharp
void Kick(string reason, ENetworkDisconnectionReason gameReason)
```

**参数:**

- `reason` (`string`)
- `gameReason` (`ENetworkDisconnectionReason`)

### KickAsync

```csharp
Task KickAsync(string reason, ENetworkDisconnectionReason gameReason)
```

**参数:**

- `reason` (`string`)
- `gameReason` (`ENetworkDisconnectionReason`)

**返回值:** `Task`

### SendMessage

```csharp
void SendMessage(MessageType kind, string message)
```

**参数:**

- `kind` (`MessageType`)
- `message` (`string`)

### SendMessageAsync

```csharp
Task SendMessageAsync(MessageType kind, string message)
```

**参数:**

- `kind` (`MessageType`)
- `message` (`string`)

**返回值:** `Task`

### SetListenOverride

```csharp
void SetListenOverride(int player, ListenOverride listenOverride)
```

**参数:**

- `player` (`int`)
- `listenOverride` (`ListenOverride`)

### ShouldBlockTransmitEntity

```csharp
void ShouldBlockTransmitEntity(int entityid, bool shouldBlockTransmit)
```

**参数:**

- `entityid` (`int`)
- `shouldBlockTransmit` (`bool`)

### SwitchTeam

```csharp
void SwitchTeam(Team team)
```

**参数:**

- `team` (`Team`)

### SwitchTeamAsync

```csharp
Task SwitchTeamAsync(Team team)
```

**参数:**

- `team` (`Team`)

**返回值:** `Task`

### TakeDamage

```csharp
void TakeDamage(CTakeDamageInfo damageInfo)
```

**参数:**

- `damageInfo` (`CTakeDamageInfo`)

### TakeDamageAsync

```csharp
Task TakeDamageAsync(CTakeDamageInfo damageInfo)
```

**参数:**

- `damageInfo` (`CTakeDamageInfo`)

**返回值:** `Task`

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

### TakeDamageAsync

```csharp
Task TakeDamageAsync(float damage, DamageTypes_t damageType, CBaseEntity? inflictor = null, CBaseEntity? attacker = null, CBaseEntity? ability = null)
```

**参数:**

- `damage` (`float`)
- `damageType` (`DamageTypes_t`)
- `inflictor` (`CBaseEntity?`) = `null`
- `attacker` (`CBaseEntity?`) = `null`
- `ability` (`CBaseEntity?`) = `null`

**返回值:** `Task`

### Teleport

```csharp
void Teleport(Vector pos, QAngle angle, Vector velocity)
```

**参数:**

- `pos` (`Vector`)
- `angle` (`QAngle`)
- `velocity` (`Vector`)

### Teleport

```csharp
void Teleport(Vector? pos = null, QAngle? angle = null, Vector? velocity = null)
```

**参数:**

- `pos` (`Vector?`) = `null`
- `angle` (`QAngle?`) = `null`
- `velocity` (`Vector?`) = `null`

### TeleportAsync

```csharp
Task TeleportAsync(Vector pos, QAngle angle, Vector velocity)
```

**参数:**

- `pos` (`Vector`)
- `angle` (`QAngle`)
- `velocity` (`Vector`)

**返回值:** `Task`

### TeleportAsync

```csharp
Task TeleportAsync(Vector? pos = null, QAngle? angle = null, Vector? velocity = null)
```

**参数:**

- `pos` (`Vector?`) = `null`
- `angle` (`QAngle?`) = `null`
- `velocity` (`Vector?`) = `null`

**返回值:** `Task`

### Respawn

```csharp
void Respawn()
```

### ExecuteCommand

```csharp
void ExecuteCommand(string command)
```

**参数:**

- `command` (`string`)

### ExecuteCommandAsync

```csharp
Task ExecuteCommandAsync(string command)
```

**参数:**

- `command` (`string`)

**返回值:** `Task`

### Equals

```csharp
bool Equals(IPlayer? other)
```

**参数:**

- `other` (`IPlayer?`)

**返回值:** `bool`

### Equals

```csharp
bool Equals(object? obj)
```

**参数:**

- `obj` (`object?`)

**返回值:** `bool`

### GetHashCode

```csharp
int GetHashCode()
```

**返回值:** `int`

### SendMessage

```csharp
void SendMessage(MessageType kind, string message, int htmlDuration = 5000)
```

**参数:**

- `kind` (`MessageType`)
- `message` (`string`)
- `htmlDuration` (`int`) = `5000`

### SendMessageAsync

```csharp
Task SendMessageAsync(MessageType kind, string message, int htmlDuration = 5000)
```

**参数:**

- `kind` (`MessageType`)
- `message` (`string`)
- `htmlDuration` (`int`) = `5000`

**返回值:** `Task`

### SendNotify

```csharp
void SendNotify(string message)
```

**参数:**

- `message` (`string`)

### SendNotifyAsync

```csharp
Task SendNotifyAsync(string message)
```

**参数:**

- `message` (`string`)

**返回值:** `Task`

### SendConsole

```csharp
void SendConsole(string message)
```

**参数:**

- `message` (`string`)

### SendConsoleAsync

```csharp
Task SendConsoleAsync(string message)
```

**参数:**

- `message` (`string`)

**返回值:** `Task`

### SendChat

```csharp
void SendChat(string message)
```

**参数:**

- `message` (`string`)

### SendChatAsync

```csharp
Task SendChatAsync(string message)
```

**参数:**

- `message` (`string`)

**返回值:** `Task`

### SendCenter

```csharp
void SendCenter(string message)
```

**参数:**

- `message` (`string`)

### SendCenterAsync

```csharp
Task SendCenterAsync(string message)
```

**参数:**

- `message` (`string`)

**返回值:** `Task`

### SendAlert

```csharp
void SendAlert(string message)
```

**参数:**

- `message` (`string`)

### SendAlertAsync

```csharp
Task SendAlertAsync(string message)
```

**参数:**

- `message` (`string`)

**返回值:** `Task`

### SendCenterHTML

```csharp
void SendCenterHTML(string message, int duration = 5000)
```

**参数:**

- `message` (`string`)
- `duration` (`int`) = `5000`

### SendCenterHTMLAsync

```csharp
Task SendCenterHTMLAsync(string message, int duration = 5000)
```

**参数:**

- `message` (`string`)
- `duration` (`int`) = `5000`

**返回值:** `Task`

### SendChatEOT

```csharp
void SendChatEOT(string message)
```

**参数:**

- `message` (`string`)

### SendChatEOTAsync

```csharp
Task SendChatEOTAsync(string message)
```

**参数:**

- `message` (`string`)

**返回值:** `Task`

### Dispose

```csharp
void Dispose()
```

### ThrowIfDisposed

```csharp
void ThrowIfDisposed()
```

