# 📦 EventPublisher

**命名空间:** `SwiftlyS2.Core.Events`

**类型:** `class`

## ⚙️ 方法

### Subscribe (静态)

```csharp
void Subscribe(EventSubscriber subscriber)
```

**参数:**

- `subscriber` (`EventSubscriber`)

### Unsubscribe (静态)

```csharp
void Unsubscribe(EventSubscriber subscriber)
```

**参数:**

- `subscriber` (`EventSubscriber`)

### Register (静态)

```csharp
void Register()
```

### OnConVarCreated (静态)

```csharp
void OnConVarCreated(nint convarNamePtr)
```

**参数:**

- `convarNamePtr` (`nint`)

### OnConCommandCreated (静态)

```csharp
void OnConCommandCreated(nint commandNamePtr)
```

**参数:**

- `commandNamePtr` (`nint`)

### OnConVarValueChanged (静态)

```csharp
void OnConVarValueChanged(nint convarNamePtr, int playerid, nint newValuePtr, nint oldValuePtr)
```

**参数:**

- `convarNamePtr` (`nint`)
- `playerid` (`int`)
- `newValuePtr` (`nint`)
- `oldValuePtr` (`nint`)

### OnTick (静态)

```csharp
void OnTick(byte simulating, byte first, byte last)
```

**参数:**

- `simulating` (`byte`)
- `first` (`byte`)
- `last` (`byte`)

### OnPreworldUpdate (静态)

```csharp
void OnPreworldUpdate(byte simulating)
```

**参数:**

- `simulating` (`byte`)

### OnClientConnected (静态)

```csharp
byte OnClientConnected(int playerId)
```

**参数:**

- `playerId` (`int`)

**返回值:** `byte`

### OnClientDisconnected (静态)

```csharp
void OnClientDisconnected(int playerId, int reason)
```

**参数:**

- `playerId` (`int`)
- `reason` (`int`)

### OnClientKeyStateChanged (静态)

```csharp
void OnClientKeyStateChanged(int playerId, GameButtons key, byte pressed)
```

**参数:**

- `playerId` (`int`)
- `key` (`GameButtons`)
- `pressed` (`byte`)

### OnClientPutInServer (静态)

```csharp
void OnClientPutInServer(int playerId, int clientKind)
```

**参数:**

- `playerId` (`int`)
- `clientKind` (`int`)

### OnClientSteamAuthorize (静态)

```csharp
void OnClientSteamAuthorize(int playerId)
```

**参数:**

- `playerId` (`int`)

### OnClientSteamAuthorizeFail (静态)

```csharp
void OnClientSteamAuthorizeFail(int playerId)
```

**参数:**

- `playerId` (`int`)

### OnEntityCreated (静态)

```csharp
void OnEntityCreated(nint entityPtr)
```

**参数:**

- `entityPtr` (`nint`)

### OnEntityDeleted (静态)

```csharp
void OnEntityDeleted(nint entityPtr)
```

**参数:**

- `entityPtr` (`nint`)

### OnEntityParentChanged (静态)

```csharp
void OnEntityParentChanged(nint entityPtr, nint newParentPtr)
```

**参数:**

- `entityPtr` (`nint`)
- `newParentPtr` (`nint`)

### OnEntitySpawned (静态)

```csharp
void OnEntitySpawned(nint entityPtr)
```

**参数:**

- `entityPtr` (`nint`)

### OnMapLoad (静态)

```csharp
void OnMapLoad(nint mapNamePtr)
```

**参数:**

- `mapNamePtr` (`nint`)

### OnClientVoice (静态)

```csharp
void OnClientVoice(int playerId)
```

**参数:**

- `playerId` (`int`)

### OnMapUnload (静态)

```csharp
void OnMapUnload(nint mapNamePtr)
```

**参数:**

- `mapNamePtr` (`nint`)

### OnClientProcessUsercmds (静态)

