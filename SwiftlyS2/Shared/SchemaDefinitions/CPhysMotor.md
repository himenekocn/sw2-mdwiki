# 🔌 CPhysMotor

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CLogicalEntity`

**实现接口:** `ISchemaClass\<CPhysMotor\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `NameAttach` | `string` | get, set | - |
| `NameAnchor` | `string` | get, set | - |
| `AttachedObject` | `ref CHandle\<CBaseEntity\>` | get | - |
| `AnchorObject` | `ref CHandle\<CBaseEntity\>` | get | - |
| `SpinUp` | `ref float` | get | - |
| `SpinDown` | `ref float` | get | - |
| `MotorFriction` | `ref float` | get | - |
| `AdditionalAcceleration` | `ref float` | get | - |
| `AngularAcceleration` | `ref float` | get | - |
| `TorqueScale` | `ref float` | get | - |
| `TargetSpeed` | `ref float` | get | - |
| `SpeedWhenSpinUpOrSpinDownStarted` | `ref float` | get | - |
| `Motor` | `CMotorController` | get | - |

