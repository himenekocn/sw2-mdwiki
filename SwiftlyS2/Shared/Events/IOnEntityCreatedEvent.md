# 🔌 IOnEntityCreatedEvent

在实体创建时调用。

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Entity` | `CEntityInstance` | get | 已创建的实体。在该事件被调用时，该实体尚未完全初始化，建议在下一个游戏帧（tick）中执行相关操作，并在此处添加有效性检查。 |

