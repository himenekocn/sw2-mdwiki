<a id="itracemanager"></a>

# 🔌 ITraceManager

**命名空间:** `SwiftlyS2.Shared.Services`

**类型:** `interface`

## ⚙️ 方法

### TracePlayerBBox

```csharp
void TracePlayerBBox(Vector start, Vector end, BBox_t bounds, CTraceFilter filter, ref CGameTrace trace)
```

**参数:**

- `start` (`Vector`)
- `end` (`Vector`)
- `bounds` (`BBox_t`)
- `filter` (`CTraceFilter`)
- `trace` (`ref CGameTrace`)

**用法示例:**
```csharp
manager.TracePlayerBBox(start, end, bounds, filter, ref trace);
```

### TracePlayerBBox

```csharp
TraceResult TracePlayerBBox(in Vector start, in Vector end, in BBox_t bounds, in TraceParams? param = default)
```

从指定起始位置到结束位置，使用给定的过滤器和包围盒尺寸执行玩家大小的包围盒碰撞追踪。追踪结果存储于提供的追踪对象中。

**参数:**

- `start` (`in Vector`)
- `end` (`in Vector`)
- `bounds` (`in BBox_t`)
- `param` (`in TraceParams?`) = `default`

**返回值:** `TraceResult`

**用法示例:**
```csharp
var result = manager.TracePlayerBBox(start, end, bounds, null);
```

### TraceShapeLine

```csharp
TraceResult TraceShapeLine(in Vector start, in Vector end, in TraceParams? param = default)
```

使用提供的形状选项，从 <paramref name="start"/> 到 <paramref name="end"/> 进行轨迹追踪。

**参数:**

- `start` (`in Vector`) - 追踪起始位置
- `end` (`in Vector`) - 追踪结束位置。
- `param` (`in TraceParams?`) = `default` - 射线类型和筛选的可选追踪参数。

**返回值:** `TraceResult`

**用法示例:**
```csharp
var result = manager.TraceShapeLine(start, end, null);
```

### TraceShapeAngle

```csharp
TraceResult TraceShapeAngle(in Vector start, in QAngle angle, in TraceParams? param = default)
```

使用提供的形状选项，从<paramref name="start"/>向<paramref name="angle"/>方向进行追踪。

**参数:**

- `start` (`in Vector`) - 追踪起始位置
- `angle` (`in QAngle`) - 追踪方向。
- `param` (`in TraceParams?`) = `default` - 射线类型和筛选的可选追踪参数。

**返回值:** `TraceResult`

**用法示例:**
```csharp
var result = manager.TraceShapeAngle(Vector.Zero, QAngle.Zero, null);
```

### TraceShapeAngle

```csharp
TraceResult TraceShapeAngle(in Vector start, in QAngle angle, float maxDistance = 8192f, in TraceParams? param = default)
```

使用提供的形状选项，从<paramref name="start"/>向<paramref name="angle"/>方向进行追踪。

**参数:**

- `start` (`in Vector`) - 追踪起始位置
- `angle` (`in QAngle`) - 追踪方向。
- `maxDistance` (`float`) = `8192f` - 最大追踪距离。
- `param` (`in TraceParams?`) = `default` - 射线类型和筛选的可选追踪参数。

**返回值:** `TraceResult`

**用法示例:**
```csharp
var result = manager.TraceShapeAngle(start, angle, 100f, null);
```

### TraceShape

```csharp
void TraceShape(Vector start, Vector end, Ray_t ray, CTraceFilter filter, ref CGameTrace trace)
```

**参数:**

- `start` (`Vector`)
- `end` (`Vector`)
- `ray` (`Ray_t`)
- `filter` (`CTraceFilter`)
- `trace` (`ref CGameTrace`)

**用法示例:**
```csharp
manager.TraceShape(startVec, endVec, ray, filter, ref trace);
```

### SimpleTrace

```csharp
void SimpleTrace(Vector start, Vector end, RayType_t rayKind, RnQueryObjectSet objectQuery, MaskTrace interactWith, MaskTrace interactExclude, MaskTrace interactAs, CollisionGroup collision, ref CGameTrace trace, CBaseEntity? filterEntity = null, CBaseEntity? filterSecondEntity = null)
```

**参数:**

- `start` (`Vector`)
- `end` (`Vector`)
- `rayKind` (`RayType_t`)
- `objectQuery` (`RnQueryObjectSet`)
- `interactWith` (`MaskTrace`)
- `interactExclude` (`MaskTrace`)
- `interactAs` (`MaskTrace`)
- `collision` (`CollisionGroup`)
- `trace` (`ref CGameTrace`)
- `filterEntity` (`CBaseEntity?`) = `null`
- `filterSecondEntity` (`CBaseEntity?`) = `null`

**用法示例:**
```csharp
manager.SimpleTrace(start, end, RayType_t.RAY_TYPE_LINE, RnQueryObjectSet.QUERY_SET_DEFAULT, MaskTrace.MASK_ALL, MaskTrace.MASK_NONE, MaskTrace.MASK_ALL, CollisionGroup.COLLISION_GROUP_NONE, ref trace, null, null);
```

### SimpleTrace

```csharp
void SimpleTrace(Vector start, QAngle angle, RayType_t rayKind, RnQueryObjectSet objectQuery, MaskTrace interactWith, MaskTrace interactExclude, MaskTrace interactAs, CollisionGroup collision, ref CGameTrace trace, CBaseEntity? filterEntity = null, CBaseEntity? filterSecondEntity = null)
```

**参数:**

- `start` (`Vector`)
- `angle` (`QAngle`)
- `rayKind` (`RayType_t`)
- `objectQuery` (`RnQueryObjectSet`)
- `interactWith` (`MaskTrace`)
- `interactExclude` (`MaskTrace`)
- `interactAs` (`MaskTrace`)
- `collision` (`CollisionGroup`)
- `trace` (`ref CGameTrace`)
- `filterEntity` (`CBaseEntity?`) = `null`
- `filterSecondEntity` (`CBaseEntity?`) = `null`

**用法示例:**
```csharp
manager.SimpleTrace(Vector.Zero, QAngle.Zero, RayType_t.RAY_TYPE_ENTITY, RnQueryObjectSet.OBJECT_SET_DEFAULT, MaskTrace.MASK_SOLID, MaskTrace.MASK_NONE, MaskTrace.MASK_NONE, CollisionGroup.COLLISION_GROUP_NONE, ref trace, null, null);
```

