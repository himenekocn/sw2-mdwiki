<a id="imenuapi"></a>

# 🔌 IMenuAPI

表示一个可向玩家显示的交互式菜单。

**命名空间:** `SwiftlyS2.Shared.Menus`

**类型:** `interface`

**继承:** `IDisposable`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MenuManager` | `IMenuManagerAPI` | get | 此菜单所属的菜单管理器。 |
| `Configuration` | `MenuConfiguration` | get | 此菜单的配置设置。 |
| `KeybindOverrides` | `MenuKeybindOverrides` | get | 此菜单的按键绑定覆盖设置。 |
| `OptionScrollStyle` | `MenuOptionScrollStyle` | get | 此菜单选项的滚动样式。 |
| `Builder` | `IMenuBuilderAPI?` | get | 用于构建和配置此菜单的构建器。 |
| `Tag` | `object?` | get, set | 获取或设置包含此菜单数据的对象。 |
| `Options` | `IReadOnlyList\<IMenuOption\>` | get | 此菜单中所有选项的只读集合。 |

## ⚙️ 方法

### ShowForPlayer

```csharp
void ShowForPlayer(IPlayer player)
```

向指定玩家显示此菜单，通过展示其内容。

**参数:**

- `player` (`IPlayer`) - 将看到菜单的玩家。

**用法示例:**
```csharp
menuAPI.ShowForPlayer(player);
```

### HideForPlayer

```csharp
void HideForPlayer(IPlayer player)
```

通过移除其视觉显示，为指定玩家隐藏此菜单。

**参数:**

- `player` (`IPlayer`) - 将隐藏其菜单的玩家。

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
menu.AddOption(existingOption);
```

### RemoveOption

```csharp
bool RemoveOption(IMenuOption option)
```

从此菜单中移除一个选项。

**参数:**

- `option` (`IMenuOption`) - 要移除的菜单选项。

**返回值:** `bool` - 如果选项成功移除则为真，如果未找到该选项则为假。

**用法示例:**
```csharp
bool result = menuAPI.RemoveOption(existingOption);
```

### MoveToOption

```csharp
bool MoveToOption(IPlayer player, IMenuOption option)
```

将玩家的选择移动到指定选项。

**参数:**

- `player` (`IPlayer`) - 要移动的选中的玩家。
- `option` (`IMenuOption`) - 将选择项移动到的选项。

**返回值:** `bool` - 如果移动成功则为真，如果未找到选项则为假。

**用法示例:**
```csharp
menuAPI.MoveToOption(player, selectedOption);
```

### MoveToOptionIndex

```csharp
bool MoveToOptionIndex(IPlayer player, int index)
```

将玩家选择移动到指定的选项索引。

**参数:**

- `player` (`IPlayer`) - 要移动的选中的玩家。
- `index` (`int`) - 要将选项移动到的索引。

**返回值:** `bool` - 如果移动成功则为真，如果索引越界则为假。

**用法示例:**
```csharp
menuAPI.MoveToOptionIndex(player, 2);
```

### GetCurrentOption

```csharp
IMenuOption? GetCurrentOption(IPlayer player)
```

获取指定玩家当前高亮的菜单选项。

**参数:**

- `player` (`IPlayer`) - 要检索的当前选中玩家。

**返回值:** `IMenuOption?` - 当前选中的选项，若未选中任何项则为 null。

**用法示例:**
```csharp
IMenuOption? currentOption = menuApi.GetCurrentOption(player);
```

### GetCurrentOptionIndex

```csharp
int GetCurrentOptionIndex(IPlayer player)
```

获取指定玩家当前高亮选项的索引。

**参数:**

- `player` (`IPlayer`) - 要检索其当前选择索引的玩家。

**返回值:** `int` - 当前所选选项的索引，如果未选择任何选项则为 -1。

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
int line = menuAPI.GetCurrentOptionDisplayLine(player);
```

