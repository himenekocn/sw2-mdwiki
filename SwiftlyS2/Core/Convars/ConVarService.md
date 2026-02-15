# 📦 ConVarService

**命名空间:** `SwiftlyS2.Core.Convars`

**类型:** `class`

**继承:** `IConVarService`

## ⚙️ 方法

### FindAsString

```csharp
IConVar? FindAsString(string name)
```

**参数:**

- `name` (`string`)

**返回值:** `IConVar?`

### ReplicateToClient

```csharp
void ReplicateToClient(int clientId, string name, string value)
```

**参数:**

- `clientId` (`int`)
- `name` (`string`)
- `value` (`string`)

### ReplicateToAll

```csharp
void ReplicateToAll(string name, string value)
```

**参数:**

- `name` (`string`)
- `value` (`string`)

