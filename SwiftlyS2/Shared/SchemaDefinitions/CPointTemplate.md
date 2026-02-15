# 🔌 CPointTemplate

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CLogicalEntity`

**实现接口:** `ISchemaClass\<CPointTemplate\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `WorldName` | `string` | get, set | - |
| `Source2EntityLumpName` | `string` | get, set | - |
| `EntityFilterName` | `string` | get, set | - |
| `TimeoutInterval` | `ref float` | get | - |
| `AsynchronouslySpawnEntities` | `ref bool` | get | - |
| `ClientOnlyEntityBehavior` | `ref PointTemplateClientOnlyEntityBehavior_t` | get | - |
| `OwnerSpawnGroupType` | `ref PointTemplateOwnerSpawnGroupType_t` | get | - |
| `CreatedSpawnGroupHandles` | `ref CUtlVector\<uint\>` | get | - |
| `SpawnedEntityHandles` | `ref CUtlVector\<CHandle\<CEntityInstance\>\>` | get | - |
| `ScriptSpawnCallback` | `ref HSCRIPTHandler` | get | - |
| `ScriptCallbackScope` | `ref HSCRIPTHandler` | get | - |

