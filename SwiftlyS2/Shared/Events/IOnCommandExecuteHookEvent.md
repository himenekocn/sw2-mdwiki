<a id="ioncommandexecutehookevent"></a>

# 🔌 IOnCommandExecuteHookEvent

当命令被执行时调用。

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Command` | `ref CCommand` | get | 该命令。 |
| `HookMode` | `HookMode` | get | 钩子模式。 |
| `Result` | `HookResult` | get, set | 挂钩结果。只能在Pre事件中更改。 |

