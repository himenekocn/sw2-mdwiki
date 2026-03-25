<a id="imenudesignapi"></a>

# 🔌 IMenuDesignAPI

**命名空间:** `SwiftlyS2.Shared.Menus`

**类型:** `interface`

## ⚙️ 方法

### SetMenuTitle

```csharp
IMenuBuilderAPI SetMenuTitle(string? title = null)
```

设置显示在菜单顶部的标题文本。

**参数:**

- `title` (`string?`) = `null` - 标题文本。传递 null 以清除标题。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuBuilder.SetMenuTitle("服务器菜单");
```

### SetMenuTitleVisible

```csharp
IMenuBuilderAPI SetMenuTitleVisible(bool visible = true)
```

控制菜单标题的可见性。

**参数:**

- `visible` (`bool`) = `true` - True 表示显示标题，false 表示隐藏标题。默认为 true。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuBuilder.SetMenuTitleVisible(true);
```

### SetMenuTitleItemCountVisible

```csharp
IMenuBuilderAPI SetMenuTitleItemCountVisible(bool visible = true)
```

控制菜单标题中物品数量的可见性。

**参数:**

- `visible` (`bool`) = `true` - True 表示显示物品数量，false 表示隐藏。默认值为 true。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignAPI.SetMenuTitleItemCountVisible(true);
```

### SetMenuFooterVisible

```csharp
IMenuBuilderAPI SetMenuFooterVisible(bool visible = true)
```

控制菜单页脚的可见性。

**参数:**

- `visible` (`bool`) = `true` - 设为 true 以显示页脚，设为 false 以隐藏页脚。默认为 true。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuBuilder.SetMenuFooterVisible(true);
```

### SetCommentVisible

```csharp
IMenuBuilderAPI SetCommentVisible(bool visible = true)
```

控制菜单选项注释的可见性。

**参数:**

- `visible` (`bool`) = `true` - 设为 true 以显示评论，设为 false 以隐藏评论。默认为 true。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuBuilder.SetCommentVisible(true);
```

### SetMaxVisibleItems

```csharp
IMenuBuilderAPI SetMaxVisibleItems(int count = 5)
```

设置屏幕上一次性可见的菜单选项的最大数量。

**参数:**

- `count` (`int`) = `5` - 最大可见物品数量。有效范围为 1-5。默认值为 5。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignAPI.SetMaxVisibleItems(5);
```

### EnableAutoAdjustVisibleItems

```csharp
IMenuBuilderAPI EnableAutoAdjustVisibleItems()
```

当标题或页脚被隐藏时，启用可见项的自动调整。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignAPI.EnableAutoAdjustVisibleItems();
```

### DisableAutoAdjustVisibleItems

```csharp
IMenuBuilderAPI DisableAutoAdjustVisibleItems()
```

禁用在隐藏标题或页脚时可见项目的自动调整。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuBuilder.DisableAutoAdjustVisibleItems();
```

### SetGlobalScrollStyle

```csharp
IMenuBuilderAPI SetGlobalScrollStyle(MenuOptionScrollStyle style)
```

为所有菜单选项设置默认滚动动画样式。

**参数:**

- `style` (`MenuOptionScrollStyle`) - 要全局应用的滚动条样式。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignAPI.SetGlobalScrollStyle(MenuOptionScrollStyle.Value);
```

### SetNavigationMarkerColor

```csharp
IMenuBuilderAPI SetNavigationMarkerColor(string? hexColor = null)
```

使用十六进制颜色格式设置导航标记的颜色。

**参数:**

- `hexColor` (`string?`) = `null` - 十六进制格式的颜色（例如，白色的"#FFFFFF"）。传递 null 以重置为默认值。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignAPI.SetNavigationMarkerColor("#FF5733");
```

### SetNavigationMarkerColor

```csharp
IMenuBuilderAPI SetNavigationMarkerColor(Natives.Color color)
```

使用 SwiftlyS2 原生颜色设置导航标记的颜色。

**参数:**

- `color` (`Natives.Color`) - SwiftlyS2 应用于导航标记的原生颜色。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuBuilder.SetNavigationMarkerColor(Natives.Color.Red);
```

### SetNavigationMarkerColor

```csharp
IMenuBuilderAPI SetNavigationMarkerColor(System.Drawing.Color color)
```

使用 System.Drawing 颜色设置导航标记的颜色。

**参数:**

- `color` (`System.Drawing.Color`) - 要应用到导航标记的系统绘制颜色。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuBuilder.SetNavigationMarkerColor(System.Drawing.Color.Blue);
```

