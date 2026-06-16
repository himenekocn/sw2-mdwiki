<a id="iallocablenativehandle"></a>

# 🔌 IAllocableNativeHandle

从Swiftly C++原生端分配到的句柄。目前我们使用原生方式来分配对象，以便利用hl2sdk和memoverride。\ TODO：不确定为此设置接口是否合适，因为从用户视角来看，这个接口与`INativeHandle`理论上不应存在差异（分配与销毁操作应仅供内部使用并由核心层处理）。

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `interface`

**继承:** `INativeHandle`

**实现接口:** `IDisposable`

