# 🔌 IOnClientConnectedEvent

Called when a client connects to the server.

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `PlayerId` | `int` | get | The player ID of the client that connected. |
| `Result` | `HookResult` | get, set | The result of the event. Set this to <see cref="HookResult.Stop"/> to prevent player from joining in. |

