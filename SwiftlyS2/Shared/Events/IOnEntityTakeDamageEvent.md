# 🔌 IOnEntityTakeDamageEvent

Called when an entity takes damage.

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `Entity` | `CEntityInstance` | get | The entity that took damage. |
| `Result` | `HookResult` | get, set | If return <see cref="HookResult.Stop"/>, the damage will not be applied. |

