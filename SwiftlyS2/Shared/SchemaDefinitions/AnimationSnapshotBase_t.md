# 🔌 AnimationSnapshotBase_t

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `ISchemaClass\<AnimationSnapshotBase_t\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `RealTime` | `ref float` | get | - |
| `RootToWorld` | `ref matrix3x4_t` | get | - |
| `BonesInWorldSpace` | `ref bool` | get | - |
| `BoneSetupMask` | `ref CUtlVector\<uint\>` | get | - |
| `BoneTransforms` | `ref CUtlVector\<matrix3x4_t\>` | get | - |
| `FlexControllers` | `ref CUtlVector\<float\>` | get | - |
| `SnapshotType` | `ref AnimationSnapshotType_t` | get | - |
| `HasDecodeDump` | `ref bool` | get | - |
| `DecodeDump` | `AnimationDecodeDebugDumpElement_t` | get | - |

