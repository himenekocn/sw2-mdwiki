# 🔌 IServerSideClientBase

**命名空间:** `SwiftlyS2.Shared.Engine`

**类型:** `interface`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `IsConnected` | `bool` | - | - |
| `IsInGame` | `bool` | - | - |
| `IsSpawned` | `bool` | - | - |
| `IsActive` | `bool` | - | - |

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIDString` | `string` | get | 获取客户端的用户 ID 字符串。 |
| `Name` | `string` | get, set | 获取客户端的名称。 |
| `ClientSlot` | `int` | get | 获取客户端槽位索引。 |
| `EntityIndex` | `uint` | get | 获取与客户端关联的实体索引。 |
| `NetChannel` | `INetChannel` | get | 获取与客户端关联的网络通道。 |
| `ConnectionTypeFlags` | `byte` | get | 获取客户端的连接类型标志。 |
| `AsyncDisconnectFlags` | `byte` | get | 获取客户端的异步断开连接标志。 |
| `MarkedToKick` | `bool` | get, set | 获取或设置一个值，该值指示客户端是否被标记为将被踢出。 |
| `SignonState` | `SignonState_t` | get | 获取客户端的登录状态。 |
| `FakePlayer` | `bool` | get | 获取一个值，指示该客户端是否为假玩家（机器人）。 |
| `SendingSnapshots` | `bool` | get | 获取一个值，指示客户端当前是否正在发送快照。 |
| `UserID` | `int` | get | 获取客户端的用户 ID。 |
| `ReceivedPacket` | `bool` | get | 获取一个值，指示客户端是否已从服务器接收到数据包。 |
| `SteamID` | `ref CSteamID` | get | 获取客户端的 Steam ID。 |
| `DisconnectedSteamID` | `ref CSteamID` | get | 获取客户端断开连接时的 Steam ID。 |
| `AuthTicketSteamID` | `ref CSteamID` | get | 获取客户端的 Steam ID 身份验证票据。 |
| `FriendsID` | `ref CSteamID` | get | 获取客户端的好友 Steam ID。 |
| `IPAddress` | `ref NSAddress` | get | 获取客户端的 IP 地址。 |
| `Convars` | `KeyValues*` | get | 获取与客户端关联的控制台变量。 |
| `ConvarsChanged` | `bool` | get | 获取一个值，指示客户端的控制台变量是否已更改。 |
| `IsHLTV` | `bool` | get | 获取一个值，该值指示客户端是否通过 HLTV 连接。 |
| `SendtableCRC` | `uint` | get | 获取客户端的发送表 CRC 值。 |
| `ChallengeID` | `uint` | get | 获取客户端的挑战 ID。 |
| `SignonTick` | `int` | get | 获取客户端的签名时间戳。 |
| `DeltaTick` | `int` | get, set | 获取客户端的增量 tick。 |
| `StringTableAckTick` | `int` | get | 获取客户端的字符串表确认 tick。 |
| `Address` | `nint` | get | ServerSideClientBase 实例在内存中的原始地址。 |
| `LoadedSpawnGroups` | `ref CUtlVector\<nint\>` | get | 获取客户端已加载的生成组列表。 |
| `BaselinesSent` | `ref CBitVec16384` | get | 获取发送给客户端的基线位向量。 |
| `BaselineUsed` | `int` | get | 获取客户端使用的基线。 |
| `LoadingProgress` | `int` | get | 获取客户端的加载进度。 |
| `ForceWaitForTick` | `int` | get | 获取客户端的强制等待 Tick 值。 |
| `LowViolence` | `bool` | get | 获取一个值，指示客户端是否处于低暴力模式。 |
| `FullyAuthenticated` | `bool` | get | 获取一个值，该值指示客户端是否已完全通过身份验证。 |
| `NextMessageTime` | `float` | get | 获取客户端的下一条消息时间。 |
| `AuthenticatedTime` | `float` | get | 获取客户端的认证时间。 |
| `SnapshotInterval` | `float` | get | 获取客户端的快照间隔。 |
| `SpamCommandsCount` | `int` | get | 获取该客户端的垃圾命令数量。 |
| `NetworkStatTrace` | `ref CNetworkStatTrace` | get | 获取客户端的网络状态跟踪信息。 |
| `LastExecutedCommand` | `double` | get | 获取客户端最后一次执行命令的时间。 |
| `IsConnected` | `bool` | - | - |
| `IsInGame` | `bool` | - | - |
| `IsSpawned` | `bool` | - | - |
| `IsActive` | `bool` | - | - |
| `ShouldSendMessages` | `bool` | get | 获取一个值，该值指示客户端是否应向服务器发送消息。 |

## ⚙️ 方法

### player

```csharp
fake player( bot)
```

**参数:**

- `bot` (``)

**返回值:** `fake`

**用法示例:**
```csharp
player.FakePlayer("bot");
```

### Reconnect

```csharp
void Reconnect()
```

将客户端重新连接到服务器。

**用法示例:**
```csharp
client.Reconnect();
```

### SetRate

```csharp
void SetRate(int rate)
```

设置客户端的速率。

**参数:**

- `rate` (`int`)

**用法示例:**
```csharp
client.SetRate(64);
```

### SetUpdateRate

```csharp
void SetUpdateRate(float updateRate)
```

设置客户端的更新频率。

**参数:**

- `updateRate` (`float`)

**用法示例:**
```csharp
client.SetUpdateRate(0.1f);
```

### GetRate

```csharp
int GetRate()
```

获取客户端的当前速率。

**返回值:** `int`

**用法示例:**
```csharp
int rate = client.GetRate();
```

### ForceFullUpdate

```csharp
void ForceFullUpdate()
```

强制客户端进行完整更新。

**用法示例:**
```csharp
client.ForceFullUpdate();
```

### UpdateSendState

```csharp
void UpdateSendState()
```

更新客户端的发送状态。

**用法示例:**
```csharp
client.UpdateSendState();
```

### UpdateUserSettings

```csharp
void UpdateUserSettings()
```

更新客户端的用户设置。

**用法示例:**
```csharp
client.UpdateUserSettings();
```

### ResetUserSettings

```csharp
void ResetUserSettings()
```

重置客户端的用户设置。

**用法示例:**
```csharp
client.ResetUserSettings();
```

### FreeBaselines

```csharp
void FreeBaselines()
```

释放客户端的基线数据。

**用法示例:**
```csharp
client.FreeBaselines();
```

### MarkToKick

```csharp
void MarkToKick()
```

标记该客户端需被服务器踢出。

**用法示例:**
```csharp
player.MarkToKick();
```

### UnmarkToKick

```csharp
void UnmarkToKick()
```

取消标记该客户端，使其不会被服务器踢出。

**用法示例:**
```csharp
client.UnmarkToKick();
```

