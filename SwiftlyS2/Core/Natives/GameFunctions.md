# 📦 GameFunctions

**命名空间:** `SwiftlyS2.Core.Natives`

**类型:** `class`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `TeleportOffset` | `int` | static | - |
| `CommitSuicideOffset` | `int` | static | - |
| `GetSkeletonInstanceOffset` | `int` | static | - |
| `FindPickerEntityOffset` | `int` | static | - |
| `RemoveWeaponsOffset` | `int` | static | - |
| `GiveNamedItemOffset` | `int` | static | - |
| `DropActiveItemOffset` | `int` | static | - |
| `DropWeaponOffset` | `int` | static | - |
| `SelectWeaponOffset` | `int` | static | - |
| `AddResourceOffset` | `int` | static | - |
| `CollisionRulesChangedOffset` | `int` | static | - |
| `RespawnOffset` | `int` | static | - |
| `GetViewVectorsOffset` | `int` | static | - |

## ⚙️ 方法

### Initialize (静态)

```csharp
void Initialize()
```

### GetVirtualFunction (静态)

```csharp
void* GetVirtualFunction(nint handle, int offset)
```

**参数:**

- `handle` (`nint`)
- `offset` (`int`)

**返回值:** `void*`

### DispatchParticleEffect (静态)

```csharp
void DispatchParticleEffect(string particleName, uint attachmentType, nint entity, byte attachmentPoint, CUtlSymbolLarge attachmentName, bool resetAllParticlesOnEntity, int splitScreenSlot, CRecipientFilter filter)
```

**参数:**

- `particleName` (`string`)
- `attachmentType` (`uint`)
- `entity` (`nint`)
- `attachmentPoint` (`byte`)
- `attachmentName` (`CUtlSymbolLarge`)
- `resetAllParticlesOnEntity` (`bool`)
- `splitScreenSlot` (`int`)
- `filter` (`CRecipientFilter`)

### TerminateRound (静态)

```csharp
void TerminateRound(nint gameRules, uint reason, float delay, uint teamId, uint unk01)
```

**参数:**

- `gameRules` (`nint`)
- `reason` (`uint`)
- `delay` (`float`)
- `teamId` (`uint`)
- `unk01` (`uint`)

### GetWeaponCSDataFromKey (静态)

```csharp
nint GetWeaponCSDataFromKey(int unknown, string key)
```

**参数:**

- `unknown` (`int`)
- `key` (`string`)

**返回值:** `nint`

### FindPickerEntity (静态)

```csharp
nint FindPickerEntity(nint handle, nint controller)
```

**参数:**

- `handle` (`nint`)
- `controller` (`nint`)

**返回值:** `nint`

### GetSkeletonInstance (静态)

```csharp
nint GetSkeletonInstance(nint handle)
```

**参数:**

- `handle` (`nint`)

**返回值:** `nint`

### PawnCommitSuicide (静态)

```csharp
void PawnCommitSuicide(nint pPawn, bool bExplode, bool bForce)
```

**参数:**

- `pPawn` (`nint`)
- `bExplode` (`bool`)
- `bForce` (`bool`)

### SetPlayerControllerPawn (静态)

```csharp
void SetPlayerControllerPawn(nint pController, nint pPawn, bool b1, bool b2, bool b3, bool b4)
```

**参数:**

- `pController` (`nint`)
- `pPawn` (`nint`)
- `b1` (`bool`)
- `b2` (`bool`)
- `b3` (`bool`)
- `b4` (`bool`)

### SetModel (静态)

```csharp
void SetModel(nint pEntity, string model)
```

**参数:**

- `pEntity` (`nint`)
- `model` (`string`)

### TakeDamage (静态)

```csharp
void TakeDamage(nint pEntity, CTakeDamageInfo* info)
```

**参数:**

- `pEntity` (`nint`)
- `info` (`CTakeDamageInfo*`)

### CCSPlayer_ItemServices_RemoveWeapons (静态)

```csharp
void CCSPlayer_ItemServices_RemoveWeapons(nint pThis)
```

**参数:**

- `pThis` (`nint`)

### CCSPlayer_ItemServices_GiveNamedItem (静态)

```csharp
nint CCSPlayer_ItemServices_GiveNamedItem(nint pThis, string name)
```

