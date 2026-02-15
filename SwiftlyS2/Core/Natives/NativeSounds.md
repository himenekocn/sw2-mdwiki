# 📦 NativeSounds

**命名空间:** `SwiftlyS2.Core.Natives`

**类型:** `class`

## ⚙️ 方法

### CreateSoundEvent (静态)

```csharp
nint CreateSoundEvent()
```

**返回值:** `nint`

### DestroySoundEvent (静态)

```csharp
void DestroySoundEvent(nint soundEvent)
```

**参数:**

- `soundEvent` (`nint`)

### Emit (静态)

```csharp
uint Emit(nint soundEvent)
```

**参数:**

- `soundEvent` (`nint`)

**返回值:** `uint`

### SetName (静态)

```csharp
void SetName(nint soundEvent, string name)
```

**参数:**

- `soundEvent` (`nint`)
- `name` (`string`)

### GetName (静态)

```csharp
string GetName(nint soundEvent)
```

**参数:**

- `soundEvent` (`nint`)

**返回值:** `string`

### SetSourceEntityIndex (静态)

```csharp
void SetSourceEntityIndex(nint soundEvent, int index)
```

**参数:**

- `soundEvent` (`nint`)
- `index` (`int`)

### GetSourceEntityIndex (静态)

```csharp
int GetSourceEntityIndex(nint soundEvent)
```

**参数:**

- `soundEvent` (`nint`)

**返回值:** `int`

### AddClient (静态)

```csharp
void AddClient(nint soundEvent, int playerid)
```

**参数:**

- `soundEvent` (`nint`)
- `playerid` (`int`)

### RemoveClient (静态)

```csharp
void RemoveClient(nint soundEvent, int playerid)
```

**参数:**

- `soundEvent` (`nint`)
- `playerid` (`int`)

### ClearClients (静态)

```csharp
void ClearClients(nint soundEvent)
```

**参数:**

- `soundEvent` (`nint`)

### AddAllClients (静态)

```csharp
void AddAllClients(nint soundEvent)
```

**参数:**

- `soundEvent` (`nint`)

### HasField (静态)

```csharp
bool HasField(nint soundEvent, string fieldName)
```

**参数:**

- `soundEvent` (`nint`)
- `fieldName` (`string`)

**返回值:** `bool`

### SetBool (静态)

```csharp
void SetBool(nint soundEvent, string fieldName, bool value)
```

**参数:**

- `soundEvent` (`nint`)
- `fieldName` (`string`)
- `value` (`bool`)

### GetBool (静态)

```csharp
bool GetBool(nint soundEvent, string fieldName)
```

**参数:**

- `soundEvent` (`nint`)
- `fieldName` (`string`)

**返回值:** `bool`

### SetInt32 (静态)

```csharp
void SetInt32(nint soundEvent, string fieldName, int value)
```

**参数:**

- `soundEvent` (`nint`)
- `fieldName` (`string`)
- `value` (`int`)

### GetInt32 (静态)

```csharp
int GetInt32(nint soundEvent, string fieldName)
```

**参数:**

- `soundEvent` (`nint`)
- `fieldName` (`string`)

**返回值:** `int`

### SetUInt32 (静态)

```csharp
void SetUInt32(nint soundEvent, string fieldName, uint value)
```

**参数:**

- `soundEvent` (`nint`)
- `fieldName` (`string`)
- `value` (`uint`)

### GetUInt32 (静态)

```csharp
uint GetUInt32(nint soundEvent, string fieldName)
```

**参数:**

- `soundEvent` (`nint`)
- `fieldName` (`string`)

**返回值:** `uint`

### SetUInt64 (静态)

```csharp
void SetUInt64(nint soundEvent, string fieldName, ulong value)
```

**参数:**

- `soundEvent` (`nint`)
- `fieldName` (`string`)
- `value` (`ulong`)

### GetUInt64 (静态)

```csharp
ulong GetUInt64(nint soundEvent, string fieldName)
```

**参数:**

- `soundEvent` (`nint`)
- `fieldName` (`string`)

**返回值:** `ulong`

### SetFloat (静态)

```csharp
void SetFloat(nint soundEvent, string fieldName, float value)
```

**参数:**

- `soundEvent` (`nint`)
- `fieldName` (`string`)
- `value` (`float`)

### GetFloat (静态)

```csharp
float GetFloat(nint soundEvent, string fieldName)
```

**参数:**

- `soundEvent` (`nint`)
- `fieldName` (`string`)

**返回值:** `float`

### SetFloat3 (静态)

```csharp
void SetFloat3(nint soundEvent, string fieldName, Vector value)
```

**参数:**

- `soundEvent` (`nint`)
- `fieldName` (`string`)
- `value` (`Vector`)

### GetFloat3 (静态)

```csharp
Vector GetFloat3(nint soundEvent, string fieldName)
```

**参数:**

- `soundEvent` (`nint`)
- `fieldName` (`string`)

**返回值:** `Vector`

### GetClients (静态)

```csharp
ulong GetClients(nint soundEvent)
```

returns player mask

**参数:**

- `soundEvent` (`nint`)

**返回值:** `ulong`

### SetClients (静态)

```csharp
void SetClients(nint soundEvent, ulong playermask)
```

**参数:**

- `soundEvent` (`nint`)
- `playermask` (`ulong`)

