# 🔌 ISchedulerService

**命名空间:** `SwiftlyS2.Shared.Scheduler`

**类型:** `interface`

## ⚙️ 方法

### NextTick

```csharp
void NextTick(Action task)
```

添加一个任务，以便在下一“tick”时执行。

**参数:**

- `task` (`Action`) - 要执行的任务。

**用法示例:**
```csharp
ISchedulerService.NextTick(() => Console.WriteLine("Next tick task"));
```

### NextTick

```csharp
void NextTick(Func<Task?> task)
```

**参数:**

- `task` (`Func\<Task?\>`)

**用法示例:**
```csharp
schedulerService.NextTick(async () => await SomeAsyncMethod());
```

### NextTick<T>

```csharp
void NextTick<T>(Func<Task<T?>> task)
```

**参数:**

- `task` (`Func\<Task\<T?\>\>`)

**用法示例:**
```csharp
scheduler.NextTick(async () => await GetResultAsync());
```

### NextTickAsync

```csharp
Task NextTickAsync(Action task)
```

添加一个任务，以便在下一个tick异步执行。

**参数:**

- `task` (`Action`) - 要执行的任务。

**返回值:** `Task`

**用法示例:**
```csharp
await schedulerService.NextTickAsync(() => Debug.Log("Next tick task"));
```

### NextTickAsync

```csharp
void NextTickAsync(Func<Task?> task)
```

**参数:**

- `task` (`Func\<Task?\>`)

**用法示例:**
```csharp
await schedulerService.NextTickAsync(async () => await SomeTaskAsync());
```

### NextTickAsync<T>

```csharp
void NextTickAsync<T>(Func<Task<T?>> task)
```

**参数:**

- `task` (`Func\<Task\<T?\>\>`)

**用法示例:**
```csharp
await scheduler.NextTickAsync(() => SomeAsyncMethod());
```

### NextTickAsync<T>

```csharp
Task<T> NextTickAsync<T>(Func<T> task)
```

添加一个任务，以便在下一个tick异步执行。

**参数:**

- `task` (`Func\<T\>`) - 要执行的任务。

**返回值:** `Task\<T\>`

**用法示例:**
```csharp
var result = await scheduler.NextTickAsync(() => CalculateSomething());
```

### NextWorldUpdate

```csharp
void NextWorldUpdate(Action task)
```

添加一个任务，以便在下一个世界更新时执行。

**参数:**

- `task` (`Action`) - 要执行的任务。

**用法示例:**
```csharp
ISchedulerService.NextWorldUpdate(() => Debug.Log("Hello World"));
```

### NextWorldUpdate

```csharp
void NextWorldUpdate(Func<Task?> task)
```

**参数:**

- `task` (`Func\<Task?\>`)

**用法示例:**
```csharp
schedulerService.NextWorldUpdate(async () => await SomeAsyncOperation());
```

### NextWorldUpdate<T>

```csharp
void NextWorldUpdate<T>(Func<Task<T?>> task)
```

**参数:**

- `task` (`Func\<Task\<T?\>\>`)

**用法示例:**
```csharp
scheduler.NextWorldUpdate(async () => await GetWorldDataAsync());
```

### NextWorldUpdateAsync

```csharp
Task NextWorldUpdateAsync(Action task)
```

将一个任务添加到下一次世界更新时异步执行。

**参数:**

- `task` (`Action`) - 要执行的任务。

**返回值:** `Task`

**用法示例:**
```csharp
await schedulerService.NextWorldUpdateAsync(() => Debug.Log("Hello World"));
```

### NextWorldUpdateAsync

```csharp
void NextWorldUpdateAsync(Func<Task?> task)
```

**参数:**

- `task` (`Func\<Task?\>`)

**用法示例:**
```csharp
await schedulerService.NextWorldUpdateAsync(async () => await SomeTaskAsync());
```

### NextWorldUpdateAsync<T>

```csharp
Task<T> NextWorldUpdateAsync<T>(Func<Task<T?>> task)
```

**参数:**

- `task` (`Func\<Task\<T?\>\>`)

**返回值:** `Task\<T\>`

**用法示例:**
```csharp
var result = await scheduler.NextWorldUpdateAsync(() => GetNextUpdateAsync());
```

### NextWorldUpdateAsync<T>

```csharp
Task<T> NextWorldUpdateAsync<T>(Func<T> task)
```

将一个任务添加到下一次世界更新时异步执行。

**参数:**

- `task` (`Func\<T\>`) - 要执行的任务。

**返回值:** `Task\<T\>`

**用法示例:**
```csharp
await scheduler.NextWorldUpdateAsync(() => ProcessWorldData());
```

### Delay

