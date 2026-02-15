# 🔌 IPluginManager

**命名空间:** `SwiftlyS2.Shared.Plugins`

**类型:** `interface`

## ⚙️ 方法

### LoadPlugin

```csharp
bool LoadPlugin(string pluginId, bool silent = false)
```

加载指定的插件。

**参数:**

- `pluginId` (`string`) - 插件ID。
- `silent` (`bool`) = `false` - 如果为 true，则抑制所有错误消息。

**返回值:** `bool` - 如果插件已成功加载，则为 true；否则为 false。

**用法示例:**
```csharp
bool loaded = pluginManager.LoadPlugin("MyPlugin", false);
```

### UnloadPlugin

```csharp
bool UnloadPlugin(string pluginId, bool silent = false)
```

卸载指定的插件。

**参数:**

- `pluginId` (`string`) - 插件ID。
- `silent` (`bool`) = `false` - 如果为 true，则抑制所有错误消息。

**返回值:** `bool` - 如果插件已成功卸载，则为 true；否则为 false。

**用法示例:**
```csharp
manager.UnloadPlugin("MyPlugin", false);
```

### ReloadPlugin

```csharp
bool ReloadPlugin(string pluginId, bool silent = false)
```

重新加载指定的插件。

**参数:**

- `pluginId` (`string`) - 插件ID。
- `silent` (`bool`) = `false` - 如果为 true，则抑制所有错误消息。

**返回值:** `bool` - 如果插件已成功重新加载，则为 true；否则为 false。

**用法示例:**
```csharp
bool success = pluginManager.ReloadPlugin("MyPlugin", false);
```

### GetPluginStatus

```csharp
PluginStatus? GetPluginStatus(string pluginId)
```

获取指定插件的当前状态。

**参数:**

- `pluginId` (`string`) - 插件ID。

**返回值:** `PluginStatus?`

**用法示例:**
```csharp
PluginStatus? status = pluginManager.GetPluginStatus("my-plugin");
```

### GetPluginMetadata

```csharp
PluginMetadata? GetPluginMetadata(string pluginId)
```

获取指定插件的元数据。

**参数:**

- `pluginId` (`string`) - 插件ID。

**返回值:** `PluginMetadata?`

**用法示例:**
```csharp
PluginMetadata? metadata = pluginManager.GetPluginMetadata("MyPlugin");
```

### GetPluginPath

```csharp
string? GetPluginPath(string pluginId)
```

获取指定插件的路径。

**参数:**

- `pluginId` (`string`) - 插件ID。

**返回值:** `string?`

**用法示例:**
```csharp
string? path = pluginManager.GetPluginPath("MyPlugin");
```

### GetPluginPaths

```csharp
string> GetPluginPaths()
```

获取一个字典，其中包含所有插件的路径，以插件 ID 作为键。

**返回值:** `string\>`

**用法示例:**
```csharp
manager.GetPluginPaths()
```

### GetAllPluginStatuses

```csharp
PluginStatus> GetAllPluginStatuses()
```

获取一个包含所有插件状态的字典，其键为插件ID。

**返回值:** `PluginStatus\>`

**用法示例:**
```csharp
Dictionary<string, PluginStatus> statuses = IPluginManager.GetAllPluginStatuses();
```

### GetAllPluginMetadata

```csharp
PluginMetadata> GetAllPluginMetadata()
```

获取一个包含所有插件元数据的字典，其键为插件 ID。

**返回值:** `PluginMetadata\>`

**用法示例:**
```csharp
IPluginManager.GetAllPluginMetadata();
```

### GetAllPlugins

```csharp
IEnumerable<string> GetAllPlugins()
```

获取所有插件 ID 的列表。

**返回值:** `IEnumerable\<string\>`

**用法示例:**
```csharp
foreach (string pluginId in manager.GetAllPlugins()) Console.WriteLine(pluginId);
```

