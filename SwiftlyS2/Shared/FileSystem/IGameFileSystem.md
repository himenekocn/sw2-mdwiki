<a id="igamefilesystem"></a>

# 🔌 IGameFileSystem

**命名空间:** `SwiftlyS2.Shared.FileSystem`

**类型:** `interface`

## ⚙️ 方法

### PrintSearchPaths

```csharp
void PrintSearchPaths()
```

将当前搜索路径打印到控制台。

**用法示例:**
```csharp
gameFileSystem.PrintSearchPaths();
```

### IsDirectory

```csharp
bool IsDirectory(string path, string pathId)
```

检查在指定路径和路径ID处是否存在目录。

**参数:**

- `path` (`string`) - 要检查的路径。
- `pathId` (`string`) - 要搜索的路径ID。

**返回值:** `bool` - 如果目录存在则为真，否则为假。

**用法示例:**
```csharp
bool exists = gameFileSystem.IsDirectory("maps/", "map_path_id");
```

### RemoveSearchPath

```csharp
bool RemoveSearchPath(string path, string pathId)
```

从文件系统中移除一个搜索路径。

**参数:**

- `path` (`string`) - 要移除的路径。
- `pathId` (`string`) - 要移除的路径的ID。

**返回值:** `bool` - 如果路径成功移除，则为 true；否则为 false。

**用法示例:**
```csharp
bool removed = fileSystem.RemoveSearchPath("addons/custom_mod", "GAME");
```

### AddSearchPath

```csharp
void AddSearchPath(string path, string pathId, SearchPathAdd_t addType, SearchPathPriority_t priority)
```

向文件系统添加搜索路径。

**参数:**

- `path` (`string`) - 添加路径。
- `pathId` (`string`) - 要添加的路径的ID。
- `addType` (`SearchPathAdd_t`) - 要执行的加法类型。
- `priority` (`SearchPathPriority_t`) - 搜索路径的优先级。

**用法示例:**
```csharp
fileSystem.AddSearchPath("content", "MOD", SearchPathAdd_t.ADD_AT_END, SearchPathPriority_t.PRIORITY_NORMAL);
```

### FileExists

```csharp
bool FileExists(string filePath, string pathId)
```

检查指定文件路径和路径ID处的文件是否存在。

**参数:**

- `filePath` (`string`) - 要检查的文件路径。
- `pathId` (`string`) - 要检入的路径ID。

**返回值:** `bool` - 如果文件存在则为真，否则为假。

**用法示例:**
```csharp
bool exists = gameFileSystem.FileExists("cfg/server.cfg", "MOD");
```

### GetSearchPath

```csharp
string GetSearchPath(string pathId, GetSearchPathTypes_t searchPathType, int searchPathsToGet)
```

获取给定路径ID和搜索路径类型的搜索路径。

**参数:**

- `pathId` (`string`) - 用于获取搜索路径的路径ID。
- `searchPathType` (`GetSearchPathTypes_t`) - 要获取的搜索路径类型。
- `searchPathsToGet` (`int`) - 要获取的搜索路径数量。

**返回值:** `string` - 给定路径ID和搜索路径类型的搜索路径。

**用法示例:**
```csharp
string path = gameFileSystem.GetSearchPath("MOD", GetSearchPathTypes_t.Value, 1);
```

### ReadFile

```csharp
string ReadFile(string filePath, string pathId)
```

读取给定文件路径和路径ID处的文件内容。

**参数:**

- `filePath` (`string`) - 要读取的文件路径。
- `pathId` (`string`) - 用于读取文件的路径ID。

**返回值:** `string` - 文件内容（字符串格式）

**用法示例:**
```csharp
string content = gameFileSystem.ReadFile("config.json", "default");
```

### WriteFile

```csharp
bool WriteFile(string filePath, string pathId, string content)
```

将内容写入指定文件路径和路径ID对应的文件。

**参数:**

- `filePath` (`string`) - 要写入的文件路径。
- `pathId` (`string`) - 要写入文件的路径ID。
- `content` (`string`) - 要写入文件的内容。

**返回值:** `bool` - 如果文件写入成功则为真，否则为假。

**用法示例:**
```csharp
bool success = gameFileSystem.WriteFile("data.txt", "default_id", "Hello World");
```

### GetFileSize

```csharp
uint GetFileSize(string filePath, string pathId)
```

获取给定文件路径和路径ID下的文件大小。

**参数:**

- `filePath` (`string`) - 要获取大小的文件路径。
- `pathId` (`string`) - 获取文件大小的路径ID。

**返回值:** `uint` - 文件大小（以字节为单位）。

**用法示例:**
```csharp
uint size = fileSystem.GetFileSize("config.cfg", "MOD");
```

### PrecacheFile

```csharp
bool PrecacheFile(string filePath, string pathId)
```

在给定文件路径和路径ID下预缓存一个文件。

**参数:**

- `filePath` (`string`) - 要预缓存的文件路径。
- `pathId` (`string`) - 预缓存文件路径的ID。

**返回值:** `bool` - 如果文件预缓存成功则为真，否则为假。

**用法示例:**
```csharp
gameFileSystem.PrecacheFile("models/player.mdl", "GAME");
```

### IsFileWritable

```csharp
bool IsFileWritable(string filePath, string pathId)
```

检查给定文件路径和路径ID的文件是否可写。

**参数:**

- `filePath` (`string`) - 要检查的文件的路径。
- `pathId` (`string`) - 要检入的路径ID。

**返回值:** `bool` - 如果文件可写则为真，否则为假。

**用法示例:**
```csharp
bool canWrite = gameFileSystem.IsFileWritable("config.cfg", "mod_data");
```

### SetFileWritable

```csharp
bool SetFileWritable(string filePath, string pathId, bool writable)
```

设置指定文件路径和路径ID下文件的可写状态。

**参数:**

- `filePath` (`string`) - 要设置可写状态的文件路径。
- `pathId` (`string`) - 用于设置可写状态的路径ID。
- `writable` (`bool`) - 设为 true 使文件可写，设为 false 使其只读。

**返回值:** `bool` - 如果可写状态设置成功则为真，否则为假。

**用法示例:**
```csharp
bool result = fileSystem.SetFileWritable("config.txt", "mod_config", true);
```

### FindFileAbsoluteList

```csharp
List<string> FindFileAbsoluteList(string wildcard, string pathId)
```

查找与给定通配符和路径ID匹配的所有文件。

**参数:**

- `wildcard` (`string`) - 用于匹配文件的通配符。
- `pathId` (`string`) - 要搜索的路径ID。

**返回值:** `List\<string\>` - 与给定的通配符和路径ID匹配的所有文件列表。

**用法示例:**
```csharp
var files = gameFileSystem.FindFileAbsoluteList("*.txt", "root");
```

