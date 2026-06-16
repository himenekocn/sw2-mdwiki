<a id="steamgameserverstats"></a>

# 📦 SteamGameServerStats

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### RequestUserStats (静态)

```csharp
SteamAPICall_t RequestUserStats(CSteamID steamIDUser)
```

<para> 下载该用户的统计数据</para>
<para> 完成时返回 GSStatsReceived_t 回调</para>
<para> 如果该用户没有统计数据，GSStatsReceived_t.m_eResult 将被设置为 k_EResultFail</para>
<para> 这些统计数据仅会自动更新给在服务器上游戏的客户端。对于其他</para>
<para> 用户，您需要再次调用 RequestUserStats() 以刷新任何数据</para>

**参数:**

- `steamIDUser` (`CSteamID`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t callHandle = SteamGameServerStats.RequestUserStats(steamIDUser);
```

### GetUserStat (静态)

```csharp
bool GetUserStat(CSteamID steamIDUser, string pchName, out int pData)
```

<para> 请求获取某用户的统计信息，应在成功调用 RequestUserStats() 后使用</para>

**参数:**

- `steamIDUser` (`CSteamID`)
- `pchName` (`string`)
- `pData` (`out int`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerStats.RequestUserStats(steamIDUser);
bool success = SteamGameServerStats.GetUserStat(steamIDUser, "kills", out int kills);
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
CSteamID userId = new CSteamID(76561197960287930);
bool success = SteamGameServerStats.GetUserStat(userId, "kills", out float kills);
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
SteamGameServerStats.GetUserAchievement(steamIDUser, "ACH_WIN_FIRST_GAME", out achieved);
```

### SetUserStat (静态)

```csharp
bool SetUserStat(CSteamID steamIDUser, string pchName, int nData)
```

<para> 设置/更新统计数据与成就。</para>
<para> 注意：这些更新仅对允许编辑统计数据的游戏服务器生效，且仅适用于</para>
<para> 已被声明为游戏创建者官方控制的游戏服务器。</para>
<para> 请在Steamworks页面设置您的官方服务器IP范围。</para>

**参数:**

- `steamIDUser` (`CSteamID`)
- `pchName` (`string`)
- `nData` (`int`)

**返回值:** `bool`

**用法示例:**
```csharp
CSteamID userId = new CSteamID(76561198000000000);
SteamGameServerStats.SetUserStat(userId, "kills", 100);
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
CSteamID userId = new CSteamID(76561198000000000);
SteamGameServerStats.SetUserStat(userId, "Speed", 12.5f);
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
SteamGameServerStats.UpdateUserAvgRateStat(steamIDUser, "kills_per_minute", 5.0f, 120.0);
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
SteamGameServerStats.SetUserAchievement(steamIDUser, "ACH_WIN_FIRST_GAME");
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
CSteamID userId = new CSteamID(76561198000000000);
SteamGameServerStats.ClearUserAchievement(userId, "ACHIEVEMENT_NAME");
```

### StoreUserStats (静态)

```csharp
SteamAPICall_t StoreUserStats(CSteamID steamIDUser)
```

<para> 将当前数据存储到服务器，设置完成后将收到 GSStatsStored_t 回调。</para> <para> 如果回调返回 k_EResultInvalidParam 结果，则表明上传的一个或多个统计数据</para> <para> 已被拒绝，原因可能是违反了约束条件</para> <para> 或数据已过时。此时服务器会返回更新后的数值。</para> <para> 应重新遍历统计数据以保持同步。</para>

**参数:**

- `steamIDUser` (`CSteamID`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t callHandle = SteamGameServerStats.StoreUserStats(steamIDUser);
```

