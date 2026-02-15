# 📦 ISteamMatchmakingPingResponse

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_VTServerResponded` | `InternalServerResponded` | - | - |
| `m_VTServerFailedToRespond` | `InternalServerFailedToRespond` | - | - |

## ⚙️ 方法

### ServerResponded

```csharp
void ServerResponded(gameserveritem_t server)
```

**参数:**

- `server` (`gameserveritem_t`)

**用法示例:**
```csharp
ISteamMatchmakingPingResponse.ServerResponded(server);
```

### ServerFailedToRespond

```csharp
void ServerFailedToRespond()
```

**用法示例:**
```csharp
ISteamMatchmakingPingResponse.ServerFailedToRespond();
```

