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

### TryParseSteamIdOnline (静态)

```csharp
bool TryParseSteamIdOnline(string input, out ulong steamId64)
```

**参数:**

- `input` (`string`)
- `steamId64` (`out ulong`)

**返回值:** `bool`

### IsValidSteamId64 (静态)

```csharp
bool IsValidSteamId64(ulong steamId64)
```

**参数:**

- `steamId64` (`ulong`)

**返回值:** `bool`

### ToSteamId (静态)

```csharp
string ToSteamId(ulong steamId64)
```

**参数:**

- `steamId64` (`ulong`)

**返回值:** `string`

### ToSteamId3 (静态)

```csharp
string ToSteamId3(ulong steamId64)
```

**参数:**

- `steamId64` (`ulong`)

**返回值:** `string`

### ToSteamIdOnline (静态)

```csharp
string ToSteamIdOnline(ulong steamId64)
```

**参数:**

- `steamId64` (`ulong`)

**返回值:** `string`

