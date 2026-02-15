# 🔌 IMenuBuilderAPI

提供用于创建和配置菜单的流式构建器接口。所有方法均支持链式调用，以便于菜单的构建。

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

将此菜单绑定到父菜单，从而创建分层导航结构。

**参数:**

- `parent` (`IMenuAPI`) - 父菜单。

**返回值:** `IMenuBuilderAPI` - 用于方法链的构建器。

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

**返回值:** `IMenuBuilderAPI` - 用于方法链的构建器。

**用法示例:**
```csharp
menuBuilder.AddOption(GameOption.Start);
```

### EnableSound

```csharp
IMenuBuilderAPI EnableSound()
```

为菜单交互启用音效。

**返回值:** `IMenuBuilderAPI` - 用于方法链的构建器。

**用法示例:**
```csharp
menuBuilder.EnableSound();
```

### DisableSound

```csharp
IMenuBuilderAPI DisableSound()
```

禁用菜单交互的音效。

**返回值:** `IMenuBuilderAPI` - 用于方法链的构建器。

**用法示例:**
```csharp
menuBuilder.DisableSound();
```

### EnableExit

```csharp
IMenuBuilderAPI EnableExit()
```

为该菜单启用退出按钮。

**返回值:** `IMenuBuilderAPI` - 用于方法链的构建器。

**用法示例:**
```csharp
menuBuilder.EnableExit();
```

### DisableExit

```csharp
IMenuBuilderAPI DisableExit()
```

禁用此菜单的退出按钮。

**返回值:** `IMenuBuilderAPI` - 用于方法链的构建器。

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

- `frozen` (`bool`) = `false` - true表示冻结玩家移动，false表示允许移动。默认值为false。

**返回值:** `IMenuBuilderAPI` - 用于方法链的构建器。

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

- `seconds` (`float`) = `0f` - 菜单自动关闭前的时间（以秒为单位）。设置为 0 可禁用自动关闭。默认值为 0。

**返回值:** `IMenuBuilderAPI` - 用于方法链的构建器。

**用法示例:**
```csharp
menuBuilder.SetAutoCloseDelay(2.0f);
```

### SetSelectButton

```csharp
IMenuBuilderAPI SetSelectButton(KeyBind keyBind)
```

重写用于选择菜单选项的默认键绑定。

**参数:**

- `keyBind` (`KeyBind`) - 要使用的键绑定。

**返回值:** `IMenuBuilderAPI` - 用于方法链的构建器。

**用法示例:**
```csharp
menuBuilder.SetSelectButton(KeyBind.Value);
```

### SetMoveForwardButton

```csharp
IMenuBuilderAPI SetMoveForwardButton(KeyBind keyBind)
```

覆盖用于在菜单选项中向前移动的默认键绑定。

**参数:**

- `keyBind` (`KeyBind`) - 要使用的键绑定。

**返回值:** `IMenuBuilderAPI` - 用于方法链的构建器。

**用法示例:**
```csharp
menuBuilder.SetMoveForwardButton(KeyBind.ArrowUp);
```

### SetMoveBackwardButton

```csharp
IMenuBuilderAPI SetMoveBackwardButton(KeyBind keyBind)
```

重写用于在菜单选项中向后移动的默认键绑定。

**参数:**

- `keyBind` (`KeyBind`) - 要使用的键绑定。

**返回值:** `IMenuBuilderAPI` - 用于方法链的构建器。

**用法示例:**
```csharp
menuBuilder.SetMoveBackwardButton(KeyBind.Backspace);
```

### SetExitButton

```csharp
IMenuBuilderAPI SetExitButton(KeyBind keyBind)
```

覆盖关闭菜单的默认键绑定。

**参数:**

- `keyBind` (`KeyBind`) - 要使用的键绑定。

**返回值:** `IMenuBuilderAPI` - 用于方法链的构建器。

**用法示例:**
```csharp
menuBuilder.SetExitButton(KeyBind.Escape);
```

### AddExtraButton

```csharp
IMenuBuilderAPI AddExtraButton(KeyBind keyBind, string label, Action<IPlayer, IMenuAPI> action)
```

在菜单中添加一个额外的按钮，当按下该按钮时执行自定义操作。

**参数:**

- `keyBind` (`KeyBind`) - 此按钮的键绑定。
- `label` (`string`) - 在菜单页脚中为此按钮显示的标签。
- `action` (`Action\<IPlayer, IMenuAPI\>`) - 当按钮被按下时执行的操作。

**返回值:** `IMenuBuilderAPI` - 用于方法链的构建器。

**用法示例:**
```csharp
menuBuilder.AddExtraButton(KeyBind.F1, "Debug", (player, menu) => Console.WriteLine("F1 pressed"));
```

### Build

```csharp
IMenuAPI Build()
```

构建菜单并返回最终的菜单实例。

**返回值:** `IMenuAPI` - 已构建的菜单实例。

**用法示例:**
```csharp
IMenuAPI menu = builder.Build();
```

