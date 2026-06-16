<a id="iswiftlycore"></a>

# 🔌 ISwiftlyCore

SwiftlyS2 框架的核心接口。

**命名空间:** `SwiftlyS2.Shared`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Event` | `IEventSubscriber` | get | 自定义事件订阅器。 |
| `Engine` | `IEngineService` | get | 获取用于执行核心引擎操作的引擎服务。 |
| `GameEvent` | `IGameEventService` | get | 游戏事件服务。 |
| `NetMessage` | `INetMessageService` | get | 网络消息服务。 |
| `Helpers` | `IHelpers` | get | 辅助服务。 |
| `GameHooks` | `IGameHooks` | get | 游戏钩子服务。 |
| `Game` | `IGameService` | get | 游戏服务。 |
| `Command` | `ICommandService` | get | Command service. |
| `ConsoleOutput` | `IConsoleOutputService` | get | 控制台输出服务。 |
| `EntitySystem` | `IEntitySystemService` | get | 实体系统服务。 |
| `ConVar` | `IConVarService` | get | Convar 服务。 |
| `Configuration` | `IPluginConfigurationService` | get | 配置服务。 |
| `GameData` | `IGameDataService` | get | 游戏数据服务。 |
| `PlayerManager` | `IPlayerManagerService` | get | 玩家管理器服务。 |
| `Memory` | `IMemoryService` | get | 内存服务。 |
| `LoggerFactory` | `ILoggerFactory` | get | 日志工厂。 |
| `Logger` | `ILogger` | get | 默认日志器。 |
| `Profiler` | `IContextedProfilerService` | get | 分析器服务。 |
| `Trace` | `ITraceManager` | get | 获取用于在游戏中控制和配置追踪操作的追踪管理器。 |
| `Scheduler` | `ISchedulerService` | get | 调度器服务。 |
| `Database` | `IDatabaseService` | get | 数据库服务。 |
| `Translation` | `ITranslationService` | get | 翻译服务。 |
| `Localizer` | `ILocalizer` | get | 本地化器. |
| `Permission` | `IPermissionManager` | get | 权限管理器。 |
| `Registrator` | `IRegistratorService` | get | 注册器服务。 |
| `MenusAPI` | `IMenuManagerAPI` | get | 菜单管理器API。 |
| `CommandLine` | `ICommandLine` | get | 命令行。 |
| `GameFileSystem` | `IGameFileSystem` | get | 游戏文件系统接口。 |
| `PluginManager` | `IPluginManager` | get | 插件管理器。 |
| `Datamap` | `IDatamapService` | get | 数据映射服务。 |
| `StringTable` | `IStringTableService` | get | 字符串表服务。 |
| `PluginPath` | `string` | get | 获取插件目录的文件路径。 |
| `CSGODirectory` | `string` | get | 获取 `game/csgo` 目录的绝对文件路径。 |
| `GameDirectory` | `string` | get | 获取游戏根目录的绝对文件路径。 |
| `PluginDataDirectory` | `string` | get | 获取插件数据目录的文件路径。此目录由框架确保存在。 |
| `IsGameThread` | `bool` | get | 检查此代码段是否在游戏线程上运行。 |

