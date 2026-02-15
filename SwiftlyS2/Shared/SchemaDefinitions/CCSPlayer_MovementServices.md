# 🔌 CCSPlayer_MovementServices

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CPlayer_MovementServices_Humanoid`

**实现接口:** `ISchemaClass\<CCSPlayer_MovementServices\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `LadderNormal` | `ref Vector` | get | - |
| `LadderSurfacePropIndex` | `ref int` | get | - |
| `Ducked` | `ref bool` | get | - |
| `DuckAmount` | `ref float` | get | - |
| `DuckSpeed` | `ref float` | get | - |
| `DuckOverride` | `ref bool` | get | - |
| `DesiresDuck` | `ref bool` | get | - |
| `Ducking` | `ref bool` | get | - |
| `DuckOffset` | `ref float` | get, set | - |
| `DuckTimeMsecs` | `ref uint` | get | - |
| `DuckJumpTimeMsecs` | `ref uint` | get | - |
| `JumpTimeMsecs` | `ref uint` | get | - |
| `LastDuckTime` | `ref float` | get | - |
| `LastPositionAtFullCrouchSpeed` | `ref Vector2D` | get | - |
| `DuckUntilOnGround` | `ref bool` | get | - |
| `HasWalkMovedSinceLastJump` | `ref bool` | get | - |
| `InStuckTest` | `ref bool` | get | - |
| `TraceCount` | `ref int` | get | - |
| `StuckLast` | `ref int` | get | - |
| `SpeedCropped` | `ref bool` | get | - |
| `OldWaterLevel` | `ref int` | get | - |
| `WaterEntryTime` | `ref float` | get | - |
| `Forward` | `ref Vector` | get | - |
| `Left` | `ref Vector` | get | - |
| `Up` | `ref Vector` | get | - |
| `GameCodeHasMovedPlayerAfterCommand` | `ref int` | get | - |
| `MadeFootstepNoise` | `ref bool` | get | - |
| `Footsteps` | `ref int` | get | - |
| `StashGrenadeParameterWhen` | `GameTime_t` | get | - |
| `ButtonDownMaskPrev` | `ref ulong` | get | - |
| `OffsetTickCompleteTime` | `ref float` | get, set | - |
| `OffsetTickStashedSpeed` | `ref float` | get, set | - |
| `Stamina` | `ref float` | get | - |
| `HeightAtJumpStart` | `ref float` | get | - |
| `MaxJumpHeightThisJump` | `ref float` | get | - |
| `MaxJumpHeightLastJump` | `ref float` | get | - |
| `StaminaAtJumpStart` | `ref float` | get | - |
| `VelMulAtJumpStart` | `ref float` | get | - |
| `AccumulatedJumpError` | `ref float` | get | - |
| `LegacyJump` | `CCSPlayerLegacyJump` | get | - |
| `ModernJump` | `CCSPlayerModernJump` | get | - |
| `LastJumpTick` | `GameTick_t` | get | - |
| `LastJumpFrac` | `ref float` | get | - |
| `LastJumpVelocityZ` | `ref float` | get | - |
| `JumpApexPending` | `ref bool` | get | - |
| `TicksSinceLastSurfingDetected` | `ref float` | get | - |
| `WasSurfing` | `ref bool` | get | - |
| `InputRotated` | `ref Vector` | get | - |

## ⚙️ 方法

### LadderSurfacePropIndexUpdated

```csharp
void LadderSurfacePropIndexUpdated()
```

### DuckedUpdated

```csharp
void DuckedUpdated()
```

### DuckAmountUpdated

```csharp
void DuckAmountUpdated()
```

### DuckSpeedUpdated

```csharp
void DuckSpeedUpdated()
```

### DuckOverrideUpdated

```csharp
void DuckOverrideUpdated()
```

### DesiresDuckUpdated

```csharp
void DesiresDuckUpdated()
```

### DuckingUpdated

```csharp
void DuckingUpdated()
```

### DuckOffsetUpdated

```csharp
void DuckOffsetUpdated()
```

### DuckTimeMsecsUpdated

```csharp
void DuckTimeMsecsUpdated()
```

### DuckJumpTimeMsecsUpdated

```csharp
void DuckJumpTimeMsecsUpdated()
```

### JumpTimeMsecsUpdated

```csharp
void JumpTimeMsecsUpdated()
```

### LastDuckTimeUpdated

```csharp
void LastDuckTimeUpdated()
```

### GameCodeHasMovedPlayerAfterCommandUpdated

```csharp
void GameCodeHasMovedPlayerAfterCommandUpdated()
```

### StashGrenadeParameterWhenUpdated

```csharp
void StashGrenadeParameterWhenUpdated()
```

### ButtonDownMaskPrevUpdated

```csharp
void ButtonDownMaskPrevUpdated()
```

### OffsetTickCompleteTimeUpdated

```csharp
void OffsetTickCompleteTimeUpdated()
```

### OffsetTickStashedSpeedUpdated

```csharp
void OffsetTickStashedSpeedUpdated()
```

### StaminaUpdated

```csharp
void StaminaUpdated()
```

### LegacyJumpUpdated

```csharp
void LegacyJumpUpdated()
```

### ModernJumpUpdated

```csharp
void ModernJumpUpdated()
```

### LastJumpTickUpdated

```csharp
void LastJumpTickUpdated()
```

### LastJumpFracUpdated

```csharp
void LastJumpFracUpdated()
```

### LastJumpVelocityZUpdated

```csharp
void LastJumpVelocityZUpdated()
```

### JumpApexPendingUpdated

```csharp
void JumpApexPendingUpdated()
```

### WasSurfingUpdated

```csharp
void WasSurfingUpdated()
```

