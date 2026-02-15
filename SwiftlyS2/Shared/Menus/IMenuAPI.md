# 🔌 IMenuAPI

Represents an interactive menu that can be displayed to players.

**命名空间:** `SwiftlyS2.Shared.Menus`

**类型:** `interface`

**继承:** `IDisposable`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `MenuManager` | `IMenuManagerAPI` | get, set | The menu manager that this menu belongs to. |
| `Configuration` | `MenuConfiguration` | get, set | Configuration settings for this menu. |
| `KeybindOverrides` | `MenuKeybindOverrides` | get | Keybind overrides for this menu. |
| `OptionScrollStyle` | `MenuOptionScrollStyle` | get | The scroll style for this menu options. |
| `Builder` | `IMenuBuilderAPI?` | get, set | The builder used to construct and configure this menu. |
| `Tag` | `object?` | get, set | Gets or sets an object that contains data about this menu. |
| `Options` | `IReadOnlyList\<IMenuOption\>` | get | Read-only collection of all options in this menu. |

