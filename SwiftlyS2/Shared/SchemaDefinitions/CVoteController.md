# 🔌 CVoteController

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBaseEntity`

**实现接口:** `ISchemaClass\<CVoteController\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ActiveIssueIndex` | `ref int` | get | - |
| `OnlyTeamToVote` | `ref int` | get | - |
| `VoteOptionCount` | `ISchemaFixedArray\<int\>` | get | - |
| `PotentialVotes` | `ref int` | get | - |
| `IsYesNoVote` | `ref bool` | get | - |
| `AcceptingVotesTimer` | `CountdownTimer` | get | - |
| `ExecuteCommandTimer` | `CountdownTimer` | get | - |
| `ResetVoteTimer` | `CountdownTimer` | get, set | - |
| `VotesCast` | `ISchemaFixedArray\<int\>` | get | - |
| `PlayerHoldingVote` | `ref uint` | get | - |
| `PlayerOverrideForVote` | `ref uint` | get | - |
| `HighestCountIndex` | `ref int` | get | - |
| `PotentialIssues` | `ref CUtlVector\<PointerTo\<CBaseIssue\>\>` | get | - |
| `VoteOptions` | `ref CUtlVector\<CString\>` | get | - |

## ⚙️ 方法

### ActiveIssueIndexUpdated

```csharp
void ActiveIssueIndexUpdated()
```

### OnlyTeamToVoteUpdated

```csharp
void OnlyTeamToVoteUpdated()
```

### VoteOptionCountUpdated

```csharp
void VoteOptionCountUpdated()
```

### PotentialVotesUpdated

```csharp
void PotentialVotesUpdated()
```

### IsYesNoVoteUpdated

```csharp
void IsYesNoVoteUpdated()
```

