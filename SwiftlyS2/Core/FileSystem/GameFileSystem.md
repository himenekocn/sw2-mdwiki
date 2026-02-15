# 📦 GameFileSystem

**命名空间:** `SwiftlyS2.Core.FileSystem`

**类型:** `class`

**继承:** `IGameFileSystem`

## ⚙️ 方法

### AddSearchPath

```csharp
void AddSearchPath(string path, string pathId, SearchPathAdd_t addType, SearchPathPriority_t priority)
```

**参数:**

- `path` (`string`)
- `pathId` (`string`)
- `addType` (`SearchPathAdd_t`)
- `priority` (`SearchPathPriority_t`)

### FileExists

```csharp
bool FileExists(string filePath, string pathId)
```

**参数:**

- `filePath` (`string`)
- `pathId` (`string`)

**返回值:** `bool`

### GetFileSize

```csharp
uint GetFileSize(string filePath, string pathId)
```

**参数:**

- `filePath` (`string`)
- `pathId` (`string`)

**返回值:** `uint`

### GetSearchPath

```csharp
string GetSearchPath(string pathId, GetSearchPathTypes_t searchPathType, int searchPathsToGet)
```

**参数:**

- `pathId` (`string`)
- `searchPathType` (`GetSearchPathTypes_t`)
- `searchPathsToGet` (`int`)

**返回值:** `string`

### IsDirectory

```csharp
bool IsDirectory(string path, string pathId)
```

**参数:**

- `path` (`string`)
- `pathId` (`string`)

**返回值:** `bool`

### IsFileWritable

```csharp
bool IsFileWritable(string filePath, string pathId)
```

**参数:**

- `filePath` (`string`)
- `pathId` (`string`)

**返回值:** `bool`

### PrecacheFile

```csharp
bool PrecacheFile(string filePath, string pathId)
```

**参数:**

- `filePath` (`string`)
- `pathId` (`string`)

**返回值:** `bool`

### PrintSearchPaths

```csharp
void PrintSearchPaths()
```

### ReadFile

```csharp
string ReadFile(string filePath, string pathId)
```

**参数:**

- `filePath` (`string`)
- `pathId` (`string`)

**返回值:** `string`

### RemoveSearchPath

```csharp
bool RemoveSearchPath(string path, string pathId)
```

**参数:**

- `path` (`string`)
- `pathId` (`string`)

**返回值:** `bool`

### SetFileWritable

```csharp
bool SetFileWritable(string filePath, string pathId, bool writable)
```

**参数:**

- `filePath` (`string`)
- `pathId` (`string`)
- `writable` (`bool`)

**返回值:** `bool`

### WriteFile

```csharp
bool WriteFile(string filePath, string pathId, string content)
```

**参数:**

- `filePath` (`string`)
- `pathId` (`string`)
- `content` (`string`)

**返回值:** `bool`

### FindFileAbsoluteList

```csharp
List<string> FindFileAbsoluteList(string wildcard, string pathId)
```

**参数:**

- `wildcard` (`string`)
- `pathId` (`string`)

**返回值:** `List\<string\>`

