# 🔌 CCSUsrMsg_SurvivalStats

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_SurvivalStats\>`

**实现接口:** `INetMessage\<CCSUsrMsg_SurvivalStats\>`, `IDisposable`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `Xuid` | `ulong` | get, set | - |
| `Facts` | `IProtobufRepeatedFieldSubMessageType\<CCSUsrMsg_SurvivalStats_Fact\>` | get | - |
| `Users` | `IProtobufRepeatedFieldSubMessageType\<CCSUsrMsg_SurvivalStats_Placement\>` | get, set | - |
| `Damages` | `IProtobufRepeatedFieldSubMessageType\<CCSUsrMsg_SurvivalStats_Damage\>` | get, set | - |
| `Ticknumber` | `int` | get, set | - |

