<a id="eventdelegates"></a>

# 📦 EventDelegates

事件委托。

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `class`

## ⚙️ 方法

### OnTick

```csharp
void OnTick()
```

在游戏处理完一个 tick 后被调用。如果服务器处于休眠状态，则不会调用此回调。此回调属于热路径，请谨慎使用，切勿执行任何耗时操作。

### OnWorldUpdate

```csharp
void OnWorldUpdate()
```

当世界更新时调用。即使在休眠状态下也会发生此回调。这是一个热点路径，请谨慎使用，切勿执行任何高开销操作。

### OnSteamAPIActivated

```csharp
void OnSteamAPIActivated()
```

当 Steam API 被激活时调用。

### OnClientConnected

```csharp
void OnClientConnected(IOnClientConnectedEvent @event)
```

当客户端连接到服务器时调用。

**参数:**

- `@event` (`IOnClientConnectedEvent`)

### OnClientDisconnected

```csharp
void OnClientDisconnected(IOnClientDisconnectedEvent @event)
```

当客户端与服务器断开连接时调用。

**参数:**

- `@event` (`IOnClientDisconnectedEvent`)

### OnClientKeyStateChanged

```csharp
void OnClientKeyStateChanged(IOnClientKeyStateChangedEvent @event)
```

当客户端的按键状态发生变化时调用。

**参数:**

- `@event` (`IOnClientKeyStateChangedEvent`)

### OnClientPutInServer

```csharp
void OnClientPutInServer(IOnClientPutInServerEvent @event)
```

当客户端完全接入服务器时调用。

**参数:**

- `@event` (`IOnClientPutInServerEvent`)

### OnClientSteamAuthorize

```csharp
void OnClientSteamAuthorize(IOnClientSteamAuthorizeEvent @event)
```

当客户端通过 Steam 授权时调用。

**参数:**

- `@event` (`IOnClientSteamAuthorizeEvent`)

### OnClientSteamAuthorizeFail

```csharp
void OnClientSteamAuthorizeFail(IOnClientSteamAuthorizeFailEvent @event)
```

当客户端的 Steam 授权失败时调用。

**参数:**

- `@event` (`IOnClientSteamAuthorizeFailEvent`)

### OnEntityCreated

```csharp
void OnEntityCreated(IOnEntityCreatedEvent @event)
```

在实体创建时调用。

**参数:**

- `@event` (`IOnEntityCreatedEvent`)

### OnEntityDeleted

```csharp
void OnEntityDeleted(IOnEntityDeletedEvent @event)
```

当实体被删除时调用。

**参数:**

- `@event` (`IOnEntityDeletedEvent`)

### OnEntityParentChanged

```csharp
void OnEntityParentChanged(IOnEntityParentChangedEvent @event)
```

当事件实体的父级发生变更时调用。

**参数:**

- `@event` (`IOnEntityParentChangedEvent`)

### OnEntitySpawned

```csharp
void OnEntitySpawned(IOnEntitySpawnedEvent @event)
```

当实体被生成时调用。

**参数:**

- `@event` (`IOnEntitySpawnedEvent`)

### OnMapLoad

```csharp
void OnMapLoad(IOnMapLoadEvent @event)
```

当地图加载时调用。

**参数:**

- `@event` (`IOnMapLoadEvent`)

### OnMapUnload

```csharp
void OnMapUnload(IOnMapUnloadEvent @event)
```

当地图卸载时被调用。

**参数:**

- `@event` (`IOnMapUnloadEvent`)

### OnClientProcessUsercmds

```csharp
void OnClientProcessUsercmds(IOnClientProcessUsercmdsEvent @event)
```

当客户端处理用户命令时调用。此回调为热点路径，请谨慎使用，避免执行任何高开销操作。

**参数:**

- `@event` (`IOnClientProcessUsercmdsEvent`)

### OnConVarValueChanged

```csharp
void OnConVarValueChanged(IOnConVarValueChanged @event)
```

当 ConVar 的值被更改时调用。

**参数:**

- `@event` (`IOnConVarValueChanged`)

### OnConCommandCreated

```csharp
void OnConCommandCreated(IOnConCommandCreated @event)
```

当创建 ConCommand 时调用。

**参数:**

- `@event` (`IOnConCommandCreated`)

