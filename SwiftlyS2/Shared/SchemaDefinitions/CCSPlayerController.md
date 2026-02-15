# 🔌 CCSPlayerController

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBasePlayerController`

**实现接口:** `ISchemaClass\<CCSPlayerController\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `InGameMoneyServices` | `CCSPlayerController_InGameMoneyServices?` | get | - |
| `InventoryServices` | `CCSPlayerController_InventoryServices?` | get | - |
| `ActionTrackingServices` | `CCSPlayerController_ActionTrackingServices?` | get | - |
| `DamageServices` | `CCSPlayerController_DamageServices?` | get | - |
| `Ping` | `ref uint` | get | - |
| `HasCommunicationAbuseMute` | `ref bool` | get | - |
| `UiCommunicationMuteFlags` | `ref uint` | get | - |
| `CrosshairCodes` | `string` | get, set | - |
| `PendingTeamNum` | `ref byte` | get | - |
| `ForceTeamTime` | `GameTime_t` | get | - |
| `CompTeammateColor` | `ref int` | get | - |
| `EverPlayedOnTeam` | `ref bool` | get | - |
| `AttemptedToGetColor` | `ref bool` | get | - |
| `TeammatePreferredColor` | `ref int` | get | - |
| `TeamChanged` | `ref bool` | get | - |
| `InSwitchTeam` | `ref bool` | get | - |
| `HasSeenJoinGame` | `ref bool` | get | - |
| `JustBecameSpectator` | `ref bool` | get | - |
| `SwitchTeamsOnNextRoundReset` | `ref bool` | get, set | - |
| `RemoveAllItemsOnNextRoundReset` | `ref bool` | get, set | - |
| `LastJoinTeamTime` | `GameTime_t` | get | - |
| `Clan` | `string` | get, set | - |
| `CoachingTeam` | `ref int` | get | - |
| `PlayerDominated` | `ref ulong` | get | - |
| `PlayerDominatingMe` | `ref ulong` | get | - |
| `CompetitiveRanking` | `ref int` | get | - |
| `CompetitiveWins` | `ref int` | get | - |
| `CompetitiveRankType` | `ref byte` | get | - |
| `CompetitiveRankingPredicted_Win` | `ref int` | get | - |
| `CompetitiveRankingPredicted_Loss` | `ref int` | get | - |
| `CompetitiveRankingPredicted_Tie` | `ref int` | get | - |
| `EndMatchNextMapVote` | `ref int` | get | - |
| `ActiveQuestId` | `ref ushort` | get | - |
| `RtActiveMissionPeriod` | `ref uint` | get | - |
| `QuestProgressReason` | `ref QuestProgress__Reason` | get | - |
| `PlayerTvControlFlags` | `ref uint` | get | - |
| `DraftIndex` | `ref int` | get | - |
| `MsQueuedModeDisconnectionTimestamp` | `ref uint` | get | - |
| `UiAbandonRecordedReason` | `ref uint` | get | - |
| `NetworkDisconnectionReason` | `ref uint` | get | - |
| `CannotBeKicked` | `ref bool` | get | - |
| `EverFullyConnected` | `ref bool` | get | - |
| `AbandonAllowsSurrender` | `ref bool` | get | - |
| `AbandonOffersInstantSurrender` | `ref bool` | get | - |
| `Disconnection1MinWarningPrinted` | `ref bool` | get | - |
| `ScoreReported` | `ref bool` | get | - |
| `DisconnectionTick` | `ref int` | get | - |
| `ControllingBot` | `ref bool` | get | - |
| `HasControlledBotThisRound` | `ref bool` | get | - |
| `HasBeenControlledByPlayerThisRound` | `ref bool` | get | - |
| `BotsControlledThisRound` | `ref int` | get | - |
| `CanControlObservedBot` | `ref bool` | get | - |
| `PlayerPawn` | `ref CHandle\<CCSPlayerPawn\>` | get | - |
| `ObserverPawn` | `ref CHandle\<CCSObserverPawn\>` | get | - |
| `DesiredObserverMode` | `ref int` | get | - |
| `DesiredObserverTarget` | `ref CHandle\<CEntityInstance\>` | get | - |
| `PawnIsAlive` | `ref bool` | get | - |
| `PawnHealth` | `ref uint` | get | - |
| `PawnArmor` | `ref int` | get | - |
| `PawnHasDefuser` | `ref bool` | get | - |
| `PawnHasHelmet` | `ref bool` | get | - |
| `PawnCharacterDefIndex` | `ref ushort` | get | - |
| `PawnLifetimeStart` | `ref int` | get | - |
| `PawnLifetimeEnd` | `ref int` | get | - |
| `PawnBotDifficulty` | `ref int` | get | - |
| `OriginalControllerOfCurrentPawn` | `ref CHandle\<CCSPlayerController\>` | get | - |
| `Score` | `ref int` | get | - |
| `RoundScore` | `ref int` | get | - |
| `RoundsWon` | `ref int` | get | - |
| `RecentKillQueue` | `ISchemaFixedArray\<byte\>` | get | - |
| `FirstKill` | `ref byte` | get | - |
| `KillCount` | `ref byte` | get | - |
| `MvpNoMusic` | `ref bool` | get | - |
| `MvpReason` | `ref int` | get | - |
| `MusicKitID` | `ref int` | get | - |
| `MusicKitMVPs` | `ref int` | get | - |
| `MVPs` | `ref int` | get | - |
| `UpdateCounter` | `ref int` | get | - |
| `SmoothedPing` | `ref float` | get | - |
| `LastHeldVoteTimer` | `IntervalTimer` | get | - |
| `ShowHints` | `ref bool` | get | - |
| `NextTimeCheck` | `ref int` | get | - |
| `JustDidTeamKill` | `ref bool` | get | - |
| `PunishForTeamKill` | `ref bool` | get | - |
| `GaveTeamDamageWarning` | `ref bool` | get | - |
| `GaveTeamDamageWarningThisRound` | `ref bool` | get | - |
| `DblLastReceivedPacketPlatFloatTime` | `ref double` | get | - |
| `LastTeamDamageWarningTime` | `GameTime_t` | get | - |
| `LastTimePlayerWasDisconnectedForPawnsRemove` | `GameTime_t` | get | - |
| `SuspiciousHitCount` | `ref uint` | get | - |
| `NonSuspiciousHitStreak` | `ref uint` | get | - |
| `FireBulletsSeedSynchronized` | `ref bool` | get | - |

