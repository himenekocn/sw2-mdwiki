# 🔌 CCSPlayer_ActionTrackingServices

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CPlayerPawnComponent`

**实现接口:** `ISchemaClass\<CCSPlayer_ActionTrackingServices\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `LastWeaponBeforeC4AutoSwitch` | `ref CHandle\<CBasePlayerWeapon\>` | get | - |
| `IsRescuing` | `ref bool` | get | - |
| `WeaponPurchasesThisMatch` | `WeaponPurchaseTracker_t` | get | - |
| `WeaponPurchasesThisRound` | `WeaponPurchaseTracker_t` | get | - |

## ⚙️ 方法

### IsRescuingUpdated

```csharp
void IsRescuingUpdated()
```

### WeaponPurchasesThisMatchUpdated

```csharp
void WeaponPurchasesThisMatchUpdated()
```

### WeaponPurchasesThisRoundUpdated

```csharp
void WeaponPurchasesThisRoundUpdated()
```

