# 🏗️ ISteamNetworkingConnectionSignaling

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

## ⚙️ 方法

### SendSignal

```csharp
bool SendSignal(HSteamNetConnection hConn, ref SteamNetConnectionInfo_t info, IntPtr pMsg, int cbMsg)
```

**参数:**

- `hConn` (`HSteamNetConnection`)
- `info` (`ref SteamNetConnectionInfo_t`)
- `pMsg` (`IntPtr`)
- `cbMsg` (`int`)

**返回值:** `bool`

**用法示例:**
```csharp
var result = signaling.SendSignal(hConn, ref info, pMsg, cbMsg);
```

### Release

```csharp
void Release()
```

**用法示例:**
```csharp
signaling.Release();
```

