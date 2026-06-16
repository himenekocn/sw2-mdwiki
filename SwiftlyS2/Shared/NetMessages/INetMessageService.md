<a id="inetmessageservice"></a>

# 🔌 INetMessageService

**命名空间:** `SwiftlyS2.Shared.NetMessages`

**类型:** `interface`

## ⚙️ 方法

### ServerNetMessageHandler<T>

```csharp
HookResult ServerNetMessageHandler<T>(T msg)
```

用于处理从服务器发送到客户端的网络消息的处理器。

**参数:**

- `msg` (`T`) - 要处理的网络消息。

**返回值:** `HookResult` - Hook 结果。

**用法示例:**
```csharp
var result = netMessageService.ServerNetMessageHandler<MyMessageType>(msg);
```

### ServerNetMessageInternalHandler<T>

```csharp
HookResult ServerNetMessageInternalHandler<T>(T msg, int playerId)
```

用于处理从服务器发送到客户端的网络消息的处理器。

**参数:**

- `msg` (`T`) - 要处理的网络消息。
- `playerId` (`int`) - 网络消息的接收者过滤器。

**返回值:** `HookResult` - Hook 结果。

**用法示例:**
```csharp
var result = netMessageService.ServerNetMessageInternalHandler(msg, playerId);
```

### ClientNetMessageHandler<T>

```csharp
HookResult ClientNetMessageHandler<T>(T msg, int playerId)
```

用于处理从客户端发送到服务器的网络消息的处理器。

**参数:**

- `msg` (`T`) - 要处理的网络消息。
- `playerId` (`int`) - 发送网络消息的客户端的玩家ID。

**返回值:** `HookResult` - Hook 结果。

**用法示例:**
```csharp
var result = netMessageService.ClientNetMessageHandler<MyMessage>(msg, playerId);
```

### HookClientMessage<T>

```csharp
Guid HookClientMessage<T>(ClientNetMessageHandler<T> callback)
```

Hook 一个客户端网络消息。

**参数:**

- `callback` (`ClientNetMessageHandler\<T\>`) - 用于处理网络消息的回调。

**返回值:** `Guid` - 该处理程序的唯一Guid。可用于稍后取消挂接。

**用法示例:**
```csharp
var hookId = netMessageService.HookClientMessage<MyMessage>(OnMyMessageReceived);
```

### HookServerMessage<T>

```csharp
Guid HookServerMessage<T>(ServerNetMessageHandler<T> callback)
```

钩取服务器网络消息。

**参数:**

- `callback` (`ServerNetMessageHandler\<T\>`) - 用于处理网络消息的回调。

**返回值:** `Guid` - 该处理程序的唯一Guid。可用于稍后取消挂接。

**用法示例:**
```csharp
Guid hookId = netMessageService.HookServerMessage<MyMessageType>(OnMessageReceived);
```

### HookServerMessageInternal<T>

```csharp
Guid HookServerMessageInternal<T>(ServerNetMessageInternalHandler<T> callback)
```

内部挂钩客户端网络消息。

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

取消挂钩网络消息处理器。

**参数:**

- `guid` (`Guid`) - 处理程序的唯一GUID。

**用法示例:**
```csharp
messageService.Unhook(messageGuid);
```

### UnhookClientMessage<T>

```csharp
void UnhookClientMessage<T>()
```

使用指定类型卸载所有客户端网络消息处理程序。

**用法示例:**
```csharp
netMessageService.UnhookClientMessage<PlayerChatMessage>();
```

### UnhookServerMessage<T>

```csharp
void UnhookServerMessage<T>()
```

移除指定类型的所有服务器网络消息处理器。

**用法示例:**
```csharp
messageService.UnhookServerMessage<PlayerConnectEvent>();
```

### UnhookServerMessageInternal<T>

```csharp
void UnhookServerMessageInternal<T>()
```

使用指定类型取消挂钩所有内部服务器网络消息处理程序。

**用法示例:**
```csharp
netMessageService.UnhookServerMessageInternal<MyMessageType>();
```

### Create<T>

```csharp
T Create<T>()
```

创建指定类型的新网络消息。

**返回值:** `T` - 新的网络消息。

**用法示例:**
```csharp
var message = netMessageService.Create<LoginRequest>();
```

### Send<T>

```csharp
void Send<T>(Action<T> configureMessage)
```

向配置了接收者过滤器的玩家发送网络消息。

**参数:**

- `configureMessage` (`Action\<T\>`) - 配置网络消息和接收方筛选器的操作。

**用法示例:**
```csharp
netMessageService.Send<PlayerMessage>(msg => msg.Text = "Hello");
```

