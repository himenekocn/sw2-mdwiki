# 🔌 CCSPlayerController_InventoryServices

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CPlayerControllerComponent`

**实现接口:** `ISchemaClass\<CCSPlayerController_InventoryServices\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MusicID` | `ref ushort` | get | - |
| `Rank` | `ISchemaFixedArray\<MedalRank_t\>` | get | - |
| `PersonaDataPublicLevel` | `ref int` | get | - |
| `PersonaDataPublicCommendsLeader` | `ref int` | get | - |
| `PersonaDataPublicCommendsTeacher` | `ref int` | get | - |
| `PersonaDataPublicCommendsFriendly` | `ref int` | get | - |
| `PersonaDataXpTrailLevel` | `ref int` | get | - |
| `EquippedPlayerSprayIDs` | `ISchemaFixedArray\<uint\>` | get | - |
| `CurrentLoadoutHash` | `ref ulong` | get | - |
| `ServerAuthoritativeWeaponSlots` | `ref CUtlVector\<ServerAuthoritativeWeaponSlot_t\>` | get | - |

## ⚙️ 方法

### MusicIDUpdated

```csharp
void MusicIDUpdated()
```

### RankUpdated

```csharp
void RankUpdated()
```

### PersonaDataPublicLevelUpdated

```csharp
void PersonaDataPublicLevelUpdated()
```

### PersonaDataPublicCommendsLeaderUpdated

```csharp
void PersonaDataPublicCommendsLeaderUpdated()
```

### PersonaDataPublicCommendsTeacherUpdated

```csharp
void PersonaDataPublicCommendsTeacherUpdated()
```

### PersonaDataPublicCommendsFriendlyUpdated

```csharp
void PersonaDataPublicCommendsFriendlyUpdated()
```

### PersonaDataXpTrailLevelUpdated

```csharp
void PersonaDataXpTrailLevelUpdated()
```

### ServerAuthoritativeWeaponSlotsUpdated

```csharp
void ServerAuthoritativeWeaponSlotsUpdated()
```

