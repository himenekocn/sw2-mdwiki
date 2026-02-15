# 📦 PermissionManager

**命名空间:** `SwiftlyS2.Core.Permissions`

**类型:** `class`

**继承:** `IPermissionManager`

## ⚙️ 方法

### PlayerHasPermissions

```csharp
bool PlayerHasPermissions(ulong playerId, IEnumerable<string> permissions)
```

**参数:**

- `playerId` (`ulong`)
- `permissions` (`IEnumerable\<string\>`)

**返回值:** `bool`

### PlayerHasPermission

```csharp
bool PlayerHasPermission(ulong playerId, string permission)
```

**参数:**

- `playerId` (`ulong`)
- `permission` (`string`)

**返回值:** `bool`

### AddPermission

```csharp
void AddPermission(ulong playerId, string permission)
```

**参数:**

- `playerId` (`ulong`)
- `permission` (`string`)

### RemovePermission

```csharp
void RemovePermission(ulong playerId, string permission)
```

**参数:**

- `playerId` (`ulong`)
- `permission` (`string`)

### AddSubPermission

```csharp
void AddSubPermission(string permission, string subPermission)
```

**参数:**

- `permission` (`string`)
- `subPermission` (`string`)

### RemoveSubPermission

```csharp
void RemoveSubPermission(string permission, string subPermission)
```

**参数:**

- `permission` (`string`)
- `subPermission` (`string`)

### ClearPermission

```csharp
void ClearPermission(ulong playerId)
```

**参数:**

- `playerId` (`ulong`)

