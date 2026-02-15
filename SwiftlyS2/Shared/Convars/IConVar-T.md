# 🔌 IConVar<T>

**命名空间:** `SwiftlyS2.Shared.Convars`

**类型:** `interface`

**继承:** `IConVar`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Value` | `T` | get, set | 该控制台变量的值。在设置时，如果该控制台变量可以被复制，它将自动复制到所有客户端。此外，使用此方法设置值会在内部将其放入一个设置队列，这意味着对于某些特殊情况（例如，在钩子内部设置 sv_enablebunnyhopping），它将不起作用，在这种情况下，您应该改用 SetInternal 方法。 |
| `MaxValue` | `T` | get, set | 该控制台变量的最大值。 <exception cref="InvalidOperationException">当控制台变量不是最小/最大类型或没有最大值时抛出。</exception> |
| `MinValue` | `T` | get, set | 该控制台变量的最小值。 <exception cref="InvalidOperationException">当控制台变量不是最小/最大类型或没有最小值时抛出。</exception> |
| `DefaultValue` | `T` | get, set | 该控制台变量的默认值。 |
| `HasDefaultValue` | `bool` | get | 该控制台变量是否具有默认值。 |
| `HasMinValue` | `bool` | get | 该控制台变量是否具有最小值。 |
| `HasMaxValue` | `bool` | get | 该控制台变量是否具有最大值。 |
| `Flags` | `ConvarFlags` | get, set | 该控制台变量的标志。 |

## ⚙️ 方法

### SetInternal

```csharp
void SetInternal(T value)
```

在内部设置控制台变量的值。不会将更改复制到客户端。

**参数:**

- `value` (`T`) - 要设置的值。

**用法示例:**
```csharp
convar.SetInternal(10);
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

### ReplicateToClient

```csharp
void ReplicateToClient(int clientId, T value)
```

将控制台变量的值复制到指定客户端。

**参数:**

- `clientId` (`int`) - 要复制到的客户端 ID。
- `value` (`T`) - 要复制的值。

**用法示例:**
```csharp
convar.ReplicateToClient(player.Id, xxx);
```

### TryGetMinValue

```csharp
bool TryGetMinValue(out T minValue)
```

尝试获取该控制台变量的最小值。

**参数:**

- `minValue` (`out T`) - 该控制台变量的最小值。

**返回值:** `bool` - 如果找到最小值，则为 true；否则为 false。

**用法示例:**
```csharp
int minVal;
bool success = convar.TryGetMinValue(out minVal);
```

### TryGetMaxValue

```csharp
bool TryGetMaxValue(out T maxValue)
```

尝试获取该控制台变量的最大值。

**参数:**

- `maxValue` (`out T`) - 该控制台变量的最大值。

**返回值:** `bool` - 如果找到最大值，则为 true；否则为 false。

**用法示例:**
```csharp
if (convar.TryGetMaxValue(out int maxValue))
{
    Console.WriteLine($"Max value: {maxValue}");
}
```

### TryGetDefaultValue

```csharp
bool TryGetDefaultValue(out T defaultValue)
```

尝试获取该控制台变量的默认值。

**参数:**

- `defaultValue` (`out T`) - 该控制台变量的默认值。

**返回值:** `bool` - 如果找到默认值则为 true，否则为 false。

**用法示例:**
```csharp
convar.TryGetDefaultValue(out var defaultValue);
```

