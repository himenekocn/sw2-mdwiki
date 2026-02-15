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

检查指定路径和路径 ID 处是否存在目录。

**参数:**

- `path` (`string`) - 要检查的路径。
- `pathId` (`string`) - 要搜索的路径的 ID。

**返回值:** `bool` - 如果目录存在，则为 true；否则为 false。

**用法示例:**
```csharp
bool isDir = IGameFileSystem.IsDirectory("Assets/Models", "default");
```

### RemoveSearchPath

```csharp
bool RemoveSearchPath(string path, string pathId)
```

从文件系统中移除一个搜索路径。

**参数:**

- `path` (`string`) - 要移除的路径。
- `pathId` (`string`) - 要移除的路径的 ID。

**返回值:** `bool` - 如果路径已成功移除，则为 true；否则为 false。

**用法示例:**
```csharp
bool removed = gameFileSystem.RemoveSearchPath("assets/models", "models");
```

### AddSearchPath

```csharp
void AddSearchPath(string path, string pathId, SearchPathAdd_t addType, SearchPathPriority_t priority)
```

向文件系统添加搜索路径。

**参数:**

- `path` (`string`) - 要添加的路径。
- `pathId` (`string`) - 要添加的路径的 ID。
- `addType` (`SearchPathAdd_t`) - 要执行的加法类型。
- `priority` (`SearchPathPriority_t`) - 搜索路径的优先级。

**用法示例:**
```csharp
gameFileSystem.AddSearchPath("materials", "mod_content", SearchPathAdd_t.Append, SearchPathPriority_t.High);
```

### FileExists

```csharp
bool FileExists(string filePath, string pathId)
```

检查指定文件路径和路径 ID 处是否存在文件。

**参数:**

- `filePath` (`string`) - 要检查的文件路径。
- `pathId` (`string`) - 要检查的路径的 ID。

**返回值:** `bool` - 如果文件存在，则为 true；否则为 false。

**用法示例:**
```csharp
bool exists = gameFileSystem.FileExists("config.json", "assets");
```

### GetSearchPath

```csharp
string GetSearchPath(string pathId, GetSearchPathTypes_t searchPathType, int searchPathsToGet)
```

获取指定路径 ID 和搜索路径类型的搜索路径。

**参数:**

- `pathId` (`string`) - 要获取搜索路径的路径ID。
- `searchPathType` (`GetSearchPathTypes_t`) - 要获取的搜索路径类型。
- `searchPathsToGet` (`int`) - 要获取的搜索路径数量。

**返回值:** `string` - 给定路径 ID 和搜索路径类型对应的搜索路径。

**用法示例:**
```csharp
string path = gameFileSystem.GetSearchPath("maps", GetSearchPathTypes_t.Value, 1);
```

### ReadFile

```csharp
string ReadFile(string filePath, string pathId)
```

读取指定文件路径和路径 ID 处的文件内容。

**参数:**

- `filePath` (`string`) - 要读取的文件的路径。
- `pathId` (`string`) - 要读取文件的路径的 ID。

**返回值:** `string` - 文件内容，以字符串形式表示。

**用法示例:**
```csharp
string content = gameFileSystem.ReadFile("config/settings.json", "assets");
```

### WriteFile

```csharp
bool WriteFile(string filePath, string pathId, string content)
```

将内容写入指定文件路径和路径 ID 处的文件。

**参数:**

- `filePath` (`string`) - 要写入的文件的路径。
- `pathId` (`string`) - 要写入文件的路径的ID。
- `content` (`string`) - 要写入文件的内容。

**返回值:** `bool` - 如果文件写入成功，则为 true；否则为 false。

**用法示例:**
```csharp
gameFileSystem.WriteFile("data/config.json", "config_path_id", "{\"setting\": true}");
```

### GetFileSize

```csharp
uint GetFileSize(string filePath, string pathId)
```

获取指定文件路径和路径 ID 处的文件大小。

**参数:**

- `filePath` (`string`) - 要获取其大小的文件的路径。
- `pathId` (`string`) - 获取文件大小的路径的ID。

**返回值:** `uint` - 文件的大小（以字节为单位）。

**用法示例:**
```csharp
uint size = gameFileSystem.GetFileSize("config/settings.json", "assets");
```

### PrecacheFile

```csharp
bool PrecacheFile(string filePath, string pathId)
```

在给定的文件路径和路径ID处预缓存一个文件。

**参数:**

- `filePath` (`string`) - 要预缓存的文件的路径。
- `pathId` (`string`) - 用于预缓存文件的路径的 ID。

**返回值:** `bool` - 如果文件已成功预缓存，则为 true；否则为 false。

**用法示例:**
```csharp
gameFileSystem.PrecacheFile("assets/models/player.mdl", "models");
```

### IsFileWritable

```csharp
bool IsFileWritable(string filePath, string pathId)
```

检查给定文件路径和路径 ID 处的文件是否可写。

**参数:**

- `filePath` (`string`) - 要检查的文件的路径。
- `pathId` (`string`) - 要检查的路径的 ID。

**返回值:** `bool` - 如果文件可写，则为 true；否则为 false。

**用法示例:**
```csharp
bool canWrite = gameFileSystem.IsFileWritable("config.json", PathId.Save);
```

### SetFileWritable

```csharp
bool SetFileWritable(string filePath, string pathId, bool writable)
```

设置指定文件路径和路径ID对应的文件的写入状态。

**参数:**

- `filePath` (`string`) - 要设置可写状态的文件的路径。
- `pathId` (`string`) - 要设置可写状态的路径的 ID。
- `writable` (`bool`) - true 表示使文件可写，false 表示使文件只读。

**返回值:** `bool` - 如果可写状态设置成功，则为 true；否则为 false。

**用法示例:**
```csharp
bool result = gameFileSystem.SetFileWritable("config.json", "assets", true);
```

### FindFileAbsoluteList

```csharp
List<string> FindFileAbsoluteList(string wildcard, string pathId)
```

查找所有与给定通配符和路径 ID 匹配的文件。

**参数:**

- `wildcard` (`string`) - 用于匹配文件的通配符。
- `pathId` (`string`) - 要搜索的路径的 ID。

**返回值:** `List\<string\>` - 与给定通配符和路径 ID 匹配的所有文件的列表。

**用法示例:**
```csharp
List<string> files = gameFileSystem.FindFileAbsoluteList("*.txt", "Assets/Data");
```

