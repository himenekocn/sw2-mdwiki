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

## 🔌 EventAchievementEarned

事件 "achievement_earned"（成就已获得）

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAchievementEarned\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlayerController` | `CCSPlayerController` | get | 玩家的实体索引 <br/> 类型：player_controller |
| `PlayerPawn` | `CCSPlayerPawn` | get | 玩家的实体索引 <br/> 类型：player_controller |
| `Player` | `int` | get, set | 玩家的实体索引 <br/> 类型：player_controller |
| `Achievement` | `short` | get, set | 成就 ID<br/>类型：short |



---

## 🔌 EventAchievementEarnedLocal

事件"achievement_earned_local"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAchievementEarnedLocal\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Achievement` | `short` | get, set | 成就 ID<br/>类型：short |
| `SplitScreenPlayer` | `short` | get, set | 分屏 ID<br/>类型：短整型（short） |



---

## 🔌 EventAchievementEvent

事件 "achievement_event"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAchievementEvent\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AchievementName` | `string` | get, set | 成就的非本地化名称<br/>类型：字符串 |
| `CurVal` | `short` | get, set | 达成目标所需的步数<br/>类型：短整型 |
| `MaxVal` | `short` | get, set | 成就中的总步数<br/>类型：short |



---

## 🔌 EventAchievementInfoLoaded

事件“成就信息已加载”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAchievementInfoLoaded\>`



---

## 🔌 EventAchievementWriteFailed

事件“成就写入失败”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAchievementWriteFailed\>`



---

## 🔌 EventAddBulletHitMarker

事件"add_bullet_hit_marker"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAddBulletHitMarker\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Bone` | `short` | get, set | 类型：短整型 |
| `PosX` | `short` | get, set | 类型：短整型 |
| `PosY` | `short` | get, set | 类型：短整型 |
| `PosZ` | `short` | get, set | 类型：短整型 |
| `AngX` | `short` | get, set | 类型：短整型 |
| `AngY` | `short` | get, set | 类型：短整型 |
| `AngZ` | `short` | get, set | 类型：短整型 |
| `StartX` | `short` | get, set | 类型：短整型 |
| `StartY` | `short` | get, set | 类型：短整型 |
| `StartZ` | `short` | get, set | 类型：短整型 |
| `Hit` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventAddPlayerSonarIcon

事件 "add_player_sonar_icon"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAddPlayerSonarIcon\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `PosX` | `float` | get, set | 类型：浮点数 |
| `PosY` | `float` | get, set | 类型：浮点数 |
| `PosZ` | `float` | get, set | 类型：浮点数 |



---

## 🔌 EventAmmoPickup

事件"ammo_pickup"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAmmoPickup\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Item` | `string` | get, set | 可以是诸如'tmp'或'hegrenade'的武器，也可以是诸如'nvgs'的物品<br/>类型：字符串 |
| `Index` | `int` | get, set | 武器实体索引<br/>类型：long |



---

## 🔌 EventAmmoRefill

事件"ammo_refill"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAmmoRefill\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Success` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventAnnouncePhaseEnd

事件“宣布阶段结束”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAnnouncePhaseEnd\>`



---

## 🔌 EventBeginNewMatch

事件"begin_new_match"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBeginNewMatch\>`



---

## 🔌 EventBombAbortdefuse

事件"bomb_abortdefuse"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombAbortdefuse\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 正在拆弹的玩家<br/>类型：player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 正在拆弹的玩家<br/>类型：player_controller_and_pawn |
| `UserId` | `int` | get, set | 正在拆弹的玩家<br/>类型：player_controller_and_pawn |



---

## 🔌 EventBombAbortplant

事件“炸弹拆除中止”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombAbortplant\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 正在安放炸弹的玩家<br/>类型：player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 正在安放炸弹的玩家<br/>类型：player_controller_and_pawn |
| `UserId` | `int` | get, set | 正在安放炸弹的玩家<br/>类型：player_controller_and_pawn |
| `Site` | `short` | get, set | 炸弹点索引<br/>类型：short |



---

## 🔌 EventBombBeep

事件 "bomb_beep"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombBeep\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntIndex` | `int` | get, set | c4 实体<br/>类型：long |



---

## 🔌 EventBombBegindefuse

事件 "bomb_begindefuse"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombBegindefuse\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 正在拆弹的玩家<br/>类型：player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 正在拆弹的玩家<br/>类型：player_controller_and_pawn |
| `UserId` | `int` | get, set | 正在拆弹的玩家<br/>类型：player_controller_and_pawn |
| `HasKit` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventBombBeginplant

事件 "bomb_beginplant"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombBeginplant\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 正在安放炸弹的玩家<br/>类型：player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 正在安放炸弹的玩家<br/>类型：player_controller_and_pawn |
| `UserId` | `int` | get, set | 正在安放炸弹的玩家<br/>类型：player_controller_and_pawn |
| `Site` | `short` | get, set | 炸弹点索引<br/>类型：short |



---

## 🔌 EventBombDefused

事件"bomb_defused"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombDefused\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 拆除炸弹的玩家<br/>类型：player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 拆除炸弹的玩家<br/>类型：player_controller_and_pawn |
| `UserId` | `int` | get, set | 拆除炸弹的玩家<br/>类型：player_controller_and_pawn |
| `Site` | `short` | get, set | 炸弹点索引<br/>类型：short |



---

## 🔌 EventBombDropped

事件 "bomb_dropped"（炸弹已投放）

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombDropped\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 投掷炸弹的玩家<br/>类型：player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 投掷炸弹的玩家<br/>类型：player_controller_and_pawn |
| `UserId` | `int` | get, set | 投掷炸弹的玩家<br/>类型：player_controller_and_pawn |
| `EntIndex` | `int` | get, set | 类型：long |



---

## 🔌 EventBombExploded

事件“炸弹爆炸”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombExploded\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 安放炸弹的玩家<br/>类型：player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 安放炸弹的玩家<br/>类型：player_controller_and_pawn |
| `UserId` | `int` | get, set | 安放炸弹的玩家<br/>类型：player_controller_and_pawn |
| `Site` | `short` | get, set | 炸弹点索引<br/>类型：short |



---

## 🔌 EventBombPickup

事件"bomb_pickup"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombPickup\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 拾起炸弹的玩家角色 <br/> 类型：player_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 拾起炸弹的玩家角色 <br/> 类型：player_pawn |
| `UserId` | `int` | get, set | 拾起炸弹的玩家角色 <br/> 类型：player_pawn |



---

## 🔌 EventBombPlanted

事件 "bomb_planted"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombPlanted\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 安放炸弹的玩家<br/>类型：player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 安放炸弹的玩家<br/>类型：player_controller_and_pawn |
| `UserId` | `int` | get, set | 安放炸弹的玩家<br/>类型：player_controller_and_pawn |
| `Site` | `short` | get, set | 炸弹点索引<br/>类型：short |



---

## 🔌 EventBonusUpdated

事件"bonus_updated"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBonusUpdated\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `NumAdvanced` | `short` | get, set | 类型：短整型 |
| `NumBronze` | `short` | get, set | 类型：短整型 |
| `NumSilver` | `short` | get, set | 类型：短整型 |
| `NumGold` | `short` | get, set | 类型：短整型 |



---

## 🔌 EventBotTakeover

事件"bot_takeover"

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
| `P` | `float` | get, set | 类型：浮点数 |
| `Y` | `float` | get, set | 类型：浮点数 |
| `R` | `float` | get, set | 类型：浮点数 |



---

## 🔌 EventBreakBreakable

事件 "break_breakable"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBreakBreakable\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntIndex` | `int` | get, set | 类型：long |
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家生命体 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家生命体 |
| `UserId` | `int` | get, set | 类型：玩家生命体 |
| `Material` | `byte` | get, set | BREAK_GLASS、BREAK_WOOD 等 <br/>类型：byte |



---

## 🔌 EventBreakProp

事件 "break_prop"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBreakProp\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntIndex` | `int` | get, set | 类型：long |
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家生命体 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家生命体 |
| `UserId` | `int` | get, set | 类型：玩家生命体 |
| `PlayerHeld` | `bool` | get, set | 类型：布尔值 |
| `PlayerThrown` | `bool` | get, set | 类型：布尔值 |
| `PlayerDropped` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventBrokenBreakable

事件 "broken_breakable"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBrokenBreakable\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntIndex` | `int` | get, set | 类型：long |
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家生命体 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家生命体 |
| `UserId` | `int` | get, set | 类型：玩家生命体 |
| `Material` | `byte` | get, set | BREAK_GLASS、BREAK_WOOD 等 <br/>类型：byte |



---

## 🔌 EventBulletDamage

事件“子弹伤害”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBulletDamage\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `VictimController` | `CCSPlayerController` | get | 受伤玩家索引<br/>类型：player_controller_and_pawn |
| `VictimPawn` | `CCSPlayerPawn` | get | 受伤玩家索引<br/>类型：player_controller_and_pawn |
| `Victim` | `int` | get, set | 受伤玩家索引<br/>类型：player_controller_and_pawn |
| `AttackerController` | `CCSPlayerController` | get | 攻击者的玩家索引<br/>类型：player_controller_and_pawn |
| `AttackerPawn` | `CCSPlayerPawn` | get | 攻击者的玩家索引<br/>类型：player_controller_and_pawn |
| `Attacker` | `int` | get, set | 攻击者的玩家索引<br/>类型：player_controller_and_pawn |
| `Distance` | `float` | get, set | 子弹在击中玩家前飞行的距离<br/>类型：float |
| `DamageDirX` | `float` | get, set | 子弹的方向向量<br/>类型：float |
| `DamageDirY` | `float` | get, set | 子弹的方向向量<br/>类型：float |
| `DamageDirZ` | `float` | get, set | 子弹的方向向量<br/>类型：float |
| `NumPenetrations` | `byte` | get, set | 穿透的表面数量 <br/> 类型：字节 |
| `NoScope` | `bool` | get, set | 射击者是否使用了消音器？<br/>类型：布尔值 |
| `InAir` | `bool` | get, set | 射手是否在跳跃？<br/> 类型：布尔值 |
| `ShootAngX` | `float` | get, set | 射击角度 X<br/>类型：浮点数 |
| `ShootAngY` | `float` | get, set | 射击角度 Y<br/>类型：浮点数 |
| `ShootAngZ` | `float` | get, set | 射击角度 Z<br/>类型：浮点数 |
| `AimPunchX` | `float` | get, set | 瞄准后坐力 X<br/>类型：float |
| `AimPunchY` | `float` | get, set | 瞄准后坐力 Y <br/> 类型：浮点数 |
| `AimPunchZ` | `float` | get, set | 目标打击角度 <br/> 类型：浮点数 |
| `AttackTickCount` | `int` | get, set | 攻击刻 <br/> 类型：int |
| `AttackTickFrac` | `float` | get, set | 攻击进度 <br/> 类型：float |
| `RenderTickCount` | `int` | get, set | 渲染刻 <br/> 类型：整数 |
| `RenderTickFrac` | `float` | get, set | 渲染分数<br/>类型：浮点数 |
| `InaccuracyTotal` | `float` | get, set | 总偏差 <br/> 类型：浮点数 |
| `InaccuracyMove` | `float` | get, set | 移动精度误差<br/>类型：float |
| `InaccuracyAir` | `float` | get, set | 空气不精准度<br/>类型：浮点数 |
| `RecoilIndex` | `float` | get, set | 后坐力索引。是的，这确实是一个浮点数。<br/>类型：float |
| `Type` | `int` | get, set | 延迟补偿类型 <br/> 类型：int |



