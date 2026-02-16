# 🔌 IProtobufAccessor

**命名空间:** `SwiftlyS2.Shared.NetMessages`

**类型:** `interface`

**继承:** `INativeHandle`

## ⚙️ 方法

### HasField

```csharp
bool HasField(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool hasField = player.HasField("name");
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
convar.SetBool("isEnabled", true);
```

### AddBool

```csharp
void AddBool(string fieldName, bool value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`bool`)

**用法示例:**
```csharp
convar.AddBool("isEnabled", true);
```

### SetRepeatedBool

```csharp
void SetRepeatedBool(string fieldName, int index, bool value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`bool`)

**用法示例:**
```csharp
convar.SetRepeatedBool("flags", 0, true);
```

### GetRepeatedBool

```csharp
bool GetRepeatedBool(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `bool`

**用法示例:**
```csharp
bool value = IProtobufAccessor.GetRepeatedBool("isActive", 0);
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
bool value = convar.GetBool("enabled");
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
convar.SetInt32("health", 100);
```

### AddInt32

```csharp
void AddInt32(string fieldName, int value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`int`)

**用法示例:**
```csharp
convar.AddInt32("score", 100);
```

### SetRepeatedInt32

```csharp
void SetRepeatedInt32(string fieldName, int index, int value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`int`)

**用法示例:**
```csharp
convar.SetRepeatedInt32("scores", 0, 10);
```

### GetRepeatedInt32

```csharp
int GetRepeatedInt32(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `int`

**用法示例:**
```csharp
int value = convar.GetRepeatedInt32("scores", 0);
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
int value = convar.GetInt32("someField");
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
convar.SetUInt32("maxPlayers", 32);
```

### AddUInt32

```csharp
void AddUInt32(string fieldName, uint value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`uint`)

**用法示例:**
```csharp
convar.AddUInt32("score", 100u);
```

### SetRepeatedUInt32

```csharp
void SetRepeatedUInt32(string fieldName, int index, uint value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`uint`)

**用法示例:**
```csharp
convar.SetRepeatedUInt32("scores", 0, 0);
```

### GetRepeatedUInt32

```csharp
uint GetRepeatedUInt32(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `uint`

**用法示例:**
```csharp
uint value = convar.GetRepeatedUInt32("scores", 0);
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
uint value = convar.GetUInt32("maxPlayers");
```

### SetInt64

```csharp
void SetInt64(string fieldName, long value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`long`)

**用法示例:**
```csharp
convar.SetInt64("score", 100L);
```

### AddInt64

```csharp
void AddInt64(string fieldName, long value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`long`)

**用法示例:**
```csharp
convar.AddInt64("score", 100L);
```

### SetRepeatedInt64

```csharp
void SetRepeatedInt64(string fieldName, int index, long value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`long`)

**用法示例:**
```csharp
convar.SetRepeatedInt64("scores", 0, 100L);
```

### GetRepeatedInt64

```csharp
long GetRepeatedInt64(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `long`

**用法示例:**
```csharp
long value = convar.GetRepeatedInt64("scores", 0);
```

### GetInt64

```csharp
long GetInt64(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `long`

**用法示例:**
```csharp
long value = player.GetInt64("health");
```

### SetUInt64

```csharp
void SetUInt64(string fieldName, ulong value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`ulong`)

**用法示例:**
```csharp
convar.SetUInt64("Score", 100UL);
```

### AddUInt64

```csharp
void AddUInt64(string fieldName, ulong value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`ulong`)

**用法示例:**
```csharp
convar.AddUInt64("score", 100UL);
```

### SetRepeatedUInt64

```csharp
void SetRepeatedUInt64(string fieldName, int index, ulong value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`ulong`)

**用法示例:**
```csharp
convar.SetRepeatedUInt64("scores", 0, 100UL);
```

### GetRepeatedUInt64

```csharp
ulong GetRepeatedUInt64(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `ulong`

**用法示例:**
```csharp
ulong value = convar.GetRepeatedUInt64("scores", 0);
```

### GetUInt64

```csharp
ulong GetUInt64(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `ulong`

**用法示例:**
```csharp
ulong value = convar.GetUInt64("someField");
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
convar.SetFloat("health", 100f);
```

### AddFloat

```csharp
void AddFloat(string fieldName, float value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`float`)

**用法示例:**
```csharp
convar.AddFloat("speed", 3.14f);
```

### SetRepeatedFloat

```csharp
void SetRepeatedFloat(string fieldName, int index, float value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`float`)

**用法示例:**
```csharp
convar.SetRepeatedFloat("positions", 0, 1.5f);
```

### GetRepeatedFloat

```csharp
float GetRepeatedFloat(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `float`

**用法示例:**
```csharp
float value = convar.GetRepeatedFloat("speeds", 2);
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
float value = convar.GetFloat("health");
```

### SetDouble

```csharp
void SetDouble(string fieldName, double value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`double`)

**用法示例:**
```csharp
convar.SetDouble("speed", 10.5);
```

### AddDouble

```csharp
void AddDouble(string fieldName, double value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`double`)

**用法示例:**
```csharp
convar.AddDouble("speed", 10.5);
```

### SetRepeatedDouble

```csharp
void SetRepeatedDouble(string fieldName, int index, double value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`double`)

**用法示例:**
```csharp
convar.SetRepeatedDouble("scores", 0, 95.5);
```

### GetRepeatedDouble

```csharp
double GetRepeatedDouble(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `double`

**用法示例:**
```csharp
double value = IProtobufAccessor.GetRepeatedDouble("scores", 0);
```

### GetDouble

```csharp
double GetDouble(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `double`

**用法示例:**
```csharp
double value = convar.GetDouble("health");
```

### SetString

```csharp
void SetString(string fieldName, string value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`string`)

**用法示例:**
```csharp
convar.SetString("username", "Alice");
```

### AddString

```csharp
void AddString(string fieldName, string value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`string`)

**用法示例:**
```csharp
convar.AddString("name", "Alice");
```

### SetRepeatedString

```csharp
void SetRepeatedString(string fieldName, int index, string value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`string`)

**用法示例:**
```csharp
convar.SetRepeatedString("names", 0, "Alice");
```

### GetRepeatedString

```csharp
string GetRepeatedString(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `string`

**用法示例:**
```csharp
string value = convar.GetRepeatedString("names", 0);
```

### GetString

```csharp
string GetString(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `string`

**用法示例:**
```csharp
string value = convar.GetString("player_name");
```

### SetBytes

```csharp
void SetBytes(string fieldName, byte[] value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`byte[]`)

**用法示例:**
```csharp
convar.SetBytes("data", Encoding.UTF8.GetBytes("example"));
```

### AddBytes

```csharp
void AddBytes(string fieldName, byte[] value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`byte[]`)

**用法示例:**
```csharp
IProtobufAccessor.AddBytes("data", new byte[] { 1, 2, 3 });
```

### SetRepeatedBytes

```csharp
void SetRepeatedBytes(string fieldName, int index, byte[] value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`byte[]`)

**用法示例:**
```csharp
IProtobufAccessor.SetRepeatedBytes("data", 0, new byte[] { 1, 2, 3 });
```

### GetRepeatedBytes

```csharp
byte[] GetRepeatedBytes(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `byte[]`

**用法示例:**
```csharp
byte[] data = accessor.GetRepeatedBytes("items", 0);
```

### GetBytes

```csharp
byte[] GetBytes(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `byte[]`

**用法示例:**
```csharp
byte[] data = IProtobufAccessor.GetBytes("fieldName");
```

### SetVector2D

```csharp
void SetVector2D(string fieldName, Vector2D value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`Vector2D`)

**用法示例:**
```csharp
IProtobufAccessor.SetVector2D("position", new Vector2D(10, 20));
```

### AddVector2D

```csharp
void AddVector2D(string fieldName, Vector2D value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`Vector2D`)

**用法示例:**
```csharp
convar.AddVector2D("position", new Vector2D(10, 20));
```

### SetRepeatedVector2D

```csharp
void SetRepeatedVector2D(string fieldName, int index, Vector2D value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`Vector2D`)

**用法示例:**
```csharp
IProtobufAccessor.SetRepeatedVector2D("position", 0, new Vector2D(1.0f, 2.0f));
```

### GetRepeatedVector2D

```csharp
Vector2D GetRepeatedVector2D(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `Vector2D`

**用法示例:**
```csharp
Vector2D pos = accessor.GetRepeatedVector2D("positions", 0);
```

### GetVector2D

```csharp
Vector2D GetVector2D(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `Vector2D`

**用法示例:**
```csharp
Vector2D pos = IProtobufAccessor.GetVector2D("position");
```

### SetVector

```csharp
void SetVector(string fieldName, Vector value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`Vector`)

**用法示例:**
```csharp
convar.SetVector("position", new Vector(1, 2, 3));
```

### AddVector

```csharp
void AddVector(string fieldName, Vector value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`Vector`)

**用法示例:**
```csharp
IProtobufAccessor.AddVector("position", new Vector(1, 2, 3));
```

### SetRepeatedVector

```csharp
void SetRepeatedVector(string fieldName, int index, Vector value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`Vector`)

**用法示例:**
```csharp
convar.SetRepeatedVector("positions", 0, Vector.Zero);
```

### GetRepeatedVector

```csharp
Vector GetRepeatedVector(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `Vector`

**用法示例:**
```csharp
Vector pos = IProtobufAccessor.GetRepeatedVector("positions", 0);
```

### GetVector

```csharp
Vector GetVector(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `Vector`

**用法示例:**
```csharp
Vector pos = IProtobufAccessor.GetVector("position");
```

### SetColor

```csharp
void SetColor(string fieldName, Color value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`Color`)

**用法示例:**
```csharp
convar.SetColor("teamColor", Color.Red);
```

### AddColor

```csharp
void AddColor(string fieldName, Color value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`Color`)

**用法示例:**
```csharp
convar.AddColor("color", Color.Red);
```

### SetRepeatedColor

```csharp
void SetRepeatedColor(string fieldName, int index, Color value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`Color`)

**用法示例:**
```csharp
convar.SetRepeatedColor("colors", 0, Color.Red);
```

### GetRepeatedColor

```csharp
Color GetRepeatedColor(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `Color`

**用法示例:**
```csharp
Color color = convar.GetRepeatedColor("colors", 0);
```

### GetColor

```csharp
Color GetColor(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `Color`

**用法示例:**
```csharp
Color color = convar.GetColor("teamColor");
```

### SetQAngle

```csharp
void SetQAngle(string fieldName, QAngle value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`QAngle`)

**用法示例:**
```csharp
IProtobufAccessor.SetQAngle("angles", new QAngle(0, 90, 0));
```

### AddQAngle

```csharp
void AddQAngle(string fieldName, QAngle value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`QAngle`)

**用法示例:**
```csharp
IProtobufAccessor.AddQAngle("angle", new QAngle(0, 90, 0));
```

### SetRepeatedQAngle

```csharp
void SetRepeatedQAngle(string fieldName, int index, QAngle value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`QAngle`)

**用法示例:**
```csharp
player.SetRepeatedQAngle("angles", 0, QAngle.Zero);
```

### GetRepeatedQAngle

```csharp
QAngle GetRepeatedQAngle(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `QAngle`

**用法示例:**
```csharp
QAngle angle = accessor.GetRepeatedQAngle("angles", 0);
```

### GetQAngle

```csharp
QAngle GetQAngle(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `QAngle`

**用法示例:**
```csharp
QAngle angle = accessor.GetQAngle("rotation");
```

### GetNestedMessage

```csharp
nint GetNestedMessage(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `nint`

**用法示例:**
```csharp
nint nested = IProtobufAccessor.GetNestedMessage("someField");
```

### GetRepeatedNestedMessage

```csharp
nint GetRepeatedNestedMessage(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `nint`

**用法示例:**
```csharp
nint result = accessor.GetRepeatedNestedMessage("items", 0);
```

### AddNestedMessage

```csharp
nint AddNestedMessage(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `nint`

**用法示例:**
```csharp
nint handle = IProtobufAccessor.AddNestedMessage("playerInfo");
```

### GetRepeatedFieldSize

```csharp
int GetRepeatedFieldSize(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `int`

**用法示例:**
```csharp
int size = convar.GetRepeatedFieldSize("players");
```

### ClearRepeatedField

```csharp
void ClearRepeatedField(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**用法示例:**
```csharp
convar.ClearRepeatedField("players");
```

### Clear

```csharp
void Clear()
```

**用法示例:**
```csharp
convar.Clear();
```

### Set<T>

```csharp
void Set<T>(string fieldName, T value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`T`)

**用法示例:**
```csharp
accessor.Set("name", "Alice");
accessor.Set("age", 25);
accessor.Set("team", Team.T);
```

### Add<T>

```csharp
void Add<T>(string fieldName, T value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`T`)

**用法示例:**
```csharp
accessor.Add("name", "Alice");
accessor.Add("age", 25);
accessor.Add("team", Team.T);
```

### SetRepeated<T>

```csharp
void SetRepeated<T>(string fieldName, int index, T value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`T`)

**用法示例:**
```csharp
accessor.SetRepeated("items", 0, 42);
accessor.SetRepeated("teams", 1, Team.T);
```

### GetRepeated<T>

```csharp
T GetRepeated<T>(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `T`

**用法示例:**
```csharp
var item = accessor.GetRepeated<string>("items", 0);
```

### Get<T>

```csharp
T Get<T>(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `T`

**用法示例:**
```csharp
var value = accessor.Get<string>("name");
var team = accessor.Get<Team>("team");
```

