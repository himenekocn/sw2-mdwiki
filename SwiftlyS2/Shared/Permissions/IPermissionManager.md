<a id="ipermissionmanager"></a>

# 🔌 IPermissionManager

**命名空间:** `SwiftlyS2.Shared.Permissions`

**类型:** `interface`

## ⚙️ 方法

### PlayerHasPermission

```csharp
bool PlayerHasPermission(ulong steamId, string permission)
```

检查玩家是否拥有某项权限。支持使用'xxx.*'作为通配符权限。

**参数:**

- `steamId` (`ulong`) - 玩家的Steam ID。
- `permission` (`string`) - 要检查的权限。

**返回值:** `bool` - 如果玩家拥有此权限则返回true，否则返回false。

**用法示例:**
```csharp
bool hasPerm = manager.PlayerHasPermission(76561198000000000, "admin.ban");
```

### PlayerHasPermissions

```csharp
bool PlayerHasPermissions(ulong steamId, IEnumerable<string> permissions)
```

检查玩家是否拥有列表中所有权限。支持使用'xxx.*'作为通配符权限。

**参数:**

- `steamId` (`ulong`) - 玩家的Steam ID。
- `permissions` (`IEnumerable\<string\>`) - 要检查的权限列表。

**返回值:** `bool` - 如果玩家拥有所有权限，则为 True，否则为 False。

**用法示例:**
```csharp
bool hasAccess = manager.PlayerHasPermissions(steamId, new[] { "admin.kick", "admin.ban" });
```

### AddPermission

```csharp
void AddPermission(ulong steamId, string permission)
```

为玩家添加一个权限。

**参数:**

- `steamId` (`ulong`) - 玩家的Steam ID。
- `permission` (`string`) - 添加权限。

**用法示例:**
```csharp
permissionManager.AddPermission(76561198000000000UL, "admin");
```

### RemovePermission

```csharp
void RemovePermission(ulong steamId, string permission)
```

从玩家身上移除一个权限。

**参数:**

- `steamId` (`ulong`) - 玩家的Steam ID。
- `permission` (`string`) - 移除权限。

**用法示例:**
```csharp
manager.RemovePermission(76561198000000000, "admin.kick");
```

### AddSubPermission

```csharp
void AddSubPermission(string permission, string subPermission)
```

向权限添加子权限。

**参数:**

- `permission` (`string`) - 将子权限添加至的权限。
- `subPermission` (`string`) - 子权限以添加。

**用法示例:**
```csharp
permissionManager.AddSubPermission("admin", "ban");
```

### RemoveSubPermission

```csharp
void RemoveSubPermission(string permission, string subPermission)
```

从权限中移除一个子权限。

**参数:**

- `permission` (`string`) - 移除子权限的权限。
- `subPermission` (`string`) - 移除的子权限。

**用法示例:**
```csharp
manager.RemoveSubPermission("admin.access", "admin.delete");
```

### ClearPermissions

```csharp
void ClearPermissions(ulong steamId)
```

从玩家身上清除所有权限（包括基础权限与临时权限）。

**参数:**

- `steamId` (`ulong`) - 玩家的Steam ID。

**用法示例:**
```csharp
permissionManager.ClearPermissions(76561198000000000);
```

### GetPlayerPermissions

```csharp
IEnumerable<string> GetPlayerPermissions(ulong steamId)
```

获取一名玩家的所有权限，包括从子权限继承的权限。

**参数:**

- `steamId` (`ulong`) - 玩家的Steam ID。

**返回值:** `IEnumerable\<string\>`

**用法示例:**
```csharp
var permissions = manager.GetPlayerPermissions(steamId);
```

