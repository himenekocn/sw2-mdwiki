# 🔌 ISchemaClass

**命名空间:** `SwiftlyS2.Shared.Schemas`

**类型:** `interface`

**继承:** `INativeHandle`

## ⚙️ 方法

### As<K>

```csharp
K As<K>()
```

将此句柄转换为其他类型。

**返回值:** `K` - 转换后的句柄。

**用法示例:**
```csharp
var derivedInstance = existingSchemaClass.As<DerivedType>();
```

