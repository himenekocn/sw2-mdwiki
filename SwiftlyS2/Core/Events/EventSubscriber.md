# 📦 EventSubscriber

Plugin-scoped custom event subscriber.

**命名空间:** `SwiftlyS2.Core.Events`

**类型:** `class`

**继承:** `IEventSubscriber`

**实现接口:** `IDisposable`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `Disposed` | `bool` | - | - |

## ⚙️ 方法

### Dispose

```csharp
void Dispose()
```

### InvokeOnTick

```csharp
void InvokeOnTick()
```

### InvokeOnWorldUpdate

```csharp
void InvokeOnWorldUpdate()
```

### InvokeOnClientConnected

```csharp
void InvokeOnClientConnected(OnClientConnectedEvent @event)
```

**参数:**

- `@event` (`OnClientConnectedEvent`)

### InvokeOnClientDisconnected

```csharp
void InvokeOnClientDisconnected(OnClientDisconnectedEvent @event)
```

**参数:**

- `@event` (`OnClientDisconnectedEvent`)

### InvokeOnClientKeyStateChanged

```csharp
void InvokeOnClientKeyStateChanged(OnClientKeyStateChangedEvent @event)
```

**参数:**

- `@event` (`OnClientKeyStateChangedEvent`)

### InvokeOnClientPutInServer

```csharp
void InvokeOnClientPutInServer(OnClientPutInServerEvent @event)
```

**参数:**

- `@event` (`OnClientPutInServerEvent`)

### InvokeOnClientSteamAuthorize

```csharp
void InvokeOnClientSteamAuthorize(OnClientSteamAuthorizeEvent @event)
```

**参数:**

- `@event` (`OnClientSteamAuthorizeEvent`)

### InvokeOnClientSteamAuthorizeFail

```csharp
void InvokeOnClientSteamAuthorizeFail(OnClientSteamAuthorizeFailEvent @event)
```

**参数:**

- `@event` (`OnClientSteamAuthorizeFailEvent`)

### InvokeOnEntityCreated

```csharp
void InvokeOnEntityCreated(OnEntityCreatedEvent @event)
```

**参数:**

- `@event` (`OnEntityCreatedEvent`)

### InvokeOnClientVoice

```csharp
void InvokeOnClientVoice(OnClientVoiceEvent @event)
```

**参数:**

- `@event` (`OnClientVoiceEvent`)

### InvokeOnEntityDeleted

```csharp
void InvokeOnEntityDeleted(OnEntityDeletedEvent @event)
```

**参数:**

- `@event` (`OnEntityDeletedEvent`)

### InvokeOnEntityParentChanged

```csharp
void InvokeOnEntityParentChanged(OnEntityParentChangedEvent @event)
```

**参数:**

- `@event` (`OnEntityParentChangedEvent`)

### InvokeOnEntitySpawned

```csharp
void InvokeOnEntitySpawned(OnEntitySpawnedEvent @event)
```

**参数:**

- `@event` (`OnEntitySpawnedEvent`)

### InvokeOnMapLoad

```csharp
void InvokeOnMapLoad(OnMapLoadEvent @event)
```

**参数:**

- `@event` (`OnMapLoadEvent`)

### InvokeOnMapUnload

```csharp
void InvokeOnMapUnload(OnMapUnloadEvent @event)
```

**参数:**

- `@event` (`OnMapUnloadEvent`)

### InvokeOnClientProcessUsercmds

```csharp
void InvokeOnClientProcessUsercmds(OnClientProcessUsercmdsEvent @event)
```

**参数:**

- `@event` (`OnClientProcessUsercmdsEvent`)

### InvokeOnEntityTakeDamage

```csharp
void InvokeOnEntityTakeDamage(OnEntityTakeDamageEvent @event)
```

**参数:**

- `@event` (`OnEntityTakeDamageEvent`)

### InvokeOnPrecacheResource

```csharp
void InvokeOnPrecacheResource(OnPrecacheResourceEvent @event)
```

**参数:**

- `@event` (`OnPrecacheResourceEvent`)

### InvokeOnEntityStartTouch

```csharp
void InvokeOnEntityStartTouch(OnEntityStartTouchEvent @event)
```

**参数:**

- `@event` (`OnEntityStartTouchEvent`)

### InvokeOnEntityTouch

```csharp
void InvokeOnEntityTouch(OnEntityTouchEvent @event)
```

**参数:**

- `@event` (`OnEntityTouchEvent`)

### InvokeOnEntityEndTouch

```csharp
void InvokeOnEntityEndTouch(OnEntityEndTouchEvent @event)
```

**参数:**

- `@event` (`OnEntityEndTouchEvent`)

### InvokeOnSteamAPIActivatedHook

```csharp
void InvokeOnSteamAPIActivatedHook()
```

### InvokeOnItemServicesCanAcquireHook

```csharp
void InvokeOnItemServicesCanAcquireHook(OnItemServicesCanAcquireHookEvent @event)
```

**参数:**

- `@event` (`OnItemServicesCanAcquireHookEvent`)

### InvokeOnWeaponServicesCanUseHook

```csharp
void InvokeOnWeaponServicesCanUseHook(OnWeaponServicesCanUseHookEvent @event)
```

**参数:**

- `@event` (`OnWeaponServicesCanUseHookEvent`)

### InvokeOnConsoleOutput

```csharp
void InvokeOnConsoleOutput(OnConsoleOutputEvent @event)
```

**参数:**

- `@event` (`OnConsoleOutputEvent`)

### InvokeOnConVarValueChanged

```csharp
void InvokeOnConVarValueChanged(OnConVarValueChanged @event)
```

**参数:**

- `@event` (`OnConVarValueChanged`)

### InvokeOnConCommandCreated

```csharp
void InvokeOnConCommandCreated(OnConCommandCreated @event)
```

**参数:**

- `@event` (`OnConCommandCreated`)

### InvokeOnConVarCreated

```csharp
void InvokeOnConVarCreated(OnConVarCreated @event)
```

**参数:**

- `@event` (`OnConVarCreated`)

### InvokeOnCommandExecuteHook

```csharp
void InvokeOnCommandExecuteHook(OnCommandExecuteHookEvent @event)
```

**参数:**

- `@event` (`OnCommandExecuteHookEvent`)

### InvokeOnMovementServicesRunCommandHook

```csharp
void InvokeOnMovementServicesRunCommandHook(OnMovementServicesRunCommandHookEvent @event)
```

**参数:**

- `@event` (`OnMovementServicesRunCommandHookEvent`)

### InvokeOnPlayerPawnPostThinkHook

```csharp
void InvokeOnPlayerPawnPostThinkHook(OnPlayerPawnPostThinkHookEvent @event)
```

**参数:**

- `@event` (`OnPlayerPawnPostThinkHookEvent`)

### InvokeOnEntityIdentityAcceptInputHook

```csharp
void InvokeOnEntityIdentityAcceptInputHook(OnEntityIdentityAcceptInputHookEvent @event)
```

**参数:**

- `@event` (`OnEntityIdentityAcceptInputHookEvent`)

### InvokeOnWeaponServicesDropWeaponHook

```csharp
void InvokeOnWeaponServicesDropWeaponHook(OnWeaponServicesDropWeaponHook @event)
```

**参数:**

- `@event` (`OnWeaponServicesDropWeaponHook`)

### InvokeOnEntityFireOutputHook

```csharp
void InvokeOnEntityFireOutputHook(OnEntityFireOutputHookEvent @event)
```

**参数:**

- `@event` (`OnEntityFireOutputHookEvent`)

### InvokeOnStartupServer

```csharp
void InvokeOnStartupServer()
```

