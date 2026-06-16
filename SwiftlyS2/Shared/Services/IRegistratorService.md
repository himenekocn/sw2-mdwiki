<a id="iregistratorservice"></a>

# 🔌 IRegistratorService

**命名空间:** `SwiftlyS2.Shared.Services`

**类型:** `interface`

## ⚙️ 方法

### Register

```csharp
void Register(object instance)
```

注册一个包含监听器属性的对象。

**参数:**

- `instance` (`object`) - 任何包含监听器属性的对象。

**用法示例:**
```csharp
registrator.Register(listenerInstance);
```

