# 🔌 EventServerCvar

事件“server_cvar”表明服务器控制台变量已更改

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventServerCvar\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CVarName` | `string` | get, set | cvar 名称，例如 "mp_roundtime" <br/> 类型：字符串 |
| `CVarValue` | `string` | get, set | 新的cvar值 <br/> 类型：字符串 |