### SetMenuFooterColor

```csharp
IMenuBuilderAPI SetMenuFooterColor(string? hexColor = null)
```

使用十六进制颜色格式设置菜单页脚的颜色。

**参数:**

- `hexColor` (`string?`) = `null` - 以十六进制格式表示的颜色（例如，红色的"#FF0000"）。传递 null 可重置为默认值。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuBuilder.SetMenuFooterColor("#FF5733");
```

### SetMenuFooterColor

```csharp
IMenuBuilderAPI SetMenuFooterColor(Natives.Color color)
```

使用 SwiftlyS2 原生颜色设置菜单页脚的颜色。

**参数:**

- `color` (`Natives.Color`) - 要应用于页脚的 SwiftlyS2 原生颜色。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuBuilder.SetMenuFooterColor(Natives.Color.Red);
```

### SetMenuFooterColor

```csharp
IMenuBuilderAPI SetMenuFooterColor(System.Drawing.Color color)
```

使用 System.Drawing 颜色设置菜单页脚的颜色。

**参数:**

- `color` (`System.Drawing.Color`) - 要应用于页脚的系统绘图颜色。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuBuilder.SetMenuFooterColor(System.Drawing.Color.Blue);
```

### SetVisualGuideLineColor

```csharp
IMenuBuilderAPI SetVisualGuideLineColor(string? hexColor = null)
```

使用十六进制颜色格式设置视觉辅助线的颜色。

**参数:**

- `hexColor` (`string?`) = `null` - 十六进制格式的颜色（例如，白色的"#FFFFFF"）。传递 null 以重置为默认值。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuBuilder.SetVisualGuideLineColor("#FF5733");
```

### SetVisualGuideLineColor

```csharp
IMenuBuilderAPI SetVisualGuideLineColor(Natives.Color color)
```

使用 SwiftlyS2 原生颜色设置视觉辅助线的颜色。

**参数:**

- `color` (`Natives.Color`) - 应用于引导线的 SwiftlyS2 原生颜色。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuBuilder.SetVisualGuideLineColor(Natives.Color.Red);
```

### SetVisualGuideLineColor

```csharp
IMenuBuilderAPI SetVisualGuideLineColor(System.Drawing.Color color)
```

使用 System.Drawing 颜色设置视觉引导线的颜色。

**参数:**

- `color` (`System.Drawing.Color`) - 应用于辅助线的 System.Drawing 颜色。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuBuilder.SetVisualGuideLineColor(System.Drawing.Color.Red);
```

### SetDisabledColor

```csharp
IMenuBuilderAPI SetDisabledColor(string? hexColor = null)
```

设置禁用菜单选项的颜色，采用十六进制颜色格式。

**参数:**

- `hexColor` (`string?`) = `null` - 十六进制格式的颜色（例如，灰色的"#808080"）。传入 null 可重置为默认值。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuBuilder.SetDisabledColor("#808080");
```

### SetDisabledColor

```csharp
IMenuBuilderAPI SetDisabledColor(Natives.Color color)
```

使用 SwiftlyS2 原生颜色设置禁用菜单选项的颜色。

**参数:**

- `color` (`Natives.Color`) - 应用于禁用选项的 SwiftlyS2 原生颜色。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuBuilder.SetDisabledColor(Natives.Color.Red);
```

### SetDisabledColor

```csharp
IMenuBuilderAPI SetDisabledColor(System.Drawing.Color color)
```

使用 System.Drawing 颜色设置禁用菜单选项的颜色。

**参数:**

- `color` (`System.Drawing.Color`) - 应用于禁用选项的 System.Drawing 颜色。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuBuilder.SetDisabledColor(System.Drawing.Color.Gray);
```

### SetDefaultComment

```csharp
IMenuBuilderAPI SetDefaultComment(string comment)
```

设置当菜单选项的 Comment 未设置时所使用的默认注释文本。

**参数:**

- `comment` (`string`) - 默认注释文本。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignAPI.SetDefaultComment("默认注释");
```

### SetGlobalOptionTextStyle

```csharp
IMenuBuilderAPI SetGlobalOptionTextStyle(MenuOptionTextStyle style)
```

**参数:**

- `style` (`MenuOptionTextStyle`)

**返回值:** `IMenuBuilderAPI`

**用法示例:**
```csharp
var builder = menuDesignApi.SetGlobalOptionTextStyle(MenuOptionTextStyle.Value);
```

