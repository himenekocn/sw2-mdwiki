# 🔌 EventInstructorServerHintStop

事件 "instructor_server_hint_stop" 销毁一个已创建的服务器/地图提示

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventInstructorServerHintStop\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `HintName` | `string` | get, set | 停止提示的指令。将停止所有具有此名称的提示 <br/> 类型：字符串 |
| `HintEntindex` | `int` | get, set | 触发事件的 env_instructor_hint 的实体 ID <br/> 类型：长整型 |

