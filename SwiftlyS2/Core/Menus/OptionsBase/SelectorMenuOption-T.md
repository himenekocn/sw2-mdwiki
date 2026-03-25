# 📦 SelectorMenuOption<T>

表示一个选择器菜单选项，允许使用左/右键在选项列表中循环切换。显示格式为：标签: 上一选项 [当前选项] 下一选项。该选项占用“退出”和“使用”键，分别用于执行上一项和下一项的选择操作。

**命名空间:** `SwiftlyS2.Core.Menus.OptionsBase`

**类型:** `class`

**继承:** `MenuOptionBase`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Choices` | `IReadOnlyList\<T\>` | get | 获取此选择器可用的选项。 |
| `WrapAround` | `bool` | get, set | 获取或设置选择器在到达末尾时是否应循环回绕。 |

## ⚙️ 方法

### Dispose

```csharp
void Dispose()
```

### PauseTextAnimation

```csharp
void PauseTextAnimation()
```

**用法示例:**
```csharp
option.PauseTextAnimation();
```

### ResumeTextAnimation

```csharp
void ResumeTextAnimation()
```

**用法示例:**
```csharp
selectorMenuOption.ResumeTextAnimation();
```

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
string text = selectorMenuOption.GetDisplayText(player, 0);
Console.WriteLine(text);
```

### GetSelectedIndex

```csharp
int GetSelectedIndex(IPlayer player)
```

获取指定玩家当前选定的索引。

**参数:**

- `player` (`IPlayer`) - 需要检索其选择的玩家。

**返回值:** `int` - 所选索引。

**用法示例:**
```csharp
int selectedIndex = selectorMenuOption.GetSelectedIndex(player);
```

### GetSelectedChoice

```csharp
T? GetSelectedChoice(IPlayer player)
```

获取指定玩家当前所选的选项。

**参数:**

- `player` (`IPlayer`) - 需要检索其选择的玩家。

**返回值:** `T?` - 选定的选项，若无可用选项则使用默认值。

**用法示例:**
```csharp
var choice = selectorMenuOption.GetSelectedChoice(player);
```

### SetSelectedIndex

```csharp
void SetSelectedIndex(IPlayer player, int index)
```

设置指定玩家的选中索引。

**参数:**

- `player` (`IPlayer`) - 要设置其选择的玩家。
- `index` (`int`) - 用于选择的索引。将被限制在有效范围内。

**用法示例:**
```csharp
selectorMenuOption.SetSelectedIndex(player, 1);
```

