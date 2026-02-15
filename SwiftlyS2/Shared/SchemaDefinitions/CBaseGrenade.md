# 🔌 CBaseGrenade

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseFlex`

**实现接口:** `ISchemaClass\<CBaseGrenade\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `OnPlayerPickup` | `ref CEntityIOOutput` | get | - |
| `OnExplode` | `ref CEntityIOOutput` | get | - |
| `HasWarnedAI` | `ref bool` | get | - |
| `IsSmokeGrenade` | `ref bool` | get | - |
| `IsLive` | `ref bool` | get | - |
| `DmgRadius` | `ref float` | get | - |
| `DetonateTime` | `GameTime_t` | get | - |
| `WarnAITime` | `ref float` | get | - |
| `Damage` | `ref float` | get | - |
| `BounceSound` | `string` | get, set | - |
| `ExplosionSound` | `string` | get, set | - |
| `Thrower` | `ref CHandle\<CCSPlayerPawn\>` | get | - |
| `NextAttack` | `GameTime_t` | get | - |
| `OriginalThrower` | `ref CHandle\<CCSPlayerPawn\>` | get | - |

## ⚙️ 方法

### IsLiveUpdated

```csharp
void IsLiveUpdated()
```

### DmgRadiusUpdated

```csharp
void DmgRadiusUpdated()
```

### DetonateTimeUpdated

```csharp
void DetonateTimeUpdated()
```

### DamageUpdated

```csharp
void DamageUpdated()
```

### ThrowerUpdated

```csharp
void ThrowerUpdated()
```

