# 📦 SteamGameServerStats

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### RequestUserStats (静态)

```csharp
SteamAPICall_t RequestUserStats(CSteamID steamIDUser)
```

<para> downloads stats for the user</para> <para> returns a GSStatsReceived_t callback when completed</para> <para> if the user has no stats, GSStatsReceived_t.m_eResult will be set to k_EResultFail</para> <para> these stats will only be auto-updated for clients playing on the server. For other</para> <para> users you'll need to call RequestUserStats() again to refresh any data</para>

**参数:**

- `steamIDUser` (`CSteamID`)

**返回值:** `SteamAPICall_t`

### GetUserStat (静态)

```csharp
bool GetUserStat(CSteamID steamIDUser, string pchName, out int pData)
```

<para> requests stat information for a user, usable after a successful call to RequestUserStats()</para>

**参数:**

- `steamIDUser` (`CSteamID`)
- `pchName` (`string`)
- `pData` (`out int`)

**返回值:** `bool`

### GetUserStat (静态)

```csharp
bool GetUserStat(CSteamID steamIDUser, string pchName, out float pData)
```

**参数:**

- `steamIDUser` (`CSteamID`)
- `pchName` (`string`)
- `pData` (`out float`)

**返回值:** `bool`

### GetUserAchievement (静态)

```csharp
bool GetUserAchievement(CSteamID steamIDUser, string pchName, out bool pbAchieved)
```

**参数:**

- `steamIDUser` (`CSteamID`)
- `pchName` (`string`)
- `pbAchieved` (`out bool`)

**返回值:** `bool`

### SetUserStat (静态)

```csharp
bool SetUserStat(CSteamID steamIDUser, string pchName, int nData)
```

<para> Set / update stats and achievements.</para> <para> Note: These updates will work only on stats game servers are allowed to edit and only for</para> <para> game servers that have been declared as officially controlled by the game creators.</para> <para> Set the IP range of your official servers on the Steamworks page</para>

**参数:**

- `steamIDUser` (`CSteamID`)
- `pchName` (`string`)
- `nData` (`int`)

**返回值:** `bool`

### SetUserStat (静态)

```csharp
bool SetUserStat(CSteamID steamIDUser, string pchName, float fData)
```

**参数:**

- `steamIDUser` (`CSteamID`)
- `pchName` (`string`)
- `fData` (`float`)

**返回值:** `bool`

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

### SetUserAchievement (静态)

```csharp
bool SetUserAchievement(CSteamID steamIDUser, string pchName)
```

**参数:**

- `steamIDUser` (`CSteamID`)
- `pchName` (`string`)

**返回值:** `bool`

### ClearUserAchievement (静态)

```csharp
bool ClearUserAchievement(CSteamID steamIDUser, string pchName)
```

**参数:**

- `steamIDUser` (`CSteamID`)
- `pchName` (`string`)

**返回值:** `bool`

### StoreUserStats (静态)

```csharp
SteamAPICall_t StoreUserStats(CSteamID steamIDUser)
```

<para> Store the current data on the server, will get a GSStatsStored_t callback when set.</para> <para> If the callback has a result of k_EResultInvalidParam, one or more stats</para> <para> uploaded has been rejected, either because they broke constraints</para> <para> or were out of date. In this case the server sends back updated values.</para> <para> The stats should be re-iterated to keep in sync.</para>

**参数:**

- `steamIDUser` (`CSteamID`)

**返回值:** `SteamAPICall_t`

