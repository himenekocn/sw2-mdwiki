# 📦 MenuManagerAPI

**命名空间:** `SwiftlyS2.Core.Menus`

**类型:** `class`

**继承:** `IMenuManagerAPI`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `Core` | `ISwiftlyCore` | get, set | The SwiftlyS2 core instance. |
| `Configuration` | `MenuManagerConfiguration` | get, set | Global Configuration settings for all menus. |

## ⚙️ 方法

### CreateBuilder

```csharp
IMenuBuilderAPI CreateBuilder()
```

**返回值:** `IMenuBuilderAPI`

### CreateMenu

```csharp
IMenuAPI CreateMenu(MenuConfiguration configuration, MenuKeybindOverrides keybindOverrides, IMenuAPI? parent = null, MenuOptionScrollStyle optionScrollStyle = MenuOptionScrollStyle.CenterFixed, MenuOptionTextStyle optionTextStyle = MenuOptionTextStyle.TruncateEnd)
```

**参数:**

- `configuration` (`MenuConfiguration`)
- `keybindOverrides` (`MenuKeybindOverrides`)
- `parent` (`IMenuAPI?`) = `null`
- `optionScrollStyle` (`MenuOptionScrollStyle`) = `MenuOptionScrollStyle.CenterFixed`
- `optionTextStyle` (`MenuOptionTextStyle`) = `MenuOptionTextStyle.TruncateEnd`

**返回值:** `IMenuAPI`

### GetCurrentMenu

```csharp
IMenuAPI? GetCurrentMenu(IPlayer player)
```

**参数:**

- `player` (`IPlayer`)

**返回值:** `IMenuAPI?`

### OpenMenu

```csharp
void OpenMenu(IMenuAPI menu)
```

**参数:**

- `menu` (`IMenuAPI`)

### OpenMenu

```csharp
void OpenMenu(IMenuAPI menu, Action<IPlayer, IMenuAPI> onClosed)
```

**参数:**

- `menu` (`IMenuAPI`)
- `onClosed` (`Action\<IPlayer, IMenuAPI\>`)

### OpenMenuForPlayer

```csharp
void OpenMenuForPlayer(IPlayer player, IMenuAPI menu)
```

**参数:**

- `player` (`IPlayer`)
- `menu` (`IMenuAPI`)

### OpenMenuForPlayer

```csharp
void OpenMenuForPlayer(IPlayer player, IMenuAPI menu, Action<IPlayer, IMenuAPI> onClosed)
```

**参数:**

- `player` (`IPlayer`)
- `menu` (`IMenuAPI`)
- `onClosed` (`Action\<IPlayer, IMenuAPI\>`)

### CloseMenu

```csharp
void CloseMenu(IMenuAPI menu)
```

**参数:**

- `menu` (`IMenuAPI`)

### CloseMenuForPlayer

```csharp
void CloseMenuForPlayer(IPlayer player, IMenuAPI menu)
```

**参数:**

- `player` (`IPlayer`)
- `menu` (`IMenuAPI`)

### CloseActiveMenu

```csharp
void CloseActiveMenu(IPlayer player)
```

**参数:**

- `player` (`IPlayer`)

### CloseAllMenus

```csharp
void CloseAllMenus()
```

