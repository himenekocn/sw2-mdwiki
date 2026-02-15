# 📦 SteamGameServer

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### SetProduct (静态)

```csharp
void SetProduct(string pszProduct)
```

<para>/ 游戏产品标识符。目前主服务器用于版本检查。</para> <para>/ 这是一个必填字段，但最终将被移除，届时将使用 AppID 来实现此目的。</para>

**参数:**

- `pszProduct` (`string`)

**用法示例:**
```csharp
SteamGameServer.SetProduct("MyGame");
```

### SetGameDescription (静态)

```csharp
void SetGameDescription(string pszGameDescription)
```

<para>/ 游戏的描述。这是一个必填字段，目前会显示在 Steam 服务器浏览器中。</para> <para>/ 这是一个必填字段，但最终会被移除，因为数据应通过 AppID 确定。</para>

**参数:**

- `pszGameDescription` (`string`)

**用法示例:**
```csharp
SteamGameServer.SetGameDescription("My Awesome Game");
```

### SetModDir (静态)

```csharp
void SetModDir(string pszModDir)
```

<para>/ 如果您的游戏是“模组”，请传入标识它的字符串。默认值为空字符串，表示</para> <para>/ 此应用程序是原始游戏，而非模组。</para> <para>/</para> <para>/ @see k_cbMaxGameServerGameDir</para>

**参数:**

- `pszModDir` (`string`)

**用法示例:**
```csharp
SteamGameServer.SetModDir("csgo");
```

### SetDedicatedServer (静态)

```csharp
void SetDedicatedServer(bool bDedicated)
```

<para>/ 这是专用服务器吗？默认值为 false。</para>

**参数:**

- `bDedicated` (`bool`)

**用法示例:**
```csharp
SteamGameServer.SetDedicatedServer(true);
```

### LogOn (静态)

```csharp
void LogOn(string pszToken)
```

<para> 登录</para> <para>/ 开始登录到持久游戏服务器账户的流程</para> <para>/</para> <para>/ 您需要注册回调以确定此操作的结果。</para> <para>/ @see SteamServersConnected_t</para> <para>/ @see SteamServerConnectFailure_t</para> <para>/ @see SteamServersDisconnected_t</para>

**参数:**

- `pszToken` (`string`)

**用法示例:**
```csharp
SteamGameServer.LogOn("your_auth_token");
```

### LogOnAnonymous (静态)

```csharp
void LogOnAnonymous()
```

<para>/ 登录到一个通用的、匿名的账户。</para> <para>/</para> <para>/ 注意：在 SDK 的早期版本中，此方法会在 SteamGameServer_Init 内被自动调用，</para> <para>/ 但现在情况已不再如此。</para>

**用法示例:**
```csharp
SteamGameServer.LogOnAnonymous();
```

### LogOff (静态)

```csharp
void LogOff()
```

<para>开始将游戏服务器从 Steam 注销的流程</para>

**用法示例:**
```csharp
SteamGameServer.LogOff();
```

### BLoggedOn (静态)

```csharp
bool BLoggedOn()
```

状态函数

**返回值:** `bool`

**用法示例:**
```csharp
bool isLoggedOn = SteamGameServer.BLoggedOn();
```

### BSecure (静态)

```csharp
bool BSecure()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isSecure = SteamGameServer.BSecure();
Console.WriteLine($"Is secure: {isSecure}");
```

### GetSteamID (静态)

```csharp
CSteamID GetSteamID()
```

**返回值:** `CSteamID`

**用法示例:**
```csharp
CSteamID mySteamID = SteamGameServer.GetSteamID();
Console.WriteLine($"Current server SteamID: {mySteamID}");
```

### WasRestartRequested (静态)

```csharp
bool WasRestartRequested()
```

<para>/ 如果主服务器已请求重启，则返回 true。</para> <para>/ 每个请求仅返回 true 一次。</para>

**返回值:** `bool`

**用法示例:**
```csharp
if (SteamGameServer.WasRestartRequested())
{
    Console.WriteLine("服务器即将重启...");
}
```

### SetMaxPlayerCount (静态)

```csharp
void SetMaxPlayerCount(int cPlayersMax)
```

<para>服务器状态。这些属性可以随时更改。</para> <para>/ 将报告给服务器浏览器和客户端查询的最大玩家数量</para>

**参数:**

- `cPlayersMax` (`int`)

**用法示例:**
```csharp
SteamGameServer.SetMaxPlayerCount(10);
```

### SetBotPlayerCount (静态)

