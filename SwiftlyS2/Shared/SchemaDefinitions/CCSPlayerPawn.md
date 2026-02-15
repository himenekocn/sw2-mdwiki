# 🔌 CCSPlayerPawn

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CCSPlayerPawnBase`

**实现接口:** `ISchemaClass\<CCSPlayerPawn\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `BulletServices` | `CCSPlayer_BulletServices?` | get | - |
| `HostageServices` | `CCSPlayer_HostageServices?` | get | - |
| `BuyServices` | `CCSPlayer_BuyServices?` | get | - |
| `ActionTrackingServices` | `CCSPlayer_ActionTrackingServices?` | get | - |
| `RadioServices` | `CCSPlayer_RadioServices?` | get | - |
| `DamageReactServices` | `CCSPlayer_DamageReactServices?` | get | - |
| `CharacterDefIndex` | `ref ushort` | get | - |
| `HasFemaleVoice` | `ref bool` | get | - |
| `StrVOPrefix` | `string` | get, set | - |
| `LastPlaceName` | `string` | get, set | - |
| `InHostageResetZone` | `ref bool` | get, set | - |
| `InBuyZone` | `ref bool` | get | - |
| `TouchingBuyZones` | `ref CUtlVector\<CHandle\<CBaseEntity\>\>` | get | - |
| `WasInBuyZone` | `ref bool` | get | - |
| `InHostageRescueZone` | `ref bool` | get | - |
| `InBombZone` | `ref bool` | get | - |
| `WasInHostageRescueZone` | `ref bool` | get | - |
| `RetakesOffering` | `ref int` | get | - |
| `RetakesOfferingCard` | `ref int` | get | - |
| `RetakesHasDefuseKit` | `ref bool` | get | - |
| `RetakesMVPLastRound` | `ref bool` | get | - |
| `RetakesMVPBoostItem` | `ref int` | get | - |
| `RetakesMVPBoostExtraUtility` | `ref loadout_slot_t` | get | - |
| `HealthShotBoostExpirationTime` | `GameTime_t` | get | - |
| `LandingTimeSeconds` | `ref float` | get | - |
| `AimPunchAngle` | `ref QAngle` | get | - |
| `AimPunchAngleVel` | `ref QAngle` | get | - |
| `AimPunchTickBase` | `GameTick_t` | get | - |
| `AimPunchTickFraction` | `ref float` | get | - |
| `AimPunchCache` | `ref CUtlVector\<QAngle\>` | get | - |
| `IsBuyMenuOpen` | `ref bool` | get | - |
| `LastLandTime` | `GameTime_t` | get | - |
| `OnGroundLastTick` | `ref bool` | get | - |
| `PlayerLocked` | `ref int` | get | - |
| `TimeOfLastInjury` | `GameTime_t` | get | - |
| `NextSprayDecalTime` | `GameTime_t` | get | - |
| `NextSprayDecalTimeExpedited` | `ref bool` | get | - |
| `RagdollDamageBone` | `ref int` | get | - |
| `RagdollDamageForce` | `ref Vector` | get | - |
| `RagdollDamagePosition` | `ref Vector` | get | - |
| `RagdollDamageWeaponName` | `string` | get, set | - |
| `RagdollDamageHeadshot` | `ref bool` | get | - |
| `RagdollServerOrigin` | `ref Vector` | get | - |
| `EconGloves` | `CEconItemView` | get | - |
| `EconGlovesChanged` | `ref byte` | get | - |
| `DeathEyeAngles` | `ref QAngle` | get | - |
| `SkipOneHeadConstraintUpdate` | `ref bool` | get | - |
| `LeftHanded` | `ref bool` | get | - |
| `SwitchedHandednessTime` | `GameTime_t` | get | - |
| `ViewmodelOffsetX` | `ref float` | get, set | - |
| `ViewmodelOffsetY` | `ref float` | get, set | - |
| `ViewmodelOffsetZ` | `ref float` | get, set | - |
| `ViewmodelFOV` | `ref float` | get | - |
| `IsWalking` | `ref bool` | get | - |
| `LastGivenDefuserTime` | `ref float` | get | - |
| `LastGivenBombTime` | `ref float` | get | - |
| `DealtDamageToEnemyMostRecentTimestamp` | `ref float` | get | - |
| `DisplayHistoryBits` | `ref uint` | get | - |
| `LastAttackedTeammate` | `ref float` | get | - |
| `AllowAutoFollowTime` | `GameTime_t` | get | - |
| `ResetArmorNextSpawn` | `ref bool` | get, set | - |
| `LastKillerIndex` | `ref uint` | get | - |
| `EntitySpottedState` | `EntitySpottedState_t` | get | - |
| `SpotRules` | `ref int` | get | - |
| `IsScoped` | `ref bool` | get | - |
| `ResumeZoom` | `ref bool` | get | - |
| `IsDefusing` | `ref bool` | get | - |
| `IsGrabbingHostage` | `ref bool` | get | - |
| `BlockingUseActionInProgress` | `ref CSPlayerBlockingUseAction_t` | get | - |
| `EmitSoundTime` | `GameTime_t` | get | - |
| `InNoDefuseArea` | `ref bool` | get | - |
| `BombSiteIndex` | `ref uint` | get | - |
| `WhichBombZone` | `ref int` | get | - |
| `InBombZoneTrigger` | `ref bool` | get | - |
| `WasInBombZoneTrigger` | `ref bool` | get | - |
| `ShotsFired` | `ref int` | get | - |
| `FlinchStack` | `ref float` | get | - |
| `VelocityModifier` | `ref float` | get | - |
| `HitHeading` | `ref float` | get | - |
| `HitBodyPart` | `ref int` | get | - |
| `TotalBulletForce` | `ref Vector` | get | - |
| `WaitForNoAttack` | `ref bool` | get | - |
| `IgnoreLadderJumpTime` | `ref float` | get | - |
| `KilledByHeadshot` | `ref bool` | get | - |
| `LastHitBox` | `ref int` | get | - |
| `Bot` | `CCSBot?` | get | - |
| `BotAllowActive` | `ref bool` | get | - |
| `ThirdPersonHeading` | `ref QAngle` | get | - |
| `SlopeDropOffset` | `ref float` | get, set | - |
| `SlopeDropHeight` | `ref float` | get | - |
| `HeadConstraintOffset` | `ref Vector` | get, set | - |
| `LastPickupPriority` | `ref int` | get | - |
| `LastPickupPriorityTime` | `ref float` | get | - |
| `ArmorValue` | `ref int` | get | - |
| `CurrentEquipmentValue` | `ref ushort` | get | - |
| `RoundStartEquipmentValue` | `ref ushort` | get | - |
| `FreezetimeEndEquipmentValue` | `ref ushort` | get | - |
| `LastWeaponFireUsercmd` | `ref int` | get | - |
| `IsSpawning` | `ref bool` | get | - |
| `DeathFlags` | `ref int` | get | - |
| `HasDeathInfo` | `ref bool` | get | - |
| `DeathInfoTime` | `ref float` | get | - |
| `DeathInfoOrigin` | `ref Vector` | get | - |
| `PlayerPatchEconIndices` | `ISchemaFixedArray\<uint\>` | get | - |
| `GunGameImmunityColor` | `ref Color` | get | - |
| `GrenadeParameterStashTime` | `GameTime_t` | get | - |
| `GrenadeParametersStashed` | `ref bool` | get | - |
| `StashedShootAngles` | `ref QAngle` | get | - |
| `StashedGrenadeThrowPosition` | `ref Vector` | get | - |
| `StashedVelocity` | `ref Vector` | get | - |
| `ShootAngleHistory` | `ISchemaFixedArray\<QAngle\>` | get | - |
| `ThrowPositionHistory` | `ISchemaFixedArray\<Vector\>` | get | - |
| `VelocityHistory` | `ISchemaFixedArray\<Vector\>` | get | - |
| `PredictedDamageTags` | `ref CUtlVector\<PredictedDamageTag_t\>` | get | - |
| `HighestAppliedDamageTagTick` | `ref int` | get | - |
| `CommittingSuicideOnTeamChange` | `ref bool` | get | - |
| `WasNotKilledNaturally` | `ref bool` | get | - |
| `ImmuneToGunGameDamageTime` | `GameTime_t` | get | - |
| `GunGameImmunity` | `ref bool` | get | - |
| `MolotovDamageTime` | `ref float` | get | - |
| `EyeAngles` | `ref QAngle` | get | - |

