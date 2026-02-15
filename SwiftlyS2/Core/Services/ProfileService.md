# 📦 ProfileService

**命名空间:** `SwiftlyS2.Core.Services`

**类型:** `class`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `Count` | `ulong` | - | - |
| `TotalUs` | `ulong` | - | - |
| `MinUs` | `ulong` | - | - |
| `MaxUs` | `ulong` | - | - |

## ⚙️ 方法

### Enable

```csharp
void Enable()
```

### Disable

```csharp
void Disable()
```

### IsEnabled

```csharp
bool IsEnabled()
```

**返回值:** `bool`

### StartRecordingWithIdentifier

```csharp
void StartRecordingWithIdentifier(string identifier, string name)
```

**参数:**

- `identifier` (`string`)
- `name` (`string`)

### StopRecordingWithIdentifier

```csharp
void StopRecordingWithIdentifier(string identifier, string name)
```

**参数:**

- `identifier` (`string`)
- `name` (`string`)

### RecordTimeWithIdentifier

```csharp
void RecordTimeWithIdentifier(string identifier, string name, double duration)
```

**参数:**

- `identifier` (`string`)
- `name` (`string`)
- `duration` (`double`)

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

### GenerateJSONPerformance

```csharp
string GenerateJSONPerformance(string pluginId)
```

**参数:**

- `pluginId` (`string`)

**返回值:** `string`

