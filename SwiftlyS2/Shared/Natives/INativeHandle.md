# 🔌 INativeHandle

Native handle from swiftly c++ native side, either allocated or borrowed from game.

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `IsValid` | `bool` | get | Return whether a handle is valid. Still might be dangerous for some pointer that borrowed from game instead of allocated by ourselves. |
| `Address` | `IntPtr` | get | Dangerous method to get the memory address of the object |

