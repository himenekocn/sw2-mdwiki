<a id="isteammatchmakingplayersresponse"></a>

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
matchmakingPlayersResponse.AddPlayerToList("PlayerOne", 100, 3600.5f);
```

### PlayersFailedToRespond

```csharp
void PlayersFailedToRespond()
```

**用法示例:**
```csharp
matchmakingPlayersResponse.PlayersFailedToRespond();
```

### PlayersRefreshComplete

```csharp
void PlayersRefreshComplete()
```

**用法示例:**
```csharp
matchmakingPlayersResponse.PlayersRefreshComplete();
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
matchmakingPlayersResponse.InternalAddPlayerToList(IntPtr.Zero, 100, 30.5f);
```

### InternalPlayersFailedToRespond

```csharp
void InternalPlayersFailedToRespond()
```

**用法示例:**
```csharp
matchmakingPlayersResponse.InternalPlayersFailedToRespond();
```

### InternalPlayersRefreshComplete

```csharp
void InternalPlayersRefreshComplete()
```

**用法示例:**
```csharp
matchmakingPlayersResponse.InternalPlayersRefreshComplete();
```

