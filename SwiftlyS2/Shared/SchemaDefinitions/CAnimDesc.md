# 🔌 CAnimDesc

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `ISchemaClass\<CAnimDesc\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `ref CBufferString` | get | - |
| `Flags` | `CAnimDesc_Flag` | get | - |
| `Fps` | `ref float` | get | - |
| `Data` | `CAnimEncodedFrames` | get | - |
| `MovementArray` | `ref CUtlVector\<CAnimMovement\>` | get | - |
| `XInitialOffset` | `ref CTransform` | get, set | - |
| `EventArray` | `ref CUtlVector\<CAnimEventDefinition\>` | get | - |
| `ActivityArray` | `ref CUtlVector\<CAnimActivity\>` | get | - |
| `HierarchyArray` | `ref CUtlVector\<CAnimLocalHierarchy\>` | get | - |
| `Framestalltime` | `ref float` | get | - |
| `RootMin` | `ref Vector` | get | - |
| `RootMax` | `ref Vector` | get | - |
| `BoneWorldMin` | `ref CUtlVector\<Vector\>` | get | - |
| `BoneWorldMax` | `ref CUtlVector\<Vector\>` | get | - |
| `SequenceParams` | `CAnimSequenceParams` | get | - |

