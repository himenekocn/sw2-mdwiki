<a id="itranslationservice"></a>

# 🔌 ITranslationService

**命名空间:** `SwiftlyS2.Shared.Translation`

**类型:** `interface`

## ⚙️ 方法

### GetPlayerLocalizer

```csharp
ILocalizer GetPlayerLocalizer(IPlayer player)
```

获取指定玩家的本地化器。

**参数:**

- `player` (`IPlayer`) - 要为其获取本地化器的玩家。

**返回值:** `ILocalizer` - 指定玩家的本地化器。

**用法示例:**
```csharp
var localizer = translationService.GetPlayerLocalizer(player);
```

