# 🔌 CC4

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CCSWeaponBase`

**实现接口:** `ISchemaClass\<CC4\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `LastValidPlayerHeldPosition` | `ref Vector` | get | - |
| `LastValidDroppedPosition` | `ref Vector` | get | - |
| `DoValidDroppedPositionCheck` | `ref bool` | get | - |
| `StartedArming` | `ref bool` | get | - |
| `ArmedTime` | `GameTime_t` | get | - |
| `BombPlacedAnimation` | `ref bool` | get | - |
| `IsPlantingViaUse` | `ref bool` | get | - |
| `EntitySpottedState` | `EntitySpottedState_t` | get | - |
| `SpotRules` | `ref int` | get | - |
| `PlayedArmingBeeps` | `ISchemaFixedArray\<bool\>` | get | - |
| `BombPlanted` | `ref bool` | get | - |

## ⚙️ 方法

### StartedArmingUpdated

```csharp
void StartedArmingUpdated()
```

### ArmedTimeUpdated

```csharp
void ArmedTimeUpdated()
```

### BombPlacedAnimationUpdated

```csharp
void BombPlacedAnimationUpdated()
```

### IsPlantingViaUseUpdated

```csharp
void IsPlantingViaUseUpdated()
```

### EntitySpottedStateUpdated

```csharp
void EntitySpottedStateUpdated()
```

