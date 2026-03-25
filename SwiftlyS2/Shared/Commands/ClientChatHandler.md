<a id="clientchathandler"></a>

# 🔗 ClientChatHandler

客户端聊天钩子的处理器。

**命名空间:** `SwiftlyS2.Shared.Commands`

**类型:** `delegate`

**委托:**
```csharp
delegate HookResult ClientChatHandler(int playerId, string text, bool teamonly);
```

**参数:**

- `playerId` (`int`) - The player id.
- `text` (`string`) - The text.
- `teamonly` (`bool`) - Whether the text is for team only.

**返回值:** `HookResult` - Whether the text should continue to be sent.

