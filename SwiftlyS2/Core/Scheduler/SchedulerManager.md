# 📦 SchedulerManager

**命名空间:** `SwiftlyS2.Core.Scheduler`

**类型:** `class`

## ⚙️ 方法

### OnWorldUpdate (静态)

```csharp
void OnWorldUpdate()
```

### OnTick (静态)

```csharp
void OnTick()
```

### NextTick (静态)

```csharp
void NextTick(Action task, CancellationToken ownerToken)
```

**参数:**

- `task` (`Action`)
- `ownerToken` (`CancellationToken`)

### NextWorldUpdate (静态)

```csharp
void NextWorldUpdate(Action task, CancellationToken ownerToken)
```

**参数:**

- `task` (`Action`)
- `ownerToken` (`CancellationToken`)

### AddTimer (静态)

```csharp
CancellationTokenSource AddTimer(Func<TimerContext, TimerStep> task, CancellationToken ownerToken)
```

**参数:**

- `task` (`Func\<TimerContext, TimerStep\>`)
- `ownerToken` (`CancellationToken`)

**返回值:** `CancellationTokenSource`

### NextTickAsync (静态)

```csharp
Task NextTickAsync()
```

**返回值:** `Task`

### NextWorldUpdateAsync (静态)

```csharp
Task NextWorldUpdateAsync()
```

**返回值:** `Task`

### NextTickAsync (静态)

```csharp
Task NextTickAsync(Action action)
```

**参数:**

- `action` (`Action`)

**返回值:** `Task`

### NextWorldUpdateAsync (静态)

```csharp
Task NextWorldUpdateAsync(Action action)
```

**参数:**

- `action` (`Action`)

**返回值:** `Task`

### QueueOrNow (静态)

```csharp
Task QueueOrNow(Action action)
```

**参数:**

- `action` (`Action`)

**返回值:** `Task`

