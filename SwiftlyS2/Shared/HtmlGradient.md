# 📦 HtmlGradient

Provides utility methods for generating HTML text with gradient color effects.

**命名空间:** `SwiftlyS2.Shared`

**类型:** `class`

## ⚙️ 方法

### GenerateGradientText (静态)

```csharp
string GenerateGradientText(string text, string startColor, string endColor)
```

Generates gradient colored text by interpolating between two colors.

**参数:**

- `text` (`string`) - The plain text to apply gradient to. Must not contain any HTML tags.
- `startColor` (`string`) - The starting color in hex format (e.g., "#FF0000").
- `endColor` (`string`) - The ending color in hex format (e.g., "#0000FF").

**返回值:** `string` - HTML string with each character wrapped in a colored font tag.

### GenerateGradientText (静态)

```csharp
string GenerateGradientText(string text, params string[] colors)
```

Generates gradient colored text by interpolating across multiple color stops.

**参数:**

- `text` (`string`) - The plain text to apply gradient to. Must not contain any HTML tags.
- `colors` (`params string[]`) - Array of color stops in hex format (e.g., "#FF0000", "#00FF00", "#0000FF").

**返回值:** `string` - HTML string with each character wrapped in a colored font tag.

### GenerateGradientText (静态)

```csharp
string GenerateGradientText(string text, Natives.Color startColor, Natives.Color endColor)
```

Generates gradient colored text by interpolating between two SwiftlyS2 native colors.

**参数:**

- `text` (`string`) - The plain text to apply gradient to. Must not contain any HTML tags.
- `startColor` (`Natives.Color`) - The starting SwiftlyS2 native color.
- `endColor` (`Natives.Color`) - The ending SwiftlyS2 native color.

**返回值:** `string` - HTML string with each character wrapped in a colored font tag.

### GenerateGradientText (静态)

```csharp
string GenerateGradientText(string text, System.Drawing.Color startColor, System.Drawing.Color endColor)
```

Generates gradient colored text by interpolating between two System.Drawing colors.

**参数:**

- `text` (`string`) - The plain text to apply gradient to. Must not contain any HTML tags.
- `startColor` (`System.Drawing.Color`) - The starting System.Drawing color.
- `endColor` (`System.Drawing.Color`) - The ending System.Drawing color.

**返回值:** `string` - HTML string with each character wrapped in a colored font tag.

### GenerateGradientText (静态)

```csharp
string GenerateGradientText(string text, params Natives.Color[] colors)
```

Generates gradient colored text by interpolating across multiple SwiftlyS2 native color stops.

**参数:**

- `text` (`string`) - The plain text to apply gradient to. Must not contain any HTML tags.
- `colors` (`params Natives.Color[]`) - Array of SwiftlyS2 native color stops.

**返回值:** `string` - HTML string with each character wrapped in a colored font tag.

### GenerateGradientText (静态)

```csharp
string GenerateGradientText(string text, params System.Drawing.Color[] colors)
```

Generates gradient colored text by interpolating across multiple System.Drawing color stops.

**参数:**

- `text` (`string`) - The plain text to apply gradient to. Must not contain any HTML tags.
- `colors` (`params System.Drawing.Color[]`) - Array of System.Drawing color stops.

**返回值:** `string` - HTML string with each character wrapped in a colored font tag.

