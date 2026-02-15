# 📦 ISteamMatchmakingPlayersResponse

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_VTAddPlayerToList` | `InternalAddPlayerToList` | - | - |
| `m_VTPlayersFailedToRespond` | `InternalPlayersFailedToRespond` | - | - |
| `m_VTPlayersRefreshComplete` | `InternalPlayersRefreshComplete` | - | - |

## ⚙️ 方法

### AddPlayerToList

```csharp
void AddPlayerToList(string pchName, int nScore, float flTimePlayed)
```

**参数:**

- `pchName` (`string`)
- `nScore` (`int`)
- `flTimePlayed` (`float`)

**用法示例:**
```csharp
ISteamMatchmakingPlayersResponse.AddPlayerToList("Alice", 100, 3600f);
```

### PlayersFailedToRespond

```csharp
void PlayersFailedToRespond()
```

**用法示例:**
```csharp
ISteamMatchmakingPlayersResponse.PlayersFailedToRespond();
```

### PlayersRefreshComplete

```csharp
void PlayersRefreshComplete()
```

**用法示例:**
```csharp
ISteamMatchmakingPlayersResponse.PlayersRefreshComplete();
```

### InternalAddPlayerToList

```csharp
void InternalAddPlayerToList(IntPtr pchName, int nScore, float flTimePlayed)
```

**参数:**

- `pchName` (`IntPtr`)
- `nScore` (`int`)
- `flTimePlayed` (`float`)

**用法示例:**
```csharp
ISteamMatchmakingPlayersResponse.InternalAddPlayerToList("Alice", 100, 5.2f);
```

### InternalPlayersFailedToRespond

```csharp
void InternalPlayersFailedToRespond()
```

**用法示例:**
```csharp
ISteamMatchmakingPlayersResponse.InternalPlayersFailedToRespond();
```

### InternalPlayersRefreshComplete

```csharp
void InternalPlayersRefreshComplete()
```

**用法示例:**
```csharp
ISteamMatchmakingPlayersResponse.InternalPlayersRefreshComplete();
```

