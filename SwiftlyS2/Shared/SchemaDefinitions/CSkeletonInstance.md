# 🔌 CSkeletonInstance

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CGameSceneNode`

**实现接口:** `ISchemaClass\<CSkeletonInstance\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ModelState` | `CModelState` | get | - |
| `IsAnimationEnabled` | `ref bool` | get | - |
| `UseParentRenderBounds` | `ref bool` | get | - |
| `DisableSolidCollisionsForHierarchy` | `ref bool` | get | - |
| `DirtyMotionType` | `SchemaUntypedField` | get | - |
| `IsGeneratingLatchedParentSpaceState` | `SchemaUntypedField` | get | - |
| `MaterialGroup` | `ref CUtlStringToken` | get | - |
| `HitboxSet` | `ref byte` | get | - |
| `ForceServerConstraintsEnabled` | `ref bool` | get | - |

## ⚙️ 方法

### ModelStateUpdated

```csharp
void ModelStateUpdated()
```

### IsAnimationEnabledUpdated

```csharp
void IsAnimationEnabledUpdated()
```

### UseParentRenderBoundsUpdated

```csharp
void UseParentRenderBoundsUpdated()
```

### MaterialGroupUpdated

```csharp
void MaterialGroupUpdated()
```

### HitboxSetUpdated

```csharp
void HitboxSetUpdated()
```

