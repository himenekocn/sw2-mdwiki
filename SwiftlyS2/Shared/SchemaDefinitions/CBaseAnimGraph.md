# 🔌 CBaseAnimGraph

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseModelEntity`

**实现接口:** `ISchemaClass\<CBaseAnimGraph\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `GraphControllerManager` | `CAnimGraphControllerManager` | get | - |
| `MainGraphController` | `CAnimGraphControllerBase?` | get | - |
| `InitiallyPopulateInterpHistory` | `ref bool` | get | - |
| `ChoreoServices` | `IChoreoServices?` | get | - |
| `AnimGraphUpdateEnabled` | `ref bool` | get | - |
| `MaxSlopeDistance` | `ref float` | get | - |
| `LastSlopeCheckPos` | `ref Vector` | get | - |
| `AnimGraphUpdateId` | `ref uint` | get | - |
| `AnimationUpdateScheduled` | `ref bool` | get | - |
| `Force` | `ref Vector` | get | - |
| `ForceBone` | `ref int` | get | - |
| `RagdollPose` | `PhysicsRagdollPose_t` | get | - |
| `RagdollEnabled` | `ref bool` | get | - |
| `RagdollClientSide` | `ref bool` | get | - |
| `XParentedRagdollRootInEntitySpace` | `ref CTransform` | get | - |

## ⚙️ 方法

### InitiallyPopulateInterpHistoryUpdated

```csharp
void InitiallyPopulateInterpHistoryUpdated()
```

### AnimGraphUpdateEnabledUpdated

```csharp
void AnimGraphUpdateEnabledUpdated()
```

### ForceUpdated

```csharp
void ForceUpdated()
```

### ForceBoneUpdated

```csharp
void ForceBoneUpdated()
```

### RagdollPoseUpdated

```csharp
void RagdollPoseUpdated()
```

### RagdollEnabledUpdated

```csharp
void RagdollEnabledUpdated()
```

### RagdollClientSideUpdated

```csharp
void RagdollClientSideUpdated()
```

