# 📦 SteamGameServer

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### SetProduct (静态)

```csharp
void SetProduct(string pszProduct)
```

<para>/ 游戏产品标识符。当前由主服务器用于版本检查。</para> <para>/ 这是必填字段，但最终将被移除，届时将使用 AppID 实现此目的。</para>

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

<para>/ 游戏描述。这是一个必填字段，当前将显示在 Steam 服务器浏览器中。</para> <para>/ 这是一个必填字段，但未来将被移除，因为该数据应从 AppID 确定。</para>

**参数:**

- `pszGameDescription` (`string`)

**用法示例:**
```csharp
SteamGameServer.SetGameDescription("My Awesome Dedicated Server");
```

### SetModDir (静态)

```csharp
void SetModDir(string pszModDir)
```

<para>/ 如果您的游戏是“模组”（mod），请传入标识它的字符串。默认值为空字符串，表示</para> <para>/ 此应用程序为原版游戏，而非模组。</para> <para>/</para> <para>/ @see k_cbMaxGameServerGameDir</para>

**参数:**

- `pszModDir` (`string`)

**用法示例:**
```csharp
SteamGameServer.SetModDir("my_mod");
```

### SetDedicatedServer (静态)

```csharp
void SetDedicatedServer(bool bDedicated)
```

<para>/ 这是否是一个专用服务器？默认值为 false。</para>

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

<para>登录</para> <para>/ 开始向持久化游戏服务器账户进行登录的流程</para> <para>/</para> <para>/ 您需要注册回调以获取此操作的结果。</para> <para>/ @see SteamServersConnected_t</para> <para>/ @see SteamServerConnectFailure_t</para> <para>/ @see SteamServersDisconnected_t</para>

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

<para>/ 登录通用匿名账户。</para> <para>/</para> <para>/ 注意：在 SDK 的早期版本中，此操作会自动在 SteamGameServer_Init 内调用，但目前已不再如此。</para>

**用法示例:**
```csharp
SteamGameServer.LogOnAnonymous();
```

### LogOff (静态)

```csharp
void LogOff()
```

