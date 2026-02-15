# 🔌 SceneObject_t

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `ISchemaClass\<SceneObject_t\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ObjectID` | `ref uint` | get | - |
| `Transform` | `ISchemaFixedArray\<Vector4D\>` | get | - |
| `FadeStartDistance` | `ref float` | get | - |
| `FadeEndDistance` | `ref float` | get | - |
| `TintColor` | `ref Vector4D` | get | - |
| `Skin` | `string` | get, set | - |
| `ObjectTypeFlags` | `ref ObjectTypeFlags_t` | get | - |
| `LightingOrigin` | `ref Vector` | get | - |
| `OverlayRenderOrder` | `ref short` | get | - |
| `LODOverride` | `ref short` | get | - |
| `CubeMapPrecomputedHandshake` | `ref int` | get | - |
| `LightProbeVolumePrecomputedHandshake` | `ref int` | get | - |
| `RenderableModel` | `ref CStrongHandle\<InfoForResourceTypeCModel\>` | get | - |
| `Renderable` | `ref CStrongHandle\<InfoForResourceTypeCRenderMesh\>` | get | - |

