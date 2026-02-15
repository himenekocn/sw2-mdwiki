# 🔌 IOnEntityCreatedEvent

Called when an entity is created.

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `Entity` | `CEntityInstance` | get | The entity that was created. The entity is not fully initialized when this event is called, better do things on next tick and also add a validity check there. |

