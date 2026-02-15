# 📦 SwiftlyCore

**命名空间:** `SwiftlyS2.Core.Services`

**类型:** `class`

**继承:** `ISwiftlyCore`

**实现接口:** `IDisposable`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `EventSubscriber` | `EventSubscriber` | get | - |
| `GameEventService` | `GameEventService` | get | - |
| `NetMessageService` | `NetMessageService` | get | - |
| `Configuration` | `PluginConfigurationService` | get | - |
| `LoggerFactory` | `ILoggerFactory` | get | - |
| `CommandService` | `CommandService` | get | - |
| `ConsoleOutputService` | `ConsoleOutputService` | get | - |
| `EntitySystemService` | `EntitySystemService` | get | - |
| `ConVarService` | `ConVarService` | get | - |
| `GameDataService` | `GameDataService` | get | - |
| `PlayerManagerService` | `PlayerManagerService` | get | - |
| `Logger` | `ILogger` | get | - |
| `Engine` | `EngineService` | get | - |
| `Trace` | `TraceManager` | get | - |
| `ProfilerService` | `ContextedProfilerService` | get | - |
| `MemoryService` | `MemoryService` | get | - |
| `SchedulerService` | `SchedulerService` | get | - |
| `DatabaseService` | `DatabaseService` | get | - |
| `TranslationService` | `TranslationService` | get | - |
| `Localizer` | `Localizer` | get | - |
| `PermissionManager` | `PermissionManager` | get | - |
| `RegistratorService` | `RegistratorService` | get | - |
| `MenuManagerAPI` | `MenuManagerAPI` | get | - |
| `CommandLineService` | `CommandLineService` | get | - |
| `Helpers` | `HelpersService` | get | - |
| `GameService` | `GameService` | get | - |
| `ContextBasePath` | `string` | get, set | - |
| `PluginDataDirectory` | `string` | get, set | - |
| `GameFileSystem` | `GameFileSystem` | get, set | - |
| `PluginManager` | `PluginManager` | get, set | - |
| `DatamapService` | `DatamapService` | get | - |
| `StringTableService` | `StringTableService` | get | - |

## ⚙️ 方法

### InitializeType

```csharp
void InitializeType(Type type)
```

**参数:**

- `type` (`Type`)

### InitializeObject

```csharp
void InitializeObject(object instance)
```

**参数:**

- `instance` (`object`)

### Dispose

```csharp
void Dispose()
```

