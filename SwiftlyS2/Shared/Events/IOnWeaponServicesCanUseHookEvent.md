<a id="ionweaponservicescanusehookevent"></a>

# 🔌 IOnWeaponServicesCanUseHookEvent

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `WeaponServices` | `CCSPlayer_WeaponServices` | get | 武器服务。 |
| `Weapon` | `CCSWeaponBase` | get | 武器。 |
| `OriginalResult` | `bool` | get | CanUse调用的原始结果。 |

## ⚙️ 方法

### SetResult

```csharp
void SetResult(bool result)
```

拦截并修改可用性检查结果。这将修改可用性检查结果并阻止后续钩子和原始函数执行。

**参数:**

- `result` (`bool`) - 修改结果。

**用法示例:**
```csharp
hookEvent.SetResult(false);
```

