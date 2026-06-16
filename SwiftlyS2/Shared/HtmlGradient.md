<a id="htmlgradient"></a>

# 📦 HtmlGradient

提供用于生成带有渐变颜色效果的HTML文本的实用方法。

**命名空间:** `SwiftlyS2.Shared`

**类型:** `class`

## ⚙️ 方法

### GenerateGradientText (静态)

```csharp
string GenerateGradientText(string text, string startColor, string endColor)
```

通过两种颜色之间的插值生成渐变彩色文本。

**参数:**

- `text` (`string`) - 要应用渐变效果的纯文本。不能包含任何HTML标签。
- `startColor` (`string`) - 起始颜色，十六进制格式（例如 "#FF0000"）。
- `endColor` (`string`) - 以十六进制格式表示的结束颜色（例如"#0000FF"）。

**返回值:** `string` - HTML 字符串，每个字符均包裹在带颜色的字体标签内。

**用法示例:**
```csharp
string result = HtmlGradient.GenerateGradientText("Hello World", "#FF0000", "#0000FF");
```

### GenerateGradientText (静态)

```csharp
string GenerateGradientText(string text, Natives.Color startColor, Natives.Color endColor)
```

通过在两个SwiftlyS2原生颜色之间插值生成渐变彩色文本。

**参数:**

- `text` (`string`) - 要应用渐变效果的纯文本。不能包含任何HTML标签。
- `startColor` (`Natives.Color`) - 起始的SwiftlyS2原生颜色。
- `endColor` (`Natives.Color`) - 结尾的SwiftlyS2原生颜色。

**返回值:** `string` - HTML 字符串，每个字符均包裹在带颜色的字体标签内。

**用法示例:**
```csharp
string gradientText = HtmlGradient.GenerateGradientText("Hello World", Natives.Color.Red, Natives.Color.Blue);
```

### GenerateGradientText (静态)

```csharp
string GenerateGradientText(string text, System.Drawing.Color startColor, System.Drawing.Color endColor)
```

通过插值两种System.Drawing颜色生成渐变彩色文本。

**参数:**

- `text` (`string`) - 要应用渐变效果的纯文本。不能包含任何HTML标签。
- `startColor` (`System.Drawing.Color`) - 起始 System.Drawing 颜色。
- `endColor` (`System.Drawing.Color`) - 结束时的 System.Drawing 颜色。

**返回值:** `string` - HTML 字符串，每个字符均包裹在带颜色的字体标签内。

**用法示例:**
```csharp
string result = HtmlGradient.GenerateGradientText("Hello World", System.Drawing.Color.Red, System.Drawing.Color.Blue);
```

### GenerateGradientText (静态)

```csharp
string GenerateGradientText(string text, params Natives.Color[] colors)
```

通过插值多个 SwiftlyS2 原生颜色节点生成渐变彩色文本。

**参数:**

- `text` (`string`) - 要应用渐变效果的纯文本。不能包含任何HTML标签。
- `colors` (`params Natives.Color[]`) - SwiftlyS2 原生颜色停止点的数组

**返回值:** `string` - HTML 字符串，每个字符均包裹在带颜色的字体标签内。

**用法示例:**
```csharp
string result = HtmlGradient.GenerateGradientText("Hello World", Natives.Color.Red, Natives.Color.Blue);
```

### GenerateGradientText (静态)

```csharp
string GenerateGradientText(string text, params System.Drawing.Color[] colors)
```

通过插值多个 System.Drawing 颜色节点生成渐变彩色文本。

**参数:**

- `text` (`string`) - 要应用渐变效果的纯文本。不能包含任何HTML标签。
- `colors` (`params System.Drawing.Color[]`) - System.Drawing 颜色停止点的数组。

**返回值:** `string` - HTML 字符串，每个字符均包裹在带颜色的字体标签内。

**用法示例:**
```csharp
string result = HtmlGradient.GenerateGradientText("Hello World", System.Drawing.Color.Red, System.Drawing.Color.Blue);
```

