# 🔌 IAllocableNativeHandle

从 Swiftly C++ 本地端分配的句柄。目前我们使用本地代码来分配对象，以利用 hl2sdk 和 memoverride。TODO：不确定为此提供一个接口是否是个好主意，因为理想情况下，从用户的角度来看，这和 `INativeHandle` 不应有任何区别，因为分配和销毁应仅为内部使用，并在核心内部处理。

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `interface`

**继承:** `INativeHandle`

**实现接口:** `IDisposable`

