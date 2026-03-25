<a id="inetmessageservice"></a>

# 🔌 INetMessageService

**命名空间:** `SwiftlyS2.Shared.NetMessages`

**类型:** `interface`

## ⚙️ 方法

### ServerNetMessageHandler<T>

```csharp
HookResult ServerNetMessageHandler<T>(T msg)
```

用于处理从服务器发送到客户端的网络消息的处理程序。

**参数:**

- `msg` (`T`) - 待处理的网络消息。

**返回值:** `HookResult` - 钩子返回值。

**用法示例:**
```csharp
var result = netMessageService.ServerNetMessageHandler<MyMessageType>(message);
```

### ServerNetMessageInternalHandler<T>

```csharp
HookResult ServerNetMessageInternalHandler<T>(T msg, int playerId)
```

用于处理从服务器发送到客户端的网络消息的处理程序。

**参数:**

- `msg` (`T`) - 待处理的网络消息。
- `playerId` (`int`) - 网络消息的接收者过滤器。

**返回值:** `HookResult` - 钩子返回值。

**用法示例:**
```csharp
var result = netMessageService.ServerNetMessageInternalHandler(msg, playerId);
```

### ClientNetMessageHandler<T>

```csharp
HookResult ClientNetMessageHandler<T>(T msg, int playerId)
```

用于处理从客户端发送至服务器的网络消息的处理程序。

**参数:**

- `msg` (`T`) - 待处理的网络消息。
- `playerId` (`int`) - 发送该网络消息的客户端的玩家 ID。

**返回值:** `HookResult` - 钩子返回值。

**用法示例:**
```csharp
var result = netMessageService.ClientNetMessageHandler(myMessage, playerId);
```

### HookClientMessage<T>

```csharp
Guid HookClientMessage<T>(ClientNetMessageHandler<T> callback)
```

挂钩客户端网络消息。

**参数:**

- `callback` (`ClientNetMessageHandler\<T\>`) - 处理网络消息的回调。

**返回值:** `Guid` - 处理程序的唯一 Guid。后续可用于取消挂钩。

**用法示例:**
```csharp
Guid hookId = netMessageService.HookClientMessage<MyNetMessage>(OnClientMessageReceived);
```

### HookServerMessage<T>

```csharp
Guid HookServerMessage<T>(ServerNetMessageHandler<T> callback)
```

挂钩服务器网络消息。

**参数:**

- `callback` (`ServerNetMessageHandler\<T\>`) - 处理网络消息的回调。

**返回值:** `Guid` - 处理程序的唯一 Guid。后续可用于取消挂钩。

**用法示例:**
```csharp
var hookId = netMessageService.HookServerMessage<MyMessageType>(OnServerMessageReceived);
```

### HookServerMessageInternal<T>

```csharp
Guid HookServerMessageInternal<T>(ServerNetMessageInternalHandler<T> callback)
```

在内部挂钩客户端网络消息。

**参数:**

- `callback` (`ServerNetMessageInternalHandler\<T\>`)

**返回值:** `Guid`

**用法示例:**
```csharp
var hookId = netMessageService.HookServerMessageInternal<MyMessageType>(OnMessageReceived);
```

### Unhook

```csharp
void Unhook(Guid guid)
```

解除对网络消息处理程序的挂钩。

**参数:**

- `guid` (`Guid`) - 处理程序的唯一 GUID。

**用法示例:**
```csharp
netMessageService.Unhook(guid);
```

### UnhookClientMessage<T>

```csharp
void UnhookClientMessage<T>()
```

移除所有指定类型的客户端网络消息处理器。

**用法示例:**
```csharp
messageService.UnhookClientMessage<PlayerChatMessage>();
```

### UnhookServerMessage<T>

```csharp
void UnhookServerMessage<T>()
```

解绑所有具有指定类型的服务器网络消息处理程序。

**用法示例:**
```csharp
netMessageService.UnhookServerMessage<MyMessageType>();
```

### UnhookServerMessageInternal<T>

```csharp
void UnhookServerMessageInternal<T>()
```

取消注册所有指定类型的内部服务器网络消息处理器。

**用法示例:**
```csharp
messageService.UnhookServerMessageInternal<MyMessageType>();
```

### Create<T>

```csharp
T Create<T>()
```

创建一个指定类型的新网络消息。

**返回值:** `T` - 新的网络消息。

**用法示例:**
```csharp
var message = netMessageService.Create<LoginRequest>();
```

### Send<T>

```csharp
void Send<T>(Action<T> configureMessage)
```

向具有已配置接收者过滤器的玩家发送网络消息。

**参数:**

- `configureMessage` (`Action\<T\>`) - 配置网络消息和接收者过滤器的操作。

**用法示例:**
```csharp
NetMessageService.Send<PlayerChatMessage>(msg => { msg.Text = "Hello"; msg.RecipientFilter = PlayerManager.All; });
```

