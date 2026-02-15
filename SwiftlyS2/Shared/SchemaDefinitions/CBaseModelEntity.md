# 🔌 CBaseModelEntity

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseEntity`

**实现接口:** `ISchemaClass\<CBaseModelEntity\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CRenderComponent` | `CRenderComponent?` | get | - |
| `CHitboxComponent` | `CHitboxComponent` | get | - |
| `DestructiblePartInitialStateDestructed0` | `ref HitGroup_t` | get | - |
| `DestructiblePartInitialStateDestructed1` | `ref HitGroup_t` | get | - |
| `DestructiblePartInitialStateDestructed2` | `ref HitGroup_t` | get | - |
| `DestructiblePartInitialStateDestructed3` | `ref HitGroup_t` | get | - |
| `DestructiblePartInitialStateDestructed4` | `ref HitGroup_t` | get | - |
| `DestructiblePartInitialStateDestructed0_PartIndex` | `ref int` | get | - |
| `DestructiblePartInitialStateDestructed1_PartIndex` | `ref int` | get | - |
| `DestructiblePartInitialStateDestructed2_PartIndex` | `ref int` | get | - |
| `DestructiblePartInitialStateDestructed3_PartIndex` | `ref int` | get | - |
| `DestructiblePartInitialStateDestructed4_PartIndex` | `ref int` | get | - |
| `DestructiblePartsSystemComponent` | `CDestructiblePartsComponent?` | get | - |
| `DissolveStartTime` | `GameTime_t` | get | - |
| `OnIgnite` | `ref CEntityIOOutput` | get | - |
| `RenderMode` | `ref RenderMode_t` | get | - |
| `RenderFX` | `ref RenderFx_t` | get | - |
| `AllowFadeInView` | `ref bool` | get | - |
| `Render` | `ref Color` | get | - |
| `RenderAttributes` | `ref CUtlVector\<EntityRenderAttribute_t\>` | get | - |
| `RenderToCubemaps` | `ref bool` | get | - |
| `NoInterpolate` | `ref bool` | get | - |
| `Collision` | `CCollisionProperty` | get | - |
| `Glow` | `CGlowProperty` | get | - |
| `GlowBackfaceMult` | `ref float` | get | - |
| `FadeMinDist` | `ref float` | get | - |
| `FadeMaxDist` | `ref float` | get | - |
| `FadeScale` | `ref float` | get | - |
| `ShadowStrength` | `ref float` | get | - |
| `ObjectCulling` | `ref byte` | get | - |
| `ViewOffset` | `CNetworkViewOffsetVector` | get, set | - |
| `DisabledHitGroups` | `ISchemaFixedArray\<uint\>` | get | - |

## ⚙️ 方法

### CHitboxComponentUpdated

```csharp
void CHitboxComponentUpdated()
```

### DestructiblePartsSystemComponentUpdated

```csharp
void DestructiblePartsSystemComponentUpdated()
```

### RenderModeUpdated

```csharp
void RenderModeUpdated()
```

### RenderFXUpdated

```csharp
void RenderFXUpdated()
```

### RenderUpdated

```csharp
void RenderUpdated()
```

### RenderAttributesUpdated

```csharp
void RenderAttributesUpdated()
```

### RenderToCubemapsUpdated

```csharp
void RenderToCubemapsUpdated()
```

### NoInterpolateUpdated

```csharp
void NoInterpolateUpdated()
```

### CollisionUpdated

```csharp
void CollisionUpdated()
```

### GlowUpdated

```csharp
void GlowUpdated()
```

### GlowBackfaceMultUpdated

```csharp
void GlowBackfaceMultUpdated()
```

### FadeMinDistUpdated

```csharp
void FadeMinDistUpdated()
```

### FadeMaxDistUpdated

```csharp
void FadeMaxDistUpdated()
```

### FadeScaleUpdated

```csharp
void FadeScaleUpdated()
```

### ShadowStrengthUpdated

```csharp
void ShadowStrengthUpdated()
```

### ObjectCullingUpdated

```csharp
void ObjectCullingUpdated()
```

### ViewOffsetUpdated

```csharp
void ViewOffsetUpdated()
```

### DisabledHitGroupsUpdated

```csharp
void DisabledHitGroupsUpdated()
```

