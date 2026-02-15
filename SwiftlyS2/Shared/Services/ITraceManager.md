# 🔌 ITraceManager

**命名空间:** `SwiftlyS2.Shared.Services`

**类型:** `interface`

## ⚙️ 方法

### TracePlayerBBox

```csharp
void TracePlayerBBox(Vector start, Vector end, BBox_t bounds, CTraceFilter filter, ref CGameTrace trace)
```

执行从指定起始位置到结束位置的玩家尺寸边界框的碰撞追踪，使用给定的筛选器和边界框尺寸。追踪结果存储在提供的追踪对象中。

**参数:**

- `start` (`Vector`) - 追踪的起始位置，通常代表玩家的初始位置。
- `end` (`Vector`) - 追踪的结束位置，表示边界框移动的目标位置。
- `bounds` (`BBox_t`) - 要追踪的玩家边界框的尺寸。
- `filter` (`CTraceFilter`) - 用于确定在追踪操作中应考虑哪些实体或表面的追踪过滤器。
- `trace` (`ref CGameTrace`) - 对 CGameTrace 对象的引用，该对象接收追踪结果，包括碰撞信息和命中详情。

**用法示例:**
```csharp
manager.TracePlayerBBox(startPos, endPos, bounds, filter, ref traceResult);
```

### TraceShape

```csharp
void TraceShape(Vector start, Vector end, Ray_t ray, CTraceFilter filter, ref CGameTrace trace)
```

使用给定的射线和筛选器，从指定的起点到终点执行追踪操作，并将碰撞信息填充到追踪结果中。

**参数:**

- `start` (`Vector`) - 跟踪的起始位置，以向量表示。
- `end` (`Vector`) - 跟踪的结束位置，以向量形式表示。
- `ray` (`Ray_t`) - 用于追踪的射线定义，指定方向和其他射线属性。
- `filter` (`CTraceFilter`) - 用于确定在追踪过程中应考虑哪些实体或表面的筛选器。
- `trace` (`ref CGameTrace`) - 一个指向 CGameTrace 结构体的引用，该结构体用于接收追踪结果，包括命中信息和表面细节。

**用法示例:**
```csharp
manager.TraceShape(startPos, endPos, ray, filter, ref traceResult);
```

### SimpleTrace

```csharp
void SimpleTrace(Vector start, Vector end, RayType_t rayKind, RnQueryObjectSet objectQuery, MaskTrace interactWith, MaskTrace interactExclude, MaskTrace interactAs, CollisionGroup collision, ref CGameTrace trace, CBaseEntity? filterEntity = null, CBaseEntity? filterSecondEntity = null)
```

执行一个简单的追踪形状操作，从指定的起点到终点，使用提供的对象查询和追踪掩码。追踪的结果存储在提供的追踪对象中。

**参数:**

- `start` (`Vector`) - 跟踪的起始位置，以向量表示。
- `end` (`Vector`) - 跟踪的结束位置，以向量形式表示。
- `rayKind` (`RayType_t`) - 用于追踪的射线类型。
- `objectQuery` (`RnQueryObjectSet`) - 用于指定在跟踪过程中要考虑哪些对象的对象查询。
- `interactWith` (`MaskTrace`) - 交互层，用于定义追踪中要包含的表面或实体的类型。
- `interactExclude` (`MaskTrace`) - 交互层，用于定义要从追踪中排除的表面或实体的类型。
- `interactAs` (`MaskTrace`) - 交互层，用于定义在追踪过程中作为交互对象的表面或实体的类型。
- `collision` (`CollisionGroup`) - 用于定义追踪过程中碰撞行为的碰撞组。
- `trace` (`ref CGameTrace`) - 一个指向 CGameTrace 结构体的引用，该结构体用于接收追踪结果，包括命中信息和表面细节。
- `filterEntity` (`CBaseEntity?`) = `null` - 要排除在跟踪之外的可选实体。
- `filterSecondEntity` (`CBaseEntity?`) = `null` - 一个可选的第二个实体，用于从跟踪中排除。

**用法示例:**
```csharp
manager.SimpleTrace(Vector.Zero, Vector.One, RayType_t.Value, RnQueryObjectSet.Value, MaskTrace.Value, MaskTrace.Value, MaskTrace.Value, CollisionGroup.Value, ref trace, null, null);
```

### SimpleTrace

```csharp
void SimpleTrace(Vector start, QAngle angle, RayType_t rayKind, RnQueryObjectSet objectQuery, MaskTrace interactWith, MaskTrace interactExclude, MaskTrace interactAs, CollisionGroup collision, ref CGameTrace trace, CBaseEntity? filterEntity = null, CBaseEntity? filterSecondEntity = null)
```

从指定的起点开始，沿给定角度定义的方向，使用提供的对象查询和追踪掩码执行简单的追踪形状操作。追踪结果存储在提供的追踪对象中。

**参数:**

- `start` (`Vector`) - 跟踪的起始位置，以向量表示。
- `angle` (`QAngle`) - 追踪的方向，以 QAngle 表示。
- `rayKind` (`RayType_t`) - 用于追踪的射线类型。
- `objectQuery` (`RnQueryObjectSet`) - 用于指定在跟踪过程中要考虑哪些对象的对象查询。
- `interactWith` (`MaskTrace`) - 交互层，用于定义追踪中要包含的表面或实体的类型。
- `interactExclude` (`MaskTrace`) - 交互层，用于定义要从追踪中排除的表面或实体的类型。
- `interactAs` (`MaskTrace`) - 交互层，用于定义在追踪过程中作为交互对象的表面或实体的类型。
- `collision` (`CollisionGroup`) - 用于定义追踪过程中碰撞行为的碰撞组。
- `trace` (`ref CGameTrace`) - 一个指向 CGameTrace 结构体的引用，该结构体用于接收追踪结果，包括命中信息和表面细节。
- `filterEntity` (`CBaseEntity?`) = `null` - 要排除在跟踪之外的可选实体。
- `filterSecondEntity` (`CBaseEntity?`) = `null` - 一个可选的第二个实体，用于从跟踪中排除。

**用法示例:**
```csharp
manager.SimpleTrace(Vector.Zero, QAngle.Zero, RayType_t.Value, RnQueryObjectSet.Value, MaskTrace.Value, MaskTrace.Value, MaskTrace.Value, CollisionGroup.Value, ref trace, null, null);
```

