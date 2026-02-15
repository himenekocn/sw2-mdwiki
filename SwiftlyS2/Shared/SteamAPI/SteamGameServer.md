# 📦 SteamGameServer

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### SetProduct (静态)

```csharp
void SetProduct(string pszProduct)
```

<para>/ Game product identifier. This is currently used by the master server for version checking purposes.</para> <para>/ It's a required field, but will eventually will go away, and the AppID will be used for this purpose.</para>

**参数:**

- `pszProduct` (`string`)

### SetGameDescription (静态)

```csharp
void SetGameDescription(string pszGameDescription)
```

<para>/ Description of the game. This is a required field and is displayed in the steam server browser....for now.</para> <para>/ This is a required field, but it will go away eventually, as the data should be determined from the AppID.</para>

**参数:**

- `pszGameDescription` (`string`)

### SetModDir (静态)

```csharp
void SetModDir(string pszModDir)
```

<para>/ If your game is a "mod," pass the string that identifies it. The default is an empty string, meaning</para> <para>/ this application is the original game, not a mod.</para> <para>/</para> <para>/ @see k_cbMaxGameServerGameDir</para>

**参数:**

- `pszModDir` (`string`)

### SetDedicatedServer (静态)

```csharp
void SetDedicatedServer(bool bDedicated)
```

<para>/ Is this is a dedicated server? The default value is false.</para>

**参数:**

- `bDedicated` (`bool`)

### LogOn (静态)

```csharp
void LogOn(string pszToken)
```

<para> Login</para> <para>/ Begin process to login to a persistent game server account</para> <para>/</para> <para>/ You need to register for callbacks to determine the result of this operation.</para> <para>/ @see SteamServersConnected_t</para> <para>/ @see SteamServerConnectFailure_t</para> <para>/ @see SteamServersDisconnected_t</para>

**参数:**

- `pszToken` (`string`)

### LogOnAnonymous (静态)

```csharp
void LogOnAnonymous()
```

<para>/ Login to a generic, anonymous account.</para> <para>/</para> <para>/ Note: in previous versions of the SDK, this was automatically called within SteamGameServer_Init,</para> <para>/ but this is no longer the case.</para>

### LogOff (静态)

```csharp
void LogOff()
```

<para>/ Begin process of logging game server out of steam</para>

### BLoggedOn (静态)

```csharp
bool BLoggedOn()
```

<para> status functions</para>

**返回值:** `bool`

### BSecure (静态)

```csharp
bool BSecure()
```

**返回值:** `bool`

### GetSteamID (静态)

```csharp
CSteamID GetSteamID()
```

**返回值:** `CSteamID`

### WasRestartRequested (静态)

```csharp
bool WasRestartRequested()
```

<para>/ Returns true if the master server has requested a restart.</para> <para>/ Only returns true once per request.</para>

**返回值:** `bool`

### SetMaxPlayerCount (静态)

```csharp
void SetMaxPlayerCount(int cPlayersMax)
```

<para> Server state. These properties may be changed at any time.</para> <para>/ Max player count that will be reported to server browser and client queries</para>

**参数:**

- `cPlayersMax` (`int`)

### SetBotPlayerCount (静态)

```csharp
void SetBotPlayerCount(int cBotplayers)
```

<para>/ Number of bots. Default value is zero</para>

**参数:**

- `cBotplayers` (`int`)

### SetServerName (静态)

```csharp
void SetServerName(string pszServerName)
```

<para>/ Set the name of server as it will appear in the server browser</para> <para>/</para> <para>/ @see k_cbMaxGameServerName</para>

**参数:**

- `pszServerName` (`string`)

### SetMapName (静态)

```csharp
void SetMapName(string pszMapName)
```

<para>/ Set name of map to report in the server browser</para> <para>/</para> <para>/ @see k_cbMaxGameServerMapName</para>

**参数:**

- `pszMapName` (`string`)

### SetPasswordProtected (静态)

```csharp
void SetPasswordProtected(bool bPasswordProtected)
```

<para>/ Let people know if your server will require a password</para>

**参数:**

- `bPasswordProtected` (`bool`)

### SetSpectatorPort (静态)

