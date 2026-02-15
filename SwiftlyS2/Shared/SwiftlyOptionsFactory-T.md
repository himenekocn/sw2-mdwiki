# 📦 SwiftlyOptionsFactory<T>

自定义选项工厂，阻止 Microsoft 的默认合并行为。配置文件值将完全替换代码默认值，而非进行合并。

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
T result = SwiftlyOptionsFactory.Create("example");
```

