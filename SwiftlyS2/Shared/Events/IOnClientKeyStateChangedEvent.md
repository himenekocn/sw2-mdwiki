# 🔌 IOnClientKeyStateChangedEvent

Called when a client's key state changes.

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `PlayerId` | `int` | get | The player ID of the client that changed their key state. |
| `Key` | `KeyKind` | get | The key that was pressed or released. |
| `Pressed` | `bool` | get | Whether the key was pressed or released. |

