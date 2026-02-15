# 📦 NativeEntitySystem

**命名空间:** `SwiftlyS2.Core.Natives`

**类型:** `class`

## ⚙️ 方法

### Spawn (静态)

```csharp
void Spawn(nint entity, nint keyvalues)
```

**参数:**

- `entity` (`nint`)
- `keyvalues` (`nint`)

### Despawn (静态)

```csharp
void Despawn(nint entity)
```

**参数:**

- `entity` (`nint`)

### CreateEntityByName (静态)

```csharp
nint CreateEntityByName(string name)
```

**参数:**

- `name` (`string`)

**返回值:** `nint`

### AcceptInput (静态)

```csharp
void AcceptInput(nint entity, string input, nint activator, nint caller, nint value, int outputID)
```

**参数:**

- `entity` (`nint`)
- `input` (`string`)
- `activator` (`nint`)
- `caller` (`nint`)
- `value` (`nint`)
- `outputID` (`int`)

### AddEntityIOEvent (静态)

```csharp
void AddEntityIOEvent(nint entity, string input, nint activator, nint caller, nint value, float delay)
```

**参数:**

- `entity` (`nint`)
- `input` (`string`)
- `activator` (`nint`)
- `caller` (`nint`)
- `value` (`nint`)
- `delay` (`float`)

### IsValidEntity (静态)

```csharp
bool IsValidEntity(nint entity)
```

**参数:**

- `entity` (`nint`)

**返回值:** `bool`

### GetGameRules (静态)

```csharp
nint GetGameRules()
```

**返回值:** `nint`

### GetEntitySystem (静态)

```csharp
nint GetEntitySystem()
```

**返回值:** `nint`

### EntityHandleIsValid (静态)

```csharp
bool EntityHandleIsValid(uint handle)
```

**参数:**

- `handle` (`uint`)

**返回值:** `bool`

### EntityHandleGet (静态)

```csharp
nint EntityHandleGet(uint handle)
```

**参数:**

- `handle` (`uint`)

**返回值:** `nint`

### GetEntityHandleFromEntity (静态)

```csharp
uint GetEntityHandleFromEntity(nint entity)
```

**参数:**

- `entity` (`nint`)

**返回值:** `uint`

### GetFirstActiveEntity (静态)

```csharp
nint GetFirstActiveEntity()
```

**返回值:** `nint`

### HookEntityOutput (静态)

```csharp
ulong HookEntityOutput(string className, string outputName, nint callback)
```

CEntityIOOutput*, string outputName, CEntityInstance* activator, CEntityInstance* caller, float delay -> int (HookResult)

**参数:**

- `className` (`string`)
- `outputName` (`string`)
- `callback` (`nint`)

**返回值:** `ulong`

### UnhookEntityOutput (静态)

```csharp
void UnhookEntityOutput(ulong hookid)
```

**参数:**

- `hookid` (`ulong`)

### GetEntityByIndex (静态)

```csharp
nint GetEntityByIndex(uint index)
```

**参数:**

- `index` (`uint`)

**返回值:** `nint`

### IsValid (静态)

```csharp
bool IsValid()
```

**返回值:** `bool`