```csharp
CancellationTokenSource Delay(int delayTick, Action task)
```

向调度器添加一个延迟任务。

**参数:**

- `delayTick` (`int`) - 计时器在刻度中的延迟。
- `task` (`Action`) - 要执行的任务。

**返回值:** `CancellationTokenSource` - 一个可用于取消计时器的 CancellationTokenSource。

**用法示例:**
```csharp
schedulerService.Delay(1000, () => Console.WriteLine("Delayed task executed"));
```

### Repeat

```csharp
CancellationTokenSource Repeat(int periodTick, Action task)
```

向调度器添加一个重复任务。该任务将立即执行一次，然后每隔 periodTick 个滴答执行一次。

**参数:**

- `periodTick` (`int`) - 计时器的时间周期（以计时周期为单位）。
- `task` (`Action`) - 要执行的任务。

**返回值:** `CancellationTokenSource` - 一个可用于取消计时器的 CancellationTokenSource。

**用法示例:**
```csharp
schedulerService.Repeat(1000, () => Console.WriteLine("Task executed"));
```

### DelayAndRepeat

```csharp
CancellationTokenSource DelayAndRepeat(int delayTick, int periodTick, Action task)
```

向调度器添加一个延迟且重复的任务。

**参数:**

- `delayTick` (`int`) - 计时器在刻度中的延迟。
- `periodTick` (`int`) - 计时器的时间周期（以计时周期为单位）。
- `task` (`Action`) - 要执行的任务。

**返回值:** `CancellationTokenSource` - 一个可用于取消计时器的 CancellationTokenSource。

**用法示例:**
```csharp
schedulerService.DelayAndRepeat(1000, 2000, () => Console.WriteLine("Task executed"));
```

### DelayBySeconds

```csharp
CancellationTokenSource DelayBySeconds(float delaySeconds, Action task)
```

向调度器添加一个延迟任务。其计时基于游戏刻，这意味着当间隔接近1个游戏刻（约15毫秒）时，计时将变得不准确。

**参数:**

- `delaySeconds` (`float`) - 计时器延迟，以秒为单位。
- `task` (`Action`) - 要执行的任务。

**返回值:** `CancellationTokenSource` - 一个可用于取消计时器的 CancellationTokenSource。

**用法示例:**
```csharp
schedulerService.DelayBySeconds(2f, () => Debug.Log("Task executed"));
```

### RepeatBySeconds

```csharp
CancellationTokenSource RepeatBySeconds(float periodSeconds, Action task)
```

向调度器添加一个重复任务。该任务将立即执行一次，然后每隔 periodSeconds 秒执行一次。其计时基于游戏tick，这意味着当间隔接近1个tick（约15毫秒）时，计时将变得不准确。

**参数:**

- `periodSeconds` (`float`) - 计时器周期，以秒为单位。
- `task` (`Action`) - 要执行的任务。

**返回值:** `CancellationTokenSource` - 一个可用于取消计时器的 CancellationTokenSource。

**用法示例:**
```csharp
schedulerService.RepeatBySeconds(2f, () => Debug.Log("任务执行"));
```

### DelayAndRepeatBySeconds

```csharp
CancellationTokenSource DelayAndRepeatBySeconds(float delaySeconds, float periodSeconds, Action task)
```

向调度器添加一个延迟且重复的任务。其计时基于游戏刻，这意味着当间隔接近1个游戏刻（约15毫秒）时，计时将变得不准确。

**参数:**

- `delaySeconds` (`float`) - 计时器延迟，以秒为单位。
- `periodSeconds` (`float`) - 计时器周期，以秒为单位。
- `task` (`Action`) - 要执行的任务。

**返回值:** `CancellationTokenSource` - 一个可用于取消计时器的 CancellationTokenSource。

**用法示例:**
```csharp
schedulerService.DelayAndRepeatBySeconds(2f, 0.5f, () => Debug.Log("Repeated task"));
```

### AddTimer

```csharp
CancellationTokenSource AddTimer(Func<ITimerContext, TimerStep> task)
```

为调度器添加高级计时器。

**参数:**

- `task` (`Func\<ITimerContext, TimerStep\>`) - 要执行的任务。

**返回值:** `CancellationTokenSource` - 一个可用于取消计时器的 CancellationTokenSource。

**用法示例:**
```csharp
schedulerService.AddTimer(ctx => TimerStep.Done);
```

### StopOnMapChange

```csharp
void StopOnMapChange(CancellationTokenSource cts)
```

当地图发生变化时停止计时器。

**参数:**

- `cts` (`CancellationTokenSource`) - 用于停止的 CancellationTokenSource。

**用法示例:**
```csharp
cts?.Cancel();
```

