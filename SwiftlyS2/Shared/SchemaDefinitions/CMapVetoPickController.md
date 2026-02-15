# 🔌 CMapVetoPickController

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseEntity`

**实现接口:** `ISchemaClass\<CMapVetoPickController\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlayedIntroVcd` | `ref bool` | get | - |
| `NeedToPlayFiveSecondsRemaining` | `ref bool` | get | - |
| `DblPreMatchDraftSequenceTime` | `ref double` | get | - |
| `PreMatchDraftStateChanged` | `ref bool` | get | - |
| `DraftType` | `ref int` | get | - |
| `TeamWinningCoinToss` | `ref int` | get | - |
| `TeamWithFirstChoice` | `ISchemaFixedArray\<int\>` | get | - |
| `VoteMapIdsList` | `ISchemaFixedArray\<int\>` | get | - |
| `AccountIDs` | `ISchemaFixedArray\<int\>` | get | - |
| `MapId0` | `ISchemaFixedArray\<int\>` | get | - |
| `MapId1` | `ISchemaFixedArray\<int\>` | get | - |
| `MapId2` | `ISchemaFixedArray\<int\>` | get | - |
| `MapId3` | `ISchemaFixedArray\<int\>` | get | - |
| `MapId4` | `ISchemaFixedArray\<int\>` | get | - |
| `MapId5` | `ISchemaFixedArray\<int\>` | get | - |
| `StartingSide0` | `ISchemaFixedArray\<int\>` | get | - |
| `CurrentPhase` | `ref int` | get | - |
| `PhaseStartTick` | `ref int` | get | - |
| `PhaseDurationTicks` | `ref int` | get | - |
| `OnMapVetoed` | `SchemaUntypedField` | get | - |
| `OnMapPicked` | `SchemaUntypedField` | get | - |
| `OnSidesPicked` | `SchemaUntypedField` | get | - |
| `OnNewPhaseStarted` | `SchemaUntypedField` | get | - |
| `OnLevelTransition` | `SchemaUntypedField` | get | - |

## ⚙️ 方法

### DraftTypeUpdated

```csharp
void DraftTypeUpdated()
```

### TeamWinningCoinTossUpdated

```csharp
void TeamWinningCoinTossUpdated()
```

### TeamWithFirstChoiceUpdated

```csharp
void TeamWithFirstChoiceUpdated()
```

### VoteMapIdsListUpdated

```csharp
void VoteMapIdsListUpdated()
```

### AccountIDsUpdated

```csharp
void AccountIDsUpdated()
```

### MapId0Updated

```csharp
void MapId0Updated()
```

### MapId1Updated

```csharp
void MapId1Updated()
```

### MapId2Updated

```csharp
void MapId2Updated()
```

### MapId3Updated

```csharp
void MapId3Updated()
```

### MapId4Updated

```csharp
void MapId4Updated()
```

### MapId5Updated

```csharp
void MapId5Updated()
```

### StartingSide0Updated

```csharp
void StartingSide0Updated()
```

### CurrentPhaseUpdated

```csharp
void CurrentPhaseUpdated()
```

### PhaseStartTickUpdated

```csharp
void PhaseStartTickUpdated()
```

### PhaseDurationTicksUpdated

```csharp
void PhaseDurationTicksUpdated()
```

