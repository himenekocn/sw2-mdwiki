# 📦 ChoiceMenuOption

表示一个在一系列选项中循环切换的菜单选项。

**命名空间:** `SwiftlyS2.Core.Menus.OptionsBase`

**类型:** `class`

**继承:** `MenuOptionBase`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Choices` | `IReadOnlyList\<string\>` | - | 获取可用选项的只读列表。 |

## ⚙️ 方法

### GetDisplayText

```csharp
string GetDisplayText(IPlayer player, int displayLine = 0)
```

**参数:**

- `player` (`IPlayer`)
- `displayLine` (`int`) = `0`

**返回值:** `string`

**用法示例:**
```csharp
string text = choiceMenuOption.GetDisplayText(player, 0);
```

### GetSelectedChoice

```csharp
string GetSelectedChoice(IPlayer player)
```

获取指定玩家的当前选定选项。

**参数:**

- `player` (`IPlayer`) - 要检索其已选择选项的玩家。

**返回值:** `string` - 当前选中的选项字符串。

**用法示例:**
```csharp
string selected = choiceMenuOption.GetSelectedChoice(player);
```

### SetSelectedChoice

```csharp
void SetSelectedChoice(IPlayer player, string choice)
```

为指定玩家设置所选选项。

**参数:**

- `player` (`IPlayer`) - 要设置选择的玩家。
- `choice` (`string`) - 要选择的选项。必须存在于 <see cref="Choices"/> 列表中。

**用法示例:**
```csharp
choiceMenuOption.SetSelectedChoice(player, "OptionA");
```