```csharp
void OnClientProcessUsercmds(int playerId, nint usercmdsPtr, int numcmds, byte paused, float margin)
```

**参数:**

- `playerId` (`int`)
- `usercmdsPtr` (`nint`)
- `numcmds` (`int`)
- `paused` (`byte`)
- `margin` (`float`)

### OnEntityTakeDamage (静态)

```csharp
byte OnEntityTakeDamage(nint entityPtr, nint takeDamageInfoPtr, nint takeDamageResultPtr)
```

**参数:**

- `entityPtr` (`nint`)
- `takeDamageInfoPtr` (`nint`)
- `takeDamageResultPtr` (`nint`)

**返回值:** `byte`

### OnPrecacheResource (静态)

```csharp
void OnPrecacheResource(nint pResourceManifest)
```

**参数:**

- `pResourceManifest` (`nint`)

### OnStartupServer (静态)

```csharp
void OnStartupServer()
```

### InvokeOnEntityStartTouch (静态)

```csharp
void InvokeOnEntityStartTouch(OnEntityStartTouchEvent @event)
```

**参数:**

- `@event` (`OnEntityStartTouchEvent`)

### InvokeOnEntityTouch (静态)

```csharp
void InvokeOnEntityTouch(OnEntityTouchEvent @event)
```

**参数:**

- `@event` (`OnEntityTouchEvent`)

### InvokeOnEntityEndTouch (静态)

```csharp
void InvokeOnEntityEndTouch(OnEntityEndTouchEvent @event)
```

**参数:**

- `@event` (`OnEntityEndTouchEvent`)

### InvokeOnSteamAPIActivatedHook (静态)

```csharp
void InvokeOnSteamAPIActivatedHook()
```

### InvokeOnCanAcquireHook (静态)

```csharp
void InvokeOnCanAcquireHook(OnItemServicesCanAcquireHookEvent @event)
```

**参数:**

- `@event` (`OnItemServicesCanAcquireHookEvent`)

### InvokeOnWeaponServicesCanUseHook (静态)

```csharp
void InvokeOnWeaponServicesCanUseHook(OnWeaponServicesCanUseHookEvent @event)
```

**参数:**

- `@event` (`OnWeaponServicesCanUseHookEvent`)

### OnConsoleOutput (静态)

```csharp
void OnConsoleOutput(nint messagePtr)
```

**参数:**

- `messagePtr` (`nint`)

### InvokeOnCommandExecuteHook (静态)

```csharp
void InvokeOnCommandExecuteHook(OnCommandExecuteHookEvent @event)
```

**参数:**

- `@event` (`OnCommandExecuteHookEvent`)

### InvokeOnMovementServicesRunCommandHook (静态)

```csharp
void InvokeOnMovementServicesRunCommandHook(OnMovementServicesRunCommandHookEvent @event)
```

**参数:**

- `@event` (`OnMovementServicesRunCommandHookEvent`)

### InvokeOnPlayerPawnPostThinkHook (静态)

```csharp
void InvokeOnPlayerPawnPostThinkHook(OnPlayerPawnPostThinkHookEvent @event)
```

**参数:**

- `@event` (`OnPlayerPawnPostThinkHookEvent`)

### InvokeOnEntityIdentityAcceptInputHook (静态)

```csharp
void InvokeOnEntityIdentityAcceptInputHook(OnEntityIdentityAcceptInputHookEvent @event)
```

**参数:**

- `@event` (`OnEntityIdentityAcceptInputHookEvent`)

### InvokeOnWeaponServicesDropWeaponHook (静态)

```csharp
void InvokeOnWeaponServicesDropWeaponHook(OnWeaponServicesDropWeaponHook @event)
```

**参数:**

- `@event` (`OnWeaponServicesDropWeaponHook`)

### InvokeEntityFireOutputHook (静态)

```csharp
void InvokeEntityFireOutputHook(OnEntityFireOutputHookEvent @event)
```

**参数:**

- `@event` (`OnEntityFireOutputHookEvent`)

