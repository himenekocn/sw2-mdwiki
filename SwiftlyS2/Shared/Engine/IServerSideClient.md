<a id="iserversideclient"></a>

# 🔌 IServerSideClient

**命名空间:** `SwiftlyS2.Shared.Engine`

**类型:** `interface`

**继承:** `IServerSideClientBase`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `VoiceStreams` | `CBitVec64` | get | 获取客户端的语音流位向量，指示该客户端当前订阅了哪些语音流。 |
| `VoiceProximity` | `CBitVec64` | get | 获取该客户端的语音距离位向量，指示哪些其他客户端位于该客户端的语音范围内。 |
| `LastClientCommandQuotaStart` | `float` | get | 获取上一个客户端指令配额起始时间，用于确定客户端指令配额的重置时机。此功能通常用于对客户端指令进行速率限制，以防止滥用行为。 |
| `TimeClientBecameFullyConnected` | `float` | get | 获取客户端完全连接到服务器的时间。此信息可用于确定客户端已连接时长，通常用于跟踪连接持续时间或为客户端实现基于时间的功能。 |
| `VoiceLoopback` | `bool` | get | 获取一个值，指示客户端当前是否处于语音回环模式，即客户端自身的语音正被发送回该客户端。此功能通常用于测试或调试语音通信特性。 |
| `HltvReplayDelay` | `int` | get, set | 获取或设置客户端的 HLTV 回放延迟，该参数决定 HLTV 客户端在回放事件时应延迟的时间（以秒为单位）。此功能通常用于为观看直播的观众提供缓冲时间，使其能够以略微延迟的方式查看事件，从而应对任何潜在的延迟或缓冲问题。 |
| `HltvReplayStopAt` | `int` | get | 获取 HLTV 回放中客户端应停止的帧（tick）。此参数与回放延迟结合使用，以确定回放何时结束，确保观众能够观看完整的事件回放而不会遗漏任何关键瞬间。 |
| `HltvReplayStartAt` | `int` | get | 获取客户端 HLTV 回放应开始的帧。此属性用于确定回放何时开始，使观众能够查看游戏中重大时刻（例如击杀或目标占领）之前发生的事件。 |
| `HltvReplaySlowdownBeginAt` | `int` | get | 获取 HLTV 回放慢动作应开始的时间戳。该值用于确定回放何时开始减速，以便观众能够以慢动作观看关键瞬间，从而提升分析效果和观赏体验。 |
| `HltvReplaySlowdownEndAt` | `int` | get | 获取 HLTV 回放减速应结束的 tick。此信息用于确定回放何时停止减速，使观众在慢动作观看重要时刻后能够恢复正常速度。 |
| `HltvReplaySlowdownRate` | `float` | get, set | 获取或设置客户端的 HLTV 回放减速率，该值决定了在减速期间回放应被放慢的程度。此值通常以倍数形式表示，例如 0.5 表示将回放速度放慢至一半，使观众能够以更详细的视角观察关键瞬间，同时保持整体回放的合理节奏。 |
| `HltvLastSendTick` | `int` | get | 获取客户端最后一次发出 HLTV 回放请求的时间片。此信息用于追踪客户端上次请求回放的时间，使服务器能够管理回放请求，并确保客户端不会过于频繁地请求回放，从而避免性能问题或滥用回放系统。 |
| `HltvLastReplayRequestTime` | `float` | get | 获取客户端最后一次向 HLTV 发起回放请求的时间。该信息用于追踪客户端最近一次请求回放的时间，使服务器能够管理回放请求，并确保客户端不会过于频繁地请求回放，从而避免导致性能问题或滥用回放系统。 |

