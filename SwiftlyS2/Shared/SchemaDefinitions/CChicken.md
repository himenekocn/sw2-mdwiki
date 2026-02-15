# 🔌 CChicken

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CDynamicProp`

**实现接口:** `ISchemaClass\<CChicken\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AttributeManager` | `CAttributeContainer` | get | - |
| `UpdateTimer` | `CountdownTimer` | get | - |
| `StuckAnchor` | `ref Vector` | get | - |
| `StuckTimer` | `CountdownTimer` | get | - |
| `CollisionStuckTimer` | `CountdownTimer` | get | - |
| `IsOnGround` | `ref bool` | get | - |
| `FallVelocity` | `ref Vector` | get | - |
| `DesiredActivity` | `ref ChickenActivity` | get | - |
| `CurrentActivity` | `ref ChickenActivity` | get | - |
| `ActivityTimer` | `CountdownTimer` | get | - |
| `TurnRate` | `ref float` | get | - |
| `FleeFrom` | `ref CHandle\<CBaseEntity\>` | get | - |
| `MoveRateThrottleTimer` | `CountdownTimer` | get | - |
| `StartleTimer` | `CountdownTimer` | get | - |
| `VocalizeTimer` | `CountdownTimer` | get | - |
| `WhenZombified` | `GameTime_t` | get | - |
| `JumpedThisFrame` | `ref bool` | get | - |
| `Leader` | `ref CHandle\<CCSPlayerPawn\>` | get | - |
| `ReuseTimer` | `CountdownTimer` | get | - |
| `HasBeenUsed` | `ref bool` | get | - |
| `JumpTimer` | `CountdownTimer` | get | - |
| `LastJumpTime` | `ref float` | get | - |
| `InJump` | `ref bool` | get | - |
| `RepathTimer` | `CountdownTimer` | get | - |
| `PathGoal` | `ref Vector` | get | - |
| `ActiveFollowStartTime` | `GameTime_t` | get | - |
| `FollowMinuteTimer` | `CountdownTimer` | get | - |
| `BlockDirectionTimer` | `CountdownTimer` | get | - |

## ⚙️ 方法

### AttributeManagerUpdated

```csharp
void AttributeManagerUpdated()
```

### JumpedThisFrameUpdated

```csharp
void JumpedThisFrameUpdated()
```

### LeaderUpdated

```csharp
void LeaderUpdated()
```

