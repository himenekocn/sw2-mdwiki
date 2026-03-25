# 📦 ToggleMenuOption

表示一个可切换的菜单选项，用于显示开/关状态。

**命名空间:** `SwiftlyS2.Core.Menus.OptionsBase`

**类型:** `class`

**继承:** `MenuOptionBase`

## ⚙️ 方法

### GetDisplayText

```csharp
string GetDisplayText(IPlayer player, int displayLine = 0)
```

获取此选项的显示文本，包括切换状态指示器。

**参数:**

- `player` (`IPlayer`) - 查看该选项的玩家。
- `displayLine` (`int`) = `0` - 显示行号（本实现中未使用）。

**返回值:** `string` - 带有切换状态指示器的格式化显示文本。

**用法示例:**
```csharp
string displayText = toggleMenuOption.GetDisplayText(player, 0);
```

### GetToggleState

```csharp
bool GetToggleState(IPlayer player)
```

获取指定玩家的切换状态。

**参数:**

- `player` (`IPlayer`) - 要检索其切换状态的玩家。

**返回值:** `bool` - 若已启用则为 true，若已禁用则为 false。对于新玩家使用配置好的默认值。

**用法示例:**
```csharp
bool isEnabled = toggleMenuOption.GetToggleState(player);
```

### SetToggleState

```csharp
bool SetToggleState(IPlayer player, bool value)
```

设置指定玩家的切换状态并触发值更改事件。

**参数:**

- `player` (`IPlayer`) - 要设置切换状态的玩家。
- `value` (`bool`) - 要设置的切换状态。

**返回值:** `bool` - 如果值被更改则为 true，如果原本就是相同值则为 false。

**用法示例:**
```csharp
bool result = toggleMenuOption.SetToggleState(player, true);
```

