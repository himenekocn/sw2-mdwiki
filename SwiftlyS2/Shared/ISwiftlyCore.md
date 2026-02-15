# 🔌 ISwiftlyCore

SwiftlyS2 框架的核心接口。

**命名空间:** `SwiftlyS2.Shared`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Event` | `IEventSubscriber` | get | 自定义事件订阅者。 |
| `Engine` | `IEngineService` | get | 获取用于执行核心引擎操作的引擎服务。 |
| `GameEvent` | `IGameEventService` | get | 游戏事件服务。 |
| `NetMessage` | `INetMessageService` | get | 网络消息服务。 |
| `Helpers` | `IHelpers` | get | 辅助服务。 |
| `Game` | `IGameService` | get | 游戏服务。 |
| `Command` | `ICommandService` | get | 命令服务。 |
| `ConsoleOutput` | `IConsoleOutputService` | get | 控制台输出服务。 |
| `EntitySystem` | `IEntitySystemService` | get | 实体系统服务。 |
| `ConVar` | `IConVarService` | get | 控制台变量服务。 |
| `Configuration` | `IPluginConfigurationService` | get | 配置服务。 |
| `GameData` | `IGameDataService` | get | 游戏数据服务。 |
| `PlayerManager` | `IPlayerManagerService` | get | 玩家管理服务。 |
| `Memory` | `IMemoryService` | get | 内存服务。 |
| `LoggerFactory` | `ILoggerFactory` | get | 日志记录器工厂。 |
| `Logger` | `ILogger` | get | 默认日志记录器。 |
| `Profiler` | `IContextedProfilerService` | get | Profiler 服务。 |
| `Trace` | `ITraceManager` | get | 获取用于控制和管理游戏内追踪操作的追踪管理器。 |
| `Scheduler` | `ISchedulerService` | get | 调度器服务。 |
| `Database` | `IDatabaseService` | get | 数据库服务。 |
| `Translation` | `ITranslationService` | get | 翻译服务。 |
| `Localizer` | `ILocalizer` | get | 本地化器。 |
| `Permission` | `IPermissionManager` | get | 权限管理器。 |
| `Registrator` | `IRegistratorService` | get | 注册服务。 |
| `MenusAPI` | `IMenuManagerAPI` | get | 菜单管理器 API。 |
| `CommandLine` | `ICommandLine` | get | 命令行。 |
| `GameFileSystem` | `IGameFileSystem` | get | 游戏文件系统接口。 |
| `PluginManager` | `IPluginManager` | get | 插件管理器。 |
| `Datamap` | `IDatamapService` | get | 数据映射服务。 |
| `StringTable` | `IStringTableService` | get | 字符串表服务。 |
| `PluginPath` | `string` | get | 获取插件目录的文件路径。 |
| `CSGODirectory` | `string` | get | 获取 `game/csgo` 目录的绝对文件路径。 |
| `GameDirectory` | `string` | get | 获取游戏根目录的绝对文件路径。 |
| `PluginDataDirectory` | `string` | get | 获取插件数据目录的文件路径。该目录由框架确保存在。 |

