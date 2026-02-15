# 🔌 IConVar

**命名空间:** `SwiftlyS2.Shared.Convars`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | get | 控制台变量名称。 |
| `HelpText` | `string` | get | 该控制台变量的帮助文本。 |
| `ValueAsString` | `string` | get, set | 该控制台变量的字符串值。当设置时，如果该控制台变量可以被复制，它将自动复制到所有客户端。此外，使用此方法设置值会将其内部放入一个设置队列，这意味着在某些特殊情况下（例如，在钩子内部设置 sv_enablebunnyhopping）它将不起作用，在这种情况下，您应该改用 SetInternal 方法。<exception cref="ArgumentException">当字符串值无法被解析时抛出。</exception> |
| `MaxValueAsString` | `string` | get, set | 该convar的字符串表示形式的最大值。<exception cref="ArgumentException">当字符串值无法解析时引发。</exception> |
| `MinValueAsString` | `string` | get, set | 该convar的字符串形式的最小值。<exception cref="ArgumentException">当字符串值无法解析时抛出。</exception> |
| `DefaultValueAsString` | `string` | get, set | 该控制台变量的默认值，类型为字符串。<exception cref="ArgumentException">当字符串值无法解析时抛出。</exception> |
| `HasDefaultValue` | `bool` | get | 该控制台变量是否具有默认值。 |
| `HasMinValue` | `bool` | get | 该控制台变量是否具有最小值。 |
| `HasMaxValue` | `bool` | get | 该控制台变量是否具有最大值。 |
| `Flags` | `ConvarFlags` | get, set | 该控制台变量的标志。 |

## ⚙️ 方法

### SetInternalAsString

```csharp
void SetInternalAsString(string value)
```

在内部设置控制台变量的值。不会将更改复制到客户端。

**参数:**

- `value` (`string`) - 要设置的值。

**用法示例:**
```csharp
convar.SetInternalAsString("123");
```

### ReplicateToClientAsString

```csharp
void ReplicateToClientAsString(int clientId, string value)
```

将控制台变量的值复制到指定客户端。

**参数:**

- `clientId` (`int`) - 要复制到的客户端 ID。
- `value` (`string`) - 要复制的值。

**用法示例:**
```csharp
convar.ReplicateToClientAsString(player.Id, "123");
```

### QueryClient

```csharp
void QueryClient(int clientId, Action<string> callback)
```

查询指定客户端的convar值。

**参数:**

- `clientId` (`int`)
- `callback` (`Action\<string\>`) - 要执行的带值的操作。

**用法示例:**
```csharp
convar.QueryClient(1, value => Console.WriteLine($"Client 1 convar: {value}"));
```

### TryGetDefaultValueAsString

```csharp
bool TryGetDefaultValueAsString(out string defaultValue)
```

尝试获取该控制台变量的默认值。

**参数:**

- `defaultValue` (`out string`) - 该控制台变量的默认值。

**返回值:** `bool` - 如果找到默认值则为 true，否则为 false。

**用法示例:**
```csharp
string defaultValue;
bool success = convar.TryGetDefaultValueAsString(out defaultValue);
```

### TryGetMinValueAsString

```csharp
bool TryGetMinValueAsString(out string minValue)
```

尝试获取该控制台变量的最小值。

**参数:**

- `minValue` (`out string`) - 该控制台变量的最小值。

**返回值:** `bool` - 如果找到最小值，则为 true；否则为 false。

**用法示例:**
```csharp
string minValue;
bool success = convar.TryGetMinValueAsString(out minValue);
```

### TryGetMaxValueAsString

```csharp
bool TryGetMaxValueAsString(out string maxValue)
```

尝试获取该控制台变量的最大值。

**参数:**

- `maxValue` (`out string`) - 该控制台变量的最大值。

**返回值:** `bool` - 如果找到最大值，则为 true；否则为 false。

**用法示例:**
```csharp
string maxValue;
bool success = convar.TryGetMaxValueAsString(out maxValue);
```

