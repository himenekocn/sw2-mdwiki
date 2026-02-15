# 📦 CommandService

**命名空间:** `SwiftlyS2.Core.Commands`

**类型:** `class`

**继承:** `ICommandService`

**实现接口:** `IDisposable`

## ⚙️ 方法

### RegisterCommand

```csharp
Guid RegisterCommand(string commandName, ICommandService.CommandListener handler, bool registerRaw, string permission)
```

**参数:**

- `commandName` (`string`)
- `handler` (`ICommandService.CommandListener`)
- `registerRaw` (`bool`)
- `permission` (`string`)

**返回值:** `Guid`

### RegisterCommand

```csharp
Guid RegisterCommand(string commandName, ICommandService.CommandListener handler, bool registerRaw = false, string permission = "", string helpText = "SwiftlyS2 registered command")
```

**参数:**

- `commandName` (`string`)
- `handler` (`ICommandService.CommandListener`)
- `registerRaw` (`bool`) = `false`
- `permission` (`string`) = `""`
- `helpText` (`string`) = `"SwiftlyS2 registered command"`

**返回值:** `Guid`

### RegisterCommandAlias

```csharp
void RegisterCommandAlias(string commandName, string alias, bool registerRaw = false)
```

**参数:**

- `commandName` (`string`)
- `alias` (`string`)
- `registerRaw` (`bool`) = `false`

### UnregisterCommand

```csharp
void UnregisterCommand(Guid guid)
```

**参数:**

- `guid` (`Guid`)

### UnregisterCommand

```csharp
void UnregisterCommand(string commandName)
```

**参数:**

- `commandName` (`string`)

### IsCommandRegistered

```csharp
bool IsCommandRegistered(string commandName)
```

**参数:**

- `commandName` (`string`)

**返回值:** `bool`

### HookClientCommand

```csharp
Guid HookClientCommand(ICommandService.ClientCommandHandler handler)
```

**参数:**

- `handler` (`ICommandService.ClientCommandHandler`)

**返回值:** `Guid`

### UnhookClientCommand

```csharp
void UnhookClientCommand(Guid guid)
```

**参数:**

- `guid` (`Guid`)

### HookClientChat

```csharp
Guid HookClientChat(ICommandService.ClientChatHandler handler)
```

**参数:**

- `handler` (`ICommandService.ClientChatHandler`)

**返回值:** `Guid`

### UnhookClientChat

```csharp
void UnhookClientChat(Guid guid)
```

**参数:**

- `guid` (`Guid`)

### Dispose

```csharp
void Dispose()
```

