# 🔌 EventInstructorServerHintCreate

事件 "instructor_server_hint_create" 使用完全由服务器/地图提供的数据创建一个提示。旨在为内容尚未准备好而提示变得不必要之前的游戏测试提供平滑的提示。**不作为可发布产品的临时解决方案**

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventInstructorServerHintCreate\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 触发提示的玩家用户ID <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 触发提示的玩家用户ID <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 触发提示的玩家用户ID <br/> 类型：玩家控制器 |
| `HintEntindex` | `int` | get, set | 触发事件的 env_instructor_hint 的实体 ID <br/> 类型：长整型 |
| `HintName` | `string` | get, set | 提示的名称。用于后续再次引用（例如，使用一个终止命令来代替超时）<br/>类型：字符串 |
| `HintReplaceKey` | `string` | get, set | 类型名称，以便相同类型的消息可以相互替换 <br/> 类型：字符串 |
| `HintTarget` | `int` | get, set | 实体ID，提示应在该ID处显示 <br/> 类型：long |
| `HintActivatorUseridController` | `CCSPlayerController` | get | 激活者的玩家槽位 <br/> 类型：玩家控制器 |
| `HintActivatorUseridPawn` | `CCSPlayerPawn` | get | 激活者的玩家槽位 <br/> 类型：玩家控制器 |
| `HintActivatorUserid` | `int` | get, set | 激活者的玩家槽位 <br/> 类型：玩家控制器 |
| `HintTimeout` | `short` | get, set | 提示自动超时的时间（以秒为单位），0 表示永不超时 <br/> 类型：short |
| `HintIconOnscreen` | `string` | get, set | 当提示显示在屏幕上时使用的提示图标。例如："icon_alert_red" <br/> 类型：字符串 |
| `HintIconOffscreen` | `string` | get, set | 当提示信息超出屏幕时使用的提示图标。例如："icon_alert" <br/> 类型：字符串 |
| `HintCaption` | `string` | get, set | 提示标题。例如：“#ThisIsDangerous” <br/> 类型：字符串 |
| `HintActivatorCaption` | `string` | get, set | 仅激活器可见的提示标题，例如 "#YouPushedItGood" <br/> 类型：字符串 |
| `HintColor` | `string` | get, set | 提示颜色，格式为“r,g,b”，其中每个分量值为 0-255 <br/> 类型：字符串 |
| `HintIconOffset` | `float` | get, set | 在z轴上与实体原点偏移的提示距离 <br/> 类型：浮点数 |
| `HintRange` | `float` | get, set | 提示前被剔除的范围 <br/> 类型：浮点数 |
| `HintFlags` | `int` | get, set | 提示标志 <br/> 类型：长整型 |
| `HintBinding` | `string` | get, set | 当 use_binding 为屏幕图标时使用的绑定 <br/> 类型：字符串 |
| `HintAllowNodrawTarget` | `bool` | get, set | 如果为 false，当目标实体不可见时，提示将消失 <br/> 类型：布尔值 |
| `HintNooffscreen` | `bool` | get, set | 如果为 true，则当提示超出玩家视野范围时将不会显示 <br/> 类型：布尔值 |
| `HintForcecaption` | `bool` | get, set | 如果为 true，即使提示被遮挡，提示标题也会显示 <br/> 类型：布尔值 |
| `HintLocalPlayerOnly` | `bool` | get, set | 如果为 true，则只有本地玩家会看到提示 <br/> 类型：布尔值 |
| `HintStartSound` | `string` | get, set | 要播放的游戏音效 <br/> 类型：字符串 |
| `HintLayoutfile` | `string` | get, set | 全景布局文件路径 <br/> 类型：字符串 |
| `HintVrPanelType` | `short` | get, set | 全景面板的附件类型 <br/> 类型：short |
| `HintVrHeightOffset` | `float` | get, set | 附加面板的高度偏移量 <br/> 类型：float |
| `HintVrOffsetX` | `float` | get, set | 附加面板的偏移量 <br/> 类型：浮点数 |
| `HintVrOffsetY` | `float` | get, set | 附加面板的偏移量 <br/> 类型：浮点数 |
| `HintVrOffsetZ` | `float` | get, set | 附加面板的偏移量 <br/> 类型：浮点数 |
| `HintGamepadBinding` | `string` | get, set | 当 use_binding 为屏幕图标时使用的游戏手柄绑定 <br/> 类型：字符串 |