## ⚙️ 方法

### InGameMoneyServicesUpdated

```csharp
void InGameMoneyServicesUpdated()
```

### InventoryServicesUpdated

```csharp
void InventoryServicesUpdated()
```

### ActionTrackingServicesUpdated

```csharp
void ActionTrackingServicesUpdated()
```

### DamageServicesUpdated

```csharp
void DamageServicesUpdated()
```

### PingUpdated

```csharp
void PingUpdated()
```

### HasCommunicationAbuseMuteUpdated

```csharp
void HasCommunicationAbuseMuteUpdated()
```

### UiCommunicationMuteFlagsUpdated

```csharp
void UiCommunicationMuteFlagsUpdated()
```

### CrosshairCodesUpdated

```csharp
void CrosshairCodesUpdated()
```

### PendingTeamNumUpdated

```csharp
void PendingTeamNumUpdated()
```

### ForceTeamTimeUpdated

```csharp
void ForceTeamTimeUpdated()
```

### CompTeammateColorUpdated

```csharp
void CompTeammateColorUpdated()
```

### EverPlayedOnTeamUpdated

```csharp
void EverPlayedOnTeamUpdated()
```

### ClanUpdated

```csharp
void ClanUpdated()
```

### CoachingTeamUpdated

```csharp
void CoachingTeamUpdated()
```

