# 🔌 CCSBot

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBot`

**实现接口:** `ISchemaClass\<CCSBot\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EyePosition` | `ref Vector` | get | - |
| `Name` | `string` | get, set | - |
| `CombatRange` | `ref float` | get | - |
| `IsRogue` | `ref bool` | get | - |
| `RogueTimer` | `CountdownTimer` | get | - |
| `DiedLastRound` | `ref bool` | get | - |
| `SafeTime` | `ref float` | get | - |
| `WasSafe` | `ref bool` | get | - |
| `BlindFire` | `ref bool` | get | - |
| `SurpriseTimer` | `CountdownTimer` | get | - |
| `AllowActive` | `ref bool` | get | - |
| `IsFollowing` | `ref bool` | get | - |
| `Leader` | `ref CHandle\<CCSPlayerPawn\>` | get | - |
| `FollowTimestamp` | `ref float` | get | - |
| `AllowAutoFollowTime` | `ref float` | get | - |
| `HurryTimer` | `CountdownTimer` | get | - |
| `AlertTimer` | `CountdownTimer` | get | - |
| `SneakTimer` | `CountdownTimer` | get | - |
| `PanicTimer` | `CountdownTimer` | get | - |
| `StateTimestamp` | `ref float` | get | - |
| `IsAttacking` | `ref bool` | get | - |
| `IsOpeningDoor` | `ref bool` | get | - |
| `TaskEntity` | `ref CHandle\<CBaseEntity\>` | get | - |
| `GoalPosition` | `ref Vector` | get | - |
| `GoalEntity` | `ref CHandle\<CBaseEntity\>` | get | - |
| `Avoid` | `ref CHandle\<CBaseEntity\>` | get | - |
| `AvoidTimestamp` | `ref float` | get | - |
| `IsStopping` | `ref bool` | get | - |
| `HasVisitedEnemySpawn` | `ref bool` | get | - |
| `StillTimer` | `IntervalTimer` | get | - |
| `EyeAnglesUnderPathFinderControl` | `ref bool` | get | - |
| `PathIndex` | `ref int` | get | - |
| `AreaEnteredTimestamp` | `GameTime_t` | get | - |
| `RepathTimer` | `CountdownTimer` | get | - |
| `AvoidFriendTimer` | `CountdownTimer` | get | - |
| `IsFriendInTheWay` | `ref bool` | get | - |
| `PoliteTimer` | `CountdownTimer` | get | - |
| `IsWaitingBehindFriend` | `ref bool` | get | - |
| `PathLadderEnd` | `ref float` | get | - |
| `MustRunTimer` | `CountdownTimer` | get | - |
| `WaitTimer` | `CountdownTimer` | get | - |
| `UpdateTravelDistanceTimer` | `CountdownTimer` | get | - |
| `PlayerTravelDistance` | `ISchemaFixedArray\<float\>` | get | - |
| `TravelDistancePhase` | `ref byte` | get | - |
| `HostageEscortCount` | `ref byte` | get | - |
| `HostageEscortCountTimestamp` | `ref float` | get | - |
| `DesiredTeam` | `ref int` | get | - |
| `HasJoined` | `ref bool` | get | - |
| `IsWaitingForHostage` | `ref bool` | get | - |
| `InhibitWaitingForHostageTimer` | `CountdownTimer` | get | - |
| `WaitForHostageTimer` | `CountdownTimer` | get | - |
| `NoisePosition` | `ref Vector` | get | - |
| `NoiseTravelDistance` | `ref float` | get | - |
| `NoiseTimestamp` | `ref float` | get | - |
| `NoiseSource` | `CCSPlayerPawn?` | get | - |
| `NoiseBendTimer` | `CountdownTimer` | get | - |
| `BentNoisePosition` | `ref Vector` | get | - |
| `BendNoisePositionValid` | `ref bool` | get | - |
| `LookAroundStateTimestamp` | `ref float` | get | - |
| `LookAheadAngle` | `ref float` | get | - |
| `ForwardAngle` | `ref float` | get | - |
| `InhibitLookAroundTimestamp` | `ref float` | get | - |
| `LookAtSpot` | `ref Vector` | get | - |
| `LookAtSpotDuration` | `ref float` | get | - |
| `LookAtSpotTimestamp` | `ref float` | get | - |
| `LookAtSpotAngleTolerance` | `ref float` | get | - |
| `LookAtSpotClearIfClose` | `ref bool` | get | - |
| `LookAtSpotAttack` | `ref bool` | get | - |
| `LookAtDesc` | `string` | get, set | - |
| `PeripheralTimestamp` | `ref float` | get | - |
| `ApproachPointCount` | `ref byte` | get | - |
| `ApproachPointViewPosition` | `ref Vector` | get | - |
| `ViewSteadyTimer` | `IntervalTimer` | get | - |
| `TossGrenadeTimer` | `CountdownTimer` | get | - |
| `IsAvoidingGrenade` | `CountdownTimer` | get | - |
| `SpotCheckTimestamp` | `ref float` | get | - |
| `CheckedHidingSpotCount` | `ref int` | get | - |
| `LookPitch` | `ref float` | get | - |
| `LookPitchVel` | `ref float` | get | - |
| `LookYaw` | `ref float` | get | - |
| `LookYawVel` | `ref float` | get | - |
| `TargetSpot` | `ref Vector` | get | - |
| `TargetSpotVelocity` | `ref Vector` | get | - |
| `TargetSpotPredicted` | `ref Vector` | get | - |
| `AimError` | `ref QAngle` | get | - |
| `AimGoal` | `ref QAngle` | get | - |
| `TargetSpotTime` | `GameTime_t` | get | - |
| `AimFocus` | `ref float` | get | - |
| `AimFocusInterval` | `ref float` | get | - |
| `AimFocusNextUpdate` | `GameTime_t` | get | - |
| `IgnoreEnemiesTimer` | `CountdownTimer` | get | - |
| `Enemy` | `ref CHandle\<CCSPlayerPawn\>` | get | - |
| `IsEnemyVisible` | `ref bool` | get | - |
| `VisibleEnemyParts` | `ref byte` | get | - |
| `LastEnemyPosition` | `ref Vector` | get | - |
| `LastSawEnemyTimestamp` | `ref float` | get | - |
| `FirstSawEnemyTimestamp` | `ref float` | get | - |
| `CurrentEnemyAcquireTimestamp` | `ref float` | get | - |
| `EnemyDeathTimestamp` | `ref float` | get | - |
| `FriendDeathTimestamp` | `ref float` | get | - |
| `IsLastEnemyDead` | `ref bool` | get | - |
| `NearbyEnemyCount` | `ref int` | get | - |
| `Bomber` | `ref CHandle\<CCSPlayerPawn\>` | get | - |
| `NearbyFriendCount` | `ref int` | get | - |
| `ClosestVisibleFriend` | `ref CHandle\<CCSPlayerPawn\>` | get | - |
| `ClosestVisibleHumanFriend` | `ref CHandle\<CCSPlayerPawn\>` | get | - |
| `AttentionInterval` | `IntervalTimer` | get | - |
| `Attacker` | `ref CHandle\<CCSPlayerPawn\>` | get | - |
| `AttackedTimestamp` | `ref float` | get | - |
| `BurnedByFlamesTimer` | `IntervalTimer` | get | - |
| `LastVictimID` | `ref int` | get | - |
| `IsAimingAtEnemy` | `ref bool` | get | - |
| `IsRapidFiring` | `ref bool` | get | - |
| `EquipTimer` | `IntervalTimer` | get | - |
| `ZoomTimer` | `CountdownTimer` | get | - |
| `FireWeaponTimestamp` | `GameTime_t` | get | - |
| `LookForWeaponsOnGroundTimer` | `CountdownTimer` | get | - |
| `IsSleeping` | `ref bool` | get | - |
| `IsEnemySniperVisible` | `ref bool` | get | - |
| `SawEnemySniperTimer` | `CountdownTimer` | get | - |
| `EnemyQueueIndex` | `ref byte` | get | - |
| `EnemyQueueCount` | `ref byte` | get | - |
| `EnemyQueueAttendIndex` | `ref byte` | get | - |
| `IsStuck` | `ref bool` | get | - |
| `StuckTimestamp` | `GameTime_t` | get | - |
| `StuckSpot` | `ref Vector` | get | - |
| `WiggleTimer` | `CountdownTimer` | get | - |
| `StuckJumpTimer` | `CountdownTimer` | get | - |
| `NextCleanupCheckTimestamp` | `GameTime_t` | get | - |
| `AvgVel` | `ISchemaFixedArray\<float\>` | get | - |
| `AvgVelIndex` | `ref int` | get | - |
| `AvgVelCount` | `ref int` | get | - |
| `LastOrigin` | `ref Vector` | get | - |
| `LastRadioRecievedTimestamp` | `ref float` | get | - |
| `LastRadioSentTimestamp` | `ref float` | get | - |
| `RadioSubject` | `ref CHandle\<CCSPlayerPawn\>` | get | - |
| `RadioPosition` | `ref Vector` | get | - |
| `VoiceEndTimestamp` | `ref float` | get | - |
| `LastValidReactionQueueFrame` | `ref int` | get | - |

