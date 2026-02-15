# 🔌 C_OP_RenderStandardLight

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CParticleFunctionRenderer`

**实现接口:** `ISchemaClass\<C_OP_RenderStandardLight\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `LightType` | `ref ParticleLightTypeChoiceList_t` | get | - |
| `ColorScale` | `CParticleCollectionVecInput` | get | - |
| `ColorBlendType` | `ref ParticleColorBlendType_t` | get | - |
| `Intensity` | `CPerParticleFloatInput` | get | - |
| `CastShadows` | `ref bool` | get | - |
| `Theta` | `CParticleCollectionFloatInput` | get | - |
| `Phi` | `CParticleCollectionFloatInput` | get | - |
| `RadiusMultiplier` | `CParticleCollectionFloatInput` | get | - |
| `AttenuationStyle` | `ref StandardLightingAttenuationStyle_t` | get | - |
| `FalloffLinearity` | `CParticleCollectionFloatInput` | get | - |
| `FiftyPercentFalloff` | `CParticleCollectionFloatInput` | get | - |
| `ZeroPercentFalloff` | `CParticleCollectionFloatInput` | get | - |
| `RenderDiffuse` | `ref bool` | get | - |
| `RenderSpecular` | `ref bool` | get | - |
| `LightCookie` | `string` | get, set | - |
| `Priority` | `ref int` | get | - |
| `FogLightingMode` | `ref ParticleLightFogLightingMode_t` | get | - |
| `FogContribution` | `CParticleCollectionRendererFloatInput` | get | - |
| `CapsuleLightBehavior` | `ref ParticleLightBehaviorChoiceList_t` | get | - |
| `CapsuleLength` | `ref float` | get | - |
| `ReverseOrder` | `ref bool` | get | - |
| `ClosedLoop` | `ref bool` | get | - |
| `PrevPntSource` | `ParticleAttributeIndex_t` | get | - |
| `MaxLength` | `ref float` | get | - |
| `MinLength` | `ref float` | get | - |
| `IgnoreDT` | `ref bool` | get | - |
| `ConstrainRadiusToLengthRatio` | `ref float` | get | - |
| `LengthScale` | `ref float` | get | - |
| `LengthFadeInTime` | `ref float` | get | - |

