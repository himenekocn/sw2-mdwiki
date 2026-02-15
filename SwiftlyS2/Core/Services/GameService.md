# 📦 GameService

**命名空间:** `SwiftlyS2.Core.Services`

**类型:** `class`

**继承:** `IGameService`

## ⚙️ 方法

### Reset

```csharp
void Reset()
```

### SetPhase

```csharp
void SetPhase(GamePhase phase)
```

**参数:**

- `phase` (`GamePhase`)

### AddTerroristWins

```csharp
void AddTerroristWins(int numWins)
```

**参数:**

- `numWins` (`int`)

### AddCTWins

```csharp
void AddCTWins(int numWins)
```

**参数:**

- `numWins` (`int`)

### IncrementRound

```csharp
void IncrementRound(int numRounds = 1)
```

**参数:**

- `numRounds` (`int`) = `1`

### AddTerroristBonusPoints

```csharp
void AddTerroristBonusPoints(int points)
```

**参数:**

- `points` (`int`)

### AddCTBonusPoints

```csharp
void AddCTBonusPoints(int points)
```

**参数:**

- `points` (`int`)

### AddTerroristScore

```csharp
void AddTerroristScore(int score)
```

**参数:**

- `score` (`int`)

### AddCTScore

```csharp
void AddCTScore(int score)
```

**参数:**

- `score` (`int`)

### GoToOvertime

```csharp
void GoToOvertime(int numOvertimesToAdd = 1)
```

**参数:**

- `numOvertimesToAdd` (`int`) = `1`

### SwapTeamScores

```csharp
void SwapTeamScores()
```

### GetWinningTeam

```csharp
int GetWinningTeam()
```

**返回值:** `int`

