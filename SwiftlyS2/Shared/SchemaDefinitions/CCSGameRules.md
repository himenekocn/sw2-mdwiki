# 🔌 CCSGameRules

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CTeamplayRules`

**实现接口:** `ISchemaClass\<CCSGameRules\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `FreezePeriod` | `ref bool` | get | - |
| `WarmupPeriod` | `ref bool` | get | - |
| `WarmupPeriodEnd` | `GameTime_t` | get | - |
| `WarmupPeriodStart` | `GameTime_t` | get | - |
| `TerroristTimeOutActive` | `ref bool` | get | - |
| `CTTimeOutActive` | `ref bool` | get | - |
| `TerroristTimeOutRemaining` | `ref float` | get | - |
| `CTTimeOutRemaining` | `ref float` | get | - |
| `TerroristTimeOuts` | `ref int` | get | - |
| `CTTimeOuts` | `ref int` | get | - |
| `TechnicalTimeOut` | `ref bool` | get | - |
| `MatchWaitingForResume` | `ref bool` | get | - |
| `FreezeTime` | `ref int` | get | - |
| `RoundTime` | `ref int` | get | - |
| `MatchStartTime` | `ref float` | get | - |
| `RoundStartTime` | `GameTime_t` | get | - |
| `RestartRoundTime` | `GameTime_t` | get | - |
| `GameRestart` | `ref bool` | get | - |
| `GameStartTime` | `ref float` | get | - |
| `TimeUntilNextPhaseStarts` | `ref float` | get | - |
| `GamePhase` | `ref int` | get | - |
| `TotalRoundsPlayed` | `ref int` | get | - |
| `RoundsPlayedThisPhase` | `ref int` | get | - |
| `OvertimePlaying` | `ref int` | get | - |
| `HostagesRemaining` | `ref int` | get | - |
| `AnyHostageReached` | `ref bool` | get | - |
| `MapHasBombTarget` | `ref bool` | get | - |
| `MapHasRescueZone` | `ref bool` | get | - |
| `MapHasBuyZone` | `ref bool` | get | - |
| `IsQueuedMatchmaking` | `ref bool` | get | - |
| `QueuedMatchmakingMode` | `ref int` | get | - |
| `IsValveDS` | `ref bool` | get | - |
| `LogoMap` | `ref bool` | get | - |
| `PlayAllStepSoundsOnServer` | `ref bool` | get | - |
| `SpectatorSlotCount` | `ref int` | get | - |
| `MatchDevice` | `ref int` | get | - |
| `HasMatchStarted` | `ref bool` | get | - |
| `NextMapInMapgroup` | `ref int` | get | - |
| `TournamentEventName` | `string` | get, set | - |
| `TournamentEventStage` | `string` | get, set | - |
| `MatchStatTxt` | `string` | get, set | - |
| `TournamentPredictionsTxt` | `string` | get, set | - |
| `TournamentPredictionsPct` | `ref int` | get | - |
| `CMMItemDropRevealStartTime` | `GameTime_t` | get | - |
| `CMMItemDropRevealEndTime` | `GameTime_t` | get | - |
| `IsDroppingItems` | `ref bool` | get | - |
| `IsQuestEligible` | `ref bool` | get | - |
| `IsHltvActive` | `ref bool` | get | - |
| `BombPlanted` | `ref bool` | get | - |
| `ProhibitedItemIndices` | `ISchemaFixedArray\<ushort\>` | get | - |
| `TournamentActiveCasterAccounts` | `ISchemaFixedArray\<uint\>` | get | - |
| `NumBestOfMaps` | `ref int` | get | - |
| `HalloweenMaskListSeed` | `ref int` | get | - |
| `BombDropped` | `ref bool` | get | - |
| `RoundWinStatus` | `ref int` | get | - |
| `RoundWinReason` | `ref int` | get | - |
| `TCantBuy` | `ref bool` | get | - |
| `CTCantBuy` | `ref bool` | get | - |
| `MatchStats_RoundResults` | `ISchemaFixedArray\<int\>` | get | - |
| `MatchStats_PlayersAlive_CT` | `ISchemaFixedArray\<int\>` | get | - |
| `MatchStats_PlayersAlive_T` | `ISchemaFixedArray\<int\>` | get | - |
| `TeamRespawnWaveTimes` | `ISchemaFixedArray\<float\>` | get | - |
| `NextRespawnWave` | `ISchemaClassFixedArray\<GameTime_t\>` | get | - |
| `MinimapMins` | `ref Vector` | get | - |
| `MinimapMaxs` | `ref Vector` | get | - |
| `MinimapVerticalSectionHeights` | `ISchemaFixedArray\<float\>` | get | - |
| `UllLocalMatchID` | `ref ulong` | get | - |
| `EndMatchMapGroupVoteTypes` | `ISchemaFixedArray\<int\>` | get | - |
| `EndMatchMapGroupVoteOptions` | `ISchemaFixedArray\<int\>` | get | - |
| `EndMatchMapVoteWinner` | `ref int` | get | - |
| `NumConsecutiveCTLoses` | `ref int` | get | - |
| `NumConsecutiveTerroristLoses` | `ref int` | get | - |
| `HasHostageBeenTouched` | `ref bool` | get | - |
| `IntermissionStartTime` | `GameTime_t` | get | - |
| `IntermissionEndTime` | `GameTime_t` | get | - |
| `LevelInitialized` | `ref bool` | get | - |
| `TotalRoundsPlayed1` | `ref int` | get | - |
| `UnBalancedRounds` | `ref int` | get | - |
| `EndMatchOnRoundReset` | `ref bool` | get, set | - |
| `EndMatchOnThink` | `ref bool` | get | - |
| `NumTerrorist` | `ref int` | get | - |
| `NumCT` | `ref int` | get | - |
| `NumSpawnableTerrorist` | `ref int` | get | - |
| `NumSpawnableCT` | `ref int` | get | - |
| `SelectedHostageSpawnIndices` | `ref CUtlVector\<int\>` | get | - |
| `SpawnPointsRandomSeed` | `ref int` | get | - |
| `FirstConnected` | `ref bool` | get | - |
| `CompleteReset` | `ref bool` | get, set | - |
| `PickNewTeamsOnReset` | `ref bool` | get, set | - |
| `ScrambleTeamsOnRestart` | `ref bool` | get | - |
| `SwapTeamsOnRestart` | `ref bool` | get | - |
| `EndMatchTiedVotes` | `ref CUtlVector\<int\>` | get | - |
| `NeedToAskPlayersForContinueVote` | `ref bool` | get | - |
| `NumQueuedMatchmakingAccounts` | `ref uint` | get | - |
| `AvgPlayerRank` | `ref float` | get | - |
| `QueuedMatchmakingReservationString` | `string` | get, set | - |
| `NumTotalTournamentDrops` | `ref uint` | get | - |
| `NumSpectatorsCountMax` | `ref uint` | get | - |
| `NumSpectatorsCountMaxTV` | `ref uint` | get | - |
| `NumSpectatorsCountMaxLnk` | `ref uint` | get | - |
| `CTsAliveAtFreezetimeEnd` | `ref int` | get | - |
| `TerroristsAliveAtFreezetimeEnd` | `ref int` | get | - |
| `ForceTeamChangeSilent` | `ref bool` | get | - |
| `LoadingRoundBackupData` | `ref bool` | get | - |
| `MatchInfoShowType` | `ref int` | get | - |
| `MatchInfoDecidedTime` | `ref float` | get | - |
| `MTeamDMLastWinningTeamNumber` | `ref int` | get | - |
| `MTeamDMLastThinkTime` | `ref float` | get | - |
| `TeamDMLastAnnouncementTime` | `ref float` | get | - |
| `AccountTerrorist` | `ref int` | get | - |
| `AccountCT` | `ref int` | get | - |
| `SpawnPointCount_Terrorist` | `ref int` | get | - |
| `SpawnPointCount_CT` | `ref int` | get | - |
| `MaxNumTerrorists` | `ref int` | get | - |
| `MaxNumCTs` | `ref int` | get | - |
| `LoserBonusMostRecentTeam` | `ref int` | get | - |
| `TmNextPeriodicThink` | `ref float` | get | - |
| `VoiceWonMatchBragFired` | `ref bool` | get | - |
| `WarmupNextChatNoticeTime` | `ref float` | get | - |
| `HostagesRescued` | `ref int` | get | - |
| `HostagesTouched` | `ref int` | get | - |
| `NextHostageAnnouncement` | `ref float` | get | - |
| `NoTerroristsKilled` | `ref bool` | get | - |
| `NoCTsKilled` | `ref bool` | get | - |
| `NoEnemiesKilled` | `ref bool` | get | - |
| `CanDonateWeapons` | `ref bool` | get | - |
| `FirstKillTime` | `ref float` | get | - |
| `FirstBloodTime` | `ref float` | get | - |
| `HostageWasInjured` | `ref bool` | get | - |
| `HostageWasKilled` | `ref bool` | get | - |
| `VoteCalled` | `ref bool` | get | - |
| `ServerVoteOnReset` | `ref bool` | get, set | - |
| `VoteCheckThrottle` | `ref float` | get | - |
| `BuyTimeEnded` | `ref bool` | get | - |
| `LastFreezeEndBeep` | `ref int` | get | - |
| `TargetBombed` | `ref bool` | get | - |
| `BombDefused` | `ref bool` | get | - |
| `MapHasBombZone` | `ref bool` | get | - |
| `MainCTSpawnPos` | `ref Vector` | get | - |
| `CTSpawnPointsMasterList` | `ref CUtlVector\<CHandle\<SpawnPoint\>\>` | get | - |
| `TerroristSpawnPointsMasterList` | `ref CUtlVector\<CHandle\<SpawnPoint\>\>` | get | - |
| `RespawningAllRespawnablePlayers` | `ref bool` | get | - |
| `NextCTSpawnPoint` | `ref int` | get | - |
| `CTSpawnPointUsedTime` | `ref float` | get | - |
| `NextTerroristSpawnPoint` | `ref int` | get | - |
| `TerroristSpawnPointUsedTime` | `ref float` | get | - |
| `CTSpawnPoints` | `ref CUtlVector\<CHandle\<SpawnPoint\>\>` | get | - |
| `TerroristSpawnPoints` | `ref CUtlVector\<CHandle\<SpawnPoint\>\>` | get | - |
| `IsUnreservedGameServer` | `ref bool` | get | - |
| `AutobalanceDisplayTime` | `ref float` | get | - |
| `AllowWeaponSwitch` | `ref bool` | get | - |
| `RoundTimeWarningTriggered` | `ref bool` | get | - |
| `PhaseChangeAnnouncementTime` | `GameTime_t` | get | - |
| `NextUpdateTeamClanNamesTime` | `ref float` | get | - |
| `LastThinkTime` | `GameTime_t` | get | - |
| `AccumulatedRoundOffDamage` | `ref float` | get | - |
| `ShorthandedBonusLastEvalRound` | `ref int` | get | - |
| `MatchAbortedEarlyReason` | `ref int` | get | - |
| `HasTriggeredRoundStartMusic` | `ref bool` | get | - |
| `SwitchingTeamsAtRoundReset` | `ref bool` | get, set | - |
| `GameModeRules` | `CCSGameModeRules?` | get | - |
| `BtGlobalBlackboard` | `SchemaUntypedField` | get | - |
| `PlayerResource` | `ref CHandle\<CBaseEntity\>` | get | - |
| `RetakeRules` | `CRetakeGameRules` | get | - |
| `TeamUniqueKillWeaponsMatch` | `ISchemaFixedArray\<CUtlVector\<int\>\>` | get | - |
| `TeamLastKillUsedUniqueWeaponMatch` | `ISchemaFixedArray\<bool\>` | get | - |
| `MatchEndCount` | `ref byte` | get | - |
| `TTeamIntroVariant` | `ref int` | get | - |
| `CTTeamIntroVariant` | `ref int` | get | - |
| `TeamIntroPeriod` | `ref bool` | get | - |
| `TeamIntroPeriodEnd` | `GameTime_t` | get | - |
| `PlayedTeamIntroVO` | `ref bool` | get | - |
| `RoundEndWinnerTeam` | `ref int` | get | - |
| `RoundEndReason` | `ref int` | get | - |
| `RoundEndShowTimerDefend` | `ref bool` | get | - |
| `RoundEndTimerTime` | `ref int` | get | - |
| `RoundEndFunFactToken` | `string` | get, set | - |
| `RoundEndFunFactPlayerSlot` | `ref uint` | get | - |
| `RoundEndFunFactData1` | `ref int` | get | - |
| `RoundEndFunFactData2` | `ref int` | get | - |
| `RoundEndFunFactData3` | `ref int` | get | - |
| `RoundEndMessage` | `string` | get, set | - |
| `RoundEndPlayerCount` | `ref int` | get | - |
| `RoundEndNoMusic` | `ref bool` | get | - |
| `RoundEndLegacy` | `ref int` | get | - |
| `RoundEndCount` | `ref byte` | get | - |
| `RoundStartRoundNumber` | `ref int` | get | - |
| `RoundStartCount` | `ref byte` | get | - |
| `LastPerfSampleTime` | `ref double` | get | - |

