# 🔌 CHostage

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CHostageExpresserShim`

**实现接口:** `ISchemaClass\<CHostage\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `OnHostageBeginGrab` | `ref CEntityIOOutput` | get | - |
| `OnFirstPickedUp` | `ref CEntityIOOutput` | get | - |
| `OnDroppedNotRescued` | `ref CEntityIOOutput` | get | - |
| `OnRescued` | `ref CEntityIOOutput` | get | - |
| `EntitySpottedState` | `EntitySpottedState_t` | get | - |
| `SpotRules` | `ref int` | get | - |
| `UiHostageSpawnExclusionGroupMask` | `ref uint` | get | - |
| `HostageSpawnRandomFactor` | `ref uint` | get | - |
| `Remove` | `ref bool` | get | - |
| `Vel` | `ref Vector` | get | - |
| `IsRescued` | `ref bool` | get | - |
| `JumpedThisFrame` | `ref bool` | get | - |
| `HostageState` | `ref int` | get | - |
| `Leader` | `ref CHandle\<CBaseEntity\>` | get | - |
| `LastLeader` | `ref CHandle\<CCSPlayerPawnBase\>` | get | - |
| `ReuseTimer` | `CountdownTimer` | get | - |
| `HasBeenUsed` | `ref bool` | get | - |
| `Accel` | `ref Vector` | get | - |
| `IsRunning` | `ref bool` | get | - |
| `IsCrouching` | `ref bool` | get | - |
| `JumpTimer` | `CountdownTimer` | get | - |
| `IsWaitingForLeader` | `ref bool` | get | - |
| `RepathTimer` | `CountdownTimer` | get | - |
| `InhibitDoorTimer` | `CountdownTimer` | get | - |
| `InhibitObstacleAvoidanceTimer` | `CountdownTimer` | get | - |
| `WiggleTimer` | `CountdownTimer` | get | - |
| `IsAdjusted` | `ref bool` | get | - |
| `HandsHaveBeenCut` | `ref bool` | get | - |
| `HostageGrabber` | `ref CHandle\<CCSPlayerPawn\>` | get | - |
| `LastGrabTime` | `GameTime_t` | get | - |
| `PositionWhenStartedDroppingToGround` | `ref Vector` | get | - |
| `GrabbedPos` | `ref Vector` | get | - |
| `RescueStartTime` | `GameTime_t` | get | - |
| `GrabSuccessTime` | `GameTime_t` | get | - |
| `DropStartTime` | `GameTime_t` | get | - |
| `ApproachRewardPayouts` | `ref int` | get | - |
| `PickupEventCount` | `ref int` | get | - |
| `SpawnGroundPos` | `ref Vector` | get | - |
| `HostageResetPosition` | `ref Vector` | get, set | - |

## ⚙️ 方法

### EntitySpottedStateUpdated

```csharp
void EntitySpottedStateUpdated()
```

### VelUpdated

```csharp
void VelUpdated()
```

### IsRescuedUpdated

```csharp
void IsRescuedUpdated()
```

### JumpedThisFrameUpdated

```csharp
void JumpedThisFrameUpdated()
```

### HostageStateUpdated

```csharp
void HostageStateUpdated()
```

### LeaderUpdated

```csharp
void LeaderUpdated()
```

### ReuseTimerUpdated

```csharp
void ReuseTimerUpdated()
```

### HandsHaveBeenCutUpdated

```csharp
void HandsHaveBeenCutUpdated()
```

### HostageGrabberUpdated

```csharp
void HostageGrabberUpdated()
```

### RescueStartTimeUpdated

```csharp
void RescueStartTimeUpdated()
```

### GrabSuccessTimeUpdated

```csharp
void GrabSuccessTimeUpdated()
```

### DropStartTimeUpdated

```csharp
void DropStartTimeUpdated()
```

