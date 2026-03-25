# 🔌 INetChannel

**命名空间:** `SwiftlyS2.Shared.Engine`

**类型:** `interface`

**继承:** `INetChannelInfo`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CanPacket` | `bool` | get | - |
| `IsOverflowed` | `bool` | get | - |
| `HasPendingReliableData` | `bool` | get | - |
| `IsTimedOut` | `bool` | get | - |
| `IsSuppressingTransmit` | `bool` | get | - |

## ⚙️ 方法

### SetMinDataRate

```csharp
void SetMinDataRate(int rate)
```

**参数:**

- `rate` (`int`)

**用法示例:**
```csharp
netChannel.SetMinDataRate(64);
```

### SetMaxDataRate

```csharp
void SetMaxDataRate(int rate)
```

**参数:**

- `rate` (`int`)

**用法示例:**
```csharp
channel.SetMaxDataRate(1024);
```

### SetTimeout

```csharp
void SetTimeout(float seconds, bool forceExact = false)
```

**参数:**

- `seconds` (`float`)
- `forceExact` (`bool`) = `false`

**用法示例:**
```csharp
netChannel.SetTimeout(30.5f, true);
```

### SuppressTransmit

```csharp
void SuppressTransmit(bool suppress)
```

**参数:**

- `suppress` (`bool`)

**用法示例:**
```csharp
netChannel.SuppressTransmit(true);
```

