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
entityKeyValues.SetBool("isEnabled", true);
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
entityKeyValues.SetUInt32("health", 100u);
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
entityKeyValues.SetUInt64("score", 100UL);
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
entityKeyValues.SetFloat("health", 100f);
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
entityKeyValues.SetString("name", "Player1");
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
entityKeyValues.SetPtr("health", (nint)100);
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
entityKeyValues.SetStringToken("playerName", CUtlStringToken.FromString("Alice"));
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
entityKeyValues.SetColor("health_color", Color.Red);
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
CEntityKeyValues.SetVector("origin", new Vector(100, 200, 300));
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
CEntityKeyValues.SetVector2D("position", new Vector2D(10, 20));
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
CEntityKeyValues.SetVector4D("position", new Vector4D(1f, 2f, 3f, 4f));
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
CEntityKeyValues.SetQAngle("angles", new QAngle(0, 90, 0));
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
bool value = entityKeyValues.GetBool("is_visible");
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
int value = entityKeyValues.GetInt32("health");
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
uint value = entityKeyValues.GetUInt32("health");
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
ulong value = entityKeyValues.GetUInt64("health");
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
string value = entityKeyValues.GetString("model");
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
CEntityKeyValues.GetStringToken("health");
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
Color c = entityKeyValues.GetColor("color");
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
Vector pos = entityKeyValues.GetVector("origin");
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
Vector4D v = entityKeyValues.GetVector4D("position");
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
QAngle angle = entityKeyValues.GetQAngle("angles");
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
entityKeyValues.Set("name", "Alice");
entityKeyValues.Set("age", 30);
entityKeyValues.Set("team", Team.T);
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
int value = entityKeyValues.Get<int>("key");
Team team = entityKeyValues.Get<Team>("teamKey");
```

