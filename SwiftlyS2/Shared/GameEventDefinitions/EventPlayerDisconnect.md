# 🔌 EventPlayerDisconnect

事件 "player_disconnect" 客户端已断开连接

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerDisconnect\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户ID <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户ID <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 服务器上的用户ID <br/> 类型：玩家控制器 |
| `Reason` | `short` | get, set | 查看网络断开枚举 protobuf <br/> 类型：short |
| `Name` | `string` | get, set | 玩家名称 <br/> 类型：字符串 |
| `NetworkID` | `string` | get, set | 玩家网络（例如 Steam）ID <br/> 类型：字符串 |
| `XuID` | `ulong` | get, set | Steam ID <br/> 类型：uint64 |
| `PlayerID` | `short` | get, set | 类型：短整型 |

