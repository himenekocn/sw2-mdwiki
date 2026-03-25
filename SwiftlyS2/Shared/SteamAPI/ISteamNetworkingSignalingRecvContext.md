<a id="isteamnetworkingsignalingrecvcontext"></a>

# 🏗️ ISteamNetworkingSignalingRecvContext

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

## ⚙️ 方法

### OnConnectRequest

```csharp
IntPtr OnConnectRequest(HSteamNetConnection hConn, ref SteamNetworkingIdentity identityPeer, int nLocalVirtualPort)
```

**参数:**

- `hConn` (`HSteamNetConnection`)
- `identityPeer` (`ref SteamNetworkingIdentity`)
- `nLocalVirtualPort` (`int`)

**返回值:** `IntPtr`

**用法示例:**
```csharp
var result = signalingContext.OnConnectRequest(connection, ref peerIdentity, localPort);
```

### SendRejectionSignal

```csharp
void SendRejectionSignal(ref SteamNetworkingIdentity identityPeer, IntPtr pMsg, int cbMsg)
```

**参数:**

- `identityPeer` (`ref SteamNetworkingIdentity`)
- `pMsg` (`IntPtr`)
- `cbMsg` (`int`)

**用法示例:**
```csharp
signalingContext.SendRejectionSignal(ref peerIdentity, messagePtr, messageSize);
```

