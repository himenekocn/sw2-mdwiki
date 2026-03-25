# 🔌 IOnMovementServicesRunCommandHookEvent

当移动服务运行命令钩子被触发时调用。

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MovementServices` | `CCSPlayer_MovementServices` | get | 移动服务。 |
| `ButtonState` | `CInButtonState` | get | 按钮状态。 |
| `UserCmdPB` | `CSGOUserCmdPB` | get | 用户命令的协议缓冲区（protobuf）定义。 |

