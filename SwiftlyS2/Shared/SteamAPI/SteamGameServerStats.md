# 📦 SteamGameServerStats

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### RequestUserStats (静态)

```csharp
SteamAPICall_t RequestUserStats(CSteamID steamIDUser)
```

<para>下载用户的统计数据</para> <para>完成时返回 GSStatsReceived_t 回调</para> <para>如果用户没有统计数据，GSStatsReceived_t.m_eResult 将设置为 k_EResultFail</para> <para>这些统计数据仅对在服务器上进行游戏的客户端自动更新。对于其他用户，需要再次调用 RequestUserStats() 以刷新数据</para>

**参数:**

- `steamIDUser` (`CSteamID`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServerStats.RequestUserStats(steamIDUser);
```

### GetUserStat (静态)

```csharp
bool GetUserStat(CSteamID steamIDUser, string pchName, out int pData)
```

请求用户的统计数据，该接口在成功调用 RequestUserStats() 之后可用。

**参数:**

- `steamIDUser` (`CSteamID`)
- `pchName` (`string`)
- `pData` (`out int`)

**返回值:** `bool`

**用法示例:**
```csharp
int statValue;
bool ok = SteamGameServerStats.GetUserStat(steamIDUser, "Kills", out statValue);
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
float statValue;
bool ok = SteamGameServerStats.GetUserStat(steamIDUser, "Kills", out statValue);
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
SteamGameServerStats.GetUserAchievement(steamIDUser, "AchievementName", out var achieved);
```

### SetUserStat (静态)

```csharp
bool SetUserStat(CSteamID steamIDUser, string pchName, int nData)
```

<para>设置或更新统计数据与成就。</para><para>注意：这些更新仅适用于游戏服务器被允许编辑的统计数据，且仅适用于已声明由游戏创作者官方控制的游戏服务器。</para><para>请在 Steamworks 页面上配置您官方服务器的 IP 范围。</para>

**参数:**

- `steamIDUser` (`CSteamID`)
- `pchName` (`string`)
- `nData` (`int`)

**返回值:** `bool`

**用法示例:**
```csharp
bool updated = SteamGameServerStats.SetUserStat(steamIDUser, "Kills", 10);
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
bool ok = SteamGameServerStats.SetUserStat(steamIDUser, "Kills", 12.5f);
if (ok) Console.WriteLine("Set user stat success");
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
bool ok = SteamGameServerStats.UpdateUserAvgRateStat(steamIDUser, "Score", 10f, 300.0);
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
bool ok = SteamGameServerStats.SetUserAchievement(steamIDUser, "ACH_WIN_ONE_GAME");
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
bool cleared = SteamGameServerStats.ClearUserAchievement(steamIDUser, "ACH_WIN_ONE_GAME");
```

### StoreUserStats (静态)

```csharp
SteamAPICall_t StoreUserStats(CSteamID steamIDUser)
```

将当前数据存储在服务器上，设置后将会收到 GSStatsStored_t 回调。如果回调中的结果为 k_EResultInvalidParam，则表示已上传的一个或多个统计信息被拒绝，原因可能是其违反了约束条件或已过时。在此情况下，服务器会返回更新后的数值，应重新遍历统计信息以保持同步。

**参数:**

- `steamIDUser` (`CSteamID`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServerStats.StoreUserStats(steamIDUser);
```

