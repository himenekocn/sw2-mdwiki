<a id="igameeventservice"></a>

# 🔌 IGameEventService

用于管理游戏事件的插件作用域服务。

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

**返回值:** `HookResult` - Hook 结果。

**用法示例:**
```csharp
var result = gameEventService.GameEventHandler(eventObj);
```

### HookPre<T>

```csharp
Guid HookPre<T>(GameEventHandler<T> callback)
```

钩挂一个预事件回调函数。

**参数:**

- `callback` (`GameEventHandler\<T\>`) - 要挂钩的回调。

**返回值:** `Guid` - 表示挂钩的 GUID。您可以稍后使用此标识符取消挂钩回调。

**用法示例:**
```csharp
var hookId = gameEventService.HookPre<PlayerConnect>(OnPlayerConnect);
```

### HookPost<T>

```csharp
Guid HookPost<T>(GameEventHandler<T> callback)
```

挂钩一个后事件回调函数。

**参数:**

- `callback` (`GameEventHandler\<T\>`) - 要挂钩的回调。

**返回值:** `Guid` - 表示挂钩的 GUID。您可以稍后使用此标识符取消挂钩回调。

**用法示例:**
```csharp
var hookId = gameEventService.HookPost<PlayerDeath>(OnPlayerDeath);
```

### Unhook

```csharp
void Unhook(Guid guid)
```

卸载一个回调。

**参数:**

- `guid` (`Guid`) - 要取消挂钩的钩子的GUID。

**用法示例:**
```csharp
gameEventService.Unhook(eventGuid);
```

### UnhookPre<T>

```csharp
void UnhookPre<T>()
```

取消所有事件前回调。

**用法示例:**
```csharp
gameEventService.UnhookPre<IGameEvent>();
```

### UnhookPost<T>

```csharp
void UnhookPost<T>()
```

卸载所有事件后回调。

**用法示例:**
```csharp
gameEventService.UnhookPost<PlayerConnectEvent>();
```

### Fire<T>

```csharp
void Fire<T>()
```

**用法示例:**
```csharp
gameEventService.Fire<PlayerConnect>();
```

### Fire<T>

```csharp
void Fire<T>(Action<T> configureEvent)
```

**参数:**

- `configureEvent` (`Action\<T\>`)

**用法示例:**
```csharp
gameEventService.Fire<PlayerDeath>(e => { e.UserId = player.Index; e.Attacker = attacker.Index; });
```

### FireAsync<T>

```csharp
Task FireAsync<T>()
```

向所有玩家异步触发一个事件。

**返回值:** `Task`

**用法示例:**
```csharp
await gameEventService.FireAsync<PlayerConnectEvent>();
```

### FireAsync<T>

```csharp
Task FireAsync<T>(Action<T> configureEvent)
```

异步向所有玩家触发一个配置事件。

**参数:**

- `configureEvent` (`Action\<T\>`)

**返回值:** `Task`

**用法示例:**
```csharp
await gameEventService.FireAsync<PlayerConnect>(e => e.PlayerId = playerId);
```

### FireToPlayer<T>

```csharp
void FireToPlayer<T>(int slot)
```

**参数:**

- `slot` (`int`)

**用法示例:**
```csharp
gameEventService.FireToPlayer<EventPlayerDeath>(0);
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
gameEventService.FireToPlayer<PlayerConnect>(0, e => { });
```

### FireToPlayerAsync<T>

```csharp
Task FireToPlayerAsync<T>(int slot)
```

向玩家异步触发一个事件。

**参数:**

- `slot` (`int`) - 玩家槽位。

**返回值:** `Task`

**用法示例:**
```csharp
await gameEventService.FireToPlayerAsync<PlayerDeath>(playerSlot);
```

### FireToPlayerAsync<T>

```csharp
Task FireToPlayerAsync<T>(int slot, Action<T> configureEvent)
```

向玩家异步触发一个已配置的事件。

**参数:**

- `slot` (`int`) - 玩家槽位。
- `configureEvent` (`Action\<T\>`) - 配置事件的操作。

**返回值:** `Task`

**用法示例:**
```csharp
await gameEventService.FireToPlayerAsync<PlayerHurt>(playerSlot, e => { e.UserId = userId; e.Health = 10; });
```

### FireToServer<T>

```csharp
void FireToServer<T>()
```

**用法示例:**
```csharp
gameEventService.FireToServer<MyEventData>();
```

### FireToServer<T>

```csharp
void FireToServer<T>(Action<T> configureEvent)
```

**参数:**

- `configureEvent` (`Action\<T\>`)

**用法示例:**
```csharp
gameEventService.FireToServer<PlayerHurt>(e => { e.Player = player; e.Attacker = attacker; });
```

### FireToServerAsync<T>

```csharp
Task FireToServerAsync<T>()
```

异步向服务器触发一个事件。

**返回值:** `Task`

**用法示例:**
```csharp
await gameEventService.FireToServerAsync<PlayerDeathEvent>();
```

### FireToServerAsync<T>

```csharp
Task FireToServerAsync<T>(Action<T> configureEvent)
```

异步向服务器触发一个已配置的事件。

**参数:**

- `configureEvent` (`Action\<T\>`) - 配置事件的操作。

**返回值:** `Task`

**用法示例:**
```csharp
await gameEventService.FireToServerAsync<PlayerHurt>(e => { e.Player = player; e.Damage = 10; });
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
bool isListening = gameEventService.IsListeningToEvent<PlayerConnect>(player.Slot);
```

