# 📦 EntitySystemService

**命名空间:** `SwiftlyS2.Core.EntitySystem`

**类型:** `class`

**继承:** `IEntitySystemService`

**实现接口:** `IDisposable`

## ⚙️ 方法

### CreateEntityByDesignerName

```csharp
CEntityInstance CreateEntityByDesignerName(string designerName)
```

**参数:**

- `designerName` (`string`)

**返回值:** `CEntityInstance`

### GetGameRules

```csharp
CCSGameRules? GetGameRules()
```

**返回值:** `CCSGameRules?`

### GetAllEntities

```csharp
IEnumerable<CEntityInstance> GetAllEntities()
```

**返回值:** `IEnumerable\<CEntityInstance\>`

### GetEntityByIndex

```csharp
CEntityInstance? GetEntityByIndex(uint index)
```

**参数:**

- `index` (`uint`)

**返回值:** `CEntityInstance?`

### HookEntityOutput

```csharp
Guid HookEntityOutput(string designerName, string outputName, IEntitySystemService.EntityOutputEventHandler callback)
```

**参数:**

- `designerName` (`string`)
- `outputName` (`string`)
- `callback` (`IEntitySystemService.EntityOutputEventHandler`)

**返回值:** `Guid`

### HookEntityInput

```csharp
Guid HookEntityInput(string designerName, string inputName, IEntitySystemService.EntityInputEventHandler callback)
```

**参数:**

- `designerName` (`string`)
- `inputName` (`string`)
- `callback` (`IEntitySystemService.EntityInputEventHandler`)

**返回值:** `Guid`

### UnhookEntityOutput

```csharp
bool UnhookEntityOutput(Guid guid)
```

**参数:**

- `guid` (`Guid`)

**返回值:** `bool`

### UnhookEntityInput

```csharp
bool UnhookEntityInput(Guid guid)
```

**参数:**

- `guid` (`Guid`)

**返回值:** `bool`

### Dispose

```csharp
void Dispose()
```

### GetEntityByAddress

```csharp
CEntityInstance? GetEntityByAddress(nint address)
```

**参数:**

- `address` (`nint`)

**返回值:** `CEntityInstance?`

