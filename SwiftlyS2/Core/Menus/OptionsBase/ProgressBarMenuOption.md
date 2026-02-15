# 📦 ProgressBarMenuOption

Represents a progress bar menu option that displays progress visually.

**命名空间:** `SwiftlyS2.Core.Menus.OptionsBase`

**类型:** `class`

**继承:** `MenuOptionBase`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `BarWidth` | `int` | get | Gets the width of the progress bar in characters. |
| `ShowPercentage` | `bool` | get | Gets whether to display the percentage value. |

## ⚙️ 方法

### GetDisplayText

```csharp
string GetDisplayText(IPlayer player, int displayLine = 0)
```

**参数:**

- `player` (`IPlayer`)
- `displayLine` (`int`) = `0`

**返回值:** `string`

### SetProgressProvider

```csharp
void SetProgressProvider(IPlayer player, Func<float> progressProvider)
```

Sets or updates the progress provider function for a specific player.

**参数:**

- `player` (`IPlayer`) - The player whose progress provider to set.
- `progressProvider` (`Func\<float\>`) - Function that returns progress value (0.0 to 1.0).

### GetProgress

```csharp
float GetProgress(IPlayer player)
```

Gets the current progress value for the specified player.

**参数:**

- `player` (`IPlayer`) - The player whose progress to retrieve.

**返回值:** `float` - The current progress value (0.0 to 1.0).

