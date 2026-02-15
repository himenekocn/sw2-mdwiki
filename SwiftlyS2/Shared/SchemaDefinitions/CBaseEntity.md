# 🔌 CBaseEntity

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CEntityInstance`

**实现接口:** `ISchemaClass\<CBaseEntity\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CBodyComponent` | `CBodyComponent?` | get | - |
| `NetworkTransmitComponent` | `CNetworkTransmitComponent` | get | - |
| `ThinkFunctions` | `ref CUtlVector\<thinkfunc_t\>` | get | - |
| `CurrentThinkContext` | `ref int` | get | - |
| `LastThinkTick` | `GameTick_t` | get | - |
| `DisabledContextThinks` | `ref bool` | get | - |
| `IsSteadyState` | `SchemaUntypedField` | get | - |
| `LastNetworkChange` | `ref float` | get | - |
| `ResponseContexts` | `ref CUtlVector\<ResponseContext_t\>` | get | - |
| `ResponseContext` | `string` | get, set | - |
| `Health` | `ref int` | get | - |
| `MaxHealth` | `ref int` | get | - |
| `LifeState` | `ref byte` | get | - |
| `DamageAccumulator` | `ref float` | get | - |
| `TakesDamage` | `ref bool` | get | - |
| `TakeDamageFlags` | `ref TakeDamageFlags_t` | get | - |
| `PlatformType` | `ref EntityPlatformTypes_t` | get | - |
| `MoveCollide` | `ref MoveCollide_t` | get | - |
| `MoveType` | `ref MoveType_t` | get | - |
| `ActualMoveType` | `ref MoveType_t` | get | - |
| `WaterTouch` | `ref byte` | get | - |
| `SlimeTouch` | `ref byte` | get | - |
| `RestoreInHierarchy` | `ref bool` | get | - |
| `Target` | `string` | get, set | - |
| `DamageFilter` | `ref CHandle\<CBaseFilter\>` | get | - |
| `DamageFilterName` | `string` | get, set | - |
| `MoveDoneTime` | `ref float` | get | - |
| `SubclassID` | `ref CUtlStringToken` | get | - |
| `AnimTime` | `ref float` | get | - |
| `SimulationTime` | `ref float` | get | - |
| `CreateTime` | `GameTime_t` | get | - |
| `ClientSideRagdoll` | `ref bool` | get | - |
| `InterpolationFrame` | `ref byte` | get | - |
| `PrevVPhysicsUpdatePos` | `ref Vector` | get | - |
| `TeamNum` | `ref byte` | get | - |
| `Globalname` | `string` | get, set | - |
| `SentToClients` | `ref int` | get | - |
| `Speed` | `ref float` | get | - |
| `UniqueHammerID` | `string` | get, set | - |
| `Spawnflags` | `ref uint` | get | - |
| `NextThinkTick` | `GameTick_t` | get | - |
| `SimulationTick` | `ref int` | get | - |
| `OnKilled` | `ref CEntityIOOutput` | get | - |
| `Flags` | `ref uint` | get | - |
| `AbsVelocity` | `ref Vector` | get | - |
| `Velocity` | `CNetworkVelocityVector` | get | - |
| `BaseVelocity` | `ref Vector` | get | - |
| `PushEnumCount` | `ref int` | get | - |
| `Collision` | `CCollisionProperty?` | get | - |
| `EffectEntity` | `ref CHandle\<CBaseEntity\>` | get | - |
| `OwnerEntity` | `ref CHandle\<CBaseEntity\>` | get | - |
| `Effects` | `ref uint` | get | - |
| `GroundEntity` | `ref CHandle\<CBaseEntity\>` | get | - |
| `GroundBodyIndex` | `ref int` | get | - |
| `Friction` | `ref float` | get | - |
| `Elasticity` | `ref float` | get | - |
| `GravityScale` | `ref float` | get | - |
| `TimeScale` | `ref float` | get | - |
| `WaterLevel` | `ref float` | get | - |
| `GravityDisabled` | `ref bool` | get | - |
| `AnimatedEveryTick` | `ref bool` | get | - |
| `ActualGravityScale` | `ref float` | get | - |
| `GravityActuallyDisabled` | `ref bool` | get | - |
| `DisableLowViolence` | `ref bool` | get | - |
| `WaterType` | `ref byte` | get | - |
| `EFlags` | `ref int` | get | - |
| `OnUser1` | `ref CEntityIOOutput` | get | - |
| `OnUser2` | `ref CEntityIOOutput` | get | - |
| `OnUser3` | `ref CEntityIOOutput` | get | - |
| `OnUser4` | `ref CEntityIOOutput` | get | - |
| `InitialTeamNum` | `ref int` | get | - |
| `NavIgnoreUntilTime` | `GameTime_t` | get | - |
| `AngVelocity` | `ref QAngle` | get | - |
| `NetworkQuantizeOriginAndAngles` | `ref bool` | get | - |
| `LagCompensate` | `ref bool` | get | - |
| `Blocker` | `ref CHandle\<CBaseEntity\>` | get | - |
| `LocalTime` | `ref float` | get | - |
| `VPhysicsUpdateLocalTime` | `ref float` | get | - |
| `BloodType` | `ref BloodType` | get | - |
| `PulseGraphInstance` | `CPulseGraphInstance_ServerEntity?` | get | - |

## ⚙️ 方法

### CBodyComponentUpdated

```csharp
void CBodyComponentUpdated()
```

### HealthUpdated

```csharp
void HealthUpdated()
```

### MaxHealthUpdated

```csharp
void MaxHealthUpdated()
```

### LifeStateUpdated

```csharp
void LifeStateUpdated()
```

### TakesDamageUpdated

```csharp
void TakesDamageUpdated()
```

### TakeDamageFlagsUpdated

```csharp
void TakeDamageFlagsUpdated()
```

### PlatformTypeUpdated

```csharp
void PlatformTypeUpdated()
```

### MoveCollideUpdated

```csharp
void MoveCollideUpdated()
```

### MoveTypeUpdated

```csharp
void MoveTypeUpdated()
```

### SubclassIDUpdated

```csharp
void SubclassIDUpdated()
```

### AnimTimeUpdated

```csharp
void AnimTimeUpdated()
```

### SimulationTimeUpdated

```csharp
void SimulationTimeUpdated()
```

### CreateTimeUpdated

```csharp
void CreateTimeUpdated()
```

### ClientSideRagdollUpdated

```csharp
void ClientSideRagdollUpdated()
```

### InterpolationFrameUpdated

```csharp
void InterpolationFrameUpdated()
```

### TeamNumUpdated

```csharp
void TeamNumUpdated()
```

### SpeedUpdated

```csharp
void SpeedUpdated()
```

### SpawnflagsUpdated

```csharp
void SpawnflagsUpdated()
```

### NextThinkTickUpdated

```csharp
void NextThinkTickUpdated()
```

### FlagsUpdated

```csharp
void FlagsUpdated()
```

### VelocityUpdated

```csharp
void VelocityUpdated()
```

### BaseVelocityUpdated

```csharp
void BaseVelocityUpdated()
```

### EffectEntityUpdated

```csharp
void EffectEntityUpdated()
```

### OwnerEntityUpdated

```csharp
void OwnerEntityUpdated()
```

### EffectsUpdated

```csharp
void EffectsUpdated()
```

### GroundEntityUpdated

```csharp
void GroundEntityUpdated()
```

### GroundBodyIndexUpdated

```csharp
void GroundBodyIndexUpdated()
```

### FrictionUpdated

```csharp
void FrictionUpdated()
```

### ElasticityUpdated

```csharp
void ElasticityUpdated()
```

### GravityScaleUpdated

```csharp
void GravityScaleUpdated()
```

### TimeScaleUpdated

```csharp
void TimeScaleUpdated()
```

### WaterLevelUpdated

```csharp
void WaterLevelUpdated()
```

### GravityDisabledUpdated

```csharp
void GravityDisabledUpdated()
```

### AnimatedEveryTickUpdated

```csharp
void AnimatedEveryTickUpdated()
```

### NavIgnoreUntilTimeUpdated

```csharp
void NavIgnoreUntilTimeUpdated()
```

### BloodTypeUpdated

```csharp
void BloodTypeUpdated()
```

