# 🔌 CBasePlayerPawn

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseCombatCharacter`

**实现接口:** `ISchemaClass\<CBasePlayerPawn\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `WeaponServices` | `CPlayer_WeaponServices?` | get | - |
| `ItemServices` | `CPlayer_ItemServices?` | get | - |
| `AutoaimServices` | `CPlayer_AutoaimServices?` | get | - |
| `ObserverServices` | `CPlayer_ObserverServices?` | get | - |
| `WaterServices` | `CPlayer_WaterServices?` | get | - |
| `UseServices` | `CPlayer_UseServices?` | get | - |
| `FlashlightServices` | `CPlayer_FlashlightServices?` | get | - |
| `CameraServices` | `CPlayer_CameraServices?` | get | - |
| `MovementServices` | `CPlayer_MovementServices?` | get | - |
| `ServerViewAngleChanges` | `ref CUtlVector\<ViewAngleServerChange_t\>` | get | - |
| `V_angle` | `ref QAngle` | get | - |
| `V_anglePrevious` | `ref QAngle` | get | - |
| `HideHUD` | `ref uint` | get | - |
| `Skybox3d` | `sky3dparams_t` | get | - |
| `TimeLastHurt` | `GameTime_t` | get | - |
| `DeathTime` | `GameTime_t` | get | - |
| `NextSuicideTime` | `GameTime_t` | get | - |
| `InitHUD` | `ref bool` | get | - |
| `Expresser` | `CAI_Expresser?` | get | - |
| `Controller` | `ref CHandle\<CBasePlayerController\>` | get | - |
| `DefaultController` | `ref CHandle\<CBasePlayerController\>` | get | - |
| `HltvReplayDelay` | `ref float` | get | - |
| `HltvReplayEnd` | `ref float` | get | - |
| `HltvReplayEntity` | `ref uint` | get | - |
| `SndOpvarLatchData` | `ref CUtlVector\<sndopvarlatchdata_t\>` | get | - |

## ⚙️ 方法

### WeaponServicesUpdated

```csharp
void WeaponServicesUpdated()
```

### ItemServicesUpdated

```csharp
void ItemServicesUpdated()
```

### AutoaimServicesUpdated

```csharp
void AutoaimServicesUpdated()
```

### ObserverServicesUpdated

```csharp
void ObserverServicesUpdated()
```

### WaterServicesUpdated

```csharp
void WaterServicesUpdated()
```

### UseServicesUpdated

```csharp
void UseServicesUpdated()
```

### FlashlightServicesUpdated

```csharp
void FlashlightServicesUpdated()
```

### CameraServicesUpdated

```csharp
void CameraServicesUpdated()
```

### MovementServicesUpdated

```csharp
void MovementServicesUpdated()
```

### ServerViewAngleChangesUpdated

```csharp
void ServerViewAngleChangesUpdated()
```

### HideHUDUpdated

```csharp
void HideHUDUpdated()
```

### Skybox3dUpdated

```csharp
void Skybox3dUpdated()
```

### DeathTimeUpdated

```csharp
void DeathTimeUpdated()
```

### ControllerUpdated

```csharp
void ControllerUpdated()
```

### DefaultControllerUpdated

```csharp
void DefaultControllerUpdated()
```

