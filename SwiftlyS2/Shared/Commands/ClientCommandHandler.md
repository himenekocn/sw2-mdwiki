<a id="clientcommandhandler"></a>

# 🔗 ClientCommandHandler

客户端命令钩子的处理器。

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

