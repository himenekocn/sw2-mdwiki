<a id="iprotobufaccessor"></a>

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
bool exists = accessor.HasField("player_id");
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
accessor.SetBool("isActive", true);
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
accessor.AddBool("isEnabled", true);
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
accessor.SetRepeatedBool("flags", 0, true);
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
bool value = accessor.GetRepeatedBool("myField", 0);
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
bool value = accessor.GetBool("isActive");
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
accessor.SetInt32("player_id", 1001);
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
accessor.AddInt32("score", 100);
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
accessor.SetRepeatedInt32("scores", 0, 100);
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
int value = accessor.GetRepeatedInt32("scores", 0);
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
int value = accessor.GetInt32("field_name");
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
accessor.SetUInt32("score", 100);
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
accessor.AddUInt32("score", 100);
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
accessor.SetRepeatedUInt32("scores", 0, 100);
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
uint value = accessor.GetRepeatedUInt32("field", 0);
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
uint value = accessor.GetUInt32("field_name");
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
accessor.SetInt64("timestamp", 1234567890L);
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
accessor.AddInt64("timestamp", 1234567890L);
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
accessor.SetRepeatedInt64("scores", 0, 100L);
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
long value = accessor.GetRepeatedInt64("my_field", 0);
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
long value = accessor.GetInt64("field_name");
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
accessor.SetUInt64("score", 100UL);
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
accessor.AddUInt64("score", 100UL);
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
accessor.SetRepeatedUInt64("scores", 0, 100UL);
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
ulong value = accessor.GetRepeatedUInt64("field_name", 0);
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
ulong value = accessor.GetUInt64("myField");
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
accessor.SetFloat("height", 1.85f);
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
accessor.AddFloat("temperature", 36.5f);
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
accessor.SetRepeatedFloat("scores", 0, 95.5f);
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
float value = accessor.GetRepeatedFloat("scores", 0);
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
float value = accessor.GetFloat("field_name");
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
accessor.SetDouble("score", 100.5);
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
accessor.AddDouble("score", 95.5);
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
accessor.SetRepeatedDouble("scores", 0, 98.5);
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
double value = accessor.GetRepeatedDouble("scores", 0);
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
double value = accessor.GetDouble("score");
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
accessor.SetString("name", "SwiftlyS2");
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
accessor.AddString("name", "SwiftlyS2");
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
accessor.SetRepeatedString("tags", 0, "admin");
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
string value = accessor.GetRepeatedString("tags", 0);
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
string value = accessor.GetString("name");
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
accessor.SetBytes("data", new byte[] { 0x01, 0x02 });
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
accessor.AddBytes("data", new byte[] { 0x01, 0x02 });
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
accessor.SetRepeatedBytes("data", 0, new byte[] { 1, 2, 3 });
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
var data = accessor.GetRepeatedBytes("items", 0);
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
byte[] data = accessor.GetBytes("field_name");
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
accessor.SetVector2D("position", new Vector2D(1.0f, 2.0f));
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
accessor.AddVector2D("position", new Vector2D(1.0f, 2.0f));
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
accessor.SetRepeatedVector2D("positions", 0, Vector2D.Zero);
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
var pos = accessor.GetRepeatedVector2D("positions", 0);
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
Vector2D pos = accessor.GetVector2D("position");
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
accessor.SetVector("position", new Vector(1.0f, 2.0f, 3.0f));
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
accessor.AddVector("position", new Vector(1.0f, 2.0f, 3.0f));
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
accessor.SetRepeatedVector("positions", 0, Vector.Zero);
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
Vector vec = accessor.GetRepeatedVector("positions", 0);
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
Vector vec = accessor.GetVector("position");
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
accessor.SetColor("primary", Color.Red);
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
accessor.AddColor("background", Color.Red);
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
accessor.SetRepeatedColor("colors", 0, Color.Red);
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
var color = accessor.GetRepeatedColor("colors", 0);
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
Color color = accessor.GetColor("primary_color");
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
accessor.SetQAngle("view_angles", new QAngle(0, 90, 0));
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
accessor.AddQAngle("view_angles", QAngle.Zero);
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
accessor.SetRepeatedQAngle("angles", 0, new QAngle(0f, 90f, 0f));
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
QAngle angle = accessor.GetQAngle("view_angles");
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
var nestedPtr = accessor.GetNestedMessage("player_info");
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
var ptr = accessor.GetRepeatedNestedMessage("items", 0);
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
var nestedHandle = accessor.AddNestedMessage("sub_message");
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
int size = accessor.GetRepeatedFieldSize("items");
```

### ClearRepeatedField

```csharp
void ClearRepeatedField(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**用法示例:**
```csharp
accessor.ClearRepeatedField("items");
```

### Clear

```csharp
void Clear()
```

**用法示例:**
```csharp
protobufAccessor.Clear();
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
accessor.Set("playerName", "Hero");
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
accessor.Add("score", 100);
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
accessor.SetRepeated("items", 0, "value");
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
var item = accessor.GetRepeated<int>("scores", 0);
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
var value = accessor.Get<int>("score");
```