### OnConVarCreated

```csharp
void OnConVarCreated(IOnConVarCreated @event)
```

在创建 ConVar 时被调用。

**参数:**

- `@event` (`IOnConVarCreated`)

### OnEntityTakeDamage

```csharp
void OnEntityTakeDamage(IOnEntityTakeDamageEvent @event)
```

当实体受到伤害时调用。

**参数:**

- `@event` (`IOnEntityTakeDamageEvent`)

### OnPrecacheResource

```csharp
void OnPrecacheResource(IOnPrecacheResourceEvent @event)
```

在资源预缓存时调用。

**参数:**

- `@event` (`IOnPrecacheResourceEvent`)

### OnEntityStartTouch

```csharp
void OnEntityStartTouch(IOnEntityStartTouchEvent @event)
```

当实体开始接触另一个实体时调用。

**参数:**

- `@event` (`IOnEntityStartTouchEvent`)

### OnEntityTouch

```csharp
void OnEntityTouch(IOnEntityTouchEvent @event)
```

当实体与另一实体接触时调用。

**参数:**

- `@event` (`IOnEntityTouchEvent`)

### OnEntityEndTouch

```csharp
void OnEntityEndTouch(IOnEntityEndTouchEvent @event)
```

当实体结束与另一实体的接触时调用。

**参数:**

- `@event` (`IOnEntityEndTouchEvent`)

### OnItemServicesCanAcquireHook

```csharp
void OnItemServicesCanAcquireHook(IOnItemServicesCanAcquireHookEvent @event)
```

当物品服务获取钩子被触发时调用。

**参数:**

- `@event` (`IOnItemServicesCanAcquireHookEvent`)

### OnWeaponServicesCanUseHook

```csharp
void OnWeaponServicesCanUseHook(IOnWeaponServicesCanUseHookEvent @event)
```

当武器服务可使用挂钩被触发时调用。

**参数:**

- `@event` (`IOnWeaponServicesCanUseHookEvent`)

### OnWeaponServicesDropWeaponHook

```csharp
void OnWeaponServicesDropWeaponHook(IOnWeaponServicesDropWeaponHook @event)
```

当武器服务丢弃武器钩被触发时调用。

**参数:**

- `@event` (`IOnWeaponServicesDropWeaponHook`)

### OnClientVoice

```csharp
void OnClientVoice(IOnClientVoiceEvent @event)
```

当客户端发送语音数据包时调用。

**参数:**

- `@event` (`IOnClientVoiceEvent`)

### OnConsoleOutput

```csharp
void OnConsoleOutput(IOnConsoleOutputEvent @event)
```

当接收到控制台输出时调用。

**参数:**

- `@event` (`IOnConsoleOutputEvent`)

### OnCommandExecuteHook

```csharp
void OnCommandExecuteHook(IOnCommandExecuteHookEvent @event)
```

当服务器命令（ConCommand）被执行时调用。

**参数:**

- `@event` (`IOnCommandExecuteHookEvent`)

### OnMovementServicesRunCommandHook

```csharp
void OnMovementServicesRunCommandHook(IOnMovementServicesRunCommandHookEvent @event)
```

当移动服务运行命令钩子被触发时调用。

**参数:**

- `@event` (`IOnMovementServicesRunCommandHookEvent`)

### OnPlayerPawnPostThink

```csharp
void OnPlayerPawnPostThink(IOnPlayerPawnPostThinkHookEvent @event)
```

当玩家 pawn 的后续思考钩子被触发时调用。

**参数:**

- `@event` (`IOnPlayerPawnPostThinkHookEvent`)

### OnEntityIdentityAcceptInputHook

```csharp
void OnEntityIdentityAcceptInputHook(IOnEntityIdentityAcceptInputHookEvent @event)
```

当实体身份接受输入钩子被触发时调用。

**参数:**

- `@event` (`IOnEntityIdentityAcceptInputHookEvent`)

### OnEntityFireOutputHookEvent

```csharp
void OnEntityFireOutputHookEvent(IOnEntityFireOutputHookEvent @event)
```

当实体触发输出时调用。

**参数:**

- `@event` (`IOnEntityFireOutputHookEvent`)

### OnStartupServer

```csharp
void OnStartupServer()
```

服务器启动时调用。

