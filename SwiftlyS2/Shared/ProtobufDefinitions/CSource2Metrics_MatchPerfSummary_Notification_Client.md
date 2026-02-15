# 🔌 CSource2Metrics_MatchPerfSummary_Notification_Client

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSource2Metrics_MatchPerfSummary_Notification_Client\>`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `SystemSpecs` | `CMsgSource2SystemSpecs` | get, set | - |
| `Profile` | `CMsgSource2VProfLiteReport` | get, set | - |
| `BuildId` | `uint` | get, set | - |
| `DownstreamFlow` | `CMsgSource2NetworkFlowQuality` | get, set | - |
| `UpstreamFlow` | `CMsgSource2NetworkFlowQuality` | get, set | - |
| `Steamid` | `ulong` | get, set | - |
| `PerfSamples` | `IProtobufRepeatedFieldSubMessageType\<CMsgSource2PerfIntervalSample\>` | get | - |

