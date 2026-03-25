<a id="ischedulerservice"></a>

# 🔌 ISchedulerService

**命名空间:** `SwiftlyS2.Shared.Scheduler`

**类型:** `interface`

## ⚙️ 方法

### NextTick

```csharp
void NextTick(Action task)
```

将任务添加到下一个游戏帧执行队列中。

**参数:**

- `task` (`Action`) - 要执行的任务。

**用法示例:**
```csharp
schedulerService.NextTick(() => Console.WriteLine("Task executed next tick"));
```

### NextTick

```csharp
void NextTick(Func<Task?> task)
```

**参数:**

- `task` (`Func\<Task?\>`)

**用法示例:**
```csharp
schedulerService.NextTick(async () => await SomeAsyncOperation());
```

### NextTick<T>

```csharp
void NextTick<T>(Func<Task<T?>> task)
```

**参数:**

- `task` (`Func\<Task\<T?\>\>`)

**用法示例:**
```csharp
schedulerService.NextTick(async () => await SomeAsyncOperation());
```

### NextTickAsync

```csharp
Task NextTickAsync(Action task)
```

将任务添加到下一个帧异步执行。

**参数:**

- `task` (`Action`) - 要执行的任务。

**返回值:** `Task`

**用法示例:**
```csharp
await schedulerService.NextTickAsync(() => Console.WriteLine("Executed in next tick"));
```

### NextTickAsync

```csharp
void NextTickAsync(Func<Task?> task)
```

**参数:**

- `task` (`Func\<Task?\>`)

**用法示例:**
```csharp
await schedulerService.NextTickAsync(async () => await Task.CompletedTask);
```

### NextTickAsync<T>

```csharp
void NextTickAsync<T>(Func<Task<T?>> task)
```

**参数:**

- `task` (`Func\<Task\<T?\>\>`)

**用法示例:**
```csharp
await scheduler.NextTickAsync(async () => await GetDataAsync());
```

### NextTickAsync<T>

```csharp
Task<T> NextTickAsync<T>(Func<T> task)
```

将任务添加到下一个帧异步执行。

**参数:**

- `task` (`Func\<T\>`) - 要执行的任务。

**返回值:** `Task\<T\>`

**用法示例:**
```csharp
var result = await scheduler.NextTickAsync(() => player.Health);
```

### NextWorldUpdate

```csharp
void NextWorldUpdate(Action task)
```

将任务添加到下一次世界更新时执行。

**参数:**

- `task` (`Action`) - 要执行的任务。

**用法示例:**
```csharp
schedulerService.NextWorldUpdate(() => Console.WriteLine("Task executed on next world update"));
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
schedulerService.NextWorldUpdate(async () => await FetchDataAsync());
```

### NextWorldUpdateAsync

```csharp
Task NextWorldUpdateAsync(Action task)
```

添加一个将在下一次世界更新时异步执行的任务。

**参数:**

- `task` (`Action`) - 要执行的任务。

**返回值:** `Task`

**用法示例:**
```csharp
await schedulerService.NextWorldUpdateAsync(() => Console.WriteLine("Updated"));
```

### NextWorldUpdateAsync

```csharp
void NextWorldUpdateAsync(Func<Task?> task)
```

**参数:**

- `task` (`Func\<Task?\>`)

**用法示例:**
```csharp
await schedulerService.NextWorldUpdateAsync(async () => await Task.CompletedTask);
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
var result = await scheduler.NextWorldUpdateAsync(async () => await GetDataAsync());
```

### NextWorldUpdateAsync<T>

```csharp
Task<T> NextWorldUpdateAsync<T>(Func<T> task)
```

添加一个将在下一次世界更新时异步执行的任务。

**参数:**

- `task` (`Func\<T\>`) - 要执行的任务。

**返回值:** `Task\<T\>`

**用法示例:**
```csharp
var result = await scheduler.NextWorldUpdateAsync(() => GameState.CurrentTick);
```

### Delay

```csharp
CancellationTokenSource Delay(int delayTick, Action task)
```

将延迟任务添加到调度器中。

**参数:**

- `delayTick` (`int`) - 定时器的延迟（以刻为单位）。
- `task` (`Action`) - 要执行的任务。

**返回值:** `CancellationTokenSource` - 一个可用于取消定时器的 CancellationTokenSource。

**用法示例:**
```csharp
schedulerService.Delay(100, () => player.Kill());
```

