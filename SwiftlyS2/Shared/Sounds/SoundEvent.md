# 📦 SoundEvent

**命名空间:** `SwiftlyS2.Shared.Sounds`

**类型:** `class`

**继承:** `IDisposable`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `Name` | `string` | get, set | The sound event name. |
| `SourceEntityIndex` | `int` | get, set | The index of the entity that this sound event is emitted from. Setting to -1 (default) will emit the sound from the recipient location. |
| `Volume` | `float` | get, set | The volume of the sound event. |
| `Pitch` | `float` | get, set | The pitch of the sound event. |

## ⚙️ 方法

### SetSourceEntity

```csharp
void SetSourceEntity(CEntityInstance entity)
```

**参数:**

- `entity` (`CEntityInstance`)

### SetBool

```csharp
void SetBool(string fieldName, bool value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`bool`)

### GetBool

```csharp
bool GetBool(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `bool`

### SetInt32

```csharp
void SetInt32(string fieldName, int value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`int`)

### GetInt32

```csharp
int GetInt32(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `int`

### SetUInt32

```csharp
void SetUInt32(string fieldName, uint value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`uint`)

### GetUInt32

```csharp
uint GetUInt32(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `uint`

### SetFloat

```csharp
void SetFloat(string fieldName, float value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`float`)

### GetFloat

```csharp
float GetFloat(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `float`

### SetFloat3

```csharp
void SetFloat3(string fieldName, float x, float y, float z)
```

**参数:**

- `fieldName` (`string`)
- `x` (`float`)
- `y` (`float`)
- `z` (`float`)

### SetFloat3

```csharp
void SetFloat3(string fieldName, Vector vec)
```

**参数:**

- `fieldName` (`string`)
- `vec` (`Vector`)

### GetFloat3

```csharp
Vector GetFloat3(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `Vector`

### Emit

```csharp
uint Emit()
```

**返回值:** `uint`

### EmitAsync

```csharp
Task<uint> EmitAsync()
```

Emit the sound event asynchronously.

**返回值:** `Task\<uint\>` - The emitted sound event guid.

### Dispose

```csharp
void Dispose()
```

