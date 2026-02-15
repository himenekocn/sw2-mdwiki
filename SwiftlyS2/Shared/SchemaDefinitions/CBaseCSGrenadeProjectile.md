# 🔌 CBaseCSGrenadeProjectile

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseGrenade`

**实现接口:** `ISchemaClass\<CBaseCSGrenadeProjectile\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `InitialPosition` | `ref Vector` | get | - |
| `InitialVelocity` | `ref Vector` | get | - |
| `Bounces` | `ref int` | get | - |
| `ExplodeEffectIndex` | `ref CStrongHandle\<InfoForResourceTypeIParticleSystemDefinition\>` | get | - |
| `ExplodeEffectTickBegin` | `ref int` | get | - |
| `ExplodeEffectOrigin` | `ref Vector` | get | - |
| `SpawnTime` | `GameTime_t` | get | - |
| `OGSExtraFlags` | `ref byte` | get | - |
| `DetonationRecorded` | `ref bool` | get | - |
| `ItemIndex` | `ref ushort` | get | - |
| `OriginalSpawnLocation` | `ref Vector` | get | - |
| `LastBounceSoundTime` | `GameTime_t` | get | - |
| `GrenadeSpin` | `SchemaUntypedField` | get | - |
| `LastHitSurfaceNormal` | `ref Vector` | get | - |
| `TicksAtZeroVelocity` | `ref int` | get | - |
| `HasEverHitEnemy` | `ref bool` | get | - |

## ⚙️ 方法

### InitialPositionUpdated

```csharp
void InitialPositionUpdated()
```

### InitialVelocityUpdated

```csharp
void InitialVelocityUpdated()
```

### BouncesUpdated

```csharp
void BouncesUpdated()
```

### ExplodeEffectIndexUpdated

```csharp
void ExplodeEffectIndexUpdated()
```

### ExplodeEffectTickBeginUpdated

```csharp
void ExplodeEffectTickBeginUpdated()
```

### ExplodeEffectOriginUpdated

```csharp
void ExplodeEffectOriginUpdated()
```

