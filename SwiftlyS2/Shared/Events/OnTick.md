# 🔗 OnTick

Called when game has processed a tick. Won't be called if the server is in hibernation. This callback is a hot path, be careful with it and don't do anything expensive.

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `delegate`

**委托:**
```csharp
delegate void OnTick();
```

