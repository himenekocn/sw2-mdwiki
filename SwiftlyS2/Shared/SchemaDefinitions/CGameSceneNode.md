# 🔌 CGameSceneNode

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `ISchemaClass\<CGameSceneNode\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `NodeToWorld` | `ref CTransform` | get | - |
| `Owner` | `CEntityInstance?` | get | - |
| `Parent` | `CGameSceneNode?` | get | - |
| `Child` | `CGameSceneNode?` | get | - |
| `NextSibling` | `CGameSceneNode?` | get | - |
| `Parent1` | `CGameSceneNodeHandle` | get | - |
| `Origin` | `CNetworkOriginCellCoordQuantizedVector` | get | - |
| `Rotation` | `ref QAngle` | get | - |
| `Scale` | `ref float` | get | - |
| `AbsOrigin` | `ref Vector` | get | - |
| `AbsRotation` | `ref QAngle` | get | - |
| `AbsScale` | `ref float` | get | - |
| `ParentAttachmentOrBone` | `ref short` | get | - |
| `DebugAbsOriginChanges` | `ref bool` | get | - |
| `Dormant` | `ref bool` | get | - |
| `ForceParentToBeNetworked` | `ref bool` | get | - |
| `DirtyHierarchy` | `SchemaUntypedField` | get | - |
| `DirtyBoneMergeInfo` | `SchemaUntypedField` | get | - |
| `NetworkedPositionChanged` | `SchemaUntypedField` | get | - |
| `NetworkedAnglesChanged` | `SchemaUntypedField` | get | - |
| `NetworkedScaleChanged` | `SchemaUntypedField` | get | - |
| `WillBeCallingPostDataUpdate` | `SchemaUntypedField` | get | - |
| `BoneMergeFlex` | `SchemaUntypedField` | get | - |
| `LatchAbsOrigin` | `SchemaUntypedField` | get | - |
| `DirtyBoneMergeBoneToRoot` | `SchemaUntypedField` | get | - |
| `HierarchicalDepth` | `ref byte` | get | - |
| `HierarchyType` | `ref byte` | get | - |
| `DoNotSetAnimTimeInInvalidatePhysicsCount` | `ref byte` | get | - |
| `Name` | `ref CUtlStringToken` | get | - |
| `HierarchyAttachName` | `ref CUtlStringToken` | get | - |
| `ZOffset` | `ref float` | get, set | - |
| `ClientLocalScale` | `ref float` | get | - |
| `RenderOrigin` | `ref Vector` | get | - |

## ⚙️ 方法

### Parent1Updated

```csharp
void Parent1Updated()
```

### OriginUpdated

```csharp
void OriginUpdated()
```

### RotationUpdated

```csharp
void RotationUpdated()
```

### ScaleUpdated

```csharp
void ScaleUpdated()
```

### NameUpdated

```csharp
void NameUpdated()
```

### HierarchyAttachNameUpdated

```csharp
void HierarchyAttachNameUpdated()
```

