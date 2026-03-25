<a id="ionentityidentityacceptinputhookevent"></a>

# 🔌 IOnEntityIdentityAcceptInputHookEvent

当实体身份接受输入钩子被触发时调用。

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Identity` | `CEntityIdentity` | get | 实体标识。 |
| `EntityInstance` | `CEntityInstance` | get | 实体实例。 |
| `DesignerName` | `string` | get | 调用方的设计师名称。 |
| `InputName` | `string` | get | 正在接受的输入的名称。 |
| `Activator` | `CEntityInstance?` | get | 被接受输入的数值。 |
| `Caller` | `CEntityInstance?` | get | 接受输入的调用方。 |
| `VariantValue` | `ref CVariant\<CVariantDefaultAllocator\>` | get | 正在接受的输入变体值。 |
| `OutputId` | `int` | get | 被接受输入的输出 ID。 |
| `Result` | `HookResult` | get, set | 钩子的结果。 |

