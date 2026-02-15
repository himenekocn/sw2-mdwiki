# 🔌 CBaseDoor

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseToggle`

**实现接口:** `ISchemaClass\<CBaseDoor\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MoveEntitySpace` | `ref QAngle` | get | - |
| `MoveDirParentSpace` | `ref Vector` | get | - |
| `Ls` | `locksound_t` | get | - |
| `ForceClosed` | `ref bool` | get | - |
| `DoorGroup` | `ref bool` | get | - |
| `Locked` | `ref bool` | get | - |
| `IgnoreDebris` | `ref bool` | get | - |
| `NoNPCs` | `ref bool` | get | - |
| `SpawnPosition` | `ref FuncDoorSpawnPos_t` | get | - |
| `BlockDamage` | `ref float` | get | - |
| `NoiseMoving` | `string` | get, set | - |
| `NoiseArrived` | `string` | get, set | - |
| `NoiseMovingClosed` | `string` | get, set | - |
| `NoiseArrivedClosed` | `string` | get, set | - |
| `ChainTarget` | `string` | get, set | - |
| `OnBlockedClosing` | `ref CEntityIOOutput` | get | - |
| `OnBlockedOpening` | `ref CEntityIOOutput` | get | - |
| `OnUnblockedClosing` | `ref CEntityIOOutput` | get | - |
| `OnUnblockedOpening` | `ref CEntityIOOutput` | get | - |
| `OnFullyClosed` | `ref CEntityIOOutput` | get | - |
| `OnFullyOpen` | `ref CEntityIOOutput` | get | - |
| `OnClose` | `ref CEntityIOOutput` | get | - |
| `OnOpen` | `ref CEntityIOOutput` | get | - |
| `OnLockedUse` | `ref CEntityIOOutput` | get | - |
| `LoopMoveSound` | `ref bool` | get | - |
| `CreateNavObstacle` | `ref bool` | get | - |
| `IsChaining` | `ref bool` | get | - |
| `IsUsable` | `ref bool` | get | - |

## ⚙️ 方法

### IsUsableUpdated

```csharp
void IsUsableUpdated()
```