### PlayerDominatedUpdated

```csharp
void PlayerDominatedUpdated()
```

### PlayerDominatingMeUpdated

```csharp
void PlayerDominatingMeUpdated()
```

### CompetitiveRankingUpdated

```csharp
void CompetitiveRankingUpdated()
```

### CompetitiveWinsUpdated

```csharp
void CompetitiveWinsUpdated()
```

### CompetitiveRankTypeUpdated

```csharp
void CompetitiveRankTypeUpdated()
```

### CompetitiveRankingPredicted_WinUpdated

```csharp
void CompetitiveRankingPredicted_WinUpdated()
```

### CompetitiveRankingPredicted_LossUpdated

```csharp
void CompetitiveRankingPredicted_LossUpdated()
```

### CompetitiveRankingPredicted_TieUpdated

```csharp
void CompetitiveRankingPredicted_TieUpdated()
```

### EndMatchNextMapVoteUpdated

```csharp
void EndMatchNextMapVoteUpdated()
```

### ActiveQuestIdUpdated

```csharp
void ActiveQuestIdUpdated()
```

### RtActiveMissionPeriodUpdated

```csharp
void RtActiveMissionPeriodUpdated()
```

### QuestProgressReasonUpdated

```csharp
void QuestProgressReasonUpdated()
```

### PlayerTvControlFlagsUpdated

```csharp
void PlayerTvControlFlagsUpdated()
```

### DisconnectionTickUpdated

```csharp
void DisconnectionTickUpdated()
```

### ControllingBotUpdated

```csharp
void ControllingBotUpdated()
```

### HasControlledBotThisRoundUpdated

```csharp
void HasControlledBotThisRoundUpdated()
```

### CanControlObservedBotUpdated

```csharp
void CanControlObservedBotUpdated()
```

### PlayerPawnUpdated

```csharp
void PlayerPawnUpdated()
```

### ObserverPawnUpdated

```csharp
void ObserverPawnUpdated()
```

### PawnIsAliveUpdated

```csharp
void PawnIsAliveUpdated()
```

### PawnHealthUpdated

```csharp
void PawnHealthUpdated()
```

### PawnArmorUpdated

```csharp
void PawnArmorUpdated()
```

### PawnHasDefuserUpdated

```csharp
void PawnHasDefuserUpdated()
```

### PawnHasHelmetUpdated

```csharp
void PawnHasHelmetUpdated()
```

### PawnCharacterDefIndexUpdated

```csharp
void PawnCharacterDefIndexUpdated()
```

### PawnLifetimeStartUpdated

```csharp
void PawnLifetimeStartUpdated()
```

### PawnLifetimeEndUpdated

```csharp
void PawnLifetimeEndUpdated()
```

### PawnBotDifficultyUpdated

```csharp
void PawnBotDifficultyUpdated()
```

### OriginalControllerOfCurrentPawnUpdated

```csharp
void OriginalControllerOfCurrentPawnUpdated()
```

### ScoreUpdated

```csharp
void ScoreUpdated()
```

### RecentKillQueueUpdated

```csharp
void RecentKillQueueUpdated()
```

### FirstKillUpdated

```csharp
void FirstKillUpdated()
```

### KillCountUpdated

```csharp
void KillCountUpdated()
```

### MvpNoMusicUpdated

```csharp
void MvpNoMusicUpdated()
```

### MvpReasonUpdated

```csharp
void MvpReasonUpdated()
```

### MusicKitIDUpdated

```csharp
void MusicKitIDUpdated()
```

### MusicKitMVPsUpdated

```csharp
void MusicKitMVPsUpdated()
```

### MVPsUpdated

```csharp
void MVPsUpdated()
```

### FireBulletsSeedSynchronizedUpdated

```csharp
void FireBulletsSeedSynchronizedUpdated()
```