## ⚙️ 方法

### BulletServicesUpdated

```csharp
void BulletServicesUpdated()
```

### HostageServicesUpdated

```csharp
void HostageServicesUpdated()
```

### BuyServicesUpdated

```csharp
void BuyServicesUpdated()
```

### ActionTrackingServicesUpdated

```csharp
void ActionTrackingServicesUpdated()
```

### HasFemaleVoiceUpdated

```csharp
void HasFemaleVoiceUpdated()
```

### LastPlaceNameUpdated

```csharp
void LastPlaceNameUpdated()
```

### InBuyZoneUpdated

```csharp
void InBuyZoneUpdated()
```

### InHostageRescueZoneUpdated

```csharp
void InHostageRescueZoneUpdated()
```

### InBombZoneUpdated

```csharp
void InBombZoneUpdated()
```

### RetakesOfferingUpdated

```csharp
void RetakesOfferingUpdated()
```

### RetakesOfferingCardUpdated

```csharp
void RetakesOfferingCardUpdated()
```

### RetakesHasDefuseKitUpdated

```csharp
void RetakesHasDefuseKitUpdated()
```

### RetakesMVPLastRoundUpdated

```csharp
void RetakesMVPLastRoundUpdated()
```

### RetakesMVPBoostItemUpdated

```csharp
void RetakesMVPBoostItemUpdated()
```

