<a id="iconvar"></a>

# 🔌 IConVar

**命名空间:** `SwiftlyS2.Shared.Convars`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | get | 控制台变量名称。 |
| `HelpText` | `string` | get | 控制台变量的帮助文本。 |
| `ValueAsString` | `string` | get, set | 该控制台变量的字符串值。当设置时，如果该控制台变量可被复制，则会自动复制到所有客户端。此外，使用此方法设置值会在内部将其放入一个设置队列中，这意味着对于某些特殊情况（例如在钩子内部设置sv_enablebunnyhopping）将不起作用，在这些情况下应改用SetInternal方法。<exception cref="ArgumentException">当字符串值无法解析时抛出。</exception> |
| `MaxValueAsString` | `string` | get, set | 该控制台变量字符串形式的最大值。<exception cref="ArgumentException">当字符串值无法解析时抛出。</exception> |
| `MinValueAsString` | `string` | get, set | 该convar的最小值（字符串形式）。<exception cref="ArgumentException">当字符串值无法解析时引发。</exception> |
| `DefaultValueAsString` | `string` | get, set | 该ConVar的字符串默认值。  
<exception cref="ArgumentException">当字符串值无法解析时抛出。</exception> |
| `HasDefaultValue` | `bool` | get | 该控制台变量（convar）是否具有默认值。 |
| `HasMinValue` | `bool` | get | 该 convar 是否有最小值。 |
| `HasMaxValue` | `bool` | get | 该控制变量是否存在最大值。 |
| `Flags` | `ConvarFlags` | get, set | Convar 的标记。 |

## ⚙️ 方法

### SetInternalAsString

```csharp
void SetInternalAsString(string value)
```

内部设置控制台变量的值。不会将更改复制到客户端。

**参数:**

- `value` (`string`) - 要设置的值。

**用法示例:**
```csharp
convar.SetInternalAsString("1");
```

### ReplicateToClientAsString

```csharp
void ReplicateToClientAsString(int clientId, string value)
```

将 ConVar 的值复制到指定的客户端。

**参数:**

- `clientId` (`int`) - 要复制到的客户端ID。
- `value` (`string`) - 要复制的值。

**用法示例:**
```csharp
convar.ReplicateToClientAsString(1, "true");
```

### QueryClient

```csharp
void QueryClient(int clientId, Action<string> callback)
```

从指定客户端查询控制台变量的值。

**参数:**

- `clientId` (`int`)
- `callback` (`Action\<string\>`) - 使用该值执行的动作。

**用法示例:**
```csharp
convar.QueryClient(1, value => Console.WriteLine(value));
```

### TryGetDefaultValueAsString

```csharp
bool TryGetDefaultValueAsString(out string defaultValue)
```

尝试获取控制台变量的默认值。

**参数:**

- `defaultValue` (`out string`) - 控制台变量的默认值。

**返回值:** `bool` - 若找到默认值则为True，否则为False。

**用法示例:**
```csharp
convar.TryGetDefaultValueAsString(out string defaultValue);
```

### TryGetMinValueAsString

```csharp
bool TryGetMinValueAsString(out string minValue)
```

尝试获取控制台变量的最小值。

**参数:**

- `minValue` (`out string`) - 该 convar 的最小值。

**返回值:** `bool` - 如果找到最小值则为True，否则为False。

**用法示例:**
```csharp
bool hasMin = convar.TryGetMinValueAsString(out string minValue);
```

### TryGetMaxValueAsString

```csharp
bool TryGetMaxValueAsString(out string maxValue)
```

尝试获取控制台变量的最大值。

**参数:**

- `maxValue` (`out string`) - convar 的最大值。

**返回值:** `bool` - 如果找到最大值则为真，否则为假。

**用法示例:**
```csharp
bool success = convar.TryGetMaxValueAsString(out string maxValue);
```

