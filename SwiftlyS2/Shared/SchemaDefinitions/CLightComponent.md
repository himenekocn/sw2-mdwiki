# 🔌 CLightComponent

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CEntityComponent`

**实现接口:** `ISchemaClass\<CLightComponent\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Color` | `ref Color` | get | - |
| `SecondaryColor` | `ref Color` | get | - |
| `Brightness` | `ref float` | get | - |
| `BrightnessScale` | `ref float` | get | - |
| `BrightnessMult` | `ref float` | get | - |
| `Range` | `ref float` | get | - |
| `Falloff` | `ref float` | get | - |
| `Attenuation0` | `ref float` | get | - |
| `Attenuation1` | `ref float` | get | - |
| `Attenuation2` | `ref float` | get | - |
| `Theta` | `ref float` | get | - |
| `Phi` | `ref float` | get | - |
| `LightCookie` | `ref CStrongHandle\<InfoForResourceTypeCTextureBase\>` | get | - |
| `Cascades` | `ref int` | get | - |
| `CastShadows` | `ref int` | get | - |
| `ShadowWidth` | `ref int` | get | - |
| `ShadowHeight` | `ref int` | get | - |
| `RenderDiffuse` | `ref bool` | get | - |
| `RenderSpecular` | `ref int` | get | - |
| `RenderTransmissive` | `ref bool` | get | - |
| `OrthoLightWidth` | `ref float` | get | - |
| `OrthoLightHeight` | `ref float` | get | - |
| `Style` | `ref int` | get | - |
| `Pattern` | `string` | get, set | - |
| `CascadeRenderStaticObjects` | `ref int` | get | - |
| `ShadowCascadeCrossFade` | `ref float` | get | - |
| `ShadowCascadeDistanceFade` | `ref float` | get | - |
| `ShadowCascadeDistance0` | `ref float` | get | - |
| `ShadowCascadeDistance1` | `ref float` | get | - |
| `ShadowCascadeDistance2` | `ref float` | get | - |
| `ShadowCascadeDistance3` | `ref float` | get | - |
| `ShadowCascadeResolution0` | `ref int` | get | - |
| `ShadowCascadeResolution1` | `ref int` | get | - |
| `ShadowCascadeResolution2` | `ref int` | get | - |
| `ShadowCascadeResolution3` | `ref int` | get | - |
| `UsesBakedShadowing` | `ref bool` | get | - |
| `ShadowPriority` | `ref int` | get | - |
| `BakedShadowIndex` | `ref int` | get | - |
| `LightPathUniqueId` | `ref int` | get | - |
| `LightMapUniqueId` | `ref int` | get | - |
| `RenderToCubemaps` | `ref bool` | get | - |
| `AllowSSTGeneration` | `ref bool` | get | - |
| `DirectLight` | `ref int` | get | - |
| `IndirectLight` | `ref int` | get | - |
| `DynamicBounce` | `ref bool` | get | - |
| `FadeMinDist` | `ref float` | get | - |
| `FadeMaxDist` | `ref float` | get | - |
| `ShadowFadeMinDist` | `ref float` | get | - |
| `ShadowFadeMaxDist` | `ref float` | get | - |
| `Enabled` | `ref bool` | get | - |
| `Flicker` | `ref bool` | get | - |
| `PrecomputedFieldsValid` | `ref bool` | get | - |
| `PrecomputedBoundsMins` | `ref Vector` | get | - |
| `PrecomputedBoundsMaxs` | `ref Vector` | get | - |
| `PrecomputedOBBOrigin` | `ref Vector` | get | - |
| `PrecomputedOBBAngles` | `ref QAngle` | get | - |
| `PrecomputedOBBExtent` | `ref Vector` | get | - |
| `PrecomputedMaxRange` | `ref float` | get | - |
| `FogLightingMode` | `ref int` | get | - |
| `FogContributionStength` | `ref float` | get | - |
| `NearClipPlane` | `ref float` | get | - |
| `SkyColor` | `ref Color` | get | - |
| `SkyIntensity` | `ref float` | get | - |
| `SkyAmbientBounce` | `ref Color` | get | - |
| `UseSecondaryColor` | `ref bool` | get | - |
| `MixedShadows` | `ref bool` | get | - |
| `LightStyleStartTime` | `GameTime_t` | get | - |
| `CapsuleLength` | `ref float` | get | - |
| `MinRoughness` | `ref float` | get | - |
| `PvsModifyEntity` | `ref bool` | get | - |

## ⚙️ 方法

### ColorUpdated

```csharp
void ColorUpdated()
```

### SecondaryColorUpdated

```csharp
void SecondaryColorUpdated()
```

### BrightnessUpdated

```csharp
void BrightnessUpdated()
```

### BrightnessScaleUpdated

```csharp
void BrightnessScaleUpdated()
```

### BrightnessMultUpdated

```csharp
void BrightnessMultUpdated()
```

### RangeUpdated

```csharp
void RangeUpdated()
```

### FalloffUpdated

```csharp
void FalloffUpdated()
```

### Attenuation0Updated

```csharp
void Attenuation0Updated()
```

### Attenuation1Updated

```csharp
void Attenuation1Updated()
```

### Attenuation2Updated

```csharp
void Attenuation2Updated()
```

### ThetaUpdated

```csharp
void ThetaUpdated()
```

### PhiUpdated

```csharp
void PhiUpdated()
```

### LightCookieUpdated

```csharp
void LightCookieUpdated()
```

### CascadesUpdated

```csharp
void CascadesUpdated()
```

### CastShadowsUpdated

```csharp
void CastShadowsUpdated()
```

### ShadowWidthUpdated

```csharp
void ShadowWidthUpdated()
```

### ShadowHeightUpdated

```csharp
void ShadowHeightUpdated()
```

### RenderDiffuseUpdated

```csharp
void RenderDiffuseUpdated()
```

### RenderSpecularUpdated

```csharp
void RenderSpecularUpdated()
```

### RenderTransmissiveUpdated

```csharp
void RenderTransmissiveUpdated()
```

### OrthoLightWidthUpdated

```csharp
void OrthoLightWidthUpdated()
```

### OrthoLightHeightUpdated

```csharp
void OrthoLightHeightUpdated()
```

### StyleUpdated

```csharp
void StyleUpdated()
```

### PatternUpdated

```csharp
void PatternUpdated()
```

### CascadeRenderStaticObjectsUpdated

```csharp
void CascadeRenderStaticObjectsUpdated()
```

### ShadowCascadeCrossFadeUpdated

```csharp
void ShadowCascadeCrossFadeUpdated()
```

### ShadowCascadeDistanceFadeUpdated

```csharp
void ShadowCascadeDistanceFadeUpdated()
```

### ShadowCascadeDistance0Updated

```csharp
void ShadowCascadeDistance0Updated()
```

### ShadowCascadeDistance1Updated

```csharp
void ShadowCascadeDistance1Updated()
```

### ShadowCascadeDistance2Updated

```csharp
void ShadowCascadeDistance2Updated()
```

### ShadowCascadeDistance3Updated

```csharp
void ShadowCascadeDistance3Updated()
```

### ShadowCascadeResolution0Updated

```csharp
void ShadowCascadeResolution0Updated()
```

### ShadowCascadeResolution1Updated

```csharp
void ShadowCascadeResolution1Updated()
```

### ShadowCascadeResolution2Updated

```csharp
void ShadowCascadeResolution2Updated()
```

### ShadowCascadeResolution3Updated

```csharp
void ShadowCascadeResolution3Updated()
```

### UsesBakedShadowingUpdated

```csharp
void UsesBakedShadowingUpdated()
```

### ShadowPriorityUpdated

```csharp
void ShadowPriorityUpdated()
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

