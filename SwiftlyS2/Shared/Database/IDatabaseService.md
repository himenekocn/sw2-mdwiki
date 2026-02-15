# 🔌 IDatabaseService

**命名空间:** `SwiftlyS2.Shared.Database`

**类型:** `interface`

## ⚙️ 方法

### GetConnectionString

```csharp
string GetConnectionString(string connectionName)
```

获取指定连接名称的连接字符串。

**参数:**

- `connectionName` (`string`) - 要获取字符串的连接名称。

**返回值:** `string` - 连接字符串。如果未找到连接名称，则返回默认连接字符串。

**用法示例:**
```csharp
string connStr = databaseService.GetConnectionString("MainDb");
```

### GetConnectionInfo

```csharp
DatabaseConnectionInfo GetConnectionInfo(string connectionName)
```

获取指定连接名称的连接信息。

**参数:**

- `connectionName` (`string`) - 要获取信息的连接名称。

**返回值:** `DatabaseConnectionInfo` - 连接信息。如果未找到连接名称，则返回默认连接信息。

**用法示例:**
```csharp
DatabaseConnectionInfo info = databaseService.GetConnectionInfo("PrimaryDb");
```

### GetConnection

```csharp
IDbConnection GetConnection(string connectionName)
```

获取数据库连接。

**参数:**

- `connectionName` (`string`) - 要获取连接的连接名称。

**返回值:** `IDbConnection` - 数据库连接。如果未找到指定的连接名称，则返回默认连接。

**用法示例:**
```csharp
IDbConnection conn = databaseService.GetConnection("MainDb");
```