### RetakesMVPBoostExtraUtilityUpdated

```csharp
void RetakesMVPBoostExtraUtilityUpdated()
```

### HealthShotBoostExpirationTimeUpdated

```csharp
void HealthShotBoostExpirationTimeUpdated()
```

### AimPunchAngleUpdated

```csharp
void AimPunchAngleUpdated()
```

### AimPunchAngleVelUpdated

```csharp
void AimPunchAngleVelUpdated()
```

### AimPunchTickBaseUpdated

```csharp
void AimPunchTickBaseUpdated()
```

### AimPunchTickFractionUpdated

```csharp
void AimPunchTickFractionUpdated()
```

### IsBuyMenuOpenUpdated

```csharp
void IsBuyMenuOpenUpdated()
```

### TimeOfLastInjuryUpdated

```csharp
void TimeOfLastInjuryUpdated()
```

### NextSprayDecalTimeUpdated

```csharp
void NextSprayDecalTimeUpdated()
```

### RagdollDamageBoneUpdated

```csharp
void RagdollDamageBoneUpdated()
```

### RagdollDamageForceUpdated

```csharp
void RagdollDamageForceUpdated()
```

### RagdollDamagePositionUpdated

```csharp
void RagdollDamagePositionUpdated()
```

### RagdollDamageWeaponNameUpdated

```csharp
void RagdollDamageWeaponNameUpdated()
```

### RagdollDamageHeadshotUpdated

```csharp
void RagdollDamageHeadshotUpdated()
```

### RagdollServerOriginUpdated

```csharp
void RagdollServerOriginUpdated()
```

### EconGlovesUpdated

```csharp
void EconGlovesUpdated()
```

### EconGlovesChangedUpdated

```csharp
void EconGlovesChangedUpdated()
```

