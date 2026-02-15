# 🔌 IInterfaceManager

**命名空间:** `SwiftlyS2.Shared`

**类型:** `interface`

## ⚙️ 方法

### HasSharedInterface

```csharp
bool HasSharedInterface(string key)
```

检查共享接口是否存在。

**参数:**

- `key` (`string`) - 接口的关键。

**返回值:** `bool` - 如果接口存在，则为 true；否则为 false。

**用法示例:**
```csharp
bool exists = manager.HasSharedInterface("MyKey");
```

