# 🔌 CNmClip

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `ISchemaClass\<CNmClip\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Skeleton` | `ref CStrongHandle\<InfoForResourceTypeCNmSkeleton\>` | get | - |
| `NumFrames` | `ref uint` | get | - |
| `Duration` | `ref float` | get | - |
| `CompressedPoseData` | `ref CUtlBinaryBlock` | get | - |
| `TrackCompressionSettings` | `ref CUtlVector\<NmCompressionSettings_t\>` | get | - |
| `CompressedPoseOffsets` | `ref CUtlVector\<uint\>` | get, set | - |
| `FloatCurveIDs` | `ref CUtlVector\<CGlobalSymbol\>` | get | - |
| `FloatCurveDefs` | `ref CUtlVector\<NmFloatCurveCompressionSettings_t\>` | get | - |
| `CompressedFloatCurveData` | `ref CUtlVector\<ushort\>` | get | - |
| `CompressedFloatCurveOffsets` | `ref CUtlVector\<uint\>` | get, set | - |
| `SecondaryAnimations` | `SchemaUntypedField` | get | - |
| `SyncTrack` | `CNmSyncTrack` | get | - |
| `RootMotion` | `CNmRootMotionData` | get | - |
| `IsAdditive` | `ref bool` | get | - |
| `ModelSpaceSamplingChain` | `ref CUtlVector\<CNmClip__ModelSpaceSamplingChainLink_t\>` | get | - |
| `ModelSpaceBoneSamplingIndices` | `ref CUtlVector\<int\>` | get | - |

