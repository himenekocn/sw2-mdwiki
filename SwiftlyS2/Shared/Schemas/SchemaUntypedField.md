<a id="schemauntypedfield"></a>

# 📦 SchemaUntypedField

**命名空间:** `SwiftlyS2.Shared.Schemas`

**类型:** `class`

**继承:** `INativeHandle`

**实现接口:** `ISchemaClass\<SchemaUntypedField\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `Address` | `nint` | - | - |

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `IsValid` | `bool` | - | - |
| `Address` | `nint` | - | - |

## ⚙️ 方法

### From (静态)

```csharp
SchemaUntypedField From(nint handle)
```

**参数:**

- `handle` (`nint`)

**返回值:** `SchemaUntypedField`

**用法示例:**
```csharp
nint handle = GetNativeHandle();
var field = SchemaUntypedField.From(handle);
```

