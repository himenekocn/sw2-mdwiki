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

将文本中的颜色代码替换为对应的颜色代码。

**参数:**

- `text` (`this string`) - 要替换颜色代码的文本。

**返回值:** `string` - 已替换颜色代码的文本。

**用法示例:**
```csharp
Helper.Colored("Hello [red]World[/red]")
```

