<a id="ipluginconfigurationservice"></a>

# 🔌 IPluginConfigurationService

**命名空间:** `SwiftlyS2.Shared.Services`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `BasePath` | `string` | get | 获取插件配置的基础路径。 |
| `Manager` | `IConfigurationManager` | get | 获取配置根节点。 |
| `BasePathExists` | `bool` | get | 基础路径是否存在于文件系统中。 |

## ⚙️ 方法

### GetConfigPath

```csharp
string GetConfigPath(string name)
```

获取配置文件的路径。

**参数:**

- `name` (`string`) - 配置文件名称（含扩展名）。

**返回值:** `string` - 配置文件的路径。

**用法示例:**
```csharp
string configPath = pluginConfigService.GetConfigPath("MyPlugin");
```

### InitializeWithTemplate

```csharp
IPluginConfigurationService InitializeWithTemplate(string name, string templateName)
```

使用模板初始化配置文件。要使用此功能，必须在插件中打包一个 templates 文件夹，并在其中包含该模板文件。

**参数:**

- `name` (`string`) - 配置文件的名称。
- `templateName` (`string`) - 模板文件的名称。

**返回值:** `IPluginConfigurationService`

**用法示例:**
```csharp
configService.InitializeWithTemplate("MyPlugin", "default_config");
```

### InitializeJsonWithModel<T>

```csharp
IPluginConfigurationService InitializeJsonWithModel<T>(string name, string sectionName)
```

使用类作为模板初始化 JSON 配置文件。

**参数:**

- `name` (`string`) - 配置文件的名称。
- `sectionName` (`string`) - 配置文件中的部分名称。

**返回值:** `IPluginConfigurationService`

**用法示例:**
```csharp
var configService = GetService<IPluginConfigurationService>();
configService.InitializeJsonWithModel<MyConfigModel>("MyPlugin", "Settings");
```

### InitializeTomlWithModel<T>

```csharp
IPluginConfigurationService InitializeTomlWithModel<T>(string name, string sectionName)
```

使用类作为模板初始化 TOML 配置文件。

**参数:**

- `name` (`string`) - 配置文件的名称。
- `sectionName` (`string`) - 配置文件中的部分名称。

**返回值:** `IPluginConfigurationService`

**用法示例:**
```csharp
var config = pluginConfigService.InitializeTomlWithModel<MyConfigModel>("MyPlugin", "Settings");
```

### Configure

```csharp
IPluginConfigurationService Configure(Action<IConfigurationBuilder> configure)
```

配置内部配置管理器。

**参数:**

- `configure` (`Action\<IConfigurationBuilder\>`) - 配置管理器的配置操作。

**返回值:** `IPluginConfigurationService` - 插件配置服务。

**用法示例:**
```csharp
pluginConfigurationService.Configure(builder => builder.AddJsonFile("settings.json"));
```

