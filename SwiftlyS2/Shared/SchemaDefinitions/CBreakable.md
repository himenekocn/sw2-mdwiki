# 🔌 CBreakable

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseModelEntity`

**实现接口:** `ISchemaClass\<CBreakable\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CPropDataComponent` | `CPropDataComponent` | get | - |
| `Material` | `ref Materials` | get | - |
| `Breaker` | `ref CHandle\<CBaseEntity\>` | get | - |
| `Explosion` | `ref Explosions` | get | - |
| `SpawnObject` | `string` | get, set | - |
| `PressureDelay` | `ref float` | get | - |
| `MinHealthDmg` | `ref int` | get | - |
| `PropData` | `string` | get, set | - |
| `ImpactEnergyScale` | `ref float` | get | - |
| `OverrideBlockLOS` | `ref EOverrideBlockLOS_t` | get | - |
| `OnStartDeath` | `ref CEntityIOOutput` | get | - |
| `OnBreak` | `ref CEntityIOOutput` | get | - |
| `OnHealthChanged` | `SchemaUntypedField` | get | - |
| `PerformanceMode` | `ref PerformanceMode_t` | get | - |
| `PhysicsAttacker` | `ref CHandle\<CBasePlayerPawn\>` | get | - |
| `LastPhysicsInfluenceTime` | `GameTime_t` | get | - |

## ⚙️ 方法

### CPropDataComponentUpdated

```csharp
void CPropDataComponentUpdated()
```

