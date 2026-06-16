<a id="soundevent"></a>

# 📦 SoundEvent

**命名空间:** `SwiftlyS2.Shared.Sounds`

**类型:** `class`

**继承:** `IDisposable`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | - | 声音事件名称。 |
| `SourceEntityIndex` | `int` | - | 此声音事件发出的实体索引。设置为 -1（默认值）将从接收对象位置发出声音。 |
| `Volume` | `float` | - | 声音事件的音量。 |
| `Pitch` | `float` | - | 音调事件（sound event）的音高（pitch）。 |
| `Recipients` | `ref CRecipientFilter` | - | 声音事件的接收者。 |

## ⚙️ 方法

### SetSourceEntity

```csharp
void SetSourceEntity(CEntityInstance entity)
```

**参数:**

- `entity` (`CEntityInstance`)

**用法示例:**
```csharp
soundEvent.SetSourceEntity(entity);
```

### SetBool

```csharp
void SetBool(string fieldName, bool value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`bool`)

**用法示例:**
```csharp
soundEvent.SetBool("IsPlaying", true);
```

### GetBool

```csharp
bool GetBool(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool isActive = soundEvent.GetBool("IsPlaying");
```

### SetInt32

```csharp
void SetInt32(string fieldName, int value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`int`)

**用法示例:**
```csharp
soundEvent.SetInt32("volume", 100);
```

### GetInt32

```csharp
int GetInt32(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `int`

**用法示例:**
```csharp
int value = soundEvent.GetInt32("volume");
```

### SetUInt32

```csharp
void SetUInt32(string fieldName, uint value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`uint`)

**用法示例:**
```csharp
soundEvent.SetUInt32("Volume", 100);
```

### GetUInt32

```csharp
uint GetUInt32(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `uint`

**用法示例:**
```csharp
uint value = soundEvent.GetUInt32("volume");
```

### SetFloat

```csharp
void SetFloat(string fieldName, float value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`float`)

**用法示例:**
```csharp
soundEvent.SetFloat("volume", 0.5f);
```

### GetFloat

```csharp
float GetFloat(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `float`

**用法示例:**
```csharp
float volume = soundEvent.GetFloat("volume");
```

### SetFloat3

```csharp
void SetFloat3(string fieldName, float x, float y, float z)
```

**参数:**

- `fieldName` (`string`)
- `x` (`float`)
- `y` (`float`)
- `z` (`float`)

**用法示例:**
```csharp
soundEvent.SetFloat3("position", 1.0f, 2.0f, 3.0f);
```

### SetFloat3

```csharp
void SetFloat3(string fieldName, Vector vec)
```

**参数:**

- `fieldName` (`string`)
- `vec` (`Vector`)

**用法示例:**
```csharp
soundEvent.SetFloat3("position", Vector.Zero);
```

### GetFloat3

```csharp
Vector GetFloat3(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `Vector`

**用法示例:**
```csharp
Vector position = soundEvent.GetFloat3("position");
```

### Emit

```csharp
uint Emit()
```

**返回值:** `uint`

**用法示例:**
```csharp
uint id = soundEvent.Emit();
```

### EmitAsync

```csharp
Task<uint> EmitAsync()
```

异步触发声音事件。

**返回值:** `Task\<uint\>` - 发出的声音事件GUID。

**用法示例:**
```csharp
uint soundId = await soundEvent.EmitAsync();
```

### Dispose

```csharp
void Dispose()
```

