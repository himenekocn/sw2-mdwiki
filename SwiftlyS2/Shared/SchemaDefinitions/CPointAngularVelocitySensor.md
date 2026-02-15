# 🔌 CPointAngularVelocitySensor

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CPointEntity`

**实现接口:** `ISchemaClass\<CPointAngularVelocitySensor\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TargetEntity` | `ref CHandle\<CBaseEntity\>` | get | - |
| `Threshold` | `ref float` | get | - |
| `LastCompareResult` | `ref int` | get | - |
| `LastFireResult` | `ref int` | get | - |
| `FireTime` | `GameTime_t` | get | - |
| `FireInterval` | `ref float` | get | - |
| `LastAngVelocity` | `ref float` | get | - |
| `LastOrientation` | `ref QAngle` | get | - |
| `Axis` | `ref Vector` | get | - |
| `UseHelper` | `ref bool` | get | - |
| `AngularVelocity` | `SchemaUntypedField` | get | - |
| `OnLessThan` | `ref CEntityIOOutput` | get | - |
| `OnLessThanOrEqualTo` | `ref CEntityIOOutput` | get | - |
| `OnGreaterThan` | `ref CEntityIOOutput` | get | - |
| `OnGreaterThanOrEqualTo` | `ref CEntityIOOutput` | get | - |
| `OnEqualTo` | `ref CEntityIOOutput` | get | - |

