<a id="iconvarservice"></a>

# 🔌 IConVarService

**命名空间:** `SwiftlyS2.Shared.Convars`

**类型:** `interface`

## ⚙️ 方法

### Find<T>

```csharp
IConVar<T>? Find<T>(string name)
```

按名称查找现有 convar。

**参数:**

- `name` (`string`) - 控制台变量的名称。

**返回值:** `IConVar\<T\>?` - 如果找到该控制台变量则返回该变量，否则返回null。

**用法示例:**
```csharp
var conVar = conVarService.Find<int>("sv_cheats");
```

### FindAsString

```csharp
IConVar? FindAsString(string name)
```

按名称查找现有控制台变量，无类型限制。

**参数:**

- `name` (`string`) - 控制台变量的名称。

**返回值:** `IConVar?` - 如果找到该控制台变量则返回该变量，否则返回null。

**用法示例:**
```csharp
IConVar? convar = conVarService.FindAsString("sv_cheats");
```

### Create<T>

```csharp
IConVar<T> Create<T>(string name, string helpMessage, T defaultValue, ConvarFlags flags = ConvarFlags.NONE)
```

创建一个新的控制台变量。

**参数:**

- `name` (`string`) - 控制台变量的名称。
- `helpMessage` (`string`) - 该控制台变量的帮助信息。
- `defaultValue` (`T`) - 控制台变量的默认值。
- `flags` (`ConvarFlags`) = `ConvarFlags.NONE` - Convar 的标记。

**返回值:** `IConVar\<T\>` - 创建的convar。

**用法示例:**
```csharp
var myConVar = conVarService.Create<int>("my_var", "My variable description", 42, ConvarFlags.None);
```

### Create<T>

```csharp
IConVar<T> Create<T>(string name, string helpMessage, T defaultValue, T? minValue, T? maxValue, ConvarFlags flags = ConvarFlags.NONE)
```

创建一个带有最小值和最大值的控制台变量。

**参数:**

- `name` (`string`) - 控制台变量的名称。
- `helpMessage` (`string`) - 该控制台变量的帮助信息。
- `defaultValue` (`T`) - 控制台变量的默认值。
- `minValue` (`T?`) - 该 convar 的最小值。
- `maxValue` (`T?`) - convar 的最大值。
- `flags` (`ConvarFlags`) = `ConvarFlags.NONE` - Convar 的标记。

**返回值:** `IConVar\<T\>` - 创建的convar。

**用法示例:**
```csharp
var conVar = conVarService.Create<int>("sv_maxplayers", "Maximum players allowed", 10, 1, 64, ConvarFlags.None);
```

### CreateOrFind<T>

```csharp
IConVar<T> CreateOrFind<T>(string name, string helpMessage, T defaultValue, ConvarFlags flags = ConvarFlags.NONE)
```

通过名称创建新的控制台变量或查找现有变量。

**参数:**

- `name` (`string`) - 控制台变量的名称。
- `helpMessage` (`string`) - 该控制台变量的帮助信息。
- `defaultValue` (`T`) - 控制台变量的默认值。
- `flags` (`ConvarFlags`) = `ConvarFlags.NONE` - Convar 的标记。

**返回值:** `IConVar\<T\>` - 创建或找到的控制台变量。

**用法示例:**
```csharp
var conVar = conVarService.CreateOrFind("my_var", "Help text", 10, ConvarFlags.None);
```

### CreateOrFind<T>

```csharp
IConVar<T> CreateOrFind<T>(string name, string helpMessage, T defaultValue, T? minValue, T? maxValue, ConvarFlags flags = ConvarFlags.NONE)
```

通过名称及其最小值和最大值创建或查找现有的控制台变量。

**参数:**

- `name` (`string`) - 控制台变量的名称。
- `helpMessage` (`string`) - 该控制台变量的帮助信息。
- `defaultValue` (`T`) - 控制台变量的默认值。
- `minValue` (`T?`) - 该 convar 的最小值。
- `maxValue` (`T?`) - convar 的最大值。
- `flags` (`ConvarFlags`) = `ConvarFlags.NONE` - Convar 的标记。

**返回值:** `IConVar\<T\>` - 创建或找到的控制台变量。

**用法示例:**
```csharp
var conVar = conVarService.CreateOrFind<int>("sv_maxplayers", "Max players allowed", 32, 1, 64, ConvarFlags.None);
```

### ReplicateToClient

```csharp
void ReplicateToClient(int clientId, string name, string value)
```

将该变量值复制到指定的客户端。你可以使用此方法复制那些服务器上不存在的变量。

**参数:**

- `clientId` (`int`) - 要复制到的客户端ID。
- `name` (`string`) - 控制台变量的名称。
- `value` (`string`) - 要复制的值。

**用法示例:**
```csharp
convar.ReplicateToClient(1, "sv_cheats", "1");
```

### ReplicateToAll

```csharp
void ReplicateToAll(string name, string value)
```

将该控制台变量的值复制到所有客户端。你可以使用此方法复制那些在服务器上不存在的控制台变量。

**参数:**

- `name` (`string`) - 控制台变量的名称。
- `value` (`string`) - 要复制的值。

**用法示例:**
```csharp
convar.ReplicateToAll("sv_cheats", "1");
```

