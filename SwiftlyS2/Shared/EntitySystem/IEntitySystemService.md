# 🔌 IEntitySystemService

**命名空间:** `SwiftlyS2.Shared.EntitySystem`

**类型:** `interface`

## ⚙️ 方法

### EntityOutputEventHandler

```csharp
void EntityOutputEventHandler(IOnEntityFireOutputHookEvent @event)
```

表示一种处理实体输出事件的方法，允许在实体触发输出时执行自定义逻辑。

**参数:**

- `@event` (`IOnEntityFireOutputHookEvent`)

**用法示例:**
```csharp
IEntitySystemService.EntityOutputEventHandler(eventData);
```

### EntityInputEventHandler

```csharp
void EntityInputEventHandler(IOnEntityIdentityAcceptInputHookEvent @event)
```

表示处理实体输入事件的方法，允许在实体接受输入时执行自定义逻辑。

**参数:**

- `@event` (`IOnEntityIdentityAcceptInputHookEvent`)

**用法示例:**
```csharp
entitySystemService.EntityInputEventHandler(eventData);
```

### CreateEntity<T>

```csharp
T CreateEntity<T>()
```

通过类创建实体。

**返回值:** `T` - 已创建实体。

**用法示例:**
```csharp
var entity = manager.CreateEntity<Player>();
```

### CreateEntityByDesignerName<T>

```csharp
T CreateEntityByDesignerName<T>(string designerName)
```

通过设计器名称创建实体。

**参数:**

- `designerName` (`string`) - 设计师名称。

**返回值:** `T` - 已创建实体。

**用法示例:**
```csharp
var entity = IEntitySystemService.CreateEntityByDesignerName<Entity>("info_player_start");
```

### GetRefEHandle<T>

```csharp
CHandle<T> GetRefEHandle<T>(T entity)
```

获取实体的引用句柄。

**参数:**

- `entity` (`T`) - 实体实例。

**返回值:** `CHandle\<T\>` - 引用实体的实体句柄。

**用法示例:**
```csharp
var handle = entitySystem.GetRefEHandle(player);
```

### GetGameRules

```csharp
CCSGameRules? GetGameRules()
```

获取游戏规则实体。

**返回值:** `CCSGameRules?` - 游戏实体规则。可为空。

**用法示例:**
```csharp
var rules = entitySystemService.GetGameRules();
```

### GetAllEntities

```csharp
IEnumerable<CEntityInstance> GetAllEntities()
```

获取所有实体。

**返回值:** `IEnumerable\<CEntityInstance\>` - 所有实体。

**用法示例:**
```csharp
var entities = IEntitySystemService.GetAllEntities();
```

### GetAllEntitiesByClass<T>

```csharp
IEnumerable<T> GetAllEntitiesByClass<T>()
```

按类获取所有实体。

**返回值:** `IEnumerable\<T\>` - 所有按类划分的实体。

**用法示例:**
```csharp
var entities = entitySystemService.GetAllEntitiesByClass<CBasePlayer>();
```

### GetAllEntitiesByDesignerName<T>

```csharp
IEnumerable<T> GetAllEntitiesByDesignerName<T>(string designerName)
```

通过设计师名称获取所有实体，并转换为类型 T。

**参数:**

- `designerName` (`string`) - 设计师名称。

**返回值:** `IEnumerable\<T\>` - 所有按设计师名称命名的实体。

**用法示例:**
```csharp
var entities = IEntitySystemService.GetAllEntitiesByDesignerName<MyEntity>("DesignerName");
```

### GetEntityByIndex<T>

```csharp
T? GetEntityByIndex<T>(uint index)
```

通过索引获取实体。

**参数:**

- `index` (`uint`) - 实体索引。

**返回值:** `T?` - 通过索引获取实体。可为空。

**用法示例:**
```csharp
var entity = systemService.GetEntityByIndex<Player>(1);
```

### GetEntityByIndex

```csharp
CEntityInstance? GetEntityByIndex(uint index)
```

通过索引获取实体。返回的对象将具有实体的实际类型，您可以将其转换为该实际类型。

**参数:**

- `index` (`uint`) - 实体索引。

**返回值:** `CEntityInstance?` - 通过索引获取实体。可为空。

**用法示例:**
```csharp
var entity = manager.GetEntityByIndex(5);
```

### GetEntityByAddress<T>

```csharp
T? GetEntityByAddress<T>(nint address)
```

根据地址获取实体。

**参数:**

- `address` (`nint`) - 实体地址。

**返回值:** `T?` - 按地址定位的实体。可为空。

