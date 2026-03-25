# 📦 SwiftlyOptionsFactory<T>

防止 Microsoft 默认合并行为的自定义选项工厂。配置文件中的值将完全替换代码中的默认值，而非进行合并。

**命名空间:** `SwiftlyS2.Shared`

**类型:** `class`

**继承:** `IOptionsFactory\<T\> where T : class`

**实现接口:** `new()`

## ⚙️ 方法

### Create

```csharp
T Create(string name)
```

**参数:**

- `name` (`string`)

**返回值:** `T`

**用法示例:**
```csharp
var options = swiftlyOptionsFactory.Create("MyConfig");
```

