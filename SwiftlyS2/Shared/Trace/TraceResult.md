<a id="traceresult"></a>

# 🏗️ TraceResult

**命名空间:** `SwiftlyS2.Shared.Trace`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `DidHit` | `bool` | - | 如果追踪击中物体则返回真（要么追踪分数小于1.0，要么起始位置位于实体中）。 |

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SurfaceProperties` | `PhysSurfacePropertiesTrace?` | get, set | 命中追踪的表面物理材质属性。 |
| `HitBox` | `HitBoxTrace?` | get, set | 关于被射线击中的命中盒的信息（如果适用）。 |
| `Contents` | `ulong` | get, set | 被击中的表面或体积的内容遮罩。 |
| `BodyTransform` | `CTransform` | get, set | 被击中实体的变换矩阵。 |
| `ShapeAttributes` | `TraceCollisionAttributes` | get, set | 被碰撞形状的碰撞属性。 |
| `StartPos` | `Vector` | get, set | 追踪的起始位置。 |
| `EndPos` | `Vector` | get, set | 追踪的结束位置。 |
| `HitNormal` | `Vector` | get, set | 该轨迹命中点的表面法线。 |
| `HitPoint` | `Vector` | get, set | 追踪在3D空间中击中表面或实体的确切点。 |
| `HitOffset` | `float` | get, set | 沿追踪方向从追踪起始位置到命中点的距离。 |
| `Fraction` | `float` | get, set | 在撞击到物体前已行进轨迹距离的比例（0.0 = 起点，1.0 = 终点，> 1.0 = 未命中）。 |
| `Triangle` | `int` | get, set | 命中表面的三角形索引（如适用）。 |
| `HitboxBoneIndex` | `short` | get, set | 受击命中框的骨骼索引（如适用）。 |
| `RayType` | `RayType_t` | get, set | 用于此追踪的射线类型。 |
| `StartInSolid` | `bool` | get, set | 指示追踪起始位置是否已位于固体对象内部。 |
| `ExactHitPoint` | `bool` | get, set | 指示是否为此追踪结果计算了精确命中点。 |
| `Entity` | `CEntityInstance?` | get, set | 由追踪命中的实体（如适用）。若未命中任何物体或命中静态表面则为空。 |
| `DidHit` | `bool` | - | 如果追踪击中物体则返回真（要么追踪分数小于1.0，要么起始位置位于实体中）。 |
| `Distance` | `float` | - | 计算从起始位置到结束位置的总移动距离。 |
| `Direction` | `Vector` | - | 计算从起点到终点的射线归一化方向向量。 |

## ⚙️ 方法

### HitEntityByDesignerName<T>

```csharp
bool HitEntityByDesignerName<T>(string designerName, out T? outEntity, NameMatchType matchType = NameMatchType.StartsWith)
```

**参数:**

- `designerName` (`string`)
- `outEntity` (`out T?`)
- `matchType` (`NameMatchType`) = `NameMatchType.StartsWith`

**返回值:** `bool`

**用法示例:**
```csharp
traceResult.HitEntityByDesignerName("npc_combine_s", out CBaseEntity? entity, NameMatchType.Exact);
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
bool hit = traceResult.HitEntityByDesignerName<Player>("npc_dota_hero_axe", NameMatchType.Exact);
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
bool hit = traceResult.HitPlayer(out IPlayer? player);
```

### HitPlayer

```csharp
bool HitPlayer()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool hit = traceResult.HitPlayer();
```

### HitEntity<T>

```csharp
bool HitEntity<T>(out T? entity)
```

**参数:**

- `entity` (`out T?`)

**返回值:** `bool`

**用法示例:**
```csharp
bool hit = traceResult.HitEntity(out Player? entity);
```

### HitEntity<T>

```csharp
bool HitEntity<T>()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool hit = traceResult.HitEntity<Player>();
```

### ToString

```csharp
string ToString()
```

**返回值:** `string`

