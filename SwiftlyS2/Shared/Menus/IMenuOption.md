# 🔌 IMenuOption

Represents a menu option that can be displayed and interacted with by players.

**命名空间:** `SwiftlyS2.Shared.Menus`

**类型:** `interface`

**继承:** `IDisposable`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `Menu` | `IMenuAPI?` | get, set | Gets the menu that this option belongs to. |
| `LineCount` | `int` | get, set | Gets the number of lines this option requests to occupy in the menu. |
| `Text` | `string` | get, set | Gets or sets the text content displayed for this menu option. |
| `Comment` | `string` | get, set | Gets or sets the comment content displayed for this menu option. |
| `MaxWidth` | `float` | get, set | The maximum display width for menu option text in relative units. |
| `Visible` | `bool` | get, set | Gets or sets a value indicating whether this option is visible in the menu. |
| `Enabled` | `bool` | get, set | Gets or sets a value indicating whether this option can be interacted with. |
| `CloseAfterClick` | `bool` | get, set | Gets a value indicating whether the menu should be closed after handling the click. |
| `Tag` | `object?` | get, set | Gets or sets an object that contains data about this option. |
| `TextSize` | `MenuOptionTextSize` | get, set | Gets or sets the text size for this option. |
| `TextStyle` | `MenuOptionTextStyle` | get, set | Gets or sets the text overflow style for this option. |
| `PlaySound` | `bool` | get, set | Gets or sets a value indicating whether a sound should play when this option is selected. |

