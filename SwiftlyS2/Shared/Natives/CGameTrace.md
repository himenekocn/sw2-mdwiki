# 🏗️ CGameTrace

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `SurfaceProperties` | `CPhysSurfacePropertiesTrace*` | - | - |
| `pEntity` | `void*` | - | - |
| `HitBox` | `CHitBoxTrace*` | - | - |
| `Body` | `void*` | - | - |
| `Shape` | `void*` | - | - |
| `Contents` | `ulong` | - | - |
| `BodyTransform` | `CTransform` | - | - |
| `ShapeAttributes` | `RnCollisionAttr_t` | - | - |
| `StartPos` | `Vector` | - | - |
| `EndPos` | `Vector` | - | - |
| `HitNormal` | `Vector` | - | - |
| `HitPoint` | `Vector` | - | - |
| `HitOffset` | `float` | - | - |
| `Fraction` | `float` | - | - |
| `Triangle` | `int` | - | - |
| `HitboxBoneIndex` | `short` | - | - |
| `RayType` | `RayType_t` | - | - |
| `StartInSolid` | `bool` | - | - |
| `ExactHitPoint` | `bool` | - | - |
| `DidHit` | `bool` | readonly | - |

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Entity` | `CEntityInstance` | - | - |
| `DidHit` | `bool` | - | - |
| `Distance` | `float` | - | - |
| `Direction` | `Vector` | - | - |

## ⚙️ 方法

### HitPlayer

```csharp
bool HitPlayer(out IPlayer? player)
```

**参数:**

- `player` (`out IPlayer?`)

**返回值:** `bool`

**用法示例:**
```csharp
CGameTrace.HitPlayer(out var player);
if (player != null) Console.WriteLine(player.Name);
```

### HitPlayer

```csharp
bool HitPlayer()
```

**返回值:** `bool`

**用法示例:**
```csharp
CGameTrace.HitPlayer();
```

