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

事件 "achievement_earned"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAchievementEarned\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlayerController` | `CCSPlayerController` | get | 玩家的实体索引 <br/> 类型：玩家控制器 |
| `PlayerPawn` | `CCSPlayerPawn` | get | 玩家的实体索引 <br/> 类型：玩家控制器 |
| `Player` | `int` | get, set | 玩家的实体索引 <br/> 类型：玩家控制器 |
| `Achievement` | `short` | get, set | 成就 ID <br/> 类型：短整型 |



---

## 🔌 EventAchievementEarnedLocal

事件 "achievement_earned_local"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAchievementEarnedLocal\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Achievement` | `short` | get, set | 成就 ID <br/> 类型：短整型 |
| `SplitScreenPlayer` | `short` | get, set | 分屏 ID <br/> 类型：短整型 |



---

## 🔌 EventAchievementEvent

事件 "achievement_event"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAchievementEvent\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AchievementName` | `string` | get, set | 成就的非本地化名称 <br/> 类型：字符串 |
| `CurVal` | `short` | get, set | 实现步骤数 <br/> 类型：短整型 |
| `MaxVal` | `short` | get, set | 成就中的总步骤数 <br/> 类型：short |



---

## 🔌 EventAchievementInfoLoaded

事件 "achievement_info_loaded"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAchievementInfoLoaded\>`



---

## 🔌 EventAchievementWriteFailed

事件“achievement_write_failed”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAchievementWriteFailed\>`



---

## 🔌 EventAddBulletHitMarker

事件 "add_bullet_hit_marker"

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
| `Item` | `string` | get, set | 要么是像 'tmp' 或 'hegrenade' 这样的武器，要么是像 'nvgs' 这样的物品 <br/> 类型：字符串 |
| `Index` | `int` | get, set | 武器实体索引 <br/> 类型：长整型 |



---

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
| `Success` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventAnnouncePhaseEnd

事件 "announce_phase_end"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventAnnouncePhaseEnd\>`



---

## 🔌 EventBeginNewMatch

事件 "begin_new_match"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBeginNewMatch\>`



---

## 🔌 EventBombAbortdefuse

事件 "bomb_abortdefuse"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombAbortdefuse\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 正在拆除炸弹的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 正在拆除炸弹的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 正在拆除炸弹的玩家 <br/> 类型：玩家控制器与Pawn |



---

## 🔌 EventBombAbortplant

事件 "bomb_abortplant"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombAbortplant\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 正在安放炸弹的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 正在安放炸弹的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 正在安放炸弹的玩家 <br/> 类型：玩家控制器与Pawn |
| `Site` | `short` | get, set | 炸弹点索引 <br/> 类型：短整型 |



---

## 🔌 EventBombBeep

事件 "bomb_beep"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombBeep\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntIndex` | `int` | get, set | c4 实体 <br/> 类型：长整型 |



---

## 🔌 EventBombBegindefuse

事件 "bomb_begindefuse"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombBegindefuse\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 正在拆除炸弹的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 正在拆除炸弹的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 正在拆除炸弹的玩家 <br/> 类型：玩家控制器与Pawn |
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
| `UserIdController` | `CCSPlayerController` | get | 正在安放炸弹的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 正在安放炸弹的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 正在安放炸弹的玩家 <br/> 类型：玩家控制器与Pawn |
| `Site` | `short` | get, set | 炸弹点索引 <br/> 类型：短整型 |



---

## 🔌 EventBombDefused

事件 "bomb_defused"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombDefused\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 拆除炸弹的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 拆除炸弹的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 拆除炸弹的玩家 <br/> 类型：玩家控制器与Pawn |
| `Site` | `short` | get, set | 炸弹点索引 <br/> 类型：短整型 |



---

## 🔌 EventBombDropped

事件 "bomb_dropped"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombDropped\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 投下炸弹的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 投下炸弹的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 投下炸弹的玩家 <br/> 类型：玩家控制器与Pawn |
| `EntIndex` | `int` | get, set | 类型：长整型 |



---

## 🔌 EventBombExploded

事件 "bomb_exploded"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombExploded\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 安放炸弹的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 安放炸弹的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 安放炸弹的玩家 <br/> 类型：玩家控制器与Pawn |
| `Site` | `short` | get, set | 炸弹点索引 <br/> 类型：短整型 |



---

## 🔌 EventBombPickup

事件 "bomb_pickup"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombPickup\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 拾取炸弹的玩家Pawn <br/> 类型：player_pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 拾取炸弹的玩家Pawn <br/> 类型：player_pawn |
| `UserId` | `int` | get, set | 拾取炸弹的玩家Pawn <br/> 类型：player_pawn |



---

## 🔌 EventBombPlanted

事件 "bomb_planted"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBombPlanted\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 安放炸弹的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 安放炸弹的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 安放炸弹的玩家 <br/> 类型：玩家控制器与Pawn |
| `Site` | `short` | get, set | 炸弹点索引 <br/> 类型：短整型 |



---

## 🔌 EventBonusUpdated

事件 "bonus_updated"

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
| `EntIndex` | `int` | get, set | 类型：长整型 |
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家Pawn |
| `UserId` | `int` | get, set | 类型：玩家Pawn |
| `Material` | `byte` | get, set | BREAK_GLASS, BREAK_WOOD, 等 <br/> 类型: byte |



---

## 🔌 EventBreakProp

事件 "break_prop"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBreakProp\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntIndex` | `int` | get, set | 类型：长整型 |
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家Pawn |
| `UserId` | `int` | get, set | 类型：玩家Pawn |
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
| `EntIndex` | `int` | get, set | 类型：长整型 |
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家Pawn |
| `UserId` | `int` | get, set | 类型：玩家Pawn |
| `Material` | `byte` | get, set | BREAK_GLASS, BREAK_WOOD, 等 <br/> 类型: byte |



---

## 🔌 EventBulletDamage

事件 "bullet_damage"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBulletDamage\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `VictimController` | `CCSPlayerController` | get | 受伤的玩家索引 <br/> 类型：玩家控制器与Pawn |
| `VictimPawn` | `CCSPlayerPawn` | get | 受伤的玩家索引 <br/> 类型：玩家控制器与Pawn |
| `Victim` | `int` | get, set | 受伤的玩家索引 <br/> 类型：玩家控制器与Pawn |
| `AttackerController` | `CCSPlayerController` | get | 攻击的玩家索引 <br/> 类型：玩家控制器与游戏体 |
| `AttackerPawn` | `CCSPlayerPawn` | get | 攻击的玩家索引 <br/> 类型：玩家控制器与游戏体 |
| `Attacker` | `int` | get, set | 攻击的玩家索引 <br/> 类型：玩家控制器与游戏体 |
| `Distance` | `float` | get, set | 子弹击中玩家前飞行的距离 <br/> 类型：float |
| `DamageDirX` | `float` | get, set | 子弹的方向向量 <br/> 类型：float |
| `DamageDirY` | `float` | get, set | 子弹的方向向量 <br/> 类型：float |
| `DamageDirZ` | `float` | get, set | 子弹的方向向量 <br/> 类型：float |
| `NumPenetrations` | `byte` | get, set | 穿透的表面数量 <br/> 类型：字节 |
| `NoScope` | `bool` | get, set | 射手是否被瞬狙？<br/>类型：bool |
| `InAir` | `bool` | get, set | 射手是否处于跳跃状态？<br/>类型：布尔值 |
| `ShootAngX` | `float` | get, set | 射击角度 x <br/> 类型：浮点数 |
| `ShootAngY` | `float` | get, set | 射击角度 Y <br/> 类型：浮点数 |
| `ShootAngZ` | `float` | get, set | 射击角度 Z <br/> 类型：浮点数 |
| `AimPunchX` | `float` | get, set | 瞄准偏移 X <br/> 类型：浮点数 |
| `AimPunchY` | `float` | get, set | 瞄准偏移 Y <br/> 类型：浮点数 |
| `AimPunchZ` | `float` | get, set | 瞄准偏移 Z <br/> 类型：浮点数 |
| `AttackTickCount` | `int` | get, set | 攻击节拍 <br/> 类型：int |
| `AttackTickFrac` | `float` | get, set | 攻击分数 <br/> 类型：浮点数 |
| `RenderTickCount` | `int` | get, set | 渲染刻度 <br/> 类型：int |
| `RenderTickFrac` | `float` | get, set | 渲染分数 <br/> 类型：浮点数 |
| `InaccuracyTotal` | `float` | get, set | 总不准确度 <br/> 类型：浮点数 |
| `InaccuracyMove` | `float` | get, set | 移动误差 <br/> 类型：浮点数 |
| `InaccuracyAir` | `float` | get, set | 空气偏差 <br/> 类型：浮点数 |
| `RecoilIndex` | `float` | get, set | 后坐力指数。是的，这确实是一个浮点数。<br/>类型：浮点数 |
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

事件 "buymenu_open"

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

事件 "cart_updated"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCartUpdated\>`



