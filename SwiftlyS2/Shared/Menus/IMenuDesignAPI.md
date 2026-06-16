<a id="imenudesignapi"></a>

# 🔌 IMenuDesignAPI

**命名空间:** `SwiftlyS2.Shared.Menus`

**类型:** `interface`

## ⚙️ 方法

### SetMenuTitle

```csharp
IMenuBuilderAPI SetMenuTitle(string? title = null)
```

设置菜单顶部显示的标题文本。

**参数:**

- `title` (`string?`) = `null` - 标题文本。传递null以清除标题。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignApi.SetMenuTitle("主菜单");
```

### SetMenuTitleVisible

```csharp
IMenuBuilderAPI SetMenuTitleVisible(bool visible = true)
```

控制菜单标题的可见性。

**参数:**

- `visible` (`bool`) = `true` - true 表示显示标题，false 表示隐藏标题。默认值为 true。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignAPI.SetMenuTitleVisible(false);
```

### SetMenuTitleItemCountVisible

```csharp
IMenuBuilderAPI SetMenuTitleItemCountVisible(bool visible = true)
```

控制菜单标题中物品数量的可见性。

**参数:**

- `visible` (`bool`) = `true` - 为true时显示物品计数，为false时隐藏。默认值为true。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignAPI.SetMenuTitleItemCountVisible(true);
```

### SetMenuFooterVisible

```csharp
IMenuBuilderAPI SetMenuFooterVisible(bool visible = true)
```

控制菜单底部栏的可见性。

**参数:**

- `visible` (`bool`) = `true` - 显示页脚时为true，隐藏时为false。默认值为true。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignAPI.SetMenuFooterVisible(true);
```

### SetCommentVisible

```csharp
IMenuBuilderAPI SetCommentVisible(bool visible = true)
```

控制菜单选项注释的可见性。

**参数:**

- `visible` (`bool`) = `true` - true 表示显示注释，false 表示隐藏注释。默认值为 true。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignAPI.SetCommentVisible(true);
```

### SetMaxVisibleItems

```csharp
IMenuBuilderAPI SetMaxVisibleItems(int count = 5)
```

设置屏幕上同时可见的最大菜单选项数量。

**参数:**

- `count` (`int`) = `5` - 最大可见物品数量。有效范围为1-5。默认值为5。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignAPI.SetMaxVisibleItems(5);
```

### EnableAutoAdjustVisibleItems

```csharp
IMenuBuilderAPI EnableAutoAdjustVisibleItems()
```

在标题或页脚隐藏时，启用可见项的自动调整。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignAPI.EnableAutoAdjustVisibleItems();
```

### DisableAutoAdjustVisibleItems

```csharp
IMenuBuilderAPI DisableAutoAdjustVisibleItems()
```

禁用标题或页脚隐藏时对可见项目的自动调整。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignAPI.DisableAutoAdjustVisibleItems();
```

### SetGlobalScrollStyle

```csharp
IMenuBuilderAPI SetGlobalScrollStyle(MenuOptionScrollStyle style)
```

设置所有菜单选项的默认滚动动画样式。

**参数:**

- `style` (`MenuOptionScrollStyle`) - 全局应用的滚动样式。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignAPI.SetGlobalScrollStyle(MenuOptionScrollStyle.Smooth);
```

### SetNavigationMarkerColor

```csharp
IMenuBuilderAPI SetNavigationMarkerColor(string? hexColor = null)
```

使用十六进制颜色格式设置导航标记的颜色。

**参数:**

- `hexColor` (`string?`) = `null` - 十六进制格式的颜色（例如，白色为"#FFFFFF"）。传递null以重置为默认值。

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

- `color` (`Natives.Color`) - 应用于导航标记的SwiftlyS2原生颜色。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignApi.SetNavigationMarkerColor(Natives.Color.Red);
```

### SetNavigationMarkerColor

```csharp
IMenuBuilderAPI SetNavigationMarkerColor(System.Drawing.Color color)
```

使用 System.Drawing 颜色设置导航标记的颜色。

**参数:**

