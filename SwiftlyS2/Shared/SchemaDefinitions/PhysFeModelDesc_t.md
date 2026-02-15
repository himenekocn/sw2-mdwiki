# 🔌 PhysFeModelDesc_t

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `ISchemaClass\<PhysFeModelDesc_t\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CtrlHash` | `ref CUtlVector\<uint\>` | get | - |
| `CtrlName` | `ref CUtlVector\<CUtlString\>` | get | - |
| `StaticNodeFlags` | `ref uint` | get | - |
| `DynamicNodeFlags` | `ref uint` | get | - |
| `LocalForce` | `ref float` | get | - |
| `LocalRotation` | `ref float` | get | - |
| `NodeCount` | `ref ushort` | get | - |
| `StaticNodes` | `ref ushort` | get | - |
| `RotLockStaticNodes` | `ref ushort` | get | - |
| `FirstPositionDrivenNode` | `ref ushort` | get | - |
| `SimdTriCount1` | `ref ushort` | get | - |
| `SimdTriCount2` | `ref ushort` | get | - |
| `SimdQuadCount1` | `ref ushort` | get | - |
| `SimdQuadCount2` | `ref ushort` | get | - |
| `QuadCount1` | `ref ushort` | get | - |
| `QuadCount2` | `ref ushort` | get | - |
| `TreeDepth` | `ref ushort` | get | - |
| `NodeBaseJiggleboneDependsCount` | `ref ushort` | get | - |
| `RopeCount` | `ref ushort` | get | - |
| `Ropes` | `ref CUtlVector\<ushort\>` | get | - |
| `NodeBases` | `ref CUtlVector\<FeNodeBase_t\>` | get | - |
| `SimdNodeBases` | `ref CUtlVector\<FeSimdNodeBase_t\>` | get | - |
| `Quads` | `ref CUtlVector\<FeQuad_t\>` | get | - |
| `SimdQuads` | `ref CUtlVector\<FeSimdQuad_t\>` | get | - |
| `SimdTris` | `ref CUtlVector\<SchemaUntypedField\>` | get | - |
| `SimdRods` | `ref CUtlVector\<FeSimdRodConstraint_t\>` | get | - |
| `SimdRodsAnim` | `ref CUtlVector\<FeSimdRodConstraintAnim_t\>` | get | - |
| `InitPose` | `ref CUtlVector\<CTransform\>` | get | - |
| `Rods` | `ref CUtlVector\<FeRodConstraint_t\>` | get | - |
| `Twists` | `ref CUtlVector\<FeTwistConstraint_t\>` | get | - |
| `HingeLimits` | `ref CUtlVector\<FeHingeLimit_t\>` | get | - |
| `AntiTunnelBytecode` | `ref CUtlVector\<uint\>` | get | - |
| `DynKinLinks` | `ref CUtlVector\<FeDynKinLink_t\>` | get | - |
| `AntiTunnelProbes` | `ref CUtlVector\<FeAntiTunnelProbe_t\>` | get | - |
| `AntiTunnelTargetNodes` | `ref CUtlVector\<ushort\>` | get | - |
| `NodeStrayBoxes` | `ref CUtlVector\<FeNodeStrayBox_t\>` | get | - |
| `AxialEdges` | `ref CUtlVector\<FeAxialEdgeBend_t\>` | get | - |
| `NodeInvMasses` | `ref CUtlVector\<float\>` | get | - |
| `CtrlOffsets` | `ref CUtlVector\<FeCtrlOffset_t\>` | get, set | - |
| `CtrlOsOffsets` | `ref CUtlVector\<FeCtrlOsOffset_t\>` | get, set | - |
| `FollowNodes` | `ref CUtlVector\<FeFollowNode_t\>` | get | - |
| `CollisionPlanes` | `ref CUtlVector\<FeCollisionPlane_t\>` | get | - |
| `NodeIntegrator` | `ref CUtlVector\<FeNodeIntegrator_t\>` | get | - |
| `SpringIntegrator` | `ref CUtlVector\<FeSpringIntegrator_t\>` | get | - |
| `SimdSpringIntegrator` | `ref CUtlVector\<FeSimdSpringIntegrator_t\>` | get | - |
| `WorldCollisionParams` | `ref CUtlVector\<FeWorldCollisionParams_t\>` | get | - |
| `LegacyStretchForce` | `ref CUtlVector\<float\>` | get | - |
| `NodeCollisionRadii` | `ref CUtlVector\<float\>` | get | - |
| `DynNodeFriction` | `ref CUtlVector\<float\>` | get | - |
| `LocalRotation1` | `ref CUtlVector\<float\>` | get | - |
| `LocalForce2` | `ref CUtlVector\<float\>` | get | - |
| `TaperedCapsuleStretches` | `ref CUtlVector\<FeTaperedCapsuleStretch_t\>` | get | - |
| `TaperedCapsuleRigids` | `ref CUtlVector\<FeTaperedCapsuleRigid_t\>` | get | - |
| `SphereRigids` | `ref CUtlVector\<FeSphereRigid_t\>` | get | - |
| `WorldCollisionNodes` | `ref CUtlVector\<ushort\>` | get | - |
| `TreeParents` | `ref CUtlVector\<ushort\>` | get | - |
| `TreeCollisionMasks` | `ref CUtlVector\<ushort\>` | get | - |
| `TreeChildren` | `ref CUtlVector\<FeTreeChildren_t\>` | get | - |
| `FreeNodes` | `ref CUtlVector\<ushort\>` | get | - |
| `FitMatrices` | `ref CUtlVector\<FeFitMatrix_t\>` | get | - |
| `FitWeights` | `ref CUtlVector\<FeFitWeight_t\>` | get | - |
| `ReverseOffsets` | `ref CUtlVector\<FeNodeReverseOffset_t\>` | get, set | - |
| `AnimStrayRadii` | `ref CUtlVector\<FeAnimStrayRadius_t\>` | get | - |
| `SimdAnimStrayRadii` | `ref CUtlVector\<FeSimdAnimStrayRadius_t\>` | get | - |
| `KelagerBends` | `ref CUtlVector\<FeKelagerBend2_t\>` | get | - |
| `CtrlSoftOffsets` | `ref CUtlVector\<FeCtrlSoftOffset_t\>` | get, set | - |
| `JiggleBones` | `ref CUtlVector\<CFeIndexedJiggleBone\>` | get | - |
| `SourceElems` | `ref CUtlVector\<ushort\>` | get | - |
| `GoalDampedSpringIntegrators` | `ref CUtlVector\<uint\>` | get | - |
| `Tris` | `ref CUtlVector\<FeTri_t\>` | get | - |
| `TriCount1` | `ref ushort` | get | - |
| `TriCount2` | `ref ushort` | get | - |
| `ReservedUint8` | `ref byte` | get | - |
| `ExtraPressureIterations` | `ref byte` | get | - |
| `ExtraGoalIterations` | `ref byte` | get | - |
| `ExtraIterations` | `ref byte` | get | - |
| `SDFRigids` | `ref CUtlVector\<FeSDFRigid_t\>` | get | - |
| `BoxRigids` | `ref CUtlVector\<FeBoxRigid_t\>` | get | - |
| `DynNodeVertexSet` | `ref CUtlVector\<byte\>` | get | - |
| `VertexSetNames` | `ref CUtlVector\<uint\>` | get | - |
| `RigidColliderPriorities` | `ref CUtlVector\<FeRigidColliderIndices_t\>` | get | - |
| `MorphLayers` | `ref CUtlVector\<FeMorphLayerDepr_t\>` | get | - |
| `MorphSetData` | `ref CUtlVector\<byte\>` | get | - |
| `VertexMaps` | `ref CUtlVector\<FeVertexMapDesc_t\>` | get | - |
| `VertexMapValues` | `ref CUtlVector\<byte\>` | get | - |
| `Effects` | `ref CUtlVector\<FeEffectDesc_t\>` | get | - |
| `LockToParent` | `ref CUtlVector\<FeCtrlOffset_t\>` | get, set | - |
| `LockToGoal` | `ref CUtlVector\<ushort\>` | get | - |
| `SkelParents` | `ref CUtlVector\<short\>` | get | - |
| `DynNodeWindBases` | `ref CUtlVector\<FeNodeWindBase_t\>` | get | - |
| `SelfCollisionLayers` | `ref CUtlVector\<FeModelSelfCollisionLayer_t\>` | get | - |
| `InternalPressure` | `ref float` | get | - |
| `DefaultTimeDilation` | `ref float` | get | - |
| `Windage` | `ref float` | get | - |
| `WindDrag` | `ref float` | get | - |
| `DefaultSurfaceStretch` | `ref float` | get | - |
| `DefaultThreadStretch` | `ref float` | get | - |
| `DefaultGravityScale` | `ref float` | get | - |
| `DefaultVelAirDrag` | `ref float` | get | - |
| `DefaultExpAirDrag` | `ref float` | get | - |
| `DefaultVelQuadAirDrag` | `ref float` | get | - |
| `DefaultExpQuadAirDrag` | `ref float` | get | - |
| `RodVelocitySmoothRate` | `ref float` | get | - |
| `QuadVelocitySmoothRate` | `ref float` | get | - |
| `AddWorldCollisionRadius` | `ref float` | get | - |
| `DefaultVolumetricSolveAmount` | `ref float` | get | - |
| `MotionSmoothCDT` | `ref float` | get | - |
| `LocalDrag1` | `ref float` | get | - |
| `RodVelocitySmoothIterations` | `ref ushort` | get | - |
| `QuadVelocitySmoothIterations` | `ref ushort` | get | - |

