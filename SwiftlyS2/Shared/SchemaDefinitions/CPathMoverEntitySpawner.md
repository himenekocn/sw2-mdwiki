# 🔌 CPathMoverEntitySpawner

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CLogicalEntity`

**实现接口:** `ISchemaClass\<CPathMoverEntitySpawner\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SpawnTemplates` | `ISchemaStringFixedArray` | get | - |
| `SpawnIndex` | `ref int` | get | - |
| `PathMover` | `ref CHandle\<CPathMover\>` | get | - |
| `SpawnFrequencySeconds` | `ref float` | get | - |
| `SpawnFrequencyDistToNearestMover` | `ref float` | get | - |
| `MapSpawnedMoverTemplates` | `SchemaUntypedField` | get | - |
| `MaxActive` | `ref int` | get | - |
| `LastSpawnTime` | `GameTime_t` | get | - |
| `Enabled` | `ref bool` | get | - |