---

## 🔌 EventChoppersIncomingWarning

事件 "choppers_incoming_warning"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventChoppersIncomingWarning\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Global` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventClientDisconnect

事件 "client_disconnect"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventClientDisconnect\>`



---

## 🔌 EventClientLoadoutChanged

事件 "client_loadout_changed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventClientLoadoutChanged\>`



---

## 🔌 EventClientsideLessonClosed

事件 "clientside_lesson_closed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventClientsideLessonClosed\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `LessonName` | `string` | get, set | 类型：字符串 |



---

## 🔌 EventClientsideReloadCustomEcon

事件 "clientside_reload_custom_econ"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventClientsideReloadCustomEcon\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SteamID` | `string` | get, set | 类型：字符串 |



---

## 🔌 EventCoreGameEvents

事件 "核心游戏事件"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCoreGameEvents\>`



---

## 🔌 EventCsGameDisconnected

事件 "cs_game_disconnected"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCsGameDisconnected\>`



---

## 🔌 EventCsIntermission

事件 "cs_intermission"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCsIntermission\>`



---

## 🔌 EventCsMatchEndRestart

事件 "cs_match_end_restart"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCsMatchEndRestart\>`



---

## 🔌 EventCsPreRestart

事件 "cs_pre_restart"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCsPreRestart\>`



---

## 🔌 EventCsPrevNextSpectator

事件 "cs_prev_next_spectator"

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

事件 "cs_round_start_beep"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCsRoundStartBeep\>`



---

## 🔌 EventCsWinPanelMatch

事件 "cs_win_panel_match"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCsWinPanelMatch\>`



---

## 🔌 EventCsWinPanelRound

事件 "cs_win_panel_round"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCsWinPanelRound\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ShowTimerDefend` | `bool` | get, set | 类型：布尔值 |
| `ShowTimerAttack` | `bool` | get, set | 类型：布尔值 |
| `TimerTime` | `short` | get, set | 类型：短整型 |
| `FinalEvent` | `byte` | get, set | 在 cs_gamerules.h 中定义 <br/> 类型：字节 |
| `FunfactToken` | `string` | get, set | 类型：字符串 |
| `FunfactPlayerController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `FunfactPlayerPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `FunfactPlayer` | `int` | get, set | 类型：玩家控制器 |
| `FunfactData1` | `int` | get, set | 类型：长整型 |
| `FunfactData2` | `int` | get, set | 类型：长整型 |
| `FunfactData3` | `int` | get, set | 类型：长整型 |



---

## 🔌 EventCstrikeevents

事件 "cstrikeevents"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventCstrikeevents\>`



---

## 🔌 EventDecoyDetonate

事件 "诱饵引爆"

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
| `EntityID` | `short` | get, set | 类型：短整型 |
| `X` | `float` | get, set | 类型：浮点数 |
| `Y` | `float` | get, set | 类型：浮点数 |
| `Z` | `float` | get, set | 类型：浮点数 |



---

## 🔌 EventDecoyStarted

事件 "decoy_started"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDecoyStarted\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家Pawn |
| `UserId` | `int` | get, set | 类型：玩家Pawn |
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
| `EntityID` | `int` | get, set | 拆弹者的实体 ID <br/> 类型：长整型 |



---

## 🔌 EventDefuserPickup

事件 "defuser_pickup"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDefuserPickup\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityID` | `int` | get, set | 拆弹者的实体 ID <br/> 类型：长整型 |
| `UserIdController` | `CCSPlayerController` | get | 拾取了拆弹器的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 拾取了拆弹器的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 拾取了拆弹器的玩家 <br/> 类型：玩家控制器与Pawn |



---

## 🔌 EventDemoSkip

事件 "demo_skip"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDemoSkip\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlaybackTick` | `int` | get, set | 当前播放的滴答数 <br/> 类型：长整型 |
| `SkiptoTick` | `int` | get, set | tick 我们将 <br/> 类型：long |



---

## 🔌 EventDemoStart

事件 "demo_start"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDemoStart\>`



---

## 🔌 EventDemoStop

事件 "demo_stop"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDemoStop\>`



---

## 🔌 EventDifficultyChanged

事件 "difficulty_changed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDifficultyChanged\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `NewDifficulty` | `short` | get, set | 类型：短整型 |
| `OldDifficulty` | `short` | get, set | 类型：短整型 |
| `StrDifficulty` | `string` | get, set | 新的难度，类型为字符串 <br/> 类型：字符串 |



---

## 🔌 EventDmBonusWeaponStart

事件 "dm_bonus_weapon_start"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDmBonusWeaponStart\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Time` | `short` | get, set | 此奖励持续的时间长度 <br/> 类型：short |
| `Pos` | `short` | get, set | 奖励武器的配置位置 <br/> 类型：short |



---

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

## 🔌 EventDoorClose

事件 "door_close"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDoorClose\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 谁关了门 <br/> 类型：玩家Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 谁关了门 <br/> 类型：玩家Pawn |
| `UserId` | `int` | get, set | 谁关了门 <br/> 类型：玩家Pawn |
| `Checkpoint` | `bool` | get, set | 门是否为检查点门 <br/> 类型：布尔值 |



---

## 🔌 EventDoorClosed

事件 "door_closed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDoorClosed\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 谁关了门 <br/> 类型：玩家Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 谁关了门 <br/> 类型：玩家Pawn |
| `UserId` | `int` | get, set | 谁关了门 <br/> 类型：玩家Pawn |
| `EntIndex` | `int` | get, set | 类型：长整型 |



---

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

## 🔌 EventDoorOpen

事件 "door_open"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDoorOpen\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 谁关了门 <br/> 类型：玩家Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 谁关了门 <br/> 类型：玩家Pawn |
| `UserId` | `int` | get, set | 谁关了门 <br/> 类型：玩家Pawn |
| `EntIndex` | `int` | get, set | 类型：长整型 |



---

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
| `Cargo` | `short` | get, set | 类型：短整型 |



---

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
| `Cargo` | `short` | get, set | 类型：短整型 |
| `Delivered` | `bool` | get, set | 类型：布尔值 |



---

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

事件 "drop_rate_modified"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventDropRateModified\>`



---

## 🔌 EventDynamicShadowLightChanged

事件“动态阴影光源已更改”

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
| `UserIdController` | `CCSPlayerController` | get | 玩家实体索引 <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 玩家实体索引 <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 玩家实体索引 <br/> 类型：玩家控制器 |
| `Subject` | `short` | get, set | crate 实体索引 <br/> 类型: short |
| `Type` | `string` | get, set | 板条箱类型（金属、木材或空投）<br/>类型：字符串 |



---

## 🔌 EventEnableRestartVoting

事件 "enable_restart_voting"

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

事件 "endmatch_mapvote_selecting_map"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventEndmatchMapvoteSelectingMap\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Count` | `byte` | get, set | 平局次数 <br/> 类型：字节 |
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
| `HasBomb` | `bool` | get, set | 类型：布尔值 |
| `IsPlanted` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventEnterBuyzone

事件 "enter_buyzone"

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

事件 "enter_rescue_zone"

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
| `EntindexKilled` | `int` | get, set | 类型：长整型 |
| `EntindexAttacker` | `int` | get, set | 类型：长整型 |
| `EntindexInflictor` | `int` | get, set | 类型：长整型 |
| `DamageBits` | `int` | get, set | 类型：长整型 |



---

## 🔌 EventEntityVisible

事件 "entity_visible"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventEntityVisible\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 看到该实体的玩家 <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 看到该实体的玩家 <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 看到该实体的玩家 <br/> 类型：玩家控制器 |
| `Subject` | `int` | get, set | 他们所看到的实体的实体索引 <br/> 类型：长整型 |
| `ClassName` | `string` | get, set | 他们所看到实体的类名 <br/> 类型：字符串 |
| `EntityName` | `string` | get, set | 他们所看到的实体的名称 <br/> 类型：字符串 |



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

事件 "finale_start"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventFinaleStart\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Rushes` | `short` | get, set | 类型：短整型 |



---