## ⚙️ 方法

### FreezePeriodUpdated

```csharp
void FreezePeriodUpdated()
```

### WarmupPeriodUpdated

```csharp
void WarmupPeriodUpdated()
```

### WarmupPeriodEndUpdated

```csharp
void WarmupPeriodEndUpdated()
```

### WarmupPeriodStartUpdated

```csharp
void WarmupPeriodStartUpdated()
```

### TerroristTimeOutActiveUpdated

```csharp
void TerroristTimeOutActiveUpdated()
```

### CTTimeOutActiveUpdated

```csharp
void CTTimeOutActiveUpdated()
```

### TerroristTimeOutRemainingUpdated

```csharp
void TerroristTimeOutRemainingUpdated()
```

### CTTimeOutRemainingUpdated

```csharp
void CTTimeOutRemainingUpdated()
```

### TerroristTimeOutsUpdated

```csharp
void TerroristTimeOutsUpdated()
```

### CTTimeOutsUpdated

```csharp
void CTTimeOutsUpdated()
```

### TechnicalTimeOutUpdated

```csharp
void TechnicalTimeOutUpdated()
```

### MatchWaitingForResumeUpdated

```csharp
void MatchWaitingForResumeUpdated()
```

### FreezeTimeUpdated

```csharp
void FreezeTimeUpdated()
```

