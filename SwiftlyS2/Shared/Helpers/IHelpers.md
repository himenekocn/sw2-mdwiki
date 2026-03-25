# 🔌 IHelpers

**命名空间:** `SwiftlyS2.Shared.Helpers`

**类型:** `interface`

## ⚙️ 方法

### GetWeaponCSDataFromKey

```csharp
CCSWeaponBaseVData? GetWeaponCSDataFromKey(int unknown, string key)
```

根据键值获取武器的 vdata。

**参数:**

- `unknown` (`int`) - 不确定此参数的用途，但通常情况下其值为 -1。
- `key` (`string`) - 武器的键值（通常为物品索引 idx）。

**返回值:** `CCSWeaponBaseVData?` - 武器 vdata（变量数据）。

**用法示例:**
```csharp
var weaponData = helpers.GetWeaponCSDataFromKey(0, "weapon_ak47");
```

### GetWeaponCSDataFromKey

```csharp
CCSWeaponBaseVData? GetWeaponCSDataFromKey(int itemDefinitionIndex)
```

从物品定义索引获取武器 VData。

**参数:**

- `itemDefinitionIndex` (`int`) - 武器的物品定义索引。

**返回值:** `CCSWeaponBaseVData?` - 武器 vdata（变量数据）。

**用法示例:**
```csharp
var weaponData = helpers.GetWeaponCSDataFromKey(1);
```

### GetWeaponCSDataFromKey

```csharp
CCSWeaponBaseVData? GetWeaponCSDataFromKey(ItemDefinitionIndex itemDefinitionIndex)
```

从物品定义索引获取武器 VData。

**参数:**

- `itemDefinitionIndex` (`ItemDefinitionIndex`) - 武器的物品定义索引。

**返回值:** `CCSWeaponBaseVData?` - 武器 vdata（变量数据）。

**用法示例:**
```csharp
var weaponData = helpers.GetWeaponCSDataFromKey(ItemDefinitionIndex.AK47);
```

### GetClassnameByDefinitionIndex

```csharp
string? GetClassnameByDefinitionIndex(int itemDefinitionIndex)
```

根据物品定义索引获取武器类名。

**参数:**

- `itemDefinitionIndex` (`int`) - 武器的物品定义索引。

**返回值:** `string?` - 武器类名（例如"weapon_awp"），若未找到则为 null。

**用法示例:**
```csharp
string? className = helpers.GetClassnameByDefinitionIndex(1);
```

### GetClassnameByDefinitionIndex

```csharp
string? GetClassnameByDefinitionIndex(ItemDefinitionIndex itemDefinitionIndex)
```

根据物品定义索引获取武器类名。

**参数:**

- `itemDefinitionIndex` (`ItemDefinitionIndex`) - 武器的物品定义索引。

**返回值:** `string?` - 武器类名（例如"weapon_awp"），若未找到则为 null。

**用法示例:**
```csharp
string? className = helpers.GetClassnameByDefinitionIndex(ItemDefinitionIndex.AK47);
```

### GetDefinitionIndexByClassname

```csharp
int? GetDefinitionIndexByClassname(string classname)
```

从武器类名获取物品定义索引。

**参数:**

- `classname` (`string`) - 武器类名（例如："weapon_awp"）。

**返回值:** `int?` - 物品定义索引，若未找到则为 null。

**用法示例:**
```csharp
int? index = helpers.GetDefinitionIndexByClassname("weapon_ak47");
```

