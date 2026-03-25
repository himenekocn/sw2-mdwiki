# 🔌 ITraceManager

**命名空间:** `SwiftlyS2.Shared.Services`

**类型:** `interface`

## ⚙️ 方法

### TracePlayerBBox

```csharp
void TracePlayerBBox(Vector start, Vector end, BBox_t bounds, CTraceFilter filter, ref CGameTrace trace)
```

执行从指定起始位置到结束位置的玩家尺寸包围盒碰撞追踪，使用给定的过滤条件和包围盒尺寸。追踪结果将存储于提供的追踪对象中。

**参数:**

- `start` (`Vector`) - 追踪的起始位置，通常代表玩家的初始位置。
- `end` (`Vector`) - 追踪的结束位置，表示边界框移动的目标位置。
- `bounds` (`BBox_t`) - 待追踪的玩家包围盒尺寸。
- `filter` (`CTraceFilter`) - 用于确定在追踪操作中哪些实体或表面被考虑的追踪过滤器。
- `trace` (`ref CGameTrace`) - 一个指向 CGameTrace 对象的引用，该对象接收射线检测（trace）的结果，包括碰撞信息和命中详情。

**用法示例:**
```csharp
manager.TracePlayerBBox(player.EyePosition, targetPosition, player.Mins, new CTraceFilter(), ref traceResult);
```

### TraceShape

```csharp
void TraceShape(Vector start, Vector end, Ray_t ray, CTraceFilter filter, ref CGameTrace trace)
```

使用给定的射线和过滤器，从指定的起点到终点执行追踪操作，并将碰撞信息填充至追踪结果中。

**参数:**

- `start` (`Vector`) - 轨迹的起始位置，表示为向量。
- `end` (`Vector`) - 追踪的终点位置，表示为向量。
- `ray` (`Ray_t`) - 用于追踪的射线定义，指定方向及其他射线属性。
- `filter` (`CTraceFilter`) - 确定在追踪过程中被视为有效实体或表面的过滤器。
- `trace` (`ref CGameTrace`) - 一个指向 CGameTrace 结构的引用，用于接收追踪结果，包括命中信息和表面细节。

**用法示例:**
```csharp
Vector start = new Vector(0, 0, 0); Vector end = new Vector(100, 100, 100); manager.TraceShape(start, end, ray, filter, ref trace);
```

### SimpleTrace

```csharp
void SimpleTrace(Vector start, Vector end, RayType_t rayKind, RnQueryObjectSet objectQuery, MaskTrace interactWith, MaskTrace interactExclude, MaskTrace interactAs, CollisionGroup collision, ref CGameTrace trace, CBaseEntity? filterEntity = null, CBaseEntity? filterSecondEntity = null)
```

使用提供的对象查询和追踪掩码，从指定起点到终点执行简单的形状追踪操作。追踪结果将存储于提供的追踪对象中。

**参数:**

- `start` (`Vector`) - 轨迹的起始位置，表示为向量。
- `end` (`Vector`) - 追踪的终点位置，表示为向量。
- `rayKind` (`RayType_t`) - 用于追踪的光线类型。
- `objectQuery` (`RnQueryObjectSet`) - 指定在追踪过程中应考虑哪些对象的对象查询。
- `interactWith` (`MaskTrace`) - 定义在射线检测中应包含的表面或实体类型的交互层。
- `interactExclude` (`MaskTrace`) - 定义从射线检测中排除的表面或实体类型的交互层。
- `interactAs` (`MaskTrace`) - 定义在射线检测（trace）期间要作为交互对象进行交互的表面或实体类型的交互层。
- `collision` (`CollisionGroup`) - 定义追踪期间碰撞行为的碰撞组。
- `trace` (`ref CGameTrace`) - 一个指向 CGameTrace 结构的引用，用于接收追踪结果，包括命中信息和表面细节。
- `filterEntity` (`CBaseEntity?`) = `null` - 一个可选的实体，用于从射线检测中排除。
- `filterSecondEntity` (`CBaseEntity?`) = `null` - 一个可选的第二个实体，用于从射线检测中排除。

**用法示例:**
```csharp
manager.SimpleTrace(start, end, RayType_t.Value, RnQueryObjectSet.Value, MaskTrace.Value, MaskTrace.Value, MaskTrace.Value, CollisionGroup.Value, ref trace, null, null);
```

### SimpleTrace

```csharp
void SimpleTrace(Vector start, QAngle angle, RayType_t rayKind, RnQueryObjectSet objectQuery, MaskTrace interactWith, MaskTrace interactExclude, MaskTrace interactAs, CollisionGroup collision, ref CGameTrace trace, CBaseEntity? filterEntity = null, CBaseEntity? filterSecondEntity = null)
```

从指定的起点沿给定角度定义的方向执行简单的射线形状检测操作，使用提供的对象查询和遮挡掩码。检测结果将存储在提供的检测对象中。

**参数:**

- `start` (`Vector`) - 轨迹的起始位置，表示为向量。
- `angle` (`QAngle`) - 射线的方向，表示为 QAngle。
- `rayKind` (`RayType_t`) - 用于追踪的光线类型。
- `objectQuery` (`RnQueryObjectSet`) - 指定在追踪过程中应考虑哪些对象的对象查询。
- `interactWith` (`MaskTrace`) - 定义在射线检测中应包含的表面或实体类型的交互层。
- `interactExclude` (`MaskTrace`) - 定义从射线检测中排除的表面或实体类型的交互层。
- `interactAs` (`MaskTrace`) - 定义在射线检测（trace）期间要作为交互对象进行交互的表面或实体类型的交互层。
- `collision` (`CollisionGroup`) - 定义追踪期间碰撞行为的碰撞组。
- `trace` (`ref CGameTrace`) - 一个指向 CGameTrace 结构的引用，用于接收追踪结果，包括命中信息和表面细节。
- `filterEntity` (`CBaseEntity?`) = `null` - 一个可选的实体，用于从射线检测中排除。
- `filterSecondEntity` (`CBaseEntity?`) = `null` - 一个可选的第二个实体，用于从射线检测中排除。

**用法示例:**
```csharp
manager.SimpleTrace(start, angle, RayType_t.Value, RnQueryObjectSet.Value, MaskTrace.Value, MaskTrace.Value, MaskTrace.Value, CollisionGroup.Value, ref trace, null, null);
```

