# 🔌 IOnCommandExecuteHookEvent

当命令执行时调用。

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Command` | `ref CCommand` | get | 命令。 |
| `HookMode` | `HookMode` | get | 钩子模式。 |
| `Result` | `HookResult` | get, set | 钩子结果。您只能在 Pre 事件中修改它。 |

