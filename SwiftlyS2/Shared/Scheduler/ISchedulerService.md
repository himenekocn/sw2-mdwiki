<a id="ischedulerservice"></a>

# 🔌 ISchedulerService

**命名空间:** `SwiftlyS2.Shared.Scheduler`

**类型:** `interface`

## ⚙️ 方法

### NextTick

```csharp
void NextTick(Action task)
```

在下一个tick添加一个要执行的任务。

**参数:**

- `task` (`Action`) - 要执行的任务。

**用法示例:**
```csharp
schedulerService.NextTick(() => Console.WriteLine("Task executed on next tick"));
```

### NextTick

```csharp
void NextTick(Func<Task?> task)
```

**参数:**

- `task` (`Func\<Task?\>`)

**用法示例:**
```csharp
scheduler.NextTick(async () => { await Task.Delay(100); return null; });
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

在下一个游戏帧异步添加一个待执行的任务。

**参数:**

- `task` (`Action`) - 要执行的任务。

**返回值:** `Task`

**用法示例:**
```csharp
await scheduler.NextTickAsync(() => Console.WriteLine("Executed on next tick"));
```

### NextTickAsync

```csharp
void NextTickAsync(Func<Task?> task)
```

**参数:**

- `task` (`Func\<Task?\>`)

**用法示例:**
```csharp
scheduler.NextTickAsync(async () => await Task.CompletedTask);
```

### NextTickAsync<T>

```csharp
void NextTickAsync<T>(Func<Task<T?>> task)
```

**参数:**

- `task` (`Func\<Task\<T?\>\>`)

**用法示例:**
```csharp
schedulerService.NextTickAsync(async () => await SomeAsyncOperation());
```

### NextTickAsync<T>

```csharp
Task<T> NextTickAsync<T>(Func<T> task)
```

在下一个游戏帧异步添加一个待执行的任务。

**参数:**

- `task` (`Func\<T\>`) - 要执行的任务。

**返回值:** `Task\<T\>`

**用法示例:**
```csharp
var result = await scheduler.NextTickAsync(() => 42);
```

### NextWorldUpdate

```csharp
void NextWorldUpdate(Action task)
```

将任务添加至下一世界更新时执行。

**参数:**

- `task` (`Action`) - 要执行的任务。

**用法示例:**
```csharp
scheduler.NextWorldUpdate(() => Console.WriteLine("Task executed"));
```

### NextWorldUpdate

```csharp
void NextWorldUpdate(Func<Task?> task)
```

**参数:**

- `task` (`Func\<Task?\>`)

**用法示例:**
```csharp
scheduler.NextWorldUpdate(async () => { await Task.CompletedTask; });
```

### NextWorldUpdate<T>

```csharp
void NextWorldUpdate<T>(Func<Task<T?>> task)
```

**参数:**

- `task` (`Func\<Task\<T?\>\>`)

**用法示例:**
```csharp
scheduler.NextWorldUpdate(async () => await GetDataAsync());
```

### NextWorldUpdateAsync

```csharp
Task NextWorldUpdateAsync(Action task)
```

将任务添加到下一次世界更新中异步执行。

**参数:**

- `task` (`Action`) - 要执行的任务。

**返回值:** `Task`

**用法示例:**
```csharp
await scheduler.NextWorldUpdateAsync(() => Console.WriteLine("Updated"));
```

### NextWorldUpdateAsync

```csharp
void NextWorldUpdateAsync(Func<Task?> task)
```

**参数:**

- `task` (`Func\<Task?\>`)

**用法示例:**
```csharp
scheduler.NextWorldUpdateAsync(async () => { await Task.CompletedTask; });
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

将任务添加到下一次世界更新中异步执行。

**参数:**

- `task` (`Func\<T\>`) - 要执行的任务。

**返回值:** `Task\<T\>`

**用法示例:**
```csharp
var result = await schedulerService.NextWorldUpdateAsync(() => 42);
```

### Delay

```csharp
CancellationTokenSource Delay(int delayTick, Action task)
```

向调度器添加一个延迟任务。

**参数:**

- `delayTick` (`int`) - 计时器的延迟（以滴答数计）。
- `task` (`Action`) - 要执行的任务。

**返回值:** `CancellationTokenSource` - 一个可用于取消计时器的 CancellationTokenSource。

**用法示例:**
```csharp
schedulerService.Delay(100, () => Console.WriteLine("Task executed"));
```

