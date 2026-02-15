# 🔌 CGameInfo_CDotaGameInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CGameInfo_CDotaGameInfo\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MatchId` | `ulong` | get, set | - |
| `GameMode` | `int` | get, set | - |
| `GameWinner` | `int` | get, set | - |
| `PlayerInfo` | `IProtobufRepeatedFieldSubMessageType\<CGameInfo_CDotaGameInfo_CPlayerInfo\>` | get | - |
| `Leagueid` | `uint` | get, set | - |
| `PicksBans` | `IProtobufRepeatedFieldSubMessageType\<CGameInfo_CDotaGameInfo_CHeroSelectEvent\>` | get | - |
| `RadiantTeamId` | `uint` | get, set | - |
| `DireTeamId` | `uint` | get, set | - |
| `RadiantTeamTag` | `string` | get, set | - |
| `DireTeamTag` | `string` | get, set | - |
| `EndTime` | `uint` | get, set | - |

