# 🔌 CBlend2DUpdateNode

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CAnimUpdateNodeBase`

**实现接口:** `ISchemaClass\<CBlend2DUpdateNode\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Items` | `ref CUtlVector\<BlendItem_t\>` | get | - |
| `Tags` | `ref CUtlVector\<TagSpan_t\>` | get | - |
| `ParamSpans` | `CParamSpanUpdater` | get | - |
| `NodeItemIndices` | `ref CUtlVector\<int\>` | get | - |
| `Damping` | `CAnimInputDamping` | get | - |
| `BlendSourceX` | `ref AnimValueSource` | get | - |
| `ParamX` | `CAnimParamHandle` | get | - |
| `BlendSourceY` | `ref AnimValueSource` | get | - |
| `ParamY` | `CAnimParamHandle` | get | - |
| `BlendMode` | `ref Blend2DMode` | get | - |
| `PlaybackSpeed` | `ref float` | get | - |
| `Loop` | `ref bool` | get | - |
| `LockBlendOnReset` | `ref bool` | get, set | - |
| `LockWhenWaning` | `ref bool` | get | - |
| `AnimEventsAndTagsOnMostWeightedOnly` | `ref bool` | get | - |

