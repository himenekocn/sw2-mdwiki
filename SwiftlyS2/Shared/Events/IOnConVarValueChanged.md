<a id="ionconvarvaluechanged"></a>

# 🔌 IOnConVarValueChanged

当 ConVar 值发生改变时调用。

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ConVarName` | `string` | get | 改变的ConVar名称。 |
| `PlayerId` | `int` | get | 发起更改的客户端的玩家ID。 |
| `NewValue` | `string` | get | ConVar 的旧值（字符串格式）。 |
| `OldValue` | `string` | get | ConVar 的新值，以字符串格式表示。 |

