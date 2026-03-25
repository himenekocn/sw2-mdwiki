<a id="idatabaseservice"></a>

# 🔌 IDatabaseService

**命名空间:** `SwiftlyS2.Shared.Database`

**类型:** `interface`

## ⚙️ 方法

### GetConnectionString

```csharp
string GetConnectionString(string connectionName)
```

获取给定连接名称的连接字符串。

**参数:**

- `connectionName` (`string`) - 要获取其字符串的连接名称。

**返回值:** `string` - 连接字符串。若未找到指定的连接名称，则返回默认连接字符串。

**用法示例:**
```csharp
string connStr = databaseService.GetConnectionString("DefaultDB");
```

### GetConnectionInfo

```csharp
DatabaseConnectionInfo GetConnectionInfo(string connectionName)
```

获取指定连接名称的连接信息。

**参数:**

- `connectionName` (`string`) - 获取信息所需的连接名称。

**返回值:** `DatabaseConnectionInfo` - 连接信息。若未找到指定的连接名称，则返回默认连接信息。

**用法示例:**
```csharp
var info = databaseService.GetConnectionInfo("MainDB");
```

### GetConnection

```csharp
IDbConnection GetConnection(string connectionName)
```

获取数据库连接。

**参数:**

- `connectionName` (`string`) - 获取连接所使用的连接名称。

**返回值:** `IDbConnection` - 数据库连接。如果未找到指定的连接名称，则返回默认连接。

**用法示例:**
```csharp
var connection = databaseService.GetConnection("MainDB");
```

