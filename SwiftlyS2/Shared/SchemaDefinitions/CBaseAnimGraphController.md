# 🔌 CBaseAnimGraphController

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CSkeletonAnimationController`

**实现接口:** `ISchemaClass\<CBaseAnimGraphController\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AnimationAlgorithm` | `ref AnimationAlgorithm_t` | get | - |
| `AnimGraphNetworkedVars` | `CAnimGraphNetworkedVariables` | get | - |
| `AnimGraphInstance` | `SchemaUntypedField` | get | - |
| `NextExternalGraphHandle` | `ExternalAnimGraphHandle_t` | get | - |
| `SecondarySkeletonNames` | `ref CUtlVector\<CGlobalSymbol\>` | get | - |
| `SecondarySkeletons` | `ref CUtlVector\<CHandle\<CBaseAnimGraph\>\>` | get | - |
| `SecondarySkeletonMasterCount` | `ref int` | get | - |
| `SoundSyncTime` | `ref float` | get | - |
| `ActiveIKChainMask` | `ref uint` | get | - |
| `Sequence` | `HSequence` | get | - |
| `SeqStartTime` | `GameTime_t` | get | - |
| `SeqFixedCycle` | `ref float` | get | - |
| `AnimLoopMode` | `ref AnimLoopMode_t` | get | - |
| `PlaybackRate` | `ref CNetworkedQuantizedFloat` | get | - |
| `NotifyState` | `ref SequenceFinishNotifyState_t` | get | - |
| `NetworkedAnimationInputsChanged` | `ref bool` | get | - |
| `NetworkedSequenceChanged` | `ref bool` | get | - |
| `LastUpdateSkipped` | `ref bool` | get | - |
| `SequenceFinished` | `ref bool` | get | - |
| `PrevAnimUpdateTick` | `GameTick_t` | get | - |
| `GraphDefinitionAG2` | `ref CStrongHandle\<InfoForResourceTypeCNmGraphDefinition\>` | get | - |
| `SerializedPoseRecipeAG2` | `ref CUtlVector\<byte\>` | get | - |
| `SerializePoseRecipeSizeAG2` | `ref int` | get | - |
| `SerializePoseRecipeVersionAG2` | `ref int` | get | - |
| `ServerGraphInstanceIteration` | `ref int` | get | - |
| `ServerSerializationContextIteration` | `ref int` | get | - |
| `PrimaryGraphId` | `ResourceId_t` | get | - |
| `ExternalGraphIds` | `ref CUtlVector\<ResourceId_t\>` | get | - |
| `ExternalClipIds` | `ref CUtlVector\<ResourceId_t\>` | get | - |
| `AnimGraph2Identifier` | `ref CGlobalSymbol` | get | - |
| `ExternalGraphs` | `ref CUtlVector\<ExternalAnimGraph_t\>` | get | - |

## ⚙️ 方法

### AnimationAlgorithmUpdated

```csharp
void AnimationAlgorithmUpdated()
```

### AnimGraphNetworkedVarsUpdated

```csharp
void AnimGraphNetworkedVarsUpdated()
```

### SecondarySkeletonsUpdated

```csharp
void SecondarySkeletonsUpdated()
```

### SecondarySkeletonMasterCountUpdated

```csharp
void SecondarySkeletonMasterCountUpdated()
```

### SequenceUpdated

```csharp
void SequenceUpdated()
```

### SeqStartTimeUpdated

```csharp
void SeqStartTimeUpdated()
```

### SeqFixedCycleUpdated

```csharp
void SeqFixedCycleUpdated()
```

### AnimLoopModeUpdated

```csharp
void AnimLoopModeUpdated()
```

### PlaybackRateUpdated

```csharp
void PlaybackRateUpdated()
```

### GraphDefinitionAG2Updated

```csharp
void GraphDefinitionAG2Updated()
```

### SerializedPoseRecipeAG2Updated

```csharp
void SerializedPoseRecipeAG2Updated()
```

### SerializePoseRecipeSizeAG2Updated

```csharp
void SerializePoseRecipeSizeAG2Updated()
```

### SerializePoseRecipeVersionAG2Updated

```csharp
void SerializePoseRecipeVersionAG2Updated()
```

### ServerGraphInstanceIterationUpdated

```csharp
void ServerGraphInstanceIterationUpdated()
```

### ServerSerializationContextIterationUpdated

```csharp
void ServerSerializationContextIterationUpdated()
```

### PrimaryGraphIdUpdated

```csharp
void PrimaryGraphIdUpdated()
```

### ExternalGraphIdsUpdated

```csharp
void ExternalGraphIdsUpdated()
```

### ExternalClipIdsUpdated

```csharp
void ExternalClipIdsUpdated()
```

