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

- `key` (`string`) - 该接口的键。

**返回值:** `bool` - 若接口存在则为 true，否则为 false。

**用法示例:**
```csharp
bool exists = manager.HasSharedInterface("MyKey");
```

### GetSharedInterface<TInterface>

```csharp
TInterface GetSharedInterface<TInterface>(string key)
```

获取一个共享接口。

**参数:**

- `key` (`string`) - 该接口的键。

**返回值:** `TInterface` - 接口的实现。

**用法示例:**
```csharp
var myInterface = manager.GetSharedInterface<IMyService>("MyKey");
```

### TryGetSharedInterface<TInterface>

```csharp
bool TryGetSharedInterface<TInterface>(string key, [NotNullWhen(true )
```

尝试通过键获取共享接口实现。

**参数:**

- `key` (`string`) - 接口实现的键。
- `` (`[NotNullWhen(true`)

**返回值:** `bool` - 如果找到了实现，则为 <see langword="true"/>，否则为 <see langword="false"/>。

**用法示例:**
```csharp
if (manager.TryGetSharedInterface<IMyService>("MyKey", out var service)) { service.DoWork(); }
```