## 🔌 EventFirstbombsIncomingWarning

事件 "firstbombs_incoming_warning"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventFirstbombsIncomingWarning\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Global` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventFlareIgniteNpc

事件 "flare_ignite_npc"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventFlareIgniteNpc\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntIndex` | `int` | get, set | 实体被点燃 <br/> 类型：长整型 |



---

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
| `EntityID` | `short` | get, set | 类型：短整型 |
| `X` | `float` | get, set | 类型：浮点数 |
| `Y` | `float` | get, set | 类型：浮点数 |
| `Z` | `float` | get, set | 类型：浮点数 |



---

## 🔌 EventGameEnd

事件 "game_end" 表示一场游戏结束

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGameEnd\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Winner` | `byte` | get, set | 获胜方团队/用户 ID <br/> 类型：字节 |



---

## 🔌 EventGameInit

当新游戏开始时发送事件 "game_init"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGameInit\>`



---

## 🔌 EventGameMessage

事件 "game_message" 是由游戏逻辑向所有人发送的一条消息

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGameMessage\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Target` | `byte` | get, set | 0 = 控制台, 1 = HUD <br/> 类型: 字节 |
| `Text` | `string` | get, set | 消息文本 <br/> 类型：字符串 |



---

## 🔌 EventGameNewmap

当新地图完全加载后，发送事件 "game_newmap"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGameNewmap\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MapName` | `string` | get, set | 映射名称 <br/> 类型：字符串 |
| `Transition` | `bool` | get, set | 如果这是从一个地图到另一个地图的转换，则为 true <br/> 类型：布尔值 |



---

## 🔌 EventGamePhaseChanged

事件 "game_phase_changed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGamePhaseChanged\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `NewPhase` | `short` | get, set | 类型：短整型 |



---

## 🔌 EventGameStart

事件 "game_start" 表示新游戏开始

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGameStart\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `RoundsLimit` | `int` | get, set | 最大轮次 <br/> 类型：长整型 |
| `TimeLimit` | `int` | get, set | 时间限制 <br/> 类型：长整型 |
| `FragLimit` | `int` | get, set | 碎片限制 <br/> 类型：长整型 |
| `Objective` | `string` | get, set | 轮次目标 <br/> 类型：字符串 |



---

## 🔌 EventGameevents

事件 "gameevents"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGameevents\>`



---

## 🔌 EventGameinstructorDraw

事件 "gameinstructor_draw"

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
| `VictimIDController` | `CCSPlayerController` | get | 已死亡的用户ID <br/> 类型：玩家控制器 |
| `VictimIDPawn` | `CCSPlayerPawn` | get | 已死亡的用户ID <br/> 类型：玩家控制器 |
| `VictimID` | `int` | get, set | 已死亡的用户ID <br/> 类型：玩家控制器 |
| `AttackerIDController` | `CCSPlayerController` | get | 击杀者用户ID <br/> 类型：玩家控制器 |
| `AttackerIDPawn` | `CCSPlayerPawn` | get | 击杀者用户ID <br/> 类型：玩家控制器 |
| `AttackerID` | `int` | get, set | 击杀者用户ID <br/> 类型：玩家控制器 |
| `Dominated` | `short` | get, set | 凶手是否通过此击杀压制了受害者 <br/> 类型：简短 |
| `Revenge` | `short` | get, set | 凶手是否通过此次击杀向受害者复仇 <br/> 类型：简短 |
| `Bonus` | `bool` | get, set | 杀手是否使用奖励武器杀人？<br/>类型：布尔值 |



---

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

## 🔌 EventGrenadeThrown

事件 "grenade_thrown"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventGrenadeThrown\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `Weapon` | `string` | get, set | 武器名称使用 <br/> 类型：字符串 |



---

## 🔌 EventGuardianWaveRestart

事件 "guardian_wave_restart"

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

事件 "helicopter_grenade_punt_miss"

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

事件 "hltv_cameraman" 中，一名观众/玩家是摄像师

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvCameraman\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 摄像师实体索引 <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 摄像师实体索引 <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 摄像师实体索引 <br/> 类型：玩家控制器 |



---

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

## 🔌 EventHltvChase

事件 "hltv_chase" 对单个实体的拍摄

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvChase\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Target1Controller` | `CCSPlayerController` | get | 主要目标索引 <br/> 类型：玩家控制器 |
| `Target1Pawn` | `CCSPlayerPawn` | get | 主要目标索引 <br/> 类型：玩家控制器 |
| `Target1` | `int` | get, set | 主要目标索引 <br/> 类型：玩家控制器 |
| `Target2Controller` | `CCSPlayerController` | get | 次要目标索引或 0 <br/> 类型：玩家控制器 |
| `Target2Pawn` | `CCSPlayerPawn` | get | 次要目标索引或 0 <br/> 类型：玩家控制器 |
| `Target2` | `int` | get, set | 次要目标索引或 0 <br/> 类型：玩家控制器 |
| `Distance` | `short` | get, set | 相机距离 <br/> 类型：短整型 |
| `Theta` | `short` | get, set | 视角水平 <br/> 类型：短整型 |
| `Phi` | `short` | get, set | 视角垂直 <br/> 类型：短整型 |
| `Inertia` | `byte` | get, set | 相机惯性 <br/> 类型：字节 |
| `InEye` | `byte` | get, set | diretcor 建议显示 ineye <br/> 类型：字节 |



---

## 🔌 EventHltvChat

事件 "hltv_chat" 是由观众发送的 HLTV 聊天消息

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvChat\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Text` | `string` | get, set | 类型：字符串 |
| `SteamID` | `ulong` | get, set | Steam ID <br/> 类型：uint64 |



---

## 🔌 EventHltvFixed

事件 "hltv_fixed" 从固定视角显示

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvFixed\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PosX` | `int` | get, set | 相机在世界中的位置 <br/> 类型：长整型 |
| `Posy` | `int` | get, set | 类型：长整型 |
| `PosZ` | `int` | get, set | 类型：长整型 |
| `Theta` | `short` | get, set | 摄像机角度 <br/> 类型：short |
| `Phi` | `short` | get, set | 类型：短整型 |
| `Offset` | `short` | get, set | 类型：短整型 |
| `FOv` | `float` | get, set | 类型：浮点数 |
| `TargetController` | `CCSPlayerController` | get | 跟随此玩家 <br/> 类型：玩家控制器 |
| `TargetPawn` | `CCSPlayerPawn` | get | 跟随此玩家 <br/> 类型：玩家控制器 |
| `Target` | `int` | get, set | 跟随此玩家 <br/> 类型：玩家控制器 |



---

## 🔌 EventHltvMessage

事件 "hltv_message" 由管理员发送的HLTV消息

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvMessage\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Text` | `string` | get, set | 类型：字符串 |



---

## 🔌 EventHltvRankCamera

事件 "hltv_rank_camera" 一个相机排名

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvRankCamera\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Index` | `byte` | get, set | 固定摄像机索引 <br/> 类型：字节 |
| `Rank` | `float` | get, set | 排名，此摄像头视图的有趣程度 <br/> 类型：浮点数 |
| `TargetController` | `CCSPlayerController` | get | 最佳/最近的目标实体 <br/> 类型：玩家控制器 |
| `TargetPawn` | `CCSPlayerPawn` | get | 最佳/最近的目标实体 <br/> 类型：玩家控制器 |
| `Target` | `int` | get, set | 最佳/最近的目标实体 <br/> 类型：玩家控制器 |



---

## 🔌 EventHltvRankEntity

事件 "hltv_rank_entity" 一个实体排名

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvRankEntity\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 玩家槽位 <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 玩家槽位 <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 玩家槽位 <br/> 类型：玩家控制器 |
| `Rank` | `float` | get, set | 排名，此实体被查看的有趣程度 <br/> 类型：浮点数 |
| `TargetController` | `CCSPlayerController` | get | 最佳/最近的目标实体 <br/> 类型：玩家控制器 |
| `TargetPawn` | `CCSPlayerPawn` | get | 最佳/最近的目标实体 <br/> 类型：玩家控制器 |
| `Target` | `int` | get, set | 最佳/最近的目标实体 <br/> 类型：玩家控制器 |



---

## 🔌 EventHltvReplay

事件 "hltv_replay"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvReplay\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Delay` | `int` | get, set | 杀手重播延迟的秒数 <br/> 类型：long |
| `Reason` | `int` | get, set | 重放原因 (ReplayEventType_t) <br/> 类型: long |



---

## 🔌 EventHltvReplayStatus

事件 "hltv_replay_status"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvReplayStatus\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Reason` | `int` | get, set | hltv重播状态变更原因 () <br/> 类型: long |



