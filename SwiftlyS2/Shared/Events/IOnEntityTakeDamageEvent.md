# 🔌 IOnEntityTakeDamageEvent

当实体受到伤害时调用。

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Entity` | `CEntityInstance` | get | 受到伤害的实体。 |
| `Info` | `ref CTakeDamageInfo` | get | 伤害信息。 |
| `DamageResult` | `ref CTakeDamageResult` | get | 伤害结果。 |
| `Result` | `HookResult` | get, set | 如果返回 <see cref="HookResult.Stop"/>，则不会应用伤害。 |

