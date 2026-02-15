# 🔗 OnClientProcessUsercmds

Called when a client processes user commands. This callback is a hot path, be careful with it and don't do anything expensive.

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `delegate`

**委托:**
```csharp
delegate void OnClientProcessUsercmds(IOnClientProcessUsercmdsEvent @event);
```

**参数:**

- `@event` (`IOnClientProcessUsercmdsEvent`)