### Repeat

```csharp
CancellationTokenSource Repeat(int periodTick, Action task)
```

向调度器添加一个重复任务。该任务将立即执行一次，随后每隔 periodTick 个时钟刻度执行一次。

**参数:**

- `periodTick` (`int`) - 计时器的周期，单位为刻。
- `task` (`Action`) - 要执行的任务。

**返回值:** `CancellationTokenSource` - 一个可用于取消定时器的 CancellationTokenSource。

**用法示例:**
```csharp
var cts = scheduler.Repeat(100, () => Console.WriteLine("Task executed"));
```

### DelayAndRepeat

```csharp
CancellationTokenSource DelayAndRepeat(int delayTick, int periodTick, Action task)
```

向调度器添加一个延迟且重复的任务。

**参数:**

- `delayTick` (`int`) - 定时器的延迟（以刻为单位）。
- `periodTick` (`int`) - 计时器的周期，单位为刻。
- `task` (`Action`) - 要执行的任务。

**返回值:** `CancellationTokenSource` - 一个可用于取消定时器的 CancellationTokenSource。

**用法示例:**
```csharp
schedulerService.DelayAndRepeat(10, 50, () => Console.WriteLine("Task executed"));
```

### DelayBySeconds

```csharp
CancellationTokenSource DelayBySeconds(float delaySeconds, Action task)
```

向调度器添加一个延迟任务。计时基于游戏帧（tick），这意味着当时间间隔接近 1 帧（约 15 毫秒）时，精度会下降。

**参数:**

- `delaySeconds` (`float`) - 定时器的延迟时间（以秒为单位）。
- `task` (`Action`) - 要执行的任务。

**返回值:** `CancellationTokenSource` - 一个可用于取消定时器的 CancellationTokenSource。

**用法示例:**
```csharp
schedulerService.DelayBySeconds(2.5f, () => player.PrintMessage("延迟任务已执行"));
```

### RepeatBySeconds

```csharp
CancellationTokenSource RepeatBySeconds(float periodSeconds, Action task)
```

向调度器添加一个重复任务。该任务将立即执行一次，随后每隔 periodSeconds 秒执行一次。计时基于游戏帧（tick），因此当事件间隔接近 1 帧（约 15 毫秒）时，精度会下降。

**参数:**

- `periodSeconds` (`float`) - 计时器的周期，单位为秒。
- `task` (`Action`) - 要执行的任务。

**返回值:** `CancellationTokenSource` - 一个可用于取消定时器的 CancellationTokenSource。

**用法示例:**
```csharp
scheduler.RepeatBySeconds(5.0f, () => Log("Task executed"));
```

### DelayAndRepeatBySeconds

```csharp
CancellationTokenSource DelayAndRepeatBySeconds(float delaySeconds, float periodSeconds, Action task)
```

向调度器添加一个延迟并重复执行的任务。该计时基于游戏帧（tick），这意味着当时间间隔接近 1 帧（约 15 毫秒）时，计时将变得不准确。

**参数:**

- `delaySeconds` (`float`) - 定时器的延迟时间（以秒为单位）。
- `periodSeconds` (`float`) - 计时器的周期，单位为秒。
- `task` (`Action`) - 要执行的任务。

**返回值:** `CancellationTokenSource` - 一个可用于取消定时器的 CancellationTokenSource。

**用法示例:**
```csharp
var cts = scheduler.DelayAndRepeatBySeconds(2.0f, 5.0f, () => Console.WriteLine("Task executed"));
```

### AddTimer

```csharp
CancellationTokenSource AddTimer(Func<ITimerContext, TimerStep> task)
```

向调度器添加一个高级计时器。

**参数:**

- `task` (`Func\<ITimerContext, TimerStep\>`) - 要执行的任务。

**返回值:** `CancellationTokenSource` - 一个可用于取消定时器的 CancellationTokenSource。

**用法示例:**
```csharp
CancellationTokenSource cts = scheduler.AddTimer(ctx => TimerStep.Continue);
```

### StopOnMapChange

```csharp
void StopOnMapChange(CancellationTokenSource cts)
```

在地图切换时停止计时器。

**参数:**

- `cts` (`CancellationTokenSource`) - 要停止的 CancellationTokenSource。

**用法示例:**
```csharp
schedulerService.StopOnMapChange(cts);
```

