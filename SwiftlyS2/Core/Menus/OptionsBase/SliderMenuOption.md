# 📦 SliderMenuOption

Represents a slider menu option that allows selecting a numeric value within a range.

**命名空间:** `SwiftlyS2.Core.Menus.OptionsBase`

**类型:** `class`

**继承:** `MenuOptionBase`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `Min` | `float` | get | Gets the minimum value of the slider. |
| `Max` | `float` | get | Gets the maximum value of the slider. |
| `Step` | `float` | get | Gets the step increment/decrement value. |

## ⚙️ 方法

### GetDisplayText

```csharp
string GetDisplayText(IPlayer player, int displayLine = 0)
```

**参数:**

- `player` (`IPlayer`)
- `displayLine` (`int`) = `0`

**返回值:** `string`

### GetValue

```csharp
float GetValue(IPlayer player)
```

Gets the current slider value for the specified player.

**参数:**

- `player` (`IPlayer`) - The player whose value to retrieve.

**返回值:** `float` - The current slider value.

### SetValue

```csharp
void SetValue(IPlayer player, float value)
```

Sets the slider value for the specified player.

**参数:**

- `player` (`IPlayer`) - The player whose value to set.
- `value` (`float`) - The value to set. Will be clamped between Min and Max.

### DecrementValue

```csharp
ValueTask DecrementValue(IPlayer player)
```

Decrements the slider value by the step amount for the specified player. Wraps to Max if the value goes below Min.

**参数:**

- `player` (`IPlayer`) - The player whose value to decrement.

**返回值:** `ValueTask`

### IncrementValue

```csharp
ValueTask IncrementValue(IPlayer player)
```

Increments the slider value by the step amount for the specified player. Wraps to Min if the value goes above Max.

**参数:**

- `player` (`IPlayer`) - The player whose value to increment.

**返回值:** `ValueTask`

