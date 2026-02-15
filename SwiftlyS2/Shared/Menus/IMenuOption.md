# 🔌 IMenuOption

表示一个可供玩家显示和交互的菜单选项。

**命名空间:** `SwiftlyS2.Shared.Menus`

**类型:** `interface`

**继承:** `IDisposable`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Menu` | `IMenuAPI?` | get | 获取此选项所属的菜单。 |
| `LineCount` | `int` | get | 获取此选项在菜单中请求占用的行数。 |
| `Text` | `string` | get, set | 获取或设置为此菜单选项显示的文本内容。 |
| `Comment` | `string` | get, set | 获取或设置为此菜单选项显示的注释内容。 |
| `MaxWidth` | `float` | get, set | 菜单选项文本的最大显示宽度（以相对单位表示）。 |
| `Visible` | `bool` | get, set | 获取或设置一个值，该值指示此选项是否在菜单中可见。 |
| `Enabled` | `bool` | get, set | 获取或设置一个值，该值指示此选项是否可以交互。 |
| `CloseAfterClick` | `bool` | get | 获取一个值，该值指示在处理完点击后是否应关闭菜单。 |
| `Tag` | `object?` | get, set | 获取或设置一个包含此选项相关数据的对象。 |
| `TextSize` | `MenuOptionTextSize` | get, set | 获取或设置此选项的文本大小。 |
| `TextStyle` | `MenuOptionTextStyle` | get, set | 获取或设置此选项的文本溢出样式。 |
| `PlaySound` | `bool` | get, set | 获取或设置一个值，该值指示当选择此选项时是否应播放声音。 |

## ⚙️ 方法

### IsClickTaskCompleted

```csharp
bool IsClickTaskCompleted(IPlayer player)
```

确定指定玩家的点击任务是否已完成。

**参数:**

- `player` (`IPlayer`) - 要检查的玩家。

**返回值:** `bool` - 如果点击任务已完成，则为 true；否则为 false。

**用法示例:**
```csharp
bool completed = menuOption.IsClickTaskCompleted(player);
```

### GetVisible

```csharp
bool GetVisible(IPlayer player)
```

确定此选项是否对指定玩家可见。

**参数:**

- `player` (`IPlayer`) - 要检查其可见性的玩家。

**返回值:** `bool` - 如果该选项对玩家可见，则为 true；否则为 false。

**用法示例:**
```csharp
return menuOption.GetVisible(player);
```

### SetVisible

```csharp
void SetVisible(IPlayer player, bool visible)
```

设置此选项对特定玩家的可见性。

**参数:**

- `player` (`IPlayer`) - 要设置其可见性的玩家。
- `visible` (`bool`) - 为 true 时，使该选项对玩家可见；为 false 时，隐藏该选项。

**用法示例:**
```csharp
menuOption.SetVisible(player, true);
```

### GetEnabled

```csharp
bool GetEnabled(IPlayer player)
```

确定此选项是否为指定玩家启用。

**参数:**

- `player` (`IPlayer`) - 要检查启用状态的玩家。

**返回值:** `bool` - 如果该选项对玩家已启用，则为 true；否则为 false。

**用法示例:**
```csharp
bool enabled = menuOption.GetEnabled(player);
```

### SetEnabled

```csharp
void SetEnabled(IPlayer player, bool enabled)
```

为特定玩家设置此选项的启用状态。

**参数:**

- `player` (`IPlayer`) - 要设置启用状态的玩家。
- `enabled` (`bool`) - 为 true 时启用该玩家选项；为 false 时禁用该选项。

**用法示例:**
```csharp
menuOption.SetEnabled(player, true);
```

### GetText

```csharp
string GetText(IPlayer player)
```

**参数:**

- `player` (`IPlayer`)

**返回值:** `string`

**用法示例:**
```csharp
player.GetText();
```

### GetFormattedHtmlText

```csharp
string GetFormattedHtmlText(IPlayer player)
```

**参数:**

- `player` (`IPlayer`)

**返回值:** `string`

**用法示例:**
```csharp
option.GetFormattedHtmlText(player);
```

### GetDisplayText

```csharp
string GetDisplayText(IPlayer player, int displayLine = 0)
```

获取此选项的显示文本，该文本应显示给指定的玩家。

**参数:**

- `player` (`IPlayer`) - 请求显示文本的玩家。
- `displayLine` (`int`) = `0` - 选项的显示行索引。

**返回值:** `string` - 选项的格式化显示文本。

**用法示例:**
```csharp
return option.GetDisplayText(player, 0);
```

### OnValidatingAsync

```csharp
ValueTask<bool> OnValidatingAsync(IPlayer player)
```

验证指定的玩家是否可以与此选项进行交互。

**参数:**

- `player` (`IPlayer`) - 要验证的玩家。

**返回值:** `ValueTask\<bool\>` - 一个表示异步操作的任务。如果验证成功，任务结果为 true；否则为 false。

**用法示例:**
```csharp
await menuOption.OnValidatingAsync(player);
```

### OnClickAsync

```csharp
ValueTask OnClickAsync(IPlayer player, bool closeMenu = false)
```

**参数:**

- `player` (`IPlayer`)
- `closeMenu` (`bool`) = `false`

**返回值:** `ValueTask`

**用法示例:**
```csharp
await menuOption.OnClickAsync(player, true);
```

### OnClickAsync

```csharp
ValueTask OnClickAsync(IPlayer player)
```

处理此选项的点击操作。

**参数:**

- `player` (`IPlayer`) - 点击该选项的玩家。

**返回值:** `ValueTask` - 一个表示异步操作的任务。

**用法示例:**
```csharp
await menuOption.OnClickAsync(player);
```

