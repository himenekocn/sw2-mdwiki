# 📦 MenuAPI

**命名空间:** `SwiftlyS2.Core.Menus`

**类型:** `class`

**继承:** `IMenuAPI`

**实现接口:** `IDisposable`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `MenuManager` | `IMenuManagerAPI` | get, set | The menu manager that this menu belongs to. |
| `Configuration` | `MenuConfiguration` | get, set | Configuration settings for this menu. |
| `KeybindOverrides` | `MenuKeybindOverrides` | get | Keybind overrides for this menu. |
| `OptionScrollStyle` | `MenuOptionScrollStyle` | get | The scroll style for this menu options. |
| `Builder` | `IMenuBuilderAPI?` | get, set | The builder used to construct and configure this menu. |
| `Tag` | `object?` | get, set | Gets or sets an object that contains data about this menu. |
| `Options` | `IReadOnlyList\<IMenuOption\>` | get | Read-only collection of all options in this menu. |

## ⚙️ 方法

### Dispose

```csharp
void Dispose()
```

### ShowForPlayer

```csharp
void ShowForPlayer(IPlayer player)
```

**参数:**

- `player` (`IPlayer`)

### HideForPlayer

```csharp
void HideForPlayer(IPlayer player)
```

**参数:**

- `player` (`IPlayer`)

### AddOption

```csharp
void AddOption(IMenuOption option)
```

**参数:**

- `option` (`IMenuOption`)

### RemoveOption

```csharp
bool RemoveOption(IMenuOption option)
```

**参数:**

- `option` (`IMenuOption`)

**返回值:** `bool`

### MoveToOption

```csharp
bool MoveToOption(IPlayer player, IMenuOption option)
```

**参数:**

- `player` (`IPlayer`)
- `option` (`IMenuOption`)

**返回值:** `bool`

### MoveToOptionIndex

```csharp
bool MoveToOptionIndex(IPlayer player, int index)
```

**参数:**

- `player` (`IPlayer`)
- `index` (`int`)

**返回值:** `bool`

### GetCurrentOption

```csharp
IMenuOption? GetCurrentOption(IPlayer player)
```

**参数:**

- `player` (`IPlayer`)

**返回值:** `IMenuOption?`

### GetCurrentOptionIndex

```csharp
int GetCurrentOptionIndex(IPlayer player)
```

**参数:**

- `player` (`IPlayer`)

**返回值:** `int`

