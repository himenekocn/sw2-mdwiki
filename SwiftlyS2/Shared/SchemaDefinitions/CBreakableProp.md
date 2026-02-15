# 🔌 CBreakableProp

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseProp`

**实现接口:** `ISchemaClass\<CBreakableProp\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CPropDataComponent` | `CPropDataComponent` | get | - |
| `OnStartDeath` | `ref CEntityIOOutput` | get | - |
| `OnBreak` | `ref CEntityIOOutput` | get | - |
| `OnHealthChanged` | `SchemaUntypedField` | get | - |
| `OnTakeDamage` | `ref CEntityIOOutput` | get | - |
| `ImpactEnergyScale` | `ref float` | get | - |
| `MinHealthDmg` | `ref int` | get | - |
| `PreferredCarryAngles` | `ref QAngle` | get | - |
| `PressureDelay` | `ref float` | get | - |
| `DefBurstScale` | `ref float` | get | - |
| `DefBurstOffset` | `ref Vector` | get, set | - |
| `Breaker` | `ref CHandle\<CBaseEntity\>` | get | - |
| `PerformanceMode` | `ref PerformanceMode_t` | get | - |
| `PreventDamageBeforeTime` | `GameTime_t` | get | - |
| `BreakableContentsType` | `ref BreakableContentsType_t` | get | - |
| `StrBreakableContentsPropGroupOverride` | `string` | get, set | - |
| `StrBreakableContentsParticleOverride` | `string` | get, set | - |
| `HasBreakPiecesOrCommands` | `ref bool` | get | - |
| `ExplodeDamage` | `ref float` | get | - |
| `ExplodeRadius` | `ref float` | get | - |
| `ExplosionType` | `ref BaseExplosionTypes_t` | get | - |
| `ExplosionDelay` | `ref float` | get | - |
| `ExplosionBuildupSound` | `string` | get, set | - |
| `ExplosionCustomEffect` | `string` | get, set | - |
| `ExplosionCustomSound` | `string` | get, set | - |
| `ExplosionModifier` | `string` | get, set | - |
| `PhysicsAttacker` | `ref CHandle\<CBasePlayerPawn\>` | get | - |
| `LastPhysicsInfluenceTime` | `GameTime_t` | get | - |
| `DefaultFadeScale` | `ref float` | get | - |
| `LastAttacker` | `ref CHandle\<CBaseEntity\>` | get | - |
| `PuntSound` | `string` | get, set | - |
| `UsePuntSound` | `ref bool` | get | - |
| `OriginalBlockLOS` | `ref bool` | get | - |

## ⚙️ 方法

### CPropDataComponentUpdated

```csharp
void CPropDataComponentUpdated()
```