### RenderToCubemapsUpdated

```csharp
void RenderToCubemapsUpdated()
```

### AllowSSTGenerationUpdated

```csharp
void AllowSSTGenerationUpdated()
```

### DirectLightUpdated

```csharp
void DirectLightUpdated()
```

### IndirectLightUpdated

```csharp
void IndirectLightUpdated()
```

### DynamicBounceUpdated

```csharp
void DynamicBounceUpdated()
```

### FadeMinDistUpdated

```csharp
void FadeMinDistUpdated()
```

### FadeMaxDistUpdated

```csharp
void FadeMaxDistUpdated()
```

### ShadowFadeMinDistUpdated

```csharp
void ShadowFadeMinDistUpdated()
```

### ShadowFadeMaxDistUpdated

```csharp
void ShadowFadeMaxDistUpdated()
```

### EnabledUpdated

```csharp
void EnabledUpdated()
```

### FlickerUpdated

```csharp
void FlickerUpdated()
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

### PrecomputedMaxRangeUpdated

```csharp
void PrecomputedMaxRangeUpdated()
```

### FogLightingModeUpdated

```csharp
void FogLightingModeUpdated()
```

### FogContributionStengthUpdated

```csharp
void FogContributionStengthUpdated()
```

### NearClipPlaneUpdated

```csharp
void NearClipPlaneUpdated()
```

### SkyColorUpdated

```csharp
void SkyColorUpdated()
```

### SkyIntensityUpdated

```csharp
void SkyIntensityUpdated()
```

### SkyAmbientBounceUpdated

```csharp
void SkyAmbientBounceUpdated()
```

### UseSecondaryColorUpdated

```csharp
void UseSecondaryColorUpdated()
```

### MixedShadowsUpdated

```csharp
void MixedShadowsUpdated()
```

### LightStyleStartTimeUpdated

```csharp
void LightStyleStartTimeUpdated()
```

### CapsuleLengthUpdated

```csharp
void CapsuleLengthUpdated()
```

### MinRoughnessUpdated

```csharp
void MinRoughnessUpdated()
```

