<a id="togglemenuoption"></a>

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

- `player` (`IPlayer`) - 正在查看该选项的玩家。
- `displayLine` (`int`) = `0` - 此实现中未使用的显示行号。

**返回值:** `string` - 带切换状态指示器的格式化显示文本。

**用法示例:**
```csharp
string text = toggleMenuOption.GetDisplayText(player, 0);
```

### GetToggleState

```csharp
bool GetToggleState(IPlayer player)
```

获取指定玩家的开关状态。

**参数:**

- `player` (`IPlayer`) - 要检索其切换状态的玩家。

**返回值:** `bool` - 如果开关打开则为 true，如果开关关闭则为 false。对于新玩家，使用已配置的默认值。

**用法示例:**
```csharp
bool state = toggleMenuOption.GetToggleState(player);
```

### SetToggleState

```csharp
bool SetToggleState(IPlayer player, bool value)
```

为指定玩家设置切换状态，并触发值更改事件。

**参数:**

- `player` (`IPlayer`) - 要设置切换状态的玩家。
- `value` (`bool`) - 要设置的开关键状态。

**返回值:** `bool` - 如果值已被更改则为 true，如果已是相同值则为 false。

**用法示例:**
```csharp
bool result = toggleMenuOption.SetToggleState(player, true);
```

