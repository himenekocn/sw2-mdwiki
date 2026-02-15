# 🔌 CCSGameRules

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CTeamplayRules`

**实现接口:** `ISchemaClass\<CCSGameRules\>`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `WarmupPeriodEnd` | `GameTime_t` | get | - |
| `WarmupPeriodStart` | `GameTime_t` | get | - |
| `RoundStartTime` | `GameTime_t` | get | - |
| `RestartRoundTime` | `GameTime_t` | get | - |
| `TournamentEventName` | `string` | get, set | - |
| `TournamentEventStage` | `string` | get, set | - |
| `MatchStatTxt` | `string` | get, set | - |
| `TournamentPredictionsTxt` | `string` | get, set | - |
| `CMMItemDropRevealStartTime` | `GameTime_t` | get | - |
| `CMMItemDropRevealEndTime` | `GameTime_t` | get | - |
| `ProhibitedItemIndices` | `ISchemaFixedArray\<ushort\>` | get | - |
| `TournamentActiveCasterAccounts` | `ISchemaFixedArray\<uint\>` | get | - |
| `MatchStats_RoundResults` | `ISchemaFixedArray\<int\>` | get | - |
| `MatchStats_PlayersAlive_CT` | `ISchemaFixedArray\<int\>` | get | - |
| `MatchStats_PlayersAlive_T` | `ISchemaFixedArray\<int\>` | get | - |
| `TeamRespawnWaveTimes` | `ISchemaFixedArray\<float\>` | get | - |
| `NextRespawnWave` | `ISchemaClassFixedArray\<GameTime_t\>` | get | - |
| `MinimapVerticalSectionHeights` | `ISchemaFixedArray\<float\>` | get | - |
| `EndMatchMapGroupVoteTypes` | `ISchemaFixedArray\<int\>` | get | - |
| `EndMatchMapGroupVoteOptions` | `ISchemaFixedArray\<int\>` | get | - |
| `IntermissionStartTime` | `GameTime_t` | get | - |
| `IntermissionEndTime` | `GameTime_t` | get | - |
| `QueuedMatchmakingReservationString` | `string` | get, set | - |
| `PhaseChangeAnnouncementTime` | `GameTime_t` | get | - |
| `LastThinkTime` | `GameTime_t` | get | - |
| `GameModeRules` | `CCSGameModeRules?` | get | - |
| `BtGlobalBlackboard` | `SchemaUntypedField` | get | - |
| `RetakeRules` | `CRetakeGameRules` | get | - |
| `TeamUniqueKillWeaponsMatch` | `ISchemaFixedArray\<CUtlVector\<int\>\>` | get | - |
| `TeamLastKillUsedUniqueWeaponMatch` | `ISchemaFixedArray\<bool\>` | get | - |
| `TeamIntroPeriodEnd` | `GameTime_t` | get | - |
| `RoundEndFunFactToken` | `string` | get, set | - |
| `RoundEndMessage` | `string` | get, set | - |

