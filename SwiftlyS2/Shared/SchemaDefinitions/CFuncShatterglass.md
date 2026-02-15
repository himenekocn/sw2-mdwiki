# 🔌 CFuncShatterglass

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseModelEntity`

**实现接口:** `ISchemaClass\<CFuncShatterglass\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MatPanelTransform` | `ref matrix3x4_t` | get | - |
| `MatPanelTransformWsTemp` | `ref matrix3x4_t` | get | - |
| `ShatterGlassShards` | `ref CUtlVector\<uint\>` | get | - |
| `PanelSize` | `ref Vector2D` | get | - |
| `LastShatterSoundEmitTime` | `GameTime_t` | get | - |
| `LastCleanupTime` | `GameTime_t` | get | - |
| `InitAtTime` | `GameTime_t` | get | - |
| `GlassThickness` | `ref float` | get | - |
| `SpawnInvulnerability` | `ref float` | get | - |
| `BreakSilent` | `ref bool` | get | - |
| `BreakShardless` | `ref bool` | get | - |
| `Broken` | `ref bool` | get | - |
| `GlassNavIgnore` | `ref bool` | get | - |
| `GlassInFrame` | `ref bool` | get | - |
| `StartBroken` | `ref bool` | get | - |
| `InitialDamageType` | `ref byte` | get | - |
| `DamagePositioningEntityName01` | `string` | get, set | - |
| `DamagePositioningEntityName02` | `string` | get, set | - |
| `DamagePositioningEntityName03` | `string` | get, set | - |
| `DamagePositioningEntityName04` | `string` | get, set | - |
| `InitialDamagePositions` | `ref CUtlVector\<Vector\>` | get | - |
| `ExtraDamagePositions` | `ref CUtlVector\<Vector\>` | get | - |
| `InitialPanelVertices` | `ref CUtlVector\<Vector4D\>` | get | - |
| `OnBroken` | `ref CEntityIOOutput` | get | - |
| `SurfaceType` | `ref byte` | get | - |
| `MaterialDamageBase` | `ref CStrongHandle\<InfoForResourceTypeIMaterial2\>` | get | - |

