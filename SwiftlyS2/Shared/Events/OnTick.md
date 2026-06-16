<a id="ontick"></a>

# 🔗 OnTick

当游戏处理完一个tick时调用。如果服务器处于休眠状态则不会调用。此回调属于热路径，请谨慎操作，避免执行高开销任务。

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `delegate`

**委托:**
```csharp
delegate void OnTick();
```

