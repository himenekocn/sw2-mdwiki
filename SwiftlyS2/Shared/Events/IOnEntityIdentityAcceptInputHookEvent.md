# 🔌 IOnEntityIdentityAcceptInputHookEvent

Called when the entity identity accept input hook is triggered.

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `Identity` | `CEntityIdentity` | get | The entity identity. |
| `EntityInstance` | `CEntityInstance` | get | The entity instance. |
| `DesignerName` | `string` | get | The designer name of the caller. |
| `InputName` | `string` | get | The name of the input being accepted. |
| `Activator` | `CEntityInstance?` | get | The value of the input being accepted. |
| `Caller` | `CEntityInstance?` | get | The caller of the input being accepted. |
| `OutputId` | `int` | get, set | The output ID of the input being accepted. |
| `Result` | `HookResult` | get, set | The result of the hook. |

