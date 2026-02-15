# 🔌 CPlayer_WeaponServices

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CPlayerPawnComponent`

**实现接口:** `ISchemaClass\<CPlayer_WeaponServices\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MyWeapons` | `ref CUtlVector\<CHandle\<CBasePlayerWeapon\>\>` | get | - |
| `ActiveWeapon` | `ref CHandle\<CBasePlayerWeapon\>` | get | - |
| `LastWeapon` | `ref CHandle\<CBasePlayerWeapon\>` | get | - |
| `Ammo` | `ISchemaFixedArray\<ushort\>` | get | - |
| `PreventWeaponPickup` | `ref bool` | get | - |

## ⚙️ 方法

### MyWeaponsUpdated

```csharp
void MyWeaponsUpdated()
```

### ActiveWeaponUpdated

```csharp
void ActiveWeaponUpdated()
```

### LastWeaponUpdated

```csharp
void LastWeaponUpdated()
```

### AmmoUpdated

```csharp
void AmmoUpdated()
```

