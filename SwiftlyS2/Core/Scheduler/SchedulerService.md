# 📦 SchedulerService

**命名空间:** `SwiftlyS2.Core.Scheduler`

**类型:** `class`

**继承:** `ISchedulerService`

**实现接口:** `IDisposable`

## ⚙️ 方法

### NextTick

```csharp
void NextTick(Action task)
```

**参数:**

- `task` (`Action`)

### NextTickAsync

```csharp
Task NextTickAsync(Action task)
```

**参数:**

- `task` (`Action`)

**返回值:** `Task`

### NextWorldUpdate

```csharp
void NextWorldUpdate(Action task)
```

**参数:**

- `task` (`Action`)

### NextWorldUpdateAsync

```csharp
Task NextWorldUpdateAsync(Action task)
```

**参数:**

- `task` (`Action`)

**返回值:** `Task`

### Delay

```csharp
CancellationTokenSource Delay(int delayTick, Action task)
```

**参数:**

- `delayTick` (`int`)
- `task` (`Action`)

**返回值:** `CancellationTokenSource`

### Repeat

```csharp
CancellationTokenSource Repeat(int periodTick, Action task)
```

**参数:**

- `periodTick` (`int`)
- `task` (`Action`)

**返回值:** `CancellationTokenSource`

### DelayAndRepeat

```csharp
CancellationTokenSource DelayAndRepeat(int delayTick, int periodTick, Action task)
```

**参数:**

- `delayTick` (`int`)
- `periodTick` (`int`)
- `task` (`Action`)

**返回值:** `CancellationTokenSource`

### DelayBySeconds

```csharp
CancellationTokenSource DelayBySeconds(float delaySeconds, Action task)
```

**参数:**

- `delaySeconds` (`float`)
- `task` (`Action`)

**返回值:** `CancellationTokenSource`

### RepeatBySeconds

```csharp
CancellationTokenSource RepeatBySeconds(float periodSeconds, Action task)
```

**参数:**

- `periodSeconds` (`float`)
- `task` (`Action`)

**返回值:** `CancellationTokenSource`

### DelayAndRepeatBySeconds

```csharp
CancellationTokenSource DelayAndRepeatBySeconds(float delaySeconds, float periodSeconds, Action task)
```

**参数:**

- `delaySeconds` (`float`)
- `periodSeconds` (`float`)
- `task` (`Action`)

**返回值:** `CancellationTokenSource`

### AddTimer

```csharp
CancellationTokenSource AddTimer(Func<ITimerContext, TimerStep> task)
```

**参数:**

- `task` (`Func\<ITimerContext, TimerStep\>`)

**返回值:** `CancellationTokenSource`

### StopOnMapChange

```csharp
void StopOnMapChange(CancellationTokenSource cts)
```

**参数:**

- `cts` (`CancellationTokenSource`)

### Dispose

```csharp
void Dispose()
```

