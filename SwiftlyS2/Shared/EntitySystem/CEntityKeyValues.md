<a id="centitykeyvalues"></a>

# 📦 CEntityKeyValues

**命名空间:** `SwiftlyS2.Shared.EntitySystem`

**类型:** `class`

**继承:** `IDisposable`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `Address` | `nint` | - | - |

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Address` | `nint` | - | - |

## ⚙️ 方法

### Dispose

```csharp
void Dispose()
```

### SetBool

```csharp
void SetBool(string key, bool value)
```

**参数:**

- `key` (`string`)
- `value` (`bool`)

**用法示例:**
```csharp
entityKeyValues.SetBool("is_active", true);
```

### SetInt32

```csharp
void SetInt32(string key, int value)
```

**参数:**

- `key` (`string`)
- `value` (`int`)

**用法示例:**
```csharp
entityKeyValues.SetInt32("health", 100);
```

### SetUInt32

```csharp
void SetUInt32(string key, uint value)
```

**参数:**

- `key` (`string`)
- `value` (`uint`)

**用法示例:**
```csharp
entityKeyValues.SetUInt32("round_time", 120);
```

### SetInt64

```csharp
void SetInt64(string key, long value)
```

**参数:**

- `key` (`string`)
- `value` (`long`)

**用法示例:**
```csharp
entityKeyValues.SetInt64("score", 100L);
```

### SetUInt64

```csharp
void SetUInt64(string key, ulong value)
```

**参数:**

- `key` (`string`)
- `value` (`ulong`)

**用法示例:**
```csharp
entityKeyValues.SetUInt64("match_id", 1234567890UL);
```

### SetFloat

```csharp
void SetFloat(string key, float value)
```

**参数:**

- `key` (`string`)
- `value` (`float`)

**用法示例:**
```csharp
entityKeyValues.SetFloat("health", 100.5f);
```

### SetDouble

```csharp
void SetDouble(string key, double value)
```

**参数:**

- `key` (`string`)
- `value` (`double`)

**用法示例:**
```csharp
entityKeyValues.SetDouble("health", 100.5);
```

### SetString

```csharp
void SetString(string key, string value)
```

**参数:**

- `key` (`string`)
- `value` (`string`)

**用法示例:**
```csharp
entityKeyValues.SetString("targetname", "my_entity");
```

### SetPtr

```csharp
void SetPtr(string key, nint value)
```

**参数:**

- `key` (`string`)
- `value` (`nint`)

**用法示例:**
```csharp
entityKeyValues.SetPtr("hMyEntity", someIntPtr);
```

### SetStringToken

```csharp
void SetStringToken(string key, CUtlStringToken value)
```

**参数:**

- `key` (`string`)
- `value` (`CUtlStringToken`)

**用法示例:**
```csharp
entityKeyValues.SetStringToken("name", CUtlStringToken.PlayerName);
```

### SetColor

```csharp
void SetColor(string key, Color value)
```

**参数:**

- `key` (`string`)
- `value` (`Color`)

**用法示例:**
```csharp
entityKeyValues.SetColor("light_color", Color.Red);
```

### SetVector

```csharp
void SetVector(string key, Vector value)
```

**参数:**

- `key` (`string`)
- `value` (`Vector`)

**用法示例:**
```csharp
entityKeyValues.SetVector("origin", new Vector(100, 200, 300));
```

### SetVector2D

```csharp
void SetVector2D(string key, Vector2D value)
```

**参数:**

- `key` (`string`)
- `value` (`Vector2D`)

**用法示例:**
```csharp
entityKeyValues.SetVector2D("position", new Vector2D(10.5f, 20.3f));
```

### SetVector4D

```csharp
void SetVector4D(string key, Vector4D value)
```

**参数:**

- `key` (`string`)
- `value` (`Vector4D`)

**用法示例:**
```csharp
entityKeyValues.SetVector4D("position", new Vector4D(1.0f, 2.0f, 3.0f, 4.0f));
```

### SetQAngle

```csharp
void SetQAngle(string key, QAngle value)
```

**参数:**

- `key` (`string`)
- `value` (`QAngle`)

**用法示例:**
```csharp
entityKeyValues.SetQAngle("m_angRotation", new QAngle(0f, 90f, 0f));
```

### GetBool

```csharp
bool GetBool(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool isActive = entityKeyValues.GetBool("m_bIsAlive");
```

### GetInt32

```csharp
int GetInt32(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `int`

**用法示例:**
```csharp
int health = entityKeyValues.GetInt32("health");
```

### GetUInt32

```csharp
uint GetUInt32(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `uint`

**用法示例:**
```csharp
uint value = entityKeyValues.GetUInt32("m_iHealth");
```

### GetInt64

```csharp
long GetInt64(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `long`

**用法示例:**
```csharp
long value = entityKeyValues.GetInt64("health");
```

### GetUInt64

```csharp
ulong GetUInt64(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `ulong`

**用法示例:**
```csharp
ulong value = entityKeyValues.GetUInt64("m_iHealth");
```

### GetFloat

```csharp
float GetFloat(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `float`

**用法示例:**
```csharp
float value = entityKeyValues.GetFloat("health");
```

### GetDouble

```csharp
double GetDouble(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `double`

**用法示例:**
```csharp
double value = entityKeyValues.GetDouble("health");
```

### GetString

```csharp
string GetString(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `string`

**用法示例:**
```csharp
string value = entityKeyValues.GetString("classname");
```

### GetPtr

```csharp
nint GetPtr(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `nint`

**用法示例:**
```csharp
nint ptr = entityKeyValues.GetPtr("model");
```

### GetStringToken

```csharp
CUtlStringToken GetStringToken(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `CUtlStringToken`

**用法示例:**
```csharp
CUtlStringToken token = entityKeyValues.GetStringToken("targetname");
```

### GetColor

```csharp
Color GetColor(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `Color`

**用法示例:**
```csharp
Color color = entityKeyValues.GetColor("team_color");
```

### GetVector

```csharp
Vector GetVector(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `Vector`

**用法示例:**
```csharp
Vector position = entityKeyValues.GetVector("origin");
```

### GetVector2D

```csharp
Vector2D GetVector2D(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `Vector2D`

**用法示例:**
```csharp
Vector2D pos = entityKeyValues.GetVector2D("origin");
```

### GetVector4D

```csharp
Vector4D GetVector4D(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `Vector4D`

**用法示例:**
```csharp
Vector4D vec = entityKeyValues.GetVector4D("origin");
```

### GetQAngle

```csharp
QAngle GetQAngle(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `QAngle`

**用法示例:**
```csharp
QAngle angle = entityKeyValues.GetQAngle("m_angRotation");
```

### Set<T>

```csharp
void Set<T>(string key, T value)
```

**参数:**

- `key` (`string`)
- `value` (`T`)

**用法示例:**
```csharp
entityKeyValues.Set("health", 100);
```

### Get<T>

```csharp
T Get<T>(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `T`

**用法示例:**
```csharp
var value = entityKeyValues.Get<int>("m_iHealth");
```

