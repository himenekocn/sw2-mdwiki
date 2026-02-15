# 📦 Helper

**命名空间:** `SwiftlyS2.Shared`

**类型:** `class`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `Default` | `string` | static | - |
| `White` | `string` | static | - |
| `DarkRed` | `string` | static | - |
| `Green` | `string` | static | - |
| `LightYellow` | `string` | static | - |
| `LightBlue` | `string` | static | - |
| `Olive` | `string` | static | - |
| `Lime` | `string` | static | - |
| `Red` | `string` | static | - |
| `LightPurple` | `string` | static | - |
| `Purple` | `string` | static | - |
| `Grey` | `string` | static | - |
| `Yellow` | `string` | static | - |
| `Gold` | `string` | static | - |
| `Silver` | `string` | static | - |
| `Blue` | `string` | static | - |
| `DarkBlue` | `string` | static | - |
| `BlueGrey` | `string` | static | - |
| `Magenta` | `string` | static | - |
| `LightRed` | `string` | static | - |
| `Orange` | `string` | static | - |

## ⚙️ 方法

### Colored (静态)

```csharp
string Colored(this string text)
```

Replace the color codes in the text with the corresponding color codes.

**参数:**

- `text` (`this string`) - The text to replace the color codes in.

**返回值:** `string` - The text with the color codes replaced.

### GetCharWidth (静态)

```csharp
float GetCharWidth(char c)
```

Estimates the display width of a character based on its type. Inspired by: https://github.com/spectreconsole/wcwidth

**参数:**

- `c` (`char`) - The character to measure.

**返回值:** `float` - The estimated display width in relative units.

