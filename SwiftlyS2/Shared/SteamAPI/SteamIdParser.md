<a id="steamidparser"></a>

# 📦 SteamIdParser

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### ParseToSteamId64 (静态)

```csharp
ulong? ParseToSteamId64(string input)
```

**参数:**

- `input` (`string`)

**返回值:** `ulong?`

**用法示例:**
```csharp
ulong? steamId = SteamIdParser.ParseToSteamId64("76561198000000000");
```

### TryParseSteamIdOnline (静态)

```csharp
bool TryParseSteamIdOnline(string input, out ulong steamId64)
```

**参数:**

- `input` (`string`)
- `steamId64` (`out ulong`)

**返回值:** `bool`

**用法示例:**
```csharp
if (SteamIdParser.TryParseSteamIdOnline("STEAM_0:1:12345678", out ulong steamId)) { Console.WriteLine(steamId); }
```

### IsValidSteamId64 (静态)

```csharp
bool IsValidSteamId64(ulong steamId64)
```

**参数:**

- `steamId64` (`ulong`)

**返回值:** `bool`

**用法示例:**
```csharp
bool isValid = SteamIdParser.IsValidSteamId64(76561197960287930);
```

### ToSteamId (静态)

```csharp
string ToSteamId(ulong steamId64)
```

**参数:**

- `steamId64` (`ulong`)

**返回值:** `string`

**用法示例:**
```csharp
string steamId = SteamIdParser.ToSteamId(76561198000000000);
```

### ToSteamId3 (静态)

```csharp
string ToSteamId3(ulong steamId64)
```

**参数:**

- `steamId64` (`ulong`)

**返回值:** `string`

**用法示例:**
```csharp
var parser = new SteamIdParser();
string steamId3 = parser.ToSteamId3(76561198000000000);
```

### ToSteamIdOnline (静态)

```csharp
string ToSteamIdOnline(ulong steamId64)
```

**参数:**

- `steamId64` (`ulong`)

**返回值:** `string`

**用法示例:**
```csharp
string onlineId = SteamIdParser.ToSteamIdOnline(76561198000000000);
```

