# 🔌 CMsgGCCStrike15_v2_MatchmakingGC2ServerReserve

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_MatchmakingGC2ServerReserve\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AccountIds` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `GameType` | `uint` | get, set | - |
| `MatchId` | `ulong` | get, set | - |
| `ServerVersion` | `uint` | get, set | - |
| `Flags` | `uint` | get, set | - |
| `Rankings` | `IProtobufRepeatedFieldSubMessageType\<PlayerRankingInfo\>` | get | - |
| `EncryptionKey` | `ulong` | get, set | - |
| `EncryptionKeyPub` | `ulong` | get, set | - |
| `PartyIds` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `Whitelist` | `IProtobufRepeatedFieldSubMessageType\<IpAddressMask\>` | get | - |
| `TvMasterSteamid` | `ulong` | get, set | - |
| `TournamentEvent` | `TournamentEvent` | get | - |
| `TournamentTeams` | `IProtobufRepeatedFieldSubMessageType\<TournamentTeam\>` | get | - |
| `TournamentCastersAccountIds` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `TvRelaySteamid` | `ulong` | get, set | - |
| `PreMatchData` | `CPreMatchInfoData` | get | - |
| `TvControl` | `uint` | get, set | - |
| `OpVarValues` | `IProtobufRepeatedFieldSubMessageType\<OperationalVarValue\>` | get | - |
| `SocacheControl` | `uint` | get, set | - |
| `TeammateColors` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `MatchIdAdditional` | `uint` | get, set | - |

