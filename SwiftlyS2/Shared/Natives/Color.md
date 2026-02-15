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
Color c = Color.FromInt32(0xFF00FF);
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
Color c = Color.FromBuiltin(Color.Red);
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
Color c = Color.FromHex("#FF5733");
```

### ToBuiltin

```csharp
System.Drawing.Color ToBuiltin()
```

**返回值:** `System.Drawing.Color`

**用法示例:**
```csharp
Color builtinColor = Color.Red.ToBuiltin();
```

### ToInt32

```csharp
int ToInt32()
```

**返回值:** `int`

**用法示例:**
```csharp
int colorInt = Color.Red.ToInt32();
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
string hex = color.ToHex(true);
```

### Equals

```csharp
bool Equals(Color other)
```

**参数:**

- `other` (`Color`)

**返回值:** `bool`

