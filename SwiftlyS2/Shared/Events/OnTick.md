# 🔗 OnTick

当游戏处理完一个tick时调用。如果服务器处于休眠状态，则不会调用此方法。此回调是一个热点路径，请谨慎处理，不要执行任何昂贵的操作。

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `delegate`

**委托:**
```csharp
delegate void OnTick();
```

