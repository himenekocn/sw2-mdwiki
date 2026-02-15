# 🔌 CBombTarget

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseTrigger`

**实现接口:** `ISchemaClass\<CBombTarget\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `OnBombExplode` | `ref CEntityIOOutput` | get | - |
| `OnBombPlanted` | `ref CEntityIOOutput` | get | - |
| `OnBombDefused` | `ref CEntityIOOutput` | get | - |
| `IsBombSiteB` | `ref bool` | get | - |
| `IsHeistBombTarget` | `ref bool` | get | - |
| `BombPlantedHere` | `ref bool` | get | - |
| `MountTarget` | `string` | get, set | - |
| `InstructorHint` | `ref CHandle\<CBaseEntity\>` | get | - |
| `BombSiteDesignation` | `ref int` | get | - |

## ⚙️ 方法

### BombPlantedHereUpdated

```csharp
void BombPlantedHereUpdated()
```

