# 🔌 IHelpers

**命名空间:** `SwiftlyS2.Shared.Helpers`

**类型:** `interface`

## ⚙️ 方法

### GetWeaponCSDataFromKey

```csharp
CCSWeaponBaseVData? GetWeaponCSDataFromKey(int unknown, string key)
```

根据键获取武器vdata。

**参数:**

- `unknown` (`int`) - 不确定这个参数的用途，但通常情况下其值为 -1。
- `key` (`string`) - 武器的键（通常为物品索引）。

**返回值:** `CCSWeaponBaseVData?` - 武器 vdata。

**用法示例:**
```csharp
CCSWeaponBaseVData? weaponData = helpers.GetWeaponCSDataFromKey(0, "weapon_ak47");
```

### GetWeaponCSDataFromKey

```csharp
CCSWeaponBaseVData? GetWeaponCSDataFromKey(int itemDefinitionIndex)
```

从物品定义索引中获取武器vdata。

**参数:**

- `itemDefinitionIndex` (`int`) - 武器的物品定义索引。

**返回值:** `CCSWeaponBaseVData?` - 武器 vdata。

**用法示例:**
```csharp
IHelpers.GetWeaponCSDataFromKey(1);
```

### GetWeaponCSDataFromKey

```csharp
CCSWeaponBaseVData? GetWeaponCSDataFromKey(ItemDefinitionIndex itemDefinitionIndex)
```

从物品定义索引中获取武器vdata。

**参数:**

- `itemDefinitionIndex` (`ItemDefinitionIndex`) - 武器的物品定义索引。

**返回值:** `CCSWeaponBaseVData?` - 武器 vdata。

**用法示例:**
```csharp
IHelpers.GetWeaponCSDataFromKey(ItemDefinitionIndex.AK47);
```

### GetClassnameByDefinitionIndex

```csharp
string? GetClassnameByDefinitionIndex(int itemDefinitionIndex)
```

从物品定义索引中获取武器类名。

**参数:**

- `itemDefinitionIndex` (`int`) - 武器的物品定义索引。

**返回值:** `string?` - 武器类名（例如 "weapon_awp"），如果未找到则为 null。

**用法示例:**
```csharp
string? className = helpers.GetClassnameByDefinitionIndex(123);
```

### GetClassnameByDefinitionIndex

```csharp
string? GetClassnameByDefinitionIndex(ItemDefinitionIndex itemDefinitionIndex)
```

从物品定义索引中获取武器类名。

**参数:**

- `itemDefinitionIndex` (`ItemDefinitionIndex`) - 武器的物品定义索引。

**返回值:** `string?` - 武器类名（例如 "weapon_awp"），如果未找到则为 null。

**用法示例:**
```csharp
string? className = IHelpers.GetClassnameByDefinitionIndex(ItemDefinitionIndex.AK47);
```

### GetDefinitionIndexByClassname

```csharp
int? GetDefinitionIndexByClassname(string classname)
```

从武器类名获取物品定义索引。

**参数:**

- `classname` (`string`) - 武器类名（例如："weapon_awp"）。

**返回值:** `int?` - 项目定义索引，如果未找到则为 null。

**用法示例:**
```csharp
int? index = helpers.GetDefinitionIndexByClassname("weapon_knife");
```

