<a id="convarflags"></a>

# 📋 ConvarFlags

**命名空间:** `SwiftlyS2.Shared.Convars`

**类型:** `enum`

**继承:** `ulong`

## 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `NONE` | `0UL` | 默认值，无任何标志位 |
| `LINKED_COMMAND` | `1UL << 0` | 允许命令回调链式调用。当命令被分发时，所有已链接的回调将被触发。 |
| `DEVELOPMENT_ONLY` | `1UL << 1` | 隐藏于已发布产品中。若定义了 ALLOW_DEVELOPMENT_CVARS，则该标志将自动移除。 |
| `GAMEDLL` | `1UL << 2` | 由游戏 DLL 定义。 |
| `CLIENTDLL` | `1UL << 3` | 由客户端 DLL 定义。 |
| `HIDDEN` | `1UL << 4` | 隐藏。不出现在查找或自动补全中。类似于 DEVELOPMENTONLY，但无法被编译移除。 |
| `PROTECTED` | `1UL << 5` | 这是一个服务器 CVar，但由于它涉及密码等敏感信息，我们不发送该数据。当值非空白/非零时发送 1，否则发送 0。 |
| `SPONLY` | `1UL << 6` | 此控制台变量无法由连接到多人游戏服务器的客户端进行更改。 |
| `ARCHIVE` | `1UL << 7` | 设置为使其保存到 vars.rc 文件。 |
| `NOTIFY` | `1UL << 8` | 在变更时通知玩家。 |
| `USERINFO` | `1UL << 9` | 更改客户端的信息字符串 |
| `REFERENCE` | `1UL << 10` | 表示该 cvar 为引用类型，通常用于获取在其他模块中注册的 cvar 的引用，且在目标 cvar 实际注册之前仅为临时状态。 |
| `UNLOGGED` | `1UL << 11` | 如果这是一个 FCVAR_SERVER 类型的变量，在创建日志时，请勿将变更记录到日志文件或控制台。 |
| `INITIAL_SETVALUE` | `1UL << 12` | 此标志用于首个 convar 的 SetValue，其值来自 default_value 或 gameinfo。主要用于回调函数进行判断。 |
| `REPLICATED` | `1UL << 13` | 服务器设置的值在客户端上强制生效。这些值从服务器向客户端进行复制同步。 |
| `CHEAT` | `1UL << 14` | 仅可在单机/调试模式或 sv_cheats 启用时使用。 |
| `PER_USER` | `1UL << 15` | 导致为每个用户变体（例如用于分屏的 varname2..N）自动生成。 |
| `DEMO` | `1UL << 16` | 在开始录制演示文件时记录此控制台变量。 |
| `DONTRECORD` | `1UL << 17` | 不要将此命令记录在演示文件中。 |
| `PERFORMING_CALLBACKS` | `1UL << 18` | 在 cvar 执行回调时设置；回调期间设置的值将在回调完成后统一生效。 |
| `RELEASE` | `1UL << 19` | 仅包含此标签的客户端变量（cvars）对客户可用。 |
| `MENUBAR_ITEM` | `1UL << 20` | 作为菜单栏项显示。 |
| `COMMANDLINE_ENFORCED` | `1UL << 21` | 如果通过启动选项设置，该值不会被 ResetConVarsToDefaultValuesByFlag 重置。 |
| `NOT_CONNECTED` | `1UL << 22` | Cvar 无法由已连接到服务器的客户端进行更改。 |
| `VCONSOLE_FUZZY_MATCHING` | `1UL << 23` | 在 vconsole 中启用模糊匹配功能。 |
| `SERVER_CAN_EXECUTE` | `1UL << 24` | 服务器可通过 ClientCommand/NET_StringCmd/CBaseClientState::ProcessStringCmd 在客户端执行此命令。 |
| `CLIENT_CAN_EXECUTE` | `1UL << 25` | 分配给命令，以便客户端可执行它们。 |
| `SERVER_CANNOT_QUERY` | `1UL << 26` | 如果设置了此选项，则服务器不允许查询该 cvar 的值。 |
| `VCONSOLE_SET_FOCUS` | `1UL << 27` | vconsole 设置焦点。 |
| `CLIENTCMD_CAN_EXECUTE` | `1UL << 28` | IVEngineClient::ClientCmd 允许执行此命令。 |
| `EXECUTE_PER_TICK` | `1UL << 29` | 每帧执行一次。 |
| `DEFENSIVE` | `1UL << 32` | 防御旗帜。 |

