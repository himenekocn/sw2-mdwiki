# 📦 ProtobufAccessor

**命名空间:** `SwiftlyS2.Core.NetMessages`

**类型:** `class`

**继承:** `NativeHandle`

**实现接口:** `IProtobufAccessor`

## ⚙️ 方法

### HasField

```csharp
bool HasField(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `bool`

### GetBool

```csharp
bool GetBool(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `bool`

### SetBool

```csharp
void SetBool(string fieldName, bool value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`bool`)

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

### SetInt64

```csharp
void SetInt64(string fieldName, long value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`long`)

### GetInt64

```csharp
long GetInt64(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `long`

### SetUInt64

```csharp
void SetUInt64(string fieldName, ulong value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`ulong`)

### GetUInt64

```csharp
ulong GetUInt64(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `ulong`

### GetFloat

```csharp
float GetFloat(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `float`

### SetFloat

```csharp
void SetFloat(string fieldName, float value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`float`)

### GetDouble

```csharp
double GetDouble(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `double`

### SetDouble

```csharp
void SetDouble(string fieldName, double value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`double`)

### GetString

```csharp
string GetString(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `string`

### SetString

```csharp
void SetString(string fieldName, string value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`string`)

### SetBytes

```csharp
void SetBytes(string fieldName, byte[] value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`byte[]`)

### GetBytes

```csharp
byte[] GetBytes(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `byte[]`

### SetVector2D

```csharp
void SetVector2D(string fieldName, Vector2D value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`Vector2D`)

### GetVector2D

```csharp
Vector2D GetVector2D(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `Vector2D`

### SetVector

```csharp
void SetVector(string fieldName, Vector value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`Vector`)

### GetVector

```csharp
Vector GetVector(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `Vector`

### SetColor

```csharp
void SetColor(string fieldName, Color value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`Color`)

### GetColor

```csharp
Color GetColor(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `Color`

### SetQAngle

```csharp
void SetQAngle(string fieldName, QAngle value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`QAngle`)

### GetQAngle

```csharp
QAngle GetQAngle(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `QAngle`

### GetNestedMessage

```csharp
nint GetNestedMessage(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `nint`

### GetRepeatedBool

```csharp
bool GetRepeatedBool(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `bool`

### SetRepeatedBool

```csharp
void SetRepeatedBool(string fieldName, int index, bool value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`bool`)

### AddBool

```csharp
void AddBool(string fieldName, bool value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`bool`)

### GetRepeatedInt32

```csharp
int GetRepeatedInt32(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `int`

### SetRepeatedInt32

```csharp
void SetRepeatedInt32(string fieldName, int index, int value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`int`)

### AddInt32

```csharp
void AddInt32(string fieldName, int value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`int`)

### GetRepeatedUInt32

```csharp
uint GetRepeatedUInt32(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `uint`

### SetRepeatedUInt32

```csharp
void SetRepeatedUInt32(string fieldName, int index, uint value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`uint`)

### AddUInt32

```csharp
void AddUInt32(string fieldName, uint value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`uint`)

### GetRepeatedInt64

```csharp
long GetRepeatedInt64(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `long`

### SetRepeatedInt64

```csharp
void SetRepeatedInt64(string fieldName, int index, long value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`long`)

### AddInt64

```csharp
void AddInt64(string fieldName, long value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`long`)

### GetRepeatedUInt64

```csharp
ulong GetRepeatedUInt64(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `ulong`

### SetRepeatedUInt64

```csharp
void SetRepeatedUInt64(string fieldName, int index, ulong value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`ulong`)

### AddUInt64

```csharp
void AddUInt64(string fieldName, ulong value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`ulong`)

### GetRepeatedFloat

```csharp
float GetRepeatedFloat(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `float`

### SetRepeatedFloat

```csharp
void SetRepeatedFloat(string fieldName, int index, float value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`float`)

### AddFloat

```csharp
void AddFloat(string fieldName, float value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`float`)

### GetRepeatedDouble

```csharp
double GetRepeatedDouble(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `double`

### SetRepeatedDouble

```csharp
void SetRepeatedDouble(string fieldName, int index, double value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`double`)

### AddDouble

```csharp
void AddDouble(string fieldName, double value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`double`)

### GetRepeatedString

```csharp
string GetRepeatedString(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `string`

### SetRepeatedString

```csharp
void SetRepeatedString(string fieldName, int index, string value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`string`)

### AddString

```csharp
void AddString(string fieldName, string value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`string`)

### GetRepeatedBytes

```csharp
byte[] GetRepeatedBytes(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `byte[]`

### SetRepeatedBytes

```csharp
void SetRepeatedBytes(string fieldName, int index, byte[] value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`byte[]`)

### AddBytes

```csharp
void AddBytes(string fieldName, byte[] value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`byte[]`)

### GetRepeatedVector2D

```csharp
Vector2D GetRepeatedVector2D(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `Vector2D`

### SetRepeatedVector2D

```csharp
void SetRepeatedVector2D(string fieldName, int index, Vector2D value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`Vector2D`)

### AddVector2D

```csharp
void AddVector2D(string fieldName, Vector2D value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`Vector2D`)

### GetRepeatedVector

```csharp
Vector GetRepeatedVector(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `Vector`

### SetRepeatedVector

```csharp
void SetRepeatedVector(string fieldName, int index, Vector value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`Vector`)

### AddVector

```csharp
void AddVector(string fieldName, Vector value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`Vector`)

### GetRepeatedColor

```csharp
Color GetRepeatedColor(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `Color`

### SetRepeatedColor

```csharp
void SetRepeatedColor(string fieldName, int index, Color value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`Color`)

### AddColor

```csharp
void AddColor(string fieldName, Color value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`Color`)

### GetRepeatedQAngle

```csharp
QAngle GetRepeatedQAngle(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `QAngle`

### SetRepeatedQAngle

```csharp
void SetRepeatedQAngle(string fieldName, int index, QAngle value)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)
- `value` (`QAngle`)

### AddQAngle

```csharp
void AddQAngle(string fieldName, QAngle value)
```

**参数:**

- `fieldName` (`string`)
- `value` (`QAngle`)

### GetRepeatedNestedMessage

```csharp
nint GetRepeatedNestedMessage(string fieldName, int index)
```

**参数:**

- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `nint`

### AddNestedMessage

```csharp
nint AddNestedMessage(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `nint`

### GetRepeatedFieldSize

```csharp
int GetRepeatedFieldSize(string fieldName)
```

**参数:**

- `fieldName` (`string`)

**返回值:** `int`

### ClearRepeatedField

```csharp
void ClearRepeatedField(string fieldName)
```

**参数:**

- `fieldName` (`string`)

### Clear

```csharp
void Clear()
```

