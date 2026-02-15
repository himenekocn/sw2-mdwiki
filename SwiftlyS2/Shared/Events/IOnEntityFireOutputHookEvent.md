# 🔌 IOnEntityFireOutputHookEvent

Called when the entity identity fire outputs.

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `DesignerName` | `string` | get | The designer name of the caller. |
| `OutputName` | `string` | get | The name of the input being accepted. |
| `Activator` | `CEntityInstance?` | get | The value of the input being accepted. |
| `Caller` | `CEntityInstance?` | get | The caller of the input being accepted. |
| `Delay` | `float` | get, set | This delay of this IO event, in seconds. |
| `Result` | `HookResult` | get, set | The result of the hook. |

