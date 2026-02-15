# 📦 NativeGameEvents

**命名空间:** `SwiftlyS2.Core.Natives`

**类型:** `class`

## ⚙️ 方法

### GetBool (静态)

```csharp
bool GetBool(nint _event, string key)
```

**参数:**

- `_event` (`nint`)
- `key` (`string`)

**返回值:** `bool`

### GetInt (静态)

```csharp
int GetInt(nint _event, string key)
```

**参数:**

- `_event` (`nint`)
- `key` (`string`)

**返回值:** `int`

### GetUint64 (静态)

```csharp
ulong GetUint64(nint _event, string key)
```

**参数:**

- `_event` (`nint`)
- `key` (`string`)

**返回值:** `ulong`

### GetFloat (静态)

```csharp
float GetFloat(nint _event, string key)
```

**参数:**

- `_event` (`nint`)
- `key` (`string`)

**返回值:** `float`

### GetString (静态)

```csharp
string GetString(nint _event, string key)
```

**参数:**

- `_event` (`nint`)
- `key` (`string`)

**返回值:** `string`

### GetPtr (静态)

```csharp
nint GetPtr(nint _event, string key)
```

**参数:**

- `_event` (`nint`)
- `key` (`string`)

**返回值:** `nint`

### GetEHandle (静态)

```csharp
nint GetEHandle(nint _event, string key)
```

returns the pointer stored inside the handle

**参数:**

- `_event` (`nint`)
- `key` (`string`)

**返回值:** `nint`

### GetEntity (静态)

```csharp
nint GetEntity(nint _event, string key)
```

**参数:**

- `_event` (`nint`)
- `key` (`string`)

**返回值:** `nint`

### GetEntityIndex (静态)

```csharp
int GetEntityIndex(nint _event, string key)
```

**参数:**

- `_event` (`nint`)
- `key` (`string`)

**返回值:** `int`

### GetPlayerSlot (静态)

```csharp
int GetPlayerSlot(nint _event, string key)
```

**参数:**

- `_event` (`nint`)
- `key` (`string`)

**返回值:** `int`

### GetPlayerController (静态)

```csharp
nint GetPlayerController(nint _event, string key)
```

**参数:**

- `_event` (`nint`)
- `key` (`string`)

**返回值:** `nint`

### GetPlayerPawn (静态)

```csharp
nint GetPlayerPawn(nint _event, string key)
```

**参数:**

- `_event` (`nint`)
- `key` (`string`)

**返回值:** `nint`

### GetPawnEHandle (静态)

```csharp
nint GetPawnEHandle(nint _event, string key)
```

returns the pointer stored inside the handle

**参数:**

- `_event` (`nint`)
- `key` (`string`)

**返回值:** `nint`

### GetPawnEntityIndex (静态)

```csharp
int GetPawnEntityIndex(nint _event, string key)
```

**参数:**

- `_event` (`nint`)
- `key` (`string`)

**返回值:** `int`

### SetBool (静态)

```csharp
void SetBool(nint _event, string key, bool value)
```

**参数:**

- `_event` (`nint`)
- `key` (`string`)
- `value` (`bool`)

### SetInt (静态)

```csharp
void SetInt(nint _event, string key, int value)
```

**参数:**

- `_event` (`nint`)
- `key` (`string`)
- `value` (`int`)

### SetUint64 (静态)

```csharp
void SetUint64(nint _event, string key, ulong value)
```

**参数:**

- `_event` (`nint`)
- `key` (`string`)
- `value` (`ulong`)

### SetFloat (静态)

```csharp
void SetFloat(nint _event, string key, float value)
```

**参数:**

- `_event` (`nint`)
- `key` (`string`)
- `value` (`float`)

### SetString (静态)

```csharp
void SetString(nint _event, string key, string value)
```

**参数:**

- `_event` (`nint`)
- `key` (`string`)
- `value` (`string`)

### SetPtr (静态)

```csharp
void SetPtr(nint _event, string key, nint value)
```

**参数:**

- `_event` (`nint`)
- `key` (`string`)
- `value` (`nint`)

### SetEntity (静态)

```csharp
void SetEntity(nint _event, string key, nint value)
```

**参数:**

- `_event` (`nint`)
- `key` (`string`)
- `value` (`nint`)

### SetEntityIndex (静态)

```csharp
void SetEntityIndex(nint _event, string key, int value)
```

**参数:**

- `_event` (`nint`)
- `key` (`string`)
- `value` (`int`)

### SetPlayerSlot (静态)

```csharp
void SetPlayerSlot(nint _event, string key, int value)
```

**参数:**

- `_event` (`nint`)
- `key` (`string`)
- `value` (`int`)

### HasKey (静态)

```csharp
bool HasKey(nint _event, string key)
```

**参数:**

- `_event` (`nint`)
- `key` (`string`)

**返回值:** `bool`

### IsReliable (静态)

```csharp
bool IsReliable(nint _event)
```

**参数:**

- `_event` (`nint`)

**返回值:** `bool`

### IsLocal (静态)

```csharp
bool IsLocal(nint _event)
```

**参数:**

- `_event` (`nint`)

**返回值:** `bool`

### RegisterListener (静态)

```csharp
void RegisterListener(string eventName)
```

**参数:**

- `eventName` (`string`)

### AddListenerPreCallback (静态)

```csharp
ulong AddListenerPreCallback(nint callback)
```

the callback should receive the following: uint32 eventNameHash, IntPtr gameEvent, bool* dontBroadcast, return bool (true -> ignored, false -> supercede)

**参数:**

- `callback` (`nint`)

**返回值:** `ulong`

### AddListenerPostCallback (静态)

```csharp
ulong AddListenerPostCallback(nint callback)
```

the callback should receive the following: uint32 eventNameHash, IntPtr gameEvent, bool* dontBroadcast, return bool (true -> ignored, false -> supercede)

**参数:**

- `callback` (`nint`)

**返回值:** `ulong`

### RemoveListenerPreCallback (静态)

```csharp
void RemoveListenerPreCallback(ulong listenerID)
```

**参数:**

- `listenerID` (`ulong`)

### RemoveListenerPostCallback (静态)

```csharp
void RemoveListenerPostCallback(ulong listenerID)
```

**参数:**

- `listenerID` (`ulong`)

### CreateEvent (静态)

```csharp
nint CreateEvent(string eventName)
```

**参数:**

- `eventName` (`string`)

**返回值:** `nint`

### FreeEvent (静态)

```csharp
void FreeEvent(nint _event)
```

**参数:**

- `_event` (`nint`)

### FireEvent (静态)

```csharp
void FireEvent(nint _event, bool dontBroadcast)
```

**参数:**

- `_event` (`nint`)
- `dontBroadcast` (`bool`)

### FireEventToClient (静态)

```csharp
void FireEventToClient(nint _event, int playerid)
```

**参数:**

- `_event` (`nint`)
- `playerid` (`int`)

### IsPlayerListeningToEventName (静态)

```csharp
bool IsPlayerListeningToEventName(int playerid, string eventName)
```

**参数:**

- `playerid` (`int`)
- `eventName` (`string`)

**返回值:** `bool`

### IsPlayerListeningToEvent (静态)

```csharp
bool IsPlayerListeningToEvent(int playerid, nint _event)
```

**参数:**

- `playerid` (`int`)
- `_event` (`nint`)

**返回值:** `bool`

