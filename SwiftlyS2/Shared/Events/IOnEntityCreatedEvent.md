<a id="ionentitycreatedevent"></a>

# 🔌 IOnEntityCreatedEvent

当实体被创建时调用。

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Entity` | `CEntityInstance` | get | 被创建的实体。当此事件被调用时，实体尚未完全初始化，建议在下一帧进行处理，并在该处增加有效性检查。 |

