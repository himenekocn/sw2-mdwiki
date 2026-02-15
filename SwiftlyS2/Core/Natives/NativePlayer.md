# 📦 NativePlayer

**命名空间:** `SwiftlyS2.Core.Natives`

**类型:** `class`

## ⚙️ 方法

### SendMessage (静态)

```csharp
void SendMessage(int playerid, int kind, string message, int htmlDuration)
```

**参数:**

- `playerid` (`int`)
- `kind` (`int`)
- `message` (`string`)
- `htmlDuration` (`int`)

### IsFakeClient (静态)

```csharp
bool IsFakeClient(int playerid)
```

**参数:**

- `playerid` (`int`)

**返回值:** `bool`

### IsAuthorized (静态)

```csharp
bool IsAuthorized(int playerid)
```

**参数:**

- `playerid` (`int`)

**返回值:** `bool`

### GetConnectedTime (静态)

```csharp
uint GetConnectedTime(int playerid)
```

**参数:**

- `playerid` (`int`)

**返回值:** `uint`

### GetUnauthorizedSteamID (静态)

```csharp
ulong GetUnauthorizedSteamID(int playerid)
```

**参数:**

- `playerid` (`int`)

**返回值:** `ulong`

### GetSteamID (静态)

```csharp
ulong GetSteamID(int playerid)
```

**参数:**

- `playerid` (`int`)

**返回值:** `ulong`

### GetController (静态)

```csharp
nint GetController(int playerid)
```

**参数:**

- `playerid` (`int`)

**返回值:** `nint`

### GetPawn (静态)

```csharp
nint GetPawn(int playerid)
```

**参数:**

- `playerid` (`int`)

**返回值:** `nint`

### GetPlayerPawn (静态)

```csharp
nint GetPlayerPawn(int playerid)
```

**参数:**

- `playerid` (`int`)

**返回值:** `nint`

### GetPressedButtons (静态)

```csharp
ulong GetPressedButtons(int playerid)
```

**参数:**

- `playerid` (`int`)

**返回值:** `ulong`

### PerformCommand (静态)

```csharp
void PerformCommand(int playerid, string command)
```

**参数:**

- `playerid` (`int`)
- `command` (`string`)

### GetIPAddress (静态)

```csharp
string GetIPAddress(int playerid)
```

**参数:**

- `playerid` (`int`)

**返回值:** `string`

### Kick (静态)

```csharp
void Kick(int playerid, string reason, int gamereason)
```

**参数:**

- `playerid` (`int`)
- `reason` (`string`)
- `gamereason` (`int`)

### ShouldBlockTransmitEntity (静态)

```csharp
void ShouldBlockTransmitEntity(int playerid, int entityidx, bool shouldBlockTransmit)
```

**参数:**

- `playerid` (`int`)
- `entityidx` (`int`)
- `shouldBlockTransmit` (`bool`)

### IsTransmitEntityBlocked (静态)

```csharp
bool IsTransmitEntityBlocked(int playerid, int entityidx)
```

**参数:**

- `playerid` (`int`)
- `entityidx` (`int`)

**返回值:** `bool`

### ClearTransmitEntityBlocked (静态)

```csharp
void ClearTransmitEntityBlocked(int playerid)
```

**参数:**

- `playerid` (`int`)

### ChangeTeam (静态)

```csharp
void ChangeTeam(int playerid, int newteam)
```

**参数:**

- `playerid` (`int`)
- `newteam` (`int`)

### SwitchTeam (静态)

```csharp
void SwitchTeam(int playerid, int newteam)
```

**参数:**

- `playerid` (`int`)
- `newteam` (`int`)

### TakeDamage (静态)

```csharp
void TakeDamage(int playerid, nint dmginfo)
```

**参数:**

- `playerid` (`int`)
- `dmginfo` (`nint`)

### Teleport (静态)

```csharp
void Teleport(int playerid, Vector pos, QAngle angle, Vector velocity)
```

**参数:**

- `playerid` (`int`)
- `pos` (`Vector`)
- `angle` (`QAngle`)
- `velocity` (`Vector`)

### GetLanguage (静态)

```csharp
string GetLanguage(int playerid)
```

**参数:**

- `playerid` (`int`)

**返回值:** `string`

### SetCenterMenuRender (静态)

```csharp
void SetCenterMenuRender(int playerid, string text)
```

**参数:**

- `playerid` (`int`)
- `text` (`string`)

### ClearCenterMenuRender (静态)

```csharp
void ClearCenterMenuRender(int playerid)
```

**参数:**

- `playerid` (`int`)

### HasMenuShown (静态)

```csharp
bool HasMenuShown(int playerid)
```

**参数:**

- `playerid` (`int`)

**返回值:** `bool`

### ExecuteCommand (静态)

```csharp
void ExecuteCommand(int playerid, string command)
```

**参数:**

- `playerid` (`int`)
- `command` (`string`)

### IsFirstSpawn (静态)

```csharp
bool IsFirstSpawn(int playerid)
```

**参数:**

- `playerid` (`int`)

**返回值:** `bool`

### GetUserID (静态)

```csharp
int GetUserID(int playerid)
```

**参数:**

- `playerid` (`int`)

**返回值:** `int`

### GetSessionID (静态)

```csharp
ulong GetSessionID(int playerid)
```

**参数:**

- `playerid` (`int`)

**返回值:** `ulong`

### GetName (静态)

```csharp
string GetName(int playerid)
```

**参数:**

- `playerid` (`int`)

**返回值:** `string`

