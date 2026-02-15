# 📦 MenuBuilderAPI

**命名空间:** `SwiftlyS2.Core.Menus`

**类型:** `class`

**继承:** `IMenuBuilderAPI`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `Design` | `IMenuDesignAPI` | get | Gets the design interface for this menu. |

## ⚙️ 方法

### BindToParent

```csharp
IMenuBuilderAPI BindToParent(IMenuAPI parent)
```

**参数:**

- `parent` (`IMenuAPI`)

**返回值:** `IMenuBuilderAPI`

### AddOption

```csharp
IMenuBuilderAPI AddOption(IMenuOption option)
```

**参数:**

- `option` (`IMenuOption`)

**返回值:** `IMenuBuilderAPI`

### EnableSound

```csharp
IMenuBuilderAPI EnableSound()
```

**返回值:** `IMenuBuilderAPI`

### DisableSound

```csharp
IMenuBuilderAPI DisableSound()
```

**返回值:** `IMenuBuilderAPI`

### EnableExit

```csharp
IMenuBuilderAPI EnableExit()
```

**返回值:** `IMenuBuilderAPI`

### DisableExit

```csharp
IMenuBuilderAPI DisableExit()
```

**返回值:** `IMenuBuilderAPI`

### SetPlayerFrozen

```csharp
IMenuBuilderAPI SetPlayerFrozen(bool frozen = false)
```

**参数:**

- `frozen` (`bool`) = `false`

**返回值:** `IMenuBuilderAPI`

### SetAutoCloseDelay

```csharp
IMenuBuilderAPI SetAutoCloseDelay(float seconds = 0f)
```

**参数:**

- `seconds` (`float`) = `0f`

**返回值:** `IMenuBuilderAPI`

### SetSelectButton

```csharp
IMenuBuilderAPI SetSelectButton(KeyBind keyBind)
```

**参数:**

- `keyBind` (`KeyBind`)

**返回值:** `IMenuBuilderAPI`

### SetMoveForwardButton

```csharp
IMenuBuilderAPI SetMoveForwardButton(KeyBind keyBind)
```

**参数:**

- `keyBind` (`KeyBind`)

**返回值:** `IMenuBuilderAPI`

### SetMoveBackwardButton

```csharp
IMenuBuilderAPI SetMoveBackwardButton(KeyBind keyBind)
```

**参数:**

- `keyBind` (`KeyBind`)

**返回值:** `IMenuBuilderAPI`

### SetExitButton

```csharp
IMenuBuilderAPI SetExitButton(KeyBind keyBind)
```

**参数:**

- `keyBind` (`KeyBind`)

**返回值:** `IMenuBuilderAPI`

### AddExtraButton

```csharp
IMenuBuilderAPI AddExtraButton(KeyBind keyBind, string label, Action<IPlayer, IMenuAPI> action)
```

**参数:**

- `keyBind` (`KeyBind`)
- `label` (`string`)
- `action` (`Action\<IPlayer, IMenuAPI\>`)

**返回值:** `IMenuBuilderAPI`

### Build

```csharp
IMenuAPI Build()
```

**返回值:** `IMenuAPI`