---

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
| `X` | `float` | get, set | 类型：浮点数 |
| `Y` | `float` | get, set | 类型：浮点数 |
| `Z` | `float` | get, set | 类型：浮点数 |



---

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

## 🔌 EventBuymenuOpen

事件"buymenu_open"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBuymenuOpen\>`



---

## 🔌 EventBuytimeEnded

事件 "buytime_ended"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBuytimeEnded\>`



---

## 🔌 EventCartUpdated

事件"cart_updated"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCartUpdated\>`



---

## 🔌 EventChoppersIncomingWarning

事件"choppers_incoming_warning"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventChoppersIncomingWarning\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Global` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventClientDisconnect

事件"client_disconnect"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventClientDisconnect\>`



---

## 🔌 EventClientLoadoutChanged

事件“客户端装备配置已更改”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventClientLoadoutChanged\>`



---

## 🔌 EventClientsideLessonClosed

事件 "客户端课程已关闭"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventClientsideLessonClosed\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `LessonName` | `string` | get, set | 类型：字符串 |



---

## 🔌 EventClientsideReloadCustomEcon

事件 "客户端端重新加载自定义经济"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventClientsideReloadCustomEcon\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SteamID` | `string` | get, set | 类型：字符串 |



---

## 🔌 EventCoreGameEvents

事件：“核心游戏事件”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCoreGameEvents\>`



---

## 🔌 EventCsGameDisconnected

事件"cs_game_disconnected"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCsGameDisconnected\>`



---

## 🔌 EventCsIntermission

事件"cs_intermission"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCsIntermission\>`



---

## 🔌 EventCsMatchEndRestart

事件"cs_match_end_restart"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCsMatchEndRestart\>`



---

## 🔌 EventCsPreRestart

事件"cs_pre_restart"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCsPreRestart\>`



---

## 🔌 EventCsPrevNextSpectator

事件"cs_prev_next_spectator"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCsPrevNextSpectator\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Next` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventCsRoundFinalBeep

事件 "cs_round_final_beep"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCsRoundFinalBeep\>`



---

## 🔌 EventCsRoundStartBeep

事件"cs_round_start_beep"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCsRoundStartBeep\>`



---

## 🔌 EventCsWinPanelMatch

事件"cs_win_panel_match"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCsWinPanelMatch\>`



---

## 🔌 EventCsWinPanelRound

事件"cs_win_panel_round"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCsWinPanelRound\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ShowTimerDefend` | `bool` | get, set | 类型：布尔值 |
| `ShowTimerAttack` | `bool` | get, set | 类型：布尔值 |
| `TimerTime` | `short` | get, set | 类型：短整型 |
| `FinalEvent` | `byte` | get, set | 在 cs_gamerules.h 中定义<br/>类型：字节 |
| `FunfactToken` | `string` | get, set | 类型：字符串 |
| `FunfactPlayerController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `FunfactPlayerPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `FunfactPlayer` | `int` | get, set | 类型：玩家控制器 |
| `FunfactData1` | `int` | get, set | 类型：long |
| `FunfactData2` | `int` | get, set | 类型：long |
| `FunfactData3` | `int` | get, set | 类型：long |



---

## 🔌 EventCstrikeevents

事件"cstrikeevents"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCstrikeevents\>`



---

## 🔌 EventDecoyDetonate

事件"decoy_detonate"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDecoyDetonate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `EntityID` | `short` | get, set | 类型：短整型 |
| `X` | `float` | get, set | 类型：浮点数 |
| `Y` | `float` | get, set | 类型：浮点数 |
| `Z` | `float` | get, set | 类型：浮点数 |



---

## 🔌 EventDecoyFiring

事件"decoy_firing"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDecoyFiring\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `EntityID` | `short` | get, set | 类型：短整型 |
| `X` | `float` | get, set | 类型：浮点数 |
| `Y` | `float` | get, set | 类型：浮点数 |
| `Z` | `float` | get, set | 类型：浮点数 |



---

## 🔌 EventDecoyStarted

事件"投掷闪光弹开始”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDecoyStarted\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家生命体 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家生命体 |
| `UserId` | `int` | get, set | 类型：玩家生命体 |
| `EntityID` | `short` | get, set | 类型：短整型 |
| `X` | `float` | get, set | 类型：浮点数 |
| `Y` | `float` | get, set | 类型：浮点数 |
| `Z` | `float` | get, set | 类型：浮点数 |



---

## 🔌 EventDefuserDropped

事件 "defuser_dropped"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDefuserDropped\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityID` | `int` | get, set | 拆弹者的实体 ID<br/>类型：long |



---

## 🔌 EventDefuserPickup

事件 "拆弹器拾取"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDefuserPickup\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityID` | `int` | get, set | 拆弹者的实体 ID<br/>类型：long |
| `UserIdController` | `CCSPlayerController` | get | 拾取拆弹器的玩家<br/>类型：player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 拾取拆弹器的玩家<br/>类型：player_controller_and_pawn |
| `UserId` | `int` | get, set | 拾取拆弹器的玩家<br/>类型：player_controller_and_pawn |



---

## 🔌 EventDemoSkip

事件"demo_skip"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDemoSkip\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlaybackTick` | `int` | get, set | 当前播放的 tick（游戏帧）<br/>类型：long |
| `SkiptoTick` | `int` | get, set | tick 表示游戏逻辑更新次数，类型为 long（长整型） |



---

## 🔌 EventDemoStart

事件 "demo_start"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDemoStart\>`



---

## 🔌 EventDemoStop

事件"demo_stop"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDemoStop\>`



---

## 🔌 EventDifficultyChanged

事件"difficulty_changed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDifficultyChanged\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `NewDifficulty` | `short` | get, set | 类型：短整型 |
| `OldDifficulty` | `short` | get, set | 类型：短整型 |
| `StrDifficulty` | `string` | get, set | 新的难度（作为字符串）<br/>类型：字符串 |



---

## 🔌 EventDmBonusWeaponStart

事件 "dm_bonus_weapon_start"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDmBonusWeaponStart\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Time` | `short` | get, set | 该奖励持续的时间长度<br/>类型：short |
| `Pos` | `short` | get, set | 奖励武器的装备槽位置<br/>类型：短整型 |



---

## 🔌 EventDoorBreak

事件 "door_break"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDoorBreak\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntIndex` | `int` | get, set | 类型：long |
| `DMgState` | `int` | get, set | 类型：long |



---

## 🔌 EventDoorClose

事件 "door_close"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDoorClose\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 谁关上了门<br/>类型：玩家pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 谁关上了门<br/>类型：玩家pawn |
| `UserId` | `int` | get, set | 谁关上了门<br/>类型：玩家pawn |
| `Checkpoint` | `bool` | get, set | 门是否为检查点门<br/>类型：布尔值 |



---

## 🔌 EventDoorClosed

事件“门已关闭”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDoorClosed\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 谁关上了门<br/>类型：玩家pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 谁关上了门<br/>类型：玩家pawn |
| `UserId` | `int` | get, set | 谁关上了门<br/>类型：玩家pawn |
| `EntIndex` | `int` | get, set | 类型：long |



---

## 🔌 EventDoorMoving

事件“door_moving"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDoorMoving\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `EntIndex` | `int` | get, set | 类型：long |



---

## 🔌 EventDoorOpen

事件 "door_open"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDoorOpen\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 谁关上了门<br/>类型：玩家pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 谁关上了门<br/>类型：玩家pawn |
| `UserId` | `int` | get, set | 谁关上了门<br/>类型：玩家pawn |
| `EntIndex` | `int` | get, set | 类型：long |



---

## 🔌 EventDroneAboveRoof

事件"drone_above_roof"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDroneAboveRoof\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Cargo` | `short` | get, set | 类型：短整型 |



---

## 🔌 EventDroneCargoDetached

事件 "drone_cargo_detached"（无人机货物已分离）

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDroneCargoDetached\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Cargo` | `short` | get, set | 类型：短整型 |
| `Delivered` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventDroneDispatched

事件"drone_dispatched"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDroneDispatched\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Priority` | `short` | get, set | 类型：短整型 |
| `DroneDispatched` | `short` | get, set | 类型：短整型 |



---

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

## 🔌 EventDropRateModified

事件"drop_rate_modified"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDropRateModified\>`



---

## 🔌 EventDynamicShadowLightChanged

事件 "dynamic_shadow_light_changed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDynamicShadowLightChanged\>`



---

## 🔌 EventDzItemInteraction

事件 "dz_item_interaction"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDzItemInteraction\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 玩家实体索引<br/>类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 玩家实体索引<br/>类型：玩家控制器 |
| `UserId` | `int` | get, set | 玩家实体索引<br/>类型：玩家控制器 |
| `Subject` | `short` | get, set | 木箱实体索引<br/>类型：短整型 |
| `Type` | `string` | get, set | 箱子的类型（金属、木质或空投）<br/> type: string |



---

## 🔌 EventEnableRestartVoting

事件"enable_restart_voting"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventEnableRestartVoting\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Enable` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventEndmatchCmmStartRevealItems

事件 "endmatch_cmm_start_reveal_items"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventEndmatchCmmStartRevealItems\>`



---

## 🔌 EventEndmatchMapvoteSelectingMap

事件"endmatch_mapvote_selecting_map"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventEndmatchMapvoteSelectingMap\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Count` | `byte` | get, set | “平局”数量<br/>类型：字节 |
| `Slot1` | `byte` | get, set | 类型：字节 |
| `Slot2` | `byte` | get, set | 类型：字节 |
| `Slot3` | `byte` | get, set | 类型：字节 |
| `Slot4` | `byte` | get, set | 类型：字节 |
| `Slot5` | `byte` | get, set | 类型：字节 |
| `Slot6` | `byte` | get, set | 类型：字节 |
| `Slot7` | `byte` | get, set | 类型：字节 |
| `Slot8` | `byte` | get, set | 类型：字节 |
| `Slot9` | `byte` | get, set | 类型：字节 |
| `Slot10` | `byte` | get, set | 类型：字节 |



---

## 🔌 EventEnterBombzone

事件"enter_bombzone"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventEnterBombzone\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `HasBomb` | `bool` | get, set | 类型：布尔值 |
| `IsPlanted` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventEnterBuyzone

事件"enter_buyzone"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventEnterBuyzone\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `CanBuy` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventEnterRescueZone

事件“进入救援区域”

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

## 🔌 EventEntityKilled

事件 "entity_killed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventEntityKilled\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntindexKilled` | `int` | get, set | 类型：long |
| `EntindexAttacker` | `int` | get, set | 类型：long |
| `EntindexInflictor` | `int` | get, set | 类型：long |
| `DamageBits` | `int` | get, set | 类型：long |



