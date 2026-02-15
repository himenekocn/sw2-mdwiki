# 🔌 CCSWeaponBase

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBasePlayerWeapon`

**实现接口:** `ISchemaClass\<CCSWeaponBase\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Removeable` | `ref bool` | get | - |
| `PlayerAmmoStockOnPickup` | `ref bool` | get | - |
| `RequireUseToTouch` | `ref bool` | get | - |
| `WeaponGameplayAnimState` | `ref WeaponGameplayAnimState` | get | - |
| `WeaponGameplayAnimStateTimestamp` | `GameTime_t` | get | - |
| `InspectCancelCompleteTime` | `GameTime_t` | get | - |
| `InspectPending` | `ref bool` | get | - |
| `InspectShouldLoop` | `ref bool` | get | - |
| `LastEmptySoundCmdNum` | `ref int` | get | - |
| `FireOnEmpty` | `ref bool` | get | - |
| `OnPlayerPickup` | `ref CEntityIOOutput` | get | - |
| `WeaponMode` | `ref CSWeaponMode` | get | - |
| `TurningInaccuracyDelta` | `ref float` | get | - |
| `TurningInaccuracyEyeDirLast` | `ref Vector` | get | - |
| `TurningInaccuracy` | `ref float` | get | - |
| `AccuracyPenalty` | `ref float` | get | - |
| `LastAccuracyUpdateTime` | `GameTime_t` | get | - |
| `AccuracySmoothedForZoom` | `ref float` | get | - |
| `RecoilIndex` | `ref int` | get | - |
| `RecoilIndex1` | `ref float` | get | - |
| `BurstMode` | `ref bool` | get | - |
| `PostponeFireReadyTicks` | `GameTick_t` | get | - |
| `PostponeFireReadyFrac` | `ref float` | get | - |
| `InReload` | `ref bool` | get | - |
| `DroppedAtTime` | `GameTime_t` | get | - |
| `IsHauledBack` | `ref bool` | get | - |
| `SilencerOn` | `ref bool` | get | - |
| `TimeSilencerSwitchComplete` | `GameTime_t` | get | - |
| `WeaponActionPlaybackRate` | `ref float` | get | - |
| `OriginalTeamNumber` | `ref int` | get | - |
| `MostRecentTeamNumber` | `ref int` | get | - |
| `DroppedNearBuyZone` | `ref bool` | get | - |
| `NextAttackRenderTimeOffset` | `ref float` | get, set | - |
| `CanBePickedUp` | `ref bool` | get | - |
| `UseCanOverrideNextOwnerTouchTime` | `ref bool` | get | - |
| `NextOwnerTouchTime` | `GameTime_t` | get | - |
| `NextPrevOwnerTouchTime` | `GameTime_t` | get | - |
| `NextPrevOwnerUseTime` | `GameTime_t` | get | - |
| `PrevOwner` | `ref CHandle\<CCSPlayerPawn\>` | get | - |
| `DropTick` | `GameTick_t` | get | - |
| `WasActiveWeaponWhenDropped` | `ref bool` | get | - |
| `Donated` | `ref bool` | get | - |
| `LastShotTime` | `GameTime_t` | get | - |
| `WasOwnedByCT` | `ref bool` | get | - |
| `WasOwnedByTerrorist` | `ref bool` | get | - |
| `NumRemoveUnownedWeaponThink` | `ref int` | get | - |
| `IronSightController` | `CIronSightController` | get | - |
| `IronSightMode` | `ref int` | get | - |
| `LastLOSTraceFailureTime` | `GameTime_t` | get | - |
| `WatTickOffset` | `ref float` | get, set | - |
| `LastShakeTime` | `GameTime_t` | get | - |

## ⚙️ 方法

### WeaponGameplayAnimStateUpdated

```csharp
void WeaponGameplayAnimStateUpdated()
```

### WeaponGameplayAnimStateTimestampUpdated

```csharp
void WeaponGameplayAnimStateTimestampUpdated()
```

### InspectCancelCompleteTimeUpdated

```csharp
void InspectCancelCompleteTimeUpdated()
```

### InspectPendingUpdated

```csharp
void InspectPendingUpdated()
```

### InspectShouldLoopUpdated

```csharp
void InspectShouldLoopUpdated()
```

### WeaponModeUpdated

```csharp
void WeaponModeUpdated()
```

### AccuracyPenaltyUpdated

```csharp
void AccuracyPenaltyUpdated()
```

### RecoilIndexUpdated

```csharp
void RecoilIndexUpdated()
```

### RecoilIndex1Updated

```csharp
void RecoilIndex1Updated()
```

### BurstModeUpdated

```csharp
void BurstModeUpdated()
```

### PostponeFireReadyTicksUpdated

```csharp
void PostponeFireReadyTicksUpdated()
```

### PostponeFireReadyFracUpdated

```csharp
void PostponeFireReadyFracUpdated()
```

### InReloadUpdated

```csharp
void InReloadUpdated()
```

### DroppedAtTimeUpdated

```csharp
void DroppedAtTimeUpdated()
```

### IsHauledBackUpdated

```csharp
void IsHauledBackUpdated()
```

### SilencerOnUpdated

```csharp
void SilencerOnUpdated()
```

### TimeSilencerSwitchCompleteUpdated

```csharp
void TimeSilencerSwitchCompleteUpdated()
```

### WeaponActionPlaybackRateUpdated

```csharp
void WeaponActionPlaybackRateUpdated()
```

### OriginalTeamNumberUpdated

```csharp
void OriginalTeamNumberUpdated()
```

### MostRecentTeamNumberUpdated

```csharp
void MostRecentTeamNumberUpdated()
```

### DroppedNearBuyZoneUpdated

```csharp
void DroppedNearBuyZoneUpdated()
```

### NextPrevOwnerUseTimeUpdated

```csharp
void NextPrevOwnerUseTimeUpdated()
```

### PrevOwnerUpdated

```csharp
void PrevOwnerUpdated()
```

### DropTickUpdated

```csharp
void DropTickUpdated()
```

### WasActiveWeaponWhenDroppedUpdated

```csharp
void WasActiveWeaponWhenDroppedUpdated()
```

### LastShotTimeUpdated

```csharp
void LastShotTimeUpdated()
```

### IronSightModeUpdated

```csharp
void IronSightModeUpdated()
```

### WatTickOffsetUpdated

```csharp
void WatTickOffsetUpdated()
```

### LastShakeTimeUpdated

```csharp
void LastShakeTimeUpdated()
```

