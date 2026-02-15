# 📦 ToggleMenuOption

Represents a toggleable menu option that displays an on/off state.

**命名空间:** `SwiftlyS2.Core.Menus.OptionsBase`

**类型:** `class`

**继承:** `MenuOptionBase`

## ⚙️ 方法

### GetDisplayText

```csharp
string GetDisplayText(IPlayer player, int displayLine = 0)
```

Gets the display text for this option, including the toggle state indicator.

**参数:**

- `player` (`IPlayer`) - The player viewing the option.
- `displayLine` (`int`) = `0` - The display line number (not used in this implementation).

**返回值:** `string` - The formatted display text with toggle state indicator.

### GetToggleState

```csharp
bool GetToggleState(IPlayer player)
```

Gets the toggle state for the specified player.

**参数:**

- `player` (`IPlayer`) - The player whose toggle state to retrieve.

**返回值:** `bool` - True if toggled on, false if toggled off. Uses the configured default value for new players.

### SetToggleState

```csharp
bool SetToggleState(IPlayer player, bool value)
```

Sets the toggle state for the specified player and triggers the value changed event.

**参数:**

- `player` (`IPlayer`) - The player whose toggle state to set.
- `value` (`bool`) - The toggle state to set.

**返回值:** `bool` - True if the value was changed, false if it was already the same value.