```csharp
void SetSpectatorPort(ushort unSpectatorPort)
```

<para>/ Spectator server port to advertise. The default value is zero, meaning the</para> <para>/ service is not used. If your server receives any info requests on the LAN,</para> <para>/ this is the value that will be placed into the reply for such local queries.</para> <para>/</para> <para>/ This is also the value that will be advertised by the master server.</para> <para>/ The only exception is if your server is using a FakeIP. Then then the second</para> <para>/ fake port number (index 1) assigned to your server will be listed on the master</para> <para>/ server as the spectator port, if you set this value to any nonzero value.</para> <para>/</para> <para>/ This function merely controls the values that are advertised -- it's up to you to</para> <para>/ configure the server to actually listen on this port and handle any spectator traffic</para>

**参数:**

- `unSpectatorPort` (`ushort`)

### SetSpectatorServerName (静态)

```csharp
void SetSpectatorServerName(string pszSpectatorServerName)
```

<para>/ Name of the spectator server. (Only used if spectator port is nonzero.)</para> <para>/</para> <para>/ @see k_cbMaxGameServerMapName</para>

**参数:**

- `pszSpectatorServerName` (`string`)

### ClearAllKeyValues (静态)

```csharp
void ClearAllKeyValues()
```

<para>/ Call this to clear the whole list of key/values that are sent in rules queries.</para>

### SetKeyValue (静态)

```csharp
void SetKeyValue(string pKey, string pValue)
```

<para>/ Call this to add/update a key/value pair.</para>

**参数:**

- `pKey` (`string`)
- `pValue` (`string`)

### SetGameTags (静态)

```csharp
void SetGameTags(string pchGameTags)
```

<para>/ Sets a string defining the "gametags" for this server, this is optional, but if it is set</para> <para>/ it allows users to filter in the matchmaking/server-browser interfaces based on the value</para> <para>/</para> <para>/ @see k_cbMaxGameServerTags</para>

**参数:**

- `pchGameTags` (`string`)

### SetGameData (静态)

```csharp
void SetGameData(string pchGameData)
```

<para>/ Sets a string defining the "gamedata" for this server, this is optional, but if it is set</para> <para>/ it allows users to filter in the matchmaking/server-browser interfaces based on the value</para> <para>/</para> <para>/ @see k_cbMaxGameServerGameData</para>

**参数:**

- `pchGameData` (`string`)

### SetRegion (静态)

```csharp
void SetRegion(string pszRegion)
```

<para>/ Region identifier. This is an optional field, the default value is empty, meaning the "world" region</para>

**参数:**

- `pszRegion` (`string`)

### SetAdvertiseServerActive (静态)

```csharp
void SetAdvertiseServerActive(bool bActive)
```

