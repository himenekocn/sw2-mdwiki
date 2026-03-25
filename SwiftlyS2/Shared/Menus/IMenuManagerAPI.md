# 🔌 IMenuManagerAPI

用于创建和控制所有玩家菜单的中心管理器。

**命名空间:** `SwiftlyS2.Shared.Menus`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Core` | `ISwiftlyCore` | get | SwiftlyS2 的核心实例。 |
| `Configuration` | `MenuManagerConfiguration` | get | 所有菜单的全局配置设置。 |

## ⚙️ 方法

### CreateBuilder

```csharp
IMenuBuilderAPI CreateBuilder()
```

创建一个新的菜单构建器。

**返回值:** `IMenuBuilderAPI` - 一个新的菜单构建器实例。

**用法示例:**
```csharp
var builder = menuManager.CreateBuilder();
```

### CreateMenu

```csharp
IMenuAPI CreateMenu(MenuConfiguration configuration, MenuKeybindOverrides keybindOverrides, IMenuAPI? parent = null, MenuOptionScrollStyle optionScrollStyle = MenuOptionScrollStyle.CenterFixed, MenuOptionTextStyle optionTextStyle = MenuOptionTextStyle.TruncateEnd)
```

创建一个带有可选标题的新菜单。

**参数:**

- `configuration` (`MenuConfiguration`) - 菜单的配置。
- `keybindOverrides` (`MenuKeybindOverrides`) - 菜单的按键绑定覆盖。
- `parent` (`IMenuAPI?`) = `null` - 父菜单，若无父菜单则为 null。
- `optionScrollStyle` (`MenuOptionScrollStyle`) = `MenuOptionScrollStyle.CenterFixed` - 菜单选项的滚动样式。
- `optionTextStyle` (`MenuOptionTextStyle`) = `MenuOptionTextStyle.TruncateEnd` - 菜单选项的文本溢出样式。

**返回值:** `IMenuAPI` - 一个已准备好进行配置的新菜单实例。

**用法示例:**
```csharp
var menu = manager.CreateMenu(config, overrides, null, MenuOptionScrollStyle.Default, MenuOptionTextStyle.Plain);
```

### GetCurrentMenu

```csharp
IMenuAPI? GetCurrentMenu(IPlayer player)
```

获取指定玩家当前打开的菜单。

**参数:**

- `player` (`IPlayer`) - 待检查的玩家。

**返回值:** `IMenuAPI?` - 玩家当前激活的菜单，若未打开任何菜单则为 null。

**用法示例:**
```csharp
var currentMenu = menuManager.GetCurrentMenu(player);
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
menuManager.OpenMenu(mainMenu);
```

### OpenMenu

```csharp
void OpenMenu(IMenuAPI menu, Action<IPlayer, IMenuAPI> onClosed)
```

为所有玩家打开指定的菜单。

**参数:**

- `menu` (`IMenuAPI`) - 要显示的菜单。
- `onClosed` (`Action\<IPlayer, IMenuAPI\>`) - 菜单关闭时调用的回调。

**用法示例:**
```csharp
manager.OpenMenu(menu, (player, m) => player.Print("Menu closed"));
```

### OpenMenuForPlayer

```csharp
void OpenMenuForPlayer(IPlayer player, IMenuAPI menu)
```

为指定玩家打开指定的菜单。首先将关闭任何当前已打开的菜单。

**参数:**

- `player` (`IPlayer`) - 将看到该菜单的玩家。
- `menu` (`IMenuAPI`) - 要显示的菜单。

**用法示例:**
```csharp
manager.OpenMenuForPlayer(player, menu);
```

### OpenMenuForPlayer

```csharp
void OpenMenuForPlayer(IPlayer player, IMenuAPI menu, Action<IPlayer, IMenuAPI> onClosed)
```

为指定玩家打开指定的菜单。首先将关闭任何当前已打开的菜单。

**参数:**

- `player` (`IPlayer`) - 将看到该菜单的玩家。
- `menu` (`IMenuAPI`) - 要显示的菜单。
- `onClosed` (`Action\<IPlayer, IMenuAPI\>`) - 当玩家的菜单关闭时调用的回调。

**用法示例:**
```csharp
manager.OpenMenuForPlayer(player, menu, (p, m) => { });
```

### CloseMenu

```csharp
void CloseMenu(IMenuAPI menu)
```

关闭所有拥有该菜单的玩家的指定菜单。

**参数:**

- `menu` (`IMenuAPI`) - 关闭菜单。

**用法示例:**
```csharp
manager.CloseMenu(menu);
```

### CloseMenuForPlayer

```csharp
void CloseMenuForPlayer(IPlayer player, IMenuAPI menu)
```

关闭指定玩家的菜单。如果该玩家未打开此菜单，则不会产生任何效果。

**参数:**

- `player` (`IPlayer`) - 即将关闭菜单的玩家。
- `menu` (`IMenuAPI`) - 关闭菜单。

**用法示例:**
```csharp
manager.CloseMenuForPlayer(player, menu);
```

### CloseActiveMenu

```csharp
void CloseActiveMenu(IPlayer player)
```

关闭玩家当前的菜单。如果玩家未打开任何菜单，则此操作无效。

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

关闭所有玩家的所有打开菜单。

**用法示例:**
```csharp
manager.CloseAllMenus();
```

