<a id="ccommand"></a>

# 🏗️ CCommand

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `ArgC` | `int` | readonly | - |

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ArgC` | `int` | - | - |
| `ArgS` | `string?` | - | - |
| `GetCommandString` | `string?` | - | - |
| `this[int index]` | `string?` | - | - |

## ⚙️ 方法

### Reset

```csharp
void Reset()
```

**用法示例:**
```csharp
CCommand.Reset();
```

### FindArg

```csharp
int FindArg(string name)
```

**参数:**

- `name` (`string`)

**返回值:** `int`

**用法示例:**
```csharp
int index = command.FindArg("-target");
```

### FindArgInt

```csharp
int FindArgInt(string name, int defaultVal)
```

**参数:**

- `name` (`string`)
- `defaultVal` (`int`)

**返回值:** `int`

**用法示例:**
```csharp
int value = cmd.FindArgInt("count", 10);
```

### Tokenize

```csharp
bool Tokenize(string commandString)
```

**参数:**

- `commandString` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = command.Tokenize("say Hello");
```

