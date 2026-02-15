# 🔌 CNavLinkAreaEntity

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CPointEntity`

**实现接口:** `ISchemaClass\<CNavLinkAreaEntity\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Width` | `ref float` | get | - |
| `LocatorOffset` | `ref Vector` | get, set | - |
| `LocatorAnglesOffset` | `ref QAngle` | get, set | - |
| `StrMovementForward` | `string` | get, set | - |
| `StrMovementReverse` | `string` | get, set | - |
| `Enabled` | `ref bool` | get | - |
| `AllowCrossMovableConnections` | `ref bool` | get | - |
| `StrFilterName` | `string` | get, set | - |
| `Filter` | `ref CHandle\<CBaseFilter\>` | get | - |
| `OnNavLinkStart` | `ref CEntityIOOutput` | get | - |
| `OnNavLinkFinish` | `ref CEntityIOOutput` | get | - |
| `IsTerminus` | `ref bool` | get | - |
| `Splits` | `ref int` | get | - |

