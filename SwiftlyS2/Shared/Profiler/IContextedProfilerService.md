<a id="icontextedprofilerservice"></a>

# 🔌 IContextedProfilerService

**命名空间:** `SwiftlyS2.Shared.Profiler`

**类型:** `interface`

## ⚙️ 方法

### StartRecording

```csharp
void StartRecording(string name)
```

使用给定的名称开始记录新配置档案。

**参数:**

- `name` (`string`) - 要启动的配置文件名称。

**用法示例:**
```csharp
profilerService.StartRecording("PerformanceTest");
```

### StopRecording

```csharp
void StopRecording(string name)
```

停止录制指定名称的性能分析配置文件。

**参数:**

- `name` (`string`) - 要停止的配置文件名称。

**用法示例:**
```csharp
profilerService.StopRecording("GameLoop");
```

### RecordTime

```csharp
void RecordTime(string name, double duration)
```

记录给定配置文件的耗时。

**参数:**

- `name` (`string`) - 要记录时间的配置文件名称。
- `duration` (`double`) - 录制时长。

**用法示例:**
```csharp
profiler.RecordTime("DatabaseQuery", 125.5);
```

