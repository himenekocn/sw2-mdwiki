# 🔌 WorldNode_t

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `ISchemaClass\<WorldNode_t\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SceneObjects` | `ref CUtlVector\<SceneObject_t\>` | get | - |
| `VisClusterMembership` | `ref CUtlVector\<ushort\>` | get | - |
| `AggregateSceneObjects` | `ref CUtlVector\<AggregateSceneObject_t\>` | get | - |
| `ClutterSceneObjects` | `ref CUtlVector\<ClutterSceneObject_t\>` | get | - |
| `RtProxies` | `ref CUtlVector\<AggregateRTProxySceneObject_t\>` | get | - |
| `ExtraVertexStreamOverrides` | `ref CUtlVector\<ExtraVertexStreamOverride_t\>` | get | - |
| `MaterialOverrides` | `ref CUtlVector\<MaterialOverride_t\>` | get | - |
| `ExtraVertexStreams` | `ref CUtlVector\<WorldNodeOnDiskBufferData_t\>` | get | - |
| `AggregateInstanceStreams` | `ref CUtlVector\<AggregateInstanceStreamOnDiskData_t\>` | get | - |
| `VertexAlbedoStreams` | `ref CUtlVector\<AggregateVertexAlbedoStreamOnDiskData_t\>` | get | - |
| `LayerNames` | `ref CUtlVector\<CUtlString\>` | get | - |
| `SceneObjectLayerIndices` | `ref CUtlVector\<byte\>` | get | - |
| `GrassFileName` | `string` | get, set | - |
| `NodeLightingInfo` | `BakedLightingInfo_t` | get | - |
| `HasBakedGeometryFlag` | `ref bool` | get | - |

