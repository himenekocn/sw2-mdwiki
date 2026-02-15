# 🔌 EventHltvStatus

事件 "hltv_status" 通用HLTV状态

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvStatus\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Clients` | `int` | get, set | HLTV 观众数量 <br/> 类型：长整型 |
| `Slots` | `int` | get, set | HLTV槽位数 <br/> 类型：长整型 |
| `Proxies` | `short` | get, set | HLTV代理数量 <br/> 类型：短整型 |
| `Master` | `string` | get, set | 分发主IP:端口 <br/> 类型: 字符串 |

