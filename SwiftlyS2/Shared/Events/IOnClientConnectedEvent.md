<a id="ionclientconnectedevent"></a>

# 🔌 IOnClientConnectedEvent

当客户端连接到服务器时调用。

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlayerId` | `int` | get | 已连接客户端的玩家ID。 |
| `Result` | `HookResult` | get, set | 事件的结果。将其设置为 <see cref="HookResult.Stop"/> 或 <see cref="HookResult.CancelOriginal"/> 可阻止玩家加入。 |

