# 🔌 CPlayer_MovementServices

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CPlayerPawnComponent`

**实现接口:** `ISchemaClass\<CPlayer_MovementServices\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Impulse` | `ref int` | get | - |
| `Buttons` | `CInButtonState` | get | - |
| `QueuedButtonDownMask` | `ref ulong` | get | - |
| `QueuedButtonChangeMask` | `ref ulong` | get | - |
| `ButtonDoublePressed` | `ref ulong` | get | - |
| `ButtonPressedCmdNumber` | `ISchemaFixedArray\<uint\>` | get | - |
| `LastCommandNumberProcessed` | `ref uint` | get | - |
| `ToggleButtonDownMask` | `ref ulong` | get | - |
| `Maxspeed` | `ref float` | get | - |
| `ForceSubtickMoveWhen` | `ISchemaFixedArray\<float\>` | get | - |
| `ForwardMove` | `ref float` | get | - |
| `LeftMove` | `ref float` | get | - |
| `UpMove` | `ref float` | get | - |
| `LastMovementImpulses` | `ref Vector` | get | - |
| `OldViewAngles` | `ref QAngle` | get | - |

## ⚙️ 方法

### ToggleButtonDownMaskUpdated

```csharp
void ToggleButtonDownMaskUpdated()
```

### MaxspeedUpdated

```csharp
void MaxspeedUpdated()
```

### ForceSubtickMoveWhenUpdated

```csharp
void ForceSubtickMoveWhenUpdated()
```

