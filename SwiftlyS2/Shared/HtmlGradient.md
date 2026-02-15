# 📦 HtmlGradient

提供用于生成带有渐变颜色效果的 HTML 文本的工具方法。

**命名空间:** `SwiftlyS2.Shared`

**类型:** `class`

## ⚙️ 方法

### GenerateGradientText (静态)

```csharp
string GenerateGradientText(string text, string startColor, string endColor)
```

通过在两种颜色之间进行插值来生成渐变色的文本。

**参数:**

- `text` (`string`) - 要应用渐变的纯文本。不得包含任何 HTML 标签。
- `startColor` (`string`) - 十六进制格式的起始颜色（例如，“#FF0000”）。
- `endColor` (`string`) - 十六进制格式的结束颜色（例如，“#0000FF”）。

**返回值:** `string` - 每个字符都包裹在带颜色的字体标签中的HTML字符串。

**用法示例:**
```csharp
string result = HtmlGradient.GenerateGradientText("Hello", "#FF0000", "#0000FF");
```

### GenerateGradientText (静态)

```csharp
string GenerateGradientText(string text, Natives.Color startColor, Natives.Color endColor)
```

通过在两种 SwiftlyS2 原生颜色之间进行插值，生成渐变色文本。

**参数:**

- `text` (`string`) - 要应用渐变的纯文本。不得包含任何 HTML 标签。
- `startColor` (`Natives.Color`) - 初始的 SwiftlyS2 原生颜色。
- `endColor` (`Natives.Color`) - 最终 SwiftlyS2 原生颜色。

**返回值:** `string` - 每个字符都包裹在带颜色的字体标签中的HTML字符串。

**用法示例:**
```csharp
string result = HtmlGradient.GenerateGradientText("Hello", Natives.Color.Red, Natives.Color.Blue);
```

### GenerateGradientText (静态)

```csharp
string GenerateGradientText(string text, System.Drawing.Color startColor, System.Drawing.Color endColor)
```

通过在两个 System.Drawing 颜色之间进行插值，生成渐变色文本。

**参数:**

- `text` (`string`) - 要应用渐变的纯文本。不得包含任何 HTML 标签。
- `startColor` (`System.Drawing.Color`) - 起始的 System.Drawing 颜色。
- `endColor` (`System.Drawing.Color`) - 结束时的 System.Drawing 颜色。

**返回值:** `string` - 每个字符都包裹在带颜色的字体标签中的HTML字符串。

**用法示例:**
```csharp
HtmlGradient.GenerateGradientText("Hello", System.Drawing.Color.Red, System.Drawing.Color.Blue);
```

### GenerateGradientText (静态)

```csharp
string GenerateGradientText(string text, params Natives.Color[] colors)
```

通过在多个 SwiftlyS2 原生色标之间进行插值，生成渐变色文本。

**参数:**

- `text` (`string`) - 要应用渐变的纯文本。不得包含任何 HTML 标签。
- `colors` (`params Natives.Color[]`) - SwiftlyS2 原生色标数组。

**返回值:** `string` - 每个字符都包裹在带颜色的字体标签中的HTML字符串。

**用法示例:**
```csharp
string result = HtmlGradient.GenerateGradientText("Hello", Natives.Color.Red, Natives.Color.Green, Natives.Color.Blue);
```

### GenerateGradientText (静态)

```csharp
string GenerateGradientText(string text, params System.Drawing.Color[] colors)
```

通过在多个 System.Drawing 颜色停止点之间进行插值，生成渐变着色文本。

**参数:**

- `text` (`string`) - 要应用渐变的纯文本。不得包含任何 HTML 标签。
- `colors` (`params System.Drawing.Color[]`) - System.Drawing 颜色渐变的数组。

**返回值:** `string` - 每个字符都包裹在带颜色的字体标签中的HTML字符串。

**用法示例:**
```csharp
string result = HtmlGradient.GenerateGradientText("Hello", Color.Red, Color.Green, Color.Blue);
```

