# 📦 SelectorMenuOption

Represents a selector menu option that allows cycling through a list of choices using left/right keys. Displays as: Label: PrevChoice [CurrentChoice] NextChoice This option claims the Exit and Use keys for previous and next selection respectively.

**命名空间:** `SwiftlyS2.Core.Menus.OptionsBase`

**类型:** `class`

**继承:** `MenuOptionBase`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `Choices` | `IReadOnlyList\<T\>` | get | Gets the available choices for this selector. |
| `WrapAround` | `bool` | get, set | Gets or sets whether the selector should wrap around when reaching the end. |

## ⚙️ 方法

### Dispose

```csharp
void Dispose()
```

### PauseTextAnimation

```csharp
void PauseTextAnimation()
```

### ResumeTextAnimation

```csharp
void ResumeTextAnimation()
```

### GetDisplayText

```csharp
string GetDisplayText(IPlayer player, int displayLine = 0)
```

**参数:**

- `player` (`IPlayer`)
- `displayLine` (`int`) = `0`

**返回值:** `string`

### GetSelectedIndex

```csharp
int GetSelectedIndex(IPlayer player)
```

Gets the currently selected index for the specified player.

**参数:**

- `player` (`IPlayer`) - The player whose selection to retrieve.

**返回值:** `int` - The selected index.

### GetSelectedChoice

```csharp
T? GetSelectedChoice(IPlayer player)
```

Gets the currently selected choice for the specified player.

**参数:**

- `player` (`IPlayer`) - The player whose selection to retrieve.

**返回值:** `T?` - The selected choice, or default if no choices available.

### SetSelectedIndex

```csharp
void SetSelectedIndex(IPlayer player, int index)
```

Sets the selected index for the specified player.

**参数:**

- `player` (`IPlayer`) - The player whose selection to set.
- `index` (`int`) - The index to select. Will be clamped to valid range.