### DeathEyeAnglesUpdated

```csharp
void DeathEyeAnglesUpdated()
```

### LeftHandedUpdated

```csharp
void LeftHandedUpdated()
```

### SwitchedHandednessTimeUpdated

```csharp
void SwitchedHandednessTimeUpdated()
```

### ViewmodelOffsetXUpdated

```csharp
void ViewmodelOffsetXUpdated()
```

### ViewmodelOffsetYUpdated

```csharp
void ViewmodelOffsetYUpdated()
```

### ViewmodelOffsetZUpdated

```csharp
void ViewmodelOffsetZUpdated()
```

### ViewmodelFOVUpdated

```csharp
void ViewmodelFOVUpdated()
```

### IsWalkingUpdated

```csharp
void IsWalkingUpdated()
```

### LastKillerIndexUpdated

```csharp
void LastKillerIndexUpdated()
```

### EntitySpottedStateUpdated

```csharp
void EntitySpottedStateUpdated()
```

### IsScopedUpdated

```csharp
void IsScopedUpdated()
```

### ResumeZoomUpdated

```csharp
void ResumeZoomUpdated()
```

### IsDefusingUpdated

```csharp
void IsDefusingUpdated()
```

### IsGrabbingHostageUpdated

```csharp
void IsGrabbingHostageUpdated()
```

### BlockingUseActionInProgressUpdated

```csharp
void BlockingUseActionInProgressUpdated()
```

### EmitSoundTimeUpdated

```csharp
void EmitSoundTimeUpdated()
```

### InNoDefuseAreaUpdated

```csharp
void InNoDefuseAreaUpdated()
```

### WhichBombZoneUpdated

```csharp
void WhichBombZoneUpdated()
```

### ShotsFiredUpdated

```csharp
void ShotsFiredUpdated()
```

### FlinchStackUpdated

```csharp
void FlinchStackUpdated()
```

### VelocityModifierUpdated

```csharp
void VelocityModifierUpdated()
```

### HitHeadingUpdated

```csharp
void HitHeadingUpdated()
```

### HitBodyPartUpdated

```csharp
void HitBodyPartUpdated()
```

### WaitForNoAttackUpdated

```csharp
void WaitForNoAttackUpdated()
```

### KilledByHeadshotUpdated

```csharp
void KilledByHeadshotUpdated()
```

### ThirdPersonHeadingUpdated

```csharp
void ThirdPersonHeadingUpdated()
```

### SlopeDropOffsetUpdated

```csharp
void SlopeDropOffsetUpdated()
```

### SlopeDropHeightUpdated

```csharp
void SlopeDropHeightUpdated()
```

### HeadConstraintOffsetUpdated

```csharp
void HeadConstraintOffsetUpdated()
```

### ArmorValueUpdated

```csharp
void ArmorValueUpdated()
```

### CurrentEquipmentValueUpdated

```csharp
void CurrentEquipmentValueUpdated()
```

### RoundStartEquipmentValueUpdated

```csharp
void RoundStartEquipmentValueUpdated()
```

### FreezetimeEndEquipmentValueUpdated

```csharp
void FreezetimeEndEquipmentValueUpdated()
```

### PlayerPatchEconIndicesUpdated

```csharp
void PlayerPatchEconIndicesUpdated()
```

### GunGameImmunityColorUpdated

```csharp
void GunGameImmunityColorUpdated()
```

### PredictedDamageTagsUpdated

```csharp
void PredictedDamageTagsUpdated()
```

### ImmuneToGunGameDamageTimeUpdated

```csharp
void ImmuneToGunGameDamageTimeUpdated()
```

### GunGameImmunityUpdated

```csharp
void GunGameImmunityUpdated()
```

### MolotovDamageTimeUpdated

```csharp
void MolotovDamageTimeUpdated()
```

### EyeAnglesUpdated

```csharp
void EyeAnglesUpdated()
```