**参数:**

- `pThis` (`nint`)
- `name` (`string`)

**返回值:** `nint`

### CCSPlayer_ItemServices_DropActiveItem (静态)

```csharp
void CCSPlayer_ItemServices_DropActiveItem(nint pThis, Vector momentum)
```

**参数:**

- `pThis` (`nint`)
- `momentum` (`Vector`)

### CCSPlayer_WeaponServices_DropWeapon (静态)

```csharp
void CCSPlayer_WeaponServices_DropWeapon(nint pThis, nint pWeapon, Vector* momentum)
```

**参数:**

- `pThis` (`nint`)
- `pWeapon` (`nint`)
- `momentum` (`Vector*`)

### CCSPlayer_WeaponServices_SelectWeapon (静态)

```csharp
void CCSPlayer_WeaponServices_SelectWeapon(nint pThis, nint pWeapon)
```

**参数:**

- `pThis` (`nint`)
- `pWeapon` (`nint`)

### CEntityResourceManifest_AddResource (静态)

```csharp
void CEntityResourceManifest_AddResource(nint pThis, string path)
```

**参数:**

- `pThis` (`nint`)
- `path` (`string`)

### SetOrAddAttribute (静态)

```csharp
void SetOrAddAttribute(nint handle, string name, float value)
```

**参数:**

- `handle` (`nint`)
- `name` (`string`)
- `value` (`float`)

### CBaseEntity_CollisionRulesChanged (静态)

```csharp
void CBaseEntity_CollisionRulesChanged(nint pThis)
```

**参数:**

- `pThis` (`nint`)

### CCSPlayerController_Respawn (静态)

```csharp
void CCSPlayerController_Respawn(nint pThis)
```

**参数:**

- `pThis` (`nint`)

### CSmokeGrenadeProjectile_EmitGrenade (静态)

```csharp
nint CSmokeGrenadeProjectile_EmitGrenade(Vector pos, QAngle angle, Vector velocity, nint owner, Team team, uint itemdefindex)
```

**参数:**

- `pos` (`Vector`)
- `angle` (`QAngle`)
- `velocity` (`Vector`)
- `owner` (`nint`)
- `team` (`Team`)
- `itemdefindex` (`uint`)

**返回值:** `nint`

### CFlashbangProjectile_EmitGrenade (静态)

```csharp
nint CFlashbangProjectile_EmitGrenade(Vector pos, QAngle angle, Vector velocity, nint owner, uint itemdefindex)
```

**参数:**

- `pos` (`Vector`)
- `angle` (`QAngle`)
- `velocity` (`Vector`)
- `owner` (`nint`)
- `itemdefindex` (`uint`)

**返回值:** `nint`

### CHEGrenadeProjectile_EmitGrenade (静态)

```csharp
nint CHEGrenadeProjectile_EmitGrenade(Vector pos, QAngle angle, Vector velocity, nint owner, uint itemdefindex)
```

**参数:**

- `pos` (`Vector`)
- `angle` (`QAngle`)
- `velocity` (`Vector`)
- `owner` (`nint`)
- `itemdefindex` (`uint`)

**返回值:** `nint`

### CDecoyProjectile_EmitGrenade (静态)

```csharp
nint CDecoyProjectile_EmitGrenade(Vector pos, QAngle angle, Vector velocity, nint owner, uint itemdefindex)
```

**参数:**

- `pos` (`Vector`)
- `angle` (`QAngle`)
- `velocity` (`Vector`)
- `owner` (`nint`)
- `itemdefindex` (`uint`)

**返回值:** `nint`

### CMolotovProjectile_EmitGrenade (静态)

```csharp
nint CMolotovProjectile_EmitGrenade(Vector pos, QAngle angle, Vector velocity, nint owner, uint itemdefindex)
```

**参数:**

- `pos` (`Vector`)
- `angle` (`QAngle`)
- `velocity` (`Vector`)
- `owner` (`nint`)
- `itemdefindex` (`uint`)

**返回值:** `nint`

### CGameRules_GetViewVectors (静态)

```csharp
CViewVectors* CGameRules_GetViewVectors(nint pThis)
```

**参数:**

- `pThis` (`nint`)

**返回值:** `CViewVectors*`

