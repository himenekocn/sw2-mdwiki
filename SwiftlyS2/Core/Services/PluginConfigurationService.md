# 📦 PluginConfigurationService

**命名空间:** `SwiftlyS2.Core.Services`

**类型:** `class`

**继承:** `IPluginConfigurationService`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `BasePathExists` | `bool` | get | - |
| `Manager` | `IConfigurationManager` | get, set | - |

## ⚙️ 方法

### GetRoot

```csharp
string GetRoot()
```

**返回值:** `string`

### GetConfigPath

```csharp
string GetConfigPath(string name)
```

**参数:**

- `name` (`string`)

**返回值:** `string`

### InitializeWithTemplate

```csharp
IPluginConfigurationService InitializeWithTemplate(string name, string templatePath)
```

**参数:**

- `name` (`string`)
- `templatePath` (`string`)

**返回值:** `IPluginConfigurationService`

### Configure

```csharp
IPluginConfigurationService Configure(Action<IConfigurationBuilder> configure)
```

**参数:**

- `configure` (`Action\<IConfigurationBuilder\>`)

**返回值:** `IPluginConfigurationService`

