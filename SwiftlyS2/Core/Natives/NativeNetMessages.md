# 📦 NativeNetMessages

**命名空间:** `SwiftlyS2.Core.Natives`

**类型:** `class`

## ⚙️ 方法

### AllocateNetMessageByID (静态)

```csharp
nint AllocateNetMessageByID(int msgid)
```

**参数:**

- `msgid` (`int`)

**返回值:** `nint`

### AllocateNetMessageByPartialName (静态)

```csharp
nint AllocateNetMessageByPartialName(string name)
```

**参数:**

- `name` (`string`)

**返回值:** `nint`

### DeallocateNetMessage (静态)

```csharp
void DeallocateNetMessage(nint netmsg)
```

**参数:**

- `netmsg` (`nint`)

### HasField (静态)

```csharp
bool HasField(nint netmsg, string fieldName)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)

**返回值:** `bool`

### GetInt32 (静态)

```csharp
int GetInt32(nint netmsg, string fieldName)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)

**返回值:** `int`

### GetRepeatedInt32 (静态)

```csharp
int GetRepeatedInt32(nint netmsg, string fieldName, int index)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `int`

### SetInt32 (静态)

```csharp
void SetInt32(nint netmsg, string fieldName, int value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `value` (`int`)

### SetRepeatedInt32 (静态)

```csharp
void SetRepeatedInt32(nint netmsg, string fieldName, int index, int value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)
- `value` (`int`)

### AddInt32 (静态)

```csharp
void AddInt32(nint netmsg, string fieldName, int value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `value` (`int`)

### GetInt64 (静态)

```csharp
long GetInt64(nint netmsg, string fieldName)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)

**返回值:** `long`

### GetRepeatedInt64 (静态)

```csharp
long GetRepeatedInt64(nint netmsg, string fieldName, int index)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `long`

### SetInt64 (静态)

```csharp
void SetInt64(nint netmsg, string fieldName, long value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `value` (`long`)

### SetRepeatedInt64 (静态)

```csharp
void SetRepeatedInt64(nint netmsg, string fieldName, int index, long value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)
- `value` (`long`)

### AddInt64 (静态)

```csharp
void AddInt64(nint netmsg, string fieldName, long value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `value` (`long`)

### GetUInt32 (静态)

```csharp
uint GetUInt32(nint netmsg, string fieldName)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)

**返回值:** `uint`

### GetRepeatedUInt32 (静态)

```csharp
uint GetRepeatedUInt32(nint netmsg, string fieldName, int index)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `uint`

### SetUInt32 (静态)

```csharp
void SetUInt32(nint netmsg, string fieldName, uint value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `value` (`uint`)

### SetRepeatedUInt32 (静态)

```csharp
void SetRepeatedUInt32(nint netmsg, string fieldName, int index, uint value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)
- `value` (`uint`)

### AddUInt32 (静态)

```csharp
void AddUInt32(nint netmsg, string fieldName, uint value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `value` (`uint`)

### GetUInt64 (静态)

```csharp
ulong GetUInt64(nint netmsg, string fieldName)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)

**返回值:** `ulong`

### GetRepeatedUInt64 (静态)

```csharp
ulong GetRepeatedUInt64(nint netmsg, string fieldName, int index)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `ulong`

### SetUInt64 (静态)

```csharp
void SetUInt64(nint netmsg, string fieldName, ulong value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `value` (`ulong`)

### SetRepeatedUInt64 (静态)

```csharp
void SetRepeatedUInt64(nint netmsg, string fieldName, int index, ulong value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)
- `value` (`ulong`)

### AddUInt64 (静态)

```csharp
void AddUInt64(nint netmsg, string fieldName, ulong value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `value` (`ulong`)

### GetBool (静态)

```csharp
bool GetBool(nint netmsg, string fieldName)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)

**返回值:** `bool`

### GetRepeatedBool (静态)

```csharp
bool GetRepeatedBool(nint netmsg, string fieldName, int index)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `bool`

### SetBool (静态)

```csharp
void SetBool(nint netmsg, string fieldName, bool value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `value` (`bool`)

### SetRepeatedBool (静态)

```csharp
void SetRepeatedBool(nint netmsg, string fieldName, int index, bool value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)
- `value` (`bool`)

### AddBool (静态)

```csharp
void AddBool(nint netmsg, string fieldName, bool value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `value` (`bool`)

### GetFloat (静态)

```csharp
float GetFloat(nint netmsg, string fieldName)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)

**返回值:** `float`

### GetRepeatedFloat (静态)

```csharp
float GetRepeatedFloat(nint netmsg, string fieldName, int index)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `float`

### SetFloat (静态)

```csharp
void SetFloat(nint netmsg, string fieldName, float value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `value` (`float`)

### SetRepeatedFloat (静态)

```csharp
void SetRepeatedFloat(nint netmsg, string fieldName, int index, float value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)
- `value` (`float`)

### AddFloat (静态)

```csharp
void AddFloat(nint netmsg, string fieldName, float value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `value` (`float`)

### GetDouble (静态)

```csharp
double GetDouble(nint netmsg, string fieldName)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)

**返回值:** `double`

### GetRepeatedDouble (静态)

```csharp
double GetRepeatedDouble(nint netmsg, string fieldName, int index)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `double`

### SetDouble (静态)

```csharp
void SetDouble(nint netmsg, string fieldName, double value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `value` (`double`)

### SetRepeatedDouble (静态)

```csharp
void SetRepeatedDouble(nint netmsg, string fieldName, int index, double value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)
- `value` (`double`)

### AddDouble (静态)

```csharp
void AddDouble(nint netmsg, string fieldName, double value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `value` (`double`)

### GetString (静态)

```csharp
string GetString(nint netmsg, string fieldName)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)

**返回值:** `string`

### GetRepeatedString (静态)

```csharp
string GetRepeatedString(nint netmsg, string fieldName, int index)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `string`

### SetString (静态)

```csharp
void SetString(nint netmsg, string fieldName, string value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `value` (`string`)

### SetRepeatedString (静态)

```csharp
void SetRepeatedString(nint netmsg, string fieldName, int index, string value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)
- `value` (`string`)

### AddString (静态)

```csharp
void AddString(nint netmsg, string fieldName, string value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `value` (`string`)

### GetVector2D (静态)

```csharp
Vector2D GetVector2D(nint netmsg, string fieldName)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)

**返回值:** `Vector2D`

### GetRepeatedVector2D (静态)

```csharp
Vector2D GetRepeatedVector2D(nint netmsg, string fieldName, int index)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `Vector2D`

### SetVector2D (静态)

```csharp
void SetVector2D(nint netmsg, string fieldName, Vector2D value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `value` (`Vector2D`)

### SetRepeatedVector2D (静态)

```csharp
void SetRepeatedVector2D(nint netmsg, string fieldName, int index, Vector2D value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)
- `value` (`Vector2D`)

### AddVector2D (静态)

```csharp
void AddVector2D(nint netmsg, string fieldName, Vector2D value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `value` (`Vector2D`)

### GetVector (静态)

```csharp
Vector GetVector(nint netmsg, string fieldName)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)

**返回值:** `Vector`

### GetRepeatedVector (静态)

```csharp
Vector GetRepeatedVector(nint netmsg, string fieldName, int index)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `Vector`

### SetVector (静态)

```csharp
void SetVector(nint netmsg, string fieldName, Vector value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `value` (`Vector`)

### SetRepeatedVector (静态)

```csharp
void SetRepeatedVector(nint netmsg, string fieldName, int index, Vector value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)
- `value` (`Vector`)

### AddVector (静态)

```csharp
void AddVector(nint netmsg, string fieldName, Vector value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `value` (`Vector`)

### GetColor (静态)

```csharp
Color GetColor(nint netmsg, string fieldName)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)

**返回值:** `Color`

### GetRepeatedColor (静态)

```csharp
Color GetRepeatedColor(nint netmsg, string fieldName, int index)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `Color`

### SetColor (静态)

```csharp
void SetColor(nint netmsg, string fieldName, Color value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `value` (`Color`)

### SetRepeatedColor (静态)

```csharp
void SetRepeatedColor(nint netmsg, string fieldName, int index, Color value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)
- `value` (`Color`)

### AddColor (静态)

```csharp
void AddColor(nint netmsg, string fieldName, Color value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `value` (`Color`)

### GetQAngle (静态)

```csharp
QAngle GetQAngle(nint netmsg, string fieldName)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)

**返回值:** `QAngle`

### GetRepeatedQAngle (静态)

```csharp
QAngle GetRepeatedQAngle(nint netmsg, string fieldName, int index)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `QAngle`

### SetQAngle (静态)

```csharp
void SetQAngle(nint netmsg, string fieldName, QAngle value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `value` (`QAngle`)

### SetRepeatedQAngle (静态)

```csharp
void SetRepeatedQAngle(nint netmsg, string fieldName, int index, QAngle value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)
- `value` (`QAngle`)

### AddQAngle (静态)

```csharp
void AddQAngle(nint netmsg, string fieldName, QAngle value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `value` (`QAngle`)

### GetBytes (静态)

```csharp
byte[] GetBytes(nint netmsg, string fieldName)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)

**返回值:** `byte[]`

### GetRepeatedBytes (静态)

```csharp
byte[] GetRepeatedBytes(nint netmsg, string fieldName, int index)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `byte[]`

### SetBytes (静态)

```csharp
void SetBytes(nint netmsg, string fieldName, byte[] value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `value` (`byte[]`)

### SetRepeatedBytes (静态)

```csharp
void SetRepeatedBytes(nint netmsg, string fieldName, int index, byte[] value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)
- `value` (`byte[]`)

### AddBytes (静态)

```csharp
void AddBytes(nint netmsg, string fieldName, byte[] value)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `value` (`byte[]`)

### GetNestedMessage (静态)

```csharp
nint GetNestedMessage(nint netmsg, string fieldName)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)

**返回值:** `nint`

### GetRepeatedNestedMessage (静态)

```csharp
nint GetRepeatedNestedMessage(nint netmsg, string fieldName, int index)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)
- `index` (`int`)

**返回值:** `nint`

### AddNestedMessage (静态)

```csharp
nint AddNestedMessage(nint netmsg, string fieldName)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)

**返回值:** `nint`

### GetRepeatedFieldSize (静态)

```csharp
int GetRepeatedFieldSize(nint netmsg, string fieldName)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)

**返回值:** `int`

### ClearRepeatedField (静态)

```csharp
void ClearRepeatedField(nint netmsg, string fieldName)
```

**参数:**

- `netmsg` (`nint`)
- `fieldName` (`string`)

### Clear (静态)

```csharp
void Clear(nint netmsg)
```

**参数:**

- `netmsg` (`nint`)

### SendMessage (静态)

```csharp
void SendMessage(nint netmsg, int msgid, int playerid)
```

**参数:**

- `netmsg` (`nint`)
- `msgid` (`int`)
- `playerid` (`int`)

### SendMessageToPlayers (静态)

```csharp
void SendMessageToPlayers(nint netmsg, int msgid, ulong playermask)
```

each bit in player_mask represents a playerid

**参数:**

- `netmsg` (`nint`)
- `msgid` (`int`)
- `playermask` (`ulong`)

### AddNetMessageServerHook (静态)

```csharp
ulong AddNetMessageServerHook(nint callback)
```

the callback should receive the following: uint64* playermask_ptr, int netmessage_id, void* netmsg, return bool (true -> ignored, false -> supercede)

**参数:**

- `callback` (`nint`)

**返回值:** `ulong`

### RemoveNetMessageServerHook (静态)

```csharp
void RemoveNetMessageServerHook(ulong callbackID)
```

**参数:**

- `callbackID` (`ulong`)

### AddNetMessageClientHook (静态)

```csharp
ulong AddNetMessageClientHook(nint callback)
```

the callback should receive the following: int32 playerid, int netmessage_id, void* netmsg, return bool (true -> ignored, false -> supercede)

**参数:**

- `callback` (`nint`)

**返回值:** `ulong`

### RemoveNetMessageClientHook (静态)

```csharp
void RemoveNetMessageClientHook(ulong callbackID)
```

**参数:**

- `callbackID` (`ulong`)

### AddNetMessageServerHookInternal (静态)

```csharp
ulong AddNetMessageServerHookInternal(nint callback)
```

callback should receive the following: int32 playerid, int netmessage_id, void* netmsg, return bool (true -> ignored, false -> supercede)

**参数:**

- `callback` (`nint`)

**返回值:** `ulong`

### RemoveNetMessageServerHookInternal (静态)

```csharp
void RemoveNetMessageServerHookInternal(ulong callbackID)
```

**参数:**

- `callbackID` (`ulong`)

