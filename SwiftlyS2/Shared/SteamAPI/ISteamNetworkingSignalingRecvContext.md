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
context.OnConnectRequest(hConn, ref identityPeer, nLocalVirtualPort);
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
// 假设已存在 ISteamNetworkingSignalingRecvContext 实例 context 和 SteamNetworkingIdentity identityPeer
byte[] msgBytes = Encoding.UTF8.GetBytes("reject");
IntPtr pMsg = Marshal.AllocHGlobal(msgBytes.Length);
Marshal.Copy(msgBytes, 0, pMsg, msgBytes.Length);
context.SendRejectionSignal(ref identityPeer, pMsg, msgBytes.Length);
Marshal.FreeHGlobal(pMsg);
```

