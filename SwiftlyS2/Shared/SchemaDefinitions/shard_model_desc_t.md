# 🔌 shard_model_desc_t

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `ISchemaClass\<shard_model_desc_t\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ModelID` | `ref int` | get | - |
| `MaterialBase` | `ref CStrongHandle\<InfoForResourceTypeIMaterial2\>` | get | - |
| `MaterialDamageOverlay` | `ref CStrongHandle\<InfoForResourceTypeIMaterial2\>` | get | - |
| `Solid` | `ref ShardSolid_t` | get | - |
| `PanelSize` | `ref Vector2D` | get | - |
| `StressPositionA` | `ref Vector2D` | get | - |
| `StressPositionB` | `ref Vector2D` | get | - |
| `PanelVertices` | `ref CUtlVector\<Vector2D\>` | get | - |
| `InitialPanelVertices` | `ref CUtlVector\<Vector4D\>` | get | - |
| `GlassHalfThickness` | `ref float` | get | - |
| `HasParent` | `ref bool` | get | - |
| `ParentFrozen` | `ref bool` | get | - |
| `SurfacePropStringToken` | `ref CUtlStringToken` | get | - |

## ⚙️ 方法

### ModelIDUpdated

```csharp
void ModelIDUpdated()
```

### MaterialBaseUpdated

```csharp
void MaterialBaseUpdated()
```

### MaterialDamageOverlayUpdated

```csharp
void MaterialDamageOverlayUpdated()
```

### SolidUpdated

```csharp
void SolidUpdated()
```

### PanelSizeUpdated

```csharp
void PanelSizeUpdated()
```

### StressPositionAUpdated

```csharp
void StressPositionAUpdated()
```

### StressPositionBUpdated

```csharp
void StressPositionBUpdated()
```

### PanelVerticesUpdated

```csharp
void PanelVerticesUpdated()
```

### InitialPanelVerticesUpdated

```csharp
void InitialPanelVerticesUpdated()
```

### GlassHalfThicknessUpdated

```csharp
void GlassHalfThicknessUpdated()
```

### HasParentUpdated

```csharp
void HasParentUpdated()
```

### ParentFrozenUpdated

```csharp
void ParentFrozenUpdated()
```

### SurfacePropStringTokenUpdated

```csharp
void SurfacePropStringTokenUpdated()
```

