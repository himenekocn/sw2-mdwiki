# 🔌 CTriggerFan

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseTrigger`

**实现接口:** `ISchemaClass\<CTriggerFan\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `FanOriginOffset` | `ref Vector` | get, set | - |
| `Direction` | `ref Vector` | get | - |
| `PushTowardsInfoTarget` | `ref bool` | get | - |
| `PushAwayFromInfoTarget` | `ref bool` | get | - |
| `NoiseDelta` | `ref Quaternion` | get | - |
| `InfoFan` | `ref CHandle\<CInfoFan\>` | get | - |
| `Force` | `ref float` | get | - |
| `Falloff` | `ref bool` | get | - |
| `RampTimer` | `CountdownTimer` | get | - |
| `FanOriginWS` | `ref Vector` | get | - |
| `FanOriginLS` | `ref Vector` | get | - |
| `FanEndLS` | `ref Vector` | get | - |
| `NoiseDirectionTarget` | `ref Vector` | get | - |
| `InfoFan1` | `string` | get, set | - |
| `RopeForceScale` | `ref float` | get | - |
| `ParticleForceScale` | `ref float` | get | - |
| `PlayerForce` | `ref float` | get | - |
| `PlayerWindblock` | `ref bool` | get | - |
| `NPCForce` | `ref float` | get | - |
| `RampTime` | `ref float` | get | - |
| `NoiseDegrees` | `ref float` | get | - |
| `NoiseSpeed` | `ref float` | get | - |
| `PushPlayer` | `ref bool` | get | - |
| `RampDown` | `ref bool` | get | - |
| `ManagerFanIdx` | `ref int` | get | - |

## ⚙️ 方法

### FanOriginOffsetUpdated

```csharp
void FanOriginOffsetUpdated()
```

### DirectionUpdated

```csharp
void DirectionUpdated()
```

### PushTowardsInfoTargetUpdated

```csharp
void PushTowardsInfoTargetUpdated()
```

### PushAwayFromInfoTargetUpdated

```csharp
void PushAwayFromInfoTargetUpdated()
```

### NoiseDeltaUpdated

```csharp
void NoiseDeltaUpdated()
```

### InfoFanUpdated

```csharp
void InfoFanUpdated()
```

### ForceUpdated

```csharp
void ForceUpdated()
```

### FalloffUpdated

```csharp
void FalloffUpdated()
```

### RampTimerUpdated

```csharp
void RampTimerUpdated()
```

