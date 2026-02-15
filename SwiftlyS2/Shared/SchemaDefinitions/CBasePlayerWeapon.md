# 🔌 CBasePlayerWeapon

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CEconEntity`

**实现接口:** `ISchemaClass\<CBasePlayerWeapon\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `NextPrimaryAttackTick` | `GameTick_t` | get | - |
| `NextPrimaryAttackTickRatio` | `ref float` | get | - |
| `NextSecondaryAttackTick` | `GameTick_t` | get | - |
| `NextSecondaryAttackTickRatio` | `ref float` | get | - |
| `Clip1` | `ref int` | get | - |
| `Clip2` | `ref int` | get | - |
| `ReserveAmmo` | `ISchemaFixedArray\<int\>` | get | - |
| `OnPlayerUse` | `ref CEntityIOOutput` | get | - |

## ⚙️ 方法

### NextPrimaryAttackTickUpdated

```csharp
void NextPrimaryAttackTickUpdated()
```

### NextPrimaryAttackTickRatioUpdated

```csharp
void NextPrimaryAttackTickRatioUpdated()
```

### NextSecondaryAttackTickUpdated

```csharp
void NextSecondaryAttackTickUpdated()
```

### NextSecondaryAttackTickRatioUpdated

```csharp
void NextSecondaryAttackTickRatioUpdated()
```

### Clip1Updated

```csharp
void Clip1Updated()
```

### Clip2Updated

```csharp
void Clip2Updated()
```

### ReserveAmmoUpdated

```csharp
void ReserveAmmoUpdated()
```

