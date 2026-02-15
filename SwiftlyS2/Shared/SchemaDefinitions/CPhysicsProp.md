# 🔌 CPhysicsProp

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBreakableProp`

**实现接口:** `ISchemaClass\<CPhysicsProp\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MotionEnabled` | `ref CEntityIOOutput` | get | - |
| `OnAwakened` | `ref CEntityIOOutput` | get | - |
| `OnAwake` | `ref CEntityIOOutput` | get | - |
| `OnAsleep` | `ref CEntityIOOutput` | get | - |
| `OnPlayerUse` | `ref CEntityIOOutput` | get | - |
| `OnOutOfWorld` | `ref CEntityIOOutput` | get | - |
| `OnPlayerPickup` | `ref CEntityIOOutput` | get | - |
| `ForceNavIgnore` | `ref bool` | get | - |
| `NoNavmeshBlocker` | `ref bool` | get | - |
| `ForceNpcExclude` | `ref bool` | get | - |
| `MassScale` | `ref float` | get | - |
| `BuoyancyScale` | `ref float` | get | - |
| `DamageType` | `ref int` | get | - |
| `DamageToEnableMotion` | `ref int` | get | - |
| `ForceToEnableMotion` | `ref float` | get | - |
| `ThrownByPlayer` | `ref bool` | get | - |
| `DroppedByPlayer` | `ref bool` | get | - |
| `TouchedByPlayer` | `ref bool` | get | - |
| `FirstCollisionAfterLaunch` | `ref bool` | get | - |
| `HasBeenAwakened` | `ref bool` | get | - |
| `IsOverrideProp` | `ref bool` | get | - |
| `LastBurn` | `GameTime_t` | get | - |
| `DynamicContinuousContactBehavior` | `ref DynamicContinuousContactBehavior_t` | get | - |
| `NextCheckDisableMotionContactsTime` | `GameTime_t` | get | - |
| `InitialGlowState` | `ref int` | get | - |
| `GlowRange` | `ref int` | get | - |
| `GlowRangeMin` | `ref int` | get | - |
| `GlowColor` | `ref Color` | get | - |
| `ShouldAutoConvertBackFromDebris` | `ref bool` | get | - |
| `MuteImpactEffects` | `ref bool` | get | - |
| `UpdateNavWhenMoving` | `ref bool` | get | - |
| `ForceNavObstacleCut` | `ref bool` | get | - |
| `AllowObstacleConvexHullMerging` | `ref bool` | get | - |
| `AcceptDamageFromHeldObjects` | `ref bool` | get | - |
| `EnableUseOutput` | `ref bool` | get | - |
| `CrateType` | `ref CPhysicsProp__CrateType_t` | get | - |
| `StrItemClass` | `ISchemaStringFixedArray` | get | - |
| `ItemCount` | `ISchemaFixedArray\<int\>` | get | - |
| `RemovableForAmmoBalancing` | `ref bool` | get | - |
| `Awake` | `ref bool` | get | - |
| `AttachedToReferenceFrame` | `ref bool` | get | - |

## ⚙️ 方法

### AwakeUpdated

```csharp
void AwakeUpdated()
```

