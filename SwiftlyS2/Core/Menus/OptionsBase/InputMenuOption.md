# 📦 InputMenuOption

Represents a menu option that allows text input from players.

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

### GetValue

```csharp
string GetValue(IPlayer player)
```

Gets the current input value for the specified player.

**参数:**

- `player` (`IPlayer`) - The player whose value to retrieve.

**返回值:** `string` - The current input value.

### SetValue

```csharp
bool SetValue(IPlayer player, string value)
```

Sets the input value for the specified player and triggers validation.

**参数:**

- `player` (`IPlayer`) - The player whose value to set.
- `value` (`string`) - The value to set.

**返回值:** `bool` - True if the value is valid and was set, false otherwise.

### Dispose

```csharp
void Dispose()
```