**用法示例:**
```csharp
var entity = system.GetEntityByAddress<MyEntity>(address);
```

### GetEntityByAddress

```csharp
CEntityInstance? GetEntityByAddress(nint address)
```

根据地址获取实体。

**参数:**

- `address` (`nint`) - 实体地址。

**返回值:** `CEntityInstance?` - 按地址定位的实体。可为空。

**用法示例:**
```csharp
var entity = systemService.GetEntityByAddress(address);
```

### HookEntityOutput<T>

```csharp
Guid HookEntityOutput<T>(string outputName, EntityOutputEventHandler callback)
```

将指定实体类型的输出挂钩至回调函数。

**参数:**

- `outputName` (`string`) - 要挂钩的输出的名称。此值不能为<see langword="null"/>或空。
- `callback` (`EntityOutputEventHandler`) - 触发输出时调用的回调函数。此值不能为 <see langword="null"/>。

**返回值:** `Guid` - 一个唯一标识该挂钩的 <see cref="Guid"/>。此标识符可用于移除该挂钩。

**用法示例:**
```csharp
var hookId = entitySystem.HookEntityOutput<Player>("OnTakeDamage", (sender, args) => { });
```

### HookEntityOutput

```csharp
Guid HookEntityOutput(string designerName, string outputName, EntityOutputEventHandler callback)
```

将指定实体类型的输出挂钩至回调函数。

**参数:**

- `designerName` (`string`) - 要绑定的实体的设计器名称。此值不能为 <see langword="null"/> 或空字符串。
- `outputName` (`string`) - 要挂钩的输出的名称。此值不能为<see langword="null"/>或空。
- `callback` (`EntityOutputEventHandler`) - 触发输出时调用的回调函数。此值不能为 <see langword="null"/>。

**返回值:** `Guid` - 一个唯一标识该挂钩的 <see cref="Guid"/>。此标识符可用于移除该挂钩。

**用法示例:**
```csharp
Guid hookId = entitySystem.HookEntityOutput("func_button", "OnPressed", (entity, output) => Console.WriteLine($"Button {entity} pressed!"));
```

### UnhookEntityOutput

```csharp
bool UnhookEntityOutput(Guid guid)
```

移除指定实体输出与其处理程序之间的关联。

**参数:**

- `guid` (`Guid`) - 输出到解钩的实体的唯一标识符。

**返回值:** `bool` - 如果钩子成功移除，则为<see langword="true"/>；否则为<see langword="false"/>。

**用法示例:**
```csharp
IEntitySystemService entityService; entityService.UnhookEntityOutput(Guid.Parse("12345678-1234-1234-1234-123456789012"));
```

### HookEntityInput<T>

```csharp
Guid HookEntityInput<T>(string inputName, EntityInputEventHandler callback)
```

将指定实体类型的输入挂钩至回调函数。

**参数:**

- `inputName` (`string`) - 要拦截的输入名称。该值不能为 null 或为空。
- `callback` (`EntityInputEventHandler`) - 当输入被接受时调用的回调函数。此值不能为 <see langword="null"/>。

**返回值:** `Guid` - 一个唯一标识该挂钩的 <see cref="Guid"/>。此标识符可用于移除该挂钩。

**用法示例:**
```csharp
var hookId = entitySystemService.HookEntityInput<Player>("attack", OnPlayerAttack);
```

### HookEntityInput

```csharp
Guid HookEntityInput(string designerName, string inputName, EntityInputEventHandler callback)
```

将指定实体类型的输入挂钩至回调函数。

**参数:**

- `designerName` (`string`) - 要绑定的实体的设计器名称。此值不能为 <see langword="null"/> 或空字符串。
- `inputName` (`string`) - 要拦截的输入名称。该值不能为 null 或为空。
- `callback` (`EntityInputEventHandler`) - 当输入被接受时调用的回调函数。此值不能为 <see langword="null"/>。

**返回值:** `Guid` - 一个唯一标识该挂钩的 <see cref="Guid"/>。此标识符可用于移除该挂钩。

**用法示例:**
```csharp
Guid hookId = IEntitySystemService.HookEntityInput("player", "take_damage", OnPlayerDamage);
```

### UnhookEntityInput

```csharp
bool UnhookEntityInput(Guid guid)
```

移除指定实体输入与其处理器之间的关联。

**参数:**

- `guid` (`Guid`) - 注入解钩的目标实体的唯一标识符。

**返回值:** `bool` - 如果钩子成功移除，则为<see langword="true"/>；否则为<see langword="false"/>。

**用法示例:**
```csharp
bool result = entitySystemService.UnhookEntityInput(guid);
```