---

## 🔌 EventEntityVisible

事件"entity_visible"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventEntityVisible\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 能够看到该实体的玩家<br/>类型：player_controller |
| `UserIdPawn` | `CCSPlayerPawn` | get | 能够看到该实体的玩家<br/>类型：player_controller |
| `UserId` | `int` | get, set | 能够看到该实体的玩家<br/>类型：player_controller |
| `Subject` | `int` | get, set | 它们所见的实体的实体索引 <br/> 类型：长整型 |
| `ClassName` | `string` | get, set | 他们所见实体的类名 <br/> 类型：字符串 |
| `EntityName` | `string` | get, set | 他们看到的实体的名称<br/>类型：字符串 |



---

## 🔌 EventEventTicketModified

事件 "event_ticket_modified"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventEventTicketModified\>`



---

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
| `HasBomb` | `bool` | get, set | 类型：布尔值 |
| `IsPlanted` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventExitBuyzone

事件“退出购买区域”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventExitBuyzone\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `CanBuy` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventExitRescueZone

事件 "exit_rescue_zone"

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

## 🔌 EventFinaleStart

事件"finale_start"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventFinaleStart\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Rushes` | `short` | get, set | 类型：短整型 |



---

## 🔌 EventFirstbombsIncomingWarning

事件"firstbombs_incoming_warning"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventFirstbombsIncomingWarning\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Global` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventFlareIgniteNpc

事件"flare_ignite_npc"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventFlareIgniteNpc\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntIndex` | `int` | get, set | 实体已点燃<br/>类型：长整型 |



---

## 🔌 EventFlashbangDetonate

事件 "闪光弹引爆"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventFlashbangDetonate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `EntityID` | `short` | get, set | 类型：短整型 |
| `X` | `float` | get, set | 类型：浮点数 |
| `Y` | `float` | get, set | 类型：浮点数 |
| `Z` | `float` | get, set | 类型：浮点数 |



---

## 🔌 EventGameEnd

事件"game_end"：游戏结束

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGameEnd\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Winner` | `byte` | get, set | 获胜方队伍/用户 ID <br/> 类型：byte |



---

## 🔌 EventGameInit

当新游戏启动时发送"game_init"事件

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGameInit\>`



---

## 🔌 EventGameMessage

事件 "game_message"：由游戏逻辑向所有玩家发送的消息

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGameMessage\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Target` | `byte` | get, set | 0 = 控制台，1 = HUD <br/> 类型：字节 |
| `Text` | `string` | get, set | 消息文本<br/>类型：字符串 |



---

## 🔌 EventGameNewmap

事件 "game_newmap" 在新地图完全加载时发送。

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGameNewmap\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MapName` | `string` | get, set | 地图名称<br/>类型：字符串 |
| `Transition` | `bool` | get, set | 若此为从一张地图过渡到另一张地图，则为 true <br/> 类型：布尔值 |



---

## 🔌 EventGamePhaseChanged

事件 "game_phase_changed"（游戏阶段变更）

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGamePhaseChanged\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `NewPhase` | `short` | get, set | 类型：短整型 |



---

## 🔌 EventGameStart

事件 "game_start"：新游戏开始

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGameStart\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `RoundsLimit` | `int` | get, set | 最大回合数<br/>类型：long |
| `TimeLimit` | `int` | get, set | 时间限制<br/>类型：long |
| `FragLimit` | `int` | get, set | 击杀数上限<br/>类型：long |
| `Objective` | `string` | get, set | 回合目标<br/>类型：字符串 |



---

## 🔌 EventGameevents

事件 "gameevents"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGameevents\>`



---

## 🔌 EventGameinstructorDraw

事件"gameinstructor_draw"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGameinstructorDraw\>`



---

## 🔌 EventGameinstructorNodraw

事件 "gameinstructor_nodraw"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGameinstructorNodraw\>`



---

## 🔌 EventGameuiHidden

事件 "gameui_hidden"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGameuiHidden\>`



---

## 🔌 EventGcConnected

事件 "gc_connected"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGcConnected\>`



---

## 🔌 EventGgKilledEnemy

事件 "gg_killed_enemy"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGgKilledEnemy\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `VictimIDController` | `CCSPlayerController` | get | 死亡玩家的用户 ID<br/>类型：player_controller |
| `VictimIDPawn` | `CCSPlayerPawn` | get | 死亡玩家的用户 ID<br/>类型：player_controller |
| `VictimID` | `int` | get, set | 死亡玩家的用户 ID<br/>类型：player_controller |
| `AttackerIDController` | `CCSPlayerController` | get | 击杀者的用户 ID<br/>类型：player_controller |
| `AttackerIDPawn` | `CCSPlayerPawn` | get | 击杀者的用户 ID<br/>类型：player_controller |
| `AttackerID` | `int` | get, set | 击杀者的用户 ID<br/>类型：player_controller |
| `Dominated` | `short` | get, set | 该击杀是否使凶手支配了受害者 <br/> 类型：short |
| `Revenge` | `short` | get, set | 该击杀是否使杀手对受害者进行了复仇 <br/> 类型：short |
| `Bonus` | `bool` | get, set | 杀手是否使用附带武器击杀？<br/>类型：布尔值 |



---

## 🔌 EventGrenadeBounce

事件"grenade_bounce"

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

## 🔌 EventGrenadeThrown

事件"grenade_thrown"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGrenadeThrown\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `Weapon` | `string` | get, set | 武器名称，类型：字符串 |



---

## 🔌 EventGuardianWaveRestart

事件"guardian_wave_restart"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGuardianWaveRestart\>`



---

## 🔌 EventHegrenadeDetonate

事件 "hegrenade_detonate"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHegrenadeDetonate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `EntityID` | `short` | get, set | 类型：短整型 |
| `X` | `float` | get, set | 类型：浮点数 |
| `Y` | `float` | get, set | 类型：浮点数 |
| `Z` | `float` | get, set | 类型：浮点数 |



---

## 🔌 EventHelicopterGrenadePuntMiss

事件"helicopter_grenade_punt_miss"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHelicopterGrenadePuntMiss\>`



---

## 🔌 EventHideDeathpanel

事件 "hide_deathpanel"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHideDeathpanel\>`



---

## 🔌 EventHltvCameraman

事件"hltv_cameraman"：一名观众/玩家担任摄像师

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvCameraman\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 摄像机操作者实体索引<br/>类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 摄像机操作者实体索引<br/>类型：玩家控制器 |
| `UserId` | `int` | get, set | 摄像机操作者实体索引<br/>类型：玩家控制器 |



---

## 🔌 EventHltvChangedMode

事件"hltv_changed_mode"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvChangedMode\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `OldMode` | `int` | get, set | 类型：long |
| `NewMode` | `int` | get, set | 类型：long |
| `ObsTarget` | `int` | get, set | 类型：long |



---

## 🔌 EventHltvChase

事件"hltv_chase"：单个实体的镜头

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvChase\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Target1Controller` | `CCSPlayerController` | get | 主目标索引<br/>类型：player_controller |
| `Target1Pawn` | `CCSPlayerPawn` | get | 主目标索引<br/>类型：player_controller |
| `Target1` | `int` | get, set | 主目标索引<br/>类型：player_controller |
| `Target2Controller` | `CCSPlayerController` | get | 次要目标索引或为 0<br/>类型：玩家控制器 |
| `Target2Pawn` | `CCSPlayerPawn` | get | 次要目标索引或为 0<br/>类型：玩家控制器 |
| `Target2` | `int` | get, set | 次要目标索引或为 0<br/>类型：玩家控制器 |
| `Distance` | `short` | get, set | 相机距离<br/>类型：短整型（short） |
| `Theta` | `short` | get, set | 视角水平角度<br/>类型：短整型 |
| `Phi` | `short` | get, set | 视图角垂直 <br/> 类型：short |
| `Inertia` | `byte` | get, set | 相机惯性<br/>类型：字节 |
| `InEye` | `byte` | get, set | 导演建议显示在眼睛中<br/>类型：字节 |



---

## 🔌 EventHltvChat

事件"hltv_chat"：由观众发送的HLTV聊天消息

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvChat\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Text` | `string` | get, set | 类型：字符串 |
| `SteamID` | `ulong` | get, set | Steam ID<br/>类型：uint64 |



---

## 🔌 EventHltvFixed

事件"hltv_fixed"从固定视角显示

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvFixed\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PosX` | `int` | get, set | 世界中的相机位置<br/>类型：长整型（long） |
| `Posy` | `int` | get, set | 类型：long |
| `PosZ` | `int` | get, set | 类型：long |
| `Theta` | `short` | get, set | 相机角度<br/>类型：short |
| `Phi` | `short` | get, set | 类型：短整型 |
| `Offset` | `short` | get, set | 类型：短整型 |
| `FOv` | `float` | get, set | 类型：浮点数 |
| `TargetController` | `CCSPlayerController` | get | 跟随此玩家<br/>类型：player_controller |
| `TargetPawn` | `CCSPlayerPawn` | get | 跟随此玩家<br/>类型：player_controller |
| `Target` | `int` | get, set | 跟随此玩家<br/>类型：player_controller |



---

## 🔌 EventHltvMessage

事件"hltv_message"：由管理员发送的 HLTV 消息

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvMessage\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Text` | `string` | get, set | 类型：字符串 |



---

## 🔌 EventHltvRankCamera

事件"hltv_rank_camera"：一个用于排名视角的相机

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvRankCamera\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Index` | `byte` | get, set | 固定摄像机索引<br/>类型：byte |
| `Rank` | `float` | get, set | 排名：此摄像机视角的趣味性如何<br/>类型：浮点数 |
| `TargetController` | `CCSPlayerController` | get | 最佳/最近的目标实体<br/>类型：player_controller |
| `TargetPawn` | `CCSPlayerPawn` | get | 最佳/最近的目标实体<br/>类型：player_controller |
| `Target` | `int` | get, set | 最佳/最近的目标实体<br/>类型：player_controller |



---

## 🔌 EventHltvRankEntity

事件"hltv_rank_entity"：实体排名

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvRankEntity\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 玩家插槽 <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 玩家插槽 <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 玩家插槽 <br/> 类型：玩家控制器 |
| `Rank` | `float` | get, set | 排名：该实体值得查看的有趣程度 <br/> 类型：浮点数 |
| `TargetController` | `CCSPlayerController` | get | 最佳/最近的目标实体<br/>类型：player_controller |
| `TargetPawn` | `CCSPlayerPawn` | get | 最佳/最近的目标实体<br/>类型：player_controller |
| `Target` | `int` | get, set | 最佳/最近的目标实体<br/>类型：player_controller |



---

## 🔌 EventHltvReplay

事件"hltv_replay"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvReplay\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Delay` | `int` | get, set | 杀手回放延迟中的秒数<br/>类型：long |
| `Reason` | `int` | get, set | 重播原因（ReplayEventType_t）<br/>类型：long |



