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

### AsSchema<T> (静态)

```csharp
T AsSchema<T>(nint ptr)
```

将指针转换为架构类。

**参数:**

- `ptr` (`nint`) - 指向架构类的指针。

**返回值:** `T` - 架构类。

**用法示例:**
```csharp
var schema = Helper.AsSchema<MySchema>(ptr);
```

### AsProtobuf<T> (静态)

```csharp
T AsProtobuf<T>(nint ptr, bool manuallyAllocated)
```

将指针转换为 protobuf 类。

**参数:**

- `ptr` (`nint`) - 指向 protobuf 类的指针。
- `manuallyAllocated` (`bool`) - 指针是否为手动分配。

**返回值:** `T` - protobuf 类。

**用法示例:**
```csharp
var protobufObj = Helper.AsProtobuf<MyProto>(ptr, true);
```

### GetSchemaSize<T> (静态)

```csharp
int GetSchemaSize<T>()
```

获取架构类的大小。

**返回值:** `int` - 架构类的大小。

**用法示例:**
```csharp
int size = Helper.GetSchemaSize<MySchema>();
```

