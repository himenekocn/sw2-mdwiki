<a id="ischemaclass-t"></a>

# 🔌 ISchemaClass&lt;T&gt;

**命名空间:** `SwiftlyS2.Shared.Schemas`

**类型:** `interface`

**继承:** `ISchemaField`

**实现接口:** `ISchemaClass`, `INativeHandle where T : ISchemaClass\<T\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Size` | `int` | get | - |
| `ClassName` | `string?` | get | - |

## ⚙️ 方法

### From (静态)

```csharp
T From(nint handle)
```

**参数:**

- `handle` (`nint`)

**返回值:** `T`

**注意:** 此方法是抽象方法,需要在子类中实现 (override).

