# 🔌 CBarnLight

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseModelEntity`

**实现接口:** `ISchemaClass\<CBarnLight\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Enabled` | `ref bool` | get | - |
| `ColorMode` | `ref int` | get | - |
| `Color` | `ref Color` | get | - |
| `ColorTemperature` | `ref float` | get | - |
| `Brightness` | `ref float` | get | - |
| `BrightnessScale` | `ref float` | get | - |
| `DirectLight` | `ref int` | get | - |
| `BakedShadowIndex` | `ref int` | get | - |
| `LightPathUniqueId` | `ref int` | get | - |
| `LightMapUniqueId` | `ref int` | get | - |
| `LuminaireShape` | `ref int` | get | - |
| `LuminaireSize` | `ref float` | get | - |
| `LuminaireAnisotropy` | `ref float` | get | - |
| `LightStyleString` | `string` | get, set | - |
| `LightStyleStartTime` | `GameTime_t` | get | - |
| `QueuedLightStyleStrings` | `ref CUtlVector\<CUtlString\>` | get | - |
| `LightStyleEvents` | `ref CUtlVector\<CUtlString\>` | get | - |
| `LightStyleTargets` | `ref CUtlVector\<CHandle\<CBaseModelEntity\>\>` | get | - |
| `StyleEvent` | `ISchemaFixedArray\<CEntityIOOutput\>` | get | - |
| `LightCookie` | `ref CStrongHandle\<InfoForResourceTypeCTextureBase\>` | get | - |
| `Shape` | `ref float` | get | - |
| `SoftX` | `ref float` | get | - |
| `SoftY` | `ref float` | get | - |
| `Skirt` | `ref float` | get | - |
| `SkirtNear` | `ref float` | get | - |
| `SizeParams` | `ref Vector` | get | - |
| `Range` | `ref float` | get | - |
| `Shear` | `ref Vector` | get | - |
| `BakeSpecularToCubemaps` | `ref int` | get | - |
| `BakeSpecularToCubemapsSize` | `ref Vector` | get | - |
| `CastShadows` | `ref int` | get | - |
| `ShadowMapSize` | `ref int` | get | - |
| `ShadowPriority` | `ref int` | get | - |
| `ContactShadow` | `ref bool` | get | - |
| `ForceShadowsEnabled` | `ref bool` | get | - |
| `BounceLight` | `ref int` | get | - |
| `BounceScale` | `ref float` | get | - |
| `DynamicBounce` | `ref bool` | get | - |
| `MinRoughness` | `ref float` | get | - |
| `AlternateColor` | `ref Vector` | get | - |
| `AlternateColorBrightness` | `ref float` | get | - |
| `Fog` | `ref int` | get | - |
| `FogStrength` | `ref float` | get | - |
| `FogShadows` | `ref int` | get | - |
| `FogScale` | `ref float` | get | - |
| `FogMixedShadows` | `ref bool` | get | - |
| `FadeSizeStart` | `ref float` | get | - |
| `FadeSizeEnd` | `ref float` | get | - |
| `ShadowFadeSizeStart` | `ref float` | get | - |
| `ShadowFadeSizeEnd` | `ref float` | get | - |
| `PrecomputedFieldsValid` | `ref bool` | get | - |
| `PrecomputedBoundsMins` | `ref Vector` | get | - |
| `PrecomputedBoundsMaxs` | `ref Vector` | get | - |
| `PrecomputedOBBOrigin` | `ref Vector` | get | - |
| `PrecomputedOBBAngles` | `ref QAngle` | get | - |
| `PrecomputedOBBExtent` | `ref Vector` | get | - |
| `PrecomputedSubFrusta` | `ref int` | get | - |
| `PrecomputedOBBOrigin0` | `ref Vector` | get | - |
| `PrecomputedOBBAngles0` | `ref QAngle` | get | - |
| `PrecomputedOBBExtent0` | `ref Vector` | get | - |
| `PrecomputedOBBOrigin1` | `ref Vector` | get | - |
| `PrecomputedOBBAngles1` | `ref QAngle` | get | - |
| `PrecomputedOBBExtent1` | `ref Vector` | get | - |
| `PrecomputedOBBOrigin2` | `ref Vector` | get | - |
| `PrecomputedOBBAngles2` | `ref QAngle` | get | - |
| `PrecomputedOBBExtent2` | `ref Vector` | get | - |
| `PrecomputedOBBOrigin3` | `ref Vector` | get | - |
| `PrecomputedOBBAngles3` | `ref QAngle` | get | - |
| `PrecomputedOBBExtent3` | `ref Vector` | get | - |
| `PrecomputedOBBOrigin4` | `ref Vector` | get | - |
| `PrecomputedOBBAngles4` | `ref QAngle` | get | - |
| `PrecomputedOBBExtent4` | `ref Vector` | get | - |
| `PrecomputedOBBOrigin5` | `ref Vector` | get | - |
| `PrecomputedOBBAngles5` | `ref QAngle` | get | - |
| `PrecomputedOBBExtent5` | `ref Vector` | get | - |
| `PvsModifyEntity` | `ref bool` | get | - |
| `VisClusters` | `ref CUtlVector\<ushort\>` | get | - |

## ⚙️ 方法

### EnabledUpdated

```csharp
void EnabledUpdated()
```

### ColorModeUpdated

```csharp
void ColorModeUpdated()
```

### ColorUpdated

```csharp
void ColorUpdated()
```

### ColorTemperatureUpdated

```csharp
void ColorTemperatureUpdated()
```

### BrightnessUpdated

```csharp
void BrightnessUpdated()
```

### BrightnessScaleUpdated

```csharp
void BrightnessScaleUpdated()
```

### DirectLightUpdated

```csharp
void DirectLightUpdated()
```

### BakedShadowIndexUpdated

```csharp
void BakedShadowIndexUpdated()
```

### LightPathUniqueIdUpdated

```csharp
void LightPathUniqueIdUpdated()
```

### LightMapUniqueIdUpdated

```csharp
void LightMapUniqueIdUpdated()
```

### LuminaireShapeUpdated

```csharp
void LuminaireShapeUpdated()
```

### LuminaireSizeUpdated

```csharp
void LuminaireSizeUpdated()
```

### LuminaireAnisotropyUpdated

```csharp
void LuminaireAnisotropyUpdated()
```

### LightStyleStringUpdated

```csharp
void LightStyleStringUpdated()
```

### LightStyleStartTimeUpdated

```csharp
void LightStyleStartTimeUpdated()
```

### QueuedLightStyleStringsUpdated

```csharp
void QueuedLightStyleStringsUpdated()
```

### LightStyleEventsUpdated

```csharp
void LightStyleEventsUpdated()
```

### LightStyleTargetsUpdated

```csharp
void LightStyleTargetsUpdated()
```

### LightCookieUpdated

```csharp
void LightCookieUpdated()
```

### ShapeUpdated

```csharp
void ShapeUpdated()
```

### SoftXUpdated

```csharp
void SoftXUpdated()
```

### SoftYUpdated

```csharp
void SoftYUpdated()
```

### SkirtUpdated

```csharp
void SkirtUpdated()
```

### SkirtNearUpdated

```csharp
void SkirtNearUpdated()
```

### SizeParamsUpdated

```csharp
void SizeParamsUpdated()
```

### RangeUpdated

```csharp
void RangeUpdated()
```

### ShearUpdated

```csharp
void ShearUpdated()
```

### BakeSpecularToCubemapsUpdated

```csharp
void BakeSpecularToCubemapsUpdated()
```

### BakeSpecularToCubemapsSizeUpdated

```csharp
void BakeSpecularToCubemapsSizeUpdated()
```

### CastShadowsUpdated

```csharp
void CastShadowsUpdated()
```

### ShadowMapSizeUpdated

```csharp
void ShadowMapSizeUpdated()
```

### ShadowPriorityUpdated

```csharp
void ShadowPriorityUpdated()
```

### ContactShadowUpdated

```csharp
void ContactShadowUpdated()
```

### ForceShadowsEnabledUpdated

```csharp
void ForceShadowsEnabledUpdated()
```

### BounceLightUpdated

```csharp
void BounceLightUpdated()
```

### BounceScaleUpdated

```csharp
void BounceScaleUpdated()
```

### DynamicBounceUpdated

```csharp
void DynamicBounceUpdated()
```

### MinRoughnessUpdated

```csharp
void MinRoughnessUpdated()
```

### AlternateColorUpdated

```csharp
void AlternateColorUpdated()
```

### AlternateColorBrightnessUpdated

```csharp
void AlternateColorBrightnessUpdated()
```

### FogUpdated

```csharp
void FogUpdated()
```

### FogStrengthUpdated

```csharp
void FogStrengthUpdated()
```

### FogShadowsUpdated

```csharp
void FogShadowsUpdated()
```

### FogScaleUpdated

```csharp
void FogScaleUpdated()
```

### FogMixedShadowsUpdated

```csharp
void FogMixedShadowsUpdated()
```

### FadeSizeStartUpdated

```csharp
void FadeSizeStartUpdated()
```

### FadeSizeEndUpdated

```csharp
void FadeSizeEndUpdated()
```

### ShadowFadeSizeStartUpdated

```csharp
void ShadowFadeSizeStartUpdated()
```

### ShadowFadeSizeEndUpdated

```csharp
void ShadowFadeSizeEndUpdated()
```

### PrecomputedFieldsValidUpdated

```csharp
void PrecomputedFieldsValidUpdated()
```

### PrecomputedBoundsMinsUpdated

```csharp
void PrecomputedBoundsMinsUpdated()
```

### PrecomputedBoundsMaxsUpdated

```csharp
void PrecomputedBoundsMaxsUpdated()
```

### PrecomputedOBBOriginUpdated

```csharp
void PrecomputedOBBOriginUpdated()
```

### PrecomputedOBBAnglesUpdated

```csharp
void PrecomputedOBBAnglesUpdated()
```

### PrecomputedOBBExtentUpdated

```csharp
void PrecomputedOBBExtentUpdated()
```

### PrecomputedSubFrustaUpdated

```csharp
void PrecomputedSubFrustaUpdated()
```

### PrecomputedOBBOrigin0Updated

```csharp
void PrecomputedOBBOrigin0Updated()
```

### PrecomputedOBBAngles0Updated

```csharp
void PrecomputedOBBAngles0Updated()
```

### PrecomputedOBBExtent0Updated

```csharp
void PrecomputedOBBExtent0Updated()
```

### PrecomputedOBBOrigin1Updated

```csharp
void PrecomputedOBBOrigin1Updated()
```

### PrecomputedOBBAngles1Updated

```csharp
void PrecomputedOBBAngles1Updated()
```

### PrecomputedOBBExtent1Updated

```csharp
void PrecomputedOBBExtent1Updated()
```

### PrecomputedOBBOrigin2Updated

```csharp
void PrecomputedOBBOrigin2Updated()
```

### PrecomputedOBBAngles2Updated

```csharp
void PrecomputedOBBAngles2Updated()
```

### PrecomputedOBBExtent2Updated

```csharp
void PrecomputedOBBExtent2Updated()
```

### PrecomputedOBBOrigin3Updated

```csharp
void PrecomputedOBBOrigin3Updated()
```

### PrecomputedOBBAngles3Updated

```csharp
void PrecomputedOBBAngles3Updated()
```

### PrecomputedOBBExtent3Updated

```csharp
void PrecomputedOBBExtent3Updated()
```

### PrecomputedOBBOrigin4Updated

```csharp
void PrecomputedOBBOrigin4Updated()
```

### PrecomputedOBBAngles4Updated

```csharp
void PrecomputedOBBAngles4Updated()
```

### PrecomputedOBBExtent4Updated

```csharp
void PrecomputedOBBExtent4Updated()
```

### PrecomputedOBBOrigin5Updated

```csharp
void PrecomputedOBBOrigin5Updated()
```

### PrecomputedOBBAngles5Updated

```csharp
void PrecomputedOBBAngles5Updated()
```

### PrecomputedOBBExtent5Updated

```csharp
void PrecomputedOBBExtent5Updated()
```

### VisClustersUpdated

```csharp
void VisClustersUpdated()
```

