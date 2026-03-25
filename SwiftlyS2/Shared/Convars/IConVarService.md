<a id="iconvarservice"></a>

# 🔌 IConVarService

**命名空间:** `SwiftlyS2.Shared.Convars`

**类型:** `interface`

## ⚙️ 方法

### Find<T>

```csharp
IConVar<T>? Find<T>(string name)
```

按名称查找现有的 convar。

**参数:**

- `name` (`string`) - 该 cvar 的名称。

**返回值:** `IConVar\<T\>?` - 如果找到该控制台变量则返回，否则为 null。

**用法示例:**
```csharp
var convar = conVarService.Find<int>("maxplayers");
```

### FindAsString

```csharp
IConVar? FindAsString(string name)
```

根据名称查找一个无类型的现有控制台变量。

**参数:**

- `name` (`string`) - 该 cvar 的名称。

**返回值:** `IConVar?` - 如果找到该控制台变量则返回，否则为 null。

**用法示例:**
```csharp
var conVar = conVarService.FindAsString("sv_cheats");
```

### Create<T>

```csharp
IConVar<T> Create<T>(string name, string helpMessage, T defaultValue, ConvarFlags flags = ConvarFlags.NONE)
```

创建一个新的 convar。

**参数:**

- `name` (`string`) - 该 cvar 的名称。
- `helpMessage` (`string`) - 该控制变量的帮助信息。
- `defaultValue` (`T`) - 该变量的默认值。
- `flags` (`ConvarFlags`) = `ConvarFlags.NONE` - 该 cvar 的标志。

**返回值:** `IConVar\<T\>` - 已创建的 cvar。

**用法示例:**
```csharp
var conVar = service.Create<int>("max_players", "Maximum number of players", 10, ConvarFlags.Value);
```

### Create<T>

```csharp
IConVar<T> Create<T>(string name, string helpMessage, T defaultValue, T? minValue, T? maxValue, ConvarFlags flags = ConvarFlags.NONE)
```

创建带有最小值和最大值的新 cvar（控制台变量）。

**参数:**

- `name` (`string`) - 该 cvar 的名称。
- `helpMessage` (`string`) - 该控制变量的帮助信息。
- `defaultValue` (`T`) - 该变量的默认值。
- `minValue` (`T?`) - 该 CVar 的最小值。
- `maxValue` (`T?`) - 该 CVar 的最大值。
- `flags` (`ConvarFlags`) = `ConvarFlags.NONE` - 该 cvar 的标志。

**返回值:** `IConVar\<T\>` - 已创建的 cvar。

**用法示例:**
```csharp
var speedCvar = conVarService.Create<float>("sv_speed", "Player movement speed", 100f, 50f, 300f, ConvarFlags.Value);
```

### CreateOrFind<T>

```csharp
IConVar<T> CreateOrFind<T>(string name, string helpMessage, T defaultValue, ConvarFlags flags = ConvarFlags.NONE)
```

创建一个新的 ConVar 或根据名称查找已存在的 ConVar。

**参数:**

- `name` (`string`) - 该 cvar 的名称。
- `helpMessage` (`string`) - 该控制变量的帮助信息。
- `defaultValue` (`T`) - 该变量的默认值。
- `flags` (`ConvarFlags`) = `ConvarFlags.NONE` - 该 cvar 的标志。

**返回值:** `IConVar\<T\>` - 所创建或已存在的变量。

**用法示例:**
```csharp
var myConVar = convarService.CreateOrFind<int>("max_players", "Maximum players allowed", 10, ConvarFlags.Value);
```

### CreateOrFind<T>

```csharp
IConVar<T> CreateOrFind<T>(string name, string helpMessage, T defaultValue, T? minValue, T? maxValue, ConvarFlags flags = ConvarFlags.NONE)
```

创建一个新的 cvar 或通过名称查找一个现有的 cvar，并设置其最小值和最大值。

**参数:**

- `name` (`string`) - 该 cvar 的名称。
- `helpMessage` (`string`) - 该控制变量的帮助信息。
- `defaultValue` (`T`) - 该变量的默认值。
- `minValue` (`T?`) - 该 CVar 的最小值。
- `maxValue` (`T?`) - 该 CVar 的最大值。
- `flags` (`ConvarFlags`) = `ConvarFlags.NONE` - 该 cvar 的标志。

**返回值:** `IConVar\<T\>` - 所创建或已存在的变量。

**用法示例:**
```csharp
var speedCvar = conVarService.CreateOrFind<float>("sv_speed", "Player movement speed", 250f, 100f, 500f, ConvarFlags.None);
```

### ReplicateToClient

```csharp
void ReplicateToClient(int clientId, string name, string value)
```

将特定控制台变量的值复制给指定客户端。可使用此方法复制那些在服务器上不存在的控制台变量。

**参数:**

- `clientId` (`int`) - 用于复制的目标客户端 ID。
- `name` (`string`) - 该 cvar 的名称。
- `value` (`string`) - 需要复制的值。

**用法示例:**
```csharp
convar.ReplicateToClient(1, "sv_gravity", "800");
```

### ReplicateToAll

```csharp
void ReplicateToAll(string name, string value)
```

将该变量的值复制给所有客户端。你可以使用此方法来同步那些在服务器上不存在的变量（convar）。

**参数:**

- `name` (`string`) - 该 cvar 的名称。
- `value` (`string`) - 需要复制的值。

**用法示例:**
```csharp
convarService.ReplicateToAll("sv_custom_setting", "enabled");
```

