<a id="ihelpers"></a>

# 🔌 IHelpers

**命名空间:** `SwiftlyS2.Shared.Helpers`

**类型:** `interface`

## ⚙️ 方法

### GetWeaponCSDataFromKey

```csharp
CCSWeaponBaseVData? GetWeaponCSDataFromKey(int unknown, string key)
```

从键获取武器虚拟数据。

**参数:**

- `unknown` (`int`) - 不确定这个参数的作用，但通常为-1。
- `key` (`string`) - 武器的键（通常为物品索引）。

**返回值:** `CCSWeaponBaseVData?` - 武器虚拟数据。

**用法示例:**
```csharp
var weaponData = helpers.GetWeaponCSDataFromKey(0, "weapon_ak47");
```

### GetWeaponCSDataFromKey

```csharp
CCSWeaponBaseVData? GetWeaponCSDataFromKey(int itemDefinitionIndex)
```

从物品定义索引获取武器虚拟数据。

**参数:**

- `itemDefinitionIndex` (`int`) - 武器的物品定义索引。

**返回值:** `CCSWeaponBaseVData?` - 武器虚拟数据。

**用法示例:**
```csharp
var weaponData = helpers.GetWeaponCSDataFromKey(1);
```

### GetWeaponCSDataFromKey

```csharp
CCSWeaponBaseVData? GetWeaponCSDataFromKey(ItemDefinitionIndex itemDefinitionIndex)
```

从物品定义索引获取武器虚拟数据。

**参数:**

- `itemDefinitionIndex` (`ItemDefinitionIndex`) - 武器的物品定义索引。

**返回值:** `CCSWeaponBaseVData?` - 武器虚拟数据。

**用法示例:**
```csharp
var weaponData = helpers.GetWeaponCSDataFromKey(ItemDefinitionIndex.WeaponAk47);
```

### GetClassnameByDefinitionIndex

```csharp
string? GetClassnameByDefinitionIndex(int itemDefinitionIndex)
```

从物品定义索引获取武器类名。

**参数:**

- `itemDefinitionIndex` (`int`) - 武器的物品定义索引。

**返回值:** `string?` - 武器类名（例如"weapon_awp"），如果未找到则为null。

**用法示例:**
```csharp
string? className = helpers.GetClassnameByDefinitionIndex(1);
```

### GetClassnameByDefinitionIndex

```csharp
string? GetClassnameByDefinitionIndex(ItemDefinitionIndex itemDefinitionIndex)
```

从物品定义索引获取武器类名。

**参数:**

- `itemDefinitionIndex` (`ItemDefinitionIndex`) - 武器的物品定义索引。

**返回值:** `string?` - 武器类名（例如"weapon_awp"），如果未找到则为null。

**用法示例:**
```csharp
string? className = helpers.GetClassnameByDefinitionIndex(ItemDefinitionIndex.WeaponAk47);
```

### GetDefinitionIndexByClassname

```csharp
int? GetDefinitionIndexByClassname(string classname)
```

从武器类名获取物品定义索引。

**参数:**

- `classname` (`string`) - 武器类别名称（例如 "weapon_awp"）。

**返回值:** `int?` - 物品定义索引，如果未找到则为空。

**用法示例:**
```csharp
int? index = helpers.GetDefinitionIndexByClassname("weapon_ak47");
```

