<a id="swiftlycoreinjection"></a>

# 📦 SwiftlyCoreInjection

**命名空间:** `SwiftlyS2.Shared`

**类型:** `class`

## ⚙️ 方法

### AddSwiftly (静态)

```csharp
IServiceCollection AddSwiftly(this IServiceCollection self, ISwiftlyCore core, bool addLogger = true, bool addConfiguration = true)
```

**参数:**

- `self` (`this IServiceCollection`)
- `core` (`ISwiftlyCore`)
- `addLogger` (`bool`) = `true`
- `addConfiguration` (`bool`) = `true`

**返回值:** `IServiceCollection`

**用法示例:**
```csharp
var services = SwiftlyCoreInjection.AddSwiftly(coreInstance, true, true);
```

