# 🔌 COrientationWarpUpdateNode

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CUnaryUpdateNode`

**实现接口:** `ISchemaClass\<COrientationWarpUpdateNode\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Mode` | `ref OrientationWarpMode_t` | get | - |
| `TargetParam` | `CAnimParamHandle` | get | - |
| `TargetPositionParam` | `CAnimParamHandle` | get | - |
| `FallbackTargetPositionParam` | `CAnimParamHandle` | get | - |
| `TargetOffsetMode` | `ref OrientationWarpTargetOffsetMode_t` | get, set | - |
| `TargetOffset` | `ref float` | get, set | - |
| `TargetOffsetParam` | `CAnimParamHandle` | get, set | - |
| `Damping` | `CAnimInputDamping` | get | - |
| `RootMotionSource` | `ref OrientationWarpRootMotionSource_t` | get | - |
| `MaxRootMotionScale` | `ref float` | get | - |
| `EnablePreferredRotationDirection` | `ref bool` | get | - |
| `PreferredRotationDirection` | `ref AnimValueSource` | get | - |
| `PreferredRotationThreshold` | `ref float` | get | - |