```csharp
void SetBotPlayerCount(int cBotplayers)
```

<para>机器人数量。默认值为零</para>

**参数:**

- `cBotplayers` (`int`)

**用法示例:**
```csharp
SteamGameServer.SetBotPlayerCount(2);
```

### SetServerName (静态)

```csharp
void SetServerName(string pszServerName)
```

<para>// 设置服务器在服务器浏览器中显示的名称</para> <para>//</para> <para>// @see k_cbMaxGameServerName</para>

**参数:**

- `pszServerName` (`string`)

**用法示例:**
```csharp
SteamGameServer.SetServerName("My Awesome Server");
```

### SetMapName (静态)

```csharp
void SetMapName(string pszMapName)
```

<para>// 设置在服务器浏览器中报告的地图名称</para> <para>//</para> <para>// @see k_cbMaxGameServerMapName</para>

**参数:**

- `pszMapName` (`string`)

**用法示例:**
```csharp
SteamGameServer.SetMapName("de_dust2");
```

### SetPasswordProtected (静态)

```csharp
void SetPasswordProtected(bool bPasswordProtected)
```

<para>告知用户您的服务器是否需要密码</para>

**参数:**

- `bPasswordProtected` (`bool`)

**用法示例:**
```csharp
SteamGameServer.SetPasswordProtected(true);
```

### SetSpectatorPort (静态)

```csharp
void SetSpectatorPort(ushort unSpectatorPort)
```

<para>/ 要通告的旁观者服务器端口。默认值为零，表示该服务</para> <para>/ 未被使用。如果您的服务器在局域网上收到任何信息请求，</para> <para>/ 此值将被放置在对此类本地查询的回复中。</para> <para>/</para> <para>/ 这也是主服务器将通告的值。</para> <para>/ 唯一例外是，如果您的服务器正在使用伪造IP。那么，如果</para> <para>/ 您将此值设置为任何非零值，分配给您的服务器的第二个</para> <para>/ 伪造端口号（索引1）将被列在主服务器上作为旁观者端口。</para> <para>/</para> <para>/ 此函数仅控制要通告的值 -- 实际上配置服务器以监听此端口</para> <para>/ 并处理任何旁观者流量是您的责任。</para>

**参数:**

- `unSpectatorPort` (`ushort`)

**用法示例:**
```csharp
SteamGameServer.SetSpectatorPort(27015);
```

### SetSpectatorServerName (静态)

```csharp
void SetSpectatorServerName(string pszSpectatorServerName)
```

<para>/ 观战服务器的名称。(仅在观战端口不为零时使用。)</para> <para>/</para> <para>/ @see k_cbMaxGameServerMapName</para>

**参数:**

- `pszSpectatorServerName` (`string`)

**用法示例:**
```csharp
SteamGameServer.SetSpectatorServerName("MySpectatorServer");
```

### ClearAllKeyValues (静态)

```csharp
void ClearAllKeyValues()
```

<para>调用此方法以清除在规则查询中发送的所有键/值列表。</para>

**用法示例:**
```csharp
SteamGameServer.ClearAllKeyValues();
```

### SetKeyValue (静态)

```csharp
void SetKeyValue(string pKey, string pValue)
```

<para>调用此方法以添加/更新键值对。</para>

**参数:**

- `pKey` (`string`)
- `pValue` (`string`)

**用法示例:**
```csharp
SteamGameServer.SetKeyValue("game_type", "csgo");
```

### SetGameTags (静态)

```csharp
void SetGameTags(string pchGameTags)
```

<para>/ 设置一个字符串，用于定义此服务器的“游戏标签”，此参数为可选，但如果设置了</para> <para>/ 则允许用户在匹配/服务器浏览器界面中根据该值进行筛选</para> <para>/</para> <para>/ @see k_cbMaxGameServerTags</para>

**参数:**

- `pchGameTags` (`string`)

**用法示例:**
```csharp
SteamGameServer.SetGameTags("competitive;6v6");
```

### SetGameData (静态)

```csharp
void SetGameData(string pchGameData)
```

<para>/ 设置一个字符串，用于定义此服务器的“游戏数据”，此为可选设置，但如果已设置</para> <para>/ 则允许用户在匹配/服务器浏览器界面中根据该值进行筛选</para> <para>/</para> <para>/ @see k_cbMaxGameServerGameData</para>

**参数:**

- `pchGameData` (`string`)

**用法示例:**
```csharp
SteamGameServer.SetGameData("{\"mode\":\"deathmatch\",\"map\":\"de_dust2\"}");
```

