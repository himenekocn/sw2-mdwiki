# 🔌 ISwiftlyCore

Core interface of SwiftlyS2 framework.

**命名空间:** `SwiftlyS2.Shared`

**类型:** `interface`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `Event` | `IEventSubscriber` | get | Custom event subscriber. |
| `Engine` | `IEngineService` | get | Gets the engine service used to perform core engine operations. |
| `GameEvent` | `IGameEventService` | get | Game event service. |
| `NetMessage` | `INetMessageService` | get | Net message service. |
| `Helpers` | `IHelpers` | get | Helpers service. |
| `Game` | `IGameService` | get | Game service. |
| `Command` | `ICommandService` | get | Command service. |
| `ConsoleOutput` | `IConsoleOutputService` | get | Console output service. |
| `EntitySystem` | `IEntitySystemService` | get | Entity system service. |
| `ConVar` | `IConVarService` | get | Convar service. |
| `Configuration` | `IPluginConfigurationService` | get | Configuration service. |
| `GameData` | `IGameDataService` | get | Game data service. |
| `PlayerManager` | `IPlayerManagerService` | get | Player manager service. |
| `Memory` | `IMemoryService` | get | Memory service. |
| `LoggerFactory` | `ILoggerFactory` | get | Logger factory. |
| `Logger` | `ILogger` | get | Default logger. |
| `Profiler` | `IContextedProfilerService` | get | Profiler service. |
| `Trace` | `ITraceManager` | get | Gets the trace manager used to control and configure tracing operations within the game. |
| `Scheduler` | `ISchedulerService` | get | Scheduler service. |
| `Database` | `IDatabaseService` | get | Database service. |
| `Translation` | `ITranslationService` | get | Translation service. |
| `Localizer` | `ILocalizer` | get | Localizer. |
| `Permission` | `IPermissionManager` | get | Permission manager. |
| `Registrator` | `IRegistratorService` | get | Registrator service. |
| `MenusAPI` | `IMenuManagerAPI` | get | Menu manager API. |
| `CommandLine` | `ICommandLine` | get | Command line. |
| `GameFileSystem` | `IGameFileSystem` | get | Game file system interface. |
| `PluginManager` | `IPluginManager` | get | Plugin manager. |
| `Datamap` | `IDatamapService` | get | Datamap service. |
| `StringTable` | `IStringTableService` | get | String table service. |
| `PluginPath` | `string` | get | Gets the file path to the plugin directory. |
| `CSGODirectory` | `string` | get | Gets the absolute file path to the `game/csgo` directory. |
| `GameDirectory` | `string` | get | Gets the absolute file path to the game's root directory. |
| `PluginDataDirectory` | `string` | get | Gets the file path to the plugin data directory. This directory is ensured to exist by the framework. |

