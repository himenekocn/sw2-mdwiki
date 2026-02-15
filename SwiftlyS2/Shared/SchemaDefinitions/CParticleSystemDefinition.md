# 🔌 CParticleSystemDefinition

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `IParticleSystemDefinition`

**实现接口:** `ISchemaClass\<CParticleSystemDefinition\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `BehaviorVersion` | `ref int` | get | - |
| `PreEmissionOperators` | `ref CUtlVector\<PointerTo\<CParticleFunctionPreEmission\>\>` | get | - |
| `Emitters` | `ref CUtlVector\<PointerTo\<CParticleFunctionEmitter\>\>` | get | - |
| `Initializers` | `ref CUtlVector\<PointerTo\<CParticleFunctionInitializer\>\>` | get | - |
| `Operators` | `ref CUtlVector\<PointerTo\<CParticleFunctionOperator\>\>` | get | - |
| `ForceGenerators` | `ref CUtlVector\<PointerTo\<CParticleFunctionForce\>\>` | get | - |
| `Constraints` | `ref CUtlVector\<PointerTo\<CParticleFunctionConstraint\>\>` | get | - |
| `Renderers` | `ref CUtlVector\<PointerTo\<CParticleFunctionRenderer\>\>` | get | - |
| `Children` | `ref CUtlVector\<ParticleChildrenInfo_t\>` | get | - |
| `FirstMultipleOverride_BackwardCompat` | `ref int` | get | - |
| `InitialParticles` | `ref int` | get | - |
| `MaxParticles` | `ref int` | get | - |
| `GroupID` | `ref int` | get | - |
| `BoundingBoxMin` | `ref Vector` | get | - |
| `BoundingBoxMax` | `ref Vector` | get | - |
| `DepthSortBias` | `ref float` | get | - |
| `SortOverridePositionCP` | `ref int` | get | - |
| `InfiniteBounds` | `ref bool` | get | - |
| `EnableNamedValues` | `ref bool` | get | - |
| `NamedValueDomain` | `string` | get, set | - |
| `NamedValueLocals` | `ref CUtlVector\<PointerTo\<ParticleNamedValueSource_t\>\>` | get | - |
| `ConstantColor` | `ref Color` | get | - |
| `ConstantNormal` | `ref Vector` | get | - |
| `ConstantRadius` | `ref float` | get | - |
| `ConstantRotation` | `ref float` | get | - |
| `ConstantRotationSpeed` | `ref float` | get | - |
| `ConstantLifespan` | `ref float` | get | - |
| `ConstantSequenceNumber` | `ref int` | get | - |
| `ConstantSequenceNumber1` | `ref int` | get | - |
| `SnapshotControlPoint` | `ref int` | get | - |
| `Snapshot` | `ref CStrongHandle\<InfoForResourceTypeIParticleSnapshot\>` | get | - |
| `CullReplacementName` | `ref CStrongHandle\<InfoForResourceTypeIParticleSystemDefinition\>` | get | - |
| `CullRadius` | `ref float` | get | - |
| `CullFillCost` | `ref float` | get | - |
| `CullControlPoint` | `ref int` | get | - |
| `Fallback` | `ref CStrongHandle\<InfoForResourceTypeIParticleSystemDefinition\>` | get | - |
| `FallbackMaxCount` | `ref int` | get | - |
| `LowViolenceDef` | `ref CStrongHandle\<InfoForResourceTypeIParticleSystemDefinition\>` | get | - |
| `ReferenceReplacement` | `ref CStrongHandle\<InfoForResourceTypeIParticleSystemDefinition\>` | get | - |
| `PreSimulationTime` | `ref float` | get | - |
| `StopSimulationAfterTime` | `ref float` | get | - |
| `MaximumTimeStep` | `ref float` | get | - |
| `MaximumSimTime` | `ref float` | get | - |
| `MinimumSimTime` | `ref float` | get | - |
| `MinimumTimeStep` | `ref float` | get | - |
| `MinimumFrames` | `ref int` | get | - |
| `MinCPULevel` | `ref int` | get | - |
| `MinGPULevel` | `ref int` | get | - |
| `NoDrawTimeToGoToSleep` | `ref float` | get | - |
| `MaxDrawDistance` | `ref float` | get | - |
| `StartFadeDistance` | `ref float` | get | - |
| `MaxCreationDistance` | `ref float` | get | - |
| `AggregationMinAvailableParticles` | `ref int` | get | - |
| `AggregateRadius` | `ref float` | get | - |
| `ShouldBatch` | `ref bool` | get | - |
| `ShouldHitboxesFallbackToRenderBounds` | `ref bool` | get | - |
| `ShouldHitboxesFallbackToSnapshot` | `ref bool` | get | - |
| `ShouldHitboxesFallbackToCollisionHulls` | `ref bool` | get | - |
| `ViewModelEffect` | `ref InheritableBoolType_t` | get | - |
| `ScreenSpaceEffect` | `ref bool` | get | - |
| `TargetLayerID` | `string` | get, set | - |
| `SkipRenderControlPoint` | `ref int` | get | - |
| `AllowRenderControlPoint` | `ref int` | get | - |
| `ShouldSort` | `ref bool` | get | - |
| `ControlPointConfigurations` | `ref CUtlVector\<ParticleControlPointConfiguration_t\>` | get | - |

