<a id="igamehookentities"></a>

# 🔌 IGameHookEntities

**命名空间:** `SwiftlyS2.Shared.GameHooks`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TakeDamage` | `ITakeDamageEntityHook` | get | 当实体受到伤害时触发的钩子。 |
| `StartTouch` | `IStartTouchEntityHook` | get | 当实体开始接触另一个实体时触发的钩子。 |
| `Touch` | `ITouchEntityHook` | get | 当实体与另一个实体接触时触发的钩子。 |
| `EndTouch` | `IEndTouchEntityHook` | get | 当实体停止接触另一个实体时触发的钩子。 |
| `AcceptInput` | `IAcceptInputEntityHook` | get | 当实体接受输入时触发的钩子。 |
| `FireOutput` | `IFireOutputEntityHook` | get | 当实体触发输出时挂钩。 |

