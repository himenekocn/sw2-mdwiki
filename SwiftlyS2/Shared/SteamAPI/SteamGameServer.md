<a id="steamgameserver"></a>

# 📦 SteamGameServer

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### SetProduct (静态)

```csharp
void SetProduct(string pszProduct)
```

<para>/ 游戏产品标识符。目前主服务器用于版本校验。</para> <para>/ 此为必填字段，但最终将被移除，届时将改用AppID实现该功能。</para>

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

<para>/ 游戏描述。这是一个必填字段，目前会显示在Steam服务器浏览器中。</para>
<para>/ 这是一个必填字段，但最终会被移除，因为该数据应由AppID确定。</para>

**参数:**

- `pszGameDescription` (`string`)

**用法示例:**
```csharp
SteamGameServer.SetGameDescription("My Awesome Game Server");
```

### SetModDir (静态)

```csharp
void SetModDir(string pszModDir)
```

<para>/ 如果你的游戏是一个"模组"，请传入标识它的字符串。默认值为空字符串，表示</para> <para>/ 该应用程序是原始游戏，而非模组。</para> <para>/</para> <para>/ @see k_cbMaxGameServerGameDir</para>

**参数:**

- `pszModDir` (`string`)

**用法示例:**
```csharp
SteamGameServer.SetModDir("my_mod_name");
```

### SetDedicatedServer (静态)

```csharp
void SetDedicatedServer(bool bDedicated)
```

<para>/ 这是一个专用服务器吗？默认值为 false。</para>

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

<para> 登录</para>
<para>/ 开始登录持久化游戏服务器账号的流程</para>
<para>/</para>
<para>/ 您需要注册回调以确定此操作的结果。</para>
<para>/ @see SteamServersConnected_t</para>
<para>/ @see SteamServerConnectFailure_t</para>
<para>/ @see SteamServersDisconnected_t</para>

**参数:**

- `pszToken` (`string`)

**用法示例:**
```csharp
SteamGameServer.LogOn("your_auth_token_here");
```

### LogOnAnonymous (静态)

```csharp
void LogOnAnonymous()
```

<para>/ 登录到一个通用的匿名账户。</para>
<para>/</para>
<para>/ 注意：在SDK的早期版本中，该操作会在SteamGameServer_Init内部自动调用，</para>
<para>/ 但当前版本已不再如此。</para>

**用法示例:**
```csharp
SteamGameServer.LogOnAnonymous();
```

### LogOff (静态)

```csharp
void LogOff()
```

<para>/ 开始将游戏服务器从Steam注销的流程</para>

**用法示例:**
```csharp
SteamGameServer.LogOff();
```

### BLoggedOn (静态)

```csharp
bool BLoggedOn()
```

