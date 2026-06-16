<a id="selectormenuoption-t"></a>

# 📦 SelectorMenuOption&lt;T&gt;

表示一个选择器菜单选项，允许使用左/右键在选项列表中循环切换。显示格式为：标签：前一项 [当前项] 后一项。该选项会占用退出键和使用键，分别用于选择上一个和下一个选项。

**命名空间:** `SwiftlyS2.Core.Menus.OptionsBase`

**类型:** `class`

**继承:** `MenuOptionBase`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Choices` | `IReadOnlyList\<T\>` | get | 获取此选择器的可用选项。 |
| `WrapAround` | `bool` | get, set | 获取或设置选择器在到达末尾时是否应循环。 |

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
selectorMenuOption.PauseTextAnimation();
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
```

### GetSelectedIndex

```csharp
int GetSelectedIndex(IPlayer player)
```

获取指定玩家当前选择的索引。

**参数:**

- `player` (`IPlayer`) - 要检索其选择的玩家。

**返回值:** `int` - 选定的索引。

**用法示例:**
```csharp
int selectedIndex = selectorMenuOption.GetSelectedIndex(player);
```

### GetSelectedChoice

```csharp
T? GetSelectedChoice(IPlayer player)
```

获取指定玩家当前选中的选项。

**参数:**

- `player` (`IPlayer`) - 要检索其选择的玩家。

**返回值:** `T?` - 选定的选项，若无可用选项则为默认值。

**用法示例:**
```csharp
var selectedChoice = selectorMenuOption.GetSelectedChoice(player);
```

### SetSelectedIndex

```csharp
void SetSelectedIndex(IPlayer player, int index)
```

为指定玩家设置已选索引。

**参数:**

- `player` (`IPlayer`) - 要设置其选择的玩家。
- `index` (`int`) - 要选择的索引。将被限制在有效范围内。

**用法示例:**
```csharp
selectorMenuOption.SetSelectedIndex(player, 0);
```

