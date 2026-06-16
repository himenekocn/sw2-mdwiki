<a id="igameservice"></a>

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

- `phase` (`GamePhase`) - 要设置的游戏阶段。

**用法示例:**
```csharp
gameService.SetPhase(GamePhase.Value);
```

### AddTerroristWins

```csharp
void AddTerroristWins(int numWins)
```

为恐怖分子队伍增加胜利次数。

**参数:**

- `numWins` (`int`) - 要增加的胜利次数。

**用法示例:**
```csharp
gameService.AddTerroristWins(1);
```

### AddCTWins

```csharp
void AddCTWins(int numWins)
```

为反恐精英队伍增加胜利场次。

**参数:**

- `numWins` (`int`) - 要增加的胜利次数。

**用法示例:**
```csharp
gameService.AddCTWins(1);
```

### IncrementRound

```csharp
void IncrementRound(int numRounds = 1)
```

递增回合计数。

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

为恐怖分子队伍增加奖励分数。

**参数:**

- `points` (`int`) - 奖励积分待添加。

**用法示例:**
```csharp
gameService.AddTerroristBonusPoints(100);
```

### AddCTBonusPoints

```csharp
void AddCTBonusPoints(int points)
```

为反恐精英队伍增加奖励分数。

**参数:**

- `points` (`int`) - 奖励积分待添加。

**用法示例:**
```csharp
gameService.AddCTBonusPoints(10);
```

### AddTerroristScore

```csharp
void AddTerroristScore(int score)
```

为恐怖分子队伍增加分数。

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

为反恐精英队伍增加分数。

**参数:**

- `score` (`int`) - 要增加的分数。

**用法示例:**
```csharp
gameService.AddCTScore(1);
```

### GoToOvertime

```csharp
void GoToOvertime(int numOvertimesToAdd = 1)
```

进入加时模式。

**参数:**

- `numOvertimesToAdd` (`int`) = `1` - 要增加的加时赛局数。

**用法示例:**
```csharp
gameService.GoToOvertime(2);
```

### SwapTeamScores

```csharp
void SwapTeamScores()
```

交换恐怖分子与反恐精英的团队得分。

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

获取获胜队伍ID。

**返回值:** `int` - 赢家的队伍ID，若平局则为0。

**用法示例:**
```csharp
int winningTeamId = gameService.GetWinningTeam();
```

### TerminateRound

```csharp
void TerminateRound(RoundEndReason reason, float delay)
```

在可选延迟后以指定原因结束当前回合

**参数:**

- `reason` (`RoundEndReason`) - 回合结束的原因
- `delay` (`float`) - 回合结束前的延迟时间

**用法示例:**
```csharp
gameService.TerminateRound(RoundEndReason.TargetBombed, 3.0f);
```

### GoToIntermission

```csharp
void GoToIntermission(bool abortedMatch = false)
```

进入游戏的间歇阶段。

**参数:**

- `abortedMatch` (`bool`) = `false` - 指示比赛是否被中止

**用法示例:**
```csharp
gameService.GoToIntermission(false);
```

### EmitHEGrenade

```csharp
CHEGrenadeProjectile EmitHEGrenade(Vector pos, QAngle angle, Vector velocity, CBasePlayerPawn? owner)
```

**参数:**

- `pos` (`Vector`)
- `angle` (`QAngle`)
- `velocity` (`Vector`)
- `owner` (`CBasePlayerPawn?`)

**返回值:** `CHEGrenadeProjectile`

**用法示例:**
```csharp
var grenade = gameService.EmitHEGrenade(new Vector(0, 0, 100), new QAngle(0, 90, 0), new Vector(500, 0, 300), player);
```

### EmitHEGrenadeAsync

```csharp
Task<CHEGrenadeProjectile> EmitHEGrenadeAsync(Vector pos, QAngle angle, Vector velocity, CBasePlayerPawn? owner)
```

异步创建一个高爆手雷投射物。

**参数:**

- `pos` (`Vector`) - HE手榴弹弹丸将被创建的位置。
- `angle` (`QAngle`) - HE手雷弹丸生成时的角度。
- `velocity` (`Vector`) - HE手雷弹丸的速度。
- `owner` (`CBasePlayerPawn?`) - HE手榴弹抛射物的所有者。

**返回值:** `Task\<CHEGrenadeProjectile\>` - 已创建的高爆手雷投掷物。

**用法示例:**
```csharp
var grenade = await gameService.EmitHEGrenadeAsync(Vector.Zero, QAngle.Zero, Vector.Zero, player);
```

### EmitFlashbang

```csharp
CFlashbangProjectile EmitFlashbang(Vector pos, QAngle angle, Vector velocity, CBasePlayerPawn? owner)
```

**参数:**

- `pos` (`Vector`)
- `angle` (`QAngle`)
- `velocity` (`Vector`)
- `owner` (`CBasePlayerPawn?`)

**返回值:** `CFlashbangProjectile`

**用法示例:**
```csharp
var flashbang = gameService.EmitFlashbang(new Vector(0, 0, 100), new QAngle(0, 90, 0), new Vector(0, 500, 200), player);
```

### EmitFlashbangAsync

```csharp
Task<CFlashbangProjectile> EmitFlashbangAsync(Vector pos, QAngle angle, Vector velocity, CBasePlayerPawn? owner)
```

异步创建闪光弹投射物。

**参数:**

- `pos` (`Vector`) - 闪光弹投掷物将被创建的位置。
- `angle` (`QAngle`) - 闪光弹投射物将被创建的角度。
- `velocity` (`Vector`) - 闪光弹投射物的速度。
- `owner` (`CBasePlayerPawn?`) - 高爆闪光弹投射物的所有者。

**返回值:** `Task\<CFlashbangProjectile\>` - 创建的闪光弹抛射体。

**用法示例:**
```csharp
var flashbang = await gameService.EmitFlashbangAsync(new Vector(0, 0, 100), new QAngle(0, 0, 0), new Vector(100, 0, 0), player);
```

### EmitDecoy

```csharp
CDecoyProjectile EmitDecoy(Vector pos, QAngle angle, Vector velocity, CBasePlayerPawn? owner)
```

**参数:**

- `pos` (`Vector`)
- `angle` (`QAngle`)
- `velocity` (`Vector`)
- `owner` (`CBasePlayerPawn?`)

**返回值:** `CDecoyProjectile`

**用法示例:**
```csharp
var decoy = gameService.EmitDecoy(new Vector(0, 0, 0), QAngle.Zero, new Vector(100, 0, 0), player);
```

### EmitDecoyAsync

```csharp
Task<CDecoyProjectile> EmitDecoyAsync(Vector pos, QAngle angle, Vector velocity, CBasePlayerPawn? owner)
```

异步创建一个诱饵手雷投射物。

**参数:**

- `pos` (`Vector`) - 诱饵手榴弹弹丸将被创建的位置。
- `angle` (`QAngle`) - 诱饵手榴弹投射物将以该角度生成。
- `velocity` (`Vector`) - 诱饵手雷发射物的速度。
- `owner` (`CBasePlayerPawn?`) - 诱饵手雷抛射物的所有者。

**返回值:** `Task\<CDecoyProjectile\>` - 创建的诱饵手雷投射物。

**用法示例:**
```csharp
var decoy = await gameService.EmitDecoyAsync(new Vector(0, 0, 0), new QAngle(0, 0, 0), new Vector(100, 100, 100), player);
```

