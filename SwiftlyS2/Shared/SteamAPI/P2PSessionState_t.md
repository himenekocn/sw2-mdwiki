<a id="p2psessionstate_t"></a>

# 🏗️ P2PSessionState_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_bConnectionActive` | `byte` | - | - |
| `m_bConnecting` | `byte` | - | - |
| `m_nBytesQueuedForSend` | `int` | - | - |
| `m_nPacketsQueuedForSend` | `int` | - | - |
| `m_nRemoteIP` | `uint` | - | - |
| `m_nRemotePort` | `ushort` | - | - |

## ⚙️ 方法

### server

```csharp
relay server( TURN)
```

**参数:**

- `TURN` (``)

**返回值:** `relay`

**用法示例:**
```csharp
if (state.RelayServer()) Console.WriteLine("TURN");
```

