<a id="traceparamsbuilder"></a>

# 📦 TraceParamsBuilder

TraceParams 的流式构建器。

**命名空间:** `SwiftlyS2.Shared.Trace`

**类型:** `class`

## ⚙️ 方法

### WithRay

```csharp
TraceParamsBuilder WithRay(in Ray_t ray)
```

**参数:**

- `ray` (`in Ray_t`)

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
var builder = TraceParamsBuilder.Create().WithRay(ray);
```

### WithLineRay

```csharp
TraceParamsBuilder WithLineRay(Vector startOffset, float radius = 0f)
```

**参数:**

- `startOffset` (`Vector`)
- `radius` (`float`) = `0f`

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
var builder = TraceParamsBuilder.Create();
builder.WithLineRay(Vector.Zero, 1.0f);
```

### WithLineRay

```csharp
TraceParamsBuilder WithLineRay()
```

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
var builder = TraceParamsBuilder.Create().WithLineRay();
```

### WithSphereRay

```csharp
TraceParamsBuilder WithSphereRay(Vector center, float radius)
```

**参数:**

- `center` (`Vector`)
- `radius` (`float`)

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
var builder = TraceParamsBuilder.Create().WithSphereRay(Vector.Zero, 10.0f);
```

### WithHullRay

```csharp
TraceParamsBuilder WithHullRay(Vector mins, Vector maxs)
```

**参数:**

- `mins` (`Vector`)
- `maxs` (`Vector`)

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
var builder = TraceParamsBuilder.Create();
builder.WithHullRay(Vector.Zero, new Vector(1, 1, 1));
```

### WithCapsuleRay

```csharp
TraceParamsBuilder WithCapsuleRay(Vector centerA, Vector centerB, float radius)
```

**参数:**

- `centerA` (`Vector`)
- `centerB` (`Vector`)
- `radius` (`float`)

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
var builder = TraceParamsBuilder.Create();
builder.WithCapsuleRay(new Vector(0, 0, 0), new Vector(1, 1, 1), 0.5f);
```

### WithObjectQuery

```csharp
TraceParamsBuilder WithObjectQuery(RnQueryObjectSet objectQuery)
```

查询应包含哪些对象组。

**参数:**

- `objectQuery` (`RnQueryObjectSet`)

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
var builder = new TraceParamsBuilder();
builder.WithObjectQuery(RnQueryObjectSet.All);
```

### WithInteraction

```csharp
TraceParamsBuilder WithInteraction(MaskTrace interactWith, MaskTrace interactExclude = MaskTrace.Empty, MaskTrace interactAs = MaskTrace.Empty)
```

用于包含/排除的交互遮罩，以及用于“作为”行为的交互遮罩。

**参数:**

- `interactWith` (`MaskTrace`)
- `interactExclude` (`MaskTrace`) = `MaskTrace.Empty`
- `interactAs` (`MaskTrace`) = `MaskTrace.Empty`

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
builder.WithInteraction(MaskTrace.Value, MaskTrace.Value, MaskTrace.Value);
```

### InteractWith

```csharp
TraceParamsBuilder InteractWith(MaskTrace flags)
```

交互掩码以包含。

**参数:**

- `flags` (`MaskTrace`)

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
builder.InteractWith(MaskTrace.Value);
```

### RemoveInteractWith

```csharp
TraceParamsBuilder RemoveInteractWith(MaskTrace flags)
```

交互掩码以包含。

**参数:**

- `flags` (`MaskTrace`)

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
builder.RemoveInteractWith(MaskTrace.Value);
```

### InteractExclude

```csharp
TraceParamsBuilder InteractExclude(MaskTrace flags)
```

Interaction mask to exclude.

**参数:**

- `flags` (`MaskTrace`)

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
var builder = TraceParamsBuilder.Create();
builder.InteractExclude(MaskTrace.Value);
```

### RemoveInteractExclude

```csharp
TraceParamsBuilder RemoveInteractExclude(MaskTrace flags)
```

Interaction mask to exclude.

**参数:**

- `flags` (`MaskTrace`)

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
var builder = TraceParamsBuilder.Create();
builder.RemoveInteractExclude(MaskTrace.Players);
```

### InteractAs

```csharp
TraceParamsBuilder InteractAs(MaskTrace flags)
```

“as”行为的交互掩码。

**参数:**

- `flags` (`MaskTrace`)

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
var builder = TraceParamsBuilder.Create().InteractAs(MaskTrace.Value);
```

### RemoveInteractAs

```csharp
TraceParamsBuilder RemoveInteractAs(MaskTrace flags)
```

“as”行为的交互掩码。

**参数:**

- `flags` (`MaskTrace`)

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
var builder = TraceParamsBuilder.Create();
builder.RemoveInteractAs(MaskTrace.Value);
```

### WithCollisionGroup

```csharp
TraceParamsBuilder WithCollisionGroup(CollisionGroup collisionGroup)
```

