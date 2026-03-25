# 🔌 IGameService

**命名空间:** `SwiftlyS2.Shared.Services`

**类型:** `interface`

## ⚙️ 方法

### Reset

```csharp
void Reset()
```

将所有比赛数据重置为初始状态。

**用法示例:**
```csharp
gameService.Reset();
```

### SetPhase

```csharp
void SetPhase(GamePhase phase)
```

设置当前游戏阶段。

**参数:**

- `phase` (`GamePhase`) - 要设置的比赛阶段。

**用法示例:**
```csharp
gameService.SetPhase(GamePhase.Value);
```

### AddTerroristWins

```csharp
void AddTerroristWins(int numWins)
```

向恐怖分子阵营增加胜场数。

**参数:**

- `numWins` (`int`) - 要添加的胜利次数。

**用法示例:**
```csharp
gameService.AddTerroristWins(1);
```

### AddCTWins

```csharp
void AddCTWins(int numWins)
```

将胜利场次计入反恐精英阵营。

**参数:**

- `numWins` (`int`) - 要添加的胜利次数。

**用法示例:**
```csharp
gameService.AddCTWins(5);
```

### IncrementRound

```csharp
void IncrementRound(int numRounds = 1)
```

增加回合计数。

**参数:**

- `numRounds` (`int`) = `1` - 要增加的回合数。

**用法示例:**
```csharp
gameService.IncrementRound(1);
```

### AddTerroristBonusPoints

```csharp
void AddTerroristBonusPoints(int points)
```

为恐怖分子队伍增加额外分数。

**参数:**

- `points` (`int`) - 额外加分项。

**用法示例:**
```csharp
gameService.AddTerroristBonusPoints(50);
```

### AddCTBonusPoints

```csharp
void AddCTBonusPoints(int points)
```

为反恐精英队伍添加额外分数。

**参数:**

- `points` (`int`) - 额外加分项。

**用法示例:**
```csharp
gameService.AddCTBonusPoints(5);
```

### AddTerroristScore

```csharp
void AddTerroristScore(int score)
```

向恐怖分子队伍添加分数。

**参数:**

- `score` (`int`) - 要增加的分数。

**用法示例:**
```csharp
gameService.AddTerroristScore(10);
```

### AddCTScore

```csharp
void AddCTScore(int score)
```

向反恐精英队伍添加分数。

**参数:**

- `score` (`int`) - 要增加的分数。

**用法示例:**
```csharp
gameService.AddCTScore(15);
```

### GoToOvertime

```csharp
void GoToOvertime(int numOvertimesToAdd = 1)
```

进入加时模式。

**参数:**

- `numOvertimesToAdd` (`int`) = `1` - 要添加的加时赛节数。

**用法示例:**
```csharp
gameService.GoToOvertime(2);
```

### SwapTeamScores

```csharp
void SwapTeamScores()
```

在恐怖分子与反恐精英之间交换队伍得分。

**用法示例:**
```csharp
gameService.SwapTeamScores();
```

### UpdateTeamScores

```csharp
void UpdateTeamScores()
```

**用法示例:**
```csharp
gameService.UpdateTeamScores();
```

### GetWinningTeam

```csharp
int GetWinningTeam()
```

获取获胜队伍的 ID。

**返回值:** `int` - 获胜方的队伍 ID，平局则为 0。

**用法示例:**
```csharp
int winningTeamId = gameService.GetWinningTeam();
```

