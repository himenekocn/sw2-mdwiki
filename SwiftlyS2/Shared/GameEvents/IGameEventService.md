# 🔌 IGameEventService

插件作用域的服务，用于管理游戏事件。

**命名空间:** `SwiftlyS2.Shared.GameEvents`

**类型:** `interface`

## ⚙️ 方法

### GameEventHandler<T>

```csharp
HookResult GameEventHandler<T>(T eventObj)
```

游戏事件回调的委托类型。

**参数:**

- `eventObj` (`T`) - 事件对象。

**返回值:** `HookResult` - 钩子返回值。

**用法示例:**
```csharp
var result = gameEventService.GameEventHandler(eventObj);
```

### HookPre<T>

```csharp
Guid HookPre<T>(GameEventHandler<T> callback)
```

绑定预事件回调。

**参数:**

- `callback` (`GameEventHandler\<T\>`) - 挂钩的回调函数。

**返回值:** `Guid` - 表示钩子的 GUID。您可以稍后使用此 GUID 取消挂钩回调。

**用法示例:**
```csharp
var hookId = gameEventService.HookPre<PlayerConnectEvent>(OnPlayerConnect);
```

### HookPost<T>

```csharp
Guid HookPost<T>(GameEventHandler<T> callback)
```

挂钩一个后事件回调。

**参数:**

- `callback` (`GameEventHandler\<T\>`) - 挂钩的回调函数。

**返回值:** `Guid` - 表示钩子的 GUID。您可以稍后使用此 GUID 取消挂钩回调。

**用法示例:**
```csharp
var hookId = gameEventService.HookPost<PlayerSpawn>(e => Console.WriteLine($"Player {e.Player.Name} spawned"));
```

### Unhook

```csharp
void Unhook(Guid guid)
```

移除回调钩子。

**参数:**

- `guid` (`Guid`) - 要取消挂钩的钩子 GUID。

**用法示例:**
```csharp
gameEventService.Unhook(eventGuid);
```

### UnhookPre<T>

```csharp
void UnhookPre<T>()
```

解绑所有前置事件回调。

**用法示例:**
```csharp
gameEventService.UnhookPre<PlayerConnectEvent>();
```

### UnhookPost<T>

```csharp
void UnhookPost<T>()
```

取消所有后置事件回调的挂钩。

**用法示例:**
```csharp
gameEventService.UnhookPost<Player>();
```

### Fire<T>

```csharp
void Fire<T>()
```

**用法示例:**
```csharp
gameEventService.Fire<PlayerShootEvent>();
```

### Fire<T>

```csharp
void Fire<T>(Action<T> configureEvent)
```

**参数:**

- `configureEvent` (`Action\<T\>`)

**用法示例:**
```csharp
gameEventService.Fire<PlayerHurt>(e => e.UserId = player.Id);
```

### FireAsync<T>

```csharp
Task FireAsync<T>()
```

异步向所有玩家触发事件。

**返回值:** `Task`

**用法示例:**
```csharp
await gameEventService.FireAsync<PlayerJoinEvent>();
```

### FireAsync<T>

```csharp
Task FireAsync<T>(Action<T> configureEvent)
```

异步向所有已配置事件的玩家触发事件。

**参数:**

- `configureEvent` (`Action\<T\>`)

**返回值:** `Task`

**用法示例:**
```csharp
await gameEventService.FireAsync<PlayerShootEvent>(e => e.Damage = 50);
```

### FireToPlayer<T>

```csharp
void FireToPlayer<T>(int slot)
```

**参数:**

- `slot` (`int`)

**用法示例:**
```csharp
gameEventService.FireToPlayer<PlayerSpawned>(1);
```

### FireToPlayer<T>

```csharp
void FireToPlayer<T>(int slot, Action<T> configureEvent)
```

**参数:**

- `slot` (`int`)
- `configureEvent` (`Action\<T\>`)

**用法示例:**
```csharp
gameEventService.FireToPlayer<PlayerShootEvent>(1, e => e.Damage = 50);
```

### FireToPlayerAsync<T>

```csharp
Task FireToPlayerAsync<T>(int slot)
```

异步向玩家触发事件。

**参数:**

- `slot` (`int`) - 玩家槽位。

**返回值:** `Task`

**用法示例:**
```csharp
await gameEventService.FireToPlayerAsync<PlayerDeathEvent>(1);
```

### FireToPlayerAsync<T>

```csharp
Task FireToPlayerAsync<T>(int slot, Action<T> configureEvent)
```

异步向已配置事件的目标玩家触发事件。

**参数:**

- `slot` (`int`) - 玩家槽位。
- `configureEvent` (`Action\<T\>`) - 配置事件的指令。

**返回值:** `Task`

**用法示例:**
```csharp
await gameEventService.FireToPlayerAsync<PlayerHurt>(slot, e => e.Damage = 50);
```

### FireToServer<T>

```csharp
void FireToServer<T>()
```

**用法示例:**
```csharp
gameEventService.FireToServer<PlayerConnectEventArgs>();
```

### FireToServer<T>

```csharp
void FireToServer<T>(Action<T> configureEvent)
```

**参数:**

- `configureEvent` (`Action\<T\>`)

**用法示例:**
```csharp
gameEventService.FireToServer<PlayerHurtEvent>(e => e.Player = player);
```

### FireToServerAsync<T>

```csharp
Task FireToServerAsync<T>()
```

异步向服务器触发事件。

**返回值:** `Task`

**用法示例:**
```csharp
await gameEventService.FireToServerAsync<PlayerShootEvent>();
```

### FireToServerAsync<T>

```csharp
Task FireToServerAsync<T>(Action<T> configureEvent)
```

异步向服务器发送已配置的事件。

**参数:**

- `configureEvent` (`Action\<T\>`) - 配置事件的指令。

**返回值:** `Task`

**用法示例:**
```csharp
await gameEventService.FireToServerAsync<PlayerHurtEvent>(e => e.Player = player);
```

### IsListeningToEvent

```csharp
bool IsListeningToEvent(int slot, string eventName)
```

检查玩家是否正在监听此事件。

**参数:**

- `slot` (`int`) - 玩家槽位。
- `eventName` (`string`) - 事件名称。

**返回值:** `bool`

**用法示例:**
```csharp
bool isListening = gameEventService.IsListeningToEvent(1, "player_death");
```

### IsListeningToEvent<T>

```csharp
bool IsListeningToEvent<T>(int slot)
```

检查玩家是否正在监听此事件。

**参数:**

- `slot` (`int`) - 玩家槽位。

**返回值:** `bool`

**用法示例:**
```csharp
bool isListening = gameEventService.IsListeningToEvent<PlayerDeathEvent>(0);
```

