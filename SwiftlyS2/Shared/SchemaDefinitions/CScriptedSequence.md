# 🔌 CScriptedSequence

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseEntity`

**实现接口:** `ISchemaClass\<CScriptedSequence\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Entry` | `string` | get, set | - |
| `PreIdle` | `string` | get, set | - |
| `Play` | `string` | get, set | - |
| `PostIdle` | `string` | get, set | - |
| `ModifierToAddOnPlay` | `string` | get, set | - |
| `NextScript` | `string` | get, set | - |
| `Entity` | `string` | get, set | - |
| `SyncGroup` | `string` | get, set | - |
| `MoveTo` | `ref ScriptedMoveTo_t` | get | - |
| `MoveToGait` | `ref SharedMovementGait_t` | get | - |
| `HeldWeaponBehavior` | `ref ScriptedHeldWeaponBehavior_t` | get | - |
| `ForcedCrouchState` | `ref ForcedCrouchState_t` | get | - |
| `IsPlayingPreIdle` | `ref bool` | get | - |
| `IsPlayingEntry` | `ref bool` | get | - |
| `IsPlayingAction` | `ref bool` | get | - |
| `IsPlayingPostIdle` | `ref bool` | get | - |
| `DontRotateOther` | `ref bool` | get | - |
| `IsRepeatable` | `ref bool` | get | - |
| `ShouldLeaveCorpse` | `ref bool` | get | - |
| `StartOnSpawn` | `ref bool` | get | - |
| `DisallowInterrupts` | `ref bool` | get | - |
| `CanOverrideNPCState` | `ref bool` | get | - |
| `DontTeleportAtEnd` | `ref bool` | get | - |
| `HighPriority` | `ref bool` | get | - |
| `HideDebugComplaints` | `ref bool` | get | - |
| `ContinueOnDeath` | `ref bool` | get | - |
| `LoopPreIdleSequence` | `ref bool` | get | - |
| `LoopActionSequence` | `ref bool` | get | - |
| `LoopPostIdleSequence` | `ref bool` | get | - |
| `SynchPostIdles` | `ref bool` | get | - |
| `IgnoreLookAt` | `ref bool` | get | - |
| `IgnoreGravity` | `ref bool` | get | - |
| `DisableNPCCollisions` | `ref bool` | get | - |
| `KeepAnimgraphLockedPost` | `ref bool` | get | - |
| `DontAddModifiers` | `ref bool` | get | - |
| `DisableAimingWhileMoving` | `ref bool` | get | - |
| `IgnoreRotation` | `ref bool` | get | - |
| `Radius` | `ref float` | get | - |
| `Repeat` | `ref float` | get | - |
| `PlayAnimFadeInTime` | `ref float` | get | - |
| `MoveInterpTime` | `ref float` | get | - |
| `AngRate` | `ref float` | get | - |
| `MoveSpeed` | `ref float` | get | - |
| `WaitUntilMoveCompletesToStartAnimation` | `ref bool` | get | - |
| `NotReadySequenceCount` | `ref int` | get | - |
| `StartTime` | `GameTime_t` | get | - |
| `WaitForBeginSequence` | `ref bool` | get | - |
| `Saved_effects` | `ref int` | get | - |
| `SavedFlags` | `ref int` | get | - |
| `SavedCollisionGroup` | `ref int` | get | - |
| `Interruptable` | `ref bool` | get | - |
| `SequenceStarted` | `ref bool` | get | - |
| `PositionRelativeToOtherEntity` | `ref bool` | get | - |
| `TargetEnt` | `ref CHandle\<CBaseEntity\>` | get | - |
| `NextCine` | `ref CHandle\<CScriptedSequence\>` | get | - |
| `Thinking` | `ref bool` | get | - |
| `InitiatedSelfDelete` | `ref bool` | get | - |
| `IsTeleportingDueToMoveTo` | `ref bool` | get | - |
| `AllowCustomInterruptConditions` | `ref bool` | get | - |
| `ForcedTarget` | `ref CHandle\<CBaseAnimGraph\>` | get | - |
| `DontCancelOtherSequences` | `ref bool` | get | - |
| `ForceSynch` | `ref bool` | get | - |
| `PreventUpdateYawOnFinish` | `ref bool` | get | - |
| `EnsureOnNavmeshOnFinish` | `ref bool` | get | - |
| `OnDeathBehavior` | `ref ScriptedOnDeath_t` | get | - |
| `ConflictResponse` | `ref ScriptedConflictResponse_t` | get | - |
| `OnBeginSequence` | `ref CEntityIOOutput` | get | - |
| `OnActionStartOrLoop` | `ref CEntityIOOutput` | get | - |
| `OnEndSequence` | `ref CEntityIOOutput` | get | - |
| `OnPostIdleEndSequence` | `ref CEntityIOOutput` | get | - |
| `OnCancelSequence` | `ref CEntityIOOutput` | get | - |
| `OnCancelFailedSequence` | `ref CEntityIOOutput` | get | - |
| `OnScriptEvent` | `ISchemaFixedArray\<CEntityIOOutput\>` | get | - |
| `MatOtherToMain` | `ref CTransform` | get | - |
| `InteractionMainEntity` | `ref CHandle\<CBaseEntity\>` | get | - |
| `PlayerDeathBehavior` | `ref int` | get | - |
| `SkipFadeIn` | `ref bool` | get | - |

