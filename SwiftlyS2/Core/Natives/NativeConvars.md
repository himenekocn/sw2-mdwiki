# 📦 NativeConvars

**命名空间:** `SwiftlyS2.Core.Natives`

**类型:** `class`

## ⚙️ 方法

### QueryClientConvar (静态)

```csharp
void QueryClientConvar(int playerid, string cvarName)
```

**参数:**

- `playerid` (`int`)
- `cvarName` (`string`)

### AddQueryClientCvarCallback (静态)

```csharp
int AddQueryClientCvarCallback(nint callback)
```

the callback should receive the following: int32 playerid, string cvarName, string cvarValue

**参数:**

- `callback` (`nint`)

**返回值:** `int`

### RemoveQueryClientCvarCallback (静态)

```csharp
void RemoveQueryClientCvarCallback(int callbackID)
```

**参数:**

- `callbackID` (`int`)

### AddGlobalChangeListener (静态)

```csharp
ulong AddGlobalChangeListener(nint callback)
```

the callback should receive the following: string convarName, int playerid, string newValue, string oldValue

**参数:**

- `callback` (`nint`)

**返回值:** `ulong`

### RemoveGlobalChangeListener (静态)

```csharp
void RemoveGlobalChangeListener(ulong callbackID)
```

**参数:**

- `callbackID` (`ulong`)

### AddConvarCreatedListener (静态)

```csharp
ulong AddConvarCreatedListener(nint callback)
```

the callback should receive the following: string convarName

**参数:**

- `callback` (`nint`)

**返回值:** `ulong`

### RemoveConvarCreatedListener (静态)

```csharp
void RemoveConvarCreatedListener(ulong callbackID)
```

**参数:**

- `callbackID` (`ulong`)

### AddConCommandCreatedListener (静态)

```csharp
ulong AddConCommandCreatedListener(nint callback)
```

the callback should receive the following: string commandName

**参数:**

- `callback` (`nint`)

**返回值:** `ulong`

### RemoveConCommandCreatedListener (静态)

```csharp
void RemoveConCommandCreatedListener(ulong callbackID)
```

**参数:**

- `callbackID` (`ulong`)

### CreateConvarInt16 (静态)

```csharp
void CreateConvarInt16(string cvarName, int cvarType, ulong cvarFlags, string helpMessage, short defaultValue, nint minValue, nint maxValue)
```

**参数:**

- `cvarName` (`string`)
- `cvarType` (`int`)
- `cvarFlags` (`ulong`)
- `helpMessage` (`string`)
- `defaultValue` (`short`)
- `minValue` (`nint`)
- `maxValue` (`nint`)

### CreateConvarUInt16 (静态)

```csharp
void CreateConvarUInt16(string cvarName, int cvarType, ulong cvarFlags, string helpMessage, ushort defaultValue, nint minValue, nint maxValue)
```

**参数:**

- `cvarName` (`string`)
- `cvarType` (`int`)
- `cvarFlags` (`ulong`)
- `helpMessage` (`string`)
- `defaultValue` (`ushort`)
- `minValue` (`nint`)
- `maxValue` (`nint`)

### CreateConvarInt32 (静态)

```csharp
void CreateConvarInt32(string cvarName, int cvarType, ulong cvarFlags, string helpMessage, int defaultValue, nint minValue, nint maxValue)
```

**参数:**

- `cvarName` (`string`)
- `cvarType` (`int`)
- `cvarFlags` (`ulong`)
- `helpMessage` (`string`)
- `defaultValue` (`int`)
- `minValue` (`nint`)
- `maxValue` (`nint`)

### CreateConvarUInt32 (静态)

```csharp
void CreateConvarUInt32(string cvarName, int cvarType, ulong cvarFlags, string helpMessage, uint defaultValue, nint minValue, nint maxValue)
```

**参数:**

- `cvarName` (`string`)
- `cvarType` (`int`)
- `cvarFlags` (`ulong`)
- `helpMessage` (`string`)
- `defaultValue` (`uint`)
- `minValue` (`nint`)
- `maxValue` (`nint`)

### CreateConvarInt64 (静态)

```csharp
void CreateConvarInt64(string cvarName, int cvarType, ulong cvarFlags, string helpMessage, long defaultValue, nint minValue, nint maxValue)
```

**参数:**

- `cvarName` (`string`)
- `cvarType` (`int`)
- `cvarFlags` (`ulong`)
- `helpMessage` (`string`)
- `defaultValue` (`long`)
- `minValue` (`nint`)
- `maxValue` (`nint`)

### CreateConvarUInt64 (静态)