<para>/ 开始将游戏服务器从 Steam 登出</para>

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
Console.WriteLine(isLoggedOn);
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
CSteamID steamId = SteamGameServer.GetSteamID();
```

### WasRestartRequested (静态)

```csharp
bool WasRestartRequested()
```

/ 若主服务器已请求重启，则返回 true。  
/ 每个请求仅返回一次 true。

**返回值:** `bool`

**用法示例:**
```csharp
if (SteamGameServer.WasRestartRequested()) Console.WriteLine("Restart requested by master server.");
```

### SetMaxPlayerCount (静态)

```csharp
void SetMaxPlayerCount(int cPlayersMax)
```

<para>服务器状态。这些属性可能随时更改。</para><para>/ 向服务器浏览器和客户端查询报告的 maximum 玩家数量</para>

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

<para>/ 机器人数量。默认值为零</para>

**参数:**

- `cBotplayers` (`int`)

**用法示例:**
```csharp
SteamGameServer.SetBotPlayerCount(3);
```

### SetServerName (静态)

```csharp
void SetServerName(string pszServerName)
```

<para>/ 设置服务器名称，该名称将显示在服务器浏览器中</para> <para>/</para> <para>/ @see k_cbMaxGameServerName</para>

**参数:**

- `pszServerName` (`string`)

**用法示例:**
```csharp
SteamGameServer.SetServerName("My Dedicated Server");
```

### SetMapName (静态)

```csharp
void SetMapName(string pszMapName)
```

<para>/ 设置将在服务器浏览器中报告的地图名称</para> <para>/</para> <para>/ @see k_cbMaxGameServerMapName</para>

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

<para>/ 告知玩家您的服务器是否需要密码</para>

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

<para>/ 用于宣告的观战服务器端口。默认值为零，表示不使用该服务。如果您的服务器在局域网内收到任何信息请求，</para> <para>/ 此值将作为本地查询回复中的内容。</para> <para>/</para> <para>/ 这也是由主服务器宣告的值。</para> <para>/ 唯一的例外情况是您的服务器使用了虚假 IP（FakeIP）。此时，若将此值设置为任何非零值，则分配给服务器的第二个</para> <para>/ 虚假端口号（索引 1）将在主服务器上被列为观战端口。</para> <para>/</para> <para>/ 此函数仅控制所宣告的值；您需自行配置服务器以实际在该端口上监听并处理所有观战流量。</para>

**参数:**

- `unSpectatorPort` (`ushort`)

**用法示例:**
```csharp
SteamGameServer.SetSpectatorPort(27020);
```

### SetSpectatorServerName (静态)

```csharp
void SetSpectatorServerName(string pszSpectatorServerName)
```

<para>/ 旁观者服务器的名称。（仅在 spectator 端口非零时使用。）</para> <para>/</para> <para>/ @see k_cbMaxGameServerMapName</para>

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

<para>/ 调用此方法以清除规则查询中发送的所有键/值列表。</para>

**用法示例:**
```csharp
SteamGameServer.ClearAllKeyValues();
```

### SetKeyValue (静态)

```csharp
void SetKeyValue(string pKey, string pValue)
```

<para>/ 调用此方法以添加或更新键/值对。</para>

**参数:**

- `pKey` (`string`)
- `pValue` (`string`)

**用法示例:**
```csharp
SteamGameServer.SetKeyValue("sv_region", "CN");
```

### SetGameTags (静态)

```csharp
void SetGameTags(string pchGameTags)
```

<para>/ 设置一个字符串以定义本服务器的“游戏标签”，此为可选参数。若已设置，</para> <para>/ 用户可在匹配/服务器浏览器界面中根据该值进行筛选。</para> <para>/</para> <para>/ @see k_cbMaxGameServerTags</para>

**参数:**

- `pchGameTags` (`string`)

**用法示例:**
```csharp
SteamGameServer.SetGameTags("ranked,pvp,hardcore");
```

### SetGameData (静态)

```csharp
void SetGameData(string pchGameData)
```

<para>/ 设置一个定义该服务器“游戏数据”的字符串。此参数为可选，但若已设置</para> <para>/ 则允许用户在匹配或服务器浏览器界面中根据该值进行筛选。</para> <para>/</para> <para>/ @see k_cbMaxGameServerGameData</para>

**参数:**

- `pchGameData` (`string`)

**用法示例:**
```csharp
SteamGameServer.SetGameData("mode=deathmatch;map=arena");
```

### SetRegion (静态)

```csharp
void SetRegion(string pszRegion)
```

<para>/ 区域标识符。此字段为可选，默认值为空，表示“世界”区域</para>

**参数:**

- `pszRegion` (`string`)

**用法示例:**
```csharp
SteamGameServer.SetRegion("CN");
```

### SetAdvertiseServerActive (静态)

```csharp
void SetAdvertiseServerActive(bool bActive)
```

<para>/ 指示是否希望在主服务器列表中列出</para> <para>/ 以及/或响应服务器浏览器 / LAN 发现数据包。</para> <para>/ 服务器启动时此值默认为 false。在启用服务器广播前，您应设置所有</para> <para>/ 相关的服务器参数。</para> <para>/</para> <para>/ （此函数曾名为 EnableHeartbeats；如果您疑惑该函数的去向，它便在此处。其功能与之前相同，旧名称只是令人困惑。）</para>

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

<para>玩家列表管理与身份验证。</para><para>获取票据，该票据将发送给希望验证您身份的实体（通过 BeginAuthSession API）。</para><para>pcbTicket 用于获取实际票据的长度。</para><para>SteamNetworkingIdentity 为可选参数，用于保存您要连接的实体的公网 IP 地址。</para><para>若传递了 IP 地址，Steam 将仅允许具有该 IP 地址的实体使用该票据。</para>

**参数:**

- `pTicket` (`byte[]`)
- `cbMaxTicket` (`int`)
- `pcbTicket` (`out uint`)
- `pSnid` (`ref SteamNetworkingIdentity`)

**返回值:** `HAuthTicket`

**用法示例:**
```csharp
uint ticketLen; HAuthTicket ticket = SteamGameServer.GetAuthSessionTicket(ticketBuffer, ticketBuffer.Length, out ticketLen, ref snid);
```

### BeginAuthSession (静态)

```csharp
EBeginAuthSessionResult BeginAuthSession(byte[] pAuthTicket, int cbAuthTicket, CSteamID steamID)
```

<para>对来自 GetAuthSessionTicket 的票据进行身份验证，将其与实体 steamID 关联，以确保其有效且未被重复使用</para> <para>注册回调以监听该实体下线或取消票据的情况（参见 ValidateAuthTicketResponse_t 回调及 EAuthSessionResponse）</para>

**参数:**

- `pAuthTicket` (`byte[]`)
- `cbAuthTicket` (`int`)
- `steamID` (`CSteamID`)

**返回值:** `EBeginAuthSessionResult`

**用法示例:**
```csharp
var result = SteamGameServer.BeginAuthSession(authTicket, authTicket.Length, playerSteamID);
```

### EndAuthSession (静态)

```csharp
void EndAuthSession(CSteamID steamID)
```

<para>停止由 BeginAuthSession 启动的跟踪 - 当不再与此实体进行游戏时调用</para>

**参数:**

- `steamID` (`CSteamID`)

**用法示例:**
```csharp
CSteamID steamID = playerSteamId;
SteamGameServer.EndAuthSession(steamID);
```

### CancelAuthTicket (静态)

```csharp
void CancelAuthTicket(HAuthTicket hAuthTicket)
```

取消从 GetAuthSessionTicket 获取的身份验证票据；在与提供该票据的实体不再共同进行游戏时调用。

**参数:**

- `hAuthTicket` (`HAuthTicket`)

**用法示例:**
```csharp
SteamGameServer.CancelAuthTicket(hAuthTicket);
```

### UserHasLicenseForApp (静态)

```csharp
EUserHasLicenseForAppResult UserHasLicenseForApp(CSteamID steamID, AppId_t appID)
```

<para>在接收用户的身份验证数据并将其传递给 SendUserConnectAndAuthenticate 后，请使用此函数</para> <para>以确定该用户是否拥有由所提供的 AppID 指定的可下载内容。</para>

**参数:**

- `steamID` (`CSteamID`)
- `appID` (`AppId_t`)

**返回值:** `EUserHasLicenseForAppResult`

**用法示例:**
```csharp
var licenseResult = SteamGameServer.UserHasLicenseForApp(steamID, appID);
if (licenseResult == EUserHasLicenseForAppResult.HasLicense) { }
```

### RequestUserGroupStatus (静态)

```csharp
bool RequestUserGroupStatus(CSteamID steamIDUser, CSteamID steamIDGroup)
```

<para>询问指定用户是否属于指定组，结果通过 GSUserGroupStatus_t 异步返回</para><para>如果未连接到 Steam 服务器且因此无法发起查询，则返回 false</para>

**参数:**

- `steamIDUser` (`CSteamID`)
- `steamIDGroup` (`CSteamID`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServer.RequestUserGroupStatus(steamIDUser, steamIDGroup);
```