<para>/ Indicate whether you wish to be listed on the master server list</para> <para>/ and/or respond to server browser / LAN discovery packets.</para> <para>/ The server starts with this value set to false. You should set all</para> <para>/ relevant server parameters before enabling advertisement on the server.</para> <para>/</para> <para>/ (This function used to be named EnableHeartbeats, so if you are wondering</para> <para>/ where that function went, it's right here. It does the same thing as before,</para> <para>/ the old name was just confusing.)</para>

**参数:**

- `bActive` (`bool`)

### GetAuthSessionTicket (静态)

```csharp
HAuthTicket GetAuthSessionTicket(byte[] pTicket, int cbMaxTicket, out uint pcbTicket, ref SteamNetworkingIdentity pSnid)
```

<para> Player list management / authentication.</para> <para> Retrieve ticket to be sent to the entity who wishes to authenticate you ( using BeginAuthSession API ).</para> <para> pcbTicket retrieves the length of the actual ticket.</para> <para> SteamNetworkingIdentity is an optional parameter to hold the public IP address of the entity you are connecting to</para> <para> if an IP address is passed Steam will only allow the ticket to be used by an entity with that IP address</para>

**参数:**

- `pTicket` (`byte[]`)
- `cbMaxTicket` (`int`)
- `pcbTicket` (`out uint`)
- `pSnid` (`ref SteamNetworkingIdentity`)

**返回值:** `HAuthTicket`

### BeginAuthSession (静态)

```csharp
EBeginAuthSessionResult BeginAuthSession(byte[] pAuthTicket, int cbAuthTicket, CSteamID steamID)
```

<para> Authenticate ticket ( from GetAuthSessionTicket ) from entity steamID to be sure it is valid and isnt reused</para> <para> Registers for callbacks if the entity goes offline or cancels the ticket ( see ValidateAuthTicketResponse_t callback and EAuthSessionResponse )</para>

**参数:**

- `pAuthTicket` (`byte[]`)
- `cbAuthTicket` (`int`)
- `steamID` (`CSteamID`)

**返回值:** `EBeginAuthSessionResult`

### EndAuthSession (静态)

```csharp
void EndAuthSession(CSteamID steamID)
```

<para> Stop tracking started by BeginAuthSession - called when no longer playing game with this entity</para>

**参数:**

- `steamID` (`CSteamID`)

### CancelAuthTicket (静态)

```csharp
void CancelAuthTicket(HAuthTicket hAuthTicket)
```

<para> Cancel auth ticket from GetAuthSessionTicket, called when no longer playing game with the entity you gave the ticket to</para>

**参数:**

- `hAuthTicket` (`HAuthTicket`)

### UserHasLicenseForApp (静态)

```csharp
EUserHasLicenseForAppResult UserHasLicenseForApp(CSteamID steamID, AppId_t appID)
```

<para> After receiving a user's authentication data, and passing it to SendUserConnectAndAuthenticate, use this function</para> <para> to determine if the user owns downloadable content specified by the provided AppID.</para>

**参数:**

- `steamID` (`CSteamID`)
- `appID` (`AppId_t`)

**返回值:** `EUserHasLicenseForAppResult`

### RequestUserGroupStatus (静态)

```csharp
bool RequestUserGroupStatus(CSteamID steamIDUser, CSteamID steamIDGroup)
```

<para> Ask if a user in in the specified group, results returns async by GSUserGroupStatus_t</para> <para> returns false if we're not connected to the steam servers and thus cannot ask</para>

**参数:**

- `steamIDUser` (`CSteamID`)
- `steamIDGroup` (`CSteamID`)

**返回值:** `bool`

### GetGameplayStats (静态)

```csharp
void GetGameplayStats()
```

<para> these two functions s are deprecated, and will not return results</para> <para> they will be removed in a future version of the SDK</para>

### GetServerReputation (静态)

```csharp
SteamAPICall_t GetServerReputation()
```

**返回值:** `SteamAPICall_t`

### GetPublicIP (静态)

```csharp
SteamIPAddress_t GetPublicIP()
```

<para> Returns the public IP of the server according to Steam, useful when the server is</para> <para> behind NAT and you want to advertise its IP in a lobby for other clients to directly</para> <para> connect to</para>

**返回值:** `SteamIPAddress_t`

### HandleIncomingPacket (静态)

```csharp
bool HandleIncomingPacket(byte[] pData, int cbData, uint srcIP, ushort srcPort)
```

<para> Server browser related query packet processing for shared socket mode. These are used</para> <para> when you pass STEAMGAMESERVER_QUERY_PORT_SHARED as the query port to SteamGameServer_Init.</para> <para> IP address and port are in host order, i.e 127.0.0.1 == 0x7f000001</para> <para> These are used when you've elected to multiplex the game server's UDP socket</para> <para> rather than having the master server updater use its own sockets.</para> <para> Source games use this to simplify the job of the server admins, so they</para> <para> don't have to open up more ports on their firewalls.</para> <para> Call this when a packet that starts with 0xFFFFFFFF comes in. That means</para> <para> it's for us.</para>

**参数:**

- `pData` (`byte[]`)
- `cbData` (`int`)
- `srcIP` (`uint`)
- `srcPort` (`ushort`)

**返回值:** `bool`

### GetNextOutgoingPacket (静态)

```csharp
int GetNextOutgoingPacket(byte[] pOut, int cbMaxOut, out uint pNetAdr, out ushort pPort)
```

<para> AFTER calling HandleIncomingPacket for any packets that came in that frame, call this.</para> <para> This gets a packet that the master server updater needs to send out on UDP.</para> <para> It returns the length of the packet it wants to send, or 0 if there are no more packets to send.</para> <para> Call this each frame until it returns 0.</para>

**参数:**

- `pOut` (`byte[]`)
- `cbMaxOut` (`int`)
- `pNetAdr` (`out uint`)
- `pPort` (`out ushort`)

**返回值:** `int`

### AssociateWithClan (静态)

```csharp
SteamAPICall_t AssociateWithClan(CSteamID steamIDClan)
```

<para> Server clan association</para> <para> associate this game server with this clan for the purposes of computing player compat</para>

**参数:**

- `steamIDClan` (`CSteamID`)

**返回值:** `SteamAPICall_t`

### ComputeNewPlayerCompatibility (静态)

```csharp
SteamAPICall_t ComputeNewPlayerCompatibility(CSteamID steamIDNewPlayer)
```

<para> ask if any of the current players dont want to play with this new player - or vice versa</para>

**参数:**

- `steamIDNewPlayer` (`CSteamID`)

**返回值:** `SteamAPICall_t`

### SendUserConnectAndAuthenticate_DEPRECATED (静态)

```csharp
bool SendUserConnectAndAuthenticate_DEPRECATED(uint unIPClient, byte[] pvAuthBlob, uint cubAuthBlobSize, out CSteamID pSteamIDUser)
```

<para> Handles receiving a new connection from a Steam user. This call will ask the Steam</para> <para> servers to validate the users identity, app ownership, and VAC status. If the Steam servers</para> <para> are off-line, then it will validate the cached ticket itself which will validate app ownership</para> <para> and identity. The AuthBlob here should be acquired on the game client using SteamUser()-&gt;InitiateGameConnection()</para> <para> and must then be sent up to the game server for authentication.</para> <para> Return Value: returns true if the users ticket passes basic checks. pSteamIDUser will contain the Steam ID of this user. pSteamIDUser must NOT be NULL</para> <para> If the call succeeds then you should expect a GSClientApprove_t or GSClientDeny_t callback which will tell you whether authentication</para> <para> for the user has succeeded or failed (the steamid in the callback will match the one returned by this call)</para> <para> DEPRECATED! This function will be removed from the SDK in an upcoming version.</para> <para> Please migrate to BeginAuthSession and related functions.</para>

**参数:**

- `unIPClient` (`uint`)
- `pvAuthBlob` (`byte[]`)
- `cubAuthBlobSize` (`uint`)
- `pSteamIDUser` (`out CSteamID`)

**返回值:** `bool`

### CreateUnauthenticatedUserConnection (静态)

```csharp
CSteamID CreateUnauthenticatedUserConnection()
```

<para> Creates a fake user (ie, a bot) which will be listed as playing on the server, but skips validation.</para> <para> Return Value: Returns a SteamID for the user to be tracked with, you should call EndAuthSession()</para> <para> when this user leaves the server just like you would for a real user.</para>

**返回值:** `CSteamID`

### SendUserDisconnect_DEPRECATED (静态)

```csharp
void SendUserDisconnect_DEPRECATED(CSteamID steamIDUser)
```

<para> Should be called whenever a user leaves our game server, this lets Steam internally</para> <para> track which users are currently on which servers for the purposes of preventing a single</para> <para> account being logged into multiple servers, showing who is currently on a server, etc.</para> <para> DEPRECATED! This function will be removed from the SDK in an upcoming version.</para> <para> Please migrate to BeginAuthSession and related functions.</para>

**参数:**

- `steamIDUser` (`CSteamID`)

### BUpdateUserData (静态)

```csharp
bool BUpdateUserData(CSteamID steamIDUser, string pchPlayerName, uint uScore)
```

<para> Update the data to be displayed in the server browser and matchmaking interfaces for a user</para> <para> currently connected to the server. For regular users you must call this after you receive a</para> <para> GSUserValidationSuccess callback.</para> <para> Return Value: true if successful, false if failure (ie, steamIDUser wasn't for an active player)</para>

**参数:**

- `steamIDUser` (`CSteamID`)
- `pchPlayerName` (`string`)
- `uScore` (`uint`)

**返回值:** `bool`

