<a id="ientitysystemservice"></a>

# 🔌 IEntitySystemService

**命名空间:** `SwiftlyS2.Shared.EntitySystem`

**类型:** `interface`

## ⚙️ 方法

### EntityOutputEventHandler

```csharp
void EntityOutputEventHandler(IOnEntityFireOutputHookEvent @event)
```

表示一个处理实体输出事件的方法，允许在实体触发输出时执行自定义逻辑。

**参数:**

- `@event` (`IOnEntityFireOutputHookEvent`)

**用法示例:**
```csharp
entitySystem.EntityOutputEventHandler(event);
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
entitySystem.EntityInputEventHandler(inputEvent);
```

### CreateEntity<T>

```csharp
T CreateEntity<T>()
```

通过类创建实体。

**返回值:** `T` - 已创建实体。

**用法示例:**
```csharp
var entity = systemService.CreateEntity<MyEntity>();
```

### CreateEntityByDesignerName<T>

```csharp
T CreateEntityByDesignerName<T>(string designerName)
```

根据设计器名称创建实体。

**参数:**

- `designerName` (`string`) - 设计器名称。

**返回值:** `T` - 已创建实体。

**用法示例:**
```csharp
var entity = manager.CreateEntityByDesignerName<MyEntity>("MyEntityDesigner");
```

### GetRefEHandle<T>

```csharp
CHandle<T> GetRefEHandle<T>(T entity)
```

获取对实体的引用句柄。

**参数:**

- `entity` (`T`) - 实体实例。

**返回值:** `CHandle\<T\>` - 引用实体句柄到实体。

**用法示例:**
```csharp
CHandle<Player> handle = entitySystem.GetRefEHandle(player);
```

### GetGameRules

```csharp
CCSGameRules? GetGameRules()
```

获取游戏规则实体。

