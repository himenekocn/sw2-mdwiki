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

- `pluginId` (`string`) - 插件的 ID。
- `silent` (`bool`) = `false` - 如果为 true，则抑制任何错误消息。

**返回值:** `bool` - 若插件加载成功则为 true，否则为 false。

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

- `pluginId` (`string`) - 插件的 ID。
- `silent` (`bool`) = `false` - 如果为 true，则抑制任何错误消息。

**返回值:** `bool` - 如果插件卸载成功则为 true，否则为 false。

**用法示例:**
```csharp
manager.UnloadPlugin("example_plugin", false);
```

### ReloadPlugin

```csharp
bool ReloadPlugin(string pluginId, bool silent = false)
```

重新加载指定的插件。

**参数:**

- `pluginId` (`string`) - 插件的 ID。
- `silent` (`bool`) = `false` - 如果为 true，则抑制任何错误消息。

**返回值:** `bool` - 若插件成功重载则为 true，否则为 false。

**用法示例:**
```csharp
bool success = pluginManager.ReloadPlugin("myPlugin", true);
```

### GetPluginStatus

```csharp
PluginStatus? GetPluginStatus(string pluginId)
```

获取指定插件的状态。

**参数:**

- `pluginId` (`string`) - 插件的 ID。

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

- `pluginId` (`string`) - 插件的 ID。

**返回值:** `PluginMetadata?`

**用法示例:**
```csharp
var metadata = manager.GetPluginMetadata("MyPluginId");
```

### GetPluginPath

```csharp
string? GetPluginPath(string pluginId)
```

获取指定插件的路径。

**参数:**

- `pluginId` (`string`) - 插件的 ID。

**返回值:** `string?`

**用法示例:**
```csharp
string? path = manager.GetPluginPath("my-plugin-id");
```

### GetPluginPaths

```csharp
string> GetPluginPaths()
```

获取一个以插件 ID 为键的字典，包含所有插件路径。

**返回值:** `string\>`

**用法示例:**
```csharp
var pluginPaths = manager.GetPluginPaths();
```

### GetAllPluginStatuses

```csharp
PluginStatus> GetAllPluginStatuses()
```

获取一个字典，包含所有插件的状态，键为插件 ID。

**返回值:** `PluginStatus\>`

**用法示例:**
```csharp
var statuses = manager.GetAllPluginStatuses();
```

### GetAllPluginMetadata

```csharp
PluginMetadata> GetAllPluginMetadata()
```

获取所有插件元数据的字典，以插件 ID 为键。

**返回值:** `PluginMetadata\>`

**用法示例:**
```csharp
var metadata = manager.GetAllPluginMetadata();
```

### GetAllPlugins

```csharp
IEnumerable<string> GetAllPlugins()
```

获取所有插件 ID 的列表。

**返回值:** `IEnumerable\<string\>`

**用法示例:**
```csharp
var pluginIds = manager.GetAllPlugins();
```

