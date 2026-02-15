# 🔌 IOnConVarValueChanged

Called when a ConVar value is changed.

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `ConVarName` | `string` | get | The name of the ConVar that changed. |
| `PlayerId` | `int` | get | The player ID of the client that made the change. |
| `NewValue` | `string` | get | The old value of the ConVar in string format. |
| `OldValue` | `string` | get | The new value of the ConVar in string format. |

