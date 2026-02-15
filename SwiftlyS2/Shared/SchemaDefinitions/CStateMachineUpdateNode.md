# 🔌 CStateMachineUpdateNode

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CAnimUpdateNodeBase`

**实现接口:** `ISchemaClass\<CStateMachineUpdateNode\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `StateMachine` | `CAnimStateMachineUpdater` | get | - |
| `StateData` | `ref CUtlVector\<CStateNodeStateData\>` | get | - |
| `TransitionData` | `ref CUtlVector\<CStateNodeTransitionData\>` | get | - |
| `BlockWaningTags` | `ref bool` | get | - |
| `LockStateWhenWaning` | `ref bool` | get | - |
| `ResetWhenActivated` | `ref bool` | get, set | - |

