# 📦 InputMenuOption

表示一个允许玩家输入文本的菜单选项。

**命名空间:** `SwiftlyS2.Core.Menus.OptionsBase`

**类型:** `class`

**继承:** `MenuOptionBase`

## ⚙️ 方法

### GetDisplayText

```csharp
string GetDisplayText(IPlayer player, int displayLine = 0)
```

**参数:**

- `player` (`IPlayer`)
- `displayLine` (`int`) = `0`

**返回值:** `string`

**用法示例:**
```csharp
string text = inputMenuOption.GetDisplayText(player1, 0);
```

### GetValue

```csharp
string GetValue(IPlayer player)
```

获取指定玩家的当前输入值。

**参数:**

- `player` (`IPlayer`) - 要检索其值的玩家。

**返回值:** `string` - 当前输入值。

**用法示例:**
```csharp
string value = inputMenuOption.GetValue(player);
```

### SetValue

```csharp
bool SetValue(IPlayer player, string value)
```

为指定玩家设置输入值并触发验证。

**参数:**

- `player` (`IPlayer`) - 要设置其值的玩家。
- `value` (`string`) - 要设置的值。

**返回值:** `bool` - 如果值有效且已设置，则为 true；否则为 false。

**用法示例:**
```csharp
bool success = inputMenuOption.SetValue(player, "someValue");
```

### Dispose

```csharp
void Dispose()
```

