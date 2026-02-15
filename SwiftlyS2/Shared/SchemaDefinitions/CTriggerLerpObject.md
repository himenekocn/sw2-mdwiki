# 🔌 CTriggerLerpObject

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseTrigger`

**实现接口:** `ISchemaClass\<CTriggerLerpObject\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `LerpTarget` | `string` | get, set | - |
| `LerpTarget1` | `ref CHandle\<CBaseEntity\>` | get | - |
| `LerpTargetAttachment` | `string` | get, set | - |
| `LerpTargetAttachment2` | `AttachmentHandle_t` | get | - |
| `LerpDuration` | `ref float` | get | - |
| `AttachedEntityWasParented` | `ref bool` | get | - |
| `LerpRestoreMoveType` | `ref bool` | get | - |
| `SingleLerpObject` | `ref bool` | get | - |
| `LerpingObjects` | `ref CUtlVector\<lerpdata_t\>` | get | - |
| `LerpEffect` | `string` | get, set | - |
| `LerpSound` | `string` | get, set | - |
| `AttachTouchingObject` | `ref bool` | get | - |
| `EntityToWaitForDisconnect` | `ref CHandle\<CBaseEntity\>` | get | - |
| `OnLerpStarted` | `ref CEntityIOOutput` | get | - |
| `OnLerpFinished` | `ref CEntityIOOutput` | get | - |
| `OnDetached` | `ref CEntityIOOutput` | get | - |

