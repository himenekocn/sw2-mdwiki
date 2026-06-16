<a id="convarflags"></a>

# 📋 ConvarFlags

**命名空间:** `SwiftlyS2.Shared.Convars`

**类型:** `enum`

**继承:** `ulong`

## 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `NONE` | `0UL` | 默认，无任何标记 |
| `LINKED_COMMAND` | `1UL << 0` | 允许命令回调链式调用。当命令被调度时，所有链式回调将被触发。 |
| `DEVELOPMENT_ONLY` | `1UL << 1` | 隐藏在发布的产品中。如果定义了ALLOW_DEVELOPMENT_CVARS，该标志会被自动移除。 |
| `GAMEDLL` | `1UL << 2` | 由游戏 DLL 定义。 |
| `CLIENTDLL` | `1UL << 3` | 由客户端DLL定义。 |
| `HIDDEN` | `1UL << 4` | 隐藏。不会出现在查找或自动补全中。类似DEVELOPMENTONLY，但无法通过编译排除。 |
| `PROTECTED` | `1UL << 5` | 它是一个服务器cvar，但由于包含密码等敏感信息，我们不发送实际数据。若非空/非零则发送1，否则发送0作为值。 |
| `SPONLY` | `1UL << 6` | 此控制台变量无法由连接到多人服务器的客户端修改。 |
| `ARCHIVE` | `1UL << 7` | 设置为保存到vars.rc。 |
| `NOTIFY` | `1UL << 8` | 当发生变化时通知玩家。 |
| `USERINFO` | `1UL << 9` | 更改客户端的信息字符串 |
| `REFERENCE` | `1UL << 10` | 表示cvar是一个引用，通常用于获取其他模块中注册的cvar的引用，并且在实际cvar注册之前是临时的。 |
| `UNLOGGED` | `1UL << 11` | 如果是 FCVAR_SERVER，在创建日志时不要将更改记录到日志文件或控制台。 |
| `INITIAL_SETVALUE` | `1UL << 12` | 用于设置第一个convar SetValue，要么使用其默认值，要么使用来自gameinfo的值。主要用于回调函数进行检查。 |
| `REPLICATED` | `1UL << 13` | 服务器强制应用于客户端的设置。值从服务器复制到客户端。 |
| `CHEAT` | `1UL << 14` | 仅可在单人/调试模式或启用了sv_cheats时使用。 |
| `PER_USER` | `1UL << 15` | 导致每个用户的变体（如用于分屏的 varname2..N）被自动生成。 |
| `DEMO` | `1UL << 16` | 录制演示文件时记录此控制台变量。 |
| `DONTRECORD` | `1UL << 17` | 不在演示文件中记录此命令。 |
| `PERFORMING_CALLBACKS` | `1UL << 18` | 在cvar执行回调时设置；回调过程中的值设置将被排队，直到回调完成。 |
| `RELEASE` | `1UL << 19` | 只有标记有此属性的控制台变量对客户可用。 |
| `MENUBAR_ITEM` | `1UL << 20` | 显示为菜单栏项。 |
| `COMMANDLINE_ENFORCED` | `1UL << 21` | 若通过启动选项设置，该值将不会被`ResetConVarsToDefaultValuesByFlag`重置。 |
| `NOT_CONNECTED` | `1UL << 22` | 连接至服务器的客户端无法更改Cvar。 |
| `VCONSOLE_FUZZY_MATCHING` | `1UL << 23` | 在vconsole中启用模糊匹配。 |
| `SERVER_CAN_EXECUTE` | `1UL << 24` | 服务器被允许通过ClientCommand/NET_StringCmd/CBaseClientState::ProcessStringCmd在客户端上执行此命令。 |
| `CLIENT_CAN_EXECUTE` | `1UL << 25` | 分配给命令以让客户端执行它们。 |
| `SERVER_CANNOT_QUERY` | `1UL << 26` | 若此项被设置，则服务器不得查询此cvar的值。 |
| `VCONSOLE_SET_FOCUS` | `1UL << 27` | vconsole 设置焦点。 |
| `CLIENTCMD_CAN_EXECUTE` | `1UL << 28` | IVEngineClient::ClientCmd 被允许执行此命令。 |
| `EXECUTE_PER_TICK` | `1UL << 29` | 每个 tick 执行。 |
| `DEFENSIVE` | `1UL << 32` | 防守标记。 |

