# 🔌 IMenuBuilderAPI

提供一个用于创建和配置菜单的流畅构建器接口。所有方法均支持链式调用，以便于便捷地构建菜单。

**命名空间:** `SwiftlyS2.Shared.Menus`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Design` | `IMenuDesignAPI` | get | 获取此菜单的设计接口。 |

## ⚙️ 方法

### BindToParent

```csharp
IMenuBuilderAPI BindToParent(IMenuAPI parent)
```

将此菜单绑定到父级菜单，以创建分层导航结构。

**参数:**

- `parent` (`IMenuAPI`) - 父级菜单。

**返回值:** `IMenuBuilderAPI` - 此构建器用于方法链式调用。

**用法示例:**
```csharp
menuBuilder.BindToParent(parentMenu);
```

### AddOption

```csharp
IMenuBuilderAPI AddOption(IMenuOption option)
```

向菜单中添加一个选项。

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

启用菜单交互的音效。

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

启用此菜单的退出按钮。

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

控制当菜单打开时是否冻结玩家移动。

**参数:**

- `frozen` (`bool`) = `false` - 为冻结玩家移动设置为 true，允许移动则为 false。默认为 false。

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

- `seconds` (`float`) = `0f` - 菜单自动关闭前的秒数。设置为 0 可禁用自动关闭。默认值为 0。

**返回值:** `IMenuBuilderAPI` - 此构建器用于方法链式调用。

**用法示例:**
```csharp
menuBuilder.SetAutoCloseDelay(5.0f);
```

### SetSelectButton

```csharp
IMenuBuilderAPI SetSelectButton(KeyBind keyBind)
```

重写用于选择菜单选项的默认按键绑定。

**参数:**

- `keyBind` (`KeyBind`) - 要使用的按键绑定。

**返回值:** `IMenuBuilderAPI` - 此构建器用于方法链式调用。

**用法示例:**
```csharp
menuBuilder.SetSelectButton(KeyBind.Enter);
```

### SetMoveForwardButton

```csharp
IMenuBuilderAPI SetMoveForwardButton(KeyBind keyBind)
```

覆盖默认的前进菜单选项按键绑定。

**参数:**

- `keyBind` (`KeyBind`) - 要使用的按键绑定。

**返回值:** `IMenuBuilderAPI` - 此构建器用于方法链式调用。

**用法示例:**
```csharp
menuBuilder.SetMoveForwardButton(KeyBind.W);
```

### SetMoveBackwardButton

```csharp
IMenuBuilderAPI SetMoveBackwardButton(KeyBind keyBind)
```

重写通过菜单选项向后移动的默认按键绑定。

**参数:**

- `keyBind` (`KeyBind`) - 要使用的按键绑定。

**返回值:** `IMenuBuilderAPI` - 此构建器用于方法链式调用。

**用法示例:**
```csharp
menuBuilder.SetMoveBackwardButton(KeyBind.S);
```

### SetExitButton

```csharp
IMenuBuilderAPI SetExitButton(KeyBind keyBind)
```

重写关闭菜单的默认按键绑定。

**参数:**

- `keyBind` (`KeyBind`) - 要使用的按键绑定。

**返回值:** `IMenuBuilderAPI` - 此构建器用于方法链式调用。

**用法示例:**
```csharp
menuBuilder.SetExitButton(KeyBind.Escape);
```

### AddExtraButton

```csharp
IMenuBuilderAPI AddExtraButton(KeyBind keyBind, string label, Action<IPlayer, IMenuAPI> action)
```

向菜单中添加一个额外按钮，该按钮在按下时执行自定义操作。

**参数:**

- `keyBind` (`KeyBind`) - 此按钮的按键绑定。
- `label` (`string`) - 此按钮在菜单页脚中显示的标签。
- `action` (`Action\<IPlayer, IMenuAPI\>`) - 按下按钮时执行的操作。

**返回值:** `IMenuBuilderAPI` - 此构建器用于方法链式调用。

**用法示例:**
```csharp
menuBuilder.AddExtraButton(KeyBind.Value, "Action", (player, menu) => player.Print("Button pressed"));
```

### Build

```csharp
IMenuAPI Build()
```

构建菜单并返回最终的菜单实例。

**返回值:** `IMenuAPI` - 已构建的菜单实例。

**用法示例:**
```csharp
IMenuAPI menu = menuBuilder.Build();
```

