# 🔌 CDestructiblePart_DamageLevel

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `ISchemaClass\<CDestructiblePart_DamageLevel\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | get, set | - |
| `BreakablePieceName` | `ref CGlobalSymbol` | get | - |
| `BodyGroupValue` | `ref int` | get | - |
| `Health` | `CSkillInt` | get | - |
| `CriticalDamagePercent` | `ref float` | get | - |
| `DamagePassthroughType` | `ref EDestructiblePartDamagePassThroughType` | get | - |
| `DestructionDeathBehavior` | `ref DestructiblePartDestructionDeathBehavior_t` | get | - |
| `CustomDeathHandshake` | `ref CGlobalSymbol` | get | - |
| `ShouldDestroyOnDeath` | `ref bool` | get | - |
| `DeathDestroyTime` | `CRangeFloat` | get | - |

