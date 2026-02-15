# 🔌 CUserMessage_DllStatus

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessage_DllStatus\>`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `FileReport` | `string` | get, set | - |
| `CommandLine` | `string` | get, set | - |
| `TotalFiles` | `uint` | get, set | - |
| `ProcessId` | `uint` | get, set | - |
| `Osversion` | `int` | get, set | - |
| `ClientTime` | `ulong` | get, set | - |
| `Diagnostics` | `IProtobufRepeatedFieldSubMessageType\<CUserMessage_DllStatus_CVDiagnostic\>` | get | - |
| `Modules` | `IProtobufRepeatedFieldSubMessageType\<CUserMessage_DllStatus_CModule\>` | get | - |

