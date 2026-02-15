# 🔌 CPulseGraphDef

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `ISchemaClass\<CPulseGraphDef\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `DomainIdentifier` | `SchemaUntypedField` | get | - |
| `DomainSubType` | `SchemaUntypedField` | get | - |
| `ParentMapName` | `SchemaUntypedField` | get | - |
| `ParentXmlName` | `SchemaUntypedField` | get | - |
| `Chunks` | `ref CUtlVector\<PointerTo\<CPulse_Chunk\>\>` | get | - |
| `Cells` | `ref CUtlVector\<PointerTo\<CPulseCell_Base\>\>` | get | - |
| `Vars` | `ref CUtlVector\<CPulse_Variable\>` | get | - |
| `PublicOutputs` | `ref CUtlVector\<CPulse_PublicOutput\>` | get | - |
| `InvokeBindings` | `ref CUtlVector\<PointerTo\<CPulse_InvokeBinding\>\>` | get | - |
| `CallInfos` | `ref CUtlVector\<PointerTo\<CPulse_CallInfo\>\>` | get | - |
| `Constants` | `ref CUtlVector\<CPulse_Constant\>` | get | - |
| `DomainValues` | `ref CUtlVector\<CPulse_DomainValue\>` | get | - |
| `BlackboardReferences` | `ref CUtlVector\<CPulse_BlackboardReference\>` | get | - |
| `OutputConnections` | `ref CUtlVector\<PointerTo\<CPulse_OutputConnection\>\>` | get | - |

