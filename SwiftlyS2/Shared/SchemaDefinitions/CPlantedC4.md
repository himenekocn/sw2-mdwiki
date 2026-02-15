# 🔌 CPlantedC4

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseAnimGraph`

**实现接口:** `ISchemaClass\<CPlantedC4\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `BombTicking` | `ref bool` | get | - |
| `C4Blow` | `GameTime_t` | get | - |
| `BombSite` | `ref int` | get | - |
| `SourceSoundscapeHash` | `ref int` | get | - |
| `AbortDetonationBecauseWorldIsFrozen` | `ref bool` | get | - |
| `AttributeManager` | `CAttributeContainer` | get | - |
| `OnBombDefused` | `ref CEntityIOOutput` | get | - |
| `OnBombBeginDefuse` | `ref CEntityIOOutput` | get | - |
| `OnBombDefuseAborted` | `ref CEntityIOOutput` | get | - |
| `CannotBeDefused` | `ref bool` | get | - |
| `EntitySpottedState` | `EntitySpottedState_t` | get | - |
| `SpotRules` | `ref int` | get | - |
| `HasExploded` | `ref bool` | get | - |
| `BombDefused` | `ref bool` | get | - |
| `TrainingPlacedByPlayer` | `ref bool` | get | - |
| `TimerLength` | `ref float` | get | - |
| `BeingDefused` | `ref bool` | get | - |
| `LastDefuseTime` | `GameTime_t` | get | - |
| `DefuseLength` | `ref float` | get | - |
| `DefuseCountDown` | `GameTime_t` | get | - |
| `BombDefuser` | `ref CHandle\<CCSPlayerPawn\>` | get | - |
| `ProgressBarTime` | `ref int` | get | - |
| `VoiceAlertFired` | `ref bool` | get | - |
| `VoiceAlertPlayed` | `ISchemaFixedArray\<bool\>` | get | - |
| `NextBotBeepTime` | `GameTime_t` | get | - |
| `CatchUpToPlayerEye` | `ref QAngle` | get | - |
| `LastSpinDetectionTime` | `GameTime_t` | get | - |

## ⚙️ 方法

### BombTickingUpdated

```csharp
void BombTickingUpdated()
```

### C4BlowUpdated

```csharp
void C4BlowUpdated()
```

### BombSiteUpdated

```csharp
void BombSiteUpdated()
```

### SourceSoundscapeHashUpdated

```csharp
void SourceSoundscapeHashUpdated()
```

### AttributeManagerUpdated

```csharp
void AttributeManagerUpdated()
```

### CannotBeDefusedUpdated

```csharp
void CannotBeDefusedUpdated()
```

### EntitySpottedStateUpdated

```csharp
void EntitySpottedStateUpdated()
```

### HasExplodedUpdated

```csharp
void HasExplodedUpdated()
```

### BombDefusedUpdated

```csharp
void BombDefusedUpdated()
```

### TimerLengthUpdated

```csharp
void TimerLengthUpdated()
```

### BeingDefusedUpdated

```csharp
void BeingDefusedUpdated()
```

### DefuseLengthUpdated

```csharp
void DefuseLengthUpdated()
```

### DefuseCountDownUpdated

```csharp
void DefuseCountDownUpdated()
```

### BombDefuserUpdated

```csharp
void BombDefuserUpdated()
```

