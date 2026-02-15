# 🔌 CParticleSystem

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseModelEntity`

**实现接口:** `ISchemaClass\<CParticleSystem\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SnapshotFileName` | `string` | get, set | - |
| `Active` | `ref bool` | get | - |
| `Frozen` | `ref bool` | get | - |
| `FreezeTransitionDuration` | `ref float` | get | - |
| `StopType` | `ref int` | get | - |
| `AnimateDuringGameplayPause` | `ref bool` | get | - |
| `EffectIndex` | `ref CStrongHandle\<InfoForResourceTypeIParticleSystemDefinition\>` | get | - |
| `StartTime` | `GameTime_t` | get | - |
| `PreSimTime` | `ref float` | get | - |
| `ServerControlPoints` | `ISchemaFixedArray\<Vector\>` | get | - |
| `ServerControlPointAssignments` | `ISchemaFixedArray\<byte\>` | get | - |
| `ControlPointEnts` | `ISchemaFixedArray\<CHandle\<CBaseEntity\>\>` | get | - |
| `NoSave` | `ref bool` | get | - |
| `NoFreeze` | `ref bool` | get | - |
| `NoRamp` | `ref bool` | get | - |
| `StartActive` | `ref bool` | get | - |
| `EffectName` | `string` | get, set | - |
| `ControlPointNames` | `ISchemaStringFixedArray` | get | - |
| `DataCP` | `ref int` | get | - |
| `DataCPValue` | `ref Vector` | get | - |
| `TintCP` | `ref int` | get | - |
| `Tint` | `ref Color` | get | - |

## ⚙️ 方法

### SnapshotFileNameUpdated

```csharp
void SnapshotFileNameUpdated()
```

### ActiveUpdated

```csharp
void ActiveUpdated()
```

### FrozenUpdated

```csharp
void FrozenUpdated()
```

### FreezeTransitionDurationUpdated

```csharp
void FreezeTransitionDurationUpdated()
```

### StopTypeUpdated

```csharp
void StopTypeUpdated()
```

### AnimateDuringGameplayPauseUpdated

```csharp
void AnimateDuringGameplayPauseUpdated()
```

### EffectIndexUpdated

```csharp
void EffectIndexUpdated()
```

### StartTimeUpdated

```csharp
void StartTimeUpdated()
```

### PreSimTimeUpdated

```csharp
void PreSimTimeUpdated()
```

### ServerControlPointsUpdated

```csharp
void ServerControlPointsUpdated()
```

### ServerControlPointAssignmentsUpdated

```csharp
void ServerControlPointAssignmentsUpdated()
```

### ControlPointEntsUpdated

```csharp
void ControlPointEntsUpdated()
```

### NoSaveUpdated

```csharp
void NoSaveUpdated()
```

### NoFreezeUpdated

```csharp
void NoFreezeUpdated()
```

### NoRampUpdated

```csharp
void NoRampUpdated()
```

