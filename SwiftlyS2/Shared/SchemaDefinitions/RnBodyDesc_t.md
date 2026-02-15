# 🔌 RnBodyDesc_t

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `ISchemaClass\<RnBodyDesc_t\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `DebugName` | `string` | get, set | - |
| `Position` | `ref Vector` | get | - |
| `Orientation` | `ref QuaternionStorage` | get | - |
| `LinearVelocity` | `ref Vector` | get | - |
| `AngularVelocity` | `ref Vector` | get | - |
| `LocalMassCenter` | `ref Vector` | get | - |
| `LocalInertiaInv` | `ISchemaFixedArray\<Vector\>` | get | - |
| `MassInv` | `ref float` | get | - |
| `GameMass` | `ref float` | get | - |
| `MassScaleInv` | `ref float` | get | - |
| `InertiaScaleInv` | `ref float` | get | - |
| `LinearDamping` | `ref float` | get | - |
| `AngularDamping` | `ref float` | get | - |
| `LinearDragScale` | `ref float` | get | - |
| `AngularDragScale` | `ref float` | get | - |
| `LinearFluidDragScale` | `ref float` | get | - |
| `AngularFluidDragScale` | `ref float` | get | - |
| `LastAwakeForceAccum` | `ref Vector` | get | - |
| `LastAwakeTorqueAccum` | `ref Vector` | get | - |
| `BuoyancyScale` | `ref float` | get | - |
| `GravityScale` | `ref float` | get | - |
| `TimeScale` | `ref float` | get | - |
| `BodyType` | `ref int` | get | - |
| `GameIndex` | `ref uint` | get | - |
| `GameFlags` | `ref uint` | get | - |
| `MinVelocityIterations` | `ref byte` | get | - |
| `MinPositionIterations` | `ref byte` | get | - |
| `MassPriority` | `ref byte` | get | - |
| `Enabled` | `ref bool` | get | - |
| `Sleeping` | `ref bool` | get | - |
| `IsContinuousEnabled` | `ref bool` | get | - |
| `DragEnabled` | `ref bool` | get | - |
| `Gravity` | `ref Vector` | get | - |
| `SpeculativeEnabled` | `ref bool` | get | - |
| `HasShadowController` | `ref bool` | get | - |
| `DynamicContinuousContactBehavior` | `ref DynamicContinuousContactBehavior_t` | get | - |

