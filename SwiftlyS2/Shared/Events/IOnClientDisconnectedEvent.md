# 🔌 IOnClientDisconnectedEvent

Called when a client disconnects from the server.

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `PlayerId` | `int` | get | The player ID of the client that disconnected. |
| `Reason` | `ENetworkDisconnectionReason` | get | The reason for the client to disconnect. |

