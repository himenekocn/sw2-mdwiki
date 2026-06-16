<a id="swiftlyoptionsfactory-t"></a>

# 📦 SwiftlyOptionsFactory&lt;T&gt;

自定义选项工厂，阻止微软默认合并行为。配置文件值完全替代代码默认值，而非合并。

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
var option = factory.Create("MyOption");
```