<para>状态函数</para>

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
```

### GetSteamID (静态)

```csharp
CSteamID GetSteamID()
```

**返回值:** `CSteamID`

**用法示例:**
```csharp
CSteamID serverId = SteamGameServer.GetSteamID();
```

### WasRestartRequested (静态)

```csharp
bool WasRestartRequested()
```

<para>如果主服务器请求重启，则返回true。</para> <para>每个请求仅返回一次true。</para>

**返回值:** `bool`

**用法示例:**
```csharp
bool shouldRestart = SteamGameServer.WasRestartRequested();
```

### SetMaxPlayerCount (静态)

```csharp
void SetMaxPlayerCount(int cPlayersMax)
```

<para>服务器状态。这些属性可随时更改。</para>
<para>/ 将向服务器浏览器和客户端查询报告的最大玩家数量</para>

**参数:**

- `cPlayersMax` (`int`)

**用法示例:**
```csharp
SteamGameServer.SetMaxPlayerCount(32);
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
SteamGameServer.SetBotPlayerCount(5);
```

### SetServerName (静态)

```csharp
void SetServerName(string pszServerName)
```

<para>/ 设置服务器浏览器中显示的服务器名称</para>
<para>/</para>
<para>/ @see k_cbMaxGameServerName</para>

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

<para>/ 设置在服务器浏览器中显示的地图名称</para>
<para>/</para>
<para>/ @see k_cbMaxGameServerMapName</para>

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

<para>/ 通知用户您的服务器是否需要密码</para>

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

<para>/ 要广播的观察者服务器端口。默认值为零，表示不启用该服务。若您的服务器在局域网中收到任何信息请求，</para> <para>/ 此值将被填入此类本地查询的回复中。</para> <para>/</para> <para>/ 这也是主服务器将要广播的值。</para> <para>/ 唯一的例外是当您的服务器使用 FakeIP 时。如果将此值设置为任何非零值，</para> <para>/ 分配给服务器的第二个伪端口号（索引1）将在主服务器上列为观察者端口。</para> <para>/</para> <para>/ 此函数仅控制广播的值——您需要自行配置服务器实际监听该端口并处理观察者流量。</para>

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

<para>观察者服务器的名称。（仅当观察者端口非零时使用。）</para>
<para>/</para>
<para>/ @see k_cbMaxGameServerMapName</para>

**参数:**

- `pszSpectatorServerName` (`string`)

**用法示例:**
```csharp
SteamGameServer.SetSpectatorServerName("My Spectator Server");
```

### ClearAllKeyValues (静态)

```csharp
void ClearAllKeyValues()
```

<para>调用此方法清除规则查询中发送的整个键/值列表。</para>

**用法示例:**
```csharp
SteamGameServer.ClearAllKeyValues();
```

### SetKeyValue (静态)

```csharp
void SetKeyValue(string pKey, string pValue)
```

<para>/ 调用此方法以添加/更新键值对。</para>

**参数:**

- `pKey` (`string`)
- `pValue` (`string`)

**用法示例:**
```csharp
SteamGameServer.SetKeyValue("map", "de_dust2");
SteamGameServer.SetKeyValue("maxplayers", "16");
```

### SetGameTags (静态)

```csharp
void SetGameTags(string pchGameTags)
```

<para>/ 设置定义此服务器“游戏标签”的字符串，此为可选设置，但如果设置</para> <para>/ 将允许用户在匹配/服务器浏览器界面中基于该值进行筛选</para> <para>/</para> <para>/ @参考 k_cbMaxGameServerTags</para>

**参数:**

- `pchGameTags` (`string`)

**用法示例:**
```csharp
SteamGameServer.SetGameTags("competitive,ranked");
```

### SetGameData (静态)

```csharp
void SetGameData(string pchGameData)
```

<para>/ 设置一个字符串定义此服务器的“游戏数据”，此为可选操作，但若设置后</para> <para>/ 将允许用户在匹配/服务器浏览器界面中基于该值进行筛选</para> <para>/</para> <para>/ @see k_cbMaxGameServerGameData</para>

**参数:**

- `pchGameData` (`string`)

**用法示例:**
```csharp
SteamGameServer.SetGameData("mode=dm;map=de_dust2");
```

### SetRegion (静态)

```csharp
void SetRegion(string pszRegion)
```

<para>/ 区域标识符。这是一个可选字段，默认值为空，表示“世界”区域</para>

**参数:**

- `pszRegion` (`string`)

**用法示例:**
```csharp
SteamGameServer.SetRegion("Europe");
```

### SetAdvertiseServerActive (静态)

```csharp
void SetAdvertiseServerActive(bool bActive)
```

<para>/ 指示您是否希望被列在主服务器列表上</para>
<para>/ 以及/或响应服务器浏览器/局域网发现数据包。</para>
<para>/ 服务器启动时该值默认设置为false。您应在服务器上启用广播前</para>
<para>/ 设置所有相关的服务器参数。</para>
<para>/</para>
<para>/ （此函数曾名为EnableHeartbeats，若您想知道该函数去了哪里，</para>
<para>/ 它就在此处。其功能与之前相同，旧名称容易造成混淆。）</para>

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

<para> 玩家列表管理/身份验证。</para>
<para> 检索要发送给希望验证您身份的实体的票据（使用 BeginAuthSession API）。</para>
<para> pcbTicket 用于检索实际票据的长度。</para>
<para> SteamNetworkingIdentity 是一个可选参数，用于保存您正在连接的实体的公共 IP 地址。</para>
<para> 如果传入了 IP 地址，Steam 将只允许该票据被具有该 IP 地址的实体使用。</para>

**参数:**

- `pTicket` (`byte[]`)
- `cbMaxTicket` (`int`)
- `pcbTicket` (`out uint`)
- `pSnid` (`ref SteamNetworkingIdentity`)

**返回值:** `HAuthTicket`

**用法示例:**
```csharp
byte[] ticket = new byte[1024]; SteamGameServer.GetAuthSessionTicket(ticket, ticket.Length, out uint ticketLen, ref defaultSteamNetworkingIdentity);
```

### BeginAuthSession (静态)

```csharp
EBeginAuthSessionResult BeginAuthSession(byte[] pAuthTicket, int cbAuthTicket, CSteamID steamID)
```

<para> 验证来自实体steamID的身份验证票据（来自GetAuthSessionTicket），以确保其有效且未被重复使用</para>
<para> 注册回调函数以处理实体离线或取消票据的情况（参见ValidateAuthTicketResponse_t回调与EAuthSessionResponse）</para>

**参数:**

- `pAuthTicket` (`byte[]`)
- `cbAuthTicket` (`int`)
- `steamID` (`CSteamID`)

**返回值:** `EBeginAuthSessionResult`

**用法示例:**
```csharp
var result = SteamGameServer.BeginAuthSession(authTicket, authTicket.Length, steamID);
```

### EndAuthSession (静态)

```csharp
void EndAuthSession(CSteamID steamID)
```

<para> 停止由 BeginAuthSession 启动的跟踪 - 当不再与此实体进行游戏时调用</para>

**参数:**

- `steamID` (`CSteamID`)

**用法示例:**
```csharp
SteamGameServer.EndAuthSession(clientSteamID);
```

### CancelAuthTicket (静态)

```csharp
void CancelAuthTicket(HAuthTicket hAuthTicket)
```

<para> 取消从GetAuthSessionTicket获取的认证票据，当您不再与您授予票据的实体进行游戏时调用</para>

**参数:**

- `hAuthTicket` (`HAuthTicket`)

**用法示例:**
```csharp
SteamGameServer.CancelAuthTicket(authTicket);
```

### UserHasLicenseForApp (静态)

```csharp
EUserHasLicenseForAppResult UserHasLicenseForApp(CSteamID steamID, AppId_t appID)
```

<para> 在接收到用户的身份验证数据并将其传递给 SendUserConnectAndAuthenticate 后，使用此函数</para>
<para> 来确定该用户是否拥有指定 AppID 所对应的可下载内容。</para>

**参数:**

- `steamID` (`CSteamID`)
- `appID` (`AppId_t`)

**返回值:** `EUserHasLicenseForAppResult`

**用法示例:**
```csharp
var result = SteamGameServer.UserHasLicenseForApp(steamID, appID);
```

### RequestUserGroupStatus (静态)

```csharp
bool RequestUserGroupStatus(CSteamID steamIDUser, CSteamID steamIDGroup)
```

<para> 询问用户是否在指定组中，结果将通过 GSUserGroupStatus_t 异步返回</para>
<para> 如果未连接到 Steam 服务器，因而无法询问，则返回 false</para>

**参数:**

- `steamIDUser` (`CSteamID`)
- `steamIDGroup` (`CSteamID`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = SteamGameServer.RequestUserGroupStatus(steamIDUser, steamIDGroup);
```

