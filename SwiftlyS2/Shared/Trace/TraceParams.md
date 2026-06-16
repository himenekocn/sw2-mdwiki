<a id="traceparams"></a>

# 🏗️ TraceParams

形状追踪API的统一参数。此对象融合了追踪形状与过滤器设置。

**命名空间:** `SwiftlyS2.Shared.Trace`

**类型:** `struct`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Ray` | `Ray_t` | - | 用于追踪形状的光线定义。 |
| `IterateEntities` | `bool` | - | 指示是否启用实体迭代以进行自定义过滤。 |
| `ObjectQuery` | `RnQueryObjectSet` | - | 查询应包含哪些对象组。 |
| `InteractWith` | `MaskTrace` | - | 交互掩码以包含。 |
| `InteractExclude` | `MaskTrace` | - | Interaction mask to exclude. |
| `InteractAs` | `MaskTrace` | - | “as”行为的交互掩码。 |
| `Collision` | `CollisionGroup` | - | 追踪使用的碰撞组。 |
| `EntitiesToIgnore` | `List\<CEntityInstance\>` | - | 应被追踪忽略的实体。 |
| `OwnersToIgnore` | `List\<CEntityInstance\>` | - | 应被追踪忽略的实体拥有者。 |
| `HierarchyIds` | `List\<ushort\>` | - | 可选层次结构ID，用于原生查询形状属性（最多使用2个值）。 |
| `IncludedDetailLayers` | `ushort` | - | 原生查询形状属性所包含的细节层。 |
| `TargetDetailLayer` | `byte` | get | 目标细节层，由原生查询形状属性使用。 |
| `HitSolid` | `bool` | - | 追踪是否应报告实体命中。 |
| `HitSolidRequiresGenerateContacts` | `bool` | - | 跟踪是否应报告需要生成碰撞的命中结果。 |
| `HitTrigger` | `bool` | - | 追踪是否应报告触发器命中。 |
| `ShouldIgnoreDisabledPairs` | `bool` | - | 是否应忽略禁用的碰撞对。 |
| `IgnoreIfBothInteractWithHitboxes` | `bool` | - | 当双方与命中框交互时，是否应忽略命中框。 |
| `ForceHitEverything` | `bool` | - | 强制追踪命中所有目标。 |

## ⚙️ 方法

### Clone

```csharp
TraceParams Clone()
```

创建当前参数的深拷贝。

**返回值:** `TraceParams`

**用法示例:**
```csharp
var clonedParams = traceParams.Clone();
```

### DefaultLine (静态)

```csharp
TraceParams DefaultLine()
```

为大部分线迹创建合适的默认参数实例。

**返回值:** `TraceParams`

**用法示例:**
```csharp
var defaultParams = TraceParams.DefaultLine();
```

### Builder (静态)

```csharp
TraceParamsBuilder Builder()
```

创建一个新的流畅构建器。

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
var builder = TraceParams.Builder();
```

### Builder (静态)

```csharp
TraceParamsBuilder Builder(TraceParams? seed)
```

根据现有参数对象创建一个新的流式构建器。

**参数:**

- `seed` (`TraceParams?`)

**返回值:** `TraceParamsBuilder`

**用法示例:**
```csharp
var builder = TraceParams.Builder(null);
```

