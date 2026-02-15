# 🔌 CPulseCell_Outflow_ScriptedSequence

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CPulseCell_BaseYieldingInflow`

**实现接口:** `ISchemaClass\<CPulseCell_Outflow_ScriptedSequence\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SyncGroup` | `string` | get, set | - |
| `ExpectedNumSequencesInSyncGroup` | `ref int` | get | - |
| `EnsureOnNavmeshOnFinish` | `ref bool` | get | - |
| `DontTeleportAtEnd` | `ref bool` | get | - |
| `DisallowInterrupts` | `ref bool` | get | - |
| `ScriptedSequenceDataMain` | `PulseScriptedSequenceData_t` | get | - |
| `AdditionalActors` | `ref CUtlVector\<PulseScriptedSequenceData_t\>` | get | - |
| `OnFinished` | `CPulse_ResumePoint` | get | - |
| `OnCanceled` | `CPulse_ResumePoint` | get | - |
| `Triggers` | `ref CUtlVector\<CPulse_OutflowConnection\>` | get | - |

