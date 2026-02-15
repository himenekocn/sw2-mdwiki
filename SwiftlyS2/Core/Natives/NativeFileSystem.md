# 📦 NativeFileSystem

**命名空间:** `SwiftlyS2.Core.Natives`

**类型:** `class`

## ⚙️ 方法

### GetSearchPath (静态)

```csharp
string GetSearchPath(string pathId, int searchPathType, int searchPathsToGet)
```

**参数:**

- `pathId` (`string`)
- `searchPathType` (`int`)
- `searchPathsToGet` (`int`)

**返回值:** `string`

### AddSearchPath (静态)

```csharp
void AddSearchPath(string path, string pathId, int searchPathAdd, int searchPathPriority)
```

**参数:**

- `path` (`string`)
- `pathId` (`string`)
- `searchPathAdd` (`int`)
- `searchPathPriority` (`int`)

### RemoveSearchPath (静态)

```csharp
bool RemoveSearchPath(string path, string pathId)
```

**参数:**

- `path` (`string`)
- `pathId` (`string`)

**返回值:** `bool`

### FileExists (静态)

```csharp
bool FileExists(string fileName, string pathId)
```

**参数:**

- `fileName` (`string`)
- `pathId` (`string`)

**返回值:** `bool`

### IsDirectory (静态)

```csharp
bool IsDirectory(string path, string pathId)
```

**参数:**

- `path` (`string`)
- `pathId` (`string`)

**返回值:** `bool`

### PrintSearchPaths (静态)

```csharp
void PrintSearchPaths()
```

### ReadFile (静态)

```csharp
string ReadFile(string fileName, string pathId)
```

**参数:**

- `fileName` (`string`)
- `pathId` (`string`)

**返回值:** `string`

### WriteFile (静态)

```csharp
bool WriteFile(string fileName, string pathId, string content)
```

**参数:**

- `fileName` (`string`)
- `pathId` (`string`)
- `content` (`string`)

**返回值:** `bool`

### GetFileSize (静态)

```csharp
uint GetFileSize(string fileName, string pathId)
```

**参数:**

- `fileName` (`string`)
- `pathId` (`string`)

**返回值:** `uint`

### PrecacheFile (静态)

```csharp
bool PrecacheFile(string fileName, string pathId)
```

**参数:**

- `fileName` (`string`)
- `pathId` (`string`)

**返回值:** `bool`

### IsFileWritable (静态)

```csharp
bool IsFileWritable(string fileName, string pathId)
```

**参数:**

- `fileName` (`string`)
- `pathId` (`string`)

**返回值:** `bool`

### SetFileWritable (静态)

```csharp
bool SetFileWritable(string fileName, string pathId, bool writable)
```

**参数:**

- `fileName` (`string`)
- `pathId` (`string`)
- `writable` (`bool`)

**返回值:** `bool`

### FindFileAbsoluteList (静态)

```csharp
void FindFileAbsoluteList(nint outVector, string wildcard, string pathId)
```

**参数:**

- `outVector` (`nint`)
- `wildcard` (`string`)
- `pathId` (`string`)

