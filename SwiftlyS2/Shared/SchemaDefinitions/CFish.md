# 🔌 CFish

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseAnimGraph`

**实现接口:** `ISchemaClass\<CFish\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Pool` | `ref CHandle\<CFishPool\>` | get | - |
| `Id` | `ref uint` | get | - |
| `X` | `ref float` | get | - |
| `Y` | `ref float` | get | - |
| `Z` | `ref float` | get | - |
| `Angle` | `ref float` | get | - |
| `AngleChange` | `ref float` | get | - |
| `Forward` | `ref Vector` | get | - |
| `Perp` | `ref Vector` | get | - |
| `PoolOrigin` | `ref Vector` | get | - |
| `WaterLevel` | `ref float` | get | - |
| `Speed` | `ref float` | get | - |
| `DesiredSpeed` | `ref float` | get | - |
| `CalmSpeed` | `ref float` | get | - |
| `PanicSpeed` | `ref float` | get | - |
| `AvoidRange` | `ref float` | get | - |
| `TurnTimer` | `CountdownTimer` | get | - |
| `TurnClockwise` | `ref bool` | get | - |
| `GoTimer` | `CountdownTimer` | get | - |
| `MoveTimer` | `CountdownTimer` | get | - |
| `PanicTimer` | `CountdownTimer` | get | - |
| `DisperseTimer` | `CountdownTimer` | get | - |
| `ProximityTimer` | `CountdownTimer` | get | - |
| `Visible` | `ref CUtlVector\<PointerTo\<CFish\>\>` | get | - |

## ⚙️ 方法

### XUpdated

```csharp
void XUpdated()
```

### YUpdated

```csharp
void YUpdated()
```

### ZUpdated

```csharp
void ZUpdated()
```

### AngleUpdated

```csharp
void AngleUpdated()
```

### PoolOriginUpdated

```csharp
void PoolOriginUpdated()
```

### WaterLevelUpdated

```csharp
void WaterLevelUpdated()
```

