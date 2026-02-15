# 🔌 CStateUpdateData

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `ISchemaClass\<CStateUpdateData\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | get, set | - |
| `Script` | `AnimScriptHandle` | get | - |
| `TransitionIndices` | `ref CUtlVector\<int\>` | get | - |
| `Actions` | `ref CUtlVector\<CStateActionUpdater\>` | get | - |
| `StateID` | `AnimStateID` | get | - |
| `IsStartState` | `SchemaUntypedField` | get | - |
| `IsEndState` | `SchemaUntypedField` | get | - |
| `IsPassthrough` | `SchemaUntypedField` | get | - |
| `IsPassthroughRootMotion` | `SchemaUntypedField` | get | - |
| `PreEvaluatePassthroughTransitionPath` | `SchemaUntypedField` | get | - |

