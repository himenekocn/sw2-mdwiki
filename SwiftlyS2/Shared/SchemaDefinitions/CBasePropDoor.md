# 🔌 CBasePropDoor

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CDynamicProp`

**实现接口:** `ISchemaClass\<CBasePropDoor\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AutoReturnDelay` | `ref float` | get | - |
| `DoorList` | `ref CUtlVector\<CHandle\<CBasePropDoor\>\>` | get | - |
| `HardwareType` | `ref int` | get | - |
| `NeedsHardware` | `ref bool` | get | - |
| `DoorState` | `ref DoorState_t` | get | - |
| `Locked` | `ref bool` | get | - |
| `NoNPCs` | `ref bool` | get | - |
| `ClosedPosition` | `ref Vector` | get | - |
| `ClosedAngles` | `ref QAngle` | get | - |
| `Blocker` | `ref CHandle\<CBaseEntity\>` | get | - |
| `FirstBlocked` | `ref bool` | get | - |
| `Ls` | `locksound_t` | get | - |
| `ForceClosed` | `ref bool` | get | - |
| `LatchWorldPosition` | `ref Vector` | get | - |
| `Activator` | `ref CHandle\<CBaseEntity\>` | get | - |
| `SoundMoving` | `string` | get, set | - |
| `SoundOpen` | `string` | get, set | - |
| `SoundClose` | `string` | get, set | - |
| `SoundLock` | `string` | get, set | - |
| `SoundUnlock` | `string` | get, set | - |
| `SoundLatch` | `string` | get, set | - |
| `SoundPound` | `string` | get, set | - |
| `SoundJiggle` | `string` | get, set | - |
| `SoundLockedAnim` | `string` | get, set | - |
| `NumCloseAttempts` | `ref int` | get | - |
| `PhysicsMaterial` | `ref CUtlStringToken` | get | - |
| `SlaveName` | `string` | get, set | - |
| `Master` | `ref CHandle\<CBasePropDoor\>` | get | - |
| `OnBlockedClosing` | `ref CEntityIOOutput` | get | - |
| `OnBlockedOpening` | `ref CEntityIOOutput` | get | - |
| `OnUnblockedClosing` | `ref CEntityIOOutput` | get | - |
| `OnUnblockedOpening` | `ref CEntityIOOutput` | get | - |
| `OnFullyClosed` | `ref CEntityIOOutput` | get | - |
| `OnFullyOpen` | `ref CEntityIOOutput` | get | - |
| `OnClose` | `ref CEntityIOOutput` | get | - |
| `OnOpen` | `ref CEntityIOOutput` | get | - |
| `OnLockedUse` | `ref CEntityIOOutput` | get | - |
| `OnAjarOpen` | `ref CEntityIOOutput` | get | - |

## ⚙️ 方法

### DoorStateUpdated

```csharp
void DoorStateUpdated()
```

### LockedUpdated

```csharp
void LockedUpdated()
```

### NoNPCsUpdated

```csharp
void NoNPCsUpdated()
```

### ClosedPositionUpdated

```csharp
void ClosedPositionUpdated()
```

### ClosedAnglesUpdated

```csharp
void ClosedAnglesUpdated()
```

### MasterUpdated

```csharp
void MasterUpdated()
```