### RoundTimeUpdated

```csharp
void RoundTimeUpdated()
```

### MatchStartTimeUpdated

```csharp
void MatchStartTimeUpdated()
```

### RoundStartTimeUpdated

```csharp
void RoundStartTimeUpdated()
```

### RestartRoundTimeUpdated

```csharp
void RestartRoundTimeUpdated()
```

### GameRestartUpdated

```csharp
void GameRestartUpdated()
```

### GameStartTimeUpdated

```csharp
void GameStartTimeUpdated()
```

### TimeUntilNextPhaseStartsUpdated

```csharp
void TimeUntilNextPhaseStartsUpdated()
```

### GamePhaseUpdated

```csharp
void GamePhaseUpdated()
```

### TotalRoundsPlayedUpdated

```csharp
void TotalRoundsPlayedUpdated()
```

### RoundsPlayedThisPhaseUpdated

```csharp
void RoundsPlayedThisPhaseUpdated()
```

### OvertimePlayingUpdated

```csharp
void OvertimePlayingUpdated()
```

### HostagesRemainingUpdated

```csharp
void HostagesRemainingUpdated()
```

### AnyHostageReachedUpdated

```csharp
void AnyHostageReachedUpdated()
```

### MapHasBombTargetUpdated

```csharp
void MapHasBombTargetUpdated()
```

