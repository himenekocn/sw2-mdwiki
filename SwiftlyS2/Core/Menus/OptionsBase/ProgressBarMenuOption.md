# 📦 ProgressBarMenuOption

表示一个以可视化方式显示进度的进度条菜单选项。

**命名空间:** `SwiftlyS2.Core.Menus.OptionsBase`

**类型:** `class`

**继承:** `MenuOptionBase`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `BarWidth` | `int` | get | 获取进度条的字符宽度。 |
| `ShowPercentage` | `bool` | get | 获取是否显示百分比值。 |
| `LineCount` | `int` | - | - |

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
string text = progressBarMenuOption.GetDisplayText(player, 0);
```

### SetProgressProvider

```csharp
void SetProgressProvider(IPlayer player, Func<float> progressProvider)
```

为特定玩家设置或更新进度提供程序函数。

**参数:**

- `player` (`IPlayer`) - 要设置其进度提供程序的玩家。
- `progressProvider` (`Func\<float\>`) - 返回进度值（0.0 到 1.0）的函数。

**用法示例:**
```csharp
progressBarMenuOption.SetProgressProvider(player, () => 0.5f);
```

### GetProgress

```csharp
float GetProgress(IPlayer player)
```

获取指定玩家的当前进度值。

**参数:**

- `player` (`IPlayer`) - 要获取进度的玩家。

**返回值:** `float` - 当前进度值（范围 0.0 到 1.0）。

**用法示例:**
```csharp
float progress = progressBarMenuOption.GetProgress(player);
```

