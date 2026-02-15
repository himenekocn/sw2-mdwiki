# 🔌 CFuncMover

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseModelEntity`

**实现接口:** `ISchemaClass\<CFuncMover\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PathName` | `string` | get, set | - |
| `PathMover` | `ref CHandle\<CPathMover\>` | get | - |
| `PrevPathMover` | `ref CHandle\<CPathMover\>` | get | - |
| `PathNodeStart` | `string` | get, set | - |
| `PathNodeEnd` | `string` | get, set | - |
| `MoveType` | `ref CFuncMover__Move_t` | get | - |
| `IsReversing` | `ref bool` | get | - |
| `StartSpeed` | `ref float` | get | - |
| `PathLocation` | `ref float` | get | - |
| `T` | `ref float` | get | - |
| `CurrentNodeIndex` | `ref int` | get | - |
| `PreviousNodeIndex` | `ref int` | get | - |
| `SolidType` | `ref SolidType_t` | get | - |
| `IsMoving` | `ref bool` | get | - |
| `TimeToReachMaxSpeed` | `ref float` | get | - |
| `DistanceToReachMaxSpeed` | `ref float` | get | - |
| `TimeToReachZeroSpeed` | `ref float` | get | - |
| `ComputedDistanceToReachMaxSpeed` | `ref float` | get | - |
| `ComputedDistanceToReachZeroSpeed` | `ref float` | get | - |
| `StartCurveScale` | `ref float` | get | - |
| `StopCurveScale` | `ref float` | get | - |
| `DistanceToReachZeroSpeed` | `ref float` | get | - |
| `TimeMovementStart` | `GameTime_t` | get | - |
| `TimeMovementStop` | `GameTime_t` | get | - |
| `StopAtNode` | `ref CHandle\<CMoverPathNode\>` | get | - |
| `PathLocationToBeginStop` | `ref float` | get | - |
| `PathLocationStart` | `ref float` | get | - |
| `BeginStopT` | `ref float` | get | - |
| `StartForwardSound` | `string` | get, set | - |
| `LoopForwardSound` | `string` | get, set | - |
| `StopForwardSound` | `string` | get, set | - |
| `StartReverseSound` | `string` | get, set | - |
| `LoopReverseSound` | `string` | get, set | - |
| `StopReverseSound` | `string` | get, set | - |
| `ArriveAtDestinationSound` | `string` | get, set | - |
| `OnMovementEnd` | `ref CEntityIOOutput` | get | - |
| `StartAtClosestPoint` | `ref bool` | get | - |
| `StartAtEnd` | `ref bool` | get | - |
| `StartFollowingClosestMover` | `ref bool` | get | - |
| `OrientationUpdate` | `ref CFuncMover__OrientationUpdate_t` | get | - |
| `TimeStartOrientationChange` | `GameTime_t` | get | - |
| `TimeToBlendToNewOrientation` | `ref float` | get | - |
| `DurationBlendToNewOrientationRan` | `ref float` | get | - |
| `OriginalOrientationIndex` | `ref int` | get | - |
| `CreateMovableNavMesh` | `ref bool` | get | - |
| `AllowMovableNavMeshDockingOnEntireEntity` | `ref bool` | get | - |
| `OnNodePassed` | `SchemaUntypedField` | get | - |
| `OrientationMatchEntityName` | `string` | get, set | - |
| `OrientationMatchEntity` | `ref CHandle\<CBaseEntity\>` | get | - |
| `TimeToTraverseToNextNode` | `ref float` | get | - |
| `LerpToNewPosStartInPathEntitySpace` | `ref Vector` | get | - |
| `LerpToNewPosEndInPathEntitySpace` | `ref Vector` | get | - |
| `LerpToPositionT` | `ref float` | get | - |
| `LerpToPositionDeltaT` | `ref float` | get | - |
| `OnLerpToPositionComplete` | `ref CEntityIOOutput` | get | - |
| `IsPaused` | `ref bool` | get | - |
| `TransitionedToPathNodeAction` | `ref CFuncMover__TransitionToPathNodeAction_t` | get | - |
| `DelayedTeleportToNode` | `ref int` | get | - |
| `IsVerboseLogging` | `ref bool` | get | - |
| `FollowEntity` | `ref CHandle\<CBaseEntity\>` | get | - |
| `FollowDistance` | `ref float` | get | - |
| `FollowMinimumSpeed` | `ref float` | get | - |
| `CurFollowEntityT` | `ref float` | get | - |
| `CurFollowSpeed` | `ref float` | get | - |
| `StrOrientationFaceEntityName` | `string` | get, set | - |
| `OrientationFaceEntity` | `ref CHandle\<CBaseEntity\>` | get | - |
| `OnStart` | `ref CEntityIOOutput` | get | - |
| `OnStartForward` | `ref CEntityIOOutput` | get | - |
| `OnStartReverse` | `ref CEntityIOOutput` | get | - |
| `OnStop` | `ref CEntityIOOutput` | get | - |
| `OnStopped` | `ref CEntityIOOutput` | get | - |
| `NextNodeReturnsCurrent` | `ref bool` | get | - |
| `StartedMoving` | `ref bool` | get | - |
| `FollowEntityDirection` | `ref CFuncMover__FollowEntityDirection_t` | get | - |
| `FollowMover` | `ref CHandle\<CFuncMover\>` | get | - |
| `FollowMoverEntityName` | `string` | get, set | - |
| `FollowMoverDistance` | `ref float` | get | - |
| `FollowMoverCalculatedDistance` | `ref float` | get | - |
| `FollowMoverSpringStrength` | `ref float` | get | - |
| `FollowConstraintsInitialized` | `ref bool` | get | - |
| `FollowConstraint` | `ref CFuncMover__FollowConstraint_t` | get | - |
| `FollowMoverSpeed` | `ref float` | get | - |
| `FollowMoverVelocity` | `ref float` | get | - |
| `TickMovementRan` | `GameTick_t` | get | - |

