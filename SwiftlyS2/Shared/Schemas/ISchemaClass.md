# 🔌 ISchemaClass

**命名空间:** `SwiftlyS2.Shared.Schemas`

**类型:** `interface`

**继承:** `INativeHandle`

## ⚙️ 方法

### As<K>

```csharp
K As<K>()
```

将此句柄转换为另一种类型。

**返回值:** `K` - 转换后的句柄。

**用法示例:**
```csharp
var schema = manager.As<ISchemaClass>();
var result = schema.As<K>();
```

