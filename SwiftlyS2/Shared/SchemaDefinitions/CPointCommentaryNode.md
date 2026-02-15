# 🔌 CPointCommentaryNode

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseAnimGraph`

**实现接口:** `ISchemaClass\<CPointCommentaryNode\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PreCommands` | `string` | get, set | - |
| `PostCommands` | `string` | get, set | - |
| `CommentaryFile` | `string` | get, set | - |
| `ViewTarget` | `string` | get, set | - |
| `ViewTarget1` | `ref CHandle\<CBaseEntity\>` | get | - |
| `ViewTargetAngles` | `ref CHandle\<CBaseEntity\>` | get | - |
| `ViewPosition` | `string` | get, set | - |
| `ViewPosition2` | `ref CHandle\<CBaseEntity\>` | get | - |
| `ViewPositionMover` | `ref CHandle\<CBaseEntity\>` | get | - |
| `PreventMovement` | `ref bool` | get | - |
| `UnderCrosshair` | `ref bool` | get | - |
| `Unstoppable` | `ref bool` | get | - |
| `FinishedTime` | `GameTime_t` | get | - |
| `FinishOrigin` | `ref Vector` | get | - |
| `OriginalAngles` | `ref QAngle` | get | - |
| `FinishAngles` | `ref QAngle` | get | - |
| `PreventChangesWhileMoving` | `ref bool` | get | - |
| `Disabled` | `ref bool` | get | - |
| `TeleportOrigin` | `ref Vector` | get | - |
| `AbortedPlaybackAt` | `GameTime_t` | get | - |
| `OnCommentaryStarted` | `ref CEntityIOOutput` | get | - |
| `OnCommentaryStopped` | `ref CEntityIOOutput` | get | - |
| `Active` | `ref bool` | get | - |
| `StartTime` | `GameTime_t` | get | - |
| `StartTimeInCommentary` | `ref float` | get | - |
| `Title` | `string` | get, set | - |
| `Speakers` | `string` | get, set | - |
| `NodeNumber` | `ref int` | get | - |
| `NodeNumberMax` | `ref int` | get | - |
| `ListenedTo` | `ref bool` | get | - |

## ⚙️ 方法

### CommentaryFileUpdated

```csharp
void CommentaryFileUpdated()
```

### ViewPosition2Updated

```csharp
void ViewPosition2Updated()
```

### ActiveUpdated

```csharp
void ActiveUpdated()
```

### StartTimeUpdated

```csharp
void StartTimeUpdated()
```

### StartTimeInCommentaryUpdated

```csharp
void StartTimeInCommentaryUpdated()
```

### TitleUpdated

```csharp
void TitleUpdated()
```

### SpeakersUpdated

```csharp
void SpeakersUpdated()
```

### NodeNumberUpdated

```csharp
void NodeNumberUpdated()
```

### NodeNumberMaxUpdated

```csharp
void NodeNumberMaxUpdated()
```

### ListenedToUpdated

```csharp
void ListenedToUpdated()
```