### MapHasRescueZoneUpdated

```csharp
void MapHasRescueZoneUpdated()
```

### MapHasBuyZoneUpdated

```csharp
void MapHasBuyZoneUpdated()
```

### IsQueuedMatchmakingUpdated

```csharp
void IsQueuedMatchmakingUpdated()
```

### QueuedMatchmakingModeUpdated

```csharp
void QueuedMatchmakingModeUpdated()
```

### IsValveDSUpdated

```csharp
void IsValveDSUpdated()
```

### LogoMapUpdated

```csharp
void LogoMapUpdated()
```

### PlayAllStepSoundsOnServerUpdated

```csharp
void PlayAllStepSoundsOnServerUpdated()
```

### SpectatorSlotCountUpdated

```csharp
void SpectatorSlotCountUpdated()
```

### MatchDeviceUpdated

```csharp
void MatchDeviceUpdated()
```

### HasMatchStartedUpdated

```csharp
void HasMatchStartedUpdated()
```

### NextMapInMapgroupUpdated

```csharp
void NextMapInMapgroupUpdated()
```

### TournamentEventNameUpdated

```csharp
void TournamentEventNameUpdated()
```

### TournamentEventStageUpdated

```csharp
void TournamentEventStageUpdated()
```

### MatchStatTxtUpdated

```csharp
void MatchStatTxtUpdated()
```

### TournamentPredictionsTxtUpdated

```csharp
void TournamentPredictionsTxtUpdated()
```

### TournamentPredictionsPctUpdated

```csharp
void TournamentPredictionsPctUpdated()
```

### CMMItemDropRevealStartTimeUpdated

```csharp
void CMMItemDropRevealStartTimeUpdated()
```

### CMMItemDropRevealEndTimeUpdated

```csharp
void CMMItemDropRevealEndTimeUpdated()
```

### IsDroppingItemsUpdated

```csharp
void IsDroppingItemsUpdated()
```

### IsQuestEligibleUpdated

```csharp
void IsQuestEligibleUpdated()
```

### IsHltvActiveUpdated

```csharp
void IsHltvActiveUpdated()
```

### BombPlantedUpdated

```csharp
void BombPlantedUpdated()
```

### ProhibitedItemIndicesUpdated

```csharp
void ProhibitedItemIndicesUpdated()
```

