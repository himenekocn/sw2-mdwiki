# 📦 SteamGameServerStats

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### RequestUserStats (静态)

```csharp
SteamAPICall_t RequestUserStats(CSteamID steamIDUser)
```

<para>下载用户的统计数据</para> <para>完成后将返回 GSStatsReceived_t 回调</para> <para>如果用户没有统计数据，GSStatsReceived_t.m_eResult 将被设置为 k_EResultFail</para> <para>这些统计数据仅会为在服务器上游戏的客户端自动更新。对于其他</para> <para>用户，您需要再次调用 RequestUserStats() 来刷新任何数据</para>

**参数:**

- `steamIDUser` (`CSteamID`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamGameServerStats.RequestUserStats(new CSteamID(123456789));
```

### GetUserStat (静态)

```csharp
bool GetUserStat(CSteamID steamIDUser, string pchName, out int pData)
```

为用户请求统计信息，需在成功调用 RequestUserStats() 后使用。

**参数:**

- `steamIDUser` (`CSteamID`)
- `pchName` (`string`)
- `pData` (`out int`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerStats.GetUserStat(steamIDUser, "kills", out int kills);
if (success) Console.WriteLine($"Kills: {kills}");
```

### GetUserStat (静态)

```csharp
bool GetUserStat(CSteamID steamIDUser, string pchName, out float pData)
```

**参数:**

- `steamIDUser` (`CSteamID`)
- `pchName` (`string`)
- `pData` (`out float`)

**返回值:** `bool`

**用法示例:**
```csharp
float userStat;
bool result = SteamGameServerStats.GetUserStat(new CSteamID(12345), "Kills", out userStat);
Console.WriteLine($"User stat: {userStat}, Success: {result}");
```

### GetUserAchievement (静态)

```csharp
bool GetUserAchievement(CSteamID steamIDUser, string pchName, out bool pbAchieved)
```

**参数:**

- `steamIDUser` (`CSteamID`)
- `pchName` (`string`)
- `pbAchieved` (`out bool`)

**返回值:** `bool`

**用法示例:**
```csharp
bool achieved;
SteamGameServerStats.GetUserAchievement(new CSteamID(12345), "ACHIEVEMENT_NAME", out achieved);
Console.WriteLine($"Achieved: {achieved}");
```

### SetUserStat (静态)

```csharp
bool SetUserStat(CSteamID steamIDUser, string pchName, int nData)
```

<para>设置/更新统计信息和成就。</para> <para>注意：这些更新仅适用于游戏服务器被允许编辑的统计信息，并且仅适用于</para> <para>已被游戏创作者声明为官方控制的官方游戏服务器。</para> <para>请在Steamworks页面上设置您的官方服务器的IP范围</para>

**参数:**

- `steamIDUser` (`CSteamID`)
- `pchName` (`string`)
- `nData` (`int`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerStats.SetUserStat(new CSteamID(123456789), "Kills", 10);
```

### SetUserStat (静态)

```csharp
bool SetUserStat(CSteamID steamIDUser, string pchName, float fData)
```

**参数:**

- `steamIDUser` (`CSteamID`)
- `pchName` (`string`)
- `fData` (`float`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerStats.SetUserStat(new CSteamID(12345), "Kills", 10.0f);
```

### UpdateUserAvgRateStat (静态)

```csharp
bool UpdateUserAvgRateStat(CSteamID steamIDUser, string pchName, float flCountThisSession, double dSessionLength)
```

**参数:**

- `steamIDUser` (`CSteamID`)
- `pchName` (`string`)
- `flCountThisSession` (`float`)
- `dSessionLength` (`double`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = SteamGameServerStats.UpdateUserAvgRateStat(new CSteamID(12345), "damage_per_minute", 500f, 60.0);
```

### SetUserAchievement (静态)

```csharp
bool SetUserAchievement(CSteamID steamIDUser, string pchName)
```

**参数:**

- `steamIDUser` (`CSteamID`)
- `pchName` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerStats.SetUserAchievement(new CSteamID(123456), "ACHIEVEMENT_NAME");
```

### ClearUserAchievement (静态)

```csharp
bool ClearUserAchievement(CSteamID steamIDUser, string pchName)
```

**参数:**

- `steamIDUser` (`CSteamID`)
- `pchName` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerStats.ClearUserAchievement(new CSteamID(123456789), "ACHIEVEMENT_NAME");
```

### StoreUserStats (静态)

```csharp
SteamAPICall_t StoreUserStats(CSteamID steamIDUser)
```

<para> 将当前数据存储到服务器，设置后将收到 GSStatsStored_t 回调。</para> <para> 如果回调的结果为 k_EResultInvalidParam，则表示一个或多个已上传的统计</para> <para> 被拒绝，原因可能是违反了约束条件</para> <para> 或数据已过时。在这种情况下，服务器会返回更新后的值。</para> <para> 应重新遍历这些统计以保持同步。</para>

**参数:**

- `steamIDUser` (`CSteamID`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamGameServerStats.StoreUserStats(new CSteamID(123456789));
```

