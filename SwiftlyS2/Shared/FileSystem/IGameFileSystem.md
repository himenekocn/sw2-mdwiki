# 🔌 IGameFileSystem

**命名空间:** `SwiftlyS2.Shared.FileSystem`

**类型:** `interface`

## ⚙️ 方法

### PrintSearchPaths

```csharp
void PrintSearchPaths()
```

将当前的搜索路径打印到控制台。

**用法示例:**
```csharp
gameFileSystem.PrintSearchPaths();
```

### IsDirectory

```csharp
bool IsDirectory(string path, string pathId)
```

检查给定路径和路径 ID 处的目录是否存在。

**参数:**

- `path` (`string`) - 待检查的路径。
- `pathId` (`string`) - 要搜索的路径 ID。

**返回值:** `bool` - 如果目录存在则为 true，否则为 false。

**用法示例:**
```csharp
bool exists = gameFileSystem.IsDirectory("maps", "map01");
```

### RemoveSearchPath

```csharp
bool RemoveSearchPath(string path, string pathId)
```

从文件系统中移除搜索路径。

**参数:**

- `path` (`string`) - 要移除的路径。
- `pathId` (`string`) - 要移除的路径的 ID。

**返回值:** `bool` - 如果路径成功移除则为 true，否则为 false。

**用法示例:**
```csharp
bool result = gameFileSystem.RemoveSearchPath("/custom/maps", "map_path_01");
```

### AddSearchPath

```csharp
void AddSearchPath(string path, string pathId, SearchPathAdd_t addType, SearchPathPriority_t priority)
```

向文件系统添加搜索路径。

**参数:**

- `path` (`string`) - 要添加的路径。
- `pathId` (`string`) - 要添加的路径的 ID。
- `addType` (`SearchPathAdd_t`) - 要执行的添加类型。
- `priority` (`SearchPathPriority_t`) - 搜索路径的优先级。

**用法示例:**
```csharp
gameFileSystem.AddSearchPath("custom/maps", "mod1", SearchPathAdd_t.Value, SearchPathPriority_t.Value);
```

### FileExists

```csharp
bool FileExists(string filePath, string pathId)
```

检查给定文件路径和路径 ID 处的文件是否存在。

**参数:**

- `filePath` (`string`) - 待检查的文件路径。
- `pathId` (`string`) - 待检查路径的 ID。

**返回值:** `bool` - 如果文件存在则为 true，否则为 false。

**用法示例:**
```csharp
bool exists = gameFileSystem.FileExists("maps/de_dust2.bsp", "workshop123");
```

### GetSearchPath

```csharp
string GetSearchPath(string pathId, GetSearchPathTypes_t searchPathType, int searchPathsToGet)
```

获取给定路径 ID 和搜索路径类型的搜索路径。

**参数:**

- `pathId` (`string`) - 用于获取搜索路径的路径 ID。
- `searchPathType` (`GetSearchPathTypes_t`) - 要获取的搜索路径类型。
- `searchPathsToGet` (`int`) - 获取搜索路径的数量。

**返回值:** `string` - 给定路径 ID 和搜索路径类型的搜索路径。

**用法示例:**
```csharp
string path = fileSystem.GetSearchPath("MOD", GetSearchPathTypes_t.Value, 1);
```

### ReadFile

```csharp
string ReadFile(string filePath, string pathId)
```

读取指定文件路径及路径 ID 下的文件内容。

**参数:**

- `filePath` (`string`) - 要读取的文件路径。
- `pathId` (`string`) - 读取文件的路径 ID。

**返回值:** `string` - 文件内容作为字符串。

**用法示例:**
```csharp
string content = gameFileSystem.ReadFile("configs/map.cfg", "server_config_01");
```

### WriteFile

```csharp
bool WriteFile(string filePath, string pathId, string content)
```

将内容写入给定文件路径和路径 ID 对应的文件中。

**参数:**

- `filePath` (`string`) - 要写入的文件路径。
- `pathId` (`string`) - 要写入文件的文件路径 ID。
- `content` (`string`) - 要写入文件的内容。

**返回值:** `bool` - 如果文件写入成功则为 true，否则为 false。

**用法示例:**
```csharp
bool success = gameFileSystem.WriteFile("data/config.txt", "cfg001", "Hello World");
```

### GetFileSize

```csharp
uint GetFileSize(string filePath, string pathId)
```

获取给定文件路径和路径 ID 处文件的大小。

**参数:**

- `filePath` (`string`) - 要获取大小的文件路径。
- `pathId` (`string`) - 用于获取文件大小的路径 ID。

**返回值:** `uint` - 文件的大小，单位为字节。

**用法示例:**
```csharp
ulong size = gameFileSystem.GetFileSize("maps/de_dust2.bsp", "MOD");
```

### PrecacheFile

```csharp
bool PrecacheFile(string filePath, string pathId)
```

在指定的文件路径和路径 ID 处预缓存一个文件。

**参数:**

- `filePath` (`string`) - 预缓存文件的路径。
- `pathId` (`string`) - 要预缓存文件的目标路径的 ID。

**返回值:** `bool` - 若文件预加载成功则为 true，否则为 false。

**用法示例:**
```csharp
bool result = gameFileSystem.PrecacheFile("maps/test.bsp", "map_test");
```

### IsFileWritable

```csharp
bool IsFileWritable(string filePath, string pathId)
```

检查给定文件路径和路径 ID 下的文件是否可写。

**参数:**

- `filePath` (`string`) - 待检查文件的路径。
- `pathId` (`string`) - 待检查路径的 ID。

**返回值:** `bool` - 如果文件可写入则为 true，否则为 false。

**用法示例:**
```csharp
bool canWrite = gameFileSystem.IsFileWritable("config/settings.json", "mod_config_01");
```

### SetFileWritable

```csharp
bool SetFileWritable(string filePath, string pathId, bool writable)
```

将指定文件路径和路径 ID 处的文件的可写状态设置为指定值。

**参数:**

- `filePath` (`string`) - 要设置可写状态的文件路径。
- `pathId` (`string`) - 用于设置可写状态的路径 ID。
- `writable` (`bool`) - 设为 true 使文件可写，设为 false 使其为只读。

**返回值:** `bool` - 若可写状态设置成功则为 true，否则为 false。

**用法示例:**
```csharp
bool result = gameFileSystem.SetFileWritable("maps/test.bsp", "map01", true);
```

### FindFileAbsoluteList

```csharp
List<string> FindFileAbsoluteList(string wildcard, string pathId)
```

查找所有与给定通配符和路径 ID 匹配的文件。

**参数:**

- `wildcard` (`string`) - 用于匹配文件的通配符。
- `pathId` (`string`) - 要搜索的路径 ID。

**返回值:** `List\<string\>` - 一个包含所有匹配给定通配符和路径 ID 的文件的列表。

**用法示例:**
```csharp
var files = gameFileSystem.FindFileAbsoluteList("*.cfg", "game");
```

