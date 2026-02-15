# 🔌 IOnConVarValueChanged

当 ConVar 的值被更改时调用。

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ConVarName` | `string` | get | 已更改的ConVar的名称。 |
| `PlayerId` | `int` | get | 做出更改的客户端的玩家ID。 |
| `NewValue` | `string` | get | ConVar 的旧值，以字符串格式表示。 |
| `OldValue` | `string` | get | ConVar的新值，以字符串格式表示。 |

