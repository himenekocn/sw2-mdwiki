<a id="iconvar-t"></a>

# 🔌 IConVar&lt;T&gt;

**命名空间:** `SwiftlyS2.Shared.Convars`

**类型:** `interface`

**继承:** `IConVar`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Value` | `T` | get, set | 该控制台变量的值。设置时，若此控制台变量可被复制，则其将自动复制至所有客户端。此外，通过此方法设置值时，系统内部会将其置于设置队列中，这意味着在某些特殊情况下（例如在钩子函数内设置 sv_enablebunnyhopping）该操作将无效；此类情况下应改用 SetInternal 方法。 |
| `MaxValue` | `T` | get, set | 该ConVar的最大值。  
<exception cref="InvalidOperationException">当该ConVar不是最小值/最大值类型或没有最大值时抛出。</exception> |
| `MinValue` | `T` | get, set | 该convar的最小值。<exception cref="InvalidOperationException">当该convar不是最小值/最大值类型或没有最小值时抛出。</exception> |
| `DefaultValue` | `T` | get, set | 控制台变量的默认值。 |
| `HasDefaultValue` | `bool` | get | 该控制台变量（convar）是否具有默认值。 |
| `HasMinValue` | `bool` | get | 该 convar 是否有最小值。 |
| `HasMaxValue` | `bool` | get | 该控制变量是否存在最大值。 |
| `Flags` | `ConvarFlags` | get, set | Convar 的标记。 |

## ⚙️ 方法

### SetInternal

```csharp
void SetInternal(T value)
```

内部设置控制台变量的值。不会将更改复制到客户端。

**参数:**

- `value` (`T`) - 要设置的值。

**用法示例:**
```csharp
convar.SetInternal(1);
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

### ReplicateToClient

```csharp
void ReplicateToClient(int clientId, T value)
```

将 ConVar 的值复制到指定的客户端。

**参数:**

- `clientId` (`int`) - 要复制到的客户端ID。
- `value` (`T`) - 要复制的值。

**用法示例:**
```csharp
convar.ReplicateToClient(1, "value");
```

### TryGetMinValue

```csharp
bool TryGetMinValue(out T minValue)
```

尝试获取控制台变量的最小值。

**参数:**

- `minValue` (`out T`) - 该 convar 的最小值。

**返回值:** `bool` - 如果找到最小值则为True，否则为False。

**用法示例:**
```csharp
convar.TryGetMinValue(out var minValue);
```

### TryGetMaxValue

```csharp
bool TryGetMaxValue(out T maxValue)
```

尝试获取控制台变量的最大值。

**参数:**

- `maxValue` (`out T`) - convar 的最大值。

**返回值:** `bool` - 如果找到最大值则为真，否则为假。

**用法示例:**
```csharp
if (convar.TryGetMaxValue(out var maxValue)) Console.WriteLine(maxValue);
```

### TryGetDefaultValue

```csharp
bool TryGetDefaultValue(out T defaultValue)
```

尝试获取控制台变量的默认值。

**参数:**

- `defaultValue` (`out T`) - 控制台变量的默认值。

**返回值:** `bool` - 若找到默认值则为True，否则为False。

**用法示例:**
```csharp
convar.TryGetDefaultValue(out var defaultValue);
```

