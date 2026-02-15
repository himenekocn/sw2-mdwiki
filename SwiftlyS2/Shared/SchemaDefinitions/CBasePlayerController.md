# 🔌 CBasePlayerController

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseEntity`

**实现接口:** `ISchemaClass\<CBasePlayerController\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `InButtonsWhichAreToggles` | `ref ulong` | get | - |
| `TickBase` | `ref uint` | get | - |
| `Pawn` | `ref CHandle\<CBasePlayerPawn\>` | get | - |
| `KnownTeamMismatch` | `ref bool` | get | - |
| `SplitScreenSlot` | `ref uint` | get | - |
| `SplitOwner` | `ref CHandle\<CBasePlayerController\>` | get | - |
| `SplitScreenPlayers` | `ref CUtlVector\<CHandle\<CBasePlayerController\>\>` | get | - |
| `IsHLTV` | `ref bool` | get | - |
| `Connected` | `ref PlayerConnectedState` | get | - |
| `PlayerName` | `string` | get, set | - |
| `NetworkIDString` | `string` | get, set | - |
| `LerpTime` | `ref float` | get | - |
| `LagCompensation` | `ref bool` | get | - |
| `Predict` | `ref bool` | get | - |
| `IsLowViolence` | `ref bool` | get | - |
| `GamePaused` | `ref bool` | get | - |
| `IgnoreGlobalChat` | `ref ChatIgnoreType_t` | get | - |
| `LastPlayerTalkTime` | `ref float` | get | - |
| `LastEntitySteadyState` | `ref float` | get | - |
| `AvailableEntitySteadyState` | `ref int` | get | - |
| `HasAnySteadyStateEnts` | `ref bool` | get | - |
| `SteamID` | `ref ulong` | get | - |
| `NoClipEnabled` | `ref bool` | get | - |
| `DesiredFOV` | `ref uint` | get | - |

## ⚙️ 方法

### TickBaseUpdated

```csharp
void TickBaseUpdated()
```

### PawnUpdated

```csharp
void PawnUpdated()
```

### KnownTeamMismatchUpdated

```csharp
void KnownTeamMismatchUpdated()
```

### ConnectedUpdated

```csharp
void ConnectedUpdated()
```

### PlayerNameUpdated

```csharp
void PlayerNameUpdated()
```

### SteamIDUpdated

```csharp
void SteamIDUpdated()
```

### NoClipEnabledUpdated

```csharp
void NoClipEnabledUpdated()
```

### DesiredFOVUpdated

```csharp
void DesiredFOVUpdated()
```

