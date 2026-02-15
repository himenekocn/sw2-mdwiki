# 🔌 VPhysXAggregateData_t

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `ISchemaClass\<VPhysXAggregateData_t\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Flags` | `ref ushort` | get | - |
| `RefCounter` | `ref ushort` | get | - |
| `BonesHash` | `ref CUtlVector\<uint\>` | get | - |
| `BoneNames` | `ref CUtlVector\<CUtlString\>` | get | - |
| `IndexNames` | `ref CUtlVector\<ushort\>` | get | - |
| `IndexHash` | `ref CUtlVector\<ushort\>` | get | - |
| `BindPose` | `ref CUtlVector\<matrix3x4_t\>` | get | - |
| `Parts` | `ref CUtlVector\<VPhysXBodyPart_t\>` | get | - |
| `ShapeMarkups` | `ref CUtlVector\<PhysShapeMarkup_t\>` | get | - |
| `Constraints2` | `ref CUtlVector\<VPhysXConstraint2_t\>` | get | - |
| `Joints` | `ref CUtlVector\<VPhysXJoint_t\>` | get | - |
| `FeModel` | `PhysFeModelDesc_t?` | get | - |
| `BoneParents` | `ref CUtlVector\<ushort\>` | get | - |
| `SurfacePropertyHashes` | `ref CUtlVector\<uint\>` | get | - |
| `CollisionAttributes` | `ref CUtlVector\<VPhysXCollisionAttributes_t\>` | get | - |
| `DebugPartNames` | `ref CUtlVector\<CUtlString\>` | get | - |
| `EmbeddedKeyvalues` | `string` | get, set | - |

