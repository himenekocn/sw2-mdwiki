# 📦 EntityManager

**命名空间:** `SwiftlyS2.Core.EntitySystem`

**类型:** `class`

## ⚙️ 方法

### OnEntityCreated (静态)

```csharp
CEntityInstance OnEntityCreated(nint entityPtr)
```

**参数:**

- `entityPtr` (`nint`)

**返回值:** `CEntityInstance`

### GetEntityByIndex (静态)

```csharp
CEntityInstance? GetEntityByIndex(uint index)
```

**参数:**

- `index` (`uint`)

**返回值:** `CEntityInstance?`

### GetEntityByAddress (静态)

```csharp
CEntityInstance? GetEntityByAddress(nint address)
```

**参数:**

- `address` (`nint`)

**返回值:** `CEntityInstance?`

### OnEntityDeleted (静态)

```csharp
void OnEntityDeleted(nint entityPtr)
```

**参数:**

- `entityPtr` (`nint`)

### GetAllEntities (静态)

```csharp
IEnumerable<CEntityInstance> GetAllEntities()
```

**返回值:** `IEnumerable\<CEntityInstance\>`

### IsAddressValid (静态)

```csharp
bool IsAddressValid(nint address)
```

**参数:**

- `address` (`nint`)

**返回值:** `bool`