- `color` (`System.Drawing.Color`) - 应用于导航标记的System.Drawing颜色。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignAPI.SetNavigationMarkerColor(System.Drawing.Color.Red);
```

### SetMenuFooterColor

```csharp
IMenuBuilderAPI SetMenuFooterColor(string? hexColor = null)
```

使用十六进制颜色格式设置菜单页脚的颜色。

**参数:**

- `hexColor` (`string?`) = `null` - 十六进制格式的颜色（例如，红色为"#FF0000"）。传入null以重置为默认值。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignApi.SetMenuFooterColor("#FF5733");
```

### SetMenuFooterColor

```csharp
IMenuBuilderAPI SetMenuFooterColor(Natives.Color color)
```

使用SwiftlyS2原生颜色设置菜单底部的颜色。

**参数:**

- `color` (`Natives.Color`) - 应用于底部的SwiftlyS2原生颜色。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignAPI.SetMenuFooterColor(Natives.Color.Red);
```

### SetMenuFooterColor

```csharp
IMenuBuilderAPI SetMenuFooterColor(System.Drawing.Color color)
```

使用 System.Drawing 颜色设置菜单底部的颜色。

**参数:**

- `color` (`System.Drawing.Color`) - 要应用于页脚的System.Drawing颜色。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignAPI.SetMenuFooterColor(System.Drawing.Color.Blue);
```

### SetVisualGuideLineColor

```csharp
IMenuBuilderAPI SetVisualGuideLineColor(string? hexColor = null)
```

使用十六进制颜色格式设置视觉辅助线的颜色。

**参数:**

- `hexColor` (`string?`) = `null` - 十六进制格式的颜色（例如，白色为"#FFFFFF"）。传递null以重置为默认值。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignAPI.SetVisualGuideLineColor("#FF0000");
```

### SetVisualGuideLineColor

```csharp
IMenuBuilderAPI SetVisualGuideLineColor(Natives.Color color)
```

使用 SwiftlyS2 原生颜色设置视觉引导线的颜色。

**参数:**

- `color` (`Natives.Color`) - 应用于引导线的SwiftlyS2原生颜色。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignAPI.SetVisualGuideLineColor(Natives.Color.Red);
```

### SetVisualGuideLineColor

```csharp
IMenuBuilderAPI SetVisualGuideLineColor(System.Drawing.Color color)
```

使用 System.Drawing 颜色设置视觉引导线的颜色。

**参数:**

- `color` (`System.Drawing.Color`) - 应用于参考线的System.Drawing颜色。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignAPI.SetVisualGuideLineColor(System.Drawing.Color.Red);
```

### SetDisabledColor

```csharp
IMenuBuilderAPI SetDisabledColor(string? hexColor = null)
```

使用十六进制颜色格式设置禁用菜单选项的颜色。

**参数:**

- `hexColor` (`string?`) = `null` - 十六进制格式的颜色（例如，灰色为"#808080"）。传递 null 可重置为默认值。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignAPI.SetDisabledColor("#808080");
```

### SetDisabledColor

```csharp
IMenuBuilderAPI SetDisabledColor(Natives.Color color)
```

使用SwiftlyS2原生颜色设置禁用菜单选项的颜色。

**参数:**

- `color` (`Natives.Color`) - 应用于禁用选项的SwiftlyS2原生颜色。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignAPI.SetDisabledColor(Natives.Color.Red);
```

### SetDisabledColor

```csharp
IMenuBuilderAPI SetDisabledColor(System.Drawing.Color color)
```

使用System.Drawing颜色设置禁用菜单选项的颜色。

**参数:**

- `color` (`System.Drawing.Color`) - 应用于禁用选项的System.Drawing颜色。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignAPI.SetDisabledColor(System.Drawing.Color.Gray);
```

### SetDefaultComment

```csharp
IMenuBuilderAPI SetDefaultComment(string comment)
```

当菜单选项的注释未设置时，设置要使用的默认注释文本。

**参数:**

- `comment` (`string`) - 默认注释文本。

**返回值:** `IMenuBuilderAPI` - 用于方法链式调用的菜单构建器。

**用法示例:**
```csharp
menuDesignAPI.SetDefaultComment("请选择一个选项");
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
menuDesignAPI.SetGlobalOptionTextStyle(MenuOptionTextStyle.Bold);
```

