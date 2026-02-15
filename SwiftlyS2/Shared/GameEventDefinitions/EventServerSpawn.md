# 🔌 EventServerSpawn

事件 "server_spawn" 在服务器启动时发送一次

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventServerSpawn\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Hostname` | `string` | get, set | 主机名 <br/> 类型：字符串 |
| `Address` | `string` | get, set | 主机名、IP或DNS名称 <br/> 类型：字符串 |
| `Port` | `short` | get, set | 服务器端口 <br/> 类型：短整型 |
| `Game` | `string` | get, set | 游戏目录 <br/> 类型：字符串 |
| `MapName` | `string` | get, set | 映射名称 <br/> 类型：字符串 |
| `AddonName` | `string` | get, set | 插件名称 <br/> 类型：字符串 |
| `MaxPlayers` | `int` | get, set | 最大玩家数 <br/> 类型：长整型 |
| `Os` | `string` | get, set | WIN32, LINUX <br/> 类型：字符串 |
| `Dedicated` | `bool` | get, set | 如果为专用服务器 <br/> 类型：布尔值 |
| `Password` | `bool` | get, set | 如果受密码保护则为 true <br/> 类型：布尔值 |

