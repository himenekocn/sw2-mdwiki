# 🏗️ LobbyChatUpdate_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `k_iCallback` | `int` | const | - |
| `m_ulSteamIDLobby` | `ulong` | - | - |
| `m_ulSteamIDUserChanged` | `ulong` | - | - |
| `m_rgfChatMemberStateChange` | `uint` | - | - |

## ⚙️ 方法

### change

```csharp
the change(different from SteamIDUserChange if kicking,  muting, etc. )
```

**参数:**

- `kicking` (`different from SteamIDUserChange if`)
- `muting` (``)
- `` (`etc.`)

**返回值:** `the`

**用法示例:**
```csharp
LobbyChatUpdate_t.change(SteamIDUserChange);
```

