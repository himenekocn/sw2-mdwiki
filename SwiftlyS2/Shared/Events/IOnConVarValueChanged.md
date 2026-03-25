<a id="ionconvarvaluechanged"></a>

# 🔌 IOnConVarValueChanged

当 ConVar 的值被更改时调用。

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ConVarName` | `string` | get | 变更的 ConVar 名称。 |
| `PlayerId` | `int` | get | 执行更改的客户端的玩家 ID。 |
| `NewValue` | `string` | get | 该 ConVar 的旧值，以字符串格式表示。 |
| `OldValue` | `string` | get | CVar 的新值，以字符串格式表示。 |

