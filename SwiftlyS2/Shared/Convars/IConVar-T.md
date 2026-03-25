<a id="iconvar-t"></a>

# 🔌 IConVar&lt;T&gt;

**命名空间:** `SwiftlyS2.Shared.Convars`

**类型:** `interface`

**继承:** `IConVar`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Value` | `T` | get, set | 该 convar 的值。在设置时，如果该 convar 支持复制，它将自动复制到所有客户端。此外，通过此方法设置值会在内部将其放入设置队列中，这意味着在某些特殊情况下（例如，在钩子函数中设置 sv_enablebunnyhopping），该方法将不起作用；在这种情况下，应改用 SetInternal 方法。 |
| `MaxValue` | `T` | get, set | 该命令变量的最大值。<exception cref="InvalidOperationException">当该命令变量不是最小值/最大值类型或不存在最大值时抛出此异常。</exception> |
| `MinValue` | `T` | get, set | 该变量的最小值。 <exception cref="InvalidOperationException">当该变量不是最小/最大值类型或不包含最小值时抛出此异常。</exception> |
| `DefaultValue` | `T` | get, set | 该变量的默认值。 |
| `HasDefaultValue` | `bool` | get | 该控制台变量是否具有默认值。 |
| `HasMinValue` | `bool` | get | 该控制台变量是否包含最小值。 |
| `HasMaxValue` | `bool` | get | 该控制台变量是否具有最大值。 |
| `Flags` | `ConvarFlags` | get, set | 该 cvar 的标志。 |

## ⚙️ 方法

### SetInternal

```csharp
void SetInternal(T value)
```

内部设置该变量的值。此更改不会同步至客户端。

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

从指定客户端查询该控制变量的值。

**参数:**

- `clientId` (`int`)
- `callback` (`Action\<string\>`) - 带有该值的要执行的操作。

**用法示例:**
```csharp
convar.QueryClient(1, value => Console.WriteLine(value));
```

### ReplicateToClient

```csharp
void ReplicateToClient(int clientId, T value)
```

将指定客户端的 convar 值进行复制。

**参数:**

- `clientId` (`int`) - 用于复制的目标客户端 ID。
- `value` (`T`) - 需要复制的值。

**用法示例:**
```csharp
convar.ReplicateToClient(clientId, value);
```

### TryGetMinValue

```csharp
bool TryGetMinValue(out T minValue)
```

尝试获取该变量的最小值。

**参数:**

- `minValue` (`out T`) - 该 CVar 的最小值。

**返回值:** `bool` - 当找到最小值时为 true，否则为 false。

**用法示例:**
```csharp
if (convar.TryGetMinValue(out int minValue)) { Console.WriteLine(minValue); }
```

### TryGetMaxValue

```csharp
bool TryGetMaxValue(out T maxValue)
```

尝试获取该cvar的最大值。

**参数:**

- `maxValue` (`out T`) - 该 CVar 的最大值。

**返回值:** `bool` - 如果找到最大值，则为 true；否则为 false。

**用法示例:**
```csharp
if (convar.TryGetMaxValue(out var maxValue)) Console.WriteLine(maxValue);
```

### TryGetDefaultValue

```csharp
bool TryGetDefaultValue(out T defaultValue)
```

尝试获取该命令变量的默认值。

**参数:**

- `defaultValue` (`out T`) - 该变量的默认值。

**返回值:** `bool` - 若找到默认值则为 true，否则为 false。

**用法示例:**
```csharp
if (convar.TryGetDefaultValue(out int defaultValue)) Console.WriteLine($"Default: {defaultValue}");
```

