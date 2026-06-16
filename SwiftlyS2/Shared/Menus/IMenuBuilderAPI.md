<a id="imenubuilderapi"></a>

# 🔌 IMenuBuilderAPI

为创建和配置菜单提供流畅的构建器接口。所有方法均支持链式调用，便于进行菜单构建。

**命名空间:** `SwiftlyS2.Shared.Menus`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Design` | `IMenuDesignAPI` | get | 获取此菜单的设计界面。 |

## ⚙️ 方法

### BindToParent

```csharp
IMenuBuilderAPI BindToParent(IMenuAPI parent)
```

将此菜单绑定到父菜单，以创建层级导航结构。

**参数:**

- `parent` (`IMenuAPI`) - 父级菜单

**返回值:** `IMenuBuilderAPI` - 此构建器用于方法链式调用。

**用法示例:**
```csharp
menuBuilder.BindToParent(parentMenu);
```

### AddOption

```csharp
IMenuBuilderAPI AddOption(IMenuOption option)
```

向菜单添加一个菜单选项。

**参数:**

- `option` (`IMenuOption`) - 要添加的菜单选项。

**返回值:** `IMenuBuilderAPI` - 此构建器用于方法链式调用。

**用法示例:**
```csharp
menuBuilder.AddOption(existingOption);
```

### EnableSound

```csharp
IMenuBuilderAPI EnableSound()
```

为菜单交互启用音效。

**返回值:** `IMenuBuilderAPI` - 此构建器用于方法链式调用。

**用法示例:**
```csharp
menuBuilder.EnableSound();
```

### DisableSound

```csharp
IMenuBuilderAPI DisableSound()
```

禁用菜单交互的音效。

**返回值:** `IMenuBuilderAPI` - 此构建器用于方法链式调用。

**用法示例:**
```csharp
menuBuilder.DisableSound();
```

### EnableExit

```csharp
IMenuBuilderAPI EnableExit()
```

为此菜单启用退出按钮。

**返回值:** `IMenuBuilderAPI` - 此构建器用于方法链式调用。

**用法示例:**
```csharp
menuBuilder.EnableExit();
```

### DisableExit

```csharp
IMenuBuilderAPI DisableExit()
```

禁用此菜单的退出按钮。

**返回值:** `IMenuBuilderAPI` - 此构建器用于方法链式调用。

**用法示例:**
```csharp
menuBuilder.DisableExit();
```

### SetPlayerFrozen

```csharp
IMenuBuilderAPI SetPlayerFrozen(bool frozen = false)
```

控制菜单打开时玩家移动是否被冻结。

**参数:**

- `frozen` (`bool`) = `false` - 真：冻结玩家移动，假：允许移动。默认为假。

**返回值:** `IMenuBuilderAPI` - 此构建器用于方法链式调用。

**用法示例:**
```csharp
menuBuilder.SetPlayerFrozen(true);
```

### SetAutoCloseDelay

```csharp
IMenuBuilderAPI SetAutoCloseDelay(float seconds = 0f)
```

设置菜单的自动关闭延迟。

**参数:**

- `seconds` (`float`) = `0f` - 菜单自动关闭前的秒数。设为0可禁用自动关闭。默认值为0。

**返回值:** `IMenuBuilderAPI` - 此构建器用于方法链式调用。

**用法示例:**
```csharp
menuBuilder.SetAutoCloseDelay(5.0f);
```

### SetSelectButton

```csharp
IMenuBuilderAPI SetSelectButton(KeyBind keyBind)
```

覆盖选择菜单选项的默认键绑定。

**参数:**

- `keyBind` (`KeyBind`) - 要使用的键位绑定。

**返回值:** `IMenuBuilderAPI` - 此构建器用于方法链式调用。

**用法示例:**
```csharp
menuBuilder.SetSelectButton(KeyBind.Enter);
```

### SetMoveForwardButton

```csharp
IMenuBuilderAPI SetMoveForwardButton(KeyBind keyBind)
```

覆盖通过菜单选项前进的默认按键绑定。

**参数:**

- `keyBind` (`KeyBind`) - 要使用的键位绑定。

**返回值:** `IMenuBuilderAPI` - 此构建器用于方法链式调用。

**用法示例:**
```csharp
menuBuilder.SetMoveForwardButton(KeyBind.W);
```

### SetMoveBackwardButton

```csharp
IMenuBuilderAPI SetMoveBackwardButton(KeyBind keyBind)
```

覆盖菜单选项中向后移动的默认按键绑定。

**参数:**

- `keyBind` (`KeyBind`) - 要使用的键位绑定。

**返回值:** `IMenuBuilderAPI` - 此构建器用于方法链式调用。

**用法示例:**
```csharp
menuBuilder.SetMoveBackwardButton(KeyBind.S);
```

### SetExitButton

```csharp
IMenuBuilderAPI SetExitButton(KeyBind keyBind)
```

覆盖关闭菜单的默认按键绑定。

**参数:**

- `keyBind` (`KeyBind`) - 要使用的键位绑定。

**返回值:** `IMenuBuilderAPI` - 此构建器用于方法链式调用。

**用法示例:**
```csharp
menuBuilder.SetExitButton(KeyBind.Escape);
```

### AddExtraButton

```csharp
IMenuBuilderAPI AddExtraButton(KeyBind keyBind, string label, Action<IPlayer, IMenuAPI> action)
```

在菜单中添加一个额外的按钮，按下时执行自定义操作。

**参数:**

- `keyBind` (`KeyBind`) - 此按钮的键位绑定。
- `label` (`string`) - 菜单底部中此按钮显示的标签。
- `action` (`Action\<IPlayer, IMenuAPI\>`) - 当按钮被按下时执行的动作。

**返回值:** `IMenuBuilderAPI` - 此构建器用于方法链式调用。

**用法示例:**
```csharp
menuBuilder.AddExtraButton(KeyBind.E, "Confirm", (player, menu) => player.PrintToChat("Confirmed"));
```

### Build

```csharp
IMenuAPI Build()
```

构建菜单并返回最终的菜单实例。

**返回值:** `IMenuAPI` - 构建的菜单实例。

**用法示例:**
```csharp
var menu = builder.Build();
```