### SetRegion (静态)

```csharp
void SetRegion(string pszRegion)
```

<para>区域标识符。这是一个可选字段，默认值为空，表示“世界”区域。</para>

**参数:**

- `pszRegion` (`string`)

**用法示例:**
```csharp
SteamGameServer.SetRegion("us");
```

### SetAdvertiseServerActive (静态)

```csharp
void SetAdvertiseServerActive(bool bActive)
```

<para>/ 指示您是否希望被列入主服务器列表</para> <para>/ 以及/或响应服务器浏览器 / LAN 发现数据包。</para> <para>/ 服务器启动时此值默认为 false。您应在启用服务器广告之前</para> <para>/ 设置所有相关的服务器参数。</para> <para>/</para> <para>/ (此函数以前名为 EnableHeartbeats，因此如果您想知道</para> <para>/ 该函数去哪了，它就在这里。它和以前的功能一样，</para> <para>/ 只是旧名称容易引起混淆。)</para>

**参数:**

- `bActive` (`bool`)

**用法示例:**
```csharp
SteamGameServer.SetAdvertiseServerActive(true);
```

### GetAuthSessionTicket (静态)

```csharp
HAuthTicket GetAuthSessionTicket(byte[] pTicket, int cbMaxTicket, out uint pcbTicket, ref SteamNetworkingIdentity pSnid)
```

<para> 玩家列表管理 / 身份验证。</para> <para> 获取用于发送给希望对您进行身份验证的实体的票据（使用 BeginAuthSession API）。</para> <para> pcbTicket 用于获取实际票据的长度。</para> <para> SteamNetworkingIdentity 是一个可选参数，用于保存您正在连接的实体的公网 IP 地址</para> <para> 如果传递了 IP 地址，Steam 将只允许具有该 IP 地址的实体使用该票据</para>

**参数:**

- `pTicket` (`byte[]`)
- `cbMaxTicket` (`int`)
- `pcbTicket` (`out uint`)
- `pSnid` (`ref SteamNetworkingIdentity`)

**返回值:** `HAuthTicket`

**用法示例:**
```csharp
uint ticketSize;
byte[] ticket = new byte[1024];
SteamNetworkingIdentity snid = default;
HAuthTicket authTicket = SteamGameServer.GetAuthSessionTicket(ticket, ticket.Length, out ticketSize, ref snid);
```

### BeginAuthSession (静态)

```csharp
EBeginAuthSessionResult BeginAuthSession(byte[] pAuthTicket, int cbAuthTicket, CSteamID steamID)
```

<para> 验证来自实体 steamID 的凭证（来自 GetAuthSessionTicket）以确保其有效且未被重复使用。</para> <para> 如果实体下线或取消凭证，则注册回调（请参阅 ValidateAuthTicketResponse_t 回调和 EAuthSessionResponse）。</para>

**参数:**

- `pAuthTicket` (`byte[]`)
- `cbAuthTicket` (`int`)
- `steamID` (`CSteamID`)

**返回值:** `EBeginAuthSessionResult`

**用法示例:**
```csharp
byte[] ticket = new byte[256]; // 假设已填充有效凭证数据
CSteamID playerID = new CSteamID(123456789);
EBeginAuthSessionResult result = SteamGameServer.BeginAuthSession(ticket, ticket.Length, playerID);
```

### EndAuthSession (静态)

```csharp
void EndAuthSession(CSteamID steamID)
```

<para> 停止由 BeginAuthSession 启动的追踪 - 当不再与该实体进行游戏时调用</para>

**参数:**

- `steamID` (`CSteamID`)

**用法示例:**
```csharp
SteamGameServer.EndAuthSession(player.SteamID);
```

### CancelAuthTicket (静态)

```csharp
void CancelAuthTicket(HAuthTicket hAuthTicket)
```

<para> 取消通过 GetAuthSessionTicket 获取的授权票据，当不再与您提供票据的实体进行游戏时调用此方法</para>

**参数:**

- `hAuthTicket` (`HAuthTicket`)

**用法示例:**
```csharp
HAuthTicket ticket = SteamGameServer.GetAuthSessionTicket();
SteamGameServer.CancelAuthTicket(ticket);
```

### UserHasLicenseForApp (静态)

```csharp
EUserHasLicenseForAppResult UserHasLicenseForApp(CSteamID steamID, AppId_t appID)
```

在接收用户的身份验证数据并将其传递给 SendUserConnectAndAuthenticate 后，使用此函数来确定用户是否拥有由所提供 AppID 指定的可下载内容。

