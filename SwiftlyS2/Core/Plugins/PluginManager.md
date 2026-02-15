# 📦 PluginManager

**命名空间:** `SwiftlyS2.Core.Plugins`

**类型:** `class`

**继承:** `IPluginManager`

## ⚙️ 方法

### GetPluginStatusByDllName

```csharp
PluginStatus? GetPluginStatusByDllName(string dllName)
```

**参数:**

- `dllName` (`string`)

**返回值:** `PluginStatus?`

### RegenerateTranslations

```csharp
void RegenerateTranslations()
```

### LoadPluginById

```csharp
bool LoadPluginById(string id, bool silent = false)
```

**参数:**

- `id` (`string`)
- `silent` (`bool`) = `false`

**返回值:** `bool`

### LoadPluginByDllName

```csharp
bool LoadPluginByDllName(string dllName, bool hotReload, bool silent = false)
```

**参数:**

- `dllName` (`string`)
- `hotReload` (`bool`)
- `silent` (`bool`) = `false`

**返回值:** `bool`

### UnloadPluginById

```csharp
bool UnloadPluginById(string id, bool silent = false, bool rebuild = true)
```

**参数:**

- `id` (`string`)
- `silent` (`bool`) = `false`
- `rebuild` (`bool`) = `true`

**返回值:** `bool`

### UnloadPluginByDllName

```csharp
bool UnloadPluginByDllName(string dllName, bool silent = false, bool rebuild = true)
```

**参数:**

- `dllName` (`string`)
- `silent` (`bool`) = `false`
- `rebuild` (`bool`) = `true`

**返回值:** `bool`

### ReloadPluginById

```csharp
bool ReloadPluginById(string id, bool silent = false)
```

**参数:**

- `id` (`string`)
- `silent` (`bool`) = `false`

**返回值:** `bool`

### ReloadPluginByDllName

```csharp
bool ReloadPluginByDllName(string dllName, bool silent = false)
```

**参数:**

- `dllName` (`string`)
- `silent` (`bool`) = `false`

**返回值:** `bool`

### FindPluginDirectoryByDllName

```csharp
string? FindPluginDirectoryByDllName(string dllName)
```

**参数:**

- `dllName` (`string`)

**返回值:** `string?`

