# 🔌 CPathParticleRope

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseEntity`

**实现接口:** `ISchemaClass\<CPathParticleRope\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `StartActive` | `ref bool` | get | - |
| `MaxSimulationTime` | `ref float` | get | - |
| `EffectName` | `string` | get, set | - |
| `PathNodes_Name` | `ref CUtlVector\<SchemaUntypedField\>` | get | - |
| `ParticleSpacing` | `ref float` | get | - |
| `Slack` | `ref float` | get | - |
| `Radius` | `ref float` | get | - |
| `ColorTint` | `ref Color` | get | - |
| `EffectState` | `ref int` | get | - |
| `EffectIndex` | `ref CStrongHandle\<InfoForResourceTypeIParticleSystemDefinition\>` | get | - |
| `PathNodes_Position` | `ref CUtlVector\<Vector\>` | get | - |
| `PathNodes_TangentIn` | `ref CUtlVector\<Vector\>` | get | - |
| `PathNodes_TangentOut` | `ref CUtlVector\<Vector\>` | get | - |
| `PathNodes_Color` | `ref CUtlVector\<Vector\>` | get | - |
| `PathNodes_PinEnabled` | `ref CUtlVector\<bool\>` | get | - |
| `PathNodes_RadiusScale` | `ref CUtlVector\<float\>` | get | - |

## ⚙️ 方法

### ParticleSpacingUpdated

```csharp
void ParticleSpacingUpdated()
```

### SlackUpdated

```csharp
void SlackUpdated()
```

### RadiusUpdated

```csharp
void RadiusUpdated()
```

### ColorTintUpdated

```csharp
void ColorTintUpdated()
```

### EffectStateUpdated

```csharp
void EffectStateUpdated()
```

### EffectIndexUpdated

```csharp
void EffectIndexUpdated()
```

### PathNodes_PositionUpdated

```csharp
void PathNodes_PositionUpdated()
```

### PathNodes_TangentInUpdated

```csharp
void PathNodes_TangentInUpdated()
```

### PathNodes_TangentOutUpdated

```csharp
void PathNodes_TangentOutUpdated()
```

### PathNodes_ColorUpdated

```csharp
void PathNodes_ColorUpdated()
```

### PathNodes_PinEnabledUpdated

```csharp
void PathNodes_PinEnabledUpdated()
```

### PathNodes_RadiusScaleUpdated

```csharp
void PathNodes_RadiusScaleUpdated()
```

