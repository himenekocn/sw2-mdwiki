# 📋 ConvarFlags

**命名空间:** `SwiftlyS2.Shared.Convars`

**类型:** `enum`

**继承:** `ulong`

## 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `NONE` | `0UL` | 默认，无任何标志 |
| `LINKED_COMMAND` | `1UL << 0` | 允许命令回调链式调用。当命令被分发时，所有链式回调将被触发。 |
| `DEVELOPMENT_ONLY` | `1UL << 1` | 已发布产品中隐藏。如果定义了 ALLOW_DEVELOPMENT_CVARS，则该标志会自动移除。 |
| `GAMEDLL` | `1UL << 2` | 由游戏 DLL 定义。 |
| `CLIENTDLL` | `1UL << 3` | 由客户端 DLL 定义。 |
| `HIDDEN` | `1UL << 4` | 隐藏。不会出现在查找或自动完成中。类似于 DEVELOPMENTONLY，但无法通过编译移除。 |
| `PROTECTED` | `1UL << 5` | 这是一个服务器控制台变量（cvar），但我们不发送其数据，因为它可能是密码等敏感信息。若其值不为空或零，则发送1，否则发送0。 |
| `SPONLY` | `1UL << 6` | 该控制台变量无法被连接到多人游戏服务器的客户端修改。 |
| `ARCHIVE` | `1UL << 7` | 设置为使其保存到 vars.rc。 |
| `NOTIFY` | `1UL << 8` | 当发生变更时通知玩家。 |
| `USERINFO` | `1UL << 9` | 更改客户端的信息字符串 |
| `REFERENCE` | `1UL << 10` | 表示 cvar 是一个引用，通常用于获取在其他模块中注册的 cvar 引用，并且在实际 cvar 注册之前是临时的。 |
| `UNLOGGED` | `1UL << 11` | 如果这是一个 FCVAR_SERVER，且我们正在创建日志，则不要将更改记录到日志文件/控制台。 |
| `INITIAL_SETVALUE` | `1UL << 12` | 在首次为控制台变量（convar）设置值时使用，其值可以是默认值或来自游戏信息（gameinfo）的值。主要用于回调检查。 |
| `REPLICATED` | `1UL << 13` | 服务器设置在客户端强制执行。值从服务器复制到客户端。 |
| `CHEAT` | `1UL << 14` | 仅可在单人游戏/调试模式或开启 sv_cheats 时使用。 |
| `PER_USER` | `1UL << 15` | 导致为每个用户生成变体（例如，分屏时的 varname2..N）。 |
| `DEMO` | `1UL << 16` | 录制演示文件时记录此控制变量。 |
| `DONTRECORD` | `1UL << 17` | 不要在演示文件中记录此命令。 |
| `PERFORMING_CALLBACKS` | `1UL << 18` | 当cvar正在执行回调时设置；在回调期间设置的值将被排队，直到回调完成。 |
| `RELEASE` | `1UL << 19` | 只有标记为此的cvar才对客户可用。 |
| `MENUBAR_ITEM` | `1UL << 20` | 显示为菜单栏项。 |
| `COMMANDLINE_ENFORCED` | `1UL << 21` | 如果通过启动选项设置，则该值不会被 `ResetConVarsToDefaultValuesByFlag` 重置。 |
| `NOT_CONNECTED` | `1UL << 22` | Cvar无法被连接到服务器的客户端更改。 |
| `VCONSOLE_FUZZY_MATCHING` | `1UL << 23` | 在 vconsole 中启用模糊匹配。 |
| `SERVER_CAN_EXECUTE` | `1UL << 24` | 服务器被允许通过 ClientCommand/NET_StringCmd/CBaseClientState::ProcessStringCmd 在客户端上执行此命令。 |
| `CLIENT_CAN_EXECUTE` | `1UL << 25` | 分配给命令，以便客户端执行它们。 |
| `SERVER_CANNOT_QUERY` | `1UL << 26` | 如果设置了此值，则服务器不允许查询此cvar的值。 |
| `VCONSOLE_SET_FOCUS` | `1UL << 27` | vconsole 获取焦点。 |
| `CLIENTCMD_CAN_EXECUTE` | `1UL << 28` | IVEngineClient::ClientCmd 允许执行此命令。 |
| `EXECUTE_PER_TICK` | `1UL << 29` | 每帧执行。 |
| `DEFENSIVE` | `1UL << 32` | 防御性标记。 |

