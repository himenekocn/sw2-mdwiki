<a id="color"></a>

# 🏗️ Color

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

**继承:** `IEquatable\<Color\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `R` | `byte` | - | - |
| `G` | `byte` | - | - |
| `B` | `byte` | - | - |
| `A` | `byte` | - | - |

## ⚙️ 方法

### FromInt32 (静态)

```csharp
Color FromInt32(int color)
```

**参数:**

- `color` (`int`)

**返回值:** `Color`

**用法示例:**
```csharp
Color color = Color.FromInt32(0xFF5733);
```

### FromBuiltin (静态)

```csharp
Color FromBuiltin(System.Drawing.Color color)
```

**参数:**

- `color` (`System.Drawing.Color`)

**返回值:** `Color`

**用法示例:**
```csharp
var color = Color.FromBuiltin(System.Drawing.Color.Red);
```

### FromHex (静态)

```csharp
Color FromHex(string hex)
```

**参数:**

- `hex` (`string`)

**返回值:** `Color`

**用法示例:**
```csharp
Color color = Color.FromHex("#FF5733");
```

### ToBuiltin

```csharp
System.Drawing.Color ToBuiltin()
```

**返回值:** `System.Drawing.Color`

**用法示例:**
```csharp
System.Drawing.Color builtinColor = color.ToBuiltin();
```

### ToInt32

```csharp
int ToInt32()
```

**返回值:** `int`

**用法示例:**
```csharp
int colorValue = player.Color.ToInt32();
```

### ToHex

```csharp
string ToHex(bool includeAlpha = false)
```

**参数:**

- `includeAlpha` (`bool`) = `false`

**返回值:** `string`

**用法示例:**
```csharp
string hex = player.Color.ToHex(true);
```

### Equals

```csharp
bool Equals(Color other)
```

**参数:**

- `other` (`Color`)

**返回值:** `bool`

