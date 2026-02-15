# 🔌 AggregateSceneObject_t

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `ISchemaClass\<AggregateSceneObject_t\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AllFlags` | `ref ObjectTypeFlags_t` | get | - |
| `AnyFlags` | `ref ObjectTypeFlags_t` | get | - |
| `Layer` | `ref short` | get | - |
| `InstanceStream` | `ref short` | get | - |
| `VertexAlbedoStream` | `ref short` | get | - |
| `AggregateMeshes` | `ref CUtlVector\<AggregateMeshInfo_t\>` | get | - |
| `LodSetups` | `ref CUtlVector\<AggregateLODSetup_t\>` | get | - |
| `VisClusterMembership` | `ref CUtlVector\<ushort\>` | get | - |
| `FragmentTransforms` | `ref CUtlVector\<matrix3x4_t\>` | get | - |
| `RenderableModel` | `ref CStrongHandle\<InfoForResourceTypeCModel\>` | get | - |

