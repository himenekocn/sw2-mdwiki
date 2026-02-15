# 🔌 CPointValueRemapper

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseEntity`

**实现接口:** `ISchemaClass\<CPointValueRemapper\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Disabled` | `ref bool` | get | - |
| `UpdateOnClient` | `ref bool` | get | - |
| `InputType` | `ref ValueRemapperInputType_t` | get | - |
| `RemapLineStartName` | `string` | get, set | - |
| `RemapLineEndName` | `string` | get, set | - |
| `RemapLineStart` | `ref CHandle\<CBaseEntity\>` | get | - |
| `RemapLineEnd` | `ref CHandle\<CBaseEntity\>` | get | - |
| `MaximumChangePerSecond` | `ref float` | get | - |
| `DisengageDistance` | `ref float` | get | - |
| `EngageDistance` | `ref float` | get | - |
| `RequiresUseKey` | `ref bool` | get | - |
| `OutputType` | `ref ValueRemapperOutputType_t` | get | - |
| `OutputEntityName` | `string` | get, set | - |
| `OutputEntity2Name` | `string` | get, set | - |
| `OutputEntity3Name` | `string` | get, set | - |
| `OutputEntity4Name` | `string` | get, set | - |
| `OutputEntities` | `ref CUtlVector\<CHandle\<CBaseEntity\>\>` | get | - |
| `HapticsType` | `ref ValueRemapperHapticsType_t` | get | - |
| `MomentumType` | `ref ValueRemapperMomentumType_t` | get | - |
| `MomentumModifier` | `ref float` | get | - |
| `SnapValue` | `ref float` | get | - |
| `CurrentMomentum` | `ref float` | get | - |
| `RatchetType` | `ref ValueRemapperRatchetType_t` | get | - |
| `RatchetOffset` | `ref float` | get, set | - |
| `InputOffset` | `ref float` | get, set | - |
| `Engaged` | `ref bool` | get | - |
| `FirstUpdate` | `ref bool` | get | - |
| `PreviousValue` | `ref float` | get | - |
| `PreviousUpdateTickTime` | `GameTime_t` | get | - |
| `PreviousTestPoint` | `ref Vector` | get | - |
| `UsingPlayer` | `ref CHandle\<CBasePlayerPawn\>` | get | - |
| `CustomOutputValue` | `ref float` | get | - |
| `SoundEngage` | `string` | get, set | - |
| `SoundDisengage` | `string` | get, set | - |
| `SoundReachedValueZero` | `string` | get, set | - |
| `SoundReachedValueOne` | `string` | get, set | - |
| `SoundMovingLoop` | `string` | get, set | - |
| `Position` | `SchemaUntypedField` | get | - |
| `PositionDelta` | `SchemaUntypedField` | get | - |
| `OnReachedValueZero` | `ref CEntityIOOutput` | get | - |
| `OnReachedValueOne` | `ref CEntityIOOutput` | get | - |
| `OnReachedValueCustom` | `ref CEntityIOOutput` | get | - |
| `OnEngage` | `ref CEntityIOOutput` | get | - |
| `OnDisengage` | `ref CEntityIOOutput` | get | - |

## ⚙️ 方法

### DisabledUpdated

```csharp
void DisabledUpdated()
```

### UpdateOnClientUpdated

```csharp
void UpdateOnClientUpdated()
```

### InputTypeUpdated

```csharp
void InputTypeUpdated()
```

### RemapLineStartUpdated

```csharp
void RemapLineStartUpdated()
```

### RemapLineEndUpdated

```csharp
void RemapLineEndUpdated()
```

### MaximumChangePerSecondUpdated

```csharp
void MaximumChangePerSecondUpdated()
```

### DisengageDistanceUpdated

```csharp
void DisengageDistanceUpdated()
```

### EngageDistanceUpdated

```csharp
void EngageDistanceUpdated()
```

### RequiresUseKeyUpdated

```csharp
void RequiresUseKeyUpdated()
```

### OutputTypeUpdated

```csharp
void OutputTypeUpdated()
```

### OutputEntitiesUpdated

```csharp
void OutputEntitiesUpdated()
```

### HapticsTypeUpdated

```csharp
void HapticsTypeUpdated()
```

### MomentumTypeUpdated

```csharp
void MomentumTypeUpdated()
```

### MomentumModifierUpdated

```csharp
void MomentumModifierUpdated()
```

### SnapValueUpdated

```csharp
void SnapValueUpdated()
```

### RatchetTypeUpdated

```csharp
void RatchetTypeUpdated()
```

### InputOffsetUpdated

```csharp
void InputOffsetUpdated()
```

