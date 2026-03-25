<a id="soundevent"></a>

# 📦 SoundEvent

**命名空间:** `SwiftlyS2.Shared.Sounds`

**类型:** `class`

**继承:** `IDisposable`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | - | 音效事件名称。 |
| `SourceEntityIndex` | `int` | - | 发出此声音事件实体的索引。设置为 -1（默认值）将从接收者位置发出声音。 |
| `Volume` | `float` | - | 音效事件的音量。 |
| `Pitch` | `float` | - | 声音事件的音高。 |
| `Recipients` | `ref CRecipientFilter` | - | 声音事件的目标接收者。 |

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
soundEvent.SetInt32("volume", 75);
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
soundEvent.SetUInt32("event_id", 1001);
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
uint value = soundEvent.GetUInt32("Volume");
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
soundEvent.SetFloat("volume", 0.8f);
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
soundEvent.SetFloat3("position", 1.0f, 2.5f, -3.0f);
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
soundEvent.SetFloat3("volume", existingVector);
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
Vector result = soundEvent.GetFloat3("volume");
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

异步触发音效事件。

**返回值:** `Task\<uint\>` - 生成的声音事件 GUID。

**用法示例:**
```csharp
uint eventId = await soundEvent.EmitAsync();
```

### Dispose

```csharp
void Dispose()
```