---

## 🔌 EventHltvStatus

事件 "hltv_status" 通用HLTV状态

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHltvStatus\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Clients` | `int` | get, set | HLTV 观众数量 <br/> 类型：长整型 |
| `Slots` | `int` | get, set | HLTV槽位数 <br/> 类型：长整型 |
| `Proxies` | `short` | get, set | HLTV代理数量 <br/> 类型：短整型 |
| `Master` | `string` | get, set | 分发主IP:端口 <br/> 类型: 字符串 |



---

## 🔌 EventHltvTitle

事件 "hltv_title"

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
| `Version` | `int` | get, set | 类型：长整型 |



---

## 🔌 EventHostageCallForHelp

事件 "hostage_call_for_help"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHostageCallForHelp\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Hostage` | `short` | get, set | 人质实体索引 <br/> 类型：short |



---

## 🔌 EventHostageFollows

事件 "hostage_follows"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHostageFollows\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 接触人质的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 接触人质的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 接触人质的玩家 <br/> 类型：玩家控制器与Pawn |
| `Hostage` | `short` | get, set | 人质实体索引 <br/> 类型：short |



---

## 🔌 EventHostageHurt

事件 "hostage_hurt"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHostageHurt\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 伤害人质的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 伤害人质的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 伤害人质的玩家 <br/> 类型：玩家控制器与Pawn |
| `Hostage` | `short` | get, set | 人质实体索引 <br/> 类型：short |



---

## 🔌 EventHostageKilled

事件 "hostage_killed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHostageKilled\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 杀害人质的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 杀害人质的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 杀害人质的玩家 <br/> 类型：玩家控制器与Pawn |
| `Hostage` | `short` | get, set | 人质实体索引 <br/> 类型：short |



---

## 🔌 EventHostageRescued

事件 "hostage_rescued"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHostageRescued\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 解救人质的玩家 <br/> 类型：玩家控制器与游戏体 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 解救人质的玩家 <br/> 类型：玩家控制器与游戏体 |
| `UserId` | `int` | get, set | 解救人质的玩家 <br/> 类型：玩家控制器与游戏体 |
| `Hostage` | `short` | get, set | 人质实体索引 <br/> 类型：short |
| `Site` | `short` | get, set | 救援站点索引 <br/> 类型：短整型 |



---

## 🔌 EventHostageRescuedAll

事件 "hostage_rescued_all"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHostageRescuedAll\>`



---

## 🔌 EventHostageStopsFollowing

事件 "hostage_stops_following"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventHostageStopsFollowing\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 解救人质的玩家 <br/> 类型：玩家控制器与游戏体 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 解救人质的玩家 <br/> 类型：玩家控制器与游戏体 |
| `UserId` | `int` | get, set | 解救人质的玩家 <br/> 类型：玩家控制器与游戏体 |
| `Hostage` | `short` | get, set | 人质实体索引 <br/> 类型：short |



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

事件 "inferno_extinguish"

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

## 🔌 EventInstructorCloseLesson

事件 "instructor_close_lesson"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventInstructorCloseLesson\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 本课程面向的玩家 <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 本课程面向的玩家 <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 本课程面向的玩家 <br/> 类型：玩家控制器 |
| `HintName` | `string` | get, set | 要开始课程的名称。必须与 instructor_lesson.txt 匹配 <br/> 类型：字符串 |



---

## 🔌 EventInstructorServerHintCreate

事件 "instructor_server_hint_create" 使用完全由服务器/地图提供的数据创建一个提示。旨在为内容尚未准备好而提示变得不必要之前的游戏测试提供平滑的提示。**不作为可发布产品的临时解决方案**

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventInstructorServerHintCreate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 触发提示的玩家用户ID <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 触发提示的玩家用户ID <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 触发提示的玩家用户ID <br/> 类型：玩家控制器 |
| `HintEntindex` | `int` | get, set | 触发事件的 env_instructor_hint 的实体 ID <br/> 类型：长整型 |
| `HintName` | `string` | get, set | 提示的名称。用于后续再次引用（例如，使用一个终止命令来代替超时）<br/>类型：字符串 |
| `HintReplaceKey` | `string` | get, set | 类型名称，以便相同类型的消息可以相互替换 <br/> 类型：字符串 |
| `HintTarget` | `int` | get, set | 实体ID，提示应在该ID处显示 <br/> 类型：long |
| `HintActivatorUseridController` | `CCSPlayerController` | get | 激活者的玩家槽位 <br/> 类型：玩家控制器 |
| `HintActivatorUseridPawn` | `CCSPlayerPawn` | get | 激活者的玩家槽位 <br/> 类型：玩家控制器 |
| `HintActivatorUserid` | `int` | get, set | 激活者的玩家槽位 <br/> 类型：玩家控制器 |
| `HintTimeout` | `short` | get, set | 提示自动超时的时间（以秒为单位），0 表示永不超时 <br/> 类型：short |
| `HintIconOnscreen` | `string` | get, set | 当提示显示在屏幕上时使用的提示图标。例如："icon_alert_red" <br/> 类型：字符串 |
| `HintIconOffscreen` | `string` | get, set | 当提示信息超出屏幕时使用的提示图标。例如："icon_alert" <br/> 类型：字符串 |
| `HintCaption` | `string` | get, set | 提示标题。例如：“#ThisIsDangerous” <br/> 类型：字符串 |
| `HintActivatorCaption` | `string` | get, set | 仅激活器可见的提示标题，例如 "#YouPushedItGood" <br/> 类型：字符串 |
| `HintColor` | `string` | get, set | 提示颜色，格式为“r,g,b”，其中每个分量值为 0-255 <br/> 类型：字符串 |
| `HintIconOffset` | `float` | get, set | 在z轴上与实体原点偏移的提示距离 <br/> 类型：浮点数 |
| `HintRange` | `float` | get, set | 提示前被剔除的范围 <br/> 类型：浮点数 |
| `HintFlags` | `int` | get, set | 提示标志 <br/> 类型：长整型 |
| `HintBinding` | `string` | get, set | 当 use_binding 为屏幕图标时使用的绑定 <br/> 类型：字符串 |
| `HintAllowNodrawTarget` | `bool` | get, set | 如果为 false，当目标实体不可见时，提示将消失 <br/> 类型：布尔值 |
| `HintNooffscreen` | `bool` | get, set | 如果为 true，则当提示超出玩家视野范围时将不会显示 <br/> 类型：布尔值 |
| `HintForcecaption` | `bool` | get, set | 如果为 true，即使提示被遮挡，提示标题也会显示 <br/> 类型：布尔值 |
| `HintLocalPlayerOnly` | `bool` | get, set | 如果为 true，则只有本地玩家会看到提示 <br/> 类型：布尔值 |
| `HintStartSound` | `string` | get, set | 要播放的游戏音效 <br/> 类型：字符串 |
| `HintLayoutfile` | `string` | get, set | 全景布局文件路径 <br/> 类型：字符串 |
| `HintVrPanelType` | `short` | get, set | 全景面板的附件类型 <br/> 类型：short |
| `HintVrHeightOffset` | `float` | get, set | 附加面板的高度偏移量 <br/> 类型：float |
| `HintVrOffsetX` | `float` | get, set | 附加面板的偏移量 <br/> 类型：浮点数 |
| `HintVrOffsetY` | `float` | get, set | 附加面板的偏移量 <br/> 类型：浮点数 |
| `HintVrOffsetZ` | `float` | get, set | 附加面板的偏移量 <br/> 类型：浮点数 |
| `HintGamepadBinding` | `string` | get, set | 当 use_binding 为屏幕图标时使用的游戏手柄绑定 <br/> 类型：字符串 |



---

## 🔌 EventInstructorServerHintStop

事件 "instructor_server_hint_stop" 销毁一个已创建的服务器/地图提示

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventInstructorServerHintStop\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `HintName` | `string` | get, set | 停止提示的指令。将停止所有具有此名称的提示 <br/> 类型：字符串 |
| `HintEntindex` | `int` | get, set | 触发事件的 env_instructor_hint 的实体 ID <br/> 类型：长整型 |



---

## 🔌 EventInstructorStartLesson

事件 "instructor_start_lesson"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventInstructorStartLesson\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 本课程面向的玩家 <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 本课程面向的玩家 <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 本课程面向的玩家 <br/> 类型：玩家控制器 |
| `HintName` | `string` | get, set | 要开始课程的名称。必须与 instructor_lesson.txt 匹配 <br/> 类型：字符串 |
| `HintTarget` | `int` | get, set | 提示信息应显示的实体ID。如果控制器目标为空，则留空 <br/> 类型：long |
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
| `Itemid` | `int` | get, set | 类型：长整型 |



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
| `Item` | `string` | get, set | 要么是像 'tmp' 或 'hegrenade' 这样的武器，要么是像 'nvgs' 这样的物品 <br/> 类型：字符串 |
| `DefIndex` | `int` | get, set | 类型：长整型 |
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
| `Item` | `string` | get, set | 要么是像 'tmp' 或 'hegrenade' 这样的武器，要么是像 'nvgs' 这样的物品 <br/> 类型：字符串 |
| `Silent` | `bool` | get, set | 类型：布尔值 |
| `DefIndex` | `int` | get, set | 类型：长整型 |



---

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
| `Item` | `string` | get, set | 类型：字符串 |
| `Reason` | `short` | get, set | 类型：短整型 |
| `Limit` | `short` | get, set | 类型：短整型 |



---

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
| `Index` | `short` | get, set | 类型：短整型 |
| `Behavior` | `short` | get, set | 类型：短整型 |



---

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
| `Team` | `short` | get, set | 类型：短整型 |
| `LoadOut` | `short` | get, set | 类型：短整型 |
| `Weapon` | `string` | get, set | 类型：字符串 |



---

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
| `Item` | `string` | get, set | 要么是像 'tmp' 或 'hegrenade' 这样的武器，要么是像 'nvgs' 这样的物品 <br/> 类型：字符串 |
| `DefIndex` | `int` | get, set | 类型：长整型 |



---

## 🔌 EventItemSchemaInitialized

事件 "item_schema_initialized"

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
| `Reason` | `byte` | get, set | 0 = team_full <br/> 类型：字节 |



---

## 🔌 EventLocalPlayerControllerTeam

事件“local_player_controller_team”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventLocalPlayerControllerTeam\>`



---

## 🔌 EventLocalPlayerPawnChanged

事件“本地玩家Pawn已变更”

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

事件 "loot_crate_opened"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventLootCrateOpened\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 玩家实体索引 <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 玩家实体索引 <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 玩家实体索引 <br/> 类型：玩家控制器 |
| `Type` | `string` | get, set | 板条箱类型（金属、木材或空投）<br/>类型：字符串 |



---

## 🔌 EventLootCrateVisible

事件 "loot_crate_visible"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventLootCrateVisible\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 玩家实体索引 <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 玩家实体索引 <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 玩家实体索引 <br/> 类型：玩家控制器 |
| `Subject` | `short` | get, set | crate 实体索引 <br/> 类型: short |
| `Type` | `string` | get, set | 板条箱类型（金属、木材或空投）<br/>类型：字符串 |



---

## 🔌 EventMapShutdown

事件 "map_shutdown"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventMapShutdown\>`



---

## 🔌 EventMapTransition

事件 "map_transition"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventMapTransition\>`



---

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

## 🔌 EventMaterialDefaultComplete

事件 "material_default_complete"

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

事件 "mb_input_lock_success"

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

事件 "nav_blocked"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventNavBlocked\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Area` | `int` | get, set | 类型：长整型 |
| `Blocked` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventNavGenerate

事件 "nav_generate"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventNavGenerate\>`



---

## 🔌 EventNextlevelChanged

事件 "nextlevel_changed" 是一个游戏事件，名称最长可为 32 个字符。

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
| `UserIdController` | `CCSPlayerController` | get | 玩家实体索引 <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 玩家实体索引 <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 玩家实体索引 <br/> 类型：玩家控制器 |
| `Subject` | `short` | get, set | crate 实体索引 <br/> 类型: short |
| `Type` | `string` | get, set | 板条箱类型（金属、木材或空投）<br/>类型：字符串 |



---

## 🔌 EventOtherDeath

事件 "other_death"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventOtherDeath\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `OtherID` | `short` | get, set | 其他已死亡的实体ID <br/> 类型：short |
| `OtherType` | `string` | get, set | 其他实体类型 <br/> 类型：字符串 |
| `Attacker` | `short` | get, set | 击杀者的用户ID <br/> 类型：短整型 |
| `Weapon` | `string` | get, set | 武器名称 杀手使用 <br/> 类型：字符串 |
| `WeaponItemid` | `string` | get, set | 武器杀手使用的物品ID <br/> 类型：字符串 |
| `WeaponFauxitemid` | `string` | get, set | 武器杀手使用的伪物品ID <br/> 类型：字符串 |
| `WeaponOriginalownerXuid` | `string` | get, set | 类型：字符串 |
| `Headshot` | `bool` | get, set | 表示爆头 <br/> 类型：布尔值 |
| `Penetrated` | `short` | get, set | 击杀目标前穿透的物体数量 <br/> 类型：short |
| `NoScope` | `bool` | get, set | 击杀发生时未处于瞄准状态，用于死亡通知图标 <br/> 类型：布尔值 |
| `ThruSmoke` | `bool` | get, set | 射线武器穿透烟雾弹 <br/> 类型：布尔值 |
| `AttackerBlind` | `bool` | get, set | 攻击者因闪光弹致盲 <br/> 类型：布尔值 |



---

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

事件 "physgun_pickup"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPhysgunPickup\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Target` | `nint` | get, set | 实体已拾取 <br/> 类型：ehandle |



---

## 🔌 EventPlayerActivate

事件 "player_activate"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerActivate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户ID <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户ID <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 服务器上的用户ID <br/> 类型：玩家控制器 |



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
| `AttackerController` | `CCSPlayerController` | get | 投掷闪光弹的用户ID <br/> 类型：玩家控制器 |
| `AttackerPawn` | `CCSPlayerPawn` | get | 投掷闪光弹的用户ID <br/> 类型：玩家控制器 |
| `Attacker` | `int` | get, set | 投掷闪光弹的用户ID <br/> 类型：玩家控制器 |
| `EntityID` | `short` | get, set | 闪光弹爆炸 <br/> 类型：short |
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
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户ID <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户ID <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 服务器上的用户ID <br/> 类型：玩家控制器 |
| `OldName` | `string` | get, set | 玩家旧（当前）名称 <br/> 类型：字符串 |
| `NewName` | `string` | get, set | 玩家新名称 <br/> 类型：字符串 |



---

## 🔌 EventPlayerChat

事件 "player_chat" 公共玩家聊天

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerChat\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TeamOnly` | `bool` | get, set | 如果团队仅聊天则为 true <br/> 类型：布尔值 |
| `UserIdController` | `CCSPlayerController` | get | 聊天玩家 <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 聊天玩家 <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 聊天玩家 <br/> 类型：玩家控制器 |
| `Playerid` | `short` | get, set | 聊天玩家ID <br/> 类型：short |
| `Text` | `string` | get, set | 聊天文本 <br/> 类型：字符串 |



---

## 🔌 EventPlayerConnect

事件 "player_connect" 新客户端已连接

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerConnect\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | get, set | 玩家名称 <br/> 类型：字符串 |
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户ID（在服务器上唯一）<br/>类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户ID（在服务器上唯一）<br/>类型：玩家控制器 |
| `UserId` | `int` | get, set | 服务器上的用户ID（在服务器上唯一）<br/>类型：玩家控制器 |
| `NetworkID` | `string` | get, set | 玩家网络（例如 Steam）ID <br/> 类型：字符串 |
| `XuID` | `ulong` | get, set | Steam ID <br/> 类型：uint64 |
| `Bot` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventPlayerConnectFull

事件 "player_connect_full" 玩家已发送连接序列中的最终消息

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerConnectFull\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户ID（在服务器上唯一）<br/>类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户ID（在服务器上唯一）<br/>类型：玩家控制器 |
| `UserId` | `int` | get, set | 服务器上的用户ID（在服务器上唯一）<br/>类型：玩家控制器 |



---

## 🔌 EventPlayerDeath

