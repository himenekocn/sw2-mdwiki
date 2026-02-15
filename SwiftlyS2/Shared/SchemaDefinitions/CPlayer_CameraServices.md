# 🔌 CPlayer_CameraServices

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CPlayerPawnComponent`

**实现接口:** `ISchemaClass\<CPlayer_CameraServices\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CsViewPunchAngle` | `ref QAngle` | get | - |
| `CsViewPunchAngleTick` | `GameTick_t` | get | - |
| `CsViewPunchAngleTickRatio` | `ref float` | get | - |
| `PlayerFog` | `fogplayerparams_t` | get | - |
| `ColorCorrectionCtrl` | `ref CHandle\<CColorCorrection\>` | get | - |
| `ViewEntity` | `ref CHandle\<CBaseEntity\>` | get | - |
| `TonemapController` | `ref CHandle\<CTonemapController2\>` | get | - |
| `Audio` | `audioparams_t` | get | - |
| `PostProcessingVolumes` | `ref CUtlVector\<CHandle\<CPostProcessingVolume\>\>` | get | - |
| `OldPlayerZ` | `ref float` | get | - |
| `OldPlayerViewOffsetZ` | `ref float` | get, set | - |
| `TriggerSoundscapeList` | `ref CUtlVector\<CHandle\<CEnvSoundscapeTriggerable\>\>` | get | - |

## ⚙️ 方法

### CsViewPunchAngleUpdated

```csharp
void CsViewPunchAngleUpdated()
```

### CsViewPunchAngleTickUpdated

```csharp
void CsViewPunchAngleTickUpdated()
```

### CsViewPunchAngleTickRatioUpdated

```csharp
void CsViewPunchAngleTickRatioUpdated()
```

### PlayerFogUpdated

```csharp
void PlayerFogUpdated()
```

### ColorCorrectionCtrlUpdated

```csharp
void ColorCorrectionCtrlUpdated()
```

### ViewEntityUpdated

```csharp
void ViewEntityUpdated()
```

### TonemapControllerUpdated

```csharp
void TonemapControllerUpdated()
```

### AudioUpdated

```csharp
void AudioUpdated()
```

### PostProcessingVolumesUpdated

```csharp
void PostProcessingVolumesUpdated()
```