---

## 🔌 EventHltvReplayStatus

事件"hltv_replay_status"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvReplayStatus\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Reason` | `int` | get, set | HLTV 回放状态变更的原因（类型：long） |



---

## 🔌 EventHltvStatus

事件"hltv_status"：通用 HLTV 状态

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvStatus\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Clients` | `int` | get, set | HLTV 观战者数量<br/>类型：long |
| `Slots` | `int` | get, set | HLTV 席位数量<br/>类型：long |
| `Proxies` | `short` | get, set | HLTV 代理的数量<br/>类型：短整型 |
| `Master` | `string` | get, set | 分派主服务器 IP:端口 <br/> 类型：字符串 |



---

## 🔌 EventHltvTitle

事件"hltv_title"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvTitle\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Text` | `string` | get, set | 类型：字符串 |



---

## 🔌 EventHltvVersioninfo

事件 "hltv_versioninfo"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvVersioninfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Version` | `int` | get, set | 类型：long |



---

## 🔌 EventHostageCallForHelp

事件“人质呼救”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHostageCallForHelp\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Hostage` | `short` | get, set | 人质实体索引<br/>类型：短整型 |



---

## 🔌 EventHostageFollows

事件"人质跟随”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHostageFollows\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 触碰人质的玩家<br/>类型：player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 触碰人质的玩家<br/>类型：player_controller_and_pawn |
| `UserId` | `int` | get, set | 触碰人质的玩家<br/>类型：player_controller_and_pawn |
| `Hostage` | `short` | get, set | 人质实体索引<br/>类型：短整型 |



---

## 🔌 EventHostageHurt

事件"人质受伤”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHostageHurt\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 伤害人质的玩家 <br/> 类型：player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 伤害人质的玩家 <br/> 类型：player_controller_and_pawn |
| `UserId` | `int` | get, set | 伤害人质的玩家 <br/> 类型：player_controller_and_pawn |
| `Hostage` | `short` | get, set | 人质实体索引<br/>类型：短整型 |



---

## 🔌 EventHostageKilled

事件“人质被击杀”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHostageKilled\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 击杀人质的玩家 <br/> 类型：player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 击杀人质的玩家 <br/> 类型：player_controller_and_pawn |
| `UserId` | `int` | get, set | 击杀人质的玩家 <br/> 类型：player_controller_and_pawn |
| `Hostage` | `short` | get, set | 人质实体索引<br/>类型：短整型 |



---

## 🔌 EventHostageRescued

事件“人质被解救”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHostageRescued\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 成功解救人质的玩家<br/>类型：player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 成功解救人质的玩家<br/>类型：player_controller_and_pawn |
| `UserId` | `int` | get, set | 成功解救人质的玩家<br/>类型：player_controller_and_pawn |
| `Hostage` | `short` | get, set | 人质实体索引<br/>类型：短整型 |
| `Site` | `short` | get, set | 救援站点索引<br/>类型：short |



---

## 🔌 EventHostageRescuedAll

事件"hostage_rescued_all"（人质全部获救）

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHostageRescuedAll\>`



---

## 🔌 EventHostageStopsFollowing

事件 "人质停止跟随"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHostageStopsFollowing\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 成功解救人质的玩家<br/>类型：player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 成功解救人质的玩家<br/>类型：player_controller_and_pawn |
| `UserId` | `int` | get, set | 成功解救人质的玩家<br/>类型：player_controller_and_pawn |
| `Hostage` | `short` | get, set | 人质实体索引<br/>类型：短整型 |



---

## 🔌 EventHostnameChanged

事件 "hostname_changed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHostnameChanged\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Hostname` | `string` | get, set | 类型：字符串 |



---

## 🔌 EventInfernoExpire

事件 "inferno_expire"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventInfernoExpire\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityID` | `short` | get, set | 类型：短整型 |
| `X` | `float` | get, set | 类型：浮点数 |
| `Y` | `float` | get, set | 类型：浮点数 |
| `Z` | `float` | get, set | 类型：浮点数 |



---

## 🔌 EventInfernoExtinguish

事件"inferno_extinguish"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventInfernoExtinguish\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityID` | `short` | get, set | 类型：短整型 |
| `X` | `float` | get, set | 类型：浮点数 |
| `Y` | `float` | get, set | 类型：浮点数 |
| `Z` | `float` | get, set | 类型：浮点数 |



---

## 🔌 EventInfernoStartburn

事件 "inferno_startburn"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventInfernoStartburn\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityID` | `short` | get, set | 类型：短整型 |
| `X` | `float` | get, set | 类型：浮点数 |
| `Y` | `float` | get, set | 类型：浮点数 |
| `Z` | `float` | get, set | 类型：浮点数 |



---

## 🔌 EventInspectWeapon

事件"inspect_weapon"

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

## 🔌 EventInstructorCloseLesson

事件 "instructor_close_lesson"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventInstructorCloseLesson\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 本教程的目标玩家<br/>类型：player_controller |
| `UserIdPawn` | `CCSPlayerPawn` | get | 本教程的目标玩家<br/>类型：player_controller |
| `UserId` | `int` | get, set | 本教程的目标玩家<br/>类型：player_controller |
| `HintName` | `string` | get, set | 要启动的课程名称。必须与 instructor_lesson.txt 匹配 <br/> 类型：字符串 |



---

## 🔌 EventInstructorServerHintCreate

事件 "instructor_server_hint_create" 使用完全由服务器或地图提供的数据创建提示。该提示旨在在内容尚未就绪、无需依赖此提示之前，优化测试流程以辅助游戏调试。**严禁将其作为可发布版本的临时补救措施**。

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventInstructorServerHintCreate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 触发提示的玩家的用户 ID<br/>类型：player_controller |
| `UserIdPawn` | `CCSPlayerPawn` | get | 触发提示的玩家的用户 ID<br/>类型：player_controller |
| `UserId` | `int` | get, set | 触发提示的玩家的用户 ID<br/>类型：player_controller |
| `HintEntindex` | `int` | get, set | 触发该事件的 env_instructor_hint 实体的 ID <br/>类型：long |
| `HintName` | `string` | get, set | 提示的命名，用于后续再次引用该提示（例如，针对该提示使用击杀命令而非超时）<br/>类型：字符串 |
| `HintReplaceKey` | `string` | get, set | 消息类型，使得相同类型的消息会相互替换<br/>类型：字符串 |
| `HintTarget` | `int` | get, set | 应显示提示的目标实体 ID<br/>类型：long |
| `HintActivatorUseridController` | `CCSPlayerController` | get | 激活者的玩家槽位<br/>类型：player_controller |
| `HintActivatorUseridPawn` | `CCSPlayerPawn` | get | 激活者的玩家槽位<br/>类型：player_controller |
| `HintActivatorUserid` | `int` | get, set | 激活者的玩家槽位<br/>类型：player_controller |
| `HintTimeout` | `short` | get, set | 提示自动超时的秒数，0 表示永不超时<br/>类型：short |
| `HintIconOnscreen` | `string` | get, set | 当提示在屏幕上显示时要使用的提示图标。例如："icon_alert_red" <br/> 类型：字符串 |
| `HintIconOffscreen` | `string` | get, set | 当提示位于屏幕外时应使用的提示图标。例如："icon_alert" <br/> 类型：字符串 |
| `HintCaption` | `string` | get, set | 提示标题，例如："#ThisIsDangerous" <br/> 类型：字符串 |
| `HintActivatorCaption` | `string` | get, set | 仅由激活者可见的提示标题，例如"#YouPushedItGood"<br/>类型：字符串 |
| `HintColor` | `string` | get, set | "r,g,b"格式中的提示颜色，其中每个分量的范围为0-255 <br/> 类型：字符串 |
| `HintIconOffset` | `float` | get, set | 提示在 Z 轴上相对于实体原点的偏移距离 <br/> 类型：float |
| `HintRange` | `float` | get, set | 提示被剔除前的范围<br/>类型：float |
| `HintFlags` | `int` | get, set | 提示标志<br/>类型：long |
| `HintBinding` | `string` | get, set | 当使用绑定为屏幕图标时使用的绑定 <br/> 类型：字符串 |
| `HintAllowNodrawTarget` | `bool` | get, set | 如果为 false，当目标实体不可见时提示将消失 <br/> 类型：布尔值 |
| `HintNooffscreen` | `bool` | get, set | 如果为 true，则在玩家视野外时不显示提示<br/>类型：布尔值 |
| `HintForcecaption` | `bool` | get, set | 若为 true，即使提示被遮挡，提示说明仍将显示<br/>类型：布尔值 |
| `HintLocalPlayerOnly` | `bool` | get, set | 若为 true，则仅本地玩家能看到提示<br/>类型：bool |
| `HintStartSound` | `string` | get, set | 要播放的游戏音效<br/>类型：字符串 |
| `HintLayoutfile` | `string` | get, set | Panorama 布局文件的路径<br/>类型：字符串 |
| `HintVrPanelType` | `short` | get, set | Panorama 面板的附件类型<br/>类型：short |
| `HintVrHeightOffset` | `float` | get, set | 附着面板的高度偏移量<br/>类型：float |
| `HintVrOffsetX` | `float` | get, set | 附加面板的偏移量<br/>类型：浮点数 |
| `HintVrOffsetY` | `float` | get, set | 附加面板的偏移量<br/>类型：浮点数 |
| `HintVrOffsetZ` | `float` | get, set | 附加面板的偏移量<br/>类型：浮点数 |
| `HintGamepadBinding` | `string` | get, set | 当 use_binding 为屏幕图标时，要使用的游戏手柄绑定 <br/> 类型：字符串 |



---

## 🔌 EventInstructorServerHintStop

事件"instructor_server_hint_stop"销毁服务器/地图创建的提示

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventInstructorServerHintStop\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `HintName` | `string` | get, set | 停止提示。将停止所有具有此名称的提示<br/>类型：字符串 |
| `HintEntindex` | `int` | get, set | 触发该事件的 env_instructor_hint 实体的 ID <br/>类型：long |



---

## 🔌 EventInstructorStartLesson

事件 "instructor_start_lesson"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventInstructorStartLesson\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 本教程的目标玩家<br/>类型：player_controller |
| `UserIdPawn` | `CCSPlayerPawn` | get | 本教程的目标玩家<br/>类型：player_controller |
| `UserId` | `int` | get, set | 本教程的目标玩家<br/>类型：player_controller |
| `HintName` | `string` | get, set | 要启动的课程名称。必须与 instructor_lesson.txt 匹配 <br/> 类型：字符串 |
| `HintTarget` | `int` | get, set | 该提示应显示的目标实体 ID。若控制器目标为空，则留空。<br/>类型：long |
| `VrMovementType` | `byte` | get, set | 类型：字节 |
| `VrSingleController` | `bool` | get, set | 类型：布尔值 |
| `VrControllerType` | `byte` | get, set | 类型：字节 |



---

## 🔌 EventInventoryUpdated

事件 "inventory_updated"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventInventoryUpdated\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ItemDef` | `short` | get, set | 类型：短整型 |
| `Itemid` | `int` | get, set | 类型：long |



