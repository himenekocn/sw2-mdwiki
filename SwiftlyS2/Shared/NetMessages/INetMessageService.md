# 🔌 INetMessageService

**命名空间:** `SwiftlyS2.Shared.NetMessages`

**类型:** `interface`

## ⚙️ 方法

### Unhook

```csharp
void Unhook(Guid guid)
```

解除网络消息处理程序的挂钩。

**参数:**

- `guid` (`Guid`) - 处理程序的唯一 Guid。

**用法示例:**
```csharp
manager.Unhook(Guid.NewGuid());
```

