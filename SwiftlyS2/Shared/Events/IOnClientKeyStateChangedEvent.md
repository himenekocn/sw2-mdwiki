<a id="ionclientkeystatechangedevent"></a>

# 🔌 IOnClientKeyStateChangedEvent

当客户端的按键状态发生变化时调用。

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlayerId` | `int` | get | 修改了按键状态的客户端的玩家 ID。 |
| `Key` | `KeyKind` | get | 被按下或释放的按键。 |
| `Pressed` | `bool` | get | 该键是被按下还是被释放。 |

