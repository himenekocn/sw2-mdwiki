<a id="ipluginmanager"></a>

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

- `pluginId` (`string`) - 插件的ID。
- `silent` (`bool`) = `false` - 如果为真，则抑制所有错误消息。

**返回值:** `bool` - 如果插件加载成功则为真，否则为假。

**用法示例:**
```csharp
manager.LoadPlugin("my_plugin_id", false);
```

### UnloadPlugin

```csharp
bool UnloadPlugin(string pluginId, bool silent = false)
```

卸载指定的插件。

**参数:**

- `pluginId` (`string`) - 插件的ID。
- `silent` (`bool`) = `false` - 如果为真，则抑制所有错误消息。

**返回值:** `bool` - 如果插件成功卸载则为 true，否则为 false。

**用法示例:**
```csharp
bool result = manager.UnloadPlugin("my_plugin_id", false);
```

### ReloadPlugin

```csharp
bool ReloadPlugin(string pluginId, bool silent = false)
```

重新加载指定的插件。

**参数:**

- `pluginId` (`string`) - 插件的ID。
- `silent` (`bool`) = `false` - 如果为真，则抑制所有错误消息。

**返回值:** `bool` - 如果插件重新加载成功，则为 True，否则为 False。

**用法示例:**
```csharp
manager.ReloadPlugin("my_plugin", true);
```

### GetPluginStatus

```csharp
PluginStatus? GetPluginStatus(string pluginId)
```

获取指定插件的状态。

**参数:**

- `pluginId` (`string`) - 插件的ID。

**返回值:** `PluginStatus?`

**用法示例:**
```csharp
var status = manager.GetPluginStatus("my_plugin_id");
```

### GetPluginMetadata

```csharp
PluginMetadata? GetPluginMetadata(string pluginId)
```

获取指定插件的元数据。

**参数:**

- `pluginId` (`string`) - 插件的ID。

**返回值:** `PluginMetadata?`

**用法示例:**
```csharp
var metadata = manager.GetPluginMetadata("my_plugin_id");
```

### GetPluginPath

```csharp
string? GetPluginPath(string pluginId)
```

获取指定插件的路径。

**参数:**

- `pluginId` (`string`) - 插件的ID。

**返回值:** `string?`

**用法示例:**
```csharp
string? path = manager.GetPluginPath("example_plugin");
```

### GetPluginPaths

```csharp
string> GetPluginPaths()
```

获取所有插件路径的字典，以插件ID为键。

**返回值:** `string\>`

**用法示例:**
```csharp
var pluginPaths = manager.GetPluginPaths();
```

### GetAllPluginStatuses

```csharp
PluginStatus> GetAllPluginStatuses()
```

获取所有插件状态的字典，以插件ID为键。

**返回值:** `PluginStatus\>`

**用法示例:**
```csharp
var statuses = manager.GetAllPluginStatuses();
```

### GetAllPluginMetadata

```csharp
PluginMetadata> GetAllPluginMetadata()
```

获取所有插件元数据的字典，键为插件ID。

**返回值:** `PluginMetadata\>`

**用法示例:**
```csharp
var metadataDict = manager.GetAllPluginMetadata();
```

### GetAllPlugins

```csharp
IEnumerable<string> GetAllPlugins()
```

获取所有插件ID的列表。

**返回值:** `IEnumerable\<string\>`

**用法示例:**
```csharp
var pluginIds = manager.GetAllPlugins();
```