事件 "player_death" 是一个游戏事件，名称最长可为 32 个字符。

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerDeath\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 已死亡的用户ID <br/> 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 已死亡的用户ID <br/> 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 已死亡的用户ID <br/> 类型：玩家控制器与Pawn |
| `AttackerController` | `CCSPlayerController` | get | 杀死该实体的用户ID <br/> 类型：玩家控制器与Pawn |
| `AttackerPawn` | `CCSPlayerPawn` | get | 杀死该实体的用户ID <br/> 类型：玩家控制器与Pawn |
| `Attacker` | `int` | get, set | 杀死该实体的用户ID <br/> 类型：玩家控制器与Pawn |
| `AssisterController` | `CCSPlayerController` | get | 参与击杀的玩家 <br/> 类型：玩家控制器与游戏体 |
| `AssisterPawn` | `CCSPlayerPawn` | get | 参与击杀的玩家 <br/> 类型：玩家控制器与游戏体 |
| `Assister` | `int` | get, set | 参与击杀的玩家 <br/> 类型：玩家控制器与游戏体 |
| `AssistedFlash` | `bool` | get, set | 助手协助了闪存 <br/> 类型：布尔值 |
| `Weapon` | `string` | get, set | 武器名称 杀手使用 <br/> 类型：字符串 |
| `WeaponItemid` | `string` | get, set | 武器杀手使用的物品ID <br/> 类型：字符串 |
| `WeaponFauxitemid` | `string` | get, set | 武器杀手使用的伪物品ID <br/> 类型：字符串 |
| `WeaponOriginalownerXuid` | `string` | get, set | 类型：字符串 |
| `Headshot` | `bool` | get, set | 表示爆头 <br/> 类型：布尔值 |
| `Dominated` | `short` | get, set | 凶手是否通过此击杀压制了受害者 <br/> 类型：简短 |
| `Revenge` | `short` | get, set | 凶手是否通过此次击杀向受害者复仇 <br/> 类型：简短 |
| `Wipe` | `short` | get, set | 是否导致小队全灭 <br/> 类型：short |
| `Penetrated` | `short` | get, set | 击杀目标前穿透的物体数量 <br/> 类型：short |
| `NoReplay` | `bool` | get, set | 如果重播数据不可用，则此属性将存在并设置为 false <br/> 类型：布尔值 |
| `NoScope` | `bool` | get, set | 击杀发生时未处于瞄准状态，用于死亡通知图标 <br/> 类型：布尔值 |
| `ThruSmoke` | `bool` | get, set | 射线武器穿透烟雾弹 <br/> 类型：布尔值 |
| `AttackerBlind` | `bool` | get, set | 攻击者因闪光弹致盲 <br/> 类型：布尔值 |
| `Distance` | `float` | get, set | 与受害者的距离（单位：米）<br/>类型：浮点数 |
| `DmgHealth` | `short` | get, set | 对健康造成的伤害 <br/> 类型：short |
| `DmgArmor` | `byte` | get, set | 对护甲造成的伤害 <br/> 类型: 字节 |
| `HitGroup` | `byte` | get, set | 被损坏的命中组 <br/> 类型：字节 |
| `AttackerInAir` | `bool` | get, set | 攻击者处于空中 <br/> 类型：布尔值 |



---

## 🔌 EventPlayerDecal

事件 "player_decal"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerDecal\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家Pawn |
| `UserId` | `int` | get, set | 类型：玩家Pawn |



---

## 🔌 EventPlayerDisconnect

事件 "player_disconnect" 客户端已断开连接

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerDisconnect\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户ID <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户ID <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 服务器上的用户ID <br/> 类型：玩家控制器 |
| `Reason` | `short` | get, set | 查看网络断开枚举 protobuf <br/> 类型：short |
| `Name` | `string` | get, set | 玩家名称 <br/> 类型：字符串 |
| `NetworkID` | `string` | get, set | 玩家网络（例如 Steam）ID <br/> 类型：字符串 |
| `XuID` | `ulong` | get, set | Steam ID <br/> 类型：uint64 |
| `PlayerID` | `short` | get, set | 类型：短整型 |



---

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
| `Damage` | `float` | get, set | 类型：浮点数 |



---

## 🔌 EventPlayerFootstep

事件 "player_footstep"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerFootstep\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家Pawn |
| `UserId` | `int` | get, set | 类型：玩家Pawn |



---

## 🔌 EventPlayerFullUpdate

事件 "player_full_update"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerFullUpdate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户ID <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户ID <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 服务器上的用户ID <br/> 类型：玩家控制器 |
| `Count` | `short` | get, set | 本次完整更新的数量 <br/> 类型：short |



---

## 🔌 EventPlayerGivenC4

事件 "player_given_c4"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerGivenC4\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 收到C4的用户ID <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 收到C4的用户ID <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 收到C4的用户ID <br/> 类型：玩家控制器 |



---

## 🔌 EventPlayerHintmessage

事件 "player_hintmessage"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerHintmessage\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `HintMessage` | `string` | get, set | 提示的可本地化字符串 <br/> 类型：字符串 |



---

## 🔌 EventPlayerHurt

事件 "player_hurt"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerHurt\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 受伤的玩家 <br/> 类型：玩家控制器与模型 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 受伤的玩家 <br/> 类型：玩家控制器与模型 |
| `UserId` | `int` | get, set | 受伤的玩家 <br/> 类型：玩家控制器与模型 |
| `AttackerController` | `CCSPlayerController` | get | 攻击的玩家 <br/> 类型：玩家控制器与模型 |
| `AttackerPawn` | `CCSPlayerPawn` | get | 攻击的玩家 <br/> 类型：玩家控制器与模型 |
| `Attacker` | `int` | get, set | 攻击的玩家 <br/> 类型：玩家控制器与模型 |
| `Health` | `byte` | get, set | 剩余生命值 <br/> 类型：字节 |
| `Armor` | `byte` | get, set | 剩余护甲值 <br/> 类型：字节 |
| `Weapon` | `string` | get, set | 攻击者使用的武器名称，若未使用则为“world”<br/>类型：字符串 |
| `DmgHealth` | `short` | get, set | 对健康造成的伤害 <br/> 类型：short |
| `DmgArmor` | `byte` | get, set | 对护甲造成的伤害 <br/> 类型: 字节 |
| `HitGroup` | `byte` | get, set | 被损坏的命中组 <br/> 类型：字节 |



---

## 🔌 EventPlayerInfo

事件 "player_info" 玩家更改了其名称

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | get, set | 玩家名称 <br/> 类型：字符串 |
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户ID（在服务器上唯一）<br/>类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户ID（在服务器上唯一）<br/>类型：玩家控制器 |
| `UserId` | `int` | get, set | 服务器上的用户ID（在服务器上唯一）<br/>类型：玩家控制器 |
| `SteamID` | `ulong` | get, set | 玩家网络（例如 Steam）ID <br/> 类型：uint64 |
| `Bot` | `bool` | get, set | 如果玩家是AI机器人则为true <br/> 类型：布尔值 |



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
| `EntityID` | `short` | get, set | 类型：短整型 |
| `X` | `float` | get, set | 类型：浮点数 |
| `Y` | `float` | get, set | 类型：浮点数 |
| `Z` | `float` | get, set | 类型：浮点数 |
| `Urgent` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventPlayerPingStop

事件 "player_ping_stop"

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

事件 "player_score" 玩家分数已更改

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerScore\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户ID <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户ID <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 服务器上的用户ID <br/> 类型：玩家控制器 |
| `Kills` | `short` | get, set | 击杀数 <br/> 类型：短整型 |
| `Deaths` | `short` | get, set | 死亡人数 <br/> 类型：短整型 |
| `Score` | `short` | get, set | 总游戏分数 <br/> 类型：短整型 |



---

## 🔌 EventPlayerShoot

事件 "player_shoot" 玩家开火

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerShoot\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 服务器上的用户ID <br/> 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 服务器上的用户ID <br/> 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 服务器上的用户ID <br/> 类型：玩家控制器与Pawn |
| `Weapon` | `byte` | get, set | 武器 ID <br/> 类型：字节 |
| `Mode` | `byte` | get, set | 武器模式 <br/> 类型：字节 |



---

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
| `Radius` | `int` | get, set | 类型：int |
| `Duration` | `float` | get, set | 类型：浮点数 |
| `Step` | `bool` | get, set | 类型：布尔值 |



---

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
| `InRestart` | `bool` | get, set | 如果存在待重启的情况，则为 true <br/> 类型：布尔值 |



---

## 🔌 EventPlayerStatsUpdated

