# 🔌 PermModelData_t

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `ISchemaClass\<PermModelData_t\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | get, set | - |
| `ModelInfo` | `PermModelInfo_t` | get | - |
| `ExtParts` | `ref CUtlVector\<PermModelExtPart_t\>` | get | - |
| `RefMeshes` | `ref CUtlVector\<CStrongHandle\<InfoForResourceTypeCRenderMesh\>\>` | get | - |
| `RefMeshGroupMasks` | `ref CUtlVector\<ulong\>` | get | - |
| `RefPhysGroupMasks` | `ref CUtlVector\<ulong\>` | get | - |
| `RefLODGroupMasks` | `ref CUtlVector\<byte\>` | get | - |
| `LodGroupSwitchDistances` | `ref CUtlVector\<float\>` | get | - |
| `RefPhysicsData` | `ref CUtlVector\<CStrongHandle\<InfoForResourceTypeCPhysAggregateData\>\>` | get | - |
| `RefPhysicsHitboxData` | `ref CUtlVector\<CStrongHandle\<InfoForResourceTypeCPhysAggregateData\>\>` | get | - |
| `RefAnimGroups` | `ref CUtlVector\<CStrongHandle\<InfoForResourceTypeCAnimationGroup\>\>` | get | - |
| `RefSequenceGroups` | `ref CUtlVector\<CStrongHandle\<InfoForResourceTypeCSequenceGroupData\>\>` | get | - |
| `MeshGroups` | `ref CUtlVector\<CUtlString\>` | get | - |
| `MaterialGroups` | `ref CUtlVector\<MaterialGroup_t\>` | get | - |
| `DefaultMeshGroupMask` | `ref ulong` | get | - |
| `ModelSkeleton` | `ModelSkeletonData_t` | get | - |
| `RemappingTable` | `ref CUtlVector\<short\>` | get | - |
| `RemappingTableStarts` | `ref CUtlVector\<ushort\>` | get | - |
| `BoneFlexDrivers` | `ref CUtlVector\<ModelBoneFlexDriver_t\>` | get | - |
| `ModelConfigList` | `CModelConfigList?` | get | - |
| `BodyGroupsHiddenInTools` | `ref CUtlVector\<CUtlString\>` | get | - |
| `RefAnimIncludeModels` | `ref CUtlVector\<CStrongHandle\<InfoForResourceTypeCModel\>\>` | get | - |
| `AnimatedMaterialAttributes` | `ref CUtlVector\<PermModelDataAnimatedMaterialAttribute_t\>` | get | - |
| `AnimGraph2Refs` | `ref CUtlVector\<ModelAnimGraph2Ref_t\>` | get | - |
| `NmSkeletonRefs` | `ref CUtlVector\<CStrongHandle\<InfoForResourceTypeCNmSkeleton\>\>` | get | - |

