# 📦 PlayerManagerService

**命名空间:** `SwiftlyS2.Core.Players`

**类型:** `class`

**继承:** `IPlayerManagerService`

## ⚙️ 方法

### RegisterPlayerObject (静态)

```csharp
void RegisterPlayerObject(int playerid)
```

**参数:**

- `playerid` (`int`)

### UnregisterPlayerObject (静态)

```csharp
void UnregisterPlayerObject(int playerid)
```

**参数:**

- `playerid` (`int`)

### ClearAllBlockedTransmitEntities

```csharp
void ClearAllBlockedTransmitEntities()
```

### GetPlayer

```csharp
IPlayer? GetPlayer(int playerid)
```

**参数:**

- `playerid` (`int`)

**返回值:** `IPlayer?`

### GetPlayerFromController

```csharp
IPlayer? GetPlayerFromController(CBasePlayerController controller)
```

**参数:**

- `controller` (`CBasePlayerController`)

**返回值:** `IPlayer?`

### GetPlayerFromPawn

```csharp
IPlayer? GetPlayerFromPawn(CBasePlayerPawn pawn)
```

**参数:**

- `pawn` (`CBasePlayerPawn`)

**返回值:** `IPlayer?`

### IsPlayerOnline

```csharp
bool IsPlayerOnline(int playerid)
```

**参数:**

- `playerid` (`int`)

**返回值:** `bool`

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

### ShouldBlockTransmitEntity

```csharp
void ShouldBlockTransmitEntity(int entityid, bool shouldBlockTransmit)
```

**参数:**

- `entityid` (`int`)
- `shouldBlockTransmit` (`bool`)

### GetAllPlayers

```csharp
IEnumerable<IPlayer> GetAllPlayers()
```

**返回值:** `IEnumerable\<IPlayer\>`

### GetAllValidPlayers

```csharp
IEnumerable<IPlayer> GetAllValidPlayers()
```

**返回值:** `IEnumerable\<IPlayer\>`

### GetBots

```csharp
IEnumerable<IPlayer> GetBots()
```

**返回值:** `IEnumerable\<IPlayer\>`

### GetAlive

```csharp
IEnumerable<IPlayer> GetAlive()
```

**返回值:** `IEnumerable\<IPlayer\>`

### GetCT

```csharp
IEnumerable<IPlayer> GetCT()
```

**返回值:** `IEnumerable\<IPlayer\>`

### GetT

```csharp
IEnumerable<IPlayer> GetT()
```

**返回值:** `IEnumerable\<IPlayer\>`

### GetSpectators

```csharp
IEnumerable<IPlayer> GetSpectators()
```

**返回值:** `IEnumerable\<IPlayer\>`

### GetInTeam

```csharp
IEnumerable<IPlayer> GetInTeam(Team team)
```

**参数:**

- `team` (`Team`)

**返回值:** `IEnumerable\<IPlayer\>`

### GetTAlive

```csharp
IEnumerable<IPlayer> GetTAlive()
```

**返回值:** `IEnumerable\<IPlayer\>`

### GetCTAlive

```csharp
IEnumerable<IPlayer> GetCTAlive()
```

**返回值:** `IEnumerable\<IPlayer\>`

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

### SendMessage

```csharp
void SendMessage(MessageType kind, Func<IPlayer, ILocalizer, string> messageCallback)
```

**参数:**

- `kind` (`MessageType`)
- `messageCallback` (`Func\<IPlayer, ILocalizer, string\>`)

### SendMessage

```csharp
void SendMessage(MessageType kind, Func<IPlayer, ILocalizer, string> messageCallback, int htmlDuration = 5000)
```

**参数:**

- `kind` (`MessageType`)
- `messageCallback` (`Func\<IPlayer, ILocalizer, string\>`)
- `htmlDuration` (`int`) = `5000`

### SendMessageAsync

```csharp
Task SendMessageAsync(MessageType kind, Func<IPlayer, ILocalizer, string> messageCallback)
```

**参数:**

- `kind` (`MessageType`)
- `messageCallback` (`Func\<IPlayer, ILocalizer, string\>`)

**返回值:** `Task`

### SendMessageAsync

```csharp
Task SendMessageAsync(MessageType kind, Func<IPlayer, ILocalizer, string> messageCallback, int htmlDuration = 5000)
```

**参数:**

- `kind` (`MessageType`)
- `messageCallback` (`Func\<IPlayer, ILocalizer, string\>`)
- `htmlDuration` (`int`) = `5000`

**返回值:** `Task`

### GetPlayerFromSteamId

```csharp
IPlayer? GetPlayerFromSteamId(ulong steamId, bool allowUnauthorized = true)
```

**参数:**

- `steamId` (`ulong`)
- `allowUnauthorized` (`bool`) = `true`

**返回值:** `IPlayer?`

### IsSessionIdValid

```csharp
bool IsSessionIdValid(ulong sessionId)
```

**参数:**

- `sessionId` (`ulong`)

**返回值:** `bool`

### GetPlayerFromSessionId

```csharp
IPlayer? GetPlayerFromSessionId(ulong sessionId)
```

**参数:**

- `sessionId` (`ulong`)

**返回值:** `IPlayer?`