事件 "player_stats_updated"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerStatsUpdated\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ForceUpload` | `bool` | get, set | 类型：布尔值 |



---

## 🔌 EventPlayerTeam

事件 "player_team"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventPlayerTeam\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 玩家 <br/> 类型：玩家控制器与 pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 玩家 <br/> 类型：玩家控制器与 pawn |
| `UserId` | `int` | get, set | 玩家 <br/> 类型：玩家控制器与 pawn |
| `Team` | `byte` | get, set | 团队标识 <br/> 类型：字节 |
| `OldTeam` | `byte` | get, set | 旧团队 ID <br/> 类型：字节 |
| `Disconnect` | `bool` | get, set | 团队变更，因为玩家断开连接 <br/> 类型：布尔值 |
| `Silent` | `bool` | get, set | 类型：布尔值 |
| `Name` | `string` | get, set | 类型：字符串 |
| `IsBot` | `bool` | get, set | 如果玩家是机器人则为 true <br/> 类型：布尔值 |



---

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

## 🔌 EventReadGameTitledata

事件 "read_game_titledata" 从个人资料中读取用户头衔数据

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventReadGameTitledata\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ControllerId` | `short` | get, set | 用户控制器标识 <br/> 类型：短整型 |



---

## 🔌 EventRepostXboxAchievements

事件 "repost_xbox_achievements"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRepostXboxAchievements\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SplitScreenPlayer` | `short` | get, set | 分屏 ID <br/> 类型：短整型 |



---

## 🔌 EventResetGameTitledata

事件 "reset_game_titledata" 重置用户称号数据；不自动写入个人资料

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventResetGameTitledata\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ControllerId` | `short` | get, set | 用户控制器标识 <br/> 类型：短整型 |



---

## 🔌 EventRoundAnnounceFinal

事件 "round_announce_final"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundAnnounceFinal\>`



---

## 🔌 EventRoundAnnounceLastRoundHalf

事件 "round_announce_last_round_half"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundAnnounceLastRoundHalf\>`



---

## 🔌 EventRoundAnnounceMatchPoint

事件 "round_announce_match_point"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundAnnounceMatchPoint\>`



---

## 🔌 EventRoundAnnounceMatchStart

事件 "round_announce_match_start"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundAnnounceMatchStart\>`



---

## 🔌 EventRoundAnnounceWarmup

事件 "round_announce_warmup"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundAnnounceWarmup\>`



---

## 🔌 EventRoundEnd

事件 "round_end"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundEnd\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Winner` | `byte` | get, set | 获胜的团队/用户 i <br/> 类型：字节 |
| `Reason` | `byte` | get, set | 团队获胜原因 <br/> 类型：字节 |
| `Message` | `string` | get, set | 回合结束消息 <br/> 类型：字符串 |
| `Time` | `float` | get, set | 类型：浮点数 |
| `Legacy` | `byte` | get, set | 服务器生成的旧值 <br/> 类型：字节 |
| `PlayerCount` | `short` | get, set | 回合结束时存活玩家总数，用于统计收集，在服务器上计算，当客户端处于回放模式时接收此消息时进行计算 <br/> 类型：short |
| `NoMusic` | `byte` | get, set | 如果已设置，则不播放回合结束音乐，因为操作仍在进行中 <br/> 类型：字节 |



---

## 🔌 EventRoundEndUploadStats

事件 "round_end_upload_stats"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundEndUploadStats\>`



---

## 🔌 EventRoundFreezeEnd

事件 "round_freeze_end"

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
| `Value` | `int` | get, set | 类型：长整型 |
| `MusickItMvps` | `int` | get, set | 类型：长整型 |
| `NoMusic` | `byte` | get, set | 类型：字节 |
| `MusickItID` | `int` | get, set | 类型：长整型 |



---

## 🔌 EventRoundOfficiallyEnded

事件“round_officially_ended”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundOfficiallyEnded\>`



---

## 🔌 EventRoundPoststart

事件 "round_poststart" 在所有其他回合重启操作之后发送

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundPoststart\>`



---

## 🔌 EventRoundPrestart

事件 "round_prestart" 在所有其他回合重启操作之前发送

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundPrestart\>`



---

## 🔌 EventRoundStart

事件 "round_start"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundStart\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TimeLimit` | `int` | get, set | 轮次时间限制（以秒为单位）<br/>类型：长整型 |
| `FragLimit` | `int` | get, set | 碎片限制（以秒为单位）<br/>类型：长整型 |
| `Objective` | `string` | get, set | 轮次目标 <br/> 类型：字符串 |



---

## 🔌 EventRoundStartPostNav

事件 "round_start_post_nav"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundStartPostNav\>`



---

## 🔌 EventRoundStartPreEntity

事件 "round_start_pre_entity"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundStartPreEntity\>`



---

## 🔌 EventRoundTimeWarning

事件 "round_time_warning"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventRoundTimeWarning\>`



---

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
| `Category` | `short` | get, set | 类型：短整型 |
| `Rank` | `short` | get, set | 类型：短整型 |



---

## 🔌 EventServerCvar

事件“server_cvar”表明服务器控制台变量已更改

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventServerCvar\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CVarName` | `string` | get, set | cvar 名称，例如 "mp_roundtime" <br/> 类型：字符串 |
| `CVarValue` | `string` | get, set | 新的cvar值 <br/> 类型：字符串 |



---

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

## 🔌 EventServerPreShutdown

事件 "server_pre_shutdown" 服务器即将关闭

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventServerPreShutdown\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Reason` | `string` | get, set | 服务器即将关闭的原因 <br/> 类型：字符串 |



---

## 🔌 EventServerShutdown

事件 "server_shutdown" 服务器已关闭

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventServerShutdown\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Reason` | `string` | get, set | 服务器关闭原因 <br/> 类型：字符串 |



---

## 🔌 EventServerSpawn

事件 "server_spawn" 在服务器启动时发送一次

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventServerSpawn\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Hostname` | `string` | get, set | 主机名 <br/> 类型：字符串 |
| `Address` | `string` | get, set | 主机名、IP或DNS名称 <br/> 类型：字符串 |
| `Port` | `short` | get, set | 服务器端口 <br/> 类型：短整型 |
| `Game` | `string` | get, set | 游戏目录 <br/> 类型：字符串 |
| `MapName` | `string` | get, set | 映射名称 <br/> 类型：字符串 |
| `AddonName` | `string` | get, set | 插件名称 <br/> 类型：字符串 |
| `MaxPlayers` | `int` | get, set | 最大玩家数 <br/> 类型：长整型 |
| `Os` | `string` | get, set | WIN32, LINUX <br/> 类型：字符串 |
| `Dedicated` | `bool` | get, set | 如果为专用服务器 <br/> 类型：布尔值 |
| `Password` | `bool` | get, set | 如果受密码保护则为 true <br/> 类型：布尔值 |



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

事件 "show_deathpanel"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventShowDeathpanel\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `VictimController` | `CCSPlayerController` | get | 被击杀者的结束索引 <br/> 类型：玩家控制器与Pawn |
| `VictimPawn` | `CCSPlayerPawn` | get | 被击杀者的结束索引 <br/> 类型：玩家控制器与Pawn |
| `Victim` | `int` | get, set | 被击杀者的结束索引 <br/> 类型：玩家控制器与Pawn |
| `Killer` | `nint` | get, set | 杀手实体的实体索引 <br/> 类型：ehandle |
| `KillerControllerController` | `CCSPlayerController` | get | 类型：玩家控制器 |
| `KillerControllerPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器 |
| `KillerController` | `int` | get, set | 类型：玩家控制器 |
| `HitsTaken` | `short` | get, set | 类型：短整型 |
| `DamageTaken` | `short` | get, set | 类型：短整型 |
| `HitsGiven` | `short` | get, set | 类型：短整型 |
| `DamageGiven` | `short` | get, set | 类型：短整型 |



---

## 🔌 EventShowSurvivalRespawnStatus

事件 "show_survival_respawn_status"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventShowSurvivalRespawnStatus\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `LocToken` | `string` | get, set | 类型：字符串 |
| `Duration` | `int` | get, set | 类型：长整型 |
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |



---

## 🔌 EventSilencerDetach

事件“消音器拆卸”

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

## 🔌 EventSilencerOn

事件“消音器开启”

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
| `EntityID` | `short` | get, set | 类型：短整型 |
| `X` | `float` | get, set | 类型：浮点数 |
| `Y` | `float` | get, set | 类型：浮点数 |
| `Z` | `float` | get, set | 类型：浮点数 |



---

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
| `UserIdController` | `CCSPlayerController` | get | 观战玩家 <br/> 类型：玩家控制器与模型 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 观战玩家 <br/> 类型：玩家控制器与模型 |
| `UserId` | `int` | get, set | 观战玩家 <br/> 类型：玩家控制器与模型 |



---

## 🔌 EventSpecTargetUpdated

事件 "spec_target_updated"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSpecTargetUpdated\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 观战玩家 <br/> 类型：玩家控制器与模型 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 观战玩家 <br/> 类型：玩家控制器与模型 |
| `UserId` | `int` | get, set | 观战玩家 <br/> 类型：玩家控制器与模型 |
| `Target` | `nint` | get, set | 目标 ehandle <br/> 类型：ehandle |



---

## 🔌 EventStartHalftime

事件 "start_halftime"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventStartHalftime\>`