**参数:**

- `steamID` (`CSteamID`)
- `appID` (`AppId_t`)

**返回值:** `EUserHasLicenseForAppResult`

**用法示例:**
```csharp
EUserHasLicenseForAppResult result = SteamGameServer.UserHasLicenseForApp(steamID, appID);
```

### RequestUserGroupStatus (静态)

```csharp
bool RequestUserGroupStatus(CSteamID steamIDUser, CSteamID steamIDGroup)
```

<para> 询问指定用户是否在指定群组中，结果通过 GSUserGroupStatus_t 异步返回。</para> <para> 如果我们未连接到 Steam 服务器，因此无法查询，则返回 false。</para>

**参数:**

- `steamIDUser` (`CSteamID`)
- `steamIDGroup` (`CSteamID`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServer.RequestUserGroupStatus(new CSteamID(123456), new CSteamID(789012));
```

### GetGameplayStats (静态)

```csharp
void GetGameplayStats()
```

<para>这两个函数已弃用，将不会返回结果</para> <para>它们将在 SDK 的未来版本中被移除</para>

**用法示例:**
```csharp
SteamGameServer.GetGameplayStats();
```

### GetServerReputation (静态)

```csharp
SteamAPICall_t GetServerReputation()
```

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t reputationCall = SteamGameServer.GetServerReputation();
Console.WriteLine($"Server reputation call handle: {reputationCall}");
```

### GetPublicIP (静态)

```csharp
SteamIPAddress_t GetPublicIP()
```

<para>根据 Steam 返回服务器的公网 IP，当服务器位于 NAT 后方且您希望向大厅广告其 IP 以供其他客户端直接连接时非常有用。</para> <para></para> <para></para>

**返回值:** `SteamIPAddress_t`

**用法示例:**
```csharp
SteamIPAddress_t publicIP = SteamGameServer.GetPublicIP();
Console.WriteLine($"Public IP: {publicIP}");
```

### HandleIncomingPacket (静态)

```csharp
bool HandleIncomingPacket(byte[] pData, int cbData, uint srcIP, ushort srcPort)
```

<para> 共享套接字模式下与服务器浏览器相关的查询数据包处理。当您将 STEAMGAMESERVER_QUERY_PORT_SHARED 作为查询端口传递给 SteamGameServer_Init 时，将使用这些功能。</para> <para> IP 地址和端口为主机序，即 127.0.0.1 == 0x7f000001</para> <para> 当您选择复用游戏服务器的 UDP 套接字，而不是让主服务器更新器使用其自己的套接字时，将使用这些功能。</para> <para> 源游戏使用此功能来简化服务器管理员的工作，因此他们无需在防火墙上开放更多端口。</para> <para> 当接收到以 0xFFFFFFFF 开头的数据包时，请调用此函数。这意味着该数据包是发给我们的。</para>

**参数:**

- `pData` (`byte[]`)
- `cbData` (`int`)
- `srcIP` (`uint`)
- `srcPort` (`ushort`)

**返回值:** `bool`

**用法示例:**
```csharp
byte[] packetData = new byte[256]; // 示例数据
SteamGameServer.HandleIncomingPacket(packetData, packetData.Length, 0x7f000001, 27015); // 处理来自本地的查询包
```

### GetNextOutgoingPacket (静态)

```csharp
int GetNextOutgoingPacket(byte[] pOut, int cbMaxOut, out uint pNetAdr, out ushort pPort)
```

<para> 在为该帧内收到的任何数据包调用 HandleIncomingPacket 之后，调用此方法。</para> <para> 此方法会获取主服务器更新器需要通过 UDP 发送出去的数据包。</para> <para> 它返回要发送的数据包长度，如果没有更多数据包需要发送，则返回 0。</para> <para> 每帧调用此方法，直到它返回 0 为止。</para>

**参数:**

- `pOut` (`byte[]`)
- `cbMaxOut` (`int`)
- `pNetAdr` (`out uint`)
- `pPort` (`out ushort`)

**返回值:** `int`

**用法示例:**
```csharp
byte[] packetBuffer = new byte[1024];
uint netAddr; ushort port;
int length = SteamGameServer.GetNextOutgoingPacket(packetBuffer, packetBuffer.Length, out netAddr, out port);
```

### AssociateWithClan (静态)

```csharp
SteamAPICall_t AssociateWithClan(CSteamID steamIDClan)
```

<para> 服务器氏族关联</para> <para> 将此游戏服务器与此氏族关联，以便计算玩家兼容性</para>

**参数:**

- `steamIDClan` (`CSteamID`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamGameServer.AssociateWithClan(new CSteamID(123456789));
```

### ComputeNewPlayerCompatibility (静态)

```csharp
SteamAPICall_t ComputeNewPlayerCompatibility(CSteamID steamIDNewPlayer)
```

<para>询问当前玩家中是否有任何人不想与该新玩家一起玩，或者反过来，新玩家不想与当前玩家中的任何人一起玩。</para>

**参数:**

- `steamIDNewPlayer` (`CSteamID`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t result = SteamGameServer.ComputeNewPlayerCompatibility(new CSteamID(123456789));
```

### SendUserConnectAndAuthenticate_DEPRECATED (静态)

```csharp
bool SendUserConnectAndAuthenticate_DEPRECATED(uint unIPClient, byte[] pvAuthBlob, uint cubAuthBlobSize, out CSteamID pSteamIDUser)
```

<para>处理来自Steam用户的新连接请求。此调用将请求Steam服务器验证用户的身份、应用所有权和VAC状态。如果Steam服务器离线，则会自行验证缓存的票据，以验证应用所有权和身份。此处的AuthBlob应在游戏客户端通过SteamUser()->InitiateGameConnection()获取，然后必须发送到游戏服务器进行身份验证。</para>
<para>返回值：如果用户的票据通过基本检查，则返回true。pSteamIDUser将包含该用户的Steam ID。pSteamIDUser不得为NULL。</para>
<para>如果调用成功，则应预期收到GSClientApprove_t或GSClientDeny_t回调，该回调将告知您用户的身份验证是否成功或失败（回调中的steamid将与本调用返回的steamid匹配）。</para>
<para>已弃用！此功能将在即将发布的SDK版本中移除。</para>
<para>请迁移到BeginAuthSession及相关函数。</para>

**参数:**

- `unIPClient` (`uint`)
- `pvAuthBlob` (`byte[]`)
- `cubAuthBlobSize` (`uint`)
- `pSteamIDUser` (`out CSteamID`)

**返回值:** `bool`

**用法示例:**
```csharp
uint clientIP = 0x7F000001; // 127.0.0.1
byte[] authBlob = new byte[256]; // 示例数据
SteamGameServer.SendUserConnectAndAuthenticate_DEPRECATED(clientIP, authBlob, (uint)authBlob.Length, out CSteamID steamID);
```

### CreateUnauthenticatedUserConnection (静态)

```csharp
CSteamID CreateUnauthenticatedUserConnection()
```

<para>创建一个虚假用户（即机器人），该用户将被列为在服务器上游戏，但会跳过验证。</para> <para>返回值：返回一个用于追踪该用户的 SteamID，当此用户离开服务器时，您应像对待真实用户一样调用 EndAuthSession()。</para>

**返回值:** `CSteamID`

**用法示例:**
```csharp
CSteamID botId = SteamGameServer.CreateUnauthenticatedUserConnection();
SteamGameServer.EndAuthSession(botId);
```

### SendUserDisconnect_DEPRECATED (静态)

```csharp
void SendUserDisconnect_DEPRECATED(CSteamID steamIDUser)
```

<para>每当用户离开我们的游戏服务器时都应调用此函数，这能让 Steam 内部</para> <para>追踪哪些用户当前在哪些服务器上，以便防止单个</para> <para>账户登录到多个服务器、显示当前在服务器上的用户等。</para> <para>已弃用！此函数将在 SDK 的未来版本中移除。</para> <para>请迁移到 BeginAuthSession 及相关函数。</para>

**参数:**

- `steamIDUser` (`CSteamID`)

**用法示例:**
```csharp
SteamGameServer.SendUserDisconnect_DEPRECATED(new CSteamID(123456789));
```

### BUpdateUserData (静态)

```csharp
bool BUpdateUserData(CSteamID steamIDUser, string pchPlayerName, uint uScore)
```

<para> 更新服务器浏览器和匹配界面中显示的用户数据，该用户当前已连接到服务器。对于普通用户，您必须在收到 GSUserValidationSuccess 回调后调用此方法。</para> <para> 返回值：如果成功则返回 true，如果失败则返回 false（即，steamIDUser 不是活跃玩家的 steamID）</para>

**参数:**

- `steamIDUser` (`CSteamID`)
- `pchPlayerName` (`string`)
- `uScore` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServer.BUpdateUserData(steamIDUser, "PlayerName", 1000);
```

