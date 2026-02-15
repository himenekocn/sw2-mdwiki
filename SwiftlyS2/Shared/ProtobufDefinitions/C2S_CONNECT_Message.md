# 🔌 C2S_CONNECT_Message

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<C2S_CONNECT_Message\>`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `HostVersion` | `uint` | get, set | - |
| `AuthProtocol` | `uint` | get, set | - |
| `ChallengeNumber` | `uint` | get, set | - |
| `ReservationCookie` | `ulong` | get, set | - |
| `LowViolence` | `bool` | get, set | - |
| `EncryptedPassword` | `byte[]` | get, set | - |
| `Splitplayers` | `IProtobufRepeatedFieldSubMessageType\<CCLCMsg_SplitPlayerConnect\>` | get, set | - |
| `AuthSteam` | `byte[]` | get, set | - |
| `ChallengeContext` | `string` | get, set | - |
| `LocalhostSameProcessCheck` | `C2S_CONNECT_SameProcessCheck` | get | - |

