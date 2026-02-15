# 📦 ContextedProfilerService

**命名空间:** `SwiftlyS2.Core.Profiler`

**类型:** `class`

**继承:** `IContextedProfilerService`

## ⚙️ 方法

### StartRecording

```csharp
void StartRecording(string name)
```

**参数:**

- `name` (`string`)

### StopRecording

```csharp
void StopRecording(string name)
```

**参数:**

- `name` (`string`)

### RecordTime

```csharp
void RecordTime(string name, double duration)
```

**参数:**

- `name` (`string`)
- `duration` (`double`)

### GeneratePerformanceTraceJson

```csharp
string GeneratePerformanceTraceJson()
```

**返回值:** `string`

