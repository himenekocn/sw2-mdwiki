# 🔌 IOnClientDisconnectedEvent

当客户端与服务器断开连接时调用。

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlayerId` | `int` | get | 已断开连接的客户端的玩家ID。 |
| `Reason` | `ENetworkDisconnectionReason` | get | 客户端断开连接的原因。 |

