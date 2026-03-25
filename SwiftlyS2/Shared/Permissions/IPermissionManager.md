<a id="ipermissionmanager"></a>

# 🔌 IPermissionManager

**命名空间:** `SwiftlyS2.Shared.Permissions`

**类型:** `interface`

## ⚙️ 方法

### PlayerHasPermission

```csharp
bool PlayerHasPermission(ulong steamId, string permission)
```

检查玩家是否拥有某项权限。支持使用'xxx.*'进行通配符权限匹配。

**参数:**

- `steamId` (`ulong`) - 玩家的 Steam ID。
- `permission` (`string`) - 待检查的权限。

**返回值:** `bool` - 若玩家拥有该权限则为 true，否则为 false。

**用法示例:**
```csharp
bool hasAccess = permissionManager.PlayerHasPermission(76561198000000000, "admin.*");
```

### PlayerHasPermissions

```csharp
bool PlayerHasPermissions(ulong steamId, IEnumerable<string> permissions)
```

检查玩家是否拥有列表中所有权限。支持使用 'xxx.*' 进行通配符权限匹配。

**参数:**

- `steamId` (`ulong`) - 玩家的 Steam ID。
- `permissions` (`IEnumerable\<string\>`) - 待检查的权限列表。

**返回值:** `bool` - 若玩家拥有所有权限则为 true，否则为 false。

**用法示例:**
```csharp
bool hasAccess = manager.PlayerHasPermissions(steamId, new[] { "admin.*", "teleport" });
```

### AddPermission

```csharp
void AddPermission(ulong steamId, string permission)
```

向玩家添加权限。

**参数:**

- `steamId` (`ulong`) - 玩家的 Steam ID。
- `permission` (`string`) - 添加权限。

**用法示例:**
```csharp
permissionManager.AddPermission(76561198000000000, "admin");
```

### RemovePermission

```csharp
void RemovePermission(ulong steamId, string permission)
```

移除玩家的权限。

**参数:**

- `steamId` (`ulong`) - 玩家的 Steam ID。
- `permission` (`string`) - 移除权限。

**用法示例:**
```csharp
manager.RemovePermission(76561198000000000u, "vip");
```

### AddSubPermission

```csharp
void AddSubPermission(string permission, string subPermission)
```

为权限添加子权限。

**参数:**

- `permission` (`string`) - 可添加子权限的权限。
- `subPermission` (`string`) - 要添加的子权限。

**用法示例:**
```csharp
manager.AddSubPermission("admin", "kick");
```

### RemoveSubPermission

```csharp
void RemoveSubPermission(string permission, string subPermission)
```

从权限中移除一个子权限。

**参数:**

- `permission` (`string`) - 移除子权限的权限。
- `subPermission` (`string`) - 要移除的子权限。

**用法示例:**
```csharp
permissionManager.RemoveSubPermission("admin.access", "debug.mode");
```

### ClearPermission

```csharp
void ClearPermission(ulong steamId)
```

清除玩家的所有权限。

**参数:**

- `steamId` (`ulong`) - 玩家的 Steam ID。

**用法示例:**
```csharp
permissionManager.ClearPermission(steamId);
```

