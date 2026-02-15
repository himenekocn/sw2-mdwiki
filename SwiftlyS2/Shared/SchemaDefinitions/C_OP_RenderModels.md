# 🔌 C_OP_RenderModels

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CParticleFunctionRenderer`

**实现接口:** `ISchemaClass\<C_OP_RenderModels\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `OnlyRenderInEffectsBloomPass` | `ref bool` | get | - |
| `OnlyRenderInEffectsWaterPass` | `ref bool` | get | - |
| `UseMixedResolutionRendering` | `ref bool` | get | - |
| `OnlyRenderInEffecsGameOverlay` | `ref bool` | get | - |
| `ModelList` | `ref CUtlVector\<ModelReference_t\>` | get | - |
| `BodyGroupField` | `ParticleAttributeIndex_t` | get | - |
| `SubModelField` | `ParticleAttributeIndex_t` | get | - |
| `IgnoreNormal` | `ref bool` | get | - |
| `OrientZ` | `ref bool` | get | - |
| `CenterOffset` | `ref bool` | get, set | - |
| `LocalOffset` | `CPerParticleVecInput` | get, set | - |
| `LocalRotation` | `CPerParticleVecInput` | get | - |
| `IgnoreRadius` | `ref bool` | get | - |
| `ModelScaleCP` | `ref int` | get | - |
| `ComponentScale` | `CPerParticleVecInput` | get | - |
| `LocalScale` | `ref bool` | get | - |
| `SizeCullBloat` | `ref int` | get | - |
| `Animated` | `ref bool` | get | - |
| `AnimationRate` | `CPerParticleFloatInput` | get | - |
| `ScaleAnimationRate` | `ref bool` | get | - |
| `ForceLoopingAnimation` | `ref bool` | get | - |
| `ResetAnimOnStop` | `ref bool` | get, set | - |
| `ManualAnimFrame` | `ref bool` | get | - |
| `AnimationScaleField` | `ParticleAttributeIndex_t` | get | - |
| `AnimationField` | `ParticleAttributeIndex_t` | get | - |
| `ManualFrameField` | `ParticleAttributeIndex_t` | get | - |
| `ActivityName` | `string` | get, set | - |
| `SequenceName` | `string` | get, set | - |
| `EnableClothSimulation` | `ref bool` | get | - |
| `ClothEffectName` | `string` | get, set | - |
| `OverrideMaterial` | `ref CStrongHandle\<InfoForResourceTypeIMaterial2\>` | get | - |
| `OverrideTranslucentMaterials` | `ref bool` | get | - |
| `Skin` | `CPerParticleFloatInput` | get | - |
| `MaterialVars` | `ref CUtlVector\<MaterialVariable_t\>` | get | - |
| `RenderFilter` | `CPerParticleFloatInput` | get | - |
| `ManualModelSelection` | `CPerParticleFloatInput` | get | - |
| `ModelInput` | `CParticleModelInput` | get | - |
| `LOD` | `ref int` | get | - |
| `EconSlotName` | `string` | get, set | - |
| `OriginalModel` | `ref bool` | get | - |
| `SuppressTint` | `ref bool` | get | - |
| `SubModelFieldType` | `ref RenderModelSubModelFieldType_t` | get | - |
| `DisableShadows` | `ref bool` | get | - |
| `DisableDepthPrepass` | `ref bool` | get | - |
| `AcceptsDecals` | `ref bool` | get | - |
| `ForceDrawInterlevedWithSiblings` | `ref bool` | get | - |
| `DoNotDrawInParticlePass` | `ref bool` | get | - |
| `AllowApproximateTransforms` | `ref bool` | get | - |
| `RenderAttribute` | `string` | get, set | - |
| `RadiusScale` | `CParticleCollectionFloatInput` | get | - |
| `AlphaScale` | `CParticleCollectionFloatInput` | get | - |
| `RollScale` | `CParticleCollectionFloatInput` | get | - |
| `Alpha2Field` | `ParticleAttributeIndex_t` | get | - |
| `ColorScale` | `CParticleCollectionVecInput` | get | - |
| `ColorBlendType` | `ref ParticleColorBlendType_t` | get | - |

