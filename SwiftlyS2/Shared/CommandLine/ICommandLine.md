<a id="icommandline"></a>

# 🔌 ICommandLine

**命名空间:** `SwiftlyS2.Shared.CommandLine`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ParameterCount` | `int` | get | 获取命令行中参数的总数。 |
| `CommandLine` | `string` | get | - |
| `HasParameters` | `bool` | get | - |

## ⚙️ 方法

### HasParameter

```csharp
bool HasParameter(string paramName)
```

检查命令行中是否存在该参数。

**参数:**

- `paramName` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool exists = commandLine.HasParameter("-verbose");
```

### GetParameterString

```csharp
string GetParameterString(string paramName, string defaultValue = "")
```

从命令行获取字符串参数。

**参数:**

- `paramName` (`string`)
- `defaultValue` (`string`) = `""`

**返回值:** `string`

**用法示例:**
```csharp
string serverIp = commandLine.GetParameterString("ip", "127.0.0.1");
```

### GetParameterInt

```csharp
int GetParameterInt(string paramName, int defaultValue = 0)
```

从命令行获取一个整型参数。

**参数:**

- `paramName` (`string`)
- `defaultValue` (`int`) = `0`

**返回值:** `int`

**用法示例:**
```csharp
int port = commandLine.GetParameterInt("port", 8080);
```

### GetParameterFloat

```csharp
float GetParameterFloat(string paramName, float defaultValue = 0f)
```

从命令行获取浮点参数。

**参数:**

- `paramName` (`string`)
- `defaultValue` (`float`) = `0f`

**返回值:** `float`

**用法示例:**
```csharp
float value = commandLine.GetParameterFloat("scale", 1.0f);
```