---

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
| `Item` | `string` | get, set | 可以是诸如'tmp'或'hegrenade'的武器，也可以是诸如'nvgs'的物品<br/>类型：字符串 |
| `DefIndex` | `int` | get, set | 类型：long |
| `CanZoom` | `bool` | get, set | 类型：布尔值 |
| `HasSilencer` | `bool` | get, set | 类型：布尔值 |
| `IsSilenced` | `bool` | get, set | 类型：布尔值 |
| `HasTracers` | `bool` | get, set | 类型：布尔值 |
| `WepType` | `short` | get, set | 类型：短整型 |
| `IsPainted` | `bool` | get, set | 类型：布尔值 |



---

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
| `Item` | `string` | get, set | 可以是诸如'tmp'或'hegrenade'的武器，也可以是诸如'nvgs'的物品<br/>类型：字符串 |
| `Silent` | `bool` | get, set | 类型：布尔值 |
| `DefIndex` | `int` | get, set | 类型：long |



---

## 🔌 EventItemPickupFailed

事件“物品拾取失败”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventItemPickupFailed\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Item` | `string` | get, set | 类型：字符串 |
| `Reason` | `short` | get, set | 类型：短整型 |
| `Limit` | `short` | get, set | 类型：短整型 |



---

## 🔌 EventItemPickupSlerp

事件"item_pickup_slerp"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventItemPickupSlerp\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Index` | `short` | get, set | 类型：短整型 |
| `Behavior` | `short` | get, set | 类型：短整型 |



---

## 🔌 EventItemPurchase

事件"item_purchase"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventItemPurchase\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Team` | `short` | get, set | 类型：短整型 |
| `LoadOut` | `short` | get, set | 类型：短整型 |
| `Weapon` | `string` | get, set | 类型：字符串 |



---

## 🔌 EventItemRemove

事件"item_remove"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventItemRemove\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Item` | `string` | get, set | 可以是诸如'tmp'或'hegrenade'的武器，也可以是诸如'nvgs'的物品<br/>类型：字符串 |
| `DefIndex` | `int` | get, set | 类型：long |



---

## 🔌 EventItemSchemaInitialized

事件"item_schema_initialized"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventItemSchemaInitialized\>`



---

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
| `Reason` | `byte` | get, set | 0 = 队伍已满 <br/> 类型：byte |



---

## 🔌 EventLocalPlayerControllerTeam

事件"本地玩家控制器队伍”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventLocalPlayerControllerTeam\>`



---

## 🔌 EventLocalPlayerPawnChanged

事件 "local_player_pawn_changed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventLocalPlayerPawnChanged\>`



---

## 🔌 EventLocalPlayerTeam

事件 "local_player_team"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventLocalPlayerTeam\>`



---

## 🔌 EventLootCrateOpened

事件"loot_crate_opened"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventLootCrateOpened\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 玩家实体索引<br/>类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 玩家实体索引<br/>类型：玩家控制器 |
| `UserId` | `int` | get, set | 玩家实体索引<br/>类型：玩家控制器 |
| `Type` | `string` | get, set | 箱子的类型（金属、木质或空投）<br/> type: string |



---

## 🔌 EventLootCrateVisible

事件 "loot_crate_visible"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventLootCrateVisible\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 玩家实体索引<br/>类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 玩家实体索引<br/>类型：玩家控制器 |
| `UserId` | `int` | get, set | 玩家实体索引<br/>类型：玩家控制器 |
| `Subject` | `short` | get, set | 木箱实体索引<br/>类型：短整型 |
| `Type` | `string` | get, set | 箱子的类型（金属、木质或空投）<br/> type: string |



---

## 🔌 EventMapShutdown

事件 "map_shutdown"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventMapShutdown\>`



---

## 🔌 EventMapTransition

事件"map_transition"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventMapTransition\>`



---

## 🔌 EventMatchEndConditions

事件"match_end_conditions"（比赛结束条件）

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventMatchEndConditions\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Frags` | `int` | get, set | 类型：long |
| `MaxRounds` | `int` | get, set | 类型：long |
| `WinRounds` | `int` | get, set | 类型：long |
| `Time` | `int` | get, set | 类型：long |



---

## 🔌 EventMaterialDefaultComplete

事件"material_default_complete"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventMaterialDefaultComplete\>`



---

## 🔌 EventMbInputLockCancel

事件 "mb_input_lock_cancel"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventMbInputLockCancel\>`



---

## 🔌 EventMbInputLockSuccess

事件"mb_input_lock_success"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventMbInputLockSuccess\>`



---

## 🔌 EventMolotovDetonate

事件 "molotov_detonate"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventMolotovDetonate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `X` | `float` | get, set | 类型：浮点数 |
| `Y` | `float` | get, set | 类型：浮点数 |
| `Z` | `float` | get, set | 类型：浮点数 |



---

## 🔌 EventNavBlocked

事件"nav_blocked"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventNavBlocked\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Area` | `int` | get, set | 类型：long |
| `Blocked` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventNavGenerate

事件"nav_generate"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventNavGenerate\>`



---

## 🔌 EventNextlevelChanged

事件"nextlevel_changed"：一个游戏事件，名称长度最多可为 32 个字符。

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventNextlevelChanged\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `NextLevel` | `string` | get, set | 类型：字符串 |
| `MapGroup` | `string` | get, set | 类型：字符串 |
| `SkirmishMode` | `string` | get, set | 类型：字符串 |



---

## 🔌 EventOpenCrateInstr

事件 "open_crate_instr"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventOpenCrateInstr\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 玩家实体索引<br/>类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 玩家实体索引<br/>类型：玩家控制器 |
| `UserId` | `int` | get, set | 玩家实体索引<br/>类型：玩家控制器 |
| `Subject` | `short` | get, set | 木箱实体索引<br/>类型：短整型 |
| `Type` | `string` | get, set | 箱子的类型（金属、木质或空投）<br/> type: string |



---

## 🔌 EventOtherDeath

事件“其他死亡”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventOtherDeath\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `OtherID` | `short` | get, set | 死亡的其他实体 ID <br/> 类型：short |
| `OtherType` | `string` | get, set | 其他实体类型<br/>类型：字符串 |
| `Attacker` | `short` | get, set | 击杀者的用户 ID<br/>类型：short |
| `Weapon` | `string` | get, set | 武器名称：击杀者所使用的武器<br/>类型：字符串 |
| `WeaponItemid` | `string` | get, set | 武器击杀者使用的库存物品 ID<br/>类型：字符串 |
| `WeaponFauxitemid` | `string` | get, set | 武器击杀者使用的假物品 ID<br/>类型：字符串 |
| `WeaponOriginalownerXuid` | `string` | get, set | 类型：字符串 |
| `Headshot` | `bool` | get, set | 指示爆头 <br/> 类型：布尔值 |
| `Penetrated` | `short` | get, set | 在击杀目标前，被穿透的弹射物数量<br/>类型：short |
| `NoScope` | `bool` | get, set | 击杀未使用瞄准镜，用于死亡通知图标<br/>类型：布尔值 |
| `ThruSmoke` | `bool` | get, set | 射速武器穿透烟雾弹<br/>类型：布尔值 |
| `AttackerBlind` | `bool` | get, set | 攻击者因闪光弹致盲<br/>类型：布尔值 |



---

## 🔌 EventParachuteDeploy

事件"parachute_deploy"（降落伞部署）

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

## 🔌 EventPhysgunPickup

事件"physgun_pickup"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPhysgunPickup\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Target` | `nint` | get, set | 拾取的实体<br/>类型：ehandle |



---

## 🔌 EventPlayerActivate

事件 "player_activate"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerActivate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户 ID<br/>类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户 ID<br/>类型：玩家控制器 |
| `UserId` | `int` | get, set | 服务器上的用户 ID<br/>类型：玩家控制器 |



---

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

## 🔌 EventPlayerBlind

事件 "player_blind"（玩家致盲）

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerBlind\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `AttackerController` | `CCSPlayerController` | get | 投掷闪光弹的用户 ID<br/>类型：player_controller |
| `AttackerPawn` | `CCSPlayerPawn` | get | 投掷闪光弹的用户 ID<br/>类型：player_controller |
| `Attacker` | `int` | get, set | 投掷闪光弹的用户 ID<br/>类型：player_controller |
| `EntityID` | `short` | get, set | 闪光弹爆炸<br/>类型：short |
| `BlindDuration` | `float` | get, set | 类型：浮点数 |



---

## 🔌 EventPlayerChangename

事件 "player_changename"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerChangename\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户 ID<br/>类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户 ID<br/>类型：玩家控制器 |
| `UserId` | `int` | get, set | 服务器上的用户 ID<br/>类型：玩家控制器 |
| `OldName` | `string` | get, set | 玩家旧名称（当前名称）<br/>类型：字符串 |
| `NewName` | `string` | get, set | 玩家新名称<br/>类型：字符串 |



---

## 🔌 EventPlayerChat