```csharp
void CreateConvarUInt64(string cvarName, int cvarType, ulong cvarFlags, string helpMessage, ulong defaultValue, nint minValue, nint maxValue)
```

**参数:**

- `cvarName` (`string`)
- `cvarType` (`int`)
- `cvarFlags` (`ulong`)
- `helpMessage` (`string`)
- `defaultValue` (`ulong`)
- `minValue` (`nint`)
- `maxValue` (`nint`)

### CreateConvarBool (静态)

```csharp
void CreateConvarBool(string cvarName, int cvarType, ulong cvarFlags, string helpMessage, bool defaultValue, nint minValue, nint maxValue)
```

**参数:**

- `cvarName` (`string`)
- `cvarType` (`int`)
- `cvarFlags` (`ulong`)
- `helpMessage` (`string`)
- `defaultValue` (`bool`)
- `minValue` (`nint`)
- `maxValue` (`nint`)

### CreateConvarFloat (静态)

```csharp
void CreateConvarFloat(string cvarName, int cvarType, ulong cvarFlags, string helpMessage, float defaultValue, nint minValue, nint maxValue)
```

**参数:**

- `cvarName` (`string`)
- `cvarType` (`int`)
- `cvarFlags` (`ulong`)
- `helpMessage` (`string`)
- `defaultValue` (`float`)
- `minValue` (`nint`)
- `maxValue` (`nint`)

### CreateConvarDouble (静态)

```csharp
void CreateConvarDouble(string cvarName, int cvarType, ulong cvarFlags, string helpMessage, double defaultValue, nint minValue, nint maxValue)
```

**参数:**

- `cvarName` (`string`)
- `cvarType` (`int`)
- `cvarFlags` (`ulong`)
- `helpMessage` (`string`)
- `defaultValue` (`double`)
- `minValue` (`nint`)
- `maxValue` (`nint`)

### CreateConvarColor (静态)

```csharp
void CreateConvarColor(string cvarName, int cvarType, ulong cvarFlags, string helpMessage, Color defaultValue, nint minValue, nint maxValue)
```

**参数:**

- `cvarName` (`string`)
- `cvarType` (`int`)
- `cvarFlags` (`ulong`)
- `helpMessage` (`string`)
- `defaultValue` (`Color`)
- `minValue` (`nint`)
- `maxValue` (`nint`)

### CreateConvarVector2D (静态)

```csharp
void CreateConvarVector2D(string cvarName, int cvarType, ulong cvarFlags, string helpMessage, Vector2D defaultValue, nint minValue, nint maxValue)
```

**参数:**

- `cvarName` (`string`)
- `cvarType` (`int`)
- `cvarFlags` (`ulong`)
- `helpMessage` (`string`)
- `defaultValue` (`Vector2D`)
- `minValue` (`nint`)
- `maxValue` (`nint`)

### CreateConvarVector (静态)

```csharp
void CreateConvarVector(string cvarName, int cvarType, ulong cvarFlags, string helpMessage, Vector defaultValue, nint minValue, nint maxValue)
```

**参数:**

- `cvarName` (`string`)
- `cvarType` (`int`)
- `cvarFlags` (`ulong`)
- `helpMessage` (`string`)
- `defaultValue` (`Vector`)
- `minValue` (`nint`)
- `maxValue` (`nint`)

### CreateConvarVector4D (静态)

```csharp
void CreateConvarVector4D(string cvarName, int cvarType, ulong cvarFlags, string helpMessage, Vector4D defaultValue, nint minValue, nint maxValue)
```

**参数:**

- `cvarName` (`string`)
- `cvarType` (`int`)
- `cvarFlags` (`ulong`)
- `helpMessage` (`string`)
- `defaultValue` (`Vector4D`)
- `minValue` (`nint`)
- `maxValue` (`nint`)

### CreateConvarQAngle (静态)

```csharp
void CreateConvarQAngle(string cvarName, int cvarType, ulong cvarFlags, string helpMessage, QAngle defaultValue, nint minValue, nint maxValue)
```

**参数:**

- `cvarName` (`string`)
- `cvarType` (`int`)
- `cvarFlags` (`ulong`)
- `helpMessage` (`string`)
- `defaultValue` (`QAngle`)
- `minValue` (`nint`)
- `maxValue` (`nint`)

### CreateConvarString (静态)

```csharp
void CreateConvarString(string cvarName, int cvarType, ulong cvarFlags, string helpMessage, string defaultValue, nint minValue, nint maxValue)
```

**参数:**

- `cvarName` (`string`)
- `cvarType` (`int`)
- `cvarFlags` (`ulong`)
- `helpMessage` (`string`)
- `defaultValue` (`string`)
- `minValue` (`nint`)
- `maxValue` (`nint`)

