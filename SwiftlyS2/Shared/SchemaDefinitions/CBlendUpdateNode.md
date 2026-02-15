# 🔌 CBlendUpdateNode

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CAnimUpdateNodeBase`

**实现接口:** `ISchemaClass\<CBlendUpdateNode\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Children` | `ref CUtlVector\<CAnimUpdateNodeRef\>` | get | - |
| `SortedOrder` | `ref CUtlVector\<byte\>` | get | - |
| `TargetValues` | `ref CUtlVector\<float\>` | get | - |
| `BlendValueSource` | `ref AnimValueSource` | get | - |
| `LinearRootMotionBlendMode` | `ref LinearRootMotionBlendMode_t` | get | - |
| `ParamIndex` | `CAnimParamHandle` | get | - |
| `Damping` | `CAnimInputDamping` | get | - |
| `BlendKeyType` | `ref BlendKeyType` | get | - |
| `LockBlendOnReset` | `ref bool` | get, set | - |
| `SyncCycles` | `ref bool` | get | - |
| `Loop` | `ref bool` | get | - |
| `LockWhenWaning` | `ref bool` | get | - |
| `IsAngle` | `ref bool` | get | - |