### GetGameplayStats (静态)

```csharp
void GetGameplayStats()
```

<para>这两个函数已被弃用，将不再返回结果</para>
<para>它们将在未来版本的SDK中被移除</para>

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
SteamAPICall_t callHandle = SteamGameServer.GetServerReputation();
```

### GetPublicIP (静态)

```csharp
SteamIPAddress_t GetPublicIP()
```

<para> 根据Steam返回服务器的公网IP，当服务器处于NAT后方且您希望在游戏大厅中通告其IP以供其他客户端直接连接时，此功能非常有用</para>

**返回值:** `SteamIPAddress_t`

**用法示例:**
```csharp
SteamIPAddress_t publicIP = SteamGameServer.GetPublicIP();
```

### HandleIncomingPacket (静态)

```csharp
bool HandleIncomingPacket(byte[] pData, int cbData, uint srcIP, ushort srcPort)
```

<para> 用于共享套接字模式的服务器浏览器相关查询数据包处理。当你将 STEAMGAMESERVER_QUERY_PORT_SHARED 作为查询端口传递给 SteamGameServer_Init 时，会使用这些处理逻辑。</para>
<para> IP 地址和端口采用主机字节序，例如 127.0.0.1 == 0x7f000001</para>
<para> 当你选择复用游戏服务器的 UDP 套接字，而不是让主服务器更新程序使用其自身套接字时，会使用这些逻辑。</para>
<para> 起源引擎游戏通过此功能简化服务器管理员的工作，这样他们就不必在防火墙上开放更多端口。</para>
<para> 当接收到以 0xFFFFFFFF 开头的数据包时，调用此方法。这意味着该数据包是发送给我们的。</para>

**参数:**

- `pData` (`byte[]`)
- `cbData` (`int`)
- `srcIP` (`uint`)
- `srcPort` (`ushort`)

**返回值:** `bool`

**用法示例:**
```csharp
bool handled = SteamGameServer.HandleIncomingPacket(packetData, packetData.Length, 0x7f000001, 27015);
```

### GetNextOutgoingPacket (静态)

```csharp
int GetNextOutgoingPacket(byte[] pOut, int cbMaxOut, out uint pNetAdr, out ushort pPort)
```

<para> 在调用 HandleIncomingPacket 处理该帧内传入的所有数据包之后，请调用此方法。</para> <para> 此方法获取主服务器更新器需要通过 UDP 发送的数据包。</para> <para> 返回需要发送的数据包长度，如果没有更多数据包需要发送则返回 0。</para> <para> 每帧调用此方法直至其返回 0。</para>

**参数:**

- `pOut` (`byte[]`)
- `cbMaxOut` (`int`)
- `pNetAdr` (`out uint`)
- `pPort` (`out ushort`)

**返回值:** `int`

**用法示例:**
```csharp
var buffer = new byte[1024];
int len = SteamGameServer.GetNextOutgoingPacket(buffer, buffer.Length, out uint adr, out ushort port);
```

### AssociateWithClan (静态)

```csharp
SteamAPICall_t AssociateWithClan(CSteamID steamIDClan)
```

<para> 服务器战队关联 </para>
<para> 将此游戏服务器与该战队关联，用于计算玩家兼容性 </para>

**参数:**

- `steamIDClan` (`CSteamID`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
CSteamID clanId = new CSteamID(103582791429521412);
SteamGameServer.AssociateWithClan(clanId);
```

