# 🔌 IOnWeaponServicesCanUseHookEvent

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `WeaponServices` | `CCSPlayer_WeaponServices` | get | 武器服务。 |
| `Weapon` | `CCSWeaponBase` | get | 武器。 |
| `OriginalResult` | `bool` | get | CanUse 调用的原始结果。 |

## ⚙️ 方法

### SetResult

```csharp
void SetResult(bool result)
```

拦截并修改可用性结果。这将修改可用性结果并停止后续的钩子和原始函数。

**参数:**

- `result` (`bool`) - 要修改的结果。

**用法示例:**
```csharp
hook.SetResult(true);
```

