# 🔌 CShatterGlassShard

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `ISchemaClass\<CShatterGlassShard\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ShardHandle` | `ref uint` | get | - |
| `PanelVertices` | `ref CUtlVector\<Vector2D\>` | get | - |
| `LocalPanelSpaceOrigin` | `ref Vector2D` | get | - |
| `Model` | `ref CStrongHandle\<InfoForResourceTypeCModel\>` | get | - |
| `PhysicsEntity` | `ref CHandle\<CShatterGlassShardPhysics\>` | get | - |
| `ParentPanel` | `ref CHandle\<CFuncShatterglass\>` | get | - |
| `ParentShard` | `ref uint` | get | - |
| `ShatterStressType` | `ref ShatterGlassStressType` | get | - |
| `StressVelocity` | `ref Vector` | get | - |
| `CreatedModel` | `ref bool` | get | - |
| `LongestEdge` | `ref float` | get | - |
| `ShortestEdge` | `ref float` | get | - |
| `LongestAcross` | `ref float` | get | - |
| `ShortestAcross` | `ref float` | get | - |
| `SumOfAllEdges` | `ref float` | get | - |
| `Area` | `ref float` | get | - |
| `OnFrameEdge` | `ref OnFrame` | get | - |
| `SubShardGeneration` | `ref int` | get | - |
| `AverageVertPosition` | `ref Vector2D` | get | - |
| `AverageVertPositionIsValid` | `ref bool` | get | - |
| `PanelSpaceStressPositionA` | `ref Vector2D` | get | - |
| `PanelSpaceStressPositionB` | `ref Vector2D` | get | - |
| `StressPositionAIsValid` | `ref bool` | get | - |
| `StressPositionBIsValid` | `ref bool` | get | - |
| `FlaggedForRemoval` | `ref bool` | get | - |
| `PhysicsEntitySpawnedAtTime` | `GameTime_t` | get | - |
| `EntityHittingMe` | `ref CHandle\<CBaseEntity\>` | get | - |
| `Neighbors` | `ref CUtlVector\<uint\>` | get | - |

