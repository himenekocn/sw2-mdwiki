# 📦 ChoiceMenuOption

Represents a menu option that cycles through a list of choices.

**命名空间:** `SwiftlyS2.Core.Menus.OptionsBase`

**类型:** `class`

**继承:** `MenuOptionBase`

## ⚙️ 方法

### GetDisplayText

```csharp
string GetDisplayText(IPlayer player, int displayLine = 0)
```

**参数:**

- `player` (`IPlayer`)
- `displayLine` (`int`) = `0`

**返回值:** `string`

### GetSelectedChoice

```csharp
string GetSelectedChoice(IPlayer player)
```

Gets the currently selected choice for the specified player.

**参数:**

- `player` (`IPlayer`) - The player whose selected choice to retrieve.

**返回值:** `string` - The currently selected choice string.

### SetSelectedChoice

```csharp
void SetSelectedChoice(IPlayer player, string choice)
```

Sets the selected choice for the specified player.

**参数:**

- `player` (`IPlayer`) - The player whose choice to set.
- `choice` (`string`) - The choice to select. Must exist in the <see cref="Choices"/> list.