### GetGameplayStats (静态)

```csharp
void GetGameplayStats()
```

<para> 这两个函数已弃用，将不再返回结果。</para><para> 它们将在 SDK 的未来版本中被移除。</para>

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
var call = SteamGameServer.GetServerReputation();
```

### GetPublicIP (静态)

```csharp
SteamIPAddress_t GetPublicIP()
```

返回根据 Steam 获取的服务器公网 IP，当服务器位于 NAT 之后且您希望在大厅中公布其 IP 以供其他客户端直接连接时，此方法非常有用。

**返回值:** `SteamIPAddress_t`

**用法示例:**
```csharp
var publicIP = SteamGameServer.GetPublicIP();
Console.WriteLine(publicIP);
```

### HandleIncomingPacket (静态)

```csharp
bool HandleIncomingPacket(byte[] pData, int cbData, uint srcIP, ushort srcPort)
```

与服务器浏览器相关的查询数据包处理，适用于共享套接字模式。当您在调用 SteamGameServer_Init 时将 STEAMGAMESERVER_QUERY_PORT_SHARED 作为查询端口传入时，会使用这些接口。IP 地址和端口均以主机字节序表示，例如 127.0.0.1 对应 0x7f000001。这些接口用于您选择复用作游戏服务器的 UDP 套接字，而非由主服务器更新器使用其独立套接字的场景。Source 系列游戏采用此机制以简化服务器管理员的工作，使其无需在防火墙上额外开放更多端口。当收到以 0xFFFFFFFF 开头的数据包时，请调用此函数；这表示该数据包是发往本服务器的。

**参数:**

- `pData` (`byte[]`)
- `cbData` (`int`)
- `srcIP` (`uint`)
- `srcPort` (`ushort`)

**返回值:** `bool`

**用法示例:**
```csharp
byte[] packet = { 0xFF, 0xFF, 0xFF, 0xFF };
bool handled = SteamGameServer.HandleIncomingPacket(packet, packet.Length, 0x7f000001, 27015);
```

### GetNextOutgoingPacket (静态)

```csharp
int GetNextOutgoingPacket(byte[] pOut, int cbMaxOut, out uint pNetAdr, out ushort pPort)
```

<para>在调用 HandleIncomingPacket 处理该帧内收到的任何数据包后，请调用此方法。</para> <para>此方法获取主服务器更新器需要通过 UDP 发送的数据包。</para> <para>它返回待发送数据包的长度；若无更多数据包可发送，则返回 0。</para> <para>每帧调用一次，直到返回值变为 0 为止。</para>

**参数:**

- `pOut` (`byte[]`)
- `cbMaxOut` (`int`)
- `pNetAdr` (`out uint`)
- `pPort` (`out ushort`)

**返回值:** `int`

**用法示例:**
```csharp
uint netAdr; ushort port; int len;
while ((len = SteamGameServer.GetNextOutgoingPacket(buffer, buffer.Length, out netAdr, out port)) > 0) SendUdp(netAdr, port, buffer, len);
```

### AssociateWithClan (静态)

```csharp
SteamAPICall_t AssociateWithClan(CSteamID steamIDClan)
```

<para>服务器公会关联</para><para>将此游戏服务器与该公会关联，用于计算玩家兼容性</para>

**参数:**

- `steamIDClan` (`CSteamID`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServer.AssociateWithClan(clanId);
```

