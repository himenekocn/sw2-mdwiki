# 🔌 CCLCMsg_Diagnostic

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCLCMsg_Diagnostic\>`

**实现接口:** `INetMessage\<CCLCMsg_Diagnostic\>`, `IDisposable`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SystemSpecs` | `CMsgSource2SystemSpecs` | get | - |
| `VprofReport` | `CMsgSource2VProfLiteReport` | get | - |
| `DownstreamFlow` | `CMsgSource2NetworkFlowQuality` | get | - |
| `UpstreamFlow` | `CMsgSource2NetworkFlowQuality` | get | - |
| `PerfSamples` | `IProtobufRepeatedFieldSubMessageType\<CMsgSource2PerfIntervalSample\>` | get | - |

