# 🔌 C_OP_RenderMaterialProxy

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CParticleFunctionRenderer`

**实现接口:** `ISchemaClass\<C_OP_RenderMaterialProxy\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MaterialControlPoint` | `ref int` | get | - |
| `ProxyType` | `ref MaterialProxyType_t` | get | - |
| `MaterialVars` | `ref CUtlVector\<MaterialVariable_t\>` | get | - |
| `OverrideMaterial` | `ref CStrongHandle\<InfoForResourceTypeIMaterial2\>` | get | - |
| `MaterialOverrideEnabled` | `CParticleCollectionFloatInput` | get | - |
| `ColorScale` | `CParticleCollectionVecInput` | get | - |
| `Alpha` | `CPerParticleFloatInput` | get | - |
| `ColorBlendType` | `ref ParticleColorBlendType_t` | get | - |

