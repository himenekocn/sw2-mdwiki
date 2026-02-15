# 📦 CCSGameRulesImpl

**命名空间:** `SwiftlyS2.Core.SchemaDefinitions`

**类型:** `class`

**继承:** `CTeamplayRulesImpl`

**实现接口:** `CCSGameRules`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `WarmupPeriodEnd` | `GameTime_t` | get, set | - |
| `WarmupPeriodStart` | `GameTime_t` | get, set | - |
| `RoundStartTime` | `GameTime_t` | get, set | - |
| `RestartRoundTime` | `GameTime_t` | get, set | - |
| `TournamentEventName` | `string` | get, set | - |
| `TournamentEventStage` | `string` | get, set | - |
| `MatchStatTxt` | `string` | get, set | - |
| `TournamentPredictionsTxt` | `string` | get, set | - |
| `CMMItemDropRevealStartTime` | `GameTime_t` | get, set | - |
| `CMMItemDropRevealEndTime` | `GameTime_t` | get, set | - |
| `ProhibitedItemIndices` | `ISchemaFixedArray\<ushort\>` | get | - |
| `TournamentActiveCasterAccounts` | `ISchemaFixedArray\<uint\>` | get, set | - |
| `MatchStats_RoundResults` | `ISchemaFixedArray\<int\>` | get | - |
| `MatchStats_PlayersAlive_CT` | `ISchemaFixedArray\<int\>` | get | - |
| `MatchStats_PlayersAlive_T` | `ISchemaFixedArray\<int\>` | get | - |
| `TeamRespawnWaveTimes` | `ISchemaFixedArray\<float\>` | get | - |
| `NextRespawnWave` | `ISchemaClassFixedArray\<GameTime_t\>` | get, set | - |
| `MinimapVerticalSectionHeights` | `ISchemaFixedArray\<float\>` | get, set | - |
| `EndMatchMapGroupVoteTypes` | `ISchemaFixedArray\<int\>` | get | - |
| `EndMatchMapGroupVoteOptions` | `ISchemaFixedArray\<int\>` | get, set | - |
| `IntermissionStartTime` | `GameTime_t` | get, set | - |
| `IntermissionEndTime` | `GameTime_t` | get, set | - |
| `QueuedMatchmakingReservationString` | `string` | get, set | - |
| `PhaseChangeAnnouncementTime` | `GameTime_t` | get, set | - |
| `LastThinkTime` | `GameTime_t` | get, set | - |
| `GameModeRules` | `CCSGameModeRules?` | get, set | - |
| `BtGlobalBlackboard` | `SchemaUntypedField` | get, set | - |
| `RetakeRules` | `CRetakeGameRules` | get, set | - |
| `TeamUniqueKillWeaponsMatch` | `ISchemaFixedArray\<CUtlVector\<int\>\>` | get | - |
| `TeamLastKillUsedUniqueWeaponMatch` | `ISchemaFixedArray\<bool\>` | get, set | - |
| `TeamIntroPeriodEnd` | `GameTime_t` | get, set | - |
| `RoundEndFunFactToken` | `string` | get, set | - |
| `RoundEndMessage` | `string` | get, set | - |

