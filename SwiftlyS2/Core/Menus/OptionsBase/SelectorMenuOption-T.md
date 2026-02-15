# 📦 SelectorMenuOption<T>

表示一个选择器菜单选项，允许使用左右键循环浏览一系列选项。显示为：标签：上一个选项 [当前选项] 下一个选项。此选项分别将“退出”和“使用”键用于上一个和下一个选择。

**命名空间:** `SwiftlyS2.Core.Menus.OptionsBase`

**类型:** `class`

**继承:** `MenuOptionBase`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Choices` | `IReadOnlyList\<T\>` | get | 获取此选择器的可用选项。 |
| `WrapAround` | `bool` | get, set | 获取或设置当到达末尾时选择器是否应循环。 |

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

获取指定玩家的当前选定索引。

**参数:**

- `player` (`IPlayer`) - 要检索其选择的玩家。

**返回值:** `int` - 选中的索引。

**用法示例:**
```csharp
int index = selectorMenuOption.GetSelectedIndex(player);
```

### GetSelectedChoice

```csharp
T? GetSelectedChoice(IPlayer player)
```

获取指定玩家的当前选定选项。

**参数:**

- `player` (`IPlayer`) - 要检索其选择的玩家。

**返回值:** `T?` - 选定的选项，如果无可用选项则返回默认值。

**用法示例:**
```csharp
Team? selected = selectorMenuOption.GetSelectedChoice(player);
```

### SetSelectedIndex

```csharp
void SetSelectedIndex(IPlayer player, int index)
```

为指定玩家设置选定索引。

**参数:**

- `player` (`IPlayer`) - 要设置其选择的玩家。
- `index` (`int`) - 要选择的索引。将被限制在有效范围内。

**用法示例:**
```csharp
selectorMenuOption.SetSelectedIndex(player, 2);
```