---

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

事件 "survival_announce_phase"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSurvivalAnnouncePhase\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Phase` | `short` | get, set | 阶段 # <br/> 类型：short |



---

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

## 🔌 EventSurvivalParadropBreak

事件 "survival_paradrop_break"

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

事件 "switch_team"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventSwitchTeam\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `NumPlayers` | `short` | get, set | 双方T和CT阵营的活跃玩家数量 <br/> 类型：short |
| `NumSpectators` | `short` | get, set | 观众人数 <br/> 类型: short |
| `AvgRank` | `short` | get, set | 人类玩家的平均排名 <br/> 类型：short |
| `NumTSlotsFree` | `short` | get, set | 类型：短整型 |
| `NumCTSlotsFree` | `short` | get, set | 类型：短整型 |



---

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
| `EntityID` | `short` | get, set | 类型：短整型 |
| `X` | `float` | get, set | 类型：浮点数 |
| `Y` | `float` | get, set | 类型：浮点数 |
| `Z` | `float` | get, set | 类型：浮点数 |



---

## 🔌 EventTeamInfo

事件 "team_info" 的团队信息

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTeamInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TeamID` | `byte` | get, set | 唯一团队标识 <br/> 类型：字节 |
| `Teamname` | `string` | get, set | 团队名称，例如 "Team Blue" <br/> 类型：字符串 |



---

## 🔌 EventTeamIntroEnd

事件 "team_intro_end"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTeamIntroEnd\>`



---

## 🔌 EventTeamIntroStart

事件 "team_intro_start"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTeamIntroStart\>`



---

## 🔌 EventTeamScore

事件 "team_score" 团队分数已更改

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTeamScore\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TeamID` | `byte` | get, set | 团队标识 <br/> 类型：字节 |
| `Score` | `short` | get, set | 团队总分 <br/> 类型：短整型 |



---

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
| `ToTeam` | `byte` | get, set | 类型：字节 |



---

## 🔌 EventTeamplayBroadcastAudio

事件 "teamplay_broadcast_audio" 向团队中的所有人播放声音

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTeamplayBroadcastAudio\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Team` | `byte` | get, set | 唯一团队标识 <br/> 类型：字节 |
| `Sound` | `string` | get, set | 要发出的声音的名称 <br/> 类型：字符串 |



---

## 🔌 EventTeamplayRoundStart

事件 "teamplay_round_start" 轮次重启

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTeamplayRoundStart\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `FullReset` | `bool` | get, set | 这是否为地图的完全重置 <br/> 类型: bool |



---

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

## 🔌 EventTrialTimeExpired

事件 "trial_time_expired"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventTrialTimeExpired\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 时间已耗尽的玩家 <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 时间已耗尽的玩家 <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 时间已耗尽的玩家 <br/> 类型：玩家控制器 |



---

## 🔌 EventUgcFileDownloadFinished

事件 "ugc_file_download_finished"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventUgcFileDownloadFinished\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `HContent` | `ulong` | get, set | 此特定内容（可能是图像或地图）的ID <br/> 类型：uint64 |



---

## 🔌 EventUgcFileDownloadStart

事件 "ugc_file_download_start"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventUgcFileDownloadStart\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `HContent` | `ulong` | get, set | 此特定内容（可能是图像或地图）的ID <br/> 类型：uint64 |
| `PublishedFileId` | `ulong` | get, set | 关联内容包的ID <br/> 类型：uint64 |



---

## 🔌 EventUgcMapDownloadError

事件 "ugc_map_download_error"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventUgcMapDownloadError\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PublishedFileId` | `ulong` | get, set | 类型：uint64 |
| `ErrorCode` | `int` | get, set | 类型：长整型 |



---

## 🔌 EventUgcMapInfoReceived

事件 "ugc_map_info_received"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventUgcMapInfoReceived\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PublishedFileId` | `ulong` | get, set | 类型：uint64 |



---

## 🔌 EventUgcMapUnsubscribed

事件 "ugc_map_unsubscribed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventUgcMapUnsubscribed\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PublishedFileId` | `ulong` | get, set | 类型：uint64 |



---

## 🔌 EventUpdateMatchmakingStats

事件 "update_matchmaking_stats"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventUpdateMatchmakingStats\>`



---

## 🔌 EventUserDataDownloaded

当从 Steam 或 Xbox Live 下载成就/统计数据时触发 "user_data_downloaded" 事件

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
| `UserIdController` | `CCSPlayerController` | get | 玩家（VIP身份）<br/>类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 玩家（VIP身份）<br/>类型：玩家控制器 |
| `UserId` | `int` | get, set | 玩家（VIP身份）<br/>类型：玩家控制器 |



---

## 🔌 EventVipKilled

事件 "vip_killed"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVipKilled\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 玩家（VIP身份）<br/>类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 玩家（VIP身份）<br/>类型：玩家控制器 |
| `UserId` | `int` | get, set | 玩家（VIP身份）<br/>类型：玩家控制器 |
| `AttackerController` | `CCSPlayerController` | get | 击杀VIP的用户ID <br/> 类型：玩家控制器 |
| `AttackerPawn` | `CCSPlayerPawn` | get | 击杀VIP的用户ID <br/> 类型：玩家控制器 |
| `Attacker` | `int` | get, set | 击杀VIP的用户ID <br/> 类型：玩家控制器 |



---

## 🔌 EventVoteCast

事件 "vote_cast"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVoteCast\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `VoteOption` | `byte` | get, set | 玩家投票的选项 <br/> 类型：字节 |
| `Team` | `short` | get, set | 类型：短整型 |
| `UserIdController` | `CCSPlayerController` | get | 投票的玩家 <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 投票的玩家 <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 投票的玩家 <br/> 类型：玩家控制器 |



---

## 🔌 EventVoteCastNo

事件 "vote_cast_no"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVoteCastNo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Team` | `byte` | get, set | 类型：字节 |
| `EntityID` | `int` | get, set | 投票者的实体标识 <br/> 类型：长整型 |



---

## 🔌 EventVoteCastYes

事件 "vote_cast_yes"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVoteCastYes\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Team` | `byte` | get, set | 类型：字节 |
| `EntityID` | `int` | get, set | 投票者的实体标识 <br/> 类型：长整型 |



---

## 🔌 EventVoteChanged

事件 "vote_changed"

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

事件 "vote_ended"

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

事件 "vote_options"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventVoteOptions\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Count` | `byte` | get, set | 选项数量 - 最多为 MAX_VOTE_OPTIONS <br/> 类型: byte |
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

事件 "vote_started"

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
| `Initiator` | `int` | get, set | 发起投票的玩家实体ID <br/> 类型：长整型 |



---

## 🔌 EventWarmupEnd

事件 "warmup_end"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventWarmupEnd\>`



---

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
| `Weapon` | `string` | get, set | 武器名称使用 <br/> 类型：字符串 |
| `Silenced` | `bool` | get, set | 是否武器消音 <br/> 类型：布尔值 |



---

## 🔌 EventWeaponFireOnEmpty

事件“武器空仓射击”

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventWeaponFireOnEmpty\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 类型：玩家控制器与Pawn |
| `Weapon` | `string` | get, set | 武器名称使用 <br/> 类型：字符串 |



---

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
| `UserIdController` | `CCSPlayerController` | get | 此事件所适用的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserIdPawn` | `CCSPlayerPawn` | get | 此事件所适用的玩家 <br/> 类型：玩家控制器与Pawn |
| `UserId` | `int` | get, set | 此事件所适用的玩家 <br/> 类型：玩家控制器与Pawn |
| `Mode` | `byte` | get, set | EWeaponHudSelectionMode (切换 / 拾取 / 丢弃) <br/> 类型: 字节 |
| `EntIndex` | `int` | get, set | 武器实体索引 <br/> 类型：长整型 |



---

## 🔌 EventWriteGameTitledata

事件 "write_game_titledata" 将用户头衔数据写入个人资料

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventWriteGameTitledata\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ControllerId` | `short` | get, set | 用户控制器标识 <br/> 类型：短整型 |



---

## 🔌 EventWriteProfileData

事件 "write_profile_data"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventWriteProfileData\>`



---

