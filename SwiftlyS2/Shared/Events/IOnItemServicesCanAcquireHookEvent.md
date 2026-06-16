<a id="ionitemservicescanacquirehookevent"></a>

# 🔌 IOnItemServicesCanAcquireHookEvent

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ItemServices` | `CCSPlayer_ItemServices` | get | 物品服务。 |
| `EconItemView` | `CEconItemView` | get | 经济物品视图。 |
| `WeaponVData` | `CCSWeaponBaseVData?` | get | 如果找到武器虚拟数据则返回该数据，否则返回空值。 |
| `AcquireMethod` | `AcquireMethod` | get | 获取方法。 |
| `OriginalResult` | `AcquireResult` | get | CanAcquire调用的原始结果。 |

## ⚙️ 方法

### SetAcquireResult

```csharp
void SetAcquireResult(AcquireResult result)
```

拦截并修改获取结果。这将修改获取结果并阻止后续钩子及原始函数。

**参数:**

- `result` (`AcquireResult`) - 修改结果。

**用法示例:**
```csharp
hookEvent.SetAcquireResult(AcquireResult.Value);
```

