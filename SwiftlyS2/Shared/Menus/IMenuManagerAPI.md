<a id="imenumanagerapi"></a>

# 🔌 IMenuManagerAPI

创建和控制所有玩家菜单的中央管理器。

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

创建一个新的菜单构建器。

**返回值:** `IMenuBuilderAPI` - 一个新的菜单构建器实例。

**用法示例:**
```csharp
var builder = manager.CreateBuilder();
```

### CreateMenu

```csharp
IMenuAPI CreateMenu(MenuConfiguration configuration, MenuKeybindOverrides keybindOverrides, IMenuAPI? parent = null, MenuOptionScrollStyle optionScrollStyle = MenuOptionScrollStyle.CenterFixed, MenuOptionTextStyle optionTextStyle = MenuOptionTextStyle.TruncateEnd)
```

创建一个带有可选标题的新菜单。

**参数:**

- `configuration` (`MenuConfiguration`) - 菜单的配置。
- `keybindOverrides` (`MenuKeybindOverrides`) - 菜单的按键绑定覆盖设置。
- `parent` (`IMenuAPI?`) = `null` - 父菜单，若无则为 null。
- `optionScrollStyle` (`MenuOptionScrollStyle`) = `MenuOptionScrollStyle.CenterFixed` - 菜单选项的滚动样式。
- `optionTextStyle` (`MenuOptionTextStyle`) = `MenuOptionTextStyle.TruncateEnd` - 菜单选项的文本溢出样式。

**返回值:** `IMenuAPI` - 一个已准备好进行配置的新菜单实例。

**用法示例:**
```csharp
var menu = manager.CreateMenu(config, overrides, null, MenuOptionScrollStyle.Default, MenuOptionTextStyle.Default);
```

### GetCurrentMenu

```csharp
IMenuAPI? GetCurrentMenu(IPlayer player)
```

获取指定玩家当前打开的游戏菜单。

**参数:**

- `player` (`IPlayer`) - 要检查的玩家。

**返回值:** `IMenuAPI?` - 玩家的当前活动菜单，如果未打开任何菜单则为 null。

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
menuManager.OpenMenu(menu);
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
menuManager.OpenMenu(menu, (player, m) => {});
```

### OpenMenuForPlayer

```csharp
void OpenMenuForPlayer(IPlayer player, IMenuAPI menu)
```

为指定玩家打开指定菜单。任何当前已打开的菜单将首先被关闭。

**参数:**

- `player` (`IPlayer`) - 将看到菜单的玩家。
- `menu` (`IMenuAPI`) - 要显示的菜单。

**用法示例:**
```csharp
manager.OpenMenuForPlayer(player, menu);
```

### OpenMenuForPlayer

```csharp
void OpenMenuForPlayer(IPlayer player, IMenuAPI menu, Action<IPlayer, IMenuAPI> onClosed)
```

为指定玩家打开指定菜单。任何当前已打开的菜单将首先被关闭。

**参数:**

- `player` (`IPlayer`) - 将看到菜单的玩家。
- `menu` (`IMenuAPI`) - 要显示的菜单。
- `onClosed` (`Action\<IPlayer, IMenuAPI\>`) - 当玩家关闭菜单时回调。

**用法示例:**
```csharp
manager.OpenMenuForPlayer(player, menu, (p, m) => {});
```

### CloseMenu

```csharp
void CloseMenu(IMenuAPI menu)
```

为所有打开了指定菜单的玩家关闭该菜单。

**参数:**

- `menu` (`IMenuAPI`) - 要关闭的菜单。

**用法示例:**
```csharp
menuManager.CloseMenu(menu);
```

### CloseMenuForPlayer

```csharp
void CloseMenuForPlayer(IPlayer player, IMenuAPI menu)
```

关闭指定玩家的菜单。如果该菜单未对该玩家开启，则此操作无效。

**参数:**

- `player` (`IPlayer`) - 将要关闭其菜单的玩家。
- `menu` (`IMenuAPI`) - 要关闭的菜单。

**用法示例:**
```csharp
menuManager.CloseMenuForPlayer(player, menu);
```

### CloseActiveMenu

```csharp
void CloseActiveMenu(IPlayer player)
```

关闭玩家当前打开的菜单。如果玩家未打开任何菜单，则此操作无效。

**参数:**

- `player` (`IPlayer`) - 将关闭其活动菜单的玩家。

**用法示例:**
```csharp
menuManager.CloseActiveMenu(player);
```

### CloseAllMenus

```csharp
void CloseAllMenus()
```

为所有玩家关闭所有打开的菜单。

**用法示例:**
```csharp
menuManager.CloseAllMenus();
```

