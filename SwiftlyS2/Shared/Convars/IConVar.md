# 🔌 IConVar

**命名空间:** `SwiftlyS2.Shared.Convars`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | get | 该 convar 的名称。 |
| `HelpText` | `string` | get | 该 cvar 的辅助说明文本。 |
| `ValueAsString` | `string` | get, set | 此命令变量的字符串值。设置时，如果该命令变量可被复制，将自动向所有客户端进行复制。此外，使用此方法设置值会将其内部放入设置队列中，这意味着在某些特殊情况下（例如在钩子函数内设置 sv_enablebunnyhopping），该方法将无法生效；此类情况下应改用 SetInternal 方法。<exception cref="ArgumentException">当字符串值无法解析时抛出。</exception> |
| `MaxValueAsString` | `string` | get, set | 此控制台变量（convar）字符串形式的最大值。<exception cref="ArgumentException">当字符串值无法解析时抛出。</exception> |
| `MinValueAsString` | `string` | get, set | 此 Cvar 字符串值的最小值。<exception cref="ArgumentException">当字符串值无法解析时抛出。</exception> |
| `DefaultValueAsString` | `string` | get, set | 该字符串格式控制台变量的默认值。<exception cref="ArgumentException">当字符串值无法解析时抛出。</exception> |
| `HasDefaultValue` | `bool` | get | 该控制台变量是否具有默认值。 |
| `HasMinValue` | `bool` | get | 该控制台变量是否包含最小值。 |
| `HasMaxValue` | `bool` | get | 该控制台变量是否具有最大值。 |
| `Flags` | `ConvarFlags` | get, set | 该 cvar 的标志。 |

## ⚙️ 方法

### SetInternalAsString

```csharp
void SetInternalAsString(string value)
```

内部设置该变量的值。此更改不会同步至客户端。

**参数:**

- `value` (`string`) - 要设置的值。

**用法示例:**
```csharp
convar.SetInternalAsString("new_value");
```

### ReplicateToClientAsString

```csharp
void ReplicateToClientAsString(int clientId, string value)
```

将指定客户端的 convar 值进行复制。

**参数:**

- `clientId` (`int`) - 用于复制的目标客户端 ID。
- `value` (`string`) - 需要复制的值。

**用法示例:**
```csharp
convar.ReplicateToClientAsString(clientId, value);
```

### QueryClient

```csharp
void QueryClient(int clientId, Action<string> callback)
```

从指定客户端查询该控制变量的值。

**参数:**

- `clientId` (`int`)
- `callback` (`Action\<string\>`) - 带有该值的要执行的操作。

**用法示例:**
```csharp
convar.QueryClient(1, value => Console.WriteLine(value));
```

### TryGetDefaultValueAsString

```csharp
bool TryGetDefaultValueAsString(out string defaultValue)
```

尝试获取该命令变量的默认值。

**参数:**

- `defaultValue` (`out string`) - 该变量的默认值。

**返回值:** `bool` - 若找到默认值则为 true，否则为 false。

**用法示例:**
```csharp
bool success = convar.TryGetDefaultValueAsString(out string defaultValue);
```

### TryGetMinValueAsString

```csharp
bool TryGetMinValueAsString(out string minValue)
```

尝试获取该变量的最小值。

**参数:**

- `minValue` (`out string`) - 该 CVar 的最小值。

**返回值:** `bool` - 当找到最小值时为 true，否则为 false。

**用法示例:**
```csharp
if (convar.TryGetMinValueAsString(out string minValue)) { Console.WriteLine(minValue); }
```

### TryGetMaxValueAsString

```csharp
bool TryGetMaxValueAsString(out string maxValue)
```

尝试获取该cvar的最大值。

**参数:**

- `maxValue` (`out string`) - 该 CVar 的最大值。

**返回值:** `bool` - 如果找到最大值，则为 true；否则为 false。

**用法示例:**
```csharp
if (convar.TryGetMaxValueAsString(out string maxValue)) Console.WriteLine(maxValue);
```

