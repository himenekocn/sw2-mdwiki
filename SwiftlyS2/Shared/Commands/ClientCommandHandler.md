# 🔗 ClientCommandHandler

The handler for the client command hook.

**命名空间:** `SwiftlyS2.Shared.Commands`

**类型:** `delegate`

**委托:**
```csharp
delegate HookResult ClientCommandHandler(int playerId, string commandLine);
```

**参数:**

- `playerId` (`int`) - The player id.
- `commandLine` (`string`) - The command line.

**返回值:** `HookResult` - Whether the command should continue to be sent.

