<a id="cserversideclientbase"></a>

# 🏗️ CServerSideClientBase

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `UserIDString` | `CUtlString` | - | - |
| `Name` | `CUtlString` | - | - |
| `PlayerSlot` | `int` | - | - |
| `EntityIndex` | `int` | - | - |
| `Server` | `nint` | - | - |
| `NetworkChannel` | `nint` | - | - |
| `ConnectionTypeFlags` | `ushort` | - | - |
| `MarkedToKick` | `byte` | - | - |
| `SignonState` | `SignonState_t` | - | - |
| `SplitScreenUser` | `byte` | - | - |
| `SplitAllowFastDisconnect` | `byte` | - | - |
| `SplitScreenPlayerSlot` | `int` | - | - |
| `FirstSplitScreenUser` | `CServerSideClientBase*` | - | - |
| `SecondSplitScreenUser` | `CServerSideClientBase*` | - | - |
| `ThirdSplitScreenUser` | `CServerSideClientBase*` | - | - |
| `FourthSplitScreenUser` | `CServerSideClientBase*` | - | - |
| `AttachedTo` | `CServerSideClientBase*` | - | - |
| `SplitPlayerDisconnecting` | `byte` | - | - |
| `UnkVar` | `int` | - | - |
| `FakeClient` | `byte` | - | - |
| `SendingSnapshot` | `byte` | - | - |
| `UserID` | `ushort` | - | - |
| `ReceivedPacket` | `byte` | - | - |
| `SteamID` | `CSteamID` | - | - |
| `DisconnectedSteamID` | `CSteamID` | - | - |
| `AuthTicketSteamID` | `CSteamID` | - | - |
| `FriendsID` | `CSteamID` | - | - |
| `Address` | `NSAddress` | - | - |
| `Address2` | `NSAddress` | - | - |
| `ConVars` | `KeyValues*` | - | - |
| `Unk0` | `byte` | - | - |
| `ConVarsChanged` | `byte` | - | - |
| `IsHLTV` | `byte` | - | - |
| `SendtableCRC` | `uint` | - | - |
| `ChallengeNumber` | `uint` | - | - |
| `SignonTick` | `int` | - | - |
| `DeltaTick` | `int` | - | - |
| `UnkVariable3` | `int` | - | - |
| `StringTableAckTick` | `int` | - | - |
| `UnkVar4` | `int` | - | - |
| `LastSnapshot` | `nint` | - | - |
| `LoadedSpawnGroups` | `CUtlVector\<nint\>` | - | - |
| `BaselineSnapshot` | `nint` | - | - |
| `BaselineUpdateTick` | `int` | - | - |
| `BaselinesSent` | `CBitVec16384` | - | - |
| `BaselineUsed` | `int` | - | - |
| `LoadingProgress` | `int` | - | - |
| `ForceWaitForTick` | `int` | - | - |
| `UnkBuffer` | `CCircularBuffer` | - | - |
| `LowViolence` | `byte` | - | - |
| `SomethingWithAddressType` | `byte` | - | - |
| `FullyAuthenticated` | `byte` | - | - |
| `Unk1` | `byte` | - | - |
| `Unk` | `int` | - | - |
| `NextMessageTime` | `float` | - | - |
| `AuthenticatedTime` | `float` | - | - |
| `SnapshotInterval` | `float` | - | - |
| `Trace` | `CNetworkStatTrace` | - | - |
| `SpamCommandsCount` | `int` | - | - |
| `Unknown` | `int` | - | - |
| `LastExecutedCommand` | `double` | - | - |

