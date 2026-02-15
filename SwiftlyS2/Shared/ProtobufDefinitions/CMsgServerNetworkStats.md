# 🔌 CMsgServerNetworkStats

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgServerNetworkStats\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Dedicated` | `bool` | get, set | - |
| `CpuUsage` | `int` | get, set | - |
| `MemoryUsedMb` | `int` | get, set | - |
| `MemoryFreeMb` | `int` | get, set | - |
| `Uptime` | `int` | get, set | - |
| `SpawnCount` | `int` | get, set | - |
| `NumClients` | `int` | get, set | - |
| `NumBots` | `int` | get, set | - |
| `NumSpectators` | `int` | get, set | - |
| `NumTvRelays` | `int` | get, set | - |
| `Fps` | `float` | get, set | - |
| `Ports` | `IProtobufRepeatedFieldSubMessageType\<CMsgServerNetworkStats_Port\>` | get | - |
| `AvgPingMs` | `float` | get, set | - |
| `AvgEngineLatencyOut` | `float` | get, set | - |
| `AvgPacketsOut` | `float` | get, set | - |
| `AvgPacketsIn` | `float` | get, set | - |
| `AvgLossOut` | `float` | get, set | - |
| `AvgLossIn` | `float` | get, set | - |
| `AvgDataOut` | `float` | get, set | - |
| `AvgDataIn` | `float` | get, set | - |
| `TotalDataIn` | `ulong` | get, set | - |
| `TotalPacketsIn` | `ulong` | get, set | - |
| `TotalDataOut` | `ulong` | get, set | - |
| `TotalPacketsOut` | `ulong` | get, set | - |
| `Players` | `IProtobufRepeatedFieldSubMessageType\<CMsgServerNetworkStats_Player\>` | get | - |

