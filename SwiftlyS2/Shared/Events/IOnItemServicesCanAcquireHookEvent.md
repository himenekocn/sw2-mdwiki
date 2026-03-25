# 🔌 IOnItemServicesCanAcquireHookEvent

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ItemServices` | `CCSPlayer_ItemServices` | get | 物品服务。 |
| `EconItemView` | `CEconItemView` | get | 经济物品视图。 |
| `WeaponVData` | `CCSWeaponBaseVData?` | get | 若找到该武器的 VData，则返回；否则为 null。 |
| `AcquireMethod` | `AcquireMethod` | get | 获取方法。 |
| `OriginalResult` | `AcquireResult` | get | CanAcquire 调用的原始返回结果。 |

## ⚙️ 方法

### SetAcquireResult

```csharp
void SetAcquireResult(AcquireResult result)
```

拦截并修改获取结果。这将修改获取结果，并阻止后续钩子及原始函数的执行。

**参数:**

- `result` (`AcquireResult`) - 要修改的结果。

**用法示例:**
```csharp
hookEvent.SetAcquireResult(AcquireResult.Deny);
```

