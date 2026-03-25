<a id="inetchannelinfo"></a>

# 🔌 INetChannelInfo

**命名空间:** `SwiftlyS2.Shared.Engine`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | get | - |
| `Address` | `string` | get | - |
| `RemoteAddress` | `NetworkAddress` | get | - |
| `Time` | `float` | get | - |
| `TimeConnected` | `float` | get | - |
| `DataRate` | `int` | get | - |
| `IsLocalHost` | `bool` | get | - |
| `IsLoopback` | `bool` | get | - |
| `IsTimingOut` | `bool` | get | - |
| `IsPlayback` | `bool` | get | - |
| `AvgLatency` | `float` | get | - |
| `EngineLatency` | `float` | get | - |
| `TimeSinceLastReceived` | `float` | get | - |
| `TimeoutSeconds` | `float` | get | - |
| `TimeUntilTimeout` | `float` | get | - |

## ⚙️ 方法

### GetAvgLoss

```csharp
float GetAvgLoss(NetworkFlow flow)
```

**参数:**

- `flow` (`NetworkFlow`)

**返回值:** `float`

**用法示例:**
```csharp
float avgLoss = netChannelInfo.GetAvgLoss(NetworkFlow.Value);
```

### GetAvgChoke

```csharp
float GetAvgChoke(NetworkFlow flow)
```

**参数:**

- `flow` (`NetworkFlow`)

**返回值:** `float`

**用法示例:**
```csharp
float avgChoke = netChannelInfo.GetAvgChoke(NetworkFlow.In);
```

### GetAvgData

```csharp
float GetAvgData(NetworkFlow flow)
```

**参数:**

- `flow` (`NetworkFlow`)

**返回值:** `float`

**用法示例:**
```csharp
float avg = netChannelInfo.GetAvgData(NetworkFlow.Value);
```

### GetAvgPacketBytes

```csharp
float GetAvgPacketBytes(NetworkFlow flow)
```

**参数:**

- `flow` (`NetworkFlow`)

**返回值:** `float`

**用法示例:**
```csharp
float avgBytes = netChannelInfo.GetAvgPacketBytes(NetworkFlow.Value);
```

### GetAvgPackets

```csharp
float GetAvgPackets(NetworkFlow flow)
```

**参数:**

- `flow` (`NetworkFlow`)

**返回值:** `float`

**用法示例:**
```csharp
float avg = netChannelInfo.GetAvgPackets(NetworkFlow.Value);
```

### GetTotalData

```csharp
ulong GetTotalData(NetworkFlow flow)
```

**参数:**

- `flow` (`NetworkFlow`)

**返回值:** `ulong`

**用法示例:**
```csharp
ulong total = netChannelInfo.GetTotalData(NetworkFlow.Value);
```

### GetTotalPackets

```csharp
int GetTotalPackets(NetworkFlow flow)
```

**参数:**

- `flow` (`NetworkFlow`)

**返回值:** `int`

**用法示例:**
```csharp
int count = netChannelInfo.GetTotalPackets(NetworkFlow.Value);
```

### GetSequenceNr

```csharp
int GetSequenceNr(NetworkFlow flow)
```

**参数:**

- `flow` (`NetworkFlow`)

**返回值:** `int`

**用法示例:**
```csharp
var seq = netChannelInfo.GetSequenceNr(NetworkFlow.Outgoing);
```

### SetInterpolationAmount

```csharp
void SetInterpolationAmount(float InterpolationAmount, float UpdateRate)
```

**参数:**

- `InterpolationAmount` (`float`)
- `UpdateRate` (`float`)

**用法示例:**
```csharp
netChannelInfo.SetInterpolationAmount(0.1f, 66.0f);
```

### SetNumPredictionErrors

```csharp
void SetNumPredictionErrors(int num)
```

**参数:**

- `num` (`int`)

**用法示例:**
```csharp
channel.SetNumPredictionErrors(5);
```

### SetShowNetMessages

```csharp
void SetShowNetMessages(bool show)
```

**参数:**

- `show` (`bool`)

**用法示例:**
```csharp
netChannelInfo.SetShowNetMessages(true);
```

