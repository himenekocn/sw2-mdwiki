# 🔗 OnClientProcessUsercmds

当客户端处理用户命令时调用。此回调是热点路径，请谨慎处理，不要执行任何昂贵的操作。

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `delegate`

**委托:**
```csharp
delegate void OnClientProcessUsercmds(IOnClientProcessUsercmdsEvent @event);
```

**参数:**

- `@event` (`IOnClientProcessUsercmdsEvent`)

