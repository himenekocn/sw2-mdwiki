# 🔌 CSoundEventEntity

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseEntity`

**实现接口:** `ISchemaClass\<CSoundEventEntity\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `StartOnSpawn` | `ref bool` | get | - |
| `ToLocalPlayer` | `ref bool` | get | - |
| `StopOnNew` | `ref bool` | get | - |
| `SaveRestore` | `ref bool` | get | - |
| `SavedIsPlaying` | `ref bool` | get | - |
| `SavedElapsedTime` | `ref float` | get | - |
| `SourceEntityName` | `string` | get, set | - |
| `AttachmentName` | `string` | get, set | - |
| `OnGUIDChanged` | `SchemaUntypedField` | get | - |
| `OnSoundFinished` | `ref CEntityIOOutput` | get | - |
| `ClientCullRadius` | `ref float` | get | - |
| `SoundName` | `string` | get, set | - |
| `Source` | `ref CHandle\<CEntityInstance\>` | get | - |
| `EntityIndexSelection` | `ref int` | get | - |

