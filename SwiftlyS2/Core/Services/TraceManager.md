# 📦 TraceManager

**命名空间:** `SwiftlyS2.Core.Services`

**类型:** `class`

**继承:** `ITraceManager`

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

### SimpleTrace (静态)

```csharp
void SimpleTrace(Vector start, Vector end, RayType_t rayKind, RnQueryObjectSet objectQuery, MaskTrace interactWith, MaskTrace interactExclude, MaskTrace interactAs, CollisionGroup collision, ref CGameTrace trace, nint filterEntity, nint filterSecondEntity)
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
- `filterEntity` (`nint`)
- `filterSecondEntity` (`nint`)

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

