<a id="imenuapi"></a>

# 🔌 IMenuAPI

表示一个可以向玩家显示的交互式菜单。

**命名空间:** `SwiftlyS2.Shared.Menus`

**类型:** `interface`

**继承:** `IDisposable`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MenuManager` | `IMenuManagerAPI` | get | 该菜单所属的菜单管理器。 |
| `Configuration` | `MenuConfiguration` | get | 本菜单的配置设置。 |
| `KeybindOverrides` | `MenuKeybindOverrides` | get | 本菜单的热键覆盖设置。 |
| `OptionScrollStyle` | `MenuOptionScrollStyle` | get | 此菜单选项的滚动样式。 |
| `Builder` | `IMenuBuilderAPI?` | get | 用于构建和配置此菜单的生成器。 |
| `Tag` | `object?` | get, set | 获取或设置包含此菜单相关数据的对象。 |
| `Options` | `IReadOnlyList\<IMenuOption\>` | get | 此菜单中所有选项的只读集合。 |

## ⚙️ 方法

### ShowForPlayer

```csharp
void ShowForPlayer(IPlayer player)
```

通过显示其内容，向指定玩家展示此菜单。

**参数:**

- `player` (`IPlayer`) - 将看到该菜单的玩家。

**用法示例:**
```csharp
menuAPI.ShowForPlayer(player);
```

### HideForPlayer

```csharp
void HideForPlayer(IPlayer player)
```

通过移除其视觉显示，为该指定玩家隐藏此菜单。

**参数:**

- `player` (`IPlayer`) - 将隐藏菜单的玩家。

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

从该菜单中移除一个选项。

**参数:**

- `option` (`IMenuOption`) - 要移除的菜单选项。

**返回值:** `bool` - 如果选项成功移除则为 true，如果未找到该选项则为 false。

**用法示例:**
```csharp
menuAPI.RemoveOption(existingOption);
```

### MoveToOption

```csharp
bool MoveToOption(IPlayer player, IMenuOption option)
```

将玩家的选择移动到指定选项。

**参数:**

- `player` (`IPlayer`) - 选择进行移动的玩家。
- `option` (`IMenuOption`) - 选择移动的目标选项。

**返回值:** `bool` - 若移动成功则为 true，若选项未找到则为 false。

**用法示例:**
```csharp
bool result = menuApi.MoveToOption(player, option);
```

### MoveToOptionIndex

```csharp
bool MoveToOptionIndex(IPlayer player, int index)
```

将玩家的选择移动至指定的选项索引。

**参数:**

- `player` (`IPlayer`) - 选择进行移动的玩家。
- `index` (`int`) - 要移动选择项的目标选项索引。

**返回值:** `bool` - 如果移动成功则为 true，如果索引越界则为 false。

**用法示例:**
```csharp
var result = menuApi.MoveToOptionIndex(player, 2);
```

### GetCurrentOption

```csharp
IMenuOption? GetCurrentOption(IPlayer player)
```

获取指定玩家当前高亮的菜单选项。

**参数:**

- `player` (`IPlayer`) - 获取当前选中状态的玩家。

**返回值:** `IMenuOption?` - 当前选中的选项，若未选中任何内容则为 null。

**用法示例:**
```csharp
var currentOption = menuAPI.GetCurrentOption(player);
```

### GetCurrentOptionIndex

```csharp
int GetCurrentOptionIndex(IPlayer player)
```

获取指定玩家当前高亮选项的索引。

**参数:**

- `player` (`IPlayer`) - 需要获取其当前选择索引的玩家。

**返回值:** `int` - 当前选中选项的索引，如果未选择任何项则为 -1。

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

