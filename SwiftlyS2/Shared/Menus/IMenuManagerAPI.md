# 🔌 IMenuManagerAPI

用于创建和控制所有玩家菜单的中央管理器。

**命名空间:** `SwiftlyS2.Shared.Menus`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Core` | `ISwiftlyCore` | get | SwiftlyS2 核心实例。 |
| `Configuration` | `MenuManagerConfiguration` | get | 所有菜单的全局配置设置。 |

## ⚙️ 方法

### CreateBuilder

```csharp
IMenuBuilderAPI CreateBuilder()
```

创建一个新的菜单生成器。

**返回值:** `IMenuBuilderAPI` - 一个新的菜单构建器实例。

**用法示例:**
```csharp
IMenuBuilderAPI builder = manager.CreateBuilder();
```

### CreateMenu

```csharp
IMenuAPI CreateMenu(MenuConfiguration configuration, MenuKeybindOverrides keybindOverrides, IMenuAPI? parent = null, MenuOptionScrollStyle optionScrollStyle = MenuOptionScrollStyle.CenterFixed, MenuOptionTextStyle optionTextStyle = MenuOptionTextStyle.TruncateEnd)
```

创建一个带有可选标题的新菜单。

**参数:**

- `configuration` (`MenuConfiguration`) - 菜单的配置。
- `keybindOverrides` (`MenuKeybindOverrides`) - 菜单的按键绑定覆盖。
- `parent` (`IMenuAPI?`) = `null` - 父菜单，或无父菜单时为 null。
- `optionScrollStyle` (`MenuOptionScrollStyle`) = `MenuOptionScrollStyle.CenterFixed` - 菜单选项的滚动样式。
- `optionTextStyle` (`MenuOptionTextStyle`) = `MenuOptionTextStyle.TruncateEnd` - 菜单选项的文本溢出样式。

**返回值:** `IMenuAPI` - 一个已准备就绪、等待配置的新菜单实例。

**用法示例:**
```csharp
manager.CreateMenu(config, keybinds, parentMenu, MenuOptionScrollStyle.Value, MenuOptionTextStyle.Value);
```

### GetCurrentMenu

```csharp
IMenuAPI? GetCurrentMenu(IPlayer player)
```

获取为指定玩家当前打开的菜单。

**参数:**

- `player` (`IPlayer`) - 要检查的玩家。

**返回值:** `IMenuAPI?` - 玩家当前激活的菜单，如果他们没有打开任何菜单，则为 null。

**用法示例:**
```csharp
IMenuAPI? currentMenu = manager.GetCurrentMenu(player);
```

### OpenMenu

```csharp
void OpenMenu(IMenuAPI menu)
```

为所有玩家打开指定的菜单。

**参数:**

- `menu` (`IMenuAPI`) - 要显示的菜单。

**用法示例:**
```csharp
menuManager.OpenMenu(Menu.Main);
```

### OpenMenu

```csharp
void OpenMenu(IMenuAPI menu, Action<IPlayer, IMenuAPI> onClosed)
```

为所有玩家打开指定的菜单。

**参数:**

- `menu` (`IMenuAPI`) - 要显示的菜单。
- `onClosed` (`Action\<IPlayer, IMenuAPI\>`) - 当菜单关闭时调用的回调。

**用法示例:**
```csharp
manager.OpenMenu(menu, (player, menu) => Console.WriteLine("Menu closed"));
```

### OpenMenuForPlayer

```csharp
void OpenMenuForPlayer(IPlayer player, IMenuAPI menu)
```

为玩家打开指定的菜单。任何当前已打开的菜单将首先被关闭。

**参数:**

- `player` (`IPlayer`) - 将看到此菜单的玩家。
- `menu` (`IMenuAPI`) - 要显示的菜单。

**用法示例:**
```csharp
manager.OpenMenuForPlayer(player, menu);
```

### OpenMenuForPlayer

```csharp
void OpenMenuForPlayer(IPlayer player, IMenuAPI menu, Action<IPlayer, IMenuAPI> onClosed)
```

为玩家打开指定的菜单。任何当前已打开的菜单将首先被关闭。

**参数:**

- `player` (`IPlayer`) - 将看到此菜单的玩家。
- `menu` (`IMenuAPI`) - 要显示的菜单。
- `onClosed` (`Action\<IPlayer, IMenuAPI\>`) - 当为玩家关闭菜单时调用的回调。

**用法示例:**
```csharp
manager.OpenMenuForPlayer(player, mainMenu, (p, m) => Console.WriteLine("菜单已关闭"));
```

### CloseMenu

```csharp
void CloseMenu(IMenuAPI menu)
```

为所有已打开该菜单的玩家关闭指定的菜单。

**参数:**

- `menu` (`IMenuAPI`) - 要关闭的菜单。

**用法示例:**
```csharp
manager.CloseMenu(menu);
```

### CloseMenuForPlayer

```csharp
void CloseMenuForPlayer(IPlayer player, IMenuAPI menu)
```

为玩家关闭指定的菜单。如果该菜单未为该玩家打开，则此操作无效。

**参数:**

- `player` (`IPlayer`) - 其菜单将被关闭的玩家。
- `menu` (`IMenuAPI`) - 要关闭的菜单。

**用法示例:**
```csharp
manager.CloseMenuForPlayer(player, menu);
```

### CloseActiveMenu

```csharp
void CloseActiveMenu(IPlayer player)
```

关闭玩家当前打开的菜单。如果玩家没有打开任何菜单，则此操作无效。

**参数:**

- `player` (`IPlayer`) - 其活动菜单将被关闭的玩家。

**用法示例:**
```csharp
manager.CloseActiveMenu(player);
```

### CloseAllMenus

```csharp
void CloseAllMenus()
```

为每个玩家关闭所有已打开的菜单。

**用法示例:**
```csharp
manager.CloseAllMenus();
```