**返回值:** `CCSGameRules?` - 游戏规则实体。可为空。

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
var entities = manager.GetAllEntities();
```

### GetAllEntitiesByClass<T>

```csharp
IEnumerable<T> GetAllEntitiesByClass<T>()
```

根据类获取所有实体。

**返回值:** `IEnumerable\<T\>` - 按类别划分的所有实体。

**用法示例:**
```csharp
var entities = manager.GetAllEntitiesByClass<CBasePlayer>();
```

### GetAllEntitiesByDesignerName<T>

```csharp
IEnumerable<T> GetAllEntitiesByDesignerName<T>(string designerName)
```

按设计器名称获取所有实体，并强制转换为类型 T。

**参数:**

- `designerName` (`string`) - 设计器名称。

**返回值:** `IEnumerable\<T\>` - 所有按设计师名称分类的实体。

**用法示例:**
```csharp
var entities = manager.GetAllEntitiesByDesignerName<MyEntity>("my_designer");
```

### GetEntityByIndex<T>

```csharp
T? GetEntityByIndex<T>(uint index)
```

根据索引获取实体。

**参数:**

- `index` (`uint`) - 实体索引。

**返回值:** `T?` - 按索引获取实体。可为空。

**用法示例:**
```csharp
var entity = manager.GetEntityByIndex<Player>(0);
```

### GetEntityByIndex

```csharp
CEntityInstance? GetEntityByIndex(uint index)
```

根据索引获取实体。返回的对象将具有实体的实际类型。你可以将其转换为实际类型。

**参数:**

- `index` (`uint`) - 实体索引。

**返回值:** `CEntityInstance?` - 按索引获取实体。可为空。

**用法示例:**
```csharp
var entity = manager.GetEntityByIndex(1);
```

### GetEntityByAddress<T>

```csharp
T? GetEntityByAddress<T>(nint address)
```

根据地址获取实体。

**参数:**

- `address` (`nint`) - 实体地址。

**返回值:** `T?` - 按地址获取实体。可为空。

**用法示例:**
```csharp
var entity = systemService.GetEntityByAddress<Player>(0x12345678);
```

### GetEntityByAddress

```csharp
CEntityInstance? GetEntityByAddress(nint address)
```

根据地址获取实体。

**参数:**

- `address` (`nint`) - 实体地址。

**返回值:** `CEntityInstance?` - 按地址获取实体。可为空。

**用法示例:**
```csharp
var entity = manager.GetEntityByAddress(address);
```

### HookEntityOutput<T>

```csharp
Guid HookEntityOutput<T>(string outputName, EntityOutputEventHandler callback)
```

将指定实体类型的输出连接到回调函数。

**参数:**

- `outputName` (`string`) - 要挂钩的输出名称。该值不能为 <see langword="null"/> 或空。
- `callback` (`EntityOutputEventHandler`) - 当输出被触发时要调用的回调函数。此值不能为 <see langword="null"/>。

**返回值:** `Guid` - 一个唯一标识该钩子的 <see cref="Guid"/>。此标识符可用于移除该钩子。

**用法示例:**
```csharp
Guid hookId = entitySystem.HookEntityOutput<MyEntity>("OnBreak", (sender, args) => { });
```

### HookEntityOutput

```csharp
Guid HookEntityOutput(string designerName, string outputName, EntityOutputEventHandler callback)
```

将指定实体类型的输出连接到回调函数。

**参数:**

- `designerName` (`string`) - 要挂钩的实体的设计器名称。该值不能为 <see langword="null"/> 或空。
- `outputName` (`string`) - 要挂钩的输出名称。该值不能为 <see langword="null"/> 或空。
- `callback` (`EntityOutputEventHandler`) - 当输出被触发时要调用的回调函数。此值不能为 <see langword="null"/>。

**返回值:** `Guid` - 一个唯一标识该钩子的 <see cref="Guid"/>。此标识符可用于移除该钩子。

**用法示例:**
```csharp
Guid hookId = entitySystem.HookEntityOutput("prop_physics", "OnBreak", (entity, activator) => { });
```

### UnhookEntityOutput

```csharp
bool UnhookEntityOutput(Guid guid)
```

移除指定实体输出与其处理程序之间的关联。

**参数:**

- `guid` (`Guid`) - 要解除挂钩的实体输出的唯一标识符。

**返回值:** `bool` - <see langword="true"/> 表示钩子已成功移除；否则为 <see langword="false"/>。

**用法示例:**
```csharp
bool result = entitySystem.UnhookEntityOutput(entityGuid);
```

### HookEntityInput<T>

```csharp
Guid HookEntityInput<T>(string inputName, EntityInputEventHandler callback)
```

将指定实体类型的输入挂接到回调函数。

**参数:**

- `inputName` (`string`) - 挂钩输入的名称。该值不能为 <see langword="null"/> 或为空。
- `callback` (`EntityInputEventHandler`) - 接受输入时调用的回调函数。此值不能为<see langword="null"/>。

**返回值:** `Guid` - 一个唯一标识该钩子的 <see cref="Guid"/>。此标识符可用于移除该钩子。

**用法示例:**
```csharp
var hookId = entitySystem.HookEntityInput<Player>("Use", (entity, input) => { });
```

### HookEntityInput

```csharp
Guid HookEntityInput(string designerName, string inputName, EntityInputEventHandler callback)
```

将指定实体类型的输入挂接到回调函数。

**参数:**

- `designerName` (`string`) - 要挂钩的实体的设计器名称。该值不能为 <see langword="null"/> 或空。
- `inputName` (`string`) - 挂钩输入的名称。该值不能为 <see langword="null"/> 或为空。
- `callback` (`EntityInputEventHandler`) - 接受输入时调用的回调函数。此值不能为<see langword="null"/>。

**返回值:** `Guid` - 一个唯一标识该钩子的 <see cref="Guid"/>。此标识符可用于移除该钩子。

**用法示例:**
```csharp
var hookId = entitySystem.HookEntityInput("prop_physics", "Break", OnEntityInput);
```

### UnhookEntityInput

```csharp
bool UnhookEntityInput(Guid guid)
```

移除指定实体输入与其处理程序之间的关联。

**参数:**

- `guid` (`Guid`) - 要解除挂接的实体输入的唯一标识符。

**返回值:** `bool` - <see langword="true"/> 表示钩子已成功移除；否则为 <see langword="false"/>。

**用法示例:**
```csharp
bool result = entitySystem.UnhookEntityInput(entityGuid);
```

