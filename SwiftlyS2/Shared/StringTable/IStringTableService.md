<a id="istringtableservice"></a>

# 🔌 IStringTableService

**命名空间:** `SwiftlyS2.Shared.StringTable`

**类型:** `interface`

## ⚙️ 方法

### FindTable

```csharp
IStringTable? FindTable(string tableName)
```

根据名称查找字符串表。

**参数:**

- `tableName` (`string`) - 要查找的字符串表名称。

**返回值:** `IStringTable?` - 字符串表，如果未找到则返回 null。

**用法示例:**
```csharp
var table = stringTableService.FindTable("userinfo");
```

### FindTableById

```csharp
IStringTable? FindTableById(int tableId)
```

根据ID查找字符串表。

**参数:**

- `tableId` (`int`) - 要查找的字符串表ID。

**返回值:** `IStringTable?` - 字符串表，如果未找到则返回 null。

**用法示例:**
```csharp
var table = stringTableService.FindTableById(1);
```

