<a id="steamnetworkingmessage_t"></a>

# 🏗️ SteamNetworkingMessage_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_pData` | `IntPtr` | - | - |
| `m_cbSize` | `int` | - | - |
| `m_conn` | `HSteamNetConnection` | - | - |
| `m_identityPeer` | `SteamNetworkingIdentity` | - | - |
| `m_nConnUserData` | `long` | - | - |
| `m_usecTimeReceived` | `SteamNetworkingMicroseconds` | - | - |
| `m_nMessageNumber` | `long` | - | - |
| `m_pfnFreeData` | `IntPtr` | - | - |
| `m_nChannel` | `int` | - | - |
| `m_nFlags` | `int` | - | - |
| `m_nUserData` | `long` | - | - |
| `m_idxLane` | `ushort` | - | - |

## ⚙️ 方法

### Release

```csharp
void Release()
```

**用法示例:**
```csharp
message.Release();
```

### Release (静态)

```csharp
void Release(IntPtr pointer)
```

**参数:**

- `pointer` (`IntPtr`)

**用法示例:**
```csharp
SteamNetworkingMessage_t.Release(pointer);
```

### FromIntPtr (静态)

```csharp
SteamNetworkingMessage_t FromIntPtr(IntPtr pointer)
```

**参数:**

- `pointer` (`IntPtr`)

**返回值:** `SteamNetworkingMessage_t`

**用法示例:**
```csharp
var message = SteamNetworkingMessage_t.FromIntPtr(pointer);
```

