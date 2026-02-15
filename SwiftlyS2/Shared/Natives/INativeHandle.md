# 🔌 INativeHandle

来自 Swiftly C++ 原生端的本地句柄，该句柄由游戏分配或借用。

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `IsValid` | `bool` | get | 返回句柄是否有效。对于某些从游戏借用而非我们自己分配的指针，仍可能存在危险。 |
| `Address` | `IntPtr` | get | 获取对象内存地址的危险方法 |

