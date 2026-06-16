<a id="icommandline"></a>

# 🔌 ICommandLine

**命名空间:** `SwiftlyS2.Shared.CommandLine`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ParameterCount` | `int` | get | 获取命令行中的参数总数。 |
| `CommandLine` | `string` | get | - |
| `HasParameters` | `bool` | get | - |

## ⚙️ 方法

### HasParameter

```csharp
bool HasParameter(string paramName)
```

检查命令行中是否存在某个参数。

**参数:**

- `paramName` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool exists = commandLine.HasParameter("--verbose");
```

### GetParameterString

```csharp
string GetParameterString(string paramName, string defaultValue = "")
```

从命令行获取一个字符串参数。

**参数:**

- `paramName` (`string`)
- `defaultValue` (`string`) = `""`

**返回值:** `string`

**用法示例:**
```csharp
string value = commandLine.GetParameterString("mode", "default");
```

### GetParameterInt

```csharp
int GetParameterInt(string paramName, int defaultValue = 0)
```

从命令行获取一个整数参数。

**参数:**

- `paramName` (`string`)
- `defaultValue` (`int`) = `0`

**返回值:** `int`

**用法示例:**
```csharp
int value = commandLine.GetParameterInt("port", 8080);
```

### GetParameterFloat

```csharp
float GetParameterFloat(string paramName, float defaultValue = 0f)
```

从命令行获取一个浮点参数。

**参数:**

- `paramName` (`string`)
- `defaultValue` (`float`) = `0f`

**返回值:** `float`

**用法示例:**
```csharp
float value = commandLine.GetParameterFloat("volume", 1.0f);
```

