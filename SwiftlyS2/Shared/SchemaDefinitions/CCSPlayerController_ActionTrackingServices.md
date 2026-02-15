# 🔌 CCSPlayerController_ActionTrackingServices

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CPlayerControllerComponent`

**实现接口:** `ISchemaClass\<CCSPlayerController_ActionTrackingServices\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PerRoundStats` | `ref CUtlVector\<CSPerRoundStats_t\>` | get | - |
| `MatchStats` | `CSMatchStats_t` | get | - |
| `NumRoundKills` | `ref int` | get | - |
| `NumRoundKillsHeadshots` | `ref int` | get | - |
| `TotalRoundDamageDealt` | `ref float` | get | - |

## ⚙️ 方法

### PerRoundStatsUpdated

```csharp
void PerRoundStatsUpdated()
```

### MatchStatsUpdated

```csharp
void MatchStatsUpdated()
```

### NumRoundKillsUpdated

```csharp
void NumRoundKillsUpdated()
```

### NumRoundKillsHeadshotsUpdated

```csharp
void NumRoundKillsHeadshotsUpdated()
```

### TotalRoundDamageDealtUpdated

```csharp
void TotalRoundDamageDealtUpdated()
```

