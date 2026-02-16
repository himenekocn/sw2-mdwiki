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

### HitEntityByDesignerName<T>

```csharp
bool HitEntityByDesignerName<T>(string designerName, out T outEntity, NameMatchType matchType = NameMatchType.StartsWith)
```

**参数:**

- `designerName` (`string`)
- `outEntity` (`out T`)
- `matchType` (`NameMatchType`) = `NameMatchType.StartsWith`

**返回值:** `bool`

**用法示例:**
```csharp
if (gameTrace.HitEntityByDesignerName<MyEntity>("MyEntityName", out var entity, NameMatchType.Value))
{
    // 使用 entity
}
```

### HitEntityByDesignerName<T>

```csharp
bool HitEntityByDesignerName<T>(string designerName, NameMatchType matchType = NameMatchType.StartsWith)
```

**参数:**

- `designerName` (`string`)
- `matchType` (`NameMatchType`) = `NameMatchType.StartsWith`

**返回值:** `bool`

**用法示例:**
```csharp
bool hit = gameTrace.HitEntityByDesignerName<CEntity>(designerName, NameMatchType.Value);
```

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

### HitEntity<T>

```csharp
bool HitEntity<T>(out T entity)
```

**参数:**

- `entity` (`out T`)

**返回值:** `bool`

**用法示例:**
```csharp
if (gameTrace.HitEntity(out Player player)) { /* ... */ }
```

### HitEntity<T>

```csharp
bool HitEntity<T>()
```

**返回值:** `bool`

**用法示例:**
```csharp
if (gameTrace.HitEntity<Player>()) { /* ... */ }
```

