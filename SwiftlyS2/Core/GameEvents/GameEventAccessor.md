# 📦 GameEventAccessor

**命名空间:** `SwiftlyS2.Core.GameEvents`

**类型:** `class`

**继承:** `NativeHandle`

**实现接口:** `IGameEventAccessor`, `IDisposable`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `DontBroadcast` | `bool` | get, set | - |

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

### GetBool

```csharp
bool GetBool(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `bool`

### SetInt32

```csharp
void SetInt32(string key, int value)
```

**参数:**

- `key` (`string`)
- `value` (`int`)

### GetInt32

```csharp
int GetInt32(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `int`

### SetUInt64

```csharp
void SetUInt64(string key, ulong value)
```

**参数:**

- `key` (`string`)
- `value` (`ulong`)

### GetUInt64

```csharp
ulong GetUInt64(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `ulong`

### SetFloat

```csharp
void SetFloat(string key, float value)
```

**参数:**

- `key` (`string`)
- `value` (`float`)

### GetFloat

```csharp
float GetFloat(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `float`

### SetString

```csharp
void SetString(string key, string value)
```

**参数:**

- `key` (`string`)
- `value` (`string`)

### GetString

```csharp
string GetString(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `string`

### SetEntityIndex

```csharp
void SetEntityIndex(string key, int value)
```

**参数:**

- `key` (`string`)
- `value` (`int`)

### GetEntityIndex

```csharp
int GetEntityIndex(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `int`

### SetPlayerSlot

```csharp
void SetPlayerSlot(string key, int value)
```

**参数:**

- `key` (`string`)
- `value` (`int`)

### GetPlayerSlot

```csharp
int GetPlayerSlot(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `int`

### GetPlayerController

```csharp
CCSPlayerController GetPlayerController(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `CCSPlayerController`

### GetPlayerPawn

```csharp
CCSPlayerPawn GetPlayerPawn(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `CCSPlayerPawn`

### GetPlayer

```csharp
IPlayer? GetPlayer(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `IPlayer?`

### SetPtr

```csharp
void SetPtr(string key, nint value)
```

**参数:**

- `key` (`string`)
- `value` (`nint`)

### GetPtr

```csharp
nint GetPtr(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `nint`

### GetPawnEntityIndex

```csharp
int GetPawnEntityIndex(string key)
```

**参数:**

- `key` (`string`)

**返回值:** `int`

### IsReliable

```csharp
bool IsReliable()
```

**返回值:** `bool`

### IsLocal

```csharp
bool IsLocal()
```

**返回值:** `bool`

