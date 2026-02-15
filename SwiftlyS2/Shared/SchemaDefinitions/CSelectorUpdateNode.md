# 🔌 CSelectorUpdateNode

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CAnimUpdateNodeBase`

**实现接口:** `ISchemaClass\<CSelectorUpdateNode\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Children` | `ref CUtlVector\<CAnimUpdateNodeRef\>` | get | - |
| `Tags` | `ref CUtlVector\<byte\>` | get | - |
| `BlendCurve` | `CBlendCurve` | get | - |
| `BlendTime` | `SchemaUntypedField` | get | - |
| `Parameter` | `CAnimParamHandle` | get | - |
| `TagIndex` | `ref int` | get | - |
| `TagBehavior` | `ref SelectorTagBehavior_t` | get | - |
| `ResetOnChange` | `ref bool` | get, set | - |
| `LockWhenWaning` | `ref bool` | get | - |
| `SyncCyclesOnChange` | `ref bool` | get | - |

