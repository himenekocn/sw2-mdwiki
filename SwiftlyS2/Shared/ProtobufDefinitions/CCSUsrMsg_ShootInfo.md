# 🔌 CCSUsrMsg_ShootInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_ShootInfo\>`

**实现接口:** `INetMessage\<CCSUsrMsg_ShootInfo\>`, `IDisposable`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `FrameNumber` | `int` | get, set | - |
| `HitboxTransforms` | `IProtobufRepeatedFieldSubMessageType\<CMsgTransform\>` | get | - |
| `ShootPos` | `Vector` | get, set | - |
| `ShootDir` | `QAngle` | get, set | - |

