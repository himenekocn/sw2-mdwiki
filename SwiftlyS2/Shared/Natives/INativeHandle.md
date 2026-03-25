# 🔌 INativeHandle

来自 Swiftly C++ 原生侧的原生句柄，由游戏分配或借用。

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `IsValid` | `bool` | get | 返回句柄是否有效。对于某些借用自游戏而非由我们分配的指针，此操作仍可能存在风险。 |
| `Address` | `IntPtr` | get | 危险的用于获取对象内存地址的方法 |

