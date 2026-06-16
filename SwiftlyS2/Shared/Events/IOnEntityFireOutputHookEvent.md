<a id="ionentityfireoutputhookevent"></a>

# 🔌 IOnEntityFireOutputHookEvent

当实体标识触发输出时调用。

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityIO` | `ref CEntityIOOutput` | get | 实体实例。 |
| `DesignerName` | `string` | get | 调用者的设计器名称。 |
| `OutputName` | `string` | get | 正在接受的输入名称。 |
| `Activator` | `CEntityInstance?` | get | 正在接受的输入值。 |
| `Caller` | `CEntityInstance?` | get | 输入的调用者被接受。 |
| `VariantValue` | `ref CVariant\<CVariantDefaultAllocator\>` | get | 正在接受输入的变量值。 |
| `Delay` | `float` | get | 此 IO 事件的延迟（以秒为单位）。 |
| `Result` | `HookResult` | get, set | 钩子的结果。 |

