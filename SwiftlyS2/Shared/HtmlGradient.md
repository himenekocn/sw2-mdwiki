<a id="htmlgradient"></a>

# 📦 HtmlGradient

提供用于生成带有渐变颜色效果的 HTML 文本的工具方法。

**命名空间:** `SwiftlyS2.Shared`

**类型:** `class`

## ⚙️ 方法

### GenerateGradientText (静态)

```csharp
string GenerateGradientText(string text, string startColor, string endColor)
```

通过插值两种颜色生成渐变色文本。

**参数:**

- `text` (`string`) - 要应用渐变的纯文本。不得包含任何 HTML 标签。
- `startColor` (`string`) - 以十六进制格式表示的起始颜色（例如："#FF0000"）。
- `endColor` (`string`) - 十六进制格式（例如"#0000FF"）的结束颜色。

**返回值:** `string` - 包含每个字符都用彩色字体标签包裹的 HTML 字符串。

**用法示例:**
```csharp
string result = HtmlGradient.GenerateGradientText("Hello", "#FF0000", "#0000FF");
```

### GenerateGradientText (静态)

```csharp
string GenerateGradientText(string text, Natives.Color startColor, Natives.Color endColor)
```

通过插值两个 SwiftlyS2 原生颜色来生成渐变色文本。

**参数:**

- `text` (`string`) - 要应用渐变的纯文本。不得包含任何 HTML 标签。
- `startColor` (`Natives.Color`) - SwiftlyS2 原生起始颜色。
- `endColor` (`Natives.Color`) - SwiftlyS2 的原生颜色结束值。

**返回值:** `string` - 包含每个字符都用彩色字体标签包裹的 HTML 字符串。

**用法示例:**
```csharp
string result = HtmlGradient.GenerateGradientText("Hello", Natives.Color.Red, Natives.Color.Blue);
```

### GenerateGradientText (静态)

```csharp
string GenerateGradientText(string text, System.Drawing.Color startColor, System.Drawing.Color endColor)
```

通过插值两种 System.Drawing 颜色生成渐变色文本。

**参数:**

- `text` (`string`) - 要应用渐变的纯文本。不得包含任何 HTML 标签。
- `startColor` (`System.Drawing.Color`) - 起始的 System.Drawing 颜色。
- `endColor` (`System.Drawing.Color`) - 最终的系统绘制颜色。

**返回值:** `string` - 包含每个字符都用彩色字体标签包裹的 HTML 字符串。

**用法示例:**
```csharp
string result = HtmlGradient.GenerateGradientText("Hello", System.Drawing.Color.Red, System.Drawing.Color.Blue);
```

### GenerateGradientText (静态)

```csharp
string GenerateGradientText(string text, params Natives.Color[] colors)
```

通过插值多个 SwiftlyS2 原生颜色停止点，生成渐变色文本。

**参数:**

- `text` (`string`) - 要应用渐变的纯文本。不得包含任何 HTML 标签。
- `colors` (`params Natives.Color[]`) - SwiftlyS2 原生颜色停止点数组。

**返回值:** `string` - 包含每个字符都用彩色字体标签包裹的 HTML 字符串。

**用法示例:**
```csharp
string result = HtmlGradient.GenerateGradientText("Hello", Natives.Color.Red, Natives.Color.Blue);
```

### GenerateGradientText (静态)

```csharp
string GenerateGradientText(string text, params System.Drawing.Color[] colors)
```

通过插值多个 System.Drawing 颜色停止点，生成渐变彩色文本。

**参数:**

- `text` (`string`) - 要应用渐变的纯文本。不得包含任何 HTML 标签。
- `colors` (`params System.Drawing.Color[]`) - System.Drawing 颜色渐变的数组。

**返回值:** `string` - 包含每个字符都用彩色字体标签包裹的 HTML 字符串。

**用法示例:**
```csharp
string result = HtmlGradient.GenerateGradientText("Hello", System.Drawing.Color.Red, System.Drawing.Color.Blue);
```

