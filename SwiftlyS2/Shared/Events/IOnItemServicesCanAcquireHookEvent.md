# 🔌 IOnItemServicesCanAcquireHookEvent

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ItemServices` | `CCSPlayer_ItemServices` | get | 项目服务。 |
| `EconItemView` | `CEconItemView` | get | 经济物品视图。 |
| `WeaponVData` | `CCSWeaponBaseVData?` | get | 如果找到，则为武器 vdata，否则为 null。 |
| `AcquireMethod` | `AcquireMethod` | get | 获取方法。 |
| `OriginalResult` | `AcquireResult` | get | CanAcquire 调用的原始结果。 |

## ⚙️ 方法

### SetAcquireResult

```csharp
void SetAcquireResult(AcquireResult result)
```

拦截并修改获取结果。这将修改获取结果并停止后续的钩子和原始函数。

**参数:**

- `result` (`AcquireResult`) - 要修改的结果。

**用法示例:**
```csharp
hook.SetAcquireResult(AcquireResult.Success);
```