### DeleteConvar (静态)

```csharp
void DeleteConvar(string cvarName)
```

**参数:**

- `cvarName` (`string`)

### ExistsConvar (静态)

```csharp
bool ExistsConvar(string cvarName)
```

**参数:**

- `cvarName` (`string`)

**返回值:** `bool`

### GetConvarType (静态)

```csharp
int GetConvarType(string cvarName)
```

**参数:**

- `cvarName` (`string`)

**返回值:** `int`

### SetClientConvarValueString (静态)

```csharp
void SetClientConvarValueString(int playerid, string cvarName, string defaultValue)
```

**参数:**

- `playerid` (`int`)
- `cvarName` (`string`)
- `defaultValue` (`string`)

### GetFlags (静态)

```csharp
ulong GetFlags(string cvarName)
```

**参数:**

- `cvarName` (`string`)

**返回值:** `ulong`

### SetFlags (静态)

```csharp
void SetFlags(string cvarName, ulong flags)
```

**参数:**

- `cvarName` (`string`)
- `flags` (`ulong`)

### GetMinValuePtrPtr (静态)

```csharp
nint GetMinValuePtrPtr(string cvarName)
```

**参数:**

- `cvarName` (`string`)

**返回值:** `nint`

### GetMaxValuePtrPtr (静态)

```csharp
nint GetMaxValuePtrPtr(string cvarName)
```

**参数:**

- `cvarName` (`string`)

**返回值:** `nint`

### HasDefaultValue (静态)

```csharp
bool HasDefaultValue(string cvarName)
```

**参数:**

- `cvarName` (`string`)

**返回值:** `bool`

### GetDefaultValuePtr (静态)

```csharp
nint GetDefaultValuePtr(string cvarName)
```

**参数:**

- `cvarName` (`string`)

**返回值:** `nint`

### SetDefaultValue (静态)

```csharp
void SetDefaultValue(string cvarName, nint defaultValue)
```

**参数:**

- `cvarName` (`string`)
- `defaultValue` (`nint`)

### SetDefaultValueString (静态)

```csharp
void SetDefaultValueString(string cvarName, string defaultValue)
```

**参数:**

- `cvarName` (`string`)
- `defaultValue` (`string`)

### GetValuePtr (静态)

```csharp
nint GetValuePtr(string cvarName)
```

**参数:**

- `cvarName` (`string`)

**返回值:** `nint`

### SetValuePtr (静态)

```csharp
void SetValuePtr(string cvarName, nint value)
```

**参数:**

- `cvarName` (`string`)
- `value` (`nint`)

### SetValueInternalPtr (静态)

```csharp
void SetValueInternalPtr(string cvarName, nint value)
```

**参数:**

- `cvarName` (`string`)
- `value` (`nint`)

### SetValueAsString (静态)

```csharp
bool SetValueAsString(string cvarName, string value)
```

**参数:**

- `cvarName` (`string`)
- `value` (`string`)

**返回值:** `bool`

### GetValueAsString (静态)

```csharp
string GetValueAsString(string cvarName)
```

**参数:**

- `cvarName` (`string`)

**返回值:** `string`

### SetDefaultValueAsString (静态)

```csharp
bool SetDefaultValueAsString(string cvarName, string value)
```

**参数:**

- `cvarName` (`string`)
- `value` (`string`)

**返回值:** `bool`

### GetDefaultValueAsString (静态)

```csharp
string GetDefaultValueAsString(string cvarName)
```

**参数:**

- `cvarName` (`string`)

**返回值:** `string`

### SetMinValueAsString (静态)

```csharp
bool SetMinValueAsString(string cvarName, string value)
```

**参数:**

- `cvarName` (`string`)
- `value` (`string`)

**返回值:** `bool`

### GetMinValueAsString (静态)

```csharp
string GetMinValueAsString(string cvarName)
```

**参数:**

- `cvarName` (`string`)

**返回值:** `string`

### SetMaxValueAsString (静态)

```csharp
bool SetMaxValueAsString(string cvarName, string value)
```

**参数:**

- `cvarName` (`string`)
- `value` (`string`)

**返回值:** `bool`

### GetMaxValueAsString (静态)

```csharp
string GetMaxValueAsString(string cvarName)
```

**参数:**

- `cvarName` (`string`)

**返回值:** `string`

### SetValueInternalAsString (静态)

```csharp
void SetValueInternalAsString(string cvarName, string value)
```

**参数:**

- `cvarName` (`string`)
- `value` (`string`)

### GetDescription (静态)

```csharp
string GetDescription(string cvarName)
```

**参数:**

- `cvarName` (`string`)

**返回值:** `string`

