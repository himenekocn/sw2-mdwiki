# 🔌 CBaseCombatCharacter

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseFlex`

**实现接口:** `ISchemaClass\<CBaseCombatCharacter\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ForceServerRagdoll` | `ref bool` | get | - |
| `MyWearables` | `ref CUtlVector\<CHandle\<CEconWearable\>\>` | get | - |
| `ImpactEnergyScale` | `ref float` | get | - |
| `ApplyStressDamage` | `ref bool` | get | - |
| `DeathEventsDispatched` | `ref bool` | get | - |
| `VecRelationships` | `ref CUtlVector\<RelationshipOverride_t\>` | get | - |
| `StrRelationships` | `string` | get, set | - |
| `Hull` | `ref Hull_t` | get | - |
| `NavHullIdx` | `ref uint` | get | - |
| `MovementStats` | `CMovementStatsProperty` | get | - |

## ⚙️ 方法

### MyWearablesUpdated

```csharp
void MyWearablesUpdated()
```

