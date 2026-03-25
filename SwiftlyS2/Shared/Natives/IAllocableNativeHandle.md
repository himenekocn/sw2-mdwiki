<a id="iallocablenativehandle"></a>

# 🔌 IAllocableNativeHandle

从 Swiftly C++ 原生侧分配的句柄。目前我们使用原生方式分配对象以利用 hl2sdk 和 memoverride。TODO：不确定是否适合为此创建接口，因为理想情况下，从用户视角看此处与 `INativeHandle` 不应存在任何差异，因为对象的分配与销毁应仅限于内部使用，并在核心层内处理。

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `interface`

**继承:** `INativeHandle`

**实现接口:** `IDisposable`

