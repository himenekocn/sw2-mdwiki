# 🔌 CCSPlayerPawnBase

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBasePlayerPawn`

**实现接口:** `ISchemaClass\<CCSPlayerPawnBase\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CTouchExpansionComponent` | `CTouchExpansionComponent` | get | - |
| `PingServices` | `CCSPlayer_PingServices?` | get | - |
| `BlindUntilTime` | `GameTime_t` | get | - |
| `BlindStartTime` | `GameTime_t` | get | - |
| `PlayerState` | `ref CSPlayerState` | get | - |
| `Respawning` | `ref bool` | get | - |
| `HasMovedSinceSpawn` | `ref bool` | get | - |
| `NumSpawns` | `ref int` | get | - |
| `IdleTimeSinceLastAction` | `ref float` | get | - |
| `NextRadarUpdateTime` | `ref float` | get | - |
| `FlashDuration` | `ref float` | get | - |
| `FlashMaxAlpha` | `ref float` | get | - |
| `ProgressBarStartTime` | `ref float` | get | - |
| `ProgressBarDuration` | `ref int` | get | - |
| `OriginalController` | `ref CHandle\<CCSPlayerController\>` | get | - |

## ⚙️ 方法

### CTouchExpansionComponentUpdated

```csharp
void CTouchExpansionComponentUpdated()
```

### PingServicesUpdated

```csharp
void PingServicesUpdated()
```

### PlayerStateUpdated

```csharp
void PlayerStateUpdated()
```

### HasMovedSinceSpawnUpdated

```csharp
void HasMovedSinceSpawnUpdated()
```

### FlashDurationUpdated

```csharp
void FlashDurationUpdated()
```

### FlashMaxAlphaUpdated

```csharp
void FlashMaxAlphaUpdated()
```

### ProgressBarStartTimeUpdated

```csharp
void ProgressBarStartTimeUpdated()
```

### ProgressBarDurationUpdated

```csharp
void ProgressBarDurationUpdated()
```

### OriginalControllerUpdated

```csharp
void OriginalControllerUpdated()
```

