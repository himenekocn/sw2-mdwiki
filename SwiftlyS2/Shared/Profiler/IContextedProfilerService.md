<a id="icontextedprofilerservice"></a>

# 🔌 IContextedProfilerService

**命名空间:** `SwiftlyS2.Shared.Profiler`

**类型:** `interface`

## ⚙️ 方法

### StartRecording

```csharp
void StartRecording(string name)
```

开始使用指定名称录制新配置文件。

**参数:**

- `name` (`string`) - 启动配置文件的名称。

**用法示例:**
```csharp
profilerService.StartRecording("MyProfile");
```

### StopRecording

```csharp
void StopRecording(string name)
```

停止录制指定名称的配置文件。

**参数:**

- `name` (`string`) - 要停止的配置文件的名称。

**用法示例:**
```csharp
profilerService.StopRecording("MyProfile");
```

### RecordTime

```csharp
void RecordTime(string name, double duration)
```

记录给定配置文件所花费的时间。

**参数:**

- `name` (`string`) - 要记录时间的配置文件名。
- `duration` (`double`) - 录制的持续时间。

**用法示例:**
```csharp
profilerService.RecordTime("DatabaseQuery", 120.5);
```

