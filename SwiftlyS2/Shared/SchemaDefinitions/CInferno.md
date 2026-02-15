# 🔌 CInferno

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseModelEntity`

**实现接口:** `ISchemaClass\<CInferno\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `FirePositions` | `ISchemaFixedArray\<Vector\>` | get | - |
| `FireParentPositions` | `ISchemaFixedArray\<Vector\>` | get | - |
| `FireIsBurning` | `ISchemaFixedArray\<bool\>` | get | - |
| `BurnNormal` | `ISchemaFixedArray\<Vector\>` | get | - |
| `FireCount` | `ref int` | get | - |
| `InfernoType` | `ref int` | get | - |
| `FireEffectTickBegin` | `ref int` | get | - |
| `FireLifetime` | `ref float` | get | - |
| `InPostEffectTime` | `ref bool` | get | - |
| `WasCreatedInSmoke` | `ref bool` | get | - |
| `Extent` | `Extent` | get | - |
| `DamageTimer` | `CountdownTimer` | get | - |
| `DamageRampTimer` | `CountdownTimer` | get | - |
| `SplashVelocity` | `ref Vector` | get | - |
| `InitialSplashVelocity` | `ref Vector` | get | - |
| `StartPos` | `ref Vector` | get | - |
| `OriginalSpawnLocation` | `ref Vector` | get | - |
| `ActiveTimer` | `IntervalTimer` | get | - |
| `FireSpawnOffset` | `ref int` | get, set | - |
| `MaxFlames` | `ref int` | get | - |
| `SpreadCount` | `ref int` | get | - |
| `BookkeepingTimer` | `CountdownTimer` | get | - |
| `NextSpreadTimer` | `CountdownTimer` | get | - |
| `SourceItemDefIndex` | `ref ushort` | get | - |

## ⚙️ 方法

### FirePositionsUpdated

```csharp
void FirePositionsUpdated()
```

### FireParentPositionsUpdated

```csharp
void FireParentPositionsUpdated()
```

### FireIsBurningUpdated

```csharp
void FireIsBurningUpdated()
```

### BurnNormalUpdated

```csharp
void BurnNormalUpdated()
```

### FireCountUpdated

```csharp
void FireCountUpdated()
```

### InfernoTypeUpdated

```csharp
void InfernoTypeUpdated()
```

### FireEffectTickBeginUpdated

```csharp
void FireEffectTickBeginUpdated()
```

### FireLifetimeUpdated

```csharp
void FireLifetimeUpdated()
```

### InPostEffectTimeUpdated

```csharp
void InPostEffectTimeUpdated()
```

