# 🔌 IConVarService

**命名空间:** `SwiftlyS2.Shared.Convars`

**类型:** `interface`

## ⚙️ 方法

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