事件 "player_chat"：玩家公开聊天

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerChat\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TeamOnly` | `bool` | get, set | true 表示仅启用队伍聊天<br/>类型：bool |
| `UserIdController` | `CCSPlayerController` | get | 聊天中的玩家 <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 聊天中的玩家 <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 聊天中的玩家 <br/> 类型：玩家控制器 |
| `Playerid` | `short` | get, set | 聊天中的玩家 ID<br/>类型：short |
| `Text` | `string` | get, set | 聊天文本<br/>类型：字符串 |



---

## 🔌 EventPlayerConnect

事件"player_connect"：新客户端已连接。

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerConnect\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | get, set | 玩家名称<br/>类型：字符串 |
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户 ID（在服务器上唯一）<br/>类型：player_controller |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户 ID（在服务器上唯一）<br/>类型：player_controller |
| `UserId` | `int` | get, set | 服务器上的用户 ID（在服务器上唯一）<br/>类型：player_controller |
| `NetworkID` | `string` | get, set | 玩家网络（即 Steam）ID <br/> 类型：字符串 |
| `XuID` | `ulong` | get, set | Steam ID<br/>类型：uint64 |
| `Bot` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventPlayerConnectFull

事件"player_connect_full"：玩家已在连接序列中发送最终消息

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerConnectFull\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户 ID（在服务器上唯一）<br/>类型：player_controller |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户 ID（在服务器上唯一）<br/>类型：player_controller |
| `UserId` | `int` | get, set | 服务器上的用户 ID（在服务器上唯一）<br/>类型：player_controller |



---

## 🔌 EventPlayerDeath

事件 "player_death" 是一个游戏事件，名称最长可为 32 个字符。

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerDeath\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 死亡用户的用户 ID<br/>类型：player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 死亡用户的用户 ID<br/>类型：player_controller_and_pawn |
| `UserId` | `int` | get, set | 死亡用户的用户 ID<br/>类型：player_controller_and_pawn |
| `AttackerController` | `CCSPlayerController` | get | 击杀者的用户 ID<br/>类型：player_controller_and_pawn |
| `AttackerPawn` | `CCSPlayerPawn` | get | 击杀者的用户 ID<br/>类型：player_controller_and_pawn |
| `Attacker` | `int` | get, set | 击杀者的用户 ID<br/>类型：player_controller_and_pawn |
| `AssisterController` | `CCSPlayerController` | get | 协助击杀的玩家<br/>类型：player_controller_and_pawn |
| `AssisterPawn` | `CCSPlayerPawn` | get | 协助击杀的玩家<br/>类型：player_controller_and_pawn |
| `Assister` | `int` | get, set | 协助击杀的玩家<br/>类型：player_controller_and_pawn |
| `AssistedFlash` | `bool` | get, set | 辅助角色成功投掷闪光弹 <br/> 类型：布尔值 |
| `Weapon` | `string` | get, set | 武器名称：击杀者所使用的武器<br/>类型：字符串 |
| `WeaponItemid` | `string` | get, set | 武器击杀者使用的库存物品 ID<br/>类型：字符串 |
| `WeaponFauxitemid` | `string` | get, set | 武器击杀者使用的假物品 ID<br/>类型：字符串 |
| `WeaponOriginalownerXuid` | `string` | get, set | 类型：字符串 |
| `Headshot` | `bool` | get, set | 指示爆头 <br/> 类型：布尔值 |
| `Dominated` | `short` | get, set | 该击杀是否使凶手支配了受害者 <br/> 类型：short |
| `Revenge` | `short` | get, set | 该击杀是否使杀手对受害者进行了复仇 <br/> 类型：short |
| `Wipe` | `short` | get, set | 是否为导致小队全灭的击杀<br/>类型：short |
| `Penetrated` | `short` | get, set | 在击杀目标前，被穿透的弹射物数量<br/>类型：short |
| `NoReplay` | `bool` | get, set | 如果回放数据不可用，此项将存在并设置为 false <br/> 类型：布尔值 |
| `NoScope` | `bool` | get, set | 击杀未使用瞄准镜，用于死亡通知图标<br/>类型：布尔值 |
| `ThruSmoke` | `bool` | get, set | 射速武器穿透烟雾弹<br/>类型：布尔值 |
| `AttackerBlind` | `bool` | get, set | 攻击者因闪光弹致盲<br/>类型：布尔值 |
| `Distance` | `float` | get, set | 到受害者的距离（单位：米）<br/> 类型：float |
| `DmgHealth` | `short` | get, set | 对生命值造成的伤害<br/>类型：short |
| `DmgArmor` | `byte` | get, set | 对护甲造成的伤害<br/>类型：byte |
| `HitGroup` | `byte` | get, set | 受击部位组（Hitgroup）<br/>类型：byte |
| `AttackerInAir` | `bool` | get, set | 攻击者处于空中<br/>类型：布尔值 |



---

## 🔌 EventPlayerDecal

事件 "player_decal"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerDecal\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家生命体 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家生命体 |
| `UserId` | `int` | get, set | 类型：玩家生命体 |



---

## 🔌 EventPlayerDisconnect

事件"player_disconnect"：客户端已断开连接

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerDisconnect\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户 ID<br/>类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户 ID<br/>类型：玩家控制器 |
| `UserId` | `int` | get, set | 服务器上的用户 ID<br/>类型：玩家控制器 |
| `Reason` | `short` | get, set | 见 NetworkDisconnect 枚举 Protobuf<br/>类型：short |
| `Name` | `string` | get, set | 玩家名称<br/>类型：字符串 |
| `NetworkID` | `string` | get, set | 玩家网络（即 Steam）ID <br/> 类型：字符串 |
| `XuID` | `ulong` | get, set | Steam ID<br/>类型：uint64 |
| `PlayerID` | `short` | get, set | 类型：短整型 |



---

## 🔌 EventPlayerFalldamage

事件“玩家坠落伤害”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerFalldamage\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `Damage` | `float` | get, set | 类型：浮点数 |



---

## 🔌 EventPlayerFootstep

事件"player_footstep"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerFootstep\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家生命体 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家生命体 |
| `UserId` | `int` | get, set | 类型：玩家生命体 |



---

## 🔌 EventPlayerFullUpdate

事件 "player_full_update"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerFullUpdate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户 ID<br/>类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户 ID<br/>类型：玩家控制器 |
| `UserId` | `int` | get, set | 服务器上的用户 ID<br/>类型：玩家控制器 |
| `Count` | `short` | get, set | 本次完整更新的编号<br/>类型：short |



---

## 🔌 EventPlayerGivenC4

事件"player_given_c4"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerGivenC4\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 接收 C4 的用户 ID<br/>类型：player_controller |
| `UserIdPawn` | `CCSPlayerPawn` | get | 接收 C4 的用户 ID<br/>类型：player_controller |
| `UserId` | `int` | get, set | 接收 C4 的用户 ID<br/>类型：player_controller |



---

## 🔌 EventPlayerHintmessage

事件 "player_hintmessage"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerHintmessage\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `HintMessage` | `string` | get, set | 提示的可本地化字符串<br/>类型：string |



---

## 🔌 EventPlayerHurt

事件"player_hurt"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerHurt\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 受伤的玩家<br/>类型：player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 受伤的玩家<br/>类型：player_controller_and_pawn |
| `UserId` | `int` | get, set | 受伤的玩家<br/>类型：player_controller_and_pawn |
| `AttackerController` | `CCSPlayerController` | get | 发起攻击的玩家<br/>类型：player_controller_and_pawn |
| `AttackerPawn` | `CCSPlayerPawn` | get | 发起攻击的玩家<br/>类型：player_controller_and_pawn |
| `Attacker` | `int` | get, set | 发起攻击的玩家<br/>类型：player_controller_and_pawn |
| `Health` | `byte` | get, set | 剩余生命值 <br/> 类型：byte |
| `Armor` | `byte` | get, set | 剩余护甲值<br/>类型：byte |
| `Weapon` | `string` | get, set | 攻击者使用的武器名称，若为场景中的通用对象则为世界 <br/> 类型：字符串 |
| `DmgHealth` | `short` | get, set | 对生命值造成的伤害<br/>类型：short |
| `DmgArmor` | `byte` | get, set | 对护甲造成的伤害<br/>类型：byte |
| `HitGroup` | `byte` | get, set | 受击部位组（Hitgroup）<br/>类型：byte |



---

## 🔌 EventPlayerInfo

事件"player_info"：玩家更改了其名称

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | get, set | 玩家名称<br/>类型：字符串 |
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户 ID（在服务器上唯一）<br/>类型：player_controller |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户 ID（在服务器上唯一）<br/>类型：player_controller |
| `UserId` | `int` | get, set | 服务器上的用户 ID（在服务器上唯一）<br/>类型：player_controller |
| `SteamID` | `ulong` | get, set | 玩家网络（即 Steam）ID<br/>类型：uint64 |
| `Bot` | `bool` | get, set | 当玩家为 AI 机器人时返回 true <br/> 类型：bool |



---

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

## 🔌 EventPlayerPing

事件"player_ping"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerPing\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `EntityID` | `short` | get, set | 类型：短整型 |
| `X` | `float` | get, set | 类型：浮点数 |
| `Y` | `float` | get, set | 类型：浮点数 |
| `Z` | `float` | get, set | 类型：浮点数 |
| `Urgent` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventPlayerPingStop

事件"player_ping_stop"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerPingStop\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityID` | `short` | get, set | 类型：短整型 |



---

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
| `Slot` | `short` | get, set | 类型：短整型 |



---

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
| `Vote` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventPlayerScore

事件 "player_score"：玩家得分已变更

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerScore\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户 ID<br/>类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户 ID<br/>类型：玩家控制器 |
| `UserId` | `int` | get, set | 服务器上的用户 ID<br/>类型：玩家控制器 |
| `Kills` | `short` | get, set | 击杀数 <br/> 类型：short |
| `Deaths` | `short` | get, set | 死亡次数<br/>类型：short |
| `Score` | `short` | get, set | 总游戏分数<br/>类型：短整型（short） |



---

## 🔌 EventPlayerShoot

事件 "player_shoot"：玩家开火射击其武器。

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerShoot\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户 ID<br/>类型：player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户 ID<br/>类型：player_controller_and_pawn |
| `UserId` | `int` | get, set | 服务器上的用户 ID<br/>类型：player_controller_and_pawn |
| `Weapon` | `byte` | get, set | 武器 ID<br/>类型：byte |
| `Mode` | `byte` | get, set | 武器模式<br/>类型：字节 |



---

## 🔌 EventPlayerSound

事件"player_sound"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerSound\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `Radius` | `int` | get, set | 类型：整数 |
| `Duration` | `float` | get, set | 类型：浮点数 |
| `Step` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventPlayerSpawn

事件 "player_spawn"：玩家在游戏中生成

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
| `InRestart` | `bool` | get, set | 如果重启待处理则为 true<br/>类型：bool |



---

## 🔌 EventPlayerStatsUpdated

事件"player_stats_updated"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerStatsUpdated\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ForceUpload` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventPlayerTeam

事件“玩家队伍”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerTeam\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 玩家<br/>类型：玩家控制器与Pawn（Pawn 为游戏实体基类） |
| `UserIdPawn` | `CCSPlayerPawn` | get | 玩家<br/>类型：玩家控制器与Pawn（Pawn 为游戏实体基类） |
| `UserId` | `int` | get, set | 玩家<br/>类型：玩家控制器与Pawn（Pawn 为游戏实体基类） |
| `Team` | `byte` | get, set | 团队 ID<br/>类型：byte |
| `OldTeam` | `byte` | get, set | 旧队伍 ID<br/>类型：字节 |
| `Disconnect` | `bool` | get, set | 因玩家断开连接而更改队伍 <br/> 类型：布尔型 |
| `Silent` | `bool` | get, set | 类型：布尔值 |
| `Name` | `string` | get, set | 类型：字符串 |
| `IsBot` | `bool` | get, set | 如果玩家是机器人则为 true<br/>类型：bool |



---

## 🔌 EventRagdollDissolved

事件 "ragdoll_dissolved"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRagdollDissolved\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntIndex` | `int` | get, set | 类型：long |