追踪使用的碰撞组。

**参数:**

- `collisionGroup` (`CollisionGroup`)

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
var builder = TraceParamsBuilder.Create();
builder.WithCollisionGroup(CollisionGroup.Value);
```

### WithIterateEntities

```csharp
TraceParamsBuilder WithIterateEntities(bool iterateEntities)
```

指示是否启用实体迭代以进行自定义过滤。

**参数:**

- `iterateEntities` (`bool`)

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
var builder = TraceParamsBuilder.Create().WithIterateEntities(true);
```

### HitSolid

```csharp
TraceParamsBuilder HitSolid(bool enabled = true)
```

追踪是否应报告实体命中。

**参数:**

- `enabled` (`bool`) = `true`

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
traceParamsBuilder.HitSolid(true);
```

### HitTrigger

```csharp
TraceParamsBuilder HitTrigger(bool enabled = true)
```

追踪是否应报告触发器命中。

**参数:**

- `enabled` (`bool`) = `true`

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
traceParamsBuilder.HitTrigger(true);
```

### HitSolidRequiresGenerateContacts

```csharp
TraceParamsBuilder HitSolidRequiresGenerateContacts(bool enabled = true)
```

跟踪是否应报告需要生成碰撞的命中结果。

**参数:**

- `enabled` (`bool`) = `true`

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
builder.HitSolidRequiresGenerateContacts(true);
```

### IgnoreDisabledPairs

```csharp
TraceParamsBuilder IgnoreDisabledPairs(bool enabled = true)
```

是否应忽略禁用的碰撞对。

**参数:**

- `enabled` (`bool`) = `true`

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
var builder = TraceParamsBuilder.Create();
builder.IgnoreDisabledPairs(true);
```

### IgnoreIfBothInteractWithHitboxes

```csharp
TraceParamsBuilder IgnoreIfBothInteractWithHitboxes(bool enabled = true)
```

当双方与命中框交互时，是否应忽略命中框。

**参数:**

- `enabled` (`bool`) = `true`

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
traceParamsBuilder.IgnoreIfBothInteractWithHitboxes(true);
```

### ForceHitEverything

```csharp
TraceParamsBuilder ForceHitEverything(bool enabled = true)
```

强制追踪命中所有目标。

**参数:**

- `enabled` (`bool`) = `true`

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
traceParamsBuilder.ForceHitEverything(true);
```

### IgnoreEntity

```csharp
TraceParamsBuilder IgnoreEntity(CEntityInstance entity)
```

应被追踪忽略的实体。

**参数:**

- `entity` (`CEntityInstance`)

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
traceParamsBuilder.IgnoreEntity(entity);
```

### IgnoreEntities

```csharp
TraceParamsBuilder IgnoreEntities(IEnumerable<CEntityInstance> entities)
```

应被追踪忽略的实体。

**参数:**

- `entities` (`IEnumerable\<CEntityInstance\>`)

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
builder.IgnoreEntities(entities);
```

### IgnoreOwner

```csharp
TraceParamsBuilder IgnoreOwner(CEntityInstance owner)
```

应被追踪忽略的实体拥有者。

**参数:**

- `owner` (`CEntityInstance`)

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
var builder = TraceParamsBuilder.Create().IgnoreOwner(owner);
```

### IgnoreOwners

```csharp
TraceParamsBuilder IgnoreOwners(IEnumerable<CEntityInstance> owners)
```

应被追踪忽略的实体拥有者。

**参数:**

- `owners` (`IEnumerable\<CEntityInstance\>`)

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
traceParamsBuilder.IgnoreOwners(existingOwners);
```

### WithHierarchyIds

```csharp
TraceParamsBuilder WithHierarchyIds(params ushort[] hierarchyIds)
```

可选层次结构ID，用于原生查询形状属性（最多使用2个值）。

**参数:**

- `hierarchyIds` (`params ushort[]`)

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
var builder = TraceParamsBuilder.Create();
builder.WithHierarchyIds(1, 2);
```

### WithDetailLayers

```csharp
TraceParamsBuilder WithDetailLayers(ushort includedDetailLayers, byte targetDetailLayer = 0)
```

包含原生查询形状属性所使用的细节图层和目标细节图层。

**参数:**

- `includedDetailLayers` (`ushort`)
- `targetDetailLayer` (`byte`) = `0`

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
builder.WithDetailLayers(1, 0);
```

### WithShouldHitEntity

```csharp
TraceParamsBuilder WithShouldHitEntity(Func<CEntityInstance, bool>? shouldHitEntity)
```

用于决定实体是否应被命中的可选回调。

**参数:**

- `shouldHitEntity` (`Func\<CEntityInstance, bool\>?`)

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
builder.WithShouldHitEntity(entity => entity.IsValid);
```

### Build

```csharp
TraceParams Build()
```

**返回值:** `TraceParams`

**用法示例:**
```csharp
TraceParams params = traceParamsBuilder.Build();
```

