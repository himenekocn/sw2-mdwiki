# 🔌 IAllocableNativeHandle

Allocated handle from swiftly c++ native side. We are using native for now to allocate objects to make use of the hl2sdk and memoverride.\ TODO: Not sure if it's a good idea to have an interface for this, because ideally there shouldn't be any difference between this and the `INativeHandle` from users' perspective, as allocation and destruction should be for internal use only and handled within the core.

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `interface`

**继承:** `INativeHandle`

**实现接口:** `IDisposable`

