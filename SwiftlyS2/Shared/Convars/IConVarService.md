# 🔌 IConVarService

**命名空间:** `SwiftlyS2.Shared.Convars`

**类型:** `interface`

## ⚙️ 方法

### Find<T>

```csharp
IConVar<T>? Find<T>(string name)
```

根据名称查找现有控制台变量。

**参数:**

- `name` (`string`) - 控制台变量的名称。

**返回值:** `IConVar\<T\>?` - 如果找到该控制台变量，则为该变量；否则为 null。

**用法示例:**
```csharp
var conVar = convarService.Find<int>("sv_cheats");
```

### FindAsString

```csharp
IConVar? FindAsString(string name)
```

根据名称查找一个无类型的现有控制台变量。

**参数:**

- `name` (`string`) - 控制台变量的名称。

**返回值:** `IConVar?` - 如果找到该控制台变量，则为该变量；否则为 null。

**用法示例:**
```csharp
IConVar? var = convar.FindAsString("sv_cheats");
```

### Create<T>

```csharp
IConVar<T> Create<T>(string name, string helpMessage, T defaultValue, ConvarFlags flags = ConvarFlags.NONE)
```

创建一个新的控制台变量。

**参数:**

- `name` (`string`) - 控制台变量的名称。
- `helpMessage` (`string`) - 该控制台变量的帮助信息。
- `defaultValue` (`T`) - 该控制台变量的默认值。
- `flags` (`ConvarFlags`) = `ConvarFlags.NONE` - 该控制台变量的标志。

**返回值:** `IConVar\<T\>` - 创建的 console variable。

**用法示例:**
```csharp
var myConVar = convarService.Create("myVar", "Description", 42, ConvarFlags.Value);
```

### Create<T>

```csharp
IConVar<T> Create<T>(string name, string helpMessage, T defaultValue, T? minValue, T? maxValue, ConvarFlags flags = ConvarFlags.NONE)
```

创建一个具有最小值和最大值的新控制台变量。

**参数:**

- `name` (`string`) - 控制台变量的名称。
- `helpMessage` (`string`) - 该控制台变量的帮助信息。
- `defaultValue` (`T`) - 该控制台变量的默认值。
- `minValue` (`T?`) - 该控制台变量的最小值。
- `maxValue` (`T?`) - 该控制台变量的最大值。
- `flags` (`ConvarFlags`) = `ConvarFlags.NONE` - 该控制台变量的标志。

**返回值:** `IConVar\<T\>` - 创建的 console variable。

**用法示例:**
```csharp
var myConVar = convarService.Create("myVar", "Description", 10, 0, 100, ConvarFlags.Value);
```

### CreateOrFind<T>

```csharp
IConVar<T> CreateOrFind<T>(string name, string helpMessage, T defaultValue, ConvarFlags flags = ConvarFlags.NONE)
```

创建一个新的控制台变量，或通过名称查找一个已存在的控制台变量。

**参数:**

- `name` (`string`) - 控制台变量的名称。
- `helpMessage` (`string`) - 该控制台变量的帮助信息。
- `defaultValue` (`T`) - 该控制台变量的默认值。
- `flags` (`ConvarFlags`) = `ConvarFlags.NONE` - 该控制台变量的标志。

**返回值:** `IConVar\<T\>` - 已创建或找到的控制台变量。

**用法示例:**
```csharp
var myConVar = convarService.CreateOrFind<int>("myVar", "Help message", 10, ConvarFlags.Value);
```

### CreateOrFind<T>

```csharp
IConVar<T> CreateOrFind<T>(string name, string helpMessage, T defaultValue, T? minValue, T? maxValue, ConvarFlags flags = ConvarFlags.NONE)
```

通过名称创建新控制台变量或查找现有控制台变量，并设置其最小值和最大值。

**参数:**

- `name` (`string`) - 控制台变量的名称。
- `helpMessage` (`string`) - 该控制台变量的帮助信息。
- `defaultValue` (`T`) - 该控制台变量的默认值。
- `minValue` (`T?`) - 该控制台变量的最小值。
- `maxValue` (`T?`) - 该控制台变量的最大值。
- `flags` (`ConvarFlags`) = `ConvarFlags.NONE` - 该控制台变量的标志。

**返回值:** `IConVar\<T\>` - 已创建或找到的控制台变量。

**用法示例:**
```csharp
var myConVar = convarService.CreateOrFind<int>("myVar", "Help", 10, 0, 100, ConvarFlags.Value);
```

### ReplicateToClient

```csharp
void ReplicateToClient(int clientId, string name, string value)
```

将控制台变量的值复制到特定客户端。您可以使用此方法来复制那些服务器上不存在的控制台变量。

**参数:**

- `clientId` (`int`) - 要复制到的客户端 ID。
- `name` (`string`) - 控制台变量的名称。
- `value` (`string`) - 要复制的值。

**用法示例:**
```csharp
convar.ReplicateToClient(123, "sv_cheats", "1");
```

### ReplicateToAll

```csharp
void ReplicateToAll(string name, string value)
```

将控制台变量的值复制到所有客户端。您可以使用此方法来复制那些服务器上不存在的控制台变量。

**参数:**

- `name` (`string`) - 控制台变量的名称。
- `value` (`string`) - 要复制的值。

**用法示例:**
```csharp
convar.ReplicateToAll("sv_cheats", "1");
```

