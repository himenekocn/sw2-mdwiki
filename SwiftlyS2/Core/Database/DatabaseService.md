# 📦 DatabaseService

**命名空间:** `SwiftlyS2.Core.Database`

**类型:** `class`

**继承:** `IDatabaseService`

## ⚙️ 方法

### GetConnectionString

```csharp
string GetConnectionString(string connectionName)
```

**参数:**

- `connectionName` (`string`)

**返回值:** `string`

### GetConnectionInfo

```csharp
DatabaseConnectionInfo GetConnectionInfo(string connectionName)
```

**参数:**

- `connectionName` (`string`)

**返回值:** `DatabaseConnectionInfo`

### GetConnection

```csharp
IDbConnection GetConnection(string connectionName)
```

**参数:**

- `connectionName` (`string`)

**返回值:** `IDbConnection`