### Repeat

```csharp
CancellationTokenSource Repeat(int periodTick, Action task)
```

向调度器添加一个重复任务。该任务将立即执行一次，之后每隔 periodTick 个时钟周期执行一次。

**参数:**

- `periodTick` (`int`) - 计时器的周期，以刻度为单位。
- `task` (`Action`) - 要执行的任务。

**返回值:** `CancellationTokenSource` - 一个可用于取消计时器的 CancellationTokenSource。

**用法示例:**
```csharp
var cts = schedulerService.Repeat(60, () => Console.WriteLine("Task executed"));
```

### DelayAndRepeat

```csharp
CancellationTokenSource DelayAndRepeat(int delayTick, int periodTick, Action task)
```

向调度器添加一个延迟且重复执行的任务。

**参数:**

- `delayTick` (`int`) - 计时器的延迟（以滴答数计）。
- `periodTick` (`int`) - 计时器的周期，以刻度为单位。
- `task` (`Action`) - 要执行的任务。

**返回值:** `CancellationTokenSource` - 一个可用于取消计时器的 CancellationTokenSource。

**用法示例:**
```csharp
var cts = schedulerService.DelayAndRepeat(100, 500, () => Console.WriteLine("Task executed"));
```

### DelayBySeconds

```csharp
CancellationTokenSource DelayBySeconds(float delaySeconds, Action task)
```

向调度器添加一个延迟任务。计时基于游戏刻（tick），当间隔接近1刻（约15毫秒）时，计时将变得不准确。

**参数:**

- `delaySeconds` (`float`) - 定时器的延迟时间，单位为秒。
- `task` (`Action`) - 要执行的任务。

**返回值:** `CancellationTokenSource` - 一个可用于取消计时器的 CancellationTokenSource。

**用法示例:**
```csharp
schedulerService.DelayBySeconds(1.5f, () => Console.WriteLine("Delayed task executed"));
```

### RepeatBySeconds

```csharp
CancellationTokenSource RepeatBySeconds(float periodSeconds, Action task)
```

向调度器添加一个重复执行的任务。该任务将立即执行一次，之后每隔 periodSeconds 秒执行一次。计时基于游戏刻（tick）计算，这意味着当时间间隔接近1刻（约15毫秒）时，计时将变得不精确。

**参数:**

- `periodSeconds` (`float`) - 计时器的周期（秒）。
- `task` (`Action`) - 要执行的任务。

**返回值:** `CancellationTokenSource` - 一个可用于取消计时器的 CancellationTokenSource。

**用法示例:**
```csharp
scheduler.RepeatBySeconds(1.0f, () => Console.WriteLine("Task executed"));
```

### DelayAndRepeatBySeconds

```csharp
CancellationTokenSource DelayAndRepeatBySeconds(float delaySeconds, float periodSeconds, Action task)
```

向调度器添加一个延迟且重复执行的任务。该任务的计时基于游戏刻（tick），这意味着当时间间隔接近1个游戏刻（约15毫秒）时，其准确性会降低。

**参数:**

- `delaySeconds` (`float`) - 定时器的延迟时间，单位为秒。
- `periodSeconds` (`float`) - 计时器的周期（秒）。
- `task` (`Action`) - 要执行的任务。

**返回值:** `CancellationTokenSource` - 一个可用于取消计时器的 CancellationTokenSource。

**用法示例:**
```csharp
schedulerService.DelayAndRepeatBySeconds(2.0f, 5.0f, () => Console.WriteLine("Task executed"));
```

### AddTimer

```csharp
CancellationTokenSource AddTimer(Func<ITimerContext, TimerStep> task)
```

为调度器添加一个高级计时器。

**参数:**

- `task` (`Func\<ITimerContext, TimerStep\>`) - 要执行的任务。

**返回值:** `CancellationTokenSource` - 一个可用于取消计时器的 CancellationTokenSource。

**用法示例:**
```csharp
var cts = scheduler.AddTimer(ctx => TimerStep.Continue);
```

### StopOnMapChange

```csharp
void StopOnMapChange(CancellationTokenSource cts)
```

当地图改变时停止计时器。

**参数:**

- `cts` (`CancellationTokenSource`) - 用于停止的CancellationTokenSource。

**用法示例:**
```csharp
schedulerService.StopOnMapChange(cts);
```

