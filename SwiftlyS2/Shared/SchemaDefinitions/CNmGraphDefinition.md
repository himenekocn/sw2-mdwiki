# 🔌 CNmGraphDefinition

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `ISchemaClass\<CNmGraphDefinition\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `VariationID` | `ref CGlobalSymbol` | get | - |
| `Skeleton` | `ref CStrongHandle\<InfoForResourceTypeCNmSkeleton\>` | get | - |
| `UserData` | `CNmGraphVariationUserData?` | get | - |
| `PersistentNodeIndices` | `ref CUtlVector\<short\>` | get | - |
| `RootNodeIdx` | `ref short` | get | - |
| `ControlParameterIDs` | `ref CUtlVector\<CGlobalSymbol\>` | get | - |
| `VirtualParameterIDs` | `ref CUtlVector\<CGlobalSymbol\>` | get | - |
| `VirtualParameterNodeIndices` | `ref CUtlVector\<short\>` | get | - |
| `ReferencedGraphSlots` | `ref CUtlVector\<CNmGraphDefinition__ReferencedGraphSlot_t\>` | get | - |
| `ExternalGraphSlots` | `ref CUtlVector\<CNmGraphDefinition__ExternalGraphSlot_t\>` | get | - |
| `ExternalPoseSlots` | `ref CUtlVector\<CNmGraphDefinition__ExternalPoseSlot_t\>` | get | - |
| `NodePaths` | `ref CUtlVector\<CUtlString\>` | get | - |
| `Resources` | `ref CUtlVector\<SchemaUntypedField\>` | get | - |

