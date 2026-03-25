# 🔌 ITypedProtobuf<T>

**命名空间:** `SwiftlyS2.Shared.NetMessages`

**类型:** `interface`

**继承:** `INativeHandle where T : ITypedProtobuf\<T\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Accessor` | `IProtobufAccessor` | get | - |

## ⚙️ 方法

### Wrap (静态)

```csharp
T Wrap(nint handle, bool isManuallyAllocated)
```

**参数:**

- `handle` (`nint`)
- `isManuallyAllocated` (`bool`)

**返回值:** `T`

**注意:** 此方法是抽象方法,需要在子类中实现 (override).

