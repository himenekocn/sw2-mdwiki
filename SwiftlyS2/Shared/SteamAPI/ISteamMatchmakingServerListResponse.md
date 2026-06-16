<a id="isteammatchmakingserverlistresponse"></a>

# 📦 ISteamMatchmakingServerListResponse

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_VTServerResponded` | `InternalServerResponded` | - | - |
| `m_VTServerFailedToRespond` | `InternalServerFailedToRespond` | - | - |
| `m_VTRefreshComplete` | `InternalRefreshComplete` | - | - |

## ⚙️ 方法

### ServerResponded

```csharp
void ServerResponded(HServerListRequest hRequest, int iServer)
```

**参数:**

- `hRequest` (`HServerListRequest`)
- `iServer` (`int`)

**用法示例:**
```csharp
matchmakingResponse.ServerResponded(hRequest, 0);
```

### ServerFailedToRespond

```csharp
void ServerFailedToRespond(HServerListRequest hRequest, int iServer)
```

**参数:**

- `hRequest` (`HServerListRequest`)
- `iServer` (`int`)

**用法示例:**
```csharp
matchmakingResponse.ServerFailedToRespond(hRequest, iServer);
```

### RefreshComplete

```csharp
void RefreshComplete(HServerListRequest hRequest, EMatchMakingServerResponse response)
```

**参数:**

- `hRequest` (`HServerListRequest`)
- `response` (`EMatchMakingServerResponse`)

**用法示例:**
```csharp
matchmakingResponse.RefreshComplete(hRequest, EMatchMakingServerResponse.eMSRSucceeded);
```

