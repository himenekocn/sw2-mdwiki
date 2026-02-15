# 🔌 CAnimationGroup

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `ISchemaClass\<CAnimationGroup\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Flags` | `ref uint` | get | - |
| `Name` | `ref CBufferString` | get | - |
| `LocalHAnimArray_Handle` | `ref CUtlVector\<CStrongHandle\<InfoForResourceTypeCAnimData\>\>` | get | - |
| `IncludedGroupArray_Handle` | `ref CUtlVector\<CStrongHandle\<InfoForResourceTypeCAnimationGroup\>\>` | get | - |
| `DirectHSeqGroup_Handle` | `ref CStrongHandle\<InfoForResourceTypeCSequenceGroupData\>` | get | - |
| `DecodeKey` | `CAnimKeyData` | get | - |
| `Scripts` | `ref CUtlVector\<CBufferString\>` | get | - |
| `AdditionalExtRefs` | `ref CUtlVector\<SchemaUntypedField\>` | get | - |

