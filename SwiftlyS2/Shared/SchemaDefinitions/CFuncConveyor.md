# 🔌 CFuncConveyor

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseModelEntity`

**实现接口:** `ISchemaClass\<CFuncConveyor\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ConveyorModels` | `string` | get, set | - |
| `TransitionDurationSeconds` | `ref float` | get | - |
| `MoveEntitySpace` | `ref QAngle` | get | - |
| `MoveDirEntitySpace` | `ref Vector` | get | - |
| `TargetSpeed` | `ref float` | get | - |
| `TransitionStartTick` | `GameTick_t` | get | - |
| `TransitionDurationTicks` | `ref int` | get | - |
| `TransitionStartSpeed` | `ref float` | get | - |
| `ConveyorModels1` | `ref CUtlVector\<CHandle\<CBaseEntity\>\>` | get | - |

## ⚙️ 方法

### MoveDirEntitySpaceUpdated

```csharp
void MoveDirEntitySpaceUpdated()
```

### TargetSpeedUpdated

```csharp
void TargetSpeedUpdated()
```

### TransitionStartTickUpdated

```csharp
void TransitionStartTickUpdated()
```

### TransitionDurationTicksUpdated

```csharp
void TransitionDurationTicksUpdated()
```

### TransitionStartSpeedUpdated

```csharp
void TransitionStartSpeedUpdated()
```

### ConveyorModels1Updated

```csharp
void ConveyorModels1Updated()
```

