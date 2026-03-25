# 🔌 IOnClientConnectedEvent

当客户端连接到服务器时调用。

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlayerId` | `int` | get | 连接客户端的玩家 ID。 |
| `Result` | `HookResult` | get, set | 事件的执行结果。将其设置为 <see cref="HookResult.Stop"/> 可阻止玩家加入。 |

