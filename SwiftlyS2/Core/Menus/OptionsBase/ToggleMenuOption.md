# 📦 ToggleMenuOption

表示一个可切换的菜单选项，显示开/关状态。

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
- `displayLine` (`int`) = `0` - 显示行号（此实现中未使用）。

**返回值:** `string` - 带切换状态指示器的格式化显示文本。

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

- `player` (`IPlayer`) - 要获取其切换状态的玩家。

**返回值:** `bool` - 如果切换为开启则返回 true，如果切换为关闭则返回 false。新玩家将使用配置的默认值。

**用法示例:**
```csharp
bool state = toggleMenuOption.GetToggleState(player);
```

### SetToggleState

```csharp
bool SetToggleState(IPlayer player, bool value)
```

设置指定玩家的切换状态，并触发值更改事件。

**参数:**

- `player` (`IPlayer`) - 要设置其切换状态的玩家。
- `value` (`bool`) - 要设置的切换状态。

**返回值:** `bool` - 如果值已更改，则为 true；如果值已相同，则为 false。

**用法示例:**
```csharp
toggleMenuOption.SetToggleState(player, true);
```

