# 🔌 INetMessageService

**命名空间:** `SwiftlyS2.Shared.NetMessages`

**类型:** `interface`

## ⚙️ 方法

### HookClientMessage<T>

```csharp
Guid HookClientMessage<T>(ClientNetMessageHandler<T> callback)
```

挂钩客户端网络消息。

**参数:**

- `callback` (`ClientNetMessageHandler\<T\>`) - 用于处理网络消息的回调。

**返回值:** `Guid` - 处理程序的唯一 Guid。可用于稍后取消挂钩。

**用法示例:**
```csharp
service.HookClientMessage<MyMessage>(msg => { /* 处理消息 */ });
```

### HookServerMessage<T>

```csharp
Guid HookServerMessage<T>(ServerNetMessageHandler<T> callback)
```

挂钩服务器网络消息。

**参数:**

- `callback` (`ServerNetMessageHandler\<T\>`) - 用于处理网络消息的回调。

**返回值:** `Guid` - 处理程序的唯一 Guid。可用于稍后取消挂钩。

**用法示例:**
```csharp
var messageId = service.HookServerMessage<Player>(HandlePlayerMessage);
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
var messageId = service.HookServerMessageInternal<MyMessage>(msg => { /* 处理消息 */ });
```

### Unhook

```csharp
void Unhook(Guid guid)
```

解除网络消息处理程序的挂钩。

**参数:**

- `guid` (`Guid`) - 处理程序的唯一 Guid。

**用法示例:**
```csharp
manager.Unhook(Guid.NewGuid());
```

### UnhookClientMessage<T>

```csharp
void UnhookClientMessage<T>()
```

取消挂钩所有指定类型的客户端网络消息处理器。

**用法示例:**
```csharp
service.UnhookClientMessage<ChatMessage>();
```

### UnhookServerMessage<T>

```csharp
void UnhookServerMessage<T>()
```

取消所有指定类型的服务器网络消息处理程序的挂钩。

**用法示例:**
```csharp
service.UnhookServerMessage<ChatMessage>();
```

### UnhookServerMessageInternal<T>

```csharp
void UnhookServerMessageInternal<T>()
```

取消挂钩所有指定类型的内部服务器网络消息处理程序。

**用法示例:**
```csharp
service.UnhookServerMessageInternal<SomeMessageType>();
```

### Create<T>

```csharp
T Create<T>()
```

创建指定类型的新网络消息。

**返回值:** `T` - 新的网络消息。

**用法示例:**
```csharp
var message = service.Create<MessageType>();
```

### Send<T>

```csharp
void Send<T>(Action<T> configureMessage)
```

向符合配置的接收者筛选器的玩家发送网络消息。

**参数:**

- `configureMessage` (`Action\<T\>`) - 用于配置网络消息和接收方筛选器的操作。

**用法示例:**
```csharp
service.Send<MyMessage>(msg => msg.SetTarget(Team.T));
```