---

## 🔌 EventReadGameTitledata

事件"read_game_titledata"：从用户档案中读取游戏标题数据

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventReadGameTitledata\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ControllerId` | `short` | get, set | 用户的控制器 ID<br/>类型：short |



---

## 🔌 EventRepostXboxAchievements

事件 "repost_xbox_achievements"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRepostXboxAchievements\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SplitScreenPlayer` | `short` | get, set | 分屏 ID<br/>类型：短整型（short） |



---

## 🔌 EventResetGameTitledata

事件"reset_game_titledata"重置用户标题数据；请勿自动写入配置文件。

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventResetGameTitledata\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ControllerId` | `short` | get, set | 用户的控制器 ID<br/>类型：short |



---

## 🔌 EventRoundAnnounceFinal

事件 "round_announce_final"（回合最终播报）

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundAnnounceFinal\>`



---

## 🔌 EventRoundAnnounceLastRoundHalf

事件"round_announce_last_round_half"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundAnnounceLastRoundHalf\>`



---

## 🔌 EventRoundAnnounceMatchPoint

事件"round_announce_match_point"（宣布赛点）

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundAnnounceMatchPoint\>`



---

## 🔌 EventRoundAnnounceMatchStart

事件“round_announce_match_start”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundAnnounceMatchStart\>`



---

## 🔌 EventRoundAnnounceWarmup

事件“回合预热宣告”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundAnnounceWarmup\>`



---

## 🔌 EventRoundEnd

事件“回合结束”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundEnd\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Winner` | `byte` | get, set | 获胜方/玩家 i <br/> 类型：字节 |
| `Reason` | `byte` | get, set | 胜利原因<br/>类型：字节 |
| `Message` | `string` | get, set | 回合结束消息<br/>类型：字符串 |
| `Time` | `float` | get, set | 类型：浮点数 |
| `Legacy` | `byte` | get, set | 服务器生成的遗留值<br/>类型：byte |
| `PlayerCount` | `short` | get, set | 回合结束时存活的玩家总数，用于统计收集；该值由服务器计算（当客户端在接收此消息时处于回放模式）<br/>类型：short |
| `NoMusic` | `byte` | get, set | 如果设置，则不播放回合结束音乐，因为动作仍在进行中<br/>类型：byte |



---

## 🔌 EventRoundEndUploadStats

事件 "round_end_upload_stats"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundEndUploadStats\>`



---

## 🔌 EventRoundFreezeEnd

事件“回合冻结结束”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundFreezeEnd\>`



---

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
| `Reason` | `short` | get, set | 类型：短整型 |
| `Value` | `int` | get, set | 类型：long |
| `MusickItMvps` | `int` | get, set | 类型：long |
| `NoMusic` | `byte` | get, set | 类型：字节 |
| `MusickItID` | `int` | get, set | 类型：long |



---

## 🔌 EventRoundOfficiallyEnded

事件"round_officially_ended"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundOfficiallyEnded\>`



---

## 🔌 EventRoundPoststart

事件"round_poststart"在所有其他回合重启动作完成后发送

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundPoststart\>`



---

## 🔌 EventRoundPrestart

事件"round_prestart"在所有其他回合重启动作之前发送

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundPrestart\>`



---

## 🔌 EventRoundStart

事件"round_start"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundStart\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TimeLimit` | `int` | get, set | 回合时间限制（单位：秒）<br/>类型：long |
| `FragLimit` | `int` | get, set | 每局击杀限制（秒）<br/>类型：long |
| `Objective` | `string` | get, set | 回合目标<br/>类型：字符串 |



---

## 🔌 EventRoundStartPostNav

事件 "round_start_post_nav"（回合开始导航后）

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundStartPostNav\>`



---

## 🔌 EventRoundStartPreEntity

事件“round_start_pre_entity"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundStartPreEntity\>`



---

## 🔌 EventRoundTimeWarning

事件 "round_time_warning"（回合时间警告）

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundTimeWarning\>`



---

## 🔌 EventSeasoncoinLevelup

事件"seasoncoin_levelup"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSeasoncoinLevelup\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Category` | `short` | get, set | 类型：短整型 |
| `Rank` | `short` | get, set | 类型：短整型 |



---

## 🔌 EventServerCvar

事件"server_cvar"：服务器控制台变量已更改

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventServerCvar\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CVarName` | `string` | get, set | cvar 名称，例如 "mp_roundtime" <br/> 类型：字符串 |
| `CVarValue` | `string` | get, set | 新 cvar 值 <br/> 类型：字符串 |



---

## 🔌 EventServerMessage

事件 "server_message" 通用服务器消息

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventServerMessage\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Text` | `string` | get, set | 消息文本<br/>类型：字符串 |



---

## 🔌 EventServerPreShutdown

事件"server_pre_shutdown"：服务器即将关闭

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventServerPreShutdown\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Reason` | `string` | get, set | 服务器即将关闭的原因<br/>类型：字符串 |



---

## 🔌 EventServerShutdown

事件"server_shutdown"：服务器关闭

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventServerShutdown\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Reason` | `string` | get, set | 服务器关闭的原因 <br/> 类型：字符串 |



---

## 🔌 EventServerSpawn

事件"server_spawn"在服务器启动时触发一次

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventServerSpawn\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Hostname` | `string` | get, set | 公共主机名<br/>类型：字符串 |
| `Address` | `string` | get, set | 主机名、IP 地址或 DNS 名称 <br/> 类型：字符串 |
| `Port` | `short` | get, set | 服务器端口<br/>类型：短整型 |
| `Game` | `string` | get, set | 游戏目录<br/>类型：字符串 |
| `MapName` | `string` | get, set | 地图名称<br/>类型：字符串 |
| `AddonName` | `string` | get, set | 插件名称<br/>类型：字符串 |
| `MaxPlayers` | `int` | get, set | 最大玩家数<br/>类型：长整型 |
| `Os` | `string` | get, set | WIN32, LINUX<br/>类型：字符串 |
| `Dedicated` | `bool` | get, set | true 表示为专用服务器<br/>类型：布尔值 |
| `Password` | `bool` | get, set | true 表示密码保护 <br/> 类型：bool |



---

## 🔌 EventSetInstructorGroupEnabled

事件 "set_instructor_group_enabled"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSetInstructorGroupEnabled\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Group` | `string` | get, set | 类型：字符串 |
| `Enabled` | `short` | get, set | 类型：短整型 |



---

## 🔌 EventSfuievent

事件 "sfuievent"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSfuievent\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Action` | `string` | get, set | 类型：字符串 |
| `Data` | `string` | get, set | 类型：字符串 |
| `Slot` | `byte` | get, set | 类型：字节 |



---

## 🔌 EventShowDeathpanel

事件"show_deathpanel"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventShowDeathpanel\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `VictimController` | `CCSPlayerController` | get | 被击杀者的索引 <br/> 类型：player_controller_and_pawn |
| `VictimPawn` | `CCSPlayerPawn` | get | 被击杀者的索引 <br/> 类型：player_controller_and_pawn |
| `Victim` | `int` | get, set | 被击杀者的索引 <br/> 类型：player_controller_and_pawn |
| `Killer` | `nint` | get, set | 被击杀实体的 entindex<br/>类型：ehandle |
| `KillerControllerController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `KillerControllerPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `KillerController` | `int` | get, set | 类型：玩家控制器 |
| `HitsTaken` | `short` | get, set | 类型：短整型 |
| `DamageTaken` | `short` | get, set | 类型：短整型 |
| `HitsGiven` | `short` | get, set | 类型：短整型 |
| `DamageGiven` | `short` | get, set | 类型：短整型 |



---

## 🔌 EventShowSurvivalRespawnStatus

事件"show_survival_respawn_status"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventShowSurvivalRespawnStatus\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `LocToken` | `string` | get, set | 类型：字符串 |
| `Duration` | `int` | get, set | 类型：long |
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |



---

## 🔌 EventSilencerDetach

事件“消音器脱离”

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

## 🔌 EventSilencerOff

事件"silencer_off"

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

## 🔌 EventSilencerOn

事件"silencer_on"

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
| `ParaDrop` | `short` | get, set | 类型：短整型 |



---

## 🔌 EventSmokegrenadeDetonate

事件"smokegrenade_detonate"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSmokegrenadeDetonate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `EntityID` | `short` | get, set | 类型：短整型 |
| `X` | `float` | get, set | 类型：浮点数 |
| `Y` | `float` | get, set | 类型：浮点数 |
| `Z` | `float` | get, set | 类型：浮点数 |



---

## 🔌 EventSmokegrenadeExpired

事件"烟雾弹已过期”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSmokegrenadeExpired\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `EntityID` | `short` | get, set | 类型：短整型 |
| `X` | `float` | get, set | 类型：浮点数 |
| `Y` | `float` | get, set | 类型：浮点数 |
| `Z` | `float` | get, set | 类型：浮点数 |



---

## 🔌 EventSpecModeUpdated

事件 "spec_mode_updated"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSpecModeUpdated\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 观战玩家<br/>类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 观战玩家<br/>类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 观战玩家<br/>类型：玩家控制器与Pawn |



---

## 🔌 EventSpecTargetUpdated

事件 "spec_target_updated"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSpecTargetUpdated\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 观战玩家<br/>类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 观战玩家<br/>类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 观战玩家<br/>类型：玩家控制器与Pawn |
| `Target` | `nint` | get, set | 目标对象的 ehandle <br/> 类型：ehandle |



---

## 🔌 EventStartHalftime

事件 "start_halftime"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventStartHalftime\>`



---

## 🔌 EventStartVote

事件"start_vote"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventStartVote\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `Type` | `byte` | get, set | 类型：字节 |
| `VoteParameter` | `short` | get, set | 类型：短整型 |



---

## 🔌 EventStorePricesheetUpdated

事件 "store_pricesheet_updated"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventStorePricesheetUpdated\>`



---

## 🔌 EventSurvivalAnnouncePhase

事件"survival_announce_phase"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSurvivalAnnouncePhase\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Phase` | `short` | get, set | 阶段编号<br/>类型：short |



---

## 🔌 EventSurvivalNoRespawnsFinal

事件“生存模式_最终无重生”

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

## 🔌 EventSurvivalNoRespawnsWarning

事件"survival_no_respawns_warning"（生存模式无重生警告）

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

## 🔌 EventSurvivalParadropBreak

