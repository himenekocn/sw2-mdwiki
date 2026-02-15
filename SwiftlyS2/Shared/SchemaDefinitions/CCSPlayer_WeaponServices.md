# 🔌 CCSPlayer_WeaponServices

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CPlayer_WeaponServices`

**实现接口:** `ISchemaClass\<CCSPlayer_WeaponServices\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `NextAttack` | `GameTime_t` | get | - |
| `IsLookingAtWeapon` | `ref bool` | get | - |
| `IsHoldingLookAtWeapon` | `ref bool` | get | - |
| `SavedWeapon` | `ref CHandle\<CBasePlayerWeapon\>` | get | - |
| `TimeToMelee` | `ref int` | get | - |
| `TimeToSecondary` | `ref int` | get | - |
| `TimeToPrimary` | `ref int` | get | - |
| `TimeToSniperRifle` | `ref int` | get | - |
| `IsBeingGivenItem` | `ref bool` | get | - |
| `IsPickingUpItemWithUse` | `ref bool` | get | - |
| `PickedUpWeapon` | `ref bool` | get | - |
| `DisableAutoDeploy` | `ref bool` | get | - |
| `IsPickingUpGroundWeapon` | `ref bool` | get | - |
| `NetworkAnimTiming` | `ref CUtlVector\<byte\>` | get | - |
| `BlockInspectUntilNextGraphUpdate` | `ref bool` | get | - |

## ⚙️ 方法

### NextAttackUpdated

```csharp
void NextAttackUpdated()
```

### IsLookingAtWeaponUpdated

```csharp
void IsLookingAtWeaponUpdated()
```

### IsHoldingLookAtWeaponUpdated

```csharp
void IsHoldingLookAtWeaponUpdated()
```

### NetworkAnimTimingUpdated

```csharp
void NetworkAnimTimingUpdated()
```

### BlockInspectUntilNextGraphUpdateUpdated

```csharp
void BlockInspectUntilNextGraphUpdateUpdated()
```