### ComputeNewPlayerCompatibility (静态)

```csharp
SteamAPICall_t ComputeNewPlayerCompatibility(CSteamID steamIDNewPlayer)
```

<para>询问当前是否有任何玩家不想与该新玩家一起游戏 - 反之亦然</para>

**参数:**

- `steamIDNewPlayer` (`CSteamID`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServer.ComputeNewPlayerCompatibility(steamID);
```

### SendUserConnectAndAuthenticate_DEPRECATED (静态)

```csharp
bool SendUserConnectAndAuthenticate_DEPRECATED(uint unIPClient, byte[] pvAuthBlob, uint cubAuthBlobSize, out CSteamID pSteamIDUser)
```

<para> 处理来自Steam用户的新连接。此调用将请求Steam服务器验证用户身份、应用程序所有权以及VAC状态。如果Steam服务器离线，则会自行验证缓存的票据，从而验证应用程序所有权和身份。此处的AuthBlob应在游戏客户端通过SteamUser()-&gt;InitiateGameConnection()获取，并必须发送至游戏服务器进行身份验证。</para>
<para> 返回值：如果用户票据通过基本检查，则返回true。pSteamIDUser将包含该用户的Steam ID。pSteamIDUser不可为NULL。</para>
<para> 若调用成功，您应收到GSClientApprove_t或GSClientDeny_t回调，以告知用户身份验证是否成功（回调中的Steam ID将与此次调用返回的ID一致）。</para>
<para> 已弃用！此函数将在即将发布的SDK版本中移除。</para>
<para> 请迁移至BeginAuthSession及相关函数。</para>

**参数:**

- `unIPClient` (`uint`)
- `pvAuthBlob` (`byte[]`)
- `cubAuthBlobSize` (`uint`)
- `pSteamIDUser` (`out CSteamID`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = SteamGameServer.SendUserConnectAndAuthenticate_DEPRECATED(0xC0A80001, authBlob, (uint)authBlob.Length, out CSteamID steamID);
```

### CreateUnauthenticatedUserConnection (静态)

```csharp
CSteamID CreateUnauthenticatedUserConnection()
```

<para>创建一个虚假用户（即机器人），该用户将被列为在服务器上游戏，但跳过验证。</para>
<para>返回值：返回一个用于跟踪该用户的SteamID，当该用户离开服务器时，您应像对待真实用户一样调用EndAuthSession()。</para>

**返回值:** `CSteamID`

**用法示例:**
```csharp
CSteamID botId = SteamGameServer.CreateUnauthenticatedUserConnection();
```

### SendUserDisconnect_DEPRECATED (静态)

```csharp
void SendUserDisconnect_DEPRECATED(CSteamID steamIDUser)
```

<para> 当用户离开我们的游戏服务器时，应调用此函数，这能让Steam内部跟踪当前哪些用户位于哪些服务器上，以便防止单个账户登录到多个服务器、显示当前在服务器上的用户等。</para>
<para> 已弃用！此函数将在未来版本的SDK中移除。</para>
<para> 请迁移至BeginAuthSession及相关函数。</para>

**参数:**

- `steamIDUser` (`CSteamID`)

**用法示例:**
```csharp
SteamGameServer.SendUserDisconnect_DEPRECATED(steamIDUser);
```

### BUpdateUserData (静态)

```csharp
bool BUpdateUserData(CSteamID steamIDUser, string pchPlayerName, uint uScore)
```

<para> 更新服务器浏览器和匹配界面中要显示的数据，供当前连接到服务器的用户使用。</para>  
<para> 对于普通用户，您必须在收到 GSUserValidationSuccess 回调后调用此方法。</para>  
<para> 返回值：成功返回 true，失败返回 false（例如，steamIDUser 对应的玩家未处于活跃状态）。</para>

**参数:**

- `steamIDUser` (`CSteamID`)
- `pchPlayerName` (`string`)
- `uScore` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServer.BUpdateUserData(new CSteamID(76561198000000000), "PlayerOne", 100);
```

