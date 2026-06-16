<a id="menuoptionbase"></a>

# 📦 MenuOptionBase

为具有事件驱动行为的菜单选项提供基础实现。

**命名空间:** `SwiftlyS2.Core.Menus.OptionsBase`

**类型:** `class`

**继承:** `IMenuOption`

**实现接口:** `IDisposable`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Menu` | `IMenuAPI?` | get, set | 获取或设置此选项所属的菜单。 |
| `LineCount` | `int` | - | 获取此选项在菜单中请求占用的行数。 |
| `BindingText` | `Func\<string?\>?` | - | 获取或设置一个动态提供此菜单选项文本内容的函数。 |
| `Text` | `string` | - | 获取或设置为此菜单选项显示的文本内容。 |
| `Comment` | `string` | get, set | 获取或设置为此菜单选项显示的评论内容。 |
| `MaxWidth` | `float` | - | 菜单选项文本的最大显示宽度（相对单位）。 |
| `Visible` | `bool` | - | 获取或设置一个值，该值指示此选项在菜单中是否可见。 |
| `Enabled` | `bool` | - | 获取或设置一个值，该值指示此选项是否可交互。 |
| `CloseAfterClick` | `bool` | get | 获取或设置一个值，指示处理点击后是否应关闭菜单。 |
| `Tag` | `object?` | get, set | 获取或设置一个包含此选项相关数据的对象。 |
| `TextSize` | `MenuOptionTextSize` | get, set | 获取或设置此选项的文本大小。 |
| `TextStyle` | `MenuOptionTextStyle` | - | 获取或设置此选项的文本溢出样式。 |
| `PlaySound` | `bool` | get, set | 获取或设置一个值，该值指示选择此选项时是否应播放声音。 |

## ⚙️ 方法

### Dispose

```csharp
void Dispose()
```

**注意:** 此方法是虚方法,可以在子类中重写 (override).

### PauseTextAnimation

```csharp
void PauseTextAnimation()
```

暂停动态文本动画。

**注意:** 此方法是虚方法,可以在子类中重写 (override).

### ResumeTextAnimation

```csharp
void ResumeTextAnimation()
```

恢复动态文本动画。

**注意:** 此方法是虚方法,可以在子类中重写 (override).

### GetFormattedHtmlText

```csharp
string GetFormattedHtmlText(IPlayer player)
```

**参数:**

- `player` (`IPlayer`)

**返回值:** `string`

**注意:** 此方法是虚方法,可以在子类中重写 (override).

### GetDisplayText

```csharp
string GetDisplayText(IPlayer player, int displayLine = 0)
```

获取此选项的显示文本，如同面向指定玩家应显示的内容。

**参数:**

- `player` (`IPlayer`) - 请求显示文本的玩家。
- `displayLine` (`int`) = `0` - 选项的显示行索引。

**返回值:** `string` - 选项的格式化显示文本。

**注意:** 此方法是虚方法,可以在子类中重写 (override).

### OnValidatingAsync

```csharp
ValueTask<bool> OnValidatingAsync(IPlayer player)
```

验证指定的玩家是否能够与此选项交互。

**参数:**

- `player` (`IPlayer`) - 要验证的玩家。

**返回值:** `ValueTask\<bool\>` - 一个表示异步操作的任务。如果验证成功，任务结果为true；否则为false。

**注意:** 此方法是虚方法,可以在子类中重写 (override).

### OnClickAsync

```csharp
ValueTask OnClickAsync(IPlayer player, bool closeMenu = false)
```

**参数:**

- `player` (`IPlayer`)
- `closeMenu` (`bool`) = `false`

**返回值:** `ValueTask`

**注意:** 此方法是虚方法,可以在子类中重写 (override).

### OnClickAsync

```csharp
ValueTask OnClickAsync(IPlayer player)
```

处理此选项的点击动作。

**参数:**

- `player` (`IPlayer`) - 点击该选项的玩家。

**返回值:** `ValueTask` - 表示异步操作的任务。

**注意:** 此方法是虚方法,可以在子类中重写 (override).

