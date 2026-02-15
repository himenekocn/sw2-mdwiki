# 🏗️ GSReputation_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `k_iCallback` | `int` | const | - |
| `m_eResult` | `EResult` | - | - |
| `m_unReputationScore` | `uint` | - | - |
| `m_bBanned` | `bool` | - | - |
| `m_unBannedIP` | `uint` | - | - |
| `m_usBannedPort` | `ushort` | - | - |
| `m_ulBannedGameID` | `ulong` | - | - |

## ⚙️ 方法

### epoch

```csharp
Unix epoch(seconds since 1/1/1970)
```

**参数:**

- `1/1/1970` (`seconds since`)

**返回值:** `Unix`

**用法示例:**
```csharp
long timestamp = GSReputation_t.UnixEpoch();
```

