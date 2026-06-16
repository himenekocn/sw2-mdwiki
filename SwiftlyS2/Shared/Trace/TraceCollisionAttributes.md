<a id="tracecollisionattributes"></a>

# 🏗️ TraceCollisionAttributes

**命名空间:** `SwiftlyS2.Shared.Trace`

**类型:** `struct`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `InteractsAs` | `ulong` | get, set | 定义该对象在碰撞期间作为交互对象的表面或实体类型的交互层遮罩。 |
| `InteractsWith` | `ulong` | get, set | 定义此对象在碰撞过程中与之交互的表面或实体类型的交互层遮罩。 |
| `InteractsExclude` | `ulong` | get, set | 交互层级遮罩，用于定义此对象在碰撞期间排除交互的表面或实体类型。 |
| `EntityId` | `uint` | get, set | 与该碰撞属性关联的实体ID。 |
| `OwnerId` | `uint` | get, set | 与此碰撞属性关联的所有者实体ID。通常为拥有或创建此对象的实体ID。 |
| `HierarchyId` | `ushort` | get, set | 与此碰撞属性关联的层级ID。 |
| `DetailLayerMask` | `ushort` | get, set | 定义哪些细节层包含在碰撞检测中的细节层遮罩。 |
| `DetailLayerMaskType` | `byte` | get, set | 使用的细节层遮罩类型。 |
| `TargetDetailLayer` | `byte` | get, set | 用于碰撞检测的目标细节层。 |
| `CollisionGroup` | `CollisionGroup` | get, set | 定义这些属性碰撞行为的碰撞组。 |
| `CollisionFunctionMask` | `CollisionFunctionMask_t` | get, set | 确定哪些碰撞函数适用的碰撞函数掩码。 |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

