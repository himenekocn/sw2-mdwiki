# 📦 SliderMenuOption

表示一个滑块菜单选项，允许在指定范围内选择一个数值。

**命名空间:** `SwiftlyS2.Core.Menus.OptionsBase`

**类型:** `class`

**继承:** `MenuOptionBase`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Min` | `float` | get | 获取滑块的最小值。 |
| `Max` | `float` | get | 获取滑块的最大值。 |
| `Step` | `float` | get | 获取步进/步退值。 |

## ⚙️ 方法

### GetDisplayText

```csharp
string GetDisplayText(IPlayer player, int displayLine = 0)
```

**参数:**

- `player` (`IPlayer`)
- `displayLine` (`int`) = `0`

**返回值:** `string`

**用法示例:**
```csharp
string text = sliderMenuOption.GetDisplayText(player, 0);
```

### GetValue

```csharp
float GetValue(IPlayer player)
```

获取指定玩家的当前滑块值。

**参数:**

- `player` (`IPlayer`) - 要检索其值的玩家。

**返回值:** `float` - 当前滑块值。

**用法示例:**
```csharp
float value = sliderMenuOption.GetValue(player);
```

### SetValue

```csharp
void SetValue(IPlayer player, float value)
```

为指定玩家设置滑块值。

**参数:**

- `player` (`IPlayer`) - 要设置其值的玩家。
- `value` (`float`) - 要设置的值。该值将被限制在 Min 和 Max 之间。

**用法示例:**
```csharp
sliderMenuOption.SetValue(player, 0.75f);
```

### DecrementValue

```csharp
ValueTask DecrementValue(IPlayer player)
```

将指定玩家的滑块值按步长递减。如果值低于最小值，则回绕到最大值。

**参数:**

- `player` (`IPlayer`) - 要递减其值的玩家。

**返回值:** `ValueTask`

**用法示例:**
```csharp
await sliderMenuOption.DecrementValue(player);
```

### IncrementValue

```csharp
ValueTask IncrementValue(IPlayer player)
```

将指定玩家的滑块值按步长递增。如果值超过最大值，则回绕到最小值。

**参数:**

- `player` (`IPlayer`) - 要增加其值的玩家。

**返回值:** `ValueTask`

**用法示例:**
```csharp
await sliderMenuOption.IncrementValue(player);
```

