# 🔌 CSVCMsg_PacketEntities

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_PacketEntities\>`

**实现接口:** `INetMessage\<CSVCMsg_PacketEntities\>`, `IDisposable`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MaxEntries` | `int` | get, set | - |
| `UpdatedEntries` | `int` | get, set | - |
| `LegacyIsDelta` | `bool` | get, set | - |
| `UpdateBaseline` | `bool` | get, set | - |
| `Baseline` | `int` | get, set | - |
| `DeltaFrom` | `int` | get, set | - |
| `EntityData` | `byte[]` | get, set | - |
| `PendingFullFrame` | `bool` | get, set | - |
| `ActiveSpawngroupHandle` | `uint` | get, set | - |
| `MaxSpawngroupCreationsequence` | `uint` | get, set | - |
| `LastCmdNumberExecuted` | `uint` | get, set | - |
| `LastCmdNumberRecvDelta` | `int` | get, set | - |
| `ServerTick` | `uint` | get, set | - |
| `SerializedEntities` | `byte[]` | get, set | - |
| `AlternateBaselines` | `IProtobufRepeatedFieldSubMessageType\<CSVCMsg_PacketEntities_alternate_baseline_t\>` | get | - |
| `HasPvsVisBitsDeprecated` | `uint` | get, set | - |
| `CmdRecvStatus` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `NonTransmittedEntities` | `CSVCMsg_PacketEntities_non_transmitted_entities_t` | get | - |
| `CqStarvedCommandTicks` | `uint` | get, set | - |
| `CqDiscardedCommandTicks` | `uint` | get, set | - |
| `OutofpvsEntityUpdates` | `CSVCMsg_PacketEntities_outofpvs_entity_updates_t` | get | - |
| `DevPadding` | `byte[]` | get, set | - |

