# 📚 GameEventDefinitions

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

共 276 个定义

## 📋 目录

- 🔌 [EventAchievementEarned](#eventachievementearned)
- 🔌 [EventAchievementEarnedLocal](#eventachievementearnedlocal)
- 🔌 [EventAchievementEvent](#eventachievementevent)
- 🔌 [EventAchievementInfoLoaded](#eventachievementinfoloaded)
- 🔌 [EventAchievementWriteFailed](#eventachievementwritefailed)
- 🔌 [EventAddBulletHitMarker](#eventaddbullethitmarker)
- 🔌 [EventAddPlayerSonarIcon](#eventaddplayersonaricon)
- 🔌 [EventAmmoPickup](#eventammopickup)
- 🔌 [EventAmmoRefill](#eventammorefill)
- 🔌 [EventAnnouncePhaseEnd](#eventannouncephaseend)
- 🔌 [EventBeginNewMatch](#eventbeginnewmatch)
- 🔌 [EventBombAbortdefuse](#eventbombabortdefuse)
- 🔌 [EventBombAbortplant](#eventbombabortplant)
- 🔌 [EventBombBeep](#eventbombbeep)
- 🔌 [EventBombBegindefuse](#eventbombbegindefuse)
- 🔌 [EventBombBeginplant](#eventbombbeginplant)
- 🔌 [EventBombDefused](#eventbombdefused)
- 🔌 [EventBombDropped](#eventbombdropped)
- 🔌 [EventBombExploded](#eventbombexploded)
- 🔌 [EventBombPickup](#eventbombpickup)
- 🔌 [EventBombPlanted](#eventbombplanted)
- 🔌 [EventBonusUpdated](#eventbonusupdated)
- 🔌 [EventBotTakeover](#eventbottakeover)
- 🔌 [EventBreakBreakable](#eventbreakbreakable)
- 🔌 [EventBreakProp](#eventbreakprop)
- 🔌 [EventBrokenBreakable](#eventbrokenbreakable)
- 🔌 [EventBulletDamage](#eventbulletdamage)
- 🔌 [EventBulletImpact](#eventbulletimpact)
- 🔌 [EventBuymenuClose](#eventbuymenuclose)
- 🔌 [EventBuymenuOpen](#eventbuymenuopen)
- 🔌 [EventBuytimeEnded](#eventbuytimeended)
- 🔌 [EventCartUpdated](#eventcartupdated)
- 🔌 [EventChoppersIncomingWarning](#eventchoppersincomingwarning)
- 🔌 [EventClientDisconnect](#eventclientdisconnect)
- 🔌 [EventClientLoadoutChanged](#eventclientloadoutchanged)
- 🔌 [EventClientsideLessonClosed](#eventclientsidelessonclosed)
- 🔌 [EventClientsideReloadCustomEcon](#eventclientsidereloadcustomecon)
- 🔌 [EventCoreGameEvents](#eventcoregameevents)
- 🔌 [EventCsGameDisconnected](#eventcsgamedisconnected)
- 🔌 [EventCsIntermission](#eventcsintermission)
- 🔌 [EventCsMatchEndRestart](#eventcsmatchendrestart)
- 🔌 [EventCsPreRestart](#eventcsprerestart)
- 🔌 [EventCsPrevNextSpectator](#eventcsprevnextspectator)
- 🔌 [EventCsRoundFinalBeep](#eventcsroundfinalbeep)
- 🔌 [EventCsRoundStartBeep](#eventcsroundstartbeep)
- 🔌 [EventCsWinPanelMatch](#eventcswinpanelmatch)
- 🔌 [EventCsWinPanelRound](#eventcswinpanelround)
- 🔌 [EventCstrikeevents](#eventcstrikeevents)
- 🔌 [EventDecoyDetonate](#eventdecoydetonate)
- 🔌 [EventDecoyFiring](#eventdecoyfiring)
- 🔌 [EventDecoyStarted](#eventdecoystarted)
- 🔌 [EventDefuserDropped](#eventdefuserdropped)
- 🔌 [EventDefuserPickup](#eventdefuserpickup)
- 🔌 [EventDemoSkip](#eventdemoskip)
- 🔌 [EventDemoStart](#eventdemostart)
- 🔌 [EventDemoStop](#eventdemostop)
- 🔌 [EventDifficultyChanged](#eventdifficultychanged)
- 🔌 [EventDmBonusWeaponStart](#eventdmbonusweaponstart)
- 🔌 [EventDoorBreak](#eventdoorbreak)
- 🔌 [EventDoorClose](#eventdoorclose)
- 🔌 [EventDoorClosed](#eventdoorclosed)
- 🔌 [EventDoorMoving](#eventdoormoving)
- 🔌 [EventDoorOpen](#eventdooropen)
- 🔌 [EventDroneAboveRoof](#eventdroneaboveroof)
- 🔌 [EventDroneCargoDetached](#eventdronecargodetached)
- 🔌 [EventDroneDispatched](#eventdronedispatched)
- 🔌 [EventDronegunAttack](#eventdronegunattack)
- 🔌 [EventDropRateModified](#eventdropratemodified)
- 🔌 [EventDynamicShadowLightChanged](#eventdynamicshadowlightchanged)
- 🔌 [EventDzItemInteraction](#eventdziteminteraction)
- 🔌 [EventEnableRestartVoting](#eventenablerestartvoting)
- 🔌 [EventEndmatchCmmStartRevealItems](#eventendmatchcmmstartrevealitems)
- 🔌 [EventEndmatchMapvoteSelectingMap](#eventendmatchmapvoteselectingmap)
- 🔌 [EventEnterBombzone](#evententerbombzone)
- 🔌 [EventEnterBuyzone](#evententerbuyzone)
- 🔌 [EventEnterRescueZone](#evententerrescuezone)
- 🔌 [EventEntityKilled](#evententitykilled)
- 🔌 [EventEntityVisible](#evententityvisible)
- 🔌 [EventEventTicketModified](#eventeventticketmodified)
- 🔌 [EventExitBombzone](#eventexitbombzone)
- 🔌 [EventExitBuyzone](#eventexitbuyzone)
- 🔌 [EventExitRescueZone](#eventexitrescuezone)
- 🔌 [EventFinaleStart](#eventfinalestart)
- 🔌 [EventFirstbombsIncomingWarning](#eventfirstbombsincomingwarning)
- 🔌 [EventFlareIgniteNpc](#eventflareignitenpc)
- 🔌 [EventFlashbangDetonate](#eventflashbangdetonate)
- 🔌 [EventGameEnd](#eventgameend)
- 🔌 [EventGameInit](#eventgameinit)
- 🔌 [EventGameMessage](#eventgamemessage)
- 🔌 [EventGameNewmap](#eventgamenewmap)
- 🔌 [EventGamePhaseChanged](#eventgamephasechanged)
- 🔌 [EventGameStart](#eventgamestart)
- 🔌 [EventGameevents](#eventgameevents)
- 🔌 [EventGameinstructorDraw](#eventgameinstructordraw)
- 🔌 [EventGameinstructorNodraw](#eventgameinstructornodraw)
- 🔌 [EventGameuiHidden](#eventgameuihidden)
- 🔌 [EventGcConnected](#eventgcconnected)
- 🔌 [EventGgKilledEnemy](#eventggkilledenemy)
- 🔌 [EventGrenadeBounce](#eventgrenadebounce)
- 🔌 [EventGrenadeThrown](#eventgrenadethrown)
- 🔌 [EventGuardianWaveRestart](#eventguardianwaverestart)
- 🔌 [EventHegrenadeDetonate](#eventhegrenadedetonate)
- 🔌 [EventHelicopterGrenadePuntMiss](#eventhelicoptergrenadepuntmiss)
- 🔌 [EventHideDeathpanel](#eventhidedeathpanel)
- 🔌 [EventHltvCameraman](#eventhltvcameraman)
- 🔌 [EventHltvChangedMode](#eventhltvchangedmode)
- 🔌 [EventHltvChase](#eventhltvchase)
- 🔌 [EventHltvChat](#eventhltvchat)
- 🔌 [EventHltvFixed](#eventhltvfixed)
- 🔌 [EventHltvMessage](#eventhltvmessage)
- 🔌 [EventHltvRankCamera](#eventhltvrankcamera)
- 🔌 [EventHltvRankEntity](#eventhltvrankentity)
- 🔌 [EventHltvReplay](#eventhltvreplay)
- 🔌 [EventHltvReplayStatus](#eventhltvreplaystatus)
- 🔌 [EventHltvStatus](#eventhltvstatus)
- 🔌 [EventHltvTitle](#eventhltvtitle)
- 🔌 [EventHltvVersioninfo](#eventhltvversioninfo)
- 🔌 [EventHostageCallForHelp](#eventhostagecallforhelp)
- 🔌 [EventHostageFollows](#eventhostagefollows)
- 🔌 [EventHostageHurt](#eventhostagehurt)
- 🔌 [EventHostageKilled](#eventhostagekilled)
- 🔌 [EventHostageRescued](#eventhostagerescued)
- 🔌 [EventHostageRescuedAll](#eventhostagerescuedall)
- 🔌 [EventHostageStopsFollowing](#eventhostagestopsfollowing)
- 🔌 [EventHostnameChanged](#eventhostnamechanged)
- 🔌 [EventInfernoExpire](#eventinfernoexpire)
- 🔌 [EventInfernoExtinguish](#eventinfernoextinguish)
- 🔌 [EventInfernoStartburn](#eventinfernostartburn)
- 🔌 [EventInspectWeapon](#eventinspectweapon)
- 🔌 [EventInstructorCloseLesson](#eventinstructorcloselesson)
- 🔌 [EventInstructorServerHintCreate](#eventinstructorserverhintcreate)
- 🔌 [EventInstructorServerHintStop](#eventinstructorserverhintstop)
- 🔌 [EventInstructorStartLesson](#eventinstructorstartlesson)
- 🔌 [EventInventoryUpdated](#eventinventoryupdated)
- 🔌 [EventItemEquip](#eventitemequip)
- 🔌 [EventItemPickup](#eventitempickup)
- 🔌 [EventItemPickupFailed](#eventitempickupfailed)
- 🔌 [EventItemPickupSlerp](#eventitempickupslerp)
- 🔌 [EventItemPurchase](#eventitempurchase)
- 🔌 [EventItemRemove](#eventitemremove)
- 🔌 [EventItemSchemaInitialized](#eventitemschemainitialized)
- 🔌 [EventJointeamFailed](#eventjointeamfailed)
- 🔌 [EventLocalPlayerControllerTeam](#eventlocalplayercontrollerteam)
- 🔌 [EventLocalPlayerPawnChanged](#eventlocalplayerpawnchanged)
- 🔌 [EventLocalPlayerTeam](#eventlocalplayerteam)
- 🔌 [EventLootCrateOpened](#eventlootcrateopened)
- 🔌 [EventLootCrateVisible](#eventlootcratevisible)
- 🔌 [EventMapShutdown](#eventmapshutdown)
- 🔌 [EventMapTransition](#eventmaptransition)
- 🔌 [EventMatchEndConditions](#eventmatchendconditions)
- 🔌 [EventMaterialDefaultComplete](#eventmaterialdefaultcomplete)
- 🔌 [EventMbInputLockCancel](#eventmbinputlockcancel)
- 🔌 [EventMbInputLockSuccess](#eventmbinputlocksuccess)
- 🔌 [EventMolotovDetonate](#eventmolotovdetonate)
- 🔌 [EventNavBlocked](#eventnavblocked)
- 🔌 [EventNavGenerate](#eventnavgenerate)
- 🔌 [EventNextlevelChanged](#eventnextlevelchanged)
- 🔌 [EventOpenCrateInstr](#eventopencrateinstr)
- 🔌 [EventOtherDeath](#eventotherdeath)
- 🔌 [EventParachuteDeploy](#eventparachutedeploy)
- 🔌 [EventParachutePickup](#eventparachutepickup)
- 🔌 [EventPhysgunPickup](#eventphysgunpickup)
- 🔌 [EventPlayerActivate](#eventplayeractivate)
- 🔌 [EventPlayerAvengedTeammate](#eventplayeravengedteammate)
- 🔌 [EventPlayerBlind](#eventplayerblind)
- 🔌 [EventPlayerChangename](#eventplayerchangename)
- 🔌 [EventPlayerChat](#eventplayerchat)
- 🔌 [EventPlayerConnect](#eventplayerconnect)
- 🔌 [EventPlayerConnectFull](#eventplayerconnectfull)
- 🔌 [EventPlayerDeath](#eventplayerdeath)
- 🔌 [EventPlayerDecal](#eventplayerdecal)
- 🔌 [EventPlayerDisconnect](#eventplayerdisconnect)
- 🔌 [EventPlayerFalldamage](#eventplayerfalldamage)
- 🔌 [EventPlayerFootstep](#eventplayerfootstep)
- 🔌 [EventPlayerFullUpdate](#eventplayerfullupdate)
- 🔌 [EventPlayerGivenC4](#eventplayergivenc4)
- 🔌 [EventPlayerHintmessage](#eventplayerhintmessage)
- 🔌 [EventPlayerHurt](#eventplayerhurt)
- 🔌 [EventPlayerInfo](#eventplayerinfo)
- 🔌 [EventPlayerJump](#eventplayerjump)
- 🔌 [EventPlayerPing](#eventplayerping)
- 🔌 [EventPlayerPingStop](#eventplayerpingstop)
- 🔌 [EventPlayerRadio](#eventplayerradio)
- 🔌 [EventPlayerResetVote](#eventplayerresetvote)
- 🔌 [EventPlayerScore](#eventplayerscore)
- 🔌 [EventPlayerShoot](#eventplayershoot)
- 🔌 [EventPlayerSound](#eventplayersound)
- 🔌 [EventPlayerSpawn](#eventplayerspawn)
- 🔌 [EventPlayerSpawned](#eventplayerspawned)
- 🔌 [EventPlayerStatsUpdated](#eventplayerstatsupdated)
- 🔌 [EventPlayerTeam](#eventplayerteam)
- 🔌 [EventRagdollDissolved](#eventragdolldissolved)
- 🔌 [EventReadGameTitledata](#eventreadgametitledata)
- 🔌 [EventRepostXboxAchievements](#eventrepostxboxachievements)
- 🔌 [EventResetGameTitledata](#eventresetgametitledata)
- 🔌 [EventRoundAnnounceFinal](#eventroundannouncefinal)
- 🔌 [EventRoundAnnounceLastRoundHalf](#eventroundannouncelastroundhalf)
- 🔌 [EventRoundAnnounceMatchPoint](#eventroundannouncematchpoint)
- 🔌 [EventRoundAnnounceMatchStart](#eventroundannouncematchstart)
- 🔌 [EventRoundAnnounceWarmup](#eventroundannouncewarmup)
- 🔌 [EventRoundEnd](#eventroundend)
- 🔌 [EventRoundEndUploadStats](#eventroundenduploadstats)
- 🔌 [EventRoundFreezeEnd](#eventroundfreezeend)
- 🔌 [EventRoundMvp](#eventroundmvp)
- 🔌 [EventRoundOfficiallyEnded](#eventroundofficiallyended)
- 🔌 [EventRoundPoststart](#eventroundpoststart)
- 🔌 [EventRoundPrestart](#eventroundprestart)
- 🔌 [EventRoundStart](#eventroundstart)
- 🔌 [EventRoundStartPostNav](#eventroundstartpostnav)
- 🔌 [EventRoundStartPreEntity](#eventroundstartpreentity)
- 🔌 [EventRoundTimeWarning](#eventroundtimewarning)
- 🔌 [EventSeasoncoinLevelup](#eventseasoncoinlevelup)
- 🔌 [EventServerCvar](#eventservercvar)
- 🔌 [EventServerMessage](#eventservermessage)
- 🔌 [EventServerPreShutdown](#eventserverpreshutdown)
- 🔌 [EventServerShutdown](#eventservershutdown)
- 🔌 [EventServerSpawn](#eventserverspawn)
- 🔌 [EventSetInstructorGroupEnabled](#eventsetinstructorgroupenabled)
- 🔌 [EventSfuievent](#eventsfuievent)
- 🔌 [EventShowDeathpanel](#eventshowdeathpanel)
- 🔌 [EventShowSurvivalRespawnStatus](#eventshowsurvivalrespawnstatus)
- 🔌 [EventSilencerDetach](#eventsilencerdetach)
- 🔌 [EventSilencerOff](#eventsilenceroff)
- 🔌 [EventSilencerOn](#eventsilenceron)
- 🔌 [EventSmokeBeaconParadrop](#eventsmokebeaconparadrop)
- 🔌 [EventSmokegrenadeDetonate](#eventsmokegrenadedetonate)
- 🔌 [EventSmokegrenadeExpired](#eventsmokegrenadeexpired)
- 🔌 [EventSpecModeUpdated](#eventspecmodeupdated)
- 🔌 [EventSpecTargetUpdated](#eventspectargetupdated)
- 🔌 [EventStartHalftime](#eventstarthalftime)
- 🔌 [EventStartVote](#eventstartvote)
- 🔌 [EventStorePricesheetUpdated](#eventstorepricesheetupdated)
- 🔌 [EventSurvivalAnnouncePhase](#eventsurvivalannouncephase)
- 🔌 [EventSurvivalNoRespawnsFinal](#eventsurvivalnorespawnsfinal)
- 🔌 [EventSurvivalNoRespawnsWarning](#eventsurvivalnorespawnswarning)
- 🔌 [EventSurvivalParadropBreak](#eventsurvivalparadropbreak)
- 🔌 [EventSurvivalParadropSpawn](#eventsurvivalparadropspawn)
- 🔌 [EventSurvivalTeammateRespawn](#eventsurvivalteammaterespawn)
- 🔌 [EventSwitchTeam](#eventswitchteam)
- 🔌 [EventTagrenadeDetonate](#eventtagrenadedetonate)
- 🔌 [EventTeamInfo](#eventteaminfo)
- 🔌 [EventTeamIntroEnd](#eventteamintroend)
- 🔌 [EventTeamIntroStart](#eventteamintrostart)
- 🔌 [EventTeamScore](#eventteamscore)
- 🔌 [EventTeamchangePending](#eventteamchangepending)
- 🔌 [EventTeamplayBroadcastAudio](#eventteamplaybroadcastaudio)
- 🔌 [EventTeamplayRoundStart](#eventteamplayroundstart)
- 🔌 [EventTournamentReward](#eventtournamentreward)
- 🔌 [EventTrialTimeExpired](#eventtrialtimeexpired)
- 🔌 [EventUgcFileDownloadFinished](#eventugcfiledownloadfinished)
- 🔌 [EventUgcFileDownloadStart](#eventugcfiledownloadstart)
- 🔌 [EventUgcMapDownloadError](#eventugcmapdownloaderror)
- 🔌 [EventUgcMapInfoReceived](#eventugcmapinforeceived)
- 🔌 [EventUgcMapUnsubscribed](#eventugcmapunsubscribed)
- 🔌 [EventUpdateMatchmakingStats](#eventupdatematchmakingstats)
- 🔌 [EventUserDataDownloaded](#eventuserdatadownloaded)
- 🔌 [EventVipEscaped](#eventvipescaped)
- 🔌 [EventVipKilled](#eventvipkilled)
- 🔌 [EventVoteCast](#eventvotecast)
- 🔌 [EventVoteCastNo](#eventvotecastno)
- 🔌 [EventVoteCastYes](#eventvotecastyes)
- 🔌 [EventVoteChanged](#eventvotechanged)
- 🔌 [EventVoteEnded](#eventvoteended)
- 🔌 [EventVoteFailed](#eventvotefailed)
- 🔌 [EventVoteOptions](#eventvoteoptions)
- 🔌 [EventVotePassed](#eventvotepassed)
- 🔌 [EventVoteStarted](#eventvotestarted)
- 🔌 [EventWarmupEnd](#eventwarmupend)
- 🔌 [EventWeaponFire](#eventweaponfire)
- 🔌 [EventWeaponFireOnEmpty](#eventweaponfireonempty)
- 🔌 [EventWeaponReload](#eventweaponreload)
- 🔌 [EventWeaponZoom](#eventweaponzoom)
- 🔌 [EventWeaponZoomRifle](#eventweaponzoomrifle)
- 🔌 [EventWeaponhudSelection](#eventweaponhudselection)
- 🔌 [EventWriteGameTitledata](#eventwritegametitledata)
- 🔌 [EventWriteProfileData](#eventwriteprofiledata)

<a id="eventachievementearned"></a>

## 🔌 EventAchievementEarned

事件“成就达成”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAchievementEarned\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlayerController` | `CCSPlayerController` | get | 玩家的实体索引 <br/> 类型: player_controller |
| `PlayerPawn` | `CCSPlayerPawn` | get | 玩家的实体索引 <br/> 类型: player_controller |
| `Player` | `int` | get, set | 玩家的实体索引 <br/> 类型: player_controller |
| `Achievement` | `short` | get, set | 成就ID <br/> 类型：短整型 |



---

<a id="eventachievementearnedlocal"></a>

## 🔌 EventAchievementEarnedLocal

Event "achievement_earned_local"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAchievementEarnedLocal\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Achievement` | `short` | get, set | 成就ID <br/> 类型：短整型 |
| `SplitScreenPlayer` | `short` | get, set | 分屏ID <br/> 类型: short |



---

<a id="eventachievementevent"></a>

## 🔌 EventAchievementEvent

事件 "achievement_event"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAchievementEvent\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AchievementName` | `string` | get, set | 成就的非本地化名称<br/> 类型：字符串 |
| `CurVal` | `short` | get, set | 成就进度的步数 <br/> 类型：短整型 |
| `MaxVal` | `short` | get, set | 成就中的总步数<br/>类型: short |



---

<a id="eventachievementinfoloaded"></a>

## 🔌 EventAchievementInfoLoaded

事件 "achievement_info_loaded"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAchievementInfoLoaded\>`



---

<a id="eventachievementwritefailed"></a>

## 🔌 EventAchievementWriteFailed

事件 "achievement_write_failed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAchievementWriteFailed\>`



---

<a id="eventaddbullethitmarker"></a>

## 🔌 EventAddBulletHitMarker

事件 "添加子弹命中标记"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAddBulletHitMarker\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Bone` | `short` | get, set | type: short |
| `PosX` | `short` | get, set | type: short |
| `PosY` | `short` | get, set | type: short |
| `PosZ` | `short` | get, set | type: short |
| `AngX` | `short` | get, set | type: short |
| `AngY` | `short` | get, set | type: short |
| `AngZ` | `short` | get, set | type: short |
| `StartX` | `short` | get, set | type: short |
| `StartY` | `short` | get, set | type: short |
| `StartZ` | `short` | get, set | type: short |
| `Hit` | `bool` | get, set | 类型: bool |



---

<a id="eventaddplayersonaricon"></a>

## 🔌 EventAddPlayerSonarIcon

"添加玩家声纳图标"事件

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAddPlayerSonarIcon\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `PosX` | `float` | get, set | 类型：float |
| `PosY` | `float` | get, set | 类型：float |
| `PosZ` | `float` | get, set | 类型：float |



---

<a id="eventammopickup"></a>

## 🔌 EventAmmoPickup

事件 "ammo_pickup"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAmmoPickup\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Item` | `string` | get, set | 武器名称如 'tmp' 或 'hegrenade'，或物品名称如 'nvgs' <br/> 类型：字符串 |
| `Index` | `int` | get, set | 武器实体索引 <br/> 类型：长整型 |



---

<a id="eventammorefill"></a>

## 🔌 EventAmmoRefill

事件 "ammo_refill"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAmmoRefill\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Success` | `bool` | get, set | 类型: bool |



---

<a id="eventannouncephaseend"></a>

## 🔌 EventAnnouncePhaseEnd

事件 "announce_phase_end"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAnnouncePhaseEnd\>`



---

<a id="eventbeginnewmatch"></a>

## 🔌 EventBeginNewMatch

事件 "begin_new_match"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBeginNewMatch\>`



---

<a id="eventbombabortdefuse"></a>

## 🔌 EventBombAbortdefuse

事件 "bomb_abortdefuse"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombAbortdefuse\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 正在拆除炸弹的玩家<br/>类型：玩家控制器与角色 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 正在拆除炸弹的玩家<br/>类型：玩家控制器与角色 |
| `UserId` | `int` | get, set | 正在拆除炸弹的玩家<br/>类型：玩家控制器与角色 |



---

<a id="eventbombabortplant"></a>

## 🔌 EventBombAbortplant

事件 "bomb_abortplant"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombAbortplant\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 正在放置炸弹的玩家  
类型：player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 正在放置炸弹的玩家  
类型：player_controller_and_pawn |
| `UserId` | `int` | get, set | 正在放置炸弹的玩家  
类型：player_controller_and_pawn |
| `Site` | `short` | get, set | 炸弹点索引<br/> 类型: 短整型 |



---

<a id="eventbombbeep"></a>

## 🔌 EventBombBeep

事件 "bomb_beep"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombBeep\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntIndex` | `int` | get, set | C4 实体<br/> 类型: 长整型 |



---

<a id="eventbombbegindefuse"></a>

## 🔌 EventBombBegindefuse

事件 "bomb_begindefuse"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombBegindefuse\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 正在进行拆弹的玩家  
类型：玩家控制器及棋子 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 正在进行拆弹的玩家  
类型：玩家控制器及棋子 |
| `UserId` | `int` | get, set | 正在进行拆弹的玩家  
类型：玩家控制器及棋子 |
| `HasKit` | `bool` | get, set | 类型: bool |



---

<a id="eventbombbeginplant"></a>

## 🔌 EventBombBeginplant

事件 "bomb_beginplant"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombBeginplant\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 正在放置炸弹的玩家  
类型：player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 正在放置炸弹的玩家  
类型：player_controller_and_pawn |
| `UserId` | `int` | get, set | 正在放置炸弹的玩家  
类型：player_controller_and_pawn |
| `Site` | `short` | get, set | 炸弹点索引<br/> 类型: 短整型 |



---

<a id="eventbombdefused"></a>

## 🔌 EventBombDefused

事件 "炸弹拆除"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombDefused\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 拆弹的玩家 <br/> 类型：玩家控制器与棋子 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 拆弹的玩家 <br/> 类型：玩家控制器与棋子 |
| `UserId` | `int` | get, set | 拆弹的玩家 <br/> 类型：玩家控制器与棋子 |
| `Site` | `short` | get, set | 炸弹点索引<br/> 类型: 短整型 |



---

<a id="eventbombdropped"></a>

## 🔌 EventBombDropped

事件 "bomb_dropped"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombDropped\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 投掷炸弹的玩家 <br/> 类型：玩家控制器与玩家角色 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 投掷炸弹的玩家 <br/> 类型：玩家控制器与玩家角色 |
| `UserId` | `int` | get, set | 投掷炸弹的玩家 <br/> 类型：玩家控制器与玩家角色 |
| `EntIndex` | `int` | get, set | 类型：长整型 |



---

<a id="eventbombexploded"></a>

## 🔌 EventBombExploded

事件 "bomb_exploded"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombExploded\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 安装了炸弹的玩家<br/>类型: player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 安装了炸弹的玩家<br/>类型: player_controller_and_pawn |
| `UserId` | `int` | get, set | 安装了炸弹的玩家<br/>类型: player_controller_and_pawn |
| `Site` | `short` | get, set | 炸弹点索引<br/> 类型: 短整型 |



---

<a id="eventbombpickup"></a>

## 🔌 EventBombPickup

事件 "bomb_pickup"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombPickup\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 捡起炸弹的玩家棋子<br/> 类型: player_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 捡起炸弹的玩家棋子<br/> 类型: player_pawn |
| `UserId` | `int` | get, set | 捡起炸弹的玩家棋子<br/> 类型: player_pawn |



---

<a id="eventbombplanted"></a>

## 🔌 EventBombPlanted

Event "bomb_planted"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombPlanted\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 安装了炸弹的玩家<br/>类型: player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 安装了炸弹的玩家<br/>类型: player_controller_and_pawn |
| `UserId` | `int` | get, set | 安装了炸弹的玩家<br/>类型: player_controller_and_pawn |
| `Site` | `short` | get, set | 炸弹点索引<br/> 类型: 短整型 |



---

<a id="eventbonusupdated"></a>

## 🔌 EventBonusUpdated

事件 "bonus_updated"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBonusUpdated\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `NumAdvanced` | `short` | get, set | type: short |
| `NumBronze` | `short` | get, set | type: short |
| `NumSilver` | `short` | get, set | type: short |
| `NumGold` | `short` | get, set | type: short |



---

<a id="eventbottakeover"></a>

## 🔌 EventBotTakeover

事件 "bot_takeover"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBotTakeover\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `BotIDController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `BotIDPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `BotID` | `int` | get, set | 类型：玩家控制器 |
| `P` | `float` | get, set | 类型：float |
| `Y` | `float` | get, set | 类型：float |
| `R` | `float` | get, set | 类型：float |



---

<a id="eventbreakbreakable"></a>

## 🔌 EventBreakBreakable

事件“break_breakable”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBreakBreakable\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntIndex` | `int` | get, set | 类型：长整型 |
| `UserIdController` | `CCSPlayerController` | get | 类型: 玩家棋子 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型: 玩家棋子 |
| `UserId` | `int` | get, set | 类型: 玩家棋子 |
| `Material` | `byte` | get, set | 玻璃击碎、木头击碎等<br/>类型：byte |



---

<a id="eventbreakprop"></a>

## 🔌 EventBreakProp

事件 "break_prop"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBreakProp\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntIndex` | `int` | get, set | 类型：长整型 |
| `UserIdController` | `CCSPlayerController` | get | 类型: 玩家棋子 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型: 玩家棋子 |
| `UserId` | `int` | get, set | 类型: 玩家棋子 |
| `PlayerHeld` | `bool` | get, set | 类型: bool |
| `PlayerThrown` | `bool` | get, set | 类型: bool |
| `PlayerDropped` | `bool` | get, set | 类型: bool |



---

<a id="eventbrokenbreakable"></a>

## 🔌 EventBrokenBreakable

事件 "broken_breakable"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBrokenBreakable\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntIndex` | `int` | get, set | 类型：长整型 |
| `UserIdController` | `CCSPlayerController` | get | 类型: 玩家棋子 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型: 玩家棋子 |
| `UserId` | `int` | get, set | 类型: 玩家棋子 |
| `Material` | `byte` | get, set | 玻璃击碎、木头击碎等<br/>类型：byte |



---

<a id="eventbulletdamage"></a>

## 🔌 EventBulletDamage

事件 "bullet_damage"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBulletDamage\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `VictimController` | `CCSPlayerController` | get | 受伤的玩家索引 <br/> 类型: 玩家控制器与棋子 |
| `VictimPawn` | `CCSPlayerPawn` | get | 受伤的玩家索引 <br/> 类型: 玩家控制器与棋子 |
| `Victim` | `int` | get, set | 受伤的玩家索引 <br/> 类型: 玩家控制器与棋子 |
| `AttackerController` | `CCSPlayerController` | get | 攻击者的玩家索引<br/>类型: player_controller_and_pawn |
| `AttackerPawn` | `CCSPlayerPawn` | get | 攻击者的玩家索引<br/>类型: player_controller_and_pawn |
| `Attacker` | `int` | get, set | 攻击者的玩家索引<br/>类型: player_controller_and_pawn |
| `Distance` | `float` | get, set | 子弹击中玩家前的飞行距离  
类型：浮点数 |
| `DamageDirX` | `float` | get, set | 子弹的方向向量<br/>类型：浮点数 |
| `DamageDirY` | `float` | get, set | 子弹的方向向量<br/>类型：浮点数 |
| `DamageDirZ` | `float` | get, set | 子弹的方向向量<br/>类型：浮点数 |
| `NumPenetrations` | `byte` | get, set | 穿透了多少个表面 <br/> 类型: byte |
| `NoScope` | `bool` | get, set | 射手是否为盲狙？  
类型：布尔值 |
| `InAir` | `bool` | get, set | 射击者是否在跳跃？  
类型：布尔值 |
| `ShootAngX` | `float` | get, set | 射击角度 X <br/> 类型：浮点数 |
| `ShootAngY` | `float` | get, set | 射击角度 y <br/> 类型：浮点数 |
| `ShootAngZ` | `float` | get, set | 射击角度 Z <br/> 类型：浮点型 |
| `AimPunchX` | `float` | get, set | 瞄准抖动X <br/> 类型：浮点数 |
| `AimPunchY` | `float` | get, set | 瞄准抖动Y轴<br/>类型：浮点数 |
| `AimPunchZ` | `float` | get, set | 瞄准冲击Z <br/> 类型：浮点数 |
| `AttackTickCount` | `int` | get, set | 攻击刻 <br/> 类型：整数 |
| `AttackTickFrac` | `float` | get, set | 攻击系数  
类型：浮点数 |
| `RenderTickCount` | `int` | get, set | 渲染帧 <br/> 类型: 整型 |
| `RenderTickFrac` | `float` | get, set | 渲染碎片 <br/> 类型：浮点数 |
| `InaccuracyTotal` | `float` | get, set | 总不精确度 <br/> 类型：浮点数 |
| `InaccuracyMove` | `float` | get, set | 移动不精确度<br/> 类型：浮点数 |
| `InaccuracyAir` | `float` | get, set | 空中不精准度 <br/> 类型: 浮点数 |
| `RecoilIndex` | `float` | get, set | 后坐力索引。是的，这确实是一个浮点数。 <br/> 类型：浮点数 |
| `Type` | `int` | get, set | 延迟补偿类型<br/> 类型: 整数 |



---

<a id="eventbulletimpact"></a>

## 🔌 EventBulletImpact

事件 "bullet_impact"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBulletImpact\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `X` | `float` | get, set | 类型：float |
| `Y` | `float` | get, set | 类型：float |
| `Z` | `float` | get, set | 类型：float |



---

<a id="eventbuymenuclose"></a>

## 🔌 EventBuymenuClose

事件 "buymenu_close"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBuymenuClose\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |



---

<a id="eventbuymenuopen"></a>

## 🔌 EventBuymenuOpen

事件 "buymenu_open"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBuymenuOpen\>`



---

<a id="eventbuytimeended"></a>

## 🔌 EventBuytimeEnded

事件 "buytime_ended"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBuytimeEnded\>`



---

<a id="eventcartupdated"></a>

## 🔌 EventCartUpdated

事件 "cart_updated"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCartUpdated\>`



---

<a id="eventchoppersincomingwarning"></a>

## 🔌 EventChoppersIncomingWarning

事件 "choppers_incoming_warning"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventChoppersIncomingWarning\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Global` | `bool` | get, set | 类型: bool |



---

<a id="eventclientdisconnect"></a>

## 🔌 EventClientDisconnect

事件 "client_disconnect"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventClientDisconnect\>`



---

<a id="eventclientloadoutchanged"></a>

## 🔌 EventClientLoadoutChanged

事件 "client_loadout_changed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventClientLoadoutChanged\>`



---

<a id="eventclientsidelessonclosed"></a>

## 🔌 EventClientsideLessonClosed

事件 "clientside_lesson_closed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventClientsideLessonClosed\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `LessonName` | `string` | get, set | 类型: 字符串 |



---

<a id="eventclientsidereloadcustomecon"></a>

## 🔌 EventClientsideReloadCustomEcon

事件 "clientside_reload_custom_econ"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventClientsideReloadCustomEcon\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SteamID` | `string` | get, set | 类型: 字符串 |



---

<a id="eventcoregameevents"></a>

## 🔌 EventCoreGameEvents

事件 "核心游戏事件"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCoreGameEvents\>`



---

<a id="eventcsgamedisconnected"></a>

## 🔌 EventCsGameDisconnected

事件 "cs_game_disconnected"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCsGameDisconnected\>`



---

<a id="eventcsintermission"></a>

## 🔌 EventCsIntermission

事件 "cs_intermission"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCsIntermission\>`



---

<a id="eventcsmatchendrestart"></a>

## 🔌 EventCsMatchEndRestart

事件"cs_match_end_restart"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCsMatchEndRestart\>`



---

<a id="eventcsprerestart"></a>

## 🔌 EventCsPreRestart

事件 "cs_pre_restart"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCsPreRestart\>`



---

<a id="eventcsprevnextspectator"></a>

## 🔌 EventCsPrevNextSpectator

事件 "cs_prev_next_spectator"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCsPrevNextSpectator\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Next` | `bool` | get, set | 类型: bool |



---

<a id="eventcsroundfinalbeep"></a>

## 🔌 EventCsRoundFinalBeep

事件 "cs_round_final_beep"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCsRoundFinalBeep\>`



---

<a id="eventcsroundstartbeep"></a>

## 🔌 EventCsRoundStartBeep

事件“cs_round_start_beep”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCsRoundStartBeep\>`



---

<a id="eventcswinpanelmatch"></a>

## 🔌 EventCsWinPanelMatch

事件 "cs_win_panel_match"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCsWinPanelMatch\>`



---

<a id="eventcswinpanelround"></a>

## 🔌 EventCsWinPanelRound

事件 "cs_win_panel_round"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCsWinPanelRound\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ShowTimerDefend` | `bool` | get, set | 类型: bool |
| `ShowTimerAttack` | `bool` | get, set | 类型: bool |
| `TimerTime` | `short` | get, set | type: short |
| `FinalEvent` | `byte` | get, set | 在 cs_gamerules.h 中定义 <br/> 类型：字节 |
| `FunfactToken` | `string` | get, set | 类型: 字符串 |
| `FunfactPlayerController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `FunfactPlayerPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `FunfactPlayer` | `int` | get, set | 类型：玩家控制器 |
| `FunfactData1` | `int` | get, set | 类型：长整型 |
| `FunfactData2` | `int` | get, set | 类型：长整型 |
| `FunfactData3` | `int` | get, set | 类型：长整型 |



---

<a id="eventcstrikeevents"></a>

## 🔌 EventCstrikeevents

事件 "cstrikeevents"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCstrikeevents\>`



---

<a id="eventdecoydetonate"></a>

## 🔌 EventDecoyDetonate

decoy_detonate 事件

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDecoyDetonate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `EntityID` | `short` | get, set | type: short |
| `X` | `float` | get, set | 类型：float |
| `Y` | `float` | get, set | 类型：float |
| `Z` | `float` | get, set | 类型：float |



---

<a id="eventdecoyfiring"></a>

## 🔌 EventDecoyFiring

事件 "decoy_firing"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDecoyFiring\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `EntityID` | `short` | get, set | type: short |
| `X` | `float` | get, set | 类型：float |
| `Y` | `float` | get, set | 类型：float |
| `Z` | `float` | get, set | 类型：float |



---

<a id="eventdecoystarted"></a>

## 🔌 EventDecoyStarted

事件 "诱饵弹已部署"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDecoyStarted\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型: 玩家棋子 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型: 玩家棋子 |
| `UserId` | `int` | get, set | 类型: 玩家棋子 |
| `EntityID` | `short` | get, set | type: short |
| `X` | `float` | get, set | 类型：float |
| `Y` | `float` | get, set | 类型：float |
| `Z` | `float` | get, set | 类型：float |



---

<a id="eventdefuserdropped"></a>

## 🔌 EventDefuserDropped

事件 "defuser_dropped"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDefuserDropped\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityID` | `int` | get, set | defuser 的实体 ID<br/>类型：长整型 |



---

<a id="eventdefuserpickup"></a>

## 🔌 EventDefuserPickup

事件 "拆弹器拾取"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDefuserPickup\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityID` | `int` | get, set | defuser 的实体 ID<br/>类型：长整型 |
| `UserIdController` | `CCSPlayerController` | get | 拾取拆弹器的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 拾取拆弹器的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 拾取拆弹器的玩家 <br/> 类型：玩家控制器与Pawn |



---

<a id="eventdemoskip"></a>

## 🔌 EventDemoSkip

事件 "demo_skip"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDemoSkip\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlaybackTick` | `int` | get, set | 当前回放帧<br/> 类型：长整型 |
| `SkiptoTick` | `int` | get, set | 当前游戏刻<br/>类型：长整型 |



---

<a id="eventdemostart"></a>

## 🔌 EventDemoStart

事件 "demo_start"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDemoStart\>`



---

<a id="eventdemostop"></a>

## 🔌 EventDemoStop

事件 "demo_stop"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDemoStop\>`



---

<a id="eventdifficultychanged"></a>

## 🔌 EventDifficultyChanged

事件 "difficulty_changed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDifficultyChanged\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `NewDifficulty` | `short` | get, set | type: short |
| `OldDifficulty` | `short` | get, set | type: short |
| `StrDifficulty` | `string` | get, set | 新的难度（字符串形式）  
类型：字符串 |



---

<a id="eventdmbonusweaponstart"></a>

## 🔌 EventDmBonusWeaponStart

事件 "dm_bonus_weapon_start"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDmBonusWeaponStart\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Time` | `short` | get, set | 此加成持续的时长 <br/> 类型: short |
| `Pos` | `short` | get, set | 奖励武器的装载位置<br/> 类型：short |



---

<a id="eventdoorbreak"></a>

## 🔌 EventDoorBreak

事件 "door_break"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDoorBreak\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntIndex` | `int` | get, set | 类型：长整型 |
| `DMgState` | `int` | get, set | 类型：长整型 |



---

<a id="eventdoorclose"></a>

## 🔌 EventDoorClose

Event "door_close"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDoorClose\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 谁关闭了门 <br/> 类型: 玩家棋子 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 谁关闭了门 <br/> 类型: 玩家棋子 |
| `UserId` | `int` | get, set | 谁关闭了门 <br/> 类型: 玩家棋子 |
| `Checkpoint` | `bool` | get, set | 门是否为检查点门<br/> 类型：布尔 |



---

<a id="eventdoorclosed"></a>

## 🔌 EventDoorClosed

事件 "door_closed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDoorClosed\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 谁关闭了门 <br/> 类型: 玩家棋子 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 谁关闭了门 <br/> 类型: 玩家棋子 |
| `UserId` | `int` | get, set | 谁关闭了门 <br/> 类型: 玩家棋子 |
| `EntIndex` | `int` | get, set | 类型：长整型 |



---

<a id="eventdoormoving"></a>

## 🔌 EventDoorMoving

事件 "door_moving"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDoorMoving\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `EntIndex` | `int` | get, set | 类型：长整型 |



---

<a id="eventdooropen"></a>

## 🔌 EventDoorOpen

事件 "door_open"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDoorOpen\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 谁关闭了门 <br/> 类型: 玩家棋子 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 谁关闭了门 <br/> 类型: 玩家棋子 |
| `UserId` | `int` | get, set | 谁关闭了门 <br/> 类型: 玩家棋子 |
| `EntIndex` | `int` | get, set | 类型：长整型 |



---

<a id="eventdroneaboveroof"></a>

## 🔌 EventDroneAboveRoof

事件 "drone_above_roof"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDroneAboveRoof\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Cargo` | `short` | get, set | type: short |



---

<a id="eventdronecargodetached"></a>

## 🔌 EventDroneCargoDetached

事件 "drone_cargo_detached"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDroneCargoDetached\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Cargo` | `short` | get, set | type: short |
| `Delivered` | `bool` | get, set | 类型: bool |



---

<a id="eventdronedispatched"></a>

## 🔌 EventDroneDispatched

事件 "drone_dispatched"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDroneDispatched\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Priority` | `short` | get, set | type: short |
| `DroneDispatched` | `short` | get, set | type: short |



---

<a id="eventdronegunattack"></a>

## 🔌 EventDronegunAttack

事件 "dronegun_attack"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDronegunAttack\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |



---

<a id="eventdropratemodified"></a>

## 🔌 EventDropRateModified

事件 "drop_rate_modified"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDropRateModified\>`



---

<a id="eventdynamicshadowlightchanged"></a>

## 🔌 EventDynamicShadowLightChanged

事件 "dynamic_shadow_light_changed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDynamicShadowLightChanged\>`



---

<a id="eventdziteminteraction"></a>

## 🔌 EventDzItemInteraction

事件 "dz_item_interaction"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDzItemInteraction\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 玩家实体索引<br/>类型: 玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 玩家实体索引<br/>类型: 玩家控制器 |
| `UserId` | `int` | get, set | 玩家实体索引<br/>类型: 玩家控制器 |
| `Subject` | `short` | get, set | crate entindex <br/> 类型: short |
| `Type` | `string` | get, set | 板条箱类型（金属、木质或空投）<br/> 类型：字符串 |



---

<a id="eventenablerestartvoting"></a>

## 🔌 EventEnableRestartVoting

事件 "enable_restart_voting"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventEnableRestartVoting\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Enable` | `bool` | get, set | 类型: bool |



---

<a id="eventendmatchcmmstartrevealitems"></a>

## 🔌 EventEndmatchCmmStartRevealItems

事件 "endmatch_cmm_start_reveal_items"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventEndmatchCmmStartRevealItems\>`



---

<a id="eventendmatchmapvoteselectingmap"></a>

## 🔌 EventEndmatchMapvoteSelectingMap

事件 "endmatch_mapvote_selecting_map"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventEndmatchMapvoteSelectingMap\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Count` | `byte` | get, set | 平局数 <br/> 类型：字节 |
| `Slot1` | `byte` | get, set | 类型: 字节 |
| `Slot2` | `byte` | get, set | 类型: 字节 |
| `Slot3` | `byte` | get, set | 类型: 字节 |
| `Slot4` | `byte` | get, set | 类型: 字节 |
| `Slot5` | `byte` | get, set | 类型: 字节 |
| `Slot6` | `byte` | get, set | 类型: 字节 |
| `Slot7` | `byte` | get, set | 类型: 字节 |
| `Slot8` | `byte` | get, set | 类型: 字节 |
| `Slot9` | `byte` | get, set | 类型: 字节 |
| `Slot10` | `byte` | get, set | 类型: 字节 |



---

<a id="evententerbombzone"></a>

## 🔌 EventEnterBombzone

事件 "enter_bombzone"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventEnterBombzone\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `HasBomb` | `bool` | get, set | 类型: bool |
| `IsPlanted` | `bool` | get, set | 类型: bool |



---

<a id="evententerbuyzone"></a>

## 🔌 EventEnterBuyzone

Event "enter_buyzone"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventEnterBuyzone\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `CanBuy` | `bool` | get, set | 类型: bool |



---

<a id="evententerrescuezone"></a>

## 🔌 EventEnterRescueZone

事件 "进入救援区域"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventEnterRescueZone\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |



---

<a id="evententitykilled"></a>

## 🔌 EventEntityKilled

事件 "entity_killed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventEntityKilled\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntindexKilled` | `int` | get, set | 类型：长整型 |
| `EntindexAttacker` | `int` | get, set | 类型：长整型 |
| `EntindexInflictor` | `int` | get, set | 类型：长整型 |
| `DamageBits` | `int` | get, set | 类型：长整型 |



---

<a id="evententityvisible"></a>

## 🔌 EventEntityVisible

Event "entity_visible"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventEntityVisible\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 观察到实体的玩家 <br/> 类型: player_controller |
| `UserIdPawn` | `CCSPlayerPawn` | get | 观察到实体的玩家 <br/> 类型: player_controller |
| `UserId` | `int` | get, set | 观察到实体的玩家 <br/> 类型: player_controller |
| `Subject` | `int` | get, set | 他们看到的实体的Entindex <br/> 类型：long |
| `ClassName` | `string` | get, set | 他们看到的实体类名<br/>类型：字符串 |
| `EntityName` | `string` | get, set | 实体名称（他们所见）<br/>类型：字符串 |



---

<a id="eventeventticketmodified"></a>

## 🔌 EventEventTicketModified

事件 "event_ticket_modified"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventEventTicketModified\>`



---

<a id="eventexitbombzone"></a>

## 🔌 EventExitBombzone

事件 "exit_bombzone"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventExitBombzone\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `HasBomb` | `bool` | get, set | 类型: bool |
| `IsPlanted` | `bool` | get, set | 类型: bool |



---

<a id="eventexitbuyzone"></a>

## 🔌 EventExitBuyzone

事件 "exit_buyzone"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventExitBuyzone\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `CanBuy` | `bool` | get, set | 类型: bool |



---

<a id="eventexitrescuezone"></a>

## 🔌 EventExitRescueZone

Event "exit_rescue_zone"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventExitRescueZone\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |



---

<a id="eventfinalestart"></a>

## 🔌 EventFinaleStart

事件 "finale_start"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventFinaleStart\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Rushes` | `short` | get, set | type: short |



---

<a id="eventfirstbombsincomingwarning"></a>

## 🔌 EventFirstbombsIncomingWarning

事件 "firstbombs_incoming_warning"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventFirstbombsIncomingWarning\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Global` | `bool` | get, set | 类型: bool |



---

<a id="eventflareignitenpc"></a>

## 🔌 EventFlareIgniteNpc

事件 "flare_ignite_npc"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventFlareIgniteNpc\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntIndex` | `int` | get, set | 实体点燃  
类型：长整型 |



---

<a id="eventflashbangdetonate"></a>

## 🔌 EventFlashbangDetonate

事件 "flashbang_detonate"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventFlashbangDetonate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `EntityID` | `short` | get, set | type: short |
| `X` | `float` | get, set | 类型：float |
| `Y` | `float` | get, set | 类型：float |
| `Z` | `float` | get, set | 类型：float |



---

<a id="eventgameend"></a>

## 🔌 EventGameEnd

Event "game_end" 一场游戏结束

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGameEnd\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Winner` | `byte` | get, set | 胜者队伍/用户ID <br/> 类型：字节 |



---

<a id="eventgameinit"></a>

## 🔌 EventGameInit

事件 "game_init" 在新游戏开始时发送

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGameInit\>`



---

<a id="eventgamemessage"></a>

## 🔌 EventGameMessage

事件 "game_message"：游戏逻辑向所有玩家发送的消息

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGameMessage\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Target` | `byte` | get, set | 0 = 控制台, 1 = 抬头显示器 <br/> 类型: 字节 |
| `Text` | `string` | get, set | 消息文本 <br/> 类型：字符串 |



---

<a id="eventgamenewmap"></a>

## 🔌 EventGameNewmap

事件 "game_newmap" 在新地图完全加载时发送

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGameNewmap\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MapName` | `string` | get, set | 地图名称<br/>类型：字符串 |
| `Transition` | `bool` | get, set | 如果这是从一个地图到另一个地图的过渡，则为 true <br/> 类型：布尔 |



---

<a id="eventgamephasechanged"></a>

## 🔌 EventGamePhaseChanged

事件 "game_phase_changed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGamePhaseChanged\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `NewPhase` | `short` | get, set | type: short |



---

<a id="eventgamestart"></a>

## 🔌 EventGameStart

事件 "game_start" 一个新游戏开始

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGameStart\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `RoundsLimit` | `int` | get, set | 最大回合数<br/>类型：长整型 |
| `TimeLimit` | `int` | get, set | 时间限制 <br/> 类型: long |
| `FragLimit` | `int` | get, set | frag 限制  
类型：long |
| `Objective` | `string` | get, set | 回合目标 <br/> 类型: 字符串 |



---

<a id="eventgameevents"></a>

## 🔌 EventGameevents

事件 "gameevents"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGameevents\>`



---

<a id="eventgameinstructordraw"></a>

## 🔌 EventGameinstructorDraw

事件 "gameinstructor_draw"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGameinstructorDraw\>`



---

<a id="eventgameinstructornodraw"></a>

## 🔌 EventGameinstructorNodraw

事件 "gameinstructor_nodraw"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGameinstructorNodraw\>`



---

<a id="eventgameuihidden"></a>

## 🔌 EventGameuiHidden

事件 "gameui_hidden"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGameuiHidden\>`



---

<a id="eventgcconnected"></a>

## 🔌 EventGcConnected

事件 "gc_connected"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGcConnected\>`



---

<a id="eventggkilledenemy"></a>

## 🔌 EventGgKilledEnemy

事件 "gg_killed_enemy"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGgKilledEnemy\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `VictimIDController` | `CCSPlayerController` | get | 死亡用户的ID <br/> 类型: player_controller |
| `VictimIDPawn` | `CCSPlayerPawn` | get | 死亡用户的ID <br/> 类型: player_controller |
| `VictimID` | `int` | get, set | 死亡用户的ID <br/> 类型: player_controller |
| `AttackerIDController` | `CCSPlayerController` | get | 杀死该用户的ID <br/> 类型: player_controller |
| `AttackerIDPawn` | `CCSPlayerPawn` | get | 杀死该用户的ID <br/> 类型: player_controller |
| `AttackerID` | `int` | get, set | 杀死该用户的ID <br/> 类型: player_controller |
| `Dominated` | `short` | get, set | 杀手是否以此击杀压制了受害者 <br/> 类型: short |
| `Revenge` | `short` | get, set | 杀手是否借助此次击杀成功复仇受害者  
类型：短整型 |
| `Bonus` | `bool` | get, set | 杀手是否使用奖励武器击杀？<br/> 类型：布尔 |



---

<a id="eventgrenadebounce"></a>

## 🔌 EventGrenadeBounce

事件 "grenade_bounce"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGrenadeBounce\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |



---

<a id="eventgrenadethrown"></a>

## 🔌 EventGrenadeThrown

"手雷投掷"事件

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGrenadeThrown\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `Weapon` | `string` | get, set | 武器名称<br/>类型：字符串 |



---

<a id="eventguardianwaverestart"></a>

## 🔌 EventGuardianWaveRestart

事件 "guardian_wave_restart"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGuardianWaveRestart\>`



---

<a id="eventhegrenadedetonate"></a>

## 🔌 EventHegrenadeDetonate

Event "hegrenade_detonate"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHegrenadeDetonate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `EntityID` | `short` | get, set | type: short |
| `X` | `float` | get, set | 类型：float |
| `Y` | `float` | get, set | 类型：float |
| `Z` | `float` | get, set | 类型：float |



---

<a id="eventhelicoptergrenadepuntmiss"></a>

## 🔌 EventHelicopterGrenadePuntMiss

事件 "helicopter_grenade_punt_miss"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHelicopterGrenadePuntMiss\>`



---

<a id="eventhidedeathpanel"></a>

## 🔌 EventHideDeathpanel

事件 "hide_deathpanel"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHideDeathpanel\>`



---

<a id="eventhltvcameraman"></a>

## 🔌 EventHltvCameraman

事件 "hltv_cameraman" 一名观察者/玩家成为摄像师

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvCameraman\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 相机操作者实体索引<br/>类型: 玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 相机操作者实体索引<br/>类型: 玩家控制器 |
| `UserId` | `int` | get, set | 相机操作者实体索引<br/>类型: 玩家控制器 |



---

<a id="eventhltvchangedmode"></a>

## 🔌 EventHltvChangedMode

事件 "hltv_changed_mode"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvChangedMode\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `OldMode` | `int` | get, set | 类型：长整型 |
| `NewMode` | `int` | get, set | 类型：长整型 |
| `ObsTarget` | `int` | get, set | 类型：长整型 |



---

<a id="eventhltvchase"></a>

## 🔌 EventHltvChase

事件 "hltv_chase" 针对单个实体的镜头

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvChase\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Target1Controller` | `CCSPlayerController` | get | 主要目标索引<br/>类型：玩家控制器 |
| `Target1Pawn` | `CCSPlayerPawn` | get | 主要目标索引<br/>类型：玩家控制器 |
| `Target1` | `int` | get, set | 主要目标索引<br/>类型：玩家控制器 |
| `Target2Controller` | `CCSPlayerController` | get | 次要目标索引或0 <br/> 类型: player_controller |
| `Target2Pawn` | `CCSPlayerPawn` | get | 次要目标索引或0 <br/> 类型: player_controller |
| `Target2` | `int` | get, set | 次要目标索引或0 <br/> 类型: player_controller |
| `Distance` | `short` | get, set | 摄像机距离 <br/> 类型：短整型 |
| `Theta` | `short` | get, set | 视角水平角 <br/> 类型：短整型 |
| `Phi` | `short` | get, set | 视角垂直角度<br/> 类型：短整型 |
| `Inertia` | `byte` | get, set | 相机惯性 <br/> 类型：字节 |
| `InEye` | `byte` | get, set | 导演建议在游戏中显示 <br/> 类型: 字节 |



---

<a id="eventhltvchat"></a>

## 🔌 EventHltvChat

事件 "hltv_chat" 观众发送的HLTV聊天消息

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvChat\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Text` | `string` | get, set | 类型: 字符串 |
| `SteamID` | `ulong` | get, set | steam ID <br/> 类型：uint64 |



---

<a id="eventhltvfixed"></a>

## 🔌 EventHltvFixed

事件 "hltv_fixed" 从固定视角展示

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvFixed\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PosX` | `int` | get, set | 摄像机在世界空间中的位置 <br/> 类型：长整型 |
| `Posy` | `int` | get, set | 类型：长整型 |
| `PosZ` | `int` | get, set | 类型：长整型 |
| `Theta` | `short` | get, set | 摄像机角度 <br/> 类型: short |
| `Phi` | `short` | get, set | type: short |
| `Offset` | `short` | get, set | type: short |
| `FOv` | `float` | get, set | 类型：float |
| `TargetController` | `CCSPlayerController` | get | 跟随此玩家<br/>类型：玩家控制器 |
| `TargetPawn` | `CCSPlayerPawn` | get | 跟随此玩家<br/>类型：玩家控制器 |
| `Target` | `int` | get, set | 跟随此玩家<br/>类型：玩家控制器 |



---

<a id="eventhltvmessage"></a>

## 🔌 EventHltvMessage

事件 "hltv_message" 由管理员发送的HLTV消息

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvMessage\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Text` | `string` | get, set | 类型: 字符串 |



---

<a id="eventhltvrankcamera"></a>

## 🔌 EventHltvRankCamera

事件 "hltv_rank_camera" 摄像机排名

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvRankCamera\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Index` | `byte` | get, set | 固定摄像机索引<br/>类型：字节 |
| `Rank` | `float` | get, set | 排名，此摄像机视角的趣味性<br/> 类型：浮点数 |
| `TargetController` | `CCSPlayerController` | get | 最佳/最近的目标实体<br/>类型: player_controller |
| `TargetPawn` | `CCSPlayerPawn` | get | 最佳/最近的目标实体<br/>类型: player_controller |
| `Target` | `int` | get, set | 最佳/最近的目标实体<br/>类型: player_controller |



---

<a id="eventhltvrankentity"></a>

## 🔌 EventHltvRankEntity

事件 "hltv_rank_entity" 实体排名

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvRankEntity\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 玩家槽位<br/>类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 玩家槽位<br/>类型：玩家控制器 |
| `UserId` | `int` | get, set | 玩家槽位<br/>类型：玩家控制器 |
| `Rank` | `float` | get, set | 排名，此实体观看的有趣程度  
类型：浮点数 |
| `TargetController` | `CCSPlayerController` | get | 最佳/最近的目标实体<br/>类型: player_controller |
| `TargetPawn` | `CCSPlayerPawn` | get | 最佳/最近的目标实体<br/>类型: player_controller |
| `Target` | `int` | get, set | 最佳/最近的目标实体<br/>类型: player_controller |



---

<a id="eventhltvreplay"></a>

## 🔌 EventHltvReplay

事件"hltv_replay"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvReplay\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Delay` | `int` | get, set | 杀手回放延迟的秒数<br/> 类型: 长整型 |
| `Reason` | `int` | get, set | 回放原因 (ReplayEventType_t) <br/> 类型: long |



---

<a id="eventhltvreplaystatus"></a>

## 🔌 EventHltvReplayStatus

事件 "hltv_replay_status"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvReplayStatus\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Reason` | `int` | get, set | hltv 回放状态变更原因 () <br/> 类型: long |



---

<a id="eventhltvstatus"></a>

## 🔌 EventHltvStatus

事件 "hltv_status" 常规HLTV状态

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvStatus\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Clients` | `int` | get, set | HLTV观众数量 <br/> 类型: long |
| `Slots` | `int` | get, set | HLTV 观众位数量<br/> 类型：长整型 |
| `Proxies` | `short` | get, set | HLTV代理数量 <br/> 类型：短整型 |
| `Master` | `string` | get, set | 调度主服务器IP:端口  
类型：字符串 |



---

<a id="eventhltvtitle"></a>

## 🔌 EventHltvTitle

事件 "hltv_title"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvTitle\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Text` | `string` | get, set | 类型: 字符串 |



---

<a id="eventhltvversioninfo"></a>

## 🔌 EventHltvVersioninfo

事件 "hltv_versioninfo"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvVersioninfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Version` | `int` | get, set | 类型：长整型 |



---

<a id="eventhostagecallforhelp"></a>

## 🔌 EventHostageCallForHelp

事件“人质呼救”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHostageCallForHelp\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Hostage` | `short` | get, set | 人质实体索引<br/>类型：short |



---

<a id="eventhostagefollows"></a>

## 🔌 EventHostageFollows

事件 "hostage_follows"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHostageFollows\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 触碰人质的玩家<br/>类型: 玩家控制器与角色实体 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 触碰人质的玩家<br/>类型: 玩家控制器与角色实体 |
| `UserId` | `int` | get, set | 触碰人质的玩家<br/>类型: 玩家控制器与角色实体 |
| `Hostage` | `short` | get, set | 人质实体索引<br/>类型：short |



---

<a id="eventhostagehurt"></a>

## 🔌 EventHostageHurt

事件 "人质受伤"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHostageHurt\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 伤害人质的玩家 <br/> 类型: 玩家控制器与角色 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 伤害人质的玩家 <br/> 类型: 玩家控制器与角色 |
| `UserId` | `int` | get, set | 伤害人质的玩家 <br/> 类型: 玩家控制器与角色 |
| `Hostage` | `short` | get, set | 人质实体索引<br/>类型：short |



---

<a id="eventhostagekilled"></a>

## 🔌 EventHostageKilled

事件 "hostage_killed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHostageKilled\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 击杀过人质的玩家  
类型：玩家控制器与角色 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 击杀过人质的玩家  
类型：玩家控制器与角色 |
| `UserId` | `int` | get, set | 击杀过人质的玩家  
类型：玩家控制器与角色 |
| `Hostage` | `short` | get, set | 人质实体索引<br/>类型：short |



---

<a id="eventhostagerescued"></a>

## 🔌 EventHostageRescued

事件 "人质被解救"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHostageRescued\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 解救人质的人质 <br/> 类型：玩家控制器与棋子 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 解救人质的人质 <br/> 类型：玩家控制器与棋子 |
| `UserId` | `int` | get, set | 解救人质的人质 <br/> 类型：玩家控制器与棋子 |
| `Hostage` | `short` | get, set | 人质实体索引<br/>类型：short |
| `Site` | `short` | get, set | 救援点索引<br/>类型: short |



---

<a id="eventhostagerescuedall"></a>

## 🔌 EventHostageRescuedAll

Event "hostage_rescued_all"  

翻译：事件 "所有人质获救"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHostageRescuedAll\>`



---

<a id="eventhostagestopsfollowing"></a>

## 🔌 EventHostageStopsFollowing

事件 "人质停止跟随"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHostageStopsFollowing\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 解救人质的人质 <br/> 类型：玩家控制器与棋子 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 解救人质的人质 <br/> 类型：玩家控制器与棋子 |
| `UserId` | `int` | get, set | 解救人质的人质 <br/> 类型：玩家控制器与棋子 |
| `Hostage` | `short` | get, set | 人质实体索引<br/>类型：short |



---

<a id="eventhostnamechanged"></a>

## 🔌 EventHostnameChanged

事件 "hostname_changed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHostnameChanged\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Hostname` | `string` | get, set | 类型: 字符串 |



---

<a id="eventinfernoexpire"></a>

## 🔌 EventInfernoExpire

事件 "inferno_expire"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventInfernoExpire\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityID` | `short` | get, set | type: short |
| `X` | `float` | get, set | 类型：float |
| `Y` | `float` | get, set | 类型：float |
| `Z` | `float` | get, set | 类型：float |



---

<a id="eventinfernoextinguish"></a>

## 🔌 EventInfernoExtinguish

事件 "inferno_extinguish"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventInfernoExtinguish\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityID` | `short` | get, set | type: short |
| `X` | `float` | get, set | 类型：float |
| `Y` | `float` | get, set | 类型：float |
| `Z` | `float` | get, set | 类型：float |



---

<a id="eventinfernostartburn"></a>

## 🔌 EventInfernoStartburn

事件 "inferno_startburn"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventInfernoStartburn\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityID` | `short` | get, set | type: short |
| `X` | `float` | get, set | 类型：float |
| `Y` | `float` | get, set | 类型：float |
| `Z` | `float` | get, set | 类型：float |



---

<a id="eventinspectweapon"></a>

## 🔌 EventInspectWeapon

事件 "inspect_weapon"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventInspectWeapon\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |



---

<a id="eventinstructorcloselesson"></a>

## 🔌 EventInstructorCloseLesson

事件 "instructor_close_lesson"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventInstructorCloseLesson\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 该课程针对的玩家 <br/> 类型: player_controller |
| `UserIdPawn` | `CCSPlayerPawn` | get | 该课程针对的玩家 <br/> 类型: player_controller |
| `UserId` | `int` | get, set | 该课程针对的玩家 <br/> 类型: player_controller |
| `HintName` | `string` | get, set | 要开始的课程名称。必须与 instructor_lesson.txt 匹配 <br/> 类型：字符串 |



---

<a id="eventinstructorserverhintcreate"></a>

## 🔌 EventInstructorServerHintCreate

事件 "instructor_server_hint_create" 使用完全由服务器/地图提供的数据创建提示。旨在在内容准备就绪前，为平滑测试过程提供提示，且无需额外操作。**不适用于作为发布版本的临时补丁**。

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventInstructorServerHintCreate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 触发提示的玩家用户ID <br/> 类型: player_controller |
| `UserIdPawn` | `CCSPlayerPawn` | get | 触发提示的玩家用户ID <br/> 类型: player_controller |
| `UserId` | `int` | get, set | 触发提示的玩家用户ID <br/> 类型: player_controller |
| `HintEntindex` | `int` | get, set | 触发事件的环境指导提示的实体ID <br/> 类型: long |
| `HintName` | `string` | get, set | 提示的命名，用于后续引用（例如，为提示设置击杀命令而非超时）<br/> 类型：字符串 |
| `HintReplaceKey` | `string` | get, set | 类型名称，使相同类型的消息相互替换 <br/> 类型：字符串 |
| `HintTarget` | `int` | get, set | 提示应显示于的实体ID<br/>类型：长整型 |
| `HintActivatorUseridController` | `CCSPlayerController` | get | 激活者的玩家槽位 <br/> 类型: player_controller |
| `HintActivatorUseridPawn` | `CCSPlayerPawn` | get | 激活者的玩家槽位 <br/> 类型: player_controller |
| `HintActivatorUserid` | `int` | get, set | 激活者的玩家槽位 <br/> 类型: player_controller |
| `HintTimeout` | `short` | get, set | 提示自动超时的时间（秒），0 = 永不超时 <br/> 类型：short |
| `HintIconOnscreen` | `string` | get, set | 提示图标，用于提示在屏幕上显示时。例如："icon_alert_red"<br/>类型：字符串 |
| `HintIconOffscreen` | `string` | get, set | 当提示位于屏幕外时使用的提示图标，例如 "icon_alert" <br/> 类型：字符串 |
| `HintCaption` | `string` | get, set | 提示文本。例如："#ThisIsDangerous" <br/> 类型：字符串 |
| `HintActivatorCaption` | `string` | get, set | 仅激活者可见的提示标题，例如 "#YouPushedItGood" <br/> 类型: 字符串 |
| `HintColor` | `string` | get, set | 提示颜色，格式为"r,g,b"，每个分量取值范围0-255 <br/> 类型: string |
| `HintIconOffset` | `float` | get, set | 在Z轴上将提示从实体原点偏移的距离 <br/> 类型：浮点数 |
| `HintRange` | `float` | get, set | 提示被剔除前的范围<br/> 类型：浮点数 |
| `HintFlags` | `int` | get, set | 提示标志<br/>类型: long |
| `HintBinding` | `string` | get, set | 当 use_binding 为屏幕图标时使用的绑定<br/> 类型：字符串 |
| `HintAllowNodrawTarget` | `bool` | get, set | 若设为 false，目标实体不可见时提示将消失 <br/> 类型：布尔值 |
| `HintNooffscreen` | `bool` | get, set | 若为真，玩家视野外将不显示提示 <br/> 类型: 布尔值 |
| `HintForcecaption` | `bool` | get, set | 如果为真，即使提示被遮挡，提示标题也会显示 <br/> 类型：bool |
| `HintLocalPlayerOnly` | `bool` | get, set | 如果为真，只有本地玩家会看到提示<br/> 类型：布尔值 |
| `HintStartSound` | `string` | get, set | 游戏音效播放 <br/> 类型：字符串 |
| `HintLayoutfile` | `string` | get, set | Panorama 布局文件的路径<br/>类型：字符串 |
| `HintVrPanelType` | `short` | get, set | 全景面板的附件类型<br/>类型：短整型 |
| `HintVrHeightOffset` | `float` | get, set | 附着面板的高度偏移 <br/> 类型：浮点数 |
| `HintVrOffsetX` | `float` | get, set | 附加面板的偏移量 <br/> 类型：浮点数 |
| `HintVrOffsetY` | `float` | get, set | 附加面板的偏移量 <br/> 类型：浮点数 |
| `HintVrOffsetZ` | `float` | get, set | 附加面板的偏移量 <br/> 类型：浮点数 |
| `HintGamepadBinding` | `string` | get, set | 游戏绑定时使用的游戏手柄绑定，当use_binding为屏幕图标时<br/> 类型: string |



---

<a id="eventinstructorserverhintstop"></a>

## 🔌 EventInstructorServerHintStop

Event "instructor_server_hint_stop" 销毁服务器/地图创建的提示

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventInstructorServerHintStop\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `HintName` | `string` | get, set | 停止提示。将停止所有具有此名称的提示<br/> 类型：字符串 |
| `HintEntindex` | `int` | get, set | 触发事件的环境指导提示的实体ID <br/> 类型: long |



---

<a id="eventinstructorstartlesson"></a>

## 🔌 EventInstructorStartLesson

事件 "instructor_start_lesson"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventInstructorStartLesson\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 该课程针对的玩家 <br/> 类型: player_controller |
| `UserIdPawn` | `CCSPlayerPawn` | get | 该课程针对的玩家 <br/> 类型: player_controller |
| `UserId` | `int` | get, set | 该课程针对的玩家 <br/> 类型: player_controller |
| `HintName` | `string` | get, set | 要开始的课程名称。必须与 instructor_lesson.txt 匹配 <br/> 类型：字符串 |
| `HintTarget` | `int` | get, set | 提示信息应显示在的实体ID。如果为控制器目标则留空<br/>类型：long |
| `VrMovementType` | `byte` | get, set | 类型: 字节 |
| `VrSingleController` | `bool` | get, set | 类型: bool |
| `VrControllerType` | `byte` | get, set | 类型: 字节 |



---

<a id="eventinventoryupdated"></a>

## 🔌 EventInventoryUpdated

事件 "inventory_updated"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventInventoryUpdated\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ItemDef` | `short` | get, set | type: short |
| `Itemid` | `int` | get, set | 类型：长整型 |



---

<a id="eventitemequip"></a>

## 🔌 EventItemEquip

事件 "item_equip"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventItemEquip\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Item` | `string` | get, set | 武器名称如 'tmp' 或 'hegrenade'，或物品名称如 'nvgs' <br/> 类型：字符串 |
| `DefIndex` | `int` | get, set | 类型：长整型 |
| `CanZoom` | `bool` | get, set | 类型: bool |
| `HasSilencer` | `bool` | get, set | 类型: bool |
| `IsSilenced` | `bool` | get, set | 类型: bool |
| `HasTracers` | `bool` | get, set | 类型: bool |
| `WepType` | `short` | get, set | type: short |
| `IsPainted` | `bool` | get, set | 类型: bool |



---

<a id="eventitempickup"></a>

## 🔌 EventItemPickup

事件 "item_pickup"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventItemPickup\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Item` | `string` | get, set | 武器名称如 'tmp' 或 'hegrenade'，或物品名称如 'nvgs' <br/> 类型：字符串 |
| `Silent` | `bool` | get, set | 类型: bool |
| `DefIndex` | `int` | get, set | 类型：长整型 |



---

<a id="eventitempickupfailed"></a>

## 🔌 EventItemPickupFailed

事件 "item_pickup_failed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventItemPickupFailed\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Item` | `string` | get, set | 类型: 字符串 |
| `Reason` | `short` | get, set | type: short |
| `Limit` | `short` | get, set | type: short |



---

<a id="eventitempickupslerp"></a>

## 🔌 EventItemPickupSlerp

事件 "item_pickup_slerp"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventItemPickupSlerp\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Index` | `short` | get, set | type: short |
| `Behavior` | `short` | get, set | type: short |



---

<a id="eventitempurchase"></a>

## 🔌 EventItemPurchase

事件 "item_purchase"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventItemPurchase\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Team` | `short` | get, set | type: short |
| `LoadOut` | `short` | get, set | type: short |
| `Weapon` | `string` | get, set | 类型: 字符串 |



---

<a id="eventitemremove"></a>

## 🔌 EventItemRemove

事件 "item_remove"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventItemRemove\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Item` | `string` | get, set | 武器名称如 'tmp' 或 'hegrenade'，或物品名称如 'nvgs' <br/> 类型：字符串 |
| `DefIndex` | `int` | get, set | 类型：长整型 |



---

<a id="eventitemschemainitialized"></a>

## 🔌 EventItemSchemaInitialized

事件 "item_schema_initialized"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventItemSchemaInitialized\>`



---

<a id="eventjointeamfailed"></a>

## 🔌 EventJointeamFailed

事件 "jointeam_failed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventJointeamFailed\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Reason` | `byte` | get, set | 0 = 队伍已满 <br/> 类型：字节 |



---

<a id="eventlocalplayercontrollerteam"></a>

## 🔌 EventLocalPlayerControllerTeam

事件"本地玩家控制队伍"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventLocalPlayerControllerTeam\>`



---

<a id="eventlocalplayerpawnchanged"></a>

## 🔌 EventLocalPlayerPawnChanged

事件 "local_player_pawn_changed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventLocalPlayerPawnChanged\>`



---

<a id="eventlocalplayerteam"></a>

## 🔌 EventLocalPlayerTeam

事件 "本地玩家队伍"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventLocalPlayerTeam\>`



---

<a id="eventlootcrateopened"></a>

## 🔌 EventLootCrateOpened

事件 "loot_crate_opened"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventLootCrateOpened\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 玩家实体索引<br/>类型: 玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 玩家实体索引<br/>类型: 玩家控制器 |
| `UserId` | `int` | get, set | 玩家实体索引<br/>类型: 玩家控制器 |
| `Type` | `string` | get, set | 板条箱类型（金属、木质或空投）<br/> 类型：字符串 |



---

<a id="eventlootcratevisible"></a>

## 🔌 EventLootCrateVisible

事件 "loot_crate_visible"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventLootCrateVisible\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 玩家实体索引<br/>类型: 玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 玩家实体索引<br/>类型: 玩家控制器 |
| `UserId` | `int` | get, set | 玩家实体索引<br/>类型: 玩家控制器 |
| `Subject` | `short` | get, set | crate entindex <br/> 类型: short |
| `Type` | `string` | get, set | 板条箱类型（金属、木质或空投）<br/> 类型：字符串 |



---

<a id="eventmapshutdown"></a>

## 🔌 EventMapShutdown

事件 "map_shutdown"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventMapShutdown\>`



---

<a id="eventmaptransition"></a>

## 🔌 EventMapTransition

事件 "地图过渡"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventMapTransition\>`



---

<a id="eventmatchendconditions"></a>

## 🔌 EventMatchEndConditions

事件 "match_end_conditions"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventMatchEndConditions\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Frags` | `int` | get, set | 类型：长整型 |
| `MaxRounds` | `int` | get, set | 类型：长整型 |
| `WinRounds` | `int` | get, set | 类型：长整型 |
| `Time` | `int` | get, set | 类型：长整型 |



---

<a id="eventmaterialdefaultcomplete"></a>

## 🔌 EventMaterialDefaultComplete

事件 "material_default_complete"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventMaterialDefaultComplete\>`



---

<a id="eventmbinputlockcancel"></a>

## 🔌 EventMbInputLockCancel

事件 "mb_input_lock_cancel"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventMbInputLockCancel\>`



---

<a id="eventmbinputlocksuccess"></a>

## 🔌 EventMbInputLockSuccess

事件 "mb_input_lock_success"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventMbInputLockSuccess\>`



---

<a id="eventmolotovdetonate"></a>

## 🔌 EventMolotovDetonate

事件"燃烧弹引爆"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventMolotovDetonate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `X` | `float` | get, set | 类型：float |
| `Y` | `float` | get, set | 类型：float |
| `Z` | `float` | get, set | 类型：float |



---

<a id="eventnavblocked"></a>

## 🔌 EventNavBlocked

事件 "nav_blocked"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventNavBlocked\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Area` | `int` | get, set | 类型：长整型 |
| `Blocked` | `bool` | get, set | 类型: bool |



---

<a id="eventnavgenerate"></a>

## 🔌 EventNavGenerate

事件 "nav_generate"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventNavGenerate\>`



---

<a id="eventnextlevelchanged"></a>

## 🔌 EventNextlevelChanged

事件 "nextlevel_changed" 是一个游戏事件，名称长度可达32个字符

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventNextlevelChanged\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `NextLevel` | `string` | get, set | 类型: 字符串 |
| `MapGroup` | `string` | get, set | 类型: 字符串 |
| `SkirmishMode` | `string` | get, set | 类型: 字符串 |



---

<a id="eventopencrateinstr"></a>

## 🔌 EventOpenCrateInstr

事件 "open_crate_instr"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventOpenCrateInstr\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 玩家实体索引<br/>类型: 玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 玩家实体索引<br/>类型: 玩家控制器 |
| `UserId` | `int` | get, set | 玩家实体索引<br/>类型: 玩家控制器 |
| `Subject` | `short` | get, set | crate entindex <br/> 类型: short |
| `Type` | `string` | get, set | 板条箱类型（金属、木质或空投）<br/> 类型：字符串 |



---

<a id="eventotherdeath"></a>

## 🔌 EventOtherDeath

事件 "other_death"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventOtherDeath\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `OtherID` | `short` | get, set | 其他实体ID（死亡者）<br/> 类型：short |
| `OtherType` | `string` | get, set | 其他实体类型<br/> 类型: 字符串 |
| `Attacker` | `short` | get, set | 击杀玩家的用户ID <br/> 类型: short |
| `Weapon` | `string` | get, set | 武器名称 击杀者使用的武器 <br/> 类型: 字符串 |
| `WeaponItemid` | `string` | get, set | 武器击杀者所使用的库存物品ID <br/> 类型：字符串 |
| `WeaponFauxitemid` | `string` | get, set | 武器击杀所使用的虚假物品ID <br/> 类型：字符串 |
| `WeaponOriginalownerXuid` | `string` | get, set | 类型: 字符串 |
| `Headshot` | `bool` | get, set | 标记为爆头 <br/> 类型: 布尔值 |
| `Penetrated` | `short` | get, set | 击杀目标前穿透射击的物体数量<br/> 类型：短整型 |
| `NoScope` | `bool` | get, set | 击杀未使用瞄准镜，用于死亡通知图标<br/>类型：布尔值 |
| `ThruSmoke` | `bool` | get, set | 扫描类武器穿透烟雾弹 <br/> 类型: 布尔 |
| `AttackerBlind` | `bool` | get, set | 攻击者因闪光弹致盲 <br/> 类型：布尔值 |



---

<a id="eventparachutedeploy"></a>

## 🔌 EventParachuteDeploy

事件 "parachute_deploy"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventParachuteDeploy\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |



---

<a id="eventparachutepickup"></a>

## 🔌 EventParachutePickup

事件 "parachute_pickup"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventParachutePickup\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |



---

<a id="eventphysgunpickup"></a>

## 🔌 EventPhysgunPickup

事件 "physgun_pickup"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPhysgunPickup\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Target` | `nint` | get, set | entity 拾取 <br/> 类型: ehandle |



---

<a id="eventplayeractivate"></a>

## 🔌 EventPlayerActivate

事件 "player_activate"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerActivate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户ID <br/> 类型: 玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户ID <br/> 类型: 玩家控制器 |
| `UserId` | `int` | get, set | 服务器上的用户ID <br/> 类型: 玩家控制器 |



---

<a id="eventplayeravengedteammate"></a>

## 🔌 EventPlayerAvengedTeammate

事件 "player_avenged_teammate"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerAvengedTeammate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AvengerIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `AvengerIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `AvengerId` | `int` | get, set | 类型：玩家控制器 |
| `AvengedPlayerIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `AvengedPlayerIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `AvengedPlayerId` | `int` | get, set | 类型：玩家控制器 |



---

<a id="eventplayerblind"></a>

## 🔌 EventPlayerBlind

事件 "player_blind"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerBlind\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `AttackerController` | `CCSPlayerController` | get | 抛出闪光弹的用户ID <br/> 类型: player_controller |
| `AttackerPawn` | `CCSPlayerPawn` | get | 抛出闪光弹的用户ID <br/> 类型: player_controller |
| `Attacker` | `int` | get, set | 抛出闪光弹的用户ID <br/> 类型: player_controller |
| `EntityID` | `short` | get, set | 闪光弹爆炸 <br/> 类型: short |
| `BlindDuration` | `float` | get, set | 类型：float |



---

<a id="eventplayerchangename"></a>

## 🔌 EventPlayerChangename

事件 "player_changename"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerChangename\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户ID <br/> 类型: 玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户ID <br/> 类型: 玩家控制器 |
| `UserId` | `int` | get, set | 服务器上的用户ID <br/> 类型: 玩家控制器 |
| `OldName` | `string` | get, set | 玩家旧（当前）名称<br/>类型：字符串 |
| `NewName` | `string` | get, set | 玩家新名称  
类型：字符串 |



---

<a id="eventplayerchat"></a>

## 🔌 EventPlayerChat

Event "player_chat" 一个公共玩家聊天

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerChat\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TeamOnly` | `bool` | get, set | 如果是仅队伍聊天则返回true <br/> 类型: bool |
| `UserIdController` | `CCSPlayerController` | get | 聊天中的玩家  
类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 聊天中的玩家  
类型：玩家控制器 |
| `UserId` | `int` | get, set | 聊天中的玩家  
类型：玩家控制器 |
| `Playerid` | `short` | get, set | 聊天玩家ID <br/> 类型：短整型 |
| `Text` | `string` | get, set | 聊天文本<br/>类型: 字符串 |



---

<a id="eventplayerconnect"></a>

## 🔌 EventPlayerConnect

事件 "player_connect" 一名新客户端已连接

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerConnect\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | get, set | 玩家名称<br/>类型: 字符串 |
| `UserIdController` | `CCSPlayerController` | get | 用户ID（服务器上唯一）<br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 用户ID（服务器上唯一）<br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 用户ID（服务器上唯一）<br/> 类型：玩家控制器 |
| `NetworkID` | `string` | get, set | 玩家网络（即Steam）ID  
类型：字符串 |
| `XuID` | `ulong` | get, set | steam ID <br/> 类型：uint64 |
| `Bot` | `bool` | get, set | 类型: bool |



---

<a id="eventplayerconnectfull"></a>

## 🔌 EventPlayerConnectFull

事件 "player_connect_full" 玩家已在连接序列中发送最终消息

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerConnectFull\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 用户ID（服务器上唯一）<br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 用户ID（服务器上唯一）<br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 用户ID（服务器上唯一）<br/> 类型：玩家控制器 |



---

<a id="eventplayerdeath"></a>

## 🔌 EventPlayerDeath

事件 "player_death" 游戏事件，名称长度最多为32个字符

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerDeath\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 用户ID（死亡者）<br/> 类型：player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 用户ID（死亡者）<br/> 类型：player_controller_and_pawn |
| `UserId` | `int` | get, set | 用户ID（死亡者）<br/> 类型：player_controller_and_pawn |
| `AttackerController` | `CCSPlayerController` | get | 杀死玩家的用户ID<br/>类型：玩家控制器与棋子 |
| `AttackerPawn` | `CCSPlayerPawn` | get | 杀死玩家的用户ID<br/>类型：玩家控制器与棋子 |
| `Attacker` | `int` | get, set | 杀死玩家的用户ID<br/>类型：玩家控制器与棋子 |
| `AssisterController` | `CCSPlayerController` | get | 协助击杀的玩家<br/>类型: player_controller_and_pawn |
| `AssisterPawn` | `CCSPlayerPawn` | get | 协助击杀的玩家<br/>类型: player_controller_and_pawn |
| `Assister` | `int` | get, set | 协助击杀的玩家<br/>类型: player_controller_and_pawn |
| `AssistedFlash` | `bool` | get, set | assister 使用闪光弹辅助  
类型：布尔值 |
| `Weapon` | `string` | get, set | 武器名称 击杀者使用的武器 <br/> 类型: 字符串 |
| `WeaponItemid` | `string` | get, set | 武器击杀者所使用的库存物品ID <br/> 类型：字符串 |
| `WeaponFauxitemid` | `string` | get, set | 武器击杀所使用的虚假物品ID <br/> 类型：字符串 |
| `WeaponOriginalownerXuid` | `string` | get, set | 类型: 字符串 |
| `Headshot` | `bool` | get, set | 标记为爆头 <br/> 类型: 布尔值 |
| `Dominated` | `short` | get, set | 杀手是否以此击杀压制了受害者 <br/> 类型: short |
| `Revenge` | `short` | get, set | 杀手是否借助此次击杀成功复仇受害者  
类型：短整型 |
| `Wipe` | `short` | get, set | 是否为导致小队全灭的击杀 <br/> 类型：short |
| `Penetrated` | `short` | get, set | 击杀目标前穿透射击的物体数量<br/> 类型：短整型 |
| `NoReplay` | `bool` | get, set | 如果回放数据不可用，此字段将存在并设置为false  
类型：布尔 |
| `NoScope` | `bool` | get, set | 击杀未使用瞄准镜，用于死亡通知图标<br/>类型：布尔值 |
| `ThruSmoke` | `bool` | get, set | 扫描类武器穿透烟雾弹 <br/> 类型: 布尔 |
| `AttackerBlind` | `bool` | get, set | 攻击者因闪光弹致盲 <br/> 类型：布尔值 |
| `Distance` | `float` | get, set | 距离受害者的距离（米）<br/> 类型：浮点数 |
| `DmgHealth` | `short` | get, set | - |
| `ActualDmgHealth` | `int` | get, set | 对生命值造成的伤害 <br/> 类型：整数 |
| `DmgArmor` | `byte` | get, set | - |
| `ActualDmgArmor` | `int` | get, set | 对护甲造成的伤害<br/>类型：整型 |
| `HitGroup` | `byte` | get, set | - |
| `ActualHitGroup` | `HitGroup_t` | get, set | 命中的身体部位组 <br/> 类型: HitGroup_t |
| `AttackerInAir` | `bool` | get, set | 攻击者处于半空中 <br/> 类型: bool |



---

<a id="eventplayerdecal"></a>

## 🔌 EventPlayerDecal

事件 "player_decal"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerDecal\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型: 玩家棋子 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型: 玩家棋子 |
| `UserId` | `int` | get, set | 类型: 玩家棋子 |



---

<a id="eventplayerdisconnect"></a>

## 🔌 EventPlayerDisconnect

事件 "player_disconnect" 客户端已断开连接

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerDisconnect\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户ID <br/> 类型: 玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户ID <br/> 类型: 玩家控制器 |
| `UserId` | `int` | get, set | 服务器上的用户ID <br/> 类型: 玩家控制器 |
| `Reason` | `short` | get, set | 参见networkdisconnect枚举protobuf <br/> 类型：短整型 |
| `Name` | `string` | get, set | 玩家名称<br/>类型: 字符串 |
| `NetworkID` | `string` | get, set | 玩家网络（即Steam）ID  
类型：字符串 |
| `XuID` | `ulong` | get, set | steam ID <br/> 类型：uint64 |
| `PlayerID` | `short` | get, set | type: short |



---

<a id="eventplayerfalldamage"></a>

## 🔌 EventPlayerFalldamage

事件 "player_falldamage"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerFalldamage\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `Damage` | `float` | get, set | 类型：float |



---

<a id="eventplayerfootstep"></a>

## 🔌 EventPlayerFootstep

Event "player_footstep"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerFootstep\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型: 玩家棋子 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型: 玩家棋子 |
| `UserId` | `int` | get, set | 类型: 玩家棋子 |



---

<a id="eventplayerfullupdate"></a>

## 🔌 EventPlayerFullUpdate

事件 "player_full_update"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerFullUpdate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户ID <br/> 类型: 玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户ID <br/> 类型: 玩家控制器 |
| `UserId` | `int` | get, set | 服务器上的用户ID <br/> 类型: 玩家控制器 |
| `Count` | `short` | get, set | 此完整更新的编号<br/>类型: short |



---

<a id="eventplayergivenc4"></a>

## 🔌 EventPlayerGivenC4

事件 "player_given_c4"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerGivenC4\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 接收了C4的用户ID <br/> 类型: player_controller |
| `UserIdPawn` | `CCSPlayerPawn` | get | 接收了C4的用户ID <br/> 类型: player_controller |
| `UserId` | `int` | get, set | 接收了C4的用户ID <br/> 类型: player_controller |



---

<a id="eventplayerhintmessage"></a>

## 🔌 EventPlayerHintmessage

事件 "player_hintmessage"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerHintmessage\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `HintMessage` | `string` | get, set | 本地化提示字符串<br/>类型: 字符串 |



---

<a id="eventplayerhurt"></a>

## 🔌 EventPlayerHurt

事件 "player_hurt"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerHurt\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 受伤的玩家 <br/> 类型: player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 受伤的玩家 <br/> 类型: player_controller_and_pawn |
| `UserId` | `int` | get, set | 受伤的玩家 <br/> 类型: player_controller_and_pawn |
| `AttackerController` | `CCSPlayerController` | get | 攻击者玩家<br/>类型：玩家控制器与角色 |
| `AttackerPawn` | `CCSPlayerPawn` | get | 攻击者玩家<br/>类型：玩家控制器与角色 |
| `Attacker` | `int` | get, set | 攻击者玩家<br/>类型：玩家控制器与角色 |
| `Health` | `byte` | get, set | - |
| `ActualHealth` | `int` | get, set | 剩余生命值  
类型：整数 |
| `Armor` | `byte` | get, set | - |
| `ActualArmor` | `int` | get, set | 剩余护甲值 <br/> 类型：整数 |
| `Weapon` | `string` | get, set | 攻击者使用的武器名称，如果不是世界 <br/> 类型：字符串 |
| `DmgHealth` | `short` | get, set | - |
| `ActualDmgHealth` | `int` | get, set | 对生命值造成的伤害 <br/> 类型：整数 |
| `DmgArmor` | `byte` | get, set | - |
| `ActualDmgArmor` | `int` | get, set | 对护甲造成的伤害<br/>类型：整型 |
| `HitGroup` | `byte` | get, set | - |
| `ActualHitGroup` | `HitGroup_t` | get, set | 命中的身体部位组 <br/> 类型: HitGroup_t |



---

<a id="eventplayerinfo"></a>

## 🔌 EventPlayerInfo

事件 "player_info" 一名玩家更改了他的名称

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | get, set | 玩家名称<br/>类型: 字符串 |
| `UserIdController` | `CCSPlayerController` | get | 用户ID（服务器上唯一）<br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 用户ID（服务器上唯一）<br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 用户ID（服务器上唯一）<br/> 类型：玩家控制器 |
| `SteamID` | `ulong` | get, set | 玩家网络（如Steam）ID <br/> 类型：uint64 |
| `Bot` | `bool` | get, set | 如果玩家是AI机器人则为true <br/> 类型：bool |



---

<a id="eventplayerjump"></a>

## 🔌 EventPlayerJump

事件 "player_jump"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerJump\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |



---

<a id="eventplayerping"></a>

## 🔌 EventPlayerPing

事件 "player_ping"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerPing\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `EntityID` | `short` | get, set | type: short |
| `X` | `float` | get, set | 类型：float |
| `Y` | `float` | get, set | 类型：float |
| `Z` | `float` | get, set | 类型：float |
| `Urgent` | `bool` | get, set | 类型: bool |



---

<a id="eventplayerpingstop"></a>

## 🔌 EventPlayerPingStop

事件 "player_ping_stop"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerPingStop\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityID` | `short` | get, set | type: short |



---

<a id="eventplayerradio"></a>

## 🔌 EventPlayerRadio

事件 "player_radio"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerRadio\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `Slot` | `short` | get, set | type: short |



---

<a id="eventplayerresetvote"></a>

## 🔌 EventPlayerResetVote

事件 "player_reset_vote"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerResetVote\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Vote` | `bool` | get, set | 类型: bool |



---

<a id="eventplayerscore"></a>

## 🔌 EventPlayerScore

事件 "player_score" 玩家得分已更改

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerScore\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户ID <br/> 类型: 玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户ID <br/> 类型: 玩家控制器 |
| `UserId` | `int` | get, set | 服务器上的用户ID <br/> 类型: 玩家控制器 |
| `Kills` | `short` | get, set | # 击杀数<br/> 类型：短整型 |
| `Deaths` | `short` | get, set | # 死亡次数 <br/> 类型：short |
| `Score` | `short` | get, set | 游戏总得分 <br/> 类型: 短整型 |



---

<a id="eventplayershoot"></a>

## 🔌 EventPlayerShoot

事件 "player_shoot" 玩家射击其武器

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerShoot\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户ID <br/> 类型: 玩家控制器与棋子 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户ID <br/> 类型: 玩家控制器与棋子 |
| `UserId` | `int` | get, set | 服务器上的用户ID <br/> 类型: 玩家控制器与棋子 |
| `Weapon` | `byte` | get, set | 武器ID<br/>类型：字节 |
| `Mode` | `byte` | get, set | 武器模式 <br/> 类型: 字节 |



---

<a id="eventplayersound"></a>

## 🔌 EventPlayerSound

事件 "player_sound"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerSound\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `Radius` | `int` | get, set | 类型: int |
| `Duration` | `float` | get, set | 类型：float |
| `Step` | `bool` | get, set | 类型: bool |



---

<a id="eventplayerspawn"></a>

## 🔌 EventPlayerSpawn

事件 "player_spawn" 玩家在游戏中生成

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerSpawn\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |



---

<a id="eventplayerspawned"></a>

## 🔌 EventPlayerSpawned

事件 "player_spawned"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerSpawned\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `InRestart` | `bool` | get, set | 如果重启处于待处理状态，则为true <br/> 类型：bool |



---

<a id="eventplayerstatsupdated"></a>

## 🔌 EventPlayerStatsUpdated

事件 "player_stats_updated"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerStatsUpdated\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ForceUpload` | `bool` | get, set | 类型: bool |



---

<a id="eventplayerteam"></a>

## 🔌 EventPlayerTeam

事件 "player_team"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerTeam\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 玩家  
类型：玩家控制器与棋子 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 玩家  
类型：玩家控制器与棋子 |
| `UserId` | `int` | get, set | 玩家  
类型：玩家控制器与棋子 |
| `Team` | `byte` | get, set | 团队ID <br/> 类型：字节 |
| `OldTeam` | `byte` | get, set | 旧队伍ID <br/> 类型：字节 |
| `Disconnect` | `bool` | get, set | 团队变更因为玩家断开连接<br/> 类型：布尔值 |
| `Silent` | `bool` | get, set | 类型: bool |
| `Name` | `string` | get, set | 类型: 字符串 |
| `IsBot` | `bool` | get, set | 如果玩家是机器人则为真<br/>类型：布尔值 |



---

<a id="eventragdolldissolved"></a>

## 🔌 EventRagdollDissolved

事件 "ragdoll_dissolved"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRagdollDissolved\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntIndex` | `int` | get, set | 类型：长整型 |



---

<a id="eventreadgametitledata"></a>

## 🔌 EventReadGameTitledata

事件 "read_game_titledata" 从用户档案中读取游戏标题数据

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventReadGameTitledata\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ControllerId` | `short` | get, set | 用户控制器ID<br/>类型: short |



---

<a id="eventrepostxboxachievements"></a>

## 🔌 EventRepostXboxAchievements

事件 "repost_xbox_achievements"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRepostXboxAchievements\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SplitScreenPlayer` | `short` | get, set | 分屏ID <br/> 类型: short |



---

<a id="eventresetgametitledata"></a>

## 🔌 EventResetGameTitledata

事件 "reset_game_titledata" 重置用户标题数据；不要自动写入配置文件

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventResetGameTitledata\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ControllerId` | `short` | get, set | 用户控制器ID<br/>类型: short |



---

<a id="eventroundannouncefinal"></a>

## 🔌 EventRoundAnnounceFinal

Event "round_announce_final"

翻译：事件 "round_announce_final"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundAnnounceFinal\>`



---

<a id="eventroundannouncelastroundhalf"></a>

## 🔌 EventRoundAnnounceLastRoundHalf

事件 "round_announce_last_round_half"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundAnnounceLastRoundHalf\>`



---

<a id="eventroundannouncematchpoint"></a>

## 🔌 EventRoundAnnounceMatchPoint

事件 "round_announce_match_point"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundAnnounceMatchPoint\>`



---

<a id="eventroundannouncematchstart"></a>

## 🔌 EventRoundAnnounceMatchStart

事件 "round_announce_match_start"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundAnnounceMatchStart\>`



---

<a id="eventroundannouncewarmup"></a>

## 🔌 EventRoundAnnounceWarmup

事件 "round_announce_warmup"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundAnnounceWarmup\>`



---

<a id="eventroundend"></a>

## 🔌 EventRoundEnd

事件 "round_end"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundEnd\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Winner` | `byte` | get, set | 获胜队伍/用户 i <br/> 类型: 字节 |
| `Reason` | `byte` | get, set | 团队获胜原因 <br/> 类型: 字节 |
| `Message` | `string` | get, set | 回合结束消息  
类型：字符串 |
| `Time` | `float` | get, set | 类型：float |
| `Legacy` | `byte` | get, set | 服务端生成的遗留值 <br/> 类型：字节 |
| `PlayerCount` | `short` | get, set | 回合结束时存活玩家总数，用于数据统计收集，当客户端在回放中接收此消息时在服务器端计算 <br/> 类型：short |
| `NoMusic` | `byte` | get, set | 若已设置，则勿播放回合结束音乐，因操作仍在进行中<br/> 类型：字节 |



---

<a id="eventroundenduploadstats"></a>

## 🔌 EventRoundEndUploadStats

事件 "round_end_upload_stats"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundEndUploadStats\>`



---

<a id="eventroundfreezeend"></a>

## 🔌 EventRoundFreezeEnd

事件 "round_freeze_end"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundFreezeEnd\>`



---

<a id="eventroundmvp"></a>

## 🔌 EventRoundMvp

事件 "round_mvp"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundMvp\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Reason` | `short` | get, set | type: short |
| `Value` | `int` | get, set | 类型：长整型 |
| `MusickItMvps` | `int` | get, set | 类型：长整型 |
| `NoMusic` | `byte` | get, set | 类型: 字节 |
| `MusickItID` | `int` | get, set | 类型：长整型 |



---

<a id="eventroundofficiallyended"></a>

## 🔌 EventRoundOfficiallyEnded

事件 "round_officially_ended"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundOfficiallyEnded\>`



---

<a id="eventroundpoststart"></a>

## 🔌 EventRoundPoststart

事件 "round_poststart" 在所有其他回合重启动作之后发送

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundPoststart\>`



---

<a id="eventroundprestart"></a>

## 🔌 EventRoundPrestart

事件 "round_prestart" 在所有其他回合重启动作之前发送

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundPrestart\>`



---

<a id="eventroundstart"></a>

## 🔌 EventRoundStart

事件 "round_start"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundStart\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TimeLimit` | `int` | get, set | 回合时间限制（秒）<br/> 类型：长整型 |
| `FragLimit` | `int` | get, set | frag 限制（秒）<br/> 类型：长整型 |
| `Objective` | `string` | get, set | 回合目标 <br/> 类型: 字符串 |



---

<a id="eventroundstartpostnav"></a>

## 🔌 EventRoundStartPostNav

事件 "round_start_post_nav"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundStartPostNav\>`



---

<a id="eventroundstartpreentity"></a>

## 🔌 EventRoundStartPreEntity

事件 "round_start_pre_entity"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundStartPreEntity\>`



---

<a id="eventroundtimewarning"></a>

## 🔌 EventRoundTimeWarning

事件 "round_time_warning"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundTimeWarning\>`



---

<a id="eventseasoncoinlevelup"></a>

## 🔌 EventSeasoncoinLevelup

事件 "seasoncoin_levelup"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSeasoncoinLevelup\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Category` | `short` | get, set | type: short |
| `Rank` | `short` | get, set | type: short |



---

<a id="eventservercvar"></a>

## 🔌 EventServerCvar

事件 "server_cvar" 服务器控制台变量已更改

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventServerCvar\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CVarName` | `string` | get, set | cvar 名称，例如 "mp_roundtime" <br/> 类型：字符串 |
| `CVarValue` | `string` | get, set | 新cvar值<br/>类型: 字符串 |



---

<a id="eventservermessage"></a>

## 🔌 EventServerMessage

事件 "server_message" 通用服务器消息

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventServerMessage\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Text` | `string` | get, set | 消息文本 <br/> 类型：字符串 |



---

<a id="eventserverpreshutdown"></a>

## 🔌 EventServerPreShutdown

事件 "server_pre_shutdown" 服务器即将关闭

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventServerPreShutdown\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Reason` | `string` | get, set | 服务器即将关闭的原因 <br/> 类型: 字符串 |



---

<a id="eventservershutdown"></a>

## 🔌 EventServerShutdown

事件 "server_shutdown" 服务器关闭

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventServerShutdown\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Reason` | `string` | get, set | 服务器关闭的原因<br/> 类型: 字符串 |



---

<a id="eventserverspawn"></a>

## 🔌 EventServerSpawn

事件 "server_spawn" 在服务器启动时发送一次

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventServerSpawn\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Hostname` | `string` | get, set | 公共主机名<br/>类型：字符串 |
| `Address` | `string` | get, set | 主机名、IP或DNS名称 <br/> 类型：字符串 |
| `Port` | `short` | get, set | 服务器端口<br/>类型：short |
| `Game` | `string` | get, set | 游戏目录<br/>类型: 字符串 |
| `MapName` | `string` | get, set | 地图名称<br/>类型：字符串 |
| `AddonName` | `string` | get, set | 附加资源名称<br/>类型：字符串 |
| `MaxPlayers` | `int` | get, set | 最大玩家数<br/>类型：长整型 |
| `Os` | `string` | get, set | WIN32, LINUX  
类型：字符串 |
| `Dedicated` | `bool` | get, set | 如果是专用服务器，则为 true<br/> 类型：布尔 |
| `Password` | `bool` | get, set | 如果受密码保护则为真 <br/> 类型: 布尔 |



---

<a id="eventsetinstructorgroupenabled"></a>

## 🔌 EventSetInstructorGroupEnabled

事件 "set_instructor_group_enabled"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSetInstructorGroupEnabled\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Group` | `string` | get, set | 类型: 字符串 |
| `Enabled` | `short` | get, set | type: short |



---

<a id="eventsfuievent"></a>

## 🔌 EventSfuievent

事件“sfuievent”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSfuievent\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Action` | `string` | get, set | 类型: 字符串 |
| `Data` | `string` | get, set | 类型: 字符串 |
| `Slot` | `byte` | get, set | 类型: 字节 |



---

<a id="eventshowdeathpanel"></a>

## 🔌 EventShowDeathpanel

事件 "show_deathpanel"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventShowDeathpanel\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `VictimController` | `CCSPlayerController` | get | 被杀者的结束索引 <br/> 类型: player_controller_and_pawn |
| `VictimPawn` | `CCSPlayerPawn` | get | 被杀者的结束索引 <br/> 类型: player_controller_and_pawn |
| `Victim` | `int` | get, set | 被杀者的结束索引 <br/> 类型: player_controller_and_pawn |
| `Killer` | `nint` | get, set | 击杀者实体的实体索引 <br/> 类型：ehandle |
| `KillerControllerController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `KillerControllerPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `KillerController` | `int` | get, set | 类型：玩家控制器 |
| `HitsTaken` | `short` | get, set | type: short |
| `DamageTaken` | `short` | get, set | type: short |
| `HitsGiven` | `short` | get, set | type: short |
| `DamageGiven` | `short` | get, set | type: short |



---

<a id="eventshowsurvivalrespawnstatus"></a>

## 🔌 EventShowSurvivalRespawnStatus

Event "show_survival_respawn_status"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventShowSurvivalRespawnStatus\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `LocToken` | `string` | get, set | 类型: 字符串 |
| `Duration` | `int` | get, set | 类型：长整型 |
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |



---

<a id="eventsilencerdetach"></a>

## 🔌 EventSilencerDetach

事件 "silencer_detach"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSilencerDetach\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |



---

<a id="eventsilenceroff"></a>

## 🔌 EventSilencerOff

事件 "silencer_off"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSilencerOff\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |



---

<a id="eventsilenceron"></a>

## 🔌 EventSilencerOn

事件 "silencer_on"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSilencerOn\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |



---

<a id="eventsmokebeaconparadrop"></a>

## 🔌 EventSmokeBeaconParadrop

事件 "smoke_beacon_paradrop"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSmokeBeaconParadrop\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `ParaDrop` | `short` | get, set | type: short |



---

<a id="eventsmokegrenadedetonate"></a>

## 🔌 EventSmokegrenadeDetonate

事件 "smokegrenade_detonate"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSmokegrenadeDetonate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `EntityID` | `short` | get, set | type: short |
| `X` | `float` | get, set | 类型：float |
| `Y` | `float` | get, set | 类型：float |
| `Z` | `float` | get, set | 类型：float |



---

<a id="eventsmokegrenadeexpired"></a>

## 🔌 EventSmokegrenadeExpired

事件 "smokegrenade_expired"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSmokegrenadeExpired\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `EntityID` | `short` | get, set | type: short |
| `X` | `float` | get, set | 类型：float |
| `Y` | `float` | get, set | 类型：float |
| `Z` | `float` | get, set | 类型：float |



---

<a id="eventspecmodeupdated"></a>

## 🔌 EventSpecModeUpdated

事件 "spec_mode_updated"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSpecModeUpdated\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 观战玩家 <br/> 类型: player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 观战玩家 <br/> 类型: player_controller_and_pawn |
| `UserId` | `int` | get, set | 观战玩家 <br/> 类型: player_controller_and_pawn |



---

<a id="eventspectargetupdated"></a>

## 🔌 EventSpecTargetUpdated

事件 "spec_target_updated"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSpecTargetUpdated\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 观战玩家 <br/> 类型: player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 观战玩家 <br/> 类型: player_controller_and_pawn |
| `UserId` | `int` | get, set | 观战玩家 <br/> 类型: player_controller_and_pawn |
| `Target` | `nint` | get, set | 目标实体的eHandle<br/>类型: eHandle |



---

<a id="eventstarthalftime"></a>

## 🔌 EventStartHalftime

事件 "start_halftime"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventStartHalftime\>`



---

<a id="eventstartvote"></a>

## 🔌 EventStartVote

事件 "start_vote"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventStartVote\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Type` | `byte` | get, set | 类型: 字节 |
| `VoteParameter` | `short` | get, set | type: short |



---

<a id="eventstorepricesheetupdated"></a>

## 🔌 EventStorePricesheetUpdated

事件 "store_pricesheet_updated"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventStorePricesheetUpdated\>`



---

<a id="eventsurvivalannouncephase"></a>

## 🔌 EventSurvivalAnnouncePhase

事件 "survival_announce_phase"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSurvivalAnnouncePhase\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Phase` | `short` | get, set | 阶段编号<br/> 类型：短整型 |



---

<a id="eventsurvivalnorespawnsfinal"></a>

## 🔌 EventSurvivalNoRespawnsFinal

事件 "survival_no_respawns_final"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSurvivalNoRespawnsFinal\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |



---

<a id="eventsurvivalnorespawnswarning"></a>

## 🔌 EventSurvivalNoRespawnsWarning

事件 "survival_no_respawns_warning"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSurvivalNoRespawnsWarning\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |



---

<a id="eventsurvivalparadropbreak"></a>

## 🔌 EventSurvivalParadropBreak

事件 "survival_paradrop_break"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSurvivalParadropBreak\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityID` | `short` | get, set | type: short |



---

<a id="eventsurvivalparadropspawn"></a>

## 🔌 EventSurvivalParadropSpawn

事件 "survival_paradrop_spawn"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSurvivalParadropSpawn\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityID` | `short` | get, set | type: short |



---

<a id="eventsurvivalteammaterespawn"></a>

## 🔌 EventSurvivalTeammateRespawn

事件 "survival_teammate_respawn"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSurvivalTeammateRespawn\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |



---

<a id="eventswitchteam"></a>

## 🔌 EventSwitchTeam

事件 "switch_team"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSwitchTeam\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `NumPlayers` | `short` | get, set | 双方T和CT阵营中的活跃玩家数量 <br/> 类型：short |
| `NumSpectators` | `short` | get, set | 观众人数 <br/> 类型: short |
| `AvgRank` | `short` | get, set | 玩家平均段位 <br/> 类型: 短整型 |
| `NumTSlotsFree` | `short` | get, set | type: short |
| `NumCTSlotsFree` | `short` | get, set | type: short |



---

<a id="eventtagrenadedetonate"></a>

## 🔌 EventTagrenadeDetonate

事件 "tagrenade_detonate"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTagrenadeDetonate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `EntityID` | `short` | get, set | type: short |
| `X` | `float` | get, set | 类型：float |
| `Y` | `float` | get, set | 类型：float |
| `Z` | `float` | get, set | 类型：float |



---

<a id="eventteaminfo"></a>

## 🔌 EventTeamInfo

事件 "team_info" 关于队伍的信息

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTeamInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TeamID` | `byte` | get, set | 唯一队伍ID<br/>类型：字节 |
| `Teamname` | `string` | get, set | 队伍名称 例如"蓝队" <br/> 类型: 字符串 |



---

<a id="eventteamintroend"></a>

## 🔌 EventTeamIntroEnd

事件 "team_intro_end"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTeamIntroEnd\>`



---

<a id="eventteamintrostart"></a>

## 🔌 EventTeamIntroStart

事件 "team_intro_start"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTeamIntroStart\>`



---

<a id="eventteamscore"></a>

## 🔌 EventTeamScore

事件 "team_score" 队伍得分已改变

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTeamScore\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TeamID` | `byte` | get, set | 团队ID <br/> 类型：字节 |
| `Score` | `short` | get, set | 队伍总分 <br/> 类型：短整型 |



---

<a id="eventteamchangepending"></a>

## 🔌 EventTeamchangePending

事件 "teamchange_pending"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTeamchangePending\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `ToTeam` | `byte` | get, set | 类型: 字节 |



---

<a id="eventteamplaybroadcastaudio"></a>

## 🔌 EventTeamplayBroadcastAudio

事件 "teamplay_broadcast_audio" 向队伍内的所有玩家播放音效

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTeamplayBroadcastAudio\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Team` | `byte` | get, set | 唯一队伍ID<br/>类型：字节 |
| `Sound` | `string` | get, set | 要发出的声音名称<br/>类型：字符串 |



---

<a id="eventteamplayroundstart"></a>

## 🔌 EventTeamplayRoundStart

事件 "teamplay_round_start" 回合重启

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTeamplayRoundStart\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `FullReset` | `bool` | get, set | 是否为地图的完全重置 <br/> 类型: 布尔值 |



---

<a id="eventtournamentreward"></a>

## 🔌 EventTournamentReward

事件 "tournament_reward"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTournamentReward\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `DefIndex` | `int` | get, set | 类型：长整型 |
| `TotalRewards` | `int` | get, set | 类型：长整型 |
| `AccountID` | `int` | get, set | 类型：长整型 |



---

<a id="eventtrialtimeexpired"></a>

## 🔌 EventTrialTimeExpired

事件 "trial_time_expired"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTrialTimeExpired\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 玩家，其时间已过期 <br/> 类型：player_controller |
| `UserIdPawn` | `CCSPlayerPawn` | get | 玩家，其时间已过期 <br/> 类型：player_controller |
| `UserId` | `int` | get, set | 玩家，其时间已过期 <br/> 类型：player_controller |



---

<a id="eventugcfiledownloadfinished"></a>

## 🔌 EventUgcFileDownloadFinished

事件 "ugc_file_download_finished"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventUgcFileDownloadFinished\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `HContent` | `ulong` | get, set | 此特定内容（图像或地图）的ID <br/> 类型：uint64 |



---

<a id="eventugcfiledownloadstart"></a>

## 🔌 EventUgcFileDownloadStart

事件 "ugc_file_download_start"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventUgcFileDownloadStart\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `HContent` | `ulong` | get, set | 此特定内容（图像或地图）的ID <br/> 类型：uint64 |
| `PublishedFileId` | `ulong` | get, set | 关联内容包的ID <br/> 类型: uint64 |



---

<a id="eventugcmapdownloaderror"></a>

## 🔌 EventUgcMapDownloadError

事件 "ugc_map_download_error"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventUgcMapDownloadError\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PublishedFileId` | `ulong` | get, set | 类型: uint64 |
| `ErrorCode` | `int` | get, set | 类型：长整型 |



---

<a id="eventugcmapinforeceived"></a>

## 🔌 EventUgcMapInfoReceived

事件 "ugc_map_info_received"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventUgcMapInfoReceived\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PublishedFileId` | `ulong` | get, set | 类型: uint64 |



---

<a id="eventugcmapunsubscribed"></a>

## 🔌 EventUgcMapUnsubscribed

事件 "ugc_map_unsubscribed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventUgcMapUnsubscribed\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PublishedFileId` | `ulong` | get, set | 类型: uint64 |



---

<a id="eventupdatematchmakingstats"></a>

## 🔌 EventUpdateMatchmakingStats

事件 "update_matchmaking_stats"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventUpdateMatchmakingStats\>`



---

<a id="eventuserdatadownloaded"></a>

## 🔌 EventUserDataDownloaded

当成就/统计数据从Steam或Xbox Live下载时触发"user_data_downloaded"事件

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventUserDataDownloaded\>`



---

<a id="eventvipescaped"></a>

## 🔌 EventVipEscaped

事件 “vip_escaped”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVipEscaped\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 成为VIP的玩家 <br/> 类型: player_controller |
| `UserIdPawn` | `CCSPlayerPawn` | get | 成为VIP的玩家 <br/> 类型: player_controller |
| `UserId` | `int` | get, set | 成为VIP的玩家 <br/> 类型: player_controller |



---

<a id="eventvipkilled"></a>

## 🔌 EventVipKilled

事件 "vip_killed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVipKilled\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 成为VIP的玩家 <br/> 类型: player_controller |
| `UserIdPawn` | `CCSPlayerPawn` | get | 成为VIP的玩家 <br/> 类型: player_controller |
| `UserId` | `int` | get, set | 成为VIP的玩家 <br/> 类型: player_controller |
| `AttackerController` | `CCSPlayerController` | get | 击杀VIP的用户ID <br/> 类型: player_controller |
| `AttackerPawn` | `CCSPlayerPawn` | get | 击杀VIP的用户ID <br/> 类型: player_controller |
| `Attacker` | `int` | get, set | 击杀VIP的用户ID <br/> 类型: player_controller |



---

<a id="eventvotecast"></a>

## 🔌 EventVoteCast

事件 "vote_cast"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVoteCast\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `VoteOption` | `byte` | get, set | 玩家投票选择的选项<br/>类型：字节 |
| `Team` | `short` | get, set | type: short |
| `UserIdController` | `CCSPlayerController` | get | 投票的玩家 <br/> 类型: player_controller |
| `UserIdPawn` | `CCSPlayerPawn` | get | 投票的玩家 <br/> 类型: player_controller |
| `UserId` | `int` | get, set | 投票的玩家 <br/> 类型: player_controller |



---

<a id="eventvotecastno"></a>

## 🔌 EventVoteCastNo

事件 "vote_cast_no"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVoteCastNo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Team` | `byte` | get, set | 类型: 字节 |
| `EntityID` | `int` | get, set | 投票者的实体ID <br/> 类型: long |



---

<a id="eventvotecastyes"></a>

## 🔌 EventVoteCastYes

事件 "vote_cast_yes"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVoteCastYes\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Team` | `byte` | get, set | 类型: 字节 |
| `EntityID` | `int` | get, set | 投票者的实体ID <br/> 类型: long |



---

<a id="eventvotechanged"></a>

## 🔌 EventVoteChanged

事件 "vote_changed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVoteChanged\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `YesVotes` | `byte` | get, set | 类型: 字节 |
| `NoVotes` | `byte` | get, set | 类型: 字节 |
| `PotentialVotes` | `byte` | get, set | 类型: 字节 |
| `VoteOption1` | `byte` | get, set | 类型: 字节 |
| `VoteOption2` | `byte` | get, set | 类型: 字节 |
| `VoteOption3` | `byte` | get, set | 类型: 字节 |
| `VoteOption4` | `byte` | get, set | 类型: 字节 |
| `VoteOption5` | `byte` | get, set | 类型: 字节 |



---

<a id="eventvoteended"></a>

## 🔌 EventVoteEnded

事件 "vote_ended"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVoteEnded\>`



---

<a id="eventvotefailed"></a>

## 🔌 EventVoteFailed

事件 "vote_failed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVoteFailed\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Team` | `byte` | get, set | 类型: 字节 |



---

<a id="eventvoteoptions"></a>

## 🔌 EventVoteOptions

事件 "vote_options"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVoteOptions\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Count` | `byte` | get, set | 选项数量 - 最多MAX_VOTE_OPTIONS <br/> 类型：byte |
| `Option1` | `string` | get, set | 类型: 字符串 |
| `Option2` | `string` | get, set | 类型: 字符串 |
| `Option3` | `string` | get, set | 类型: 字符串 |
| `Option4` | `string` | get, set | 类型: 字符串 |
| `Option5` | `string` | get, set | 类型: 字符串 |



---

<a id="eventvotepassed"></a>

## 🔌 EventVotePassed

事件 "vote_passed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVotePassed\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Details` | `string` | get, set | 类型: 字符串 |
| `Param1` | `string` | get, set | 类型: 字符串 |
| `Team` | `byte` | get, set | 类型: 字节 |



---

<a id="eventvotestarted"></a>

## 🔌 EventVoteStarted

事件 "vote_started"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVoteStarted\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Issue` | `string` | get, set | 类型: 字符串 |
| `Param1` | `string` | get, set | 类型: 字符串 |
| `VoteData` | `string` | get, set | 类型: 字符串 |
| `Team` | `byte` | get, set | 类型: 字节 |
| `Initiator` | `int` | get, set | 发起投票的玩家实体ID <br/> 类型：long |



---

<a id="eventwarmupend"></a>

## 🔌 EventWarmupEnd

事件 "warmup_end"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventWarmupEnd\>`



---

<a id="eventweaponfire"></a>

## 🔌 EventWeaponFire

事件 "weapon_fire"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventWeaponFire\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `Weapon` | `string` | get, set | 武器名称<br/>类型：字符串 |
| `Silenced` | `bool` | get, set | 是否武器已消音 <br/> 类型：布尔 |



---

<a id="eventweaponfireonempty"></a>

## 🔌 EventWeaponFireOnEmpty

事件 "weapon_fire_on_empty"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventWeaponFireOnEmpty\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `Weapon` | `string` | get, set | 武器名称<br/>类型：字符串 |



---

<a id="eventweaponreload"></a>

## 🔌 EventWeaponReload

事件 "weapon_reload"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventWeaponReload\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |



---

<a id="eventweaponzoom"></a>

## 🔌 EventWeaponZoom

事件 "weapon_zoom"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventWeaponZoom\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |



---

<a id="eventweaponzoomrifle"></a>

## 🔌 EventWeaponZoomRifle

事件 "weapon_zoom_rifle"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventWeaponZoomRifle\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |



---

<a id="eventweaponhudselection"></a>

## 🔌 EventWeaponhudSelection

事件 "weaponhud_selection"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventWeaponhudSelection\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 此事件适用的玩家 <br/> 类型: player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 此事件适用的玩家 <br/> 类型: player_controller_and_pawn |
| `UserId` | `int` | get, set | 此事件适用的玩家 <br/> 类型: player_controller_and_pawn |
| `Mode` | `byte` | get, set | EWeaponHudSelectionMode (切换 / 拾取 / 丢弃) <br/> 类型：byte |
| `EntIndex` | `int` | get, set | 武器实体索引<br/>类型：long |



---

<a id="eventwritegametitledata"></a>

## 🔌 EventWriteGameTitledata

事件 "write_game_titledata" 在个人资料中写入用户标题数据

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventWriteGameTitledata\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ControllerId` | `short` | get, set | 用户控制器ID<br/>类型: short |



---

<a id="eventwriteprofiledata"></a>

## 🔌 EventWriteProfileData

事件 "write_profile_data"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventWriteProfileData\>`



---

