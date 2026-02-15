# 📦 MenuOptionBase

Provides a base implementation for menu options with event-driven behavior.

**命名空间:** `SwiftlyS2.Core.Menus.OptionsBase`

**类型:** `class`

**继承:** `IMenuOption`

**实现接口:** `IDisposable`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `Menu` | `IMenuAPI?` | get, set | Gets or sets the menu that this option belongs to. |
| `BindingText` | `Func\<string?\>?` | - | Gets or sets a function that dynamically provides the text content for this menu option. |
| `Text` | `string` | - | Gets or sets the text content displayed for this menu option. |
| `Comment` | `string` | get, set | Gets or sets the comment content displayed for this menu option. |
| `MaxWidth` | `float` | - | The maximum display width for menu option text in relative units. |
| `Visible` | `bool` | - | Gets or sets a value indicating whether this option is visible in the menu. |
| `Enabled` | `bool` | - | Gets or sets a value indicating whether this option can be interacted with. |
| `CloseAfterClick` | `bool` | get, set | Gets or sets a value indicating whether the menu should be closed after handling the click. |
| `Tag` | `object?` | get, set | Gets or sets an object that contains data about this option. |
| `TextSize` | `MenuOptionTextSize` | get, set | Gets or sets the text size for this option. |
| `TextStyle` | `MenuOptionTextStyle` | - | Gets or sets the text overflow style for this option. |
| `PlaySound` | `bool` | get, set | Gets or sets a value indicating whether a sound should play when this option is selected. |

## ⚙️ 方法

### Dispose

```csharp
void Dispose()
```

### PauseTextAnimation

```csharp
void PauseTextAnimation()
```

Pauses the dynamic text animation.

### ResumeTextAnimation

```csharp
void ResumeTextAnimation()
```

Resumes the dynamic text animation.

### GetDisplayText

```csharp
string GetDisplayText(IPlayer player, int displayLine = 0)
```

Gets the display text for this option as it should appear to the specified player.

**参数:**

- `player` (`IPlayer`) - The player requesting the display text.
- `displayLine` (`int`) = `0` - The display line index of the option.

**返回值:** `string` - The formatted display text for the option.

### OnValidatingAsync

```csharp
ValueTask<bool> OnValidatingAsync(IPlayer player)
```

Validates whether the specified player can interact with this option.

**参数:**

- `player` (`IPlayer`) - The player to validate.

**返回值:** `ValueTask\<bool\>` - A task that represents the asynchronous operation. The task result is true if validation succeeds; otherwise, false.

### OnClickAsync

```csharp
ValueTask OnClickAsync(IPlayer player)
```

Handles the click action for this option.

**参数:**

- `player` (`IPlayer`) - The player who clicked the option.

**返回值:** `ValueTask` - A task that represents the asynchronous operation.

