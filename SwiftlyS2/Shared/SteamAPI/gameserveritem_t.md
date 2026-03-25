<a id="gameserveritem_t"></a>

# 📦 gameserveritem_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_NetAdr` | `servernetadr_t` | - | - |
| `m_nPing` | `int` | - | - |
| `m_bHadSuccessfulResponse` | `bool` | - | - |
| `m_bDoNotRefresh` | `bool` | - | - |
| `m_nAppID` | `uint` | - | - |
| `m_nPlayers` | `int` | - | - |
| `m_nMaxPlayers` | `int` | - | - |
| `m_bPassword` | `bool` | - | - |
| `m_bSecure` | `bool` | - | - |
| `m_nServerVersion` | `int` | - | - |
| `m_steamID` | `CSteamID` | - | - |

## ⚙️ 方法

### GetGameDir

```csharp
string GetGameDir()
```

**返回值:** `string`

**用法示例:**
```csharp
string gameDir = item.GetGameDir();
```

### SetGameDir

```csharp
void SetGameDir(string dir)
```

**参数:**

- `dir` (`string`)

**用法示例:**
```csharp
gameserveritem_t item = serverItem;
item.SetGameDir("csgo");
```

### GetMap

```csharp
string GetMap()
```

**返回值:** `string`

**用法示例:**
```csharp
string map = item.GetMap();
```

### SetMap

```csharp
void SetMap(string map)
```

**参数:**

- `map` (`string`)

**用法示例:**
```csharp
gameserveritem_t item = existingItem;
item.SetMap("de_dust2");
```

### GetGameDescription

```csharp
string GetGameDescription()
```

**返回值:** `string`

**用法示例:**
```csharp
string desc = item.GetGameDescription();
```

### SetGameDescription

```csharp
void SetGameDescription(string desc)
```

**参数:**

- `desc` (`string`)

**用法示例:**
```csharp
serverItem.SetGameDescription("My Server");
```

### GetServerName

```csharp
string GetServerName()
```

**返回值:** `string`

**用法示例:**
```csharp
string serverName = serverItem.GetServerName();
Console.WriteLine(serverName);
```

### SetServerName

```csharp
void SetServerName(string name)
```

**参数:**

- `name` (`string`)

**用法示例:**
```csharp
serverItem.SetServerName("My Server");
```

### GetGameTags

```csharp
string GetGameTags()
```

**返回值:** `string`

**用法示例:**
```csharp
string tags = gameServerItem.GetGameTags();
```

### SetGameTags

```csharp
void SetGameTags(string tags)
```

**参数:**

- `tags` (`string`)

**用法示例:**
```csharp
serverItem.SetGameTags("deathmatch,ranked");
```

### bots

```csharp
of bots(i.e simulated players)
```

**参数:**

- `players` (`i.e simulated`)

**返回值:** `of`

**用法示例:**
```csharp
int botCount = serverItem.bots();
```

### time

```csharp
< time(in unix time)
```

**参数:**

- `time` (`in unix`)

**返回值:** `\<`

**用法示例:**
```csharp
var unixTime = item.time();
```

