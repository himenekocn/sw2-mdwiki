# 🔗 OnTick

在游戏处理完一个 tick 后被调用。如果服务器处于休眠状态，则不会调用此回调。此回调属于热路径，请谨慎使用，切勿执行任何耗时操作。

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `delegate`

**委托:**
```csharp
delegate void OnTick();
```

