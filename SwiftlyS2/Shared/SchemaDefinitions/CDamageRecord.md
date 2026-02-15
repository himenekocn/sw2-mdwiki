# 🔌 CDamageRecord

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `ISchemaClass\<CDamageRecord\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlayerDamager` | `ref CHandle\<CCSPlayerPawn\>` | get | - |
| `PlayerRecipient` | `ref CHandle\<CCSPlayerPawn\>` | get | - |
| `PlayerControllerDamager` | `ref CHandle\<CCSPlayerController\>` | get | - |
| `PlayerControllerRecipient` | `ref CHandle\<CCSPlayerController\>` | get | - |
| `PlayerDamagerName` | `string` | get, set | - |
| `PlayerRecipientName` | `string` | get, set | - |
| `DamagerXuid` | `ref ulong` | get | - |
| `RecipientXuid` | `ref ulong` | get | - |
| `BulletsDamage` | `ref float` | get | - |
| `Damage` | `ref float` | get | - |
| `ActualHealthRemoved` | `ref float` | get | - |
| `NumHits` | `ref int` | get | - |
| `LastBulletUpdate` | `ref int` | get | - |
| `IsOtherEnemy` | `ref bool` | get | - |
| `KillType` | `ref EKillTypes_t` | get | - |

## ⚙️ 方法

### PlayerDamagerUpdated

```csharp
void PlayerDamagerUpdated()
```

### PlayerRecipientUpdated

```csharp
void PlayerRecipientUpdated()
```

### PlayerControllerDamagerUpdated

```csharp
void PlayerControllerDamagerUpdated()
```

### PlayerControllerRecipientUpdated

```csharp
void PlayerControllerRecipientUpdated()
```

### PlayerDamagerNameUpdated

```csharp
void PlayerDamagerNameUpdated()
```

### PlayerRecipientNameUpdated

```csharp
void PlayerRecipientNameUpdated()
```

### DamagerXuidUpdated

```csharp
void DamagerXuidUpdated()
```

### RecipientXuidUpdated

```csharp
void RecipientXuidUpdated()
```

### DamageUpdated

```csharp
void DamageUpdated()
```

### ActualHealthRemovedUpdated

```csharp
void ActualHealthRemovedUpdated()
```

### NumHitsUpdated

```csharp
void NumHitsUpdated()
```

### LastBulletUpdateUpdated

```csharp
void LastBulletUpdateUpdated()
```

### IsOtherEnemyUpdated

```csharp
void IsOtherEnemyUpdated()
```

### KillTypeUpdated

```csharp
void KillTypeUpdated()
```

