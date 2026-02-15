# 🔌 CCSPlayerController

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `CBasePlayerController`

**实现接口:** `ISchemaClass\<CCSPlayerController\>`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `InGameMoneyServices` | `CCSPlayerController_InGameMoneyServices?` | get | - |
| `InventoryServices` | `CCSPlayerController_InventoryServices?` | get | - |
| `ActionTrackingServices` | `CCSPlayerController_ActionTrackingServices?` | get | - |
| `DamageServices` | `CCSPlayerController_DamageServices?` | get | - |
| `CrosshairCodes` | `string` | get, set | - |
| `ForceTeamTime` | `GameTime_t` | get | - |
| `LastJoinTeamTime` | `GameTime_t` | get, set | - |
| `Clan` | `string` | get, set | - |
| `RecentKillQueue` | `ISchemaFixedArray\<byte\>` | get | - |
| `LastHeldVoteTimer` | `IntervalTimer` | get | - |
| `LastTeamDamageWarningTime` | `GameTime_t` | get | - |
| `LastTimePlayerWasDisconnectedForPawnsRemove` | `GameTime_t` | get | - |