### ComputeNewPlayerCompatibility (静态)

```csharp
SteamAPICall_t ComputeNewPlayerCompatibility(CSteamID steamIDNewPlayer)
```

<para>询问当前玩家中是否有人不愿与该新玩家组队——或反之</para>

**参数:**

- `steamIDNewPlayer` (`CSteamID`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServer.ComputeNewPlayerCompatibility(steamIDNewPlayer);
```

### SendUserConnectAndAuthenticate_DEPRECATED (静态)

```csharp
bool SendUserConnectAndAuthenticate_DEPRECATED(uint unIPClient, byte[] pvAuthBlob, uint cubAuthBlobSize, out CSteamID pSteamIDUser)
```

<para>处理来自 Steam 用户的新连接请求。此调用将要求 Steam 服务器验证用户的身份、应用所有权以及 VAC 状态。如果 Steam 服务器离线，则系统将自行验证缓存票据以确认应用所有权和身份。AuthBlob 应通过游戏客户端中的 SteamUser()->InitiateGameConnection() 获取，随后必须将其发送至游戏服务器进行认证。</para><para>返回值：若用户票据通过基本检查则返回 true。pSteamIDUser 将包含该用户的 Steam ID。pSteamIDUser 不得为 NULL。</para><para>若调用成功，预期将收到 GSClientApprove_t 或 GSClientDeny_t 回调，该回调将告知用户认证成功或失败（回调中的 Steam ID 将与本调用返回的 ID 一致）。</para><para>已弃用！此函数将在未来版本的 SDK 中被移除。</para><para>请迁移至 BeginAuthSession 及相关函数。</para>

**参数:**

- `unIPClient` (`uint`)
- `pvAuthBlob` (`byte[]`)
- `cubAuthBlobSize` (`uint`)
- `pSteamIDUser` (`out CSteamID`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServer.SendUserConnectAndAuthenticate_DEPRECATED(unIPClient, authBlob, (uint)authBlob.Length, out CSteamID steamIdUser);
```

### CreateUnauthenticatedUserConnection (静态)

```csharp
CSteamID CreateUnauthenticatedUserConnection()
```

<para>创建一个虚假用户（即机器人），该用户将显示为正在服务器上游戏，但会跳过验证。</para><para>返回值：返回用于跟踪该用户的 SteamID，当该用户离开服务器时，应像对待真实用户一样调用 EndAuthSession()。</para>

**返回值:** `CSteamID`

**用法示例:**
```csharp
CSteamID botSteamId = SteamGameServer.CreateUnauthenticatedUserConnection();
```

### SendUserDisconnect_DEPRECATED (静态)

```csharp
void SendUserDisconnect_DEPRECATED(CSteamID steamIDUser)
```

当用户离开我们的游戏服务器时应调用此方法，它允许 Steam 内部跟踪当前哪些用户位于哪些服务器上，以防止单个账户同时登录多个服务器、显示当前在服务器上的用户等操作。已弃用！此函数将在后续版本的 SDK 中被移除。请迁移至 BeginAuthSession 及相关函数。

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

<para>更新当前连接到服务器的用户在服务器浏览器和匹配界面中显示的数据。</para> <para>对于普通用户，必须在收到 GSUserValidationSuccess 回调后调用此方法。</para> <para>返回值：如果成功返回 true，失败返回 false（例如，steamIDUser 不对应活跃玩家）。</para>

**参数:**

- `steamIDUser` (`CSteamID`)
- `pchPlayerName` (`string`)
- `uScore` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServer.BUpdateUserData(steamIDUser, "PlayerOne", 100);
```