### TournamentActiveCasterAccountsUpdated

```csharp
void TournamentActiveCasterAccountsUpdated()
```

### NumBestOfMapsUpdated

```csharp
void NumBestOfMapsUpdated()
```

### HalloweenMaskListSeedUpdated

```csharp
void HalloweenMaskListSeedUpdated()
```

### BombDroppedUpdated

```csharp
void BombDroppedUpdated()
```

### RoundWinStatusUpdated

```csharp
void RoundWinStatusUpdated()
```

### RoundWinReasonUpdated

```csharp
void RoundWinReasonUpdated()
```

### TCantBuyUpdated

```csharp
void TCantBuyUpdated()
```

### CTCantBuyUpdated

```csharp
void CTCantBuyUpdated()
```

### MatchStats_RoundResultsUpdated

```csharp
void MatchStats_RoundResultsUpdated()
```

### MatchStats_PlayersAlive_CTUpdated

```csharp
void MatchStats_PlayersAlive_CTUpdated()
```

### MatchStats_PlayersAlive_TUpdated

```csharp
void MatchStats_PlayersAlive_TUpdated()
```

### TeamRespawnWaveTimesUpdated

```csharp
void TeamRespawnWaveTimesUpdated()
```

### NextRespawnWaveUpdated

```csharp
void NextRespawnWaveUpdated()
```

### MinimapMinsUpdated

```csharp
void MinimapMinsUpdated()
```

### MinimapMaxsUpdated

```csharp
void MinimapMaxsUpdated()
```

### MinimapVerticalSectionHeightsUpdated

```csharp
void MinimapVerticalSectionHeightsUpdated()
```

### EndMatchMapGroupVoteTypesUpdated

```csharp
void EndMatchMapGroupVoteTypesUpdated()
```

### EndMatchMapGroupVoteOptionsUpdated

```csharp
void EndMatchMapGroupVoteOptionsUpdated()
```

### EndMatchMapVoteWinnerUpdated

```csharp
void EndMatchMapVoteWinnerUpdated()
```

### NumConsecutiveCTLosesUpdated

```csharp
void NumConsecutiveCTLosesUpdated()
```

### NumConsecutiveTerroristLosesUpdated

```csharp
void NumConsecutiveTerroristLosesUpdated()
```

### MatchAbortedEarlyReasonUpdated

```csharp
void MatchAbortedEarlyReasonUpdated()
```

### GameModeRulesUpdated

```csharp
void GameModeRulesUpdated()
```

### RetakeRulesUpdated

```csharp
void RetakeRulesUpdated()
```

### MatchEndCountUpdated

```csharp
void MatchEndCountUpdated()
```

### TTeamIntroVariantUpdated

```csharp
void TTeamIntroVariantUpdated()
```

### CTTeamIntroVariantUpdated

```csharp
void CTTeamIntroVariantUpdated()
```

### TeamIntroPeriodUpdated

```csharp
void TeamIntroPeriodUpdated()
```

### RoundEndWinnerTeamUpdated

```csharp
void RoundEndWinnerTeamUpdated()
```

### RoundEndReasonUpdated

```csharp
void RoundEndReasonUpdated()
```

### RoundEndShowTimerDefendUpdated

```csharp
void RoundEndShowTimerDefendUpdated()
```

### RoundEndTimerTimeUpdated

```csharp
void RoundEndTimerTimeUpdated()
```

### RoundEndFunFactTokenUpdated

```csharp
void RoundEndFunFactTokenUpdated()
```

### RoundEndFunFactPlayerSlotUpdated

```csharp
void RoundEndFunFactPlayerSlotUpdated()
```

### RoundEndFunFactData1Updated

```csharp
void RoundEndFunFactData1Updated()
```

### RoundEndFunFactData2Updated

```csharp
void RoundEndFunFactData2Updated()
```

### RoundEndFunFactData3Updated

```csharp
void RoundEndFunFactData3Updated()
```

### RoundEndMessageUpdated

```csharp
void RoundEndMessageUpdated()
```

### RoundEndPlayerCountUpdated

```csharp
void RoundEndPlayerCountUpdated()
```

### RoundEndNoMusicUpdated

```csharp
void RoundEndNoMusicUpdated()
```

### RoundEndLegacyUpdated

```csharp
void RoundEndLegacyUpdated()
```

### RoundEndCountUpdated

```csharp
void RoundEndCountUpdated()
```

### RoundStartRoundNumberUpdated

```csharp
void RoundStartRoundNumberUpdated()
```

### RoundStartCountUpdated

```csharp
void RoundStartCountUpdated()
```

