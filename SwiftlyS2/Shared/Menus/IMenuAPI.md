# 🔌 IMenuAPI

表示一个可显示给玩家的交互式菜单。

**命名空间:** `SwiftlyS2.Shared.Menus`

**类型:** `interface`

**继承:** `IDisposable`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MenuManager` | `IMenuManagerAPI` | get | 该菜单所属的菜单管理器。 |
| `Configuration` | `MenuConfiguration` | get | 此菜单的配置设置。 |
| `KeybindOverrides` | `MenuKeybindOverrides` | get | 此菜单的按键绑定覆盖。 |
| `OptionScrollStyle` | `MenuOptionScrollStyle` | get | 此菜单选项的滚动样式。 |
| `Builder` | `IMenuBuilderAPI?` | get | 用于构建和配置此菜单的生成器。 |
| `Tag` | `object?` | get, set | 获取或设置一个包含此菜单相关数据的对象。 |
| `Options` | `IReadOnlyList\<IMenuOption\>` | get | 此菜单中所有选项的只读集合。 |

## ⚙️ 方法

### ShowForPlayer

```csharp
void ShowForPlayer(IPlayer player)
```

通过显示其内容，将此菜单展示给指定玩家。

**参数:**

- `player` (`IPlayer`) - 将看到此菜单的玩家。

**用法示例:**
```csharp
menu.ShowForPlayer(player);
```

### HideForPlayer

```csharp
void HideForPlayer(IPlayer player)
```

通过移除其视觉显示，为指定玩家隐藏此菜单。

**参数:**

- `player` (`IPlayer`) - 其菜单将被隐藏的玩家。

**用法示例:**
```csharp
menuAPI.HideForPlayer(player);
```

### AddOption

```csharp
void AddOption(IMenuOption option)
```

向此菜单添加一个新选项。

**参数:**

- `option` (`IMenuOption`) - 要添加的菜单选项。

**用法示例:**
```csharp
menu.AddOption(option);
```

### RemoveOption

```csharp
bool RemoveOption(IMenuOption option)
```

从该菜单中移除一个选项。

**参数:**

- `option` (`IMenuOption`) - 要移除的菜单选项。

**返回值:** `bool` - 如果选项已成功移除，则为 true；如果未找到该选项，则为 false。

**用法示例:**
```csharp
menu.RemoveOption(option);
```

### MoveToOption

```csharp
bool MoveToOption(IPlayer player, IMenuOption option)
```

将玩家的选择移动到指定的选项。

**参数:**

- `player` (`IPlayer`) - 要移动的玩家选择。
- `option` (`IMenuOption`) - 将选择移动到的选项。

**返回值:** `bool` - 如果移动成功，则为 true；如果未找到该选项，则为 false。

**用法示例:**
```csharp
return menuAPI.MoveToOption(player, MenuOption.Start);
```

### MoveToOptionIndex

```csharp
bool MoveToOptionIndex(IPlayer player, int index)
```

将玩家的选择移动到指定的选项索引。

**参数:**

- `player` (`IPlayer`) - 要移动的玩家选择。
- `index` (`int`) - 要将选择移动到的选项的索引。

**返回值:** `bool` - 如果移动成功，则为 true；如果索引超出范围，则为 false。

**用法示例:**
```csharp
menuAPI.MoveToOptionIndex(player, 2);
```

### GetCurrentOption

```csharp
IMenuOption? GetCurrentOption(IPlayer player)
```

获取由指定玩家当前高亮的菜单选项。

**参数:**

- `player` (`IPlayer`) - 要获取其当前选择的玩家。

**返回值:** `IMenuOption?` - 当前选中的选项，如果未选择任何项则为 null。

**用法示例:**
```csharp
IMenuOption? option = menuAPI.GetCurrentOption(player);
```

### GetCurrentOptionIndex

```csharp
int GetCurrentOptionIndex(IPlayer player)
```

获取指定玩家的当前高亮选项的索引。

**参数:**

- `player` (`IPlayer`) - 要获取其当前选择索引的玩家。

**返回值:** `int` - 当前选中选项的索引，如果未选择任何选项则为 -1。

**用法示例:**
```csharp
int index = menuAPI.GetCurrentOptionIndex(player);
```

### GetCurrentOptionDisplayLine

```csharp
int GetCurrentOptionDisplayLine(IPlayer player)
```

**参数:**

- `player` (`IPlayer`)

**返回值:** `int`

**用法示例:**
```csharp
int line = IMenuAPI.GetCurrentOptionDisplayLine(player);
```

