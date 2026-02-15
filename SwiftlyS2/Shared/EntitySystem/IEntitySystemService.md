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
manager.EntityOutputEventHandler(new EntityFireOutputHookEvent(player, "OnKilled", null));
```

### EntityInputEventHandler

```csharp
void EntityInputEventHandler(IOnEntityIdentityAcceptInputHookEvent @event)
```

表示一个处理实体输入事件的方法，允许在实体接受输入时执行自定义逻辑。

**参数:**

- `@event` (`IOnEntityIdentityAcceptInputHookEvent`)

**用法示例:**
```csharp
manager.EntityInputEventHandler(new EntityInputAcceptInputEvent(player));
```

### GetGameRules

```csharp
CCSGameRules? GetGameRules()
```

获取游戏规则实体。

**返回值:** `CCSGameRules?` - 游戏规则实体。可为空。

**用法示例:**
```csharp
CCSGameRules? rules = entitySystem.GetGameRules();
```

### GetAllEntities

```csharp
IEnumerable<CEntityInstance> GetAllEntities()
```

获取所有实体。

**返回值:** `IEnumerable\<CEntityInstance\>` - 所有实体。

**用法示例:**
```csharp
foreach (var entity in manager.GetAllEntities()) { /* 处理实体 */ }
```

### GetEntityByIndex

```csharp
CEntityInstance? GetEntityByIndex(uint index)
```

通过索引获取实体。返回的对象将具有实体的实际类型。您可以将其强制转换为实际类型。

**参数:**

- `index` (`uint`) - 实体索引。

**返回值:** `CEntityInstance?` - 按索引获取实体。可为空。

**用法示例:**
```csharp
CEntityInstance? entity = GetEntityByIndex(0);  
if (entity is CPlayerController player) { /* use player */ }
```

### GetEntityByAddress

```csharp
CEntityInstance? GetEntityByAddress(nint address)
```

根据地址获取实体。

**参数:**

- `address` (`nint`) - 实体地址。

**返回值:** `CEntityInstance?` - 按地址获取的实体。可为空。

**用法示例:**
```csharp
CEntityInstance? entity = entitySystem.GetEntityByAddress(0x12345678);
```

### HookEntityOutput

```csharp
Guid HookEntityOutput(string designerName, string outputName, EntityOutputEventHandler callback)
```

将指定实体类型的输出绑定到回调函数。

**参数:**

- `designerName` (`string`) - 要挂钩的实体的设计器名称。该值不能为 <see langword="null"/> 或空。
- `outputName` (`string`) - 要挂钩的输出名称。该值不能为 <see langword="null"/> 或空。
- `callback` (`EntityOutputEventHandler`) - 当输出被触发时调用的回调函数。该值不能为 <see langword="null"/>。

**返回值:** `Guid` - 一个 <see cref="Guid"/>，用于唯一标识该钩子。此标识符可用于移除该钩子。

**用法示例:**
```csharp
Guid hookId = EntitySystem.HookEntityOutput("Player", "HealthChanged", (sender, args) => Console.WriteLine($"Health changed: {args.Value}"));
```

### UnhookEntityOutput

```csharp
bool UnhookEntityOutput(Guid guid)
```

移除指定实体输出与其处理程序之间的关联。

**参数:**

- `guid` (`Guid`) - 要取消挂钩的实体的唯一标识符。

**返回值:** `bool` - 如果挂钩已成功移除，则为 <see langword="true"/>；否则为 <see langword="false"/>。

**用法示例:**
```csharp
manager.UnhookEntityOutput(someGuid);
```

### HookEntityInput

```csharp
Guid HookEntityInput(string designerName, string inputName, EntityInputEventHandler callback)
```

将指定实体类型的输入挂钩到回调函数。

**参数:**

- `designerName` (`string`) - 要挂钩的实体的设计器名称。该值不能为 <see langword="null"/> 或空。
- `inputName` (`string`) - 要挂钩的输入名称。该值不能为 <see langword="null"/> 或空。
- `callback` (`EntityInputEventHandler`) - 当输入被接受时调用的回调函数。该值不能为 <see langword="null"/>。

**返回值:** `Guid` - 一个 <see cref="Guid"/>，用于唯一标识该钩子。此标识符可用于移除该钩子。

**用法示例:**
```csharp
Guid hookId = entitySystem.HookEntityInput("Player", "Jump", OnPlayerJump);

void OnPlayerJump(Entity entity) { /* handle jump */ }
```

### UnhookEntityInput

```csharp
bool UnhookEntityInput(Guid guid)
```

移除指定实体输入与其处理程序之间的关联。

**参数:**

- `guid` (`Guid`) - 要取消挂钩的实体输入的唯一标识符。

**返回值:** `bool` - 如果挂钩已成功移除，则为 <see langword="true"/>；否则为 <see langword="false"/>。

**用法示例:**
```csharp
bool result = entitySystem.UnhookEntityInput(someGuid);
```

