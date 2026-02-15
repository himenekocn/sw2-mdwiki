# 🔌 CSeqCmdSeqDesc

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `ISchemaClass\<CSeqCmdSeqDesc\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `ref CBufferString` | get | - |
| `Flags` | `CSeqSeqDescFlag` | get | - |
| `Transition` | `CSeqTransition` | get | - |
| `FrameRangeSequence` | `ref short` | get | - |
| `FrameCount` | `ref short` | get | - |
| `FPS` | `ref float` | get | - |
| `SubCycles` | `ref short` | get | - |
| `NumLocalResults` | `ref short` | get | - |
| `CmdLayerArray` | `ref CUtlVector\<CSeqCmdLayer\>` | get | - |
| `EventArray` | `ref CUtlVector\<CAnimEventDefinition\>` | get | - |
| `ActivityArray` | `ref CUtlVector\<CAnimActivity\>` | get | - |
| `PoseSettingArray` | `ref CUtlVector\<CSeqPoseSetting\>` | get | - |

