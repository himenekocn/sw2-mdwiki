# 🔌 CLogicBranchList

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CLogicalEntity`

**实现接口:** `ISchemaClass\<CLogicBranchList\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `LogicBranchNames` | `ISchemaStringFixedArray` | get | - |
| `LogicBranchList` | `ref CUtlVector\<CHandle\<CBaseEntity\>\>` | get | - |
| `LastState` | `ref CLogicBranchList__LogicBranchListenerLastState_t` | get | - |
| `OnAllTrue` | `ref CEntityIOOutput` | get | - |
| `OnAllFalse` | `ref CEntityIOOutput` | get | - |
| `OnMixed` | `ref CEntityIOOutput` | get | - |

