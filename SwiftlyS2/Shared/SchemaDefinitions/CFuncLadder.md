# 🔌 CFuncLadder

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseModelEntity`

**实现接口:** `ISchemaClass\<CFuncLadder\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `LadderDir` | `ref Vector` | get | - |
| `Dismounts` | `ref CUtlVector\<CHandle\<CInfoLadderDismount\>\>` | get | - |
| `LocalTop` | `ref Vector` | get | - |
| `PlayerMountPositionTop` | `ref Vector` | get | - |
| `PlayerMountPositionBottom` | `ref Vector` | get | - |
| `AutoRideSpeed` | `ref float` | get | - |
| `Disabled` | `ref bool` | get | - |
| `FakeLadder` | `ref bool` | get | - |
| `HasSlack` | `ref bool` | get | - |
| `SurfacePropName` | `string` | get, set | - |
| `OnPlayerGotOnLadder` | `ref CEntityIOOutput` | get | - |
| `OnPlayerGotOffLadder` | `ref CEntityIOOutput` | get | - |

## ⚙️ 方法

### LadderDirUpdated

```csharp
void LadderDirUpdated()
```

### PlayerMountPositionTopUpdated

```csharp
void PlayerMountPositionTopUpdated()
```

### PlayerMountPositionBottomUpdated

```csharp
void PlayerMountPositionBottomUpdated()
```

### AutoRideSpeedUpdated

```csharp
void AutoRideSpeedUpdated()
```

### FakeLadderUpdated

```csharp
void FakeLadderUpdated()
```