事件"survival_paradrop_break"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSurvivalParadropBreak\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityID` | `short` | get, set | 类型：短整型 |



---

## 🔌 EventSurvivalParadropSpawn

事件 "survival_paradrop_spawn"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSurvivalParadropSpawn\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityID` | `short` | get, set | 类型：短整型 |



---

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

## 🔌 EventSwitchTeam

事件"switch_team"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSwitchTeam\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `NumPlayers` | `short` | get, set | T 阵营和 CT 阵营当前活跃玩家数量 <br/> 类型：short |
| `NumSpectators` | `short` | get, set | 观众数量<br/>类型：短整型 |
| `AvgRank` | `short` | get, set | 人类玩家的平均等级<br/>类型：short |
| `NumTSlotsFree` | `short` | get, set | 类型：短整型 |
| `NumCTSlotsFree` | `short` | get, set | 类型：短整型 |



---

## 🔌 EventTagrenadeDetonate

事件"tagrenade_detonate"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTagrenadeDetonate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `EntityID` | `short` | get, set | 类型：短整型 |
| `X` | `float` | get, set | 类型：浮点数 |
| `Y` | `float` | get, set | 类型：浮点数 |
| `Z` | `float` | get, set | 类型：浮点数 |



---

## 🔌 EventTeamInfo

事件"team_info"：团队信息

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTeamInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TeamID` | `byte` | get, set | 唯一团队 ID<br/>类型：字节 |
| `Teamname` | `string` | get, set | 队伍名称，例如"Team Blue"<br/>类型：字符串 |



---

## 🔌 EventTeamIntroEnd

事件 "team_intro_end"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTeamIntroEnd\>`



---

## 🔌 EventTeamIntroStart

事件"team_intro_start"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTeamIntroStart\>`



---

## 🔌 EventTeamScore

事件"team_score"：队伍分数变更

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTeamScore\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TeamID` | `byte` | get, set | 团队 ID<br/>类型：byte |
| `Score` | `short` | get, set | 总团队分数<br/>类型：short |



---

## 🔌 EventTeamchangePending

事件"teamchange_pending"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTeamchangePending\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `UserId` | `int` | get, set | 类型：玩家控制器 |
| `ToTeam` | `byte` | get, set | 类型：字节 |



---

## 🔌 EventTeamplayBroadcastAudio

事件"teamplay_broadcast_audio"会向队伍中的每位成员播放一段声音。

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTeamplayBroadcastAudio\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Team` | `byte` | get, set | 唯一团队 ID<br/>类型：字节 |
| `Sound` | `string` | get, set | 要播放的音效名称<br/>类型：字符串 |



---

## 🔌 EventTeamplayRoundStart

事件 "teamplay_round_start"：回合重新开始

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTeamplayRoundStart\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `FullReset` | `bool` | get, set | 这是否为地图的全局重置<br/>类型：布尔值 |



---

## 🔌 EventTournamentReward

事件"tournament_reward"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTournamentReward\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `DefIndex` | `int` | get, set | 类型：long |
| `TotalRewards` | `int` | get, set | 类型：long |
| `AccountID` | `int` | get, set | 类型：long |



---

## 🔌 EventTrialTimeExpired

事件"trial_time_expired"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTrialTimeExpired\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 时间已耗尽的玩家<br/>类型：player_controller |
| `UserIdPawn` | `CCSPlayerPawn` | get | 时间已耗尽的玩家<br/>类型：player_controller |
| `UserId` | `int` | get, set | 时间已耗尽的玩家<br/>类型：player_controller |



---

## 🔌 EventUgcFileDownloadFinished

事件“ugc_file_download_finished"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventUgcFileDownloadFinished\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `HContent` | `ulong` | get, set | 该特定内容的 ID（可能是图片或地图）<br/>类型：uint64 |



---

## 🔌 EventUgcFileDownloadStart

事件"ugc_file_download_start"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventUgcFileDownloadStart\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `HContent` | `ulong` | get, set | 该特定内容的 ID（可能是图片或地图）<br/>类型：uint64 |
| `PublishedFileId` | `ulong` | get, set | 关联内容包的 ID <br/> 类型：uint64 |



---

## 🔌 EventUgcMapDownloadError

事件 "ugc_map_download_error"（创意工坊地图下载错误）

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventUgcMapDownloadError\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PublishedFileId` | `ulong` | get, set | 类型：无符号 64 位整数 |
| `ErrorCode` | `int` | get, set | 类型：long |



---

## 🔌 EventUgcMapInfoReceived

事件 "ugc_map_info_received"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventUgcMapInfoReceived\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PublishedFileId` | `ulong` | get, set | 类型：无符号 64 位整数 |



---

## 🔌 EventUgcMapUnsubscribed

事件"ugc_map_unsubscribed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventUgcMapUnsubscribed\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PublishedFileId` | `ulong` | get, set | 类型：无符号 64 位整数 |



---

## 🔌 EventUpdateMatchmakingStats

事件"update_matchmaking_stats"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventUpdateMatchmakingStats\>`



---

## 🔌 EventUserDataDownloaded

事件"user_data_downloaded"在从 Steam 或 XBox Live 下载成就/统计数据时触发

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventUserDataDownloaded\>`



---

## 🔌 EventVipEscaped

事件 "vip_escaped"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVipEscaped\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | VIP 玩家<br/>类型：player_controller |
| `UserIdPawn` | `CCSPlayerPawn` | get | VIP 玩家<br/>类型：player_controller |
| `UserId` | `int` | get, set | VIP 玩家<br/>类型：player_controller |



---

## 🔌 EventVipKilled

事件"vip_killed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVipKilled\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | VIP 玩家<br/>类型：player_controller |
| `UserIdPawn` | `CCSPlayerPawn` | get | VIP 玩家<br/>类型：player_controller |
| `UserId` | `int` | get, set | VIP 玩家<br/>类型：player_controller |
| `AttackerController` | `CCSPlayerController` | get | 击杀 VIP 的用户 ID<br/>类型：player_controller |
| `AttackerPawn` | `CCSPlayerPawn` | get | 击杀 VIP 的用户 ID<br/>类型：player_controller |
| `Attacker` | `int` | get, set | 击杀 VIP 的用户 ID<br/>类型：player_controller |



---

## 🔌 EventVoteCast

事件"vote_cast"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVoteCast\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `VoteOption` | `byte` | get, set | 玩家投票的选项 <br/> 类型：byte |
| `Team` | `short` | get, set | 类型：短整型 |
| `UserIdController` | `CCSPlayerController` | get | 投票的玩家<br/>类型：player_controller |
| `UserIdPawn` | `CCSPlayerPawn` | get | 投票的玩家<br/>类型：player_controller |
| `UserId` | `int` | get, set | 投票的玩家<br/>类型：player_controller |



---

## 🔌 EventVoteCastNo

事件“投票未通过”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVoteCastNo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Team` | `byte` | get, set | 类型：字节 |
| `EntityID` | `int` | get, set | 投票者的实体 ID<br/>类型：long |



---

## 🔌 EventVoteCastYes

事件 "vote_cast_yes"（投票投赞成票）

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVoteCastYes\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Team` | `byte` | get, set | 类型：字节 |
| `EntityID` | `int` | get, set | 投票者的实体 ID<br/>类型：long |



---

## 🔌 EventVoteChanged

事件"vote_changed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVoteChanged\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `YesVotes` | `byte` | get, set | 类型：字节 |
| `NoVotes` | `byte` | get, set | 类型：字节 |
| `PotentialVotes` | `byte` | get, set | 类型：字节 |
| `VoteOption1` | `byte` | get, set | 类型：字节 |
| `VoteOption2` | `byte` | get, set | 类型：字节 |
| `VoteOption3` | `byte` | get, set | 类型：字节 |
| `VoteOption4` | `byte` | get, set | 类型：字节 |
| `VoteOption5` | `byte` | get, set | 类型：字节 |



---

## 🔌 EventVoteEnded

事件"vote_ended"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVoteEnded\>`



---

## 🔌 EventVoteFailed

事件 "vote_failed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVoteFailed\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Team` | `byte` | get, set | 类型：字节 |



---

## 🔌 EventVoteOptions

事件"vote_options"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVoteOptions\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Count` | `byte` | get, set | 选项数量 - 最多为 MAX_VOTE_OPTIONS <br/> 类型：byte |
| `Option1` | `string` | get, set | 类型：字符串 |
| `Option2` | `string` | get, set | 类型：字符串 |
| `Option3` | `string` | get, set | 类型：字符串 |
| `Option4` | `string` | get, set | 类型：字符串 |
| `Option5` | `string` | get, set | 类型：字符串 |



---

## 🔌 EventVotePassed

事件 "vote_passed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVotePassed\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Details` | `string` | get, set | 类型：字符串 |
| `Param1` | `string` | get, set | 类型：字符串 |
| `Team` | `byte` | get, set | 类型：字节 |



---

## 🔌 EventVoteStarted

事件"vote_started"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVoteStarted\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Issue` | `string` | get, set | 类型：字符串 |
| `Param1` | `string` | get, set | 类型：字符串 |
| `VoteData` | `string` | get, set | 类型：字符串 |
| `Team` | `byte` | get, set | 类型：字节 |
| `Initiator` | `int` | get, set | 发起投票的玩家实体 ID <br/> 类型：long |



---

## 🔌 EventWarmupEnd

事件"warmup_end"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventWarmupEnd\>`



---

## 🔌 EventWeaponFire

事件"weapon_fire"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventWeaponFire\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `Weapon` | `string` | get, set | 武器名称，类型：字符串 |
| `Silenced` | `bool` | get, set | 是否为消音武器<br/>类型：布尔型 |



---

## 🔌 EventWeaponFireOnEmpty

事件“武器在空仓时开火”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventWeaponFireOnEmpty\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `Weapon` | `string` | get, set | 武器名称，类型：字符串 |



---

## 🔌 EventWeaponReload

事件"weapon_reload"

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

## 🔌 EventWeaponhudSelection

事件 "weaponhud_selection"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventWeaponhudSelection\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 该事件适用的玩家<br/>类型：player_controller_and_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 该事件适用的玩家<br/>类型：player_controller_and_pawn |
| `UserId` | `int` | get, set | 该事件适用的玩家<br/>类型：player_controller_and_pawn |
| `Mode` | `byte` | get, set | EWeaponHudSelectionMode（切换/拾取/丢弃）<br/>类型：byte |
| `EntIndex` | `int` | get, set | 武器实体索引<br/>类型：long |



---

## 🔌 EventWriteGameTitledata

事件 "write_game_titledata" 将用户标题数据写入个人资料

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventWriteGameTitledata\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ControllerId` | `short` | get, set | 用户的控制器 ID<br/>类型：short |



---

## 🔌 EventWriteProfileData

事件"write_profile_data"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventWriteProfileData\>`



---

