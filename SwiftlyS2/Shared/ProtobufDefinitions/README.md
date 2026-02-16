# 📚 ProtobufDefinitions

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

共 830 个定义

## 📋 目录

- 🔌 [AccountActivity](#accountactivity)
- 📋 [Bidirectional_Messages](#bidirectional_messages)
- 📋 [Bidirectional_Messages_LowFrequency](#bidirectional_messages_lowfrequency)
- 🔌 [C2S_CONNECTION_Message](#c2s_connection_message)
- 🔌 [C2S_CONNECT_Message](#c2s_connect_message)
- 🔌 [C2S_CONNECT_SameProcessCheck](#c2s_connect_sameprocesscheck)
- 🔌 [CAttribute_String](#cattribute_string)
- 🔌 [CBaseUserCmdExecutionNotes](#cbaseusercmdexecutionnotes)
- 🔌 [CBaseUserCmdPB](#cbaseusercmdpb)
- 🔌 [CBidirMsg_PredictionEvent](#cbidirmsg_predictionevent)
- 📋 [CBidirMsg_PredictionEvent_ESyncType](#cbidirmsg_predictionevent_esynctype)
- 🔌 [CBidirMsg_RebroadcastGameEvent](#cbidirmsg_rebroadcastgameevent)
- 🔌 [CBidirMsg_RebroadcastSource](#cbidirmsg_rebroadcastsource)
- 🔌 [CCLCMsg_BaselineAck](#cclcmsg_baselineack)
- 🔌 [CCLCMsg_ClientInfo](#cclcmsg_clientinfo)
- 🔌 [CCLCMsg_CmdKeyValues](#cclcmsg_cmdkeyvalues)
- 🔌 [CCLCMsg_Diagnostic](#cclcmsg_diagnostic)
- 🔌 [CCLCMsg_HltvFixupOperatorTick](#cclcmsg_hltvfixupoperatortick)
- 🔌 [CCLCMsg_HltvReplay](#cclcmsg_hltvreplay)
- 🔌 [CCLCMsg_ListenEvents](#cclcmsg_listenevents)
- 🔌 [CCLCMsg_LoadingProgress](#cclcmsg_loadingprogress)
- 🔌 [CCLCMsg_Move](#cclcmsg_move)
- 🔌 [CCLCMsg_RconServerDetails](#cclcmsg_rconserverdetails)
- 🔌 [CCLCMsg_RequestPause](#cclcmsg_requestpause)
- 🔌 [CCLCMsg_RespondCvarValue](#cclcmsg_respondcvarvalue)
- 🔌 [CCLCMsg_ServerStatus](#cclcmsg_serverstatus)
- 🔌 [CCLCMsg_SplitPlayerConnect](#cclcmsg_splitplayerconnect)
- 🔌 [CCLCMsg_SplitPlayerDisconnect](#cclcmsg_splitplayerdisconnect)
- 🔌 [CCLCMsg_VoiceData](#cclcmsg_voicedata)
- 🔌 [CCSPredictionEvent_AddAimPunch](#ccspredictionevent_addaimpunch)
- 🔌 [CCSPredictionEvent_DamageTag](#ccspredictionevent_damagetag)
- 🔌 [CCSUsrMsgPreMatchSayText](#ccsusrmsgprematchsaytext)
- 🔌 [CCSUsrMsg_AchievementEvent](#ccsusrmsg_achievementevent)
- 🔌 [CCSUsrMsg_AdjustMoney](#ccsusrmsg_adjustmoney)
- 🔌 [CCSUsrMsg_AmmoDenied](#ccsusrmsg_ammodenied)
- 🔌 [CCSUsrMsg_BarTime](#ccsusrmsg_bartime)
- 🔌 [CCSUsrMsg_CallVoteFailed](#ccsusrmsg_callvotefailed)
- 🔌 [CCSUsrMsg_ClientInfo](#ccsusrmsg_clientinfo)
- 🔌 [CCSUsrMsg_CloseCaption](#ccsusrmsg_closecaption)
- 🔌 [CCSUsrMsg_CloseCaptionDirect](#ccsusrmsg_closecaptiondirect)
- 🔌 [CCSUsrMsg_CounterStrafe](#ccsusrmsg_counterstrafe)
- 🔌 [CCSUsrMsg_CurrentRoundOdds](#ccsusrmsg_currentroundodds)
- 🔌 [CCSUsrMsg_CurrentTimescale](#ccsusrmsg_currenttimescale)
- 🔌 [CCSUsrMsg_Damage](#ccsusrmsg_damage)
- 🔌 [CCSUsrMsg_DamagePrediction](#ccsusrmsg_damageprediction)
- 🔌 [CCSUsrMsg_DeepStats](#ccsusrmsg_deepstats)
- 🔌 [CCSUsrMsg_DesiredTimescale](#ccsusrmsg_desiredtimescale)
- 🔌 [CCSUsrMsg_DisconnectToLobby](#ccsusrmsg_disconnecttolobby)
- 🔌 [CCSUsrMsg_EndOfMatchAllPlayersData](#ccsusrmsg_endofmatchallplayersdata)
- 🔌 [CCSUsrMsg_EndOfMatchAllPlayersData_Accolade](#ccsusrmsg_endofmatchallplayersdata_accolade)
- 🔌 [CCSUsrMsg_EndOfMatchAllPlayersData_PlayerData](#ccsusrmsg_endofmatchallplayersdata_playerdata)
- 🔌 [CCSUsrMsg_EntityOutlineHighlight](#ccsusrmsg_entityoutlinehighlight)
- 🔌 [CCSUsrMsg_Fade](#ccsusrmsg_fade)
- 🔌 [CCSUsrMsg_GameTitle](#ccsusrmsg_gametitle)
- 🔌 [CCSUsrMsg_Geiger](#ccsusrmsg_geiger)
- 🔌 [CCSUsrMsg_HintText](#ccsusrmsg_hinttext)
- 🔌 [CCSUsrMsg_HudMsg](#ccsusrmsg_hudmsg)
- 🔌 [CCSUsrMsg_HudText](#ccsusrmsg_hudtext)
- 🔌 [CCSUsrMsg_ItemDrop](#ccsusrmsg_itemdrop)
- 🔌 [CCSUsrMsg_ItemPickup](#ccsusrmsg_itempickup)
- 🔌 [CCSUsrMsg_KeyHintText](#ccsusrmsg_keyhinttext)
- 🔌 [CCSUsrMsg_KillCam](#ccsusrmsg_killcam)
- 🔌 [CCSUsrMsg_MarkAchievement](#ccsusrmsg_markachievement)
- 🔌 [CCSUsrMsg_MatchEndConditions](#ccsusrmsg_matchendconditions)
- 🔌 [CCSUsrMsg_MatchStatsUpdate](#ccsusrmsg_matchstatsupdate)
- 🔌 [CCSUsrMsg_PlayerDecalDigitalSignature](#ccsusrmsg_playerdecaldigitalsignature)
- 🔌 [CCSUsrMsg_PlayerStatsUpdate](#ccsusrmsg_playerstatsupdate)
- 🔌 [CCSUsrMsg_PlayerStatsUpdate_Stat](#ccsusrmsg_playerstatsupdate_stat)
- 🔌 [CCSUsrMsg_PostRoundDamageReport](#ccsusrmsg_postrounddamagereport)
- 🔌 [CCSUsrMsg_ProcessSpottedEntityUpdate](#ccsusrmsg_processspottedentityupdate)
- 🔌 [CCSUsrMsg_ProcessSpottedEntityUpdate_SpottedEntityUpdate](#ccsusrmsg_processspottedentityupdate_spottedentityupdate)
- 🔌 [CCSUsrMsg_QuestProgress](#ccsusrmsg_questprogress)
- 🔌 [CCSUsrMsg_RadioText](#ccsusrmsg_radiotext)
- 🔌 [CCSUsrMsg_RawAudio](#ccsusrmsg_rawaudio)
- 🔌 [CCSUsrMsg_RecurringMissionSchema](#ccsusrmsg_recurringmissionschema)
- 🔌 [CCSUsrMsg_ReloadEffect](#ccsusrmsg_reloadeffect)
- 🔌 [CCSUsrMsg_ReportHit](#ccsusrmsg_reporthit)
- 🔌 [CCSUsrMsg_RequestState](#ccsusrmsg_requeststate)
- 🔌 [CCSUsrMsg_ResetHud](#ccsusrmsg_resethud)
- 🔌 [CCSUsrMsg_RoundBackupFilenames](#ccsusrmsg_roundbackupfilenames)
- 🔌 [CCSUsrMsg_RoundEndReportData](#ccsusrmsg_roundendreportdata)
- 🔌 [CCSUsrMsg_RoundEndReportData_InitialConditions](#ccsusrmsg_roundendreportdata_initialconditions)
- 🔌 [CCSUsrMsg_RoundEndReportData_RerEvent](#ccsusrmsg_roundendreportdata_rerevent)
- 🔌 [CCSUsrMsg_RoundEndReportData_RerEvent_Damage](#ccsusrmsg_roundendreportdata_rerevent_damage)
- 🔌 [CCSUsrMsg_RoundEndReportData_RerEvent_Objective](#ccsusrmsg_roundendreportdata_rerevent_objective)
- 🔌 [CCSUsrMsg_RoundEndReportData_RerEvent_Victim](#ccsusrmsg_roundendreportdata_rerevent_victim)
- 🔌 [CCSUsrMsg_Rumble](#ccsusrmsg_rumble)
- 🔌 [CCSUsrMsg_SSUI](#ccsusrmsg_ssui)
- 🔌 [CCSUsrMsg_ScoreLeaderboardData](#ccsusrmsg_scoreleaderboarddata)
- 🔌 [CCSUsrMsg_SendAudio](#ccsusrmsg_sendaudio)
- 🔌 [CCSUsrMsg_SendLastKillerDamageToClient](#ccsusrmsg_sendlastkillerdamagetoclient)
- 🔌 [CCSUsrMsg_SendPlayerItemDrops](#ccsusrmsg_sendplayeritemdrops)
- 🔌 [CCSUsrMsg_SendPlayerItemFound](#ccsusrmsg_sendplayeritemfound)
- 🔌 [CCSUsrMsg_SendPlayerLoadout](#ccsusrmsg_sendplayerloadout)
- 🔌 [CCSUsrMsg_SendPlayerLoadout_LoadoutItem](#ccsusrmsg_sendplayerloadout_loadoutitem)
- 🔌 [CCSUsrMsg_ServerRankRevealAll](#ccsusrmsg_serverrankrevealall)
- 🔌 [CCSUsrMsg_ServerRankUpdate](#ccsusrmsg_serverrankupdate)
- 🔌 [CCSUsrMsg_ServerRankUpdate_RankUpdate](#ccsusrmsg_serverrankupdate_rankupdate)
- 🔌 [CCSUsrMsg_Shake](#ccsusrmsg_shake)
- 🔌 [CCSUsrMsg_ShootInfo](#ccsusrmsg_shootinfo)
- 🔌 [CCSUsrMsg_ShowMenu](#ccsusrmsg_showmenu)
- 🔌 [CCSUsrMsg_StopSpectatorMode](#ccsusrmsg_stopspectatormode)
- 🔌 [CCSUsrMsg_SurvivalStats](#ccsusrmsg_survivalstats)
- 🔌 [CCSUsrMsg_SurvivalStats_Damage](#ccsusrmsg_survivalstats_damage)
- 🔌 [CCSUsrMsg_SurvivalStats_Fact](#ccsusrmsg_survivalstats_fact)
- 🔌 [CCSUsrMsg_SurvivalStats_Placement](#ccsusrmsg_survivalstats_placement)
- 🔌 [CCSUsrMsg_Train](#ccsusrmsg_train)
- 🔌 [CCSUsrMsg_UpdateScreenHealthBar](#ccsusrmsg_updatescreenhealthbar)
- 🔌 [CCSUsrMsg_VGUIMenu](#ccsusrmsg_vguimenu)
- 🔌 [CCSUsrMsg_VGUIMenu_Keys](#ccsusrmsg_vguimenu_keys)
- 🔌 [CCSUsrMsg_VoiceMask](#ccsusrmsg_voicemask)
- 🔌 [CCSUsrMsg_VoiceMask_PlayerMask](#ccsusrmsg_voicemask_playermask)
- 🔌 [CCSUsrMsg_VoteFailed](#ccsusrmsg_votefailed)
- 🔌 [CCSUsrMsg_VotePass](#ccsusrmsg_votepass)
- 🔌 [CCSUsrMsg_VoteSetup](#ccsusrmsg_votesetup)
- 🔌 [CCSUsrMsg_VoteStart](#ccsusrmsg_votestart)
- 🔌 [CCSUsrMsg_WeaponSound](#ccsusrmsg_weaponsound)
- 🔌 [CCSUsrMsg_XRankGet](#ccsusrmsg_xrankget)
- 🔌 [CCSUsrMsg_XRankUpd](#ccsusrmsg_xrankupd)
- 🔌 [CCSUsrMsg_XpUpdate](#ccsusrmsg_xpupdate)
- 🔌 [CChinaAgreementSessions_StartAgreementSessionInGame_Request](#cchinaagreementsessions_startagreementsessioningame_request)
- 🔌 [CChinaAgreementSessions_StartAgreementSessionInGame_Response](#cchinaagreementsessions_startagreementsessioningame_response)
- 🔌 [CClientHeaderOverwatchEvidence](#cclientheaderoverwatchevidence)
- 🔌 [CClientMsg_ClientUIEvent](#cclientmsg_clientuievent)
- 🔌 [CClientMsg_CustomGameEvent](#cclientmsg_customgameevent)
- 🔌 [CClientMsg_CustomGameEventBounce](#cclientmsg_customgameeventbounce)
- 🔌 [CClientMsg_DevPaletteVisibilityChangedEvent](#cclientmsg_devpalettevisibilitychangedevent)
- 🔌 [CClientMsg_ListenForResponseFound](#cclientmsg_listenforresponsefound)
- 🔌 [CClientMsg_RotateAnchor](#cclientmsg_rotateanchor)
- 🔌 [CClientMsg_WorldUIControllerHasPanelChangedEvent](#cclientmsg_worlduicontrollerhaspanelchangedevent)
- 🔌 [CCommunity_GamePersonalDataCategoryInfo](#ccommunity_gamepersonaldatacategoryinfo)
- 🔌 [CCommunity_GetGamePersonalDataCategories_Request](#ccommunity_getgamepersonaldatacategories_request)
- 🔌 [CCommunity_GetGamePersonalDataCategories_Response](#ccommunity_getgamepersonaldatacategories_response)
- 🔌 [CCommunity_GetGamePersonalDataEntries_Request](#ccommunity_getgamepersonaldataentries_request)
- 🔌 [CCommunity_GetGamePersonalDataEntries_Response](#ccommunity_getgamepersonaldataentries_response)
- 🔌 [CCommunity_TerminateGamePersonalDataEntries_Request](#ccommunity_terminategamepersonaldataentries_request)
- 🔌 [CCommunity_TerminateGamePersonalDataEntries_Response](#ccommunity_terminategamepersonaldataentries_response)
- 🔌 [CDataGCCStrike15_v2_MatchInfo](#cdatagccstrike15_v2_matchinfo)
- 🔌 [CDataGCCStrike15_v2_TournamentGroup](#cdatagccstrike15_v2_tournamentgroup)
- 🔌 [CDataGCCStrike15_v2_TournamentGroupTeam](#cdatagccstrike15_v2_tournamentgroupteam)
- 🔌 [CDataGCCStrike15_v2_TournamentGroup_Picks](#cdatagccstrike15_v2_tournamentgroup_picks)
- 🔌 [CDataGCCStrike15_v2_TournamentInfo](#cdatagccstrike15_v2_tournamentinfo)
- 🔌 [CDataGCCStrike15_v2_TournamentMatchDraft](#cdatagccstrike15_v2_tournamentmatchdraft)
- 🔌 [CDataGCCStrike15_v2_TournamentMatchDraft_Entry](#cdatagccstrike15_v2_tournamentmatchdraft_entry)
- 🔌 [CDataGCCStrike15_v2_TournamentSection](#cdatagccstrike15_v2_tournamentsection)
- 🔌 [CDemoAnimationData](#cdemoanimationdata)
- 🔌 [CDemoAnimationHeader](#cdemoanimationheader)
- 🔌 [CDemoClassInfo](#cdemoclassinfo)
- 🔌 [CDemoClassInfo_class_t](#cdemoclassinfo_class_t)
- 🔌 [CDemoConsoleCmd](#cdemoconsolecmd)
- 🔌 [CDemoCustomData](#cdemocustomdata)
- 🔌 [CDemoCustomDataCallbacks](#cdemocustomdatacallbacks)
- 🔌 [CDemoFileHeader](#cdemofileheader)
- 🔌 [CDemoFileInfo](#cdemofileinfo)
- 🔌 [CDemoFullPacket](#cdemofullpacket)
- 🔌 [CDemoPacket](#cdemopacket)
- 🔌 [CDemoRecovery](#cdemorecovery)
- 🔌 [CDemoRecovery_DemoInitialSpawnGroupEntry](#cdemorecovery_demoinitialspawngroupentry)
- 🔌 [CDemoSaveGame](#cdemosavegame)
- 🔌 [CDemoSendTables](#cdemosendtables)
- 🔌 [CDemoSpawnGroups](#cdemospawngroups)
- 🔌 [CDemoSpawnGroupsHLTVBroadcast](#cdemospawngroupshltvbroadcast)
- 🔌 [CDemoStop](#cdemostop)
- 🔌 [CDemoStringTables](#cdemostringtables)
- 🔌 [CDemoStringTables_items_t](#cdemostringtables_items_t)
- 🔌 [CDemoStringTables_table_t](#cdemostringtables_table_t)
- 🔌 [CDemoSyncTick](#cdemosynctick)
- 🔌 [CDemoUserCmd](#cdemousercmd)
- 🔌 [CEconItemPreviewDataBlock](#ceconitempreviewdatablock)
- 🔌 [CEconItemPreviewDataBlock_Sticker](#ceconitempreviewdatablock_sticker)
- 🔌 [CEngineGotvSyncPacket](#cenginegotvsyncpacket)
- 🔌 [CEntityMessageDoSpark](#centitymessagedospark)
- 🔌 [CEntityMessageFixAngle](#centitymessagefixangle)
- 🔌 [CEntityMessagePlayJingle](#centitymessageplayjingle)
- 🔌 [CEntityMessagePropagateForce](#centitymessagepropagateforce)
- 🔌 [CEntityMessageRemoveAllDecals](#centitymessageremovealldecals)
- 🔌 [CEntityMessageScreenOverlay](#centitymessagescreenoverlay)
- 🔌 [CEntityMsg](#centitymsg)
- 🔌 [CGCStorePurchaseInit_LineItem](#cgcstorepurchaseinit_lineitem)
- 🔌 [CGCToGCMsgMasterAck](#cgctogcmsgmasterack)
- 🔌 [CGCToGCMsgMasterAck_Response](#cgctogcmsgmasterack_response)
- 🔌 [CGCToGCMsgMasterStartupComplete](#cgctogcmsgmasterstartupcomplete)
- 🔌 [CGCToGCMsgRouted](#cgctogcmsgrouted)
- 🔌 [CGCToGCMsgRoutedReply](#cgctogcmsgroutedreply)
- 🔌 [CGameInfo](#cgameinfo)
- 🔌 [CGameInfo_CCSGameInfo](#cgameinfo_ccsgameinfo)
- 🔌 [CGameInfo_CDotaGameInfo](#cgameinfo_cdotagameinfo)
- 🔌 [CGameInfo_CDotaGameInfo_CHeroSelectEvent](#cgameinfo_cdotagameinfo_cheroselectevent)
- 🔌 [CGameInfo_CDotaGameInfo_CPlayerInfo](#cgameinfo_cdotagameinfo_cplayerinfo)
- 🔌 [CGameServers_AggregationQuery_Request](#cgameservers_aggregationquery_request)
- 🔌 [CGameServers_AggregationQuery_Response](#cgameservers_aggregationquery_response)
- 🔌 [CGameServers_AggregationQuery_Response_Group](#cgameservers_aggregationquery_response_group)
- 🔌 [CInButtonStatePB](#cinbuttonstatepb)
- 📋 [CLC_Messages](#clc_messages)
- 🔌 [CMsgAccountDetails](#cmsgaccountdetails)
- 🔌 [CMsgAcknowledgeRentalExpiration](#cmsgacknowledgerentalexpiration)
- 🔌 [CMsgAdjustEquipSlot](#cmsgadjustequipslot)
- 🔌 [CMsgAdjustEquipSlots](#cmsgadjustequipslots)
- 🔌 [CMsgApplyEggEssence](#cmsgapplyeggessence)
- 🔌 [CMsgApplyPennantUpgrade](#cmsgapplypennantupgrade)
- 🔌 [CMsgApplyStatTrakSwap](#cmsgapplystattrakswap)
- 🔌 [CMsgApplySticker](#cmsgapplysticker)
- 🔌 [CMsgApplyStrangePart](#cmsgapplystrangepart)
- 🔌 [CMsgCStrike15Welcome](#cmsgcstrike15welcome)
- 🔌 [CMsgCasketItem](#cmsgcasketitem)
- 🔌 [CMsgClearDecalsForEntityEvent](#cmsgcleardecalsforentityevent)
- 🔌 [CMsgClearEntityDecalsEvent](#cmsgclearentitydecalsevent)
- 🔌 [CMsgClearWorldDecalsEvent](#cmsgclearworlddecalsevent)
- 🔌 [CMsgClientHello](#cmsgclienthello)
- 🔌 [CMsgClientWelcome](#cmsgclientwelcome)
- 🔌 [CMsgClientWelcome_Location](#cmsgclientwelcome_location)
- 🔌 [CMsgConVarValue](#cmsgconvarvalue)
- 🔌 [CMsgConnectionStatus](#cmsgconnectionstatus)
- 🔌 [CMsgConsumableExhausted](#cmsgconsumableexhausted)
- 🔌 [CMsgCsgoSteamUserStatChange](#cmsgcsgosteamuserstatchange)
- 🔌 [CMsgDevNewItemRequest](#cmsgdevnewitemrequest)
- 🔌 [CMsgEffectData](#cmsgeffectdata)
- 🔌 [CMsgGCBannedWord](#cmsggcbannedword)
- 🔌 [CMsgGCBannedWordListRequest](#cmsggcbannedwordlistrequest)
- 🔌 [CMsgGCBannedWordListResponse](#cmsggcbannedwordlistresponse)
- 🔌 [CMsgGCCStrike15_ClientDeepStats](#cmsggccstrike15_clientdeepstats)
- 🔌 [CMsgGCCStrike15_ClientDeepStats_DeepStatsMatch](#cmsggccstrike15_clientdeepstats_deepstatsmatch)
- 🔌 [CMsgGCCStrike15_ClientDeepStats_DeepStatsRange](#cmsggccstrike15_clientdeepstats_deepstatsrange)
- 🔌 [CMsgGCCStrike15_GotvSyncPacket](#cmsggccstrike15_gotvsyncpacket)
- 🔌 [CMsgGCCStrike15_v2_AccountPrivacySettings](#cmsggccstrike15_v2_accountprivacysettings)
- 🔌 [CMsgGCCStrike15_v2_AccountPrivacySettings_Setting](#cmsggccstrike15_v2_accountprivacysettings_setting)
- 🔌 [CMsgGCCStrike15_v2_Account_RequestCoPlays](#cmsggccstrike15_v2_account_requestcoplays)
- 🔌 [CMsgGCCStrike15_v2_Account_RequestCoPlays_Player](#cmsggccstrike15_v2_account_requestcoplays_player)
- 🔌 [CMsgGCCStrike15_v2_AcknowledgePenalty](#cmsggccstrike15_v2_acknowledgepenalty)
- 🔌 [CMsgGCCStrike15_v2_BetaEnrollment](#cmsggccstrike15_v2_betaenrollment)
- 🔌 [CMsgGCCStrike15_v2_Client2GCEconPreviewDataBlockRequest](#cmsggccstrike15_v2_client2gceconpreviewdatablockrequest)
- 🔌 [CMsgGCCStrike15_v2_Client2GCEconPreviewDataBlockResponse](#cmsggccstrike15_v2_client2gceconpreviewdatablockresponse)
- 🔌 [CMsgGCCStrike15_v2_Client2GCRequestPrestigeCoin](#cmsggccstrike15_v2_client2gcrequestprestigecoin)
- 🔌 [CMsgGCCStrike15_v2_Client2GCStreamUnlock](#cmsggccstrike15_v2_client2gcstreamunlock)
- 🔌 [CMsgGCCStrike15_v2_Client2GCTextMsg](#cmsggccstrike15_v2_client2gctextmsg)
- 🔌 [CMsgGCCStrike15_v2_Client2GcAckXPShopTracks](#cmsggccstrike15_v2_client2gcackxpshoptracks)
- 🔌 [CMsgGCCStrike15_v2_ClientAccountBalance](#cmsggccstrike15_v2_clientaccountbalance)
- 🔌 [CMsgGCCStrike15_v2_ClientAuthKeyCode](#cmsggccstrike15_v2_clientauthkeycode)
- 🔌 [CMsgGCCStrike15_v2_ClientCommendPlayer](#cmsggccstrike15_v2_clientcommendplayer)
- 🔌 [CMsgGCCStrike15_v2_ClientGCRankUpdate](#cmsggccstrike15_v2_clientgcrankupdate)
- 🔌 [CMsgGCCStrike15_v2_ClientLogonFatalError](#cmsggccstrike15_v2_clientlogonfatalerror)
- 🔌 [CMsgGCCStrike15_v2_ClientNetworkConfig](#cmsggccstrike15_v2_clientnetworkconfig)
- 🔌 [CMsgGCCStrike15_v2_ClientPartyJoinRelay](#cmsggccstrike15_v2_clientpartyjoinrelay)
- 🔌 [CMsgGCCStrike15_v2_ClientPartyWarning](#cmsggccstrike15_v2_clientpartywarning)
- 🔌 [CMsgGCCStrike15_v2_ClientPartyWarning_Entry](#cmsggccstrike15_v2_clientpartywarning_entry)
- 🔌 [CMsgGCCStrike15_v2_ClientPerfReport](#cmsggccstrike15_v2_clientperfreport)
- 🔌 [CMsgGCCStrike15_v2_ClientPerfReport_Entry](#cmsggccstrike15_v2_clientperfreport_entry)
- 🔌 [CMsgGCCStrike15_v2_ClientPlayerDecalSign](#cmsggccstrike15_v2_clientplayerdecalsign)
- 🔌 [CMsgGCCStrike15_v2_ClientPollState](#cmsggccstrike15_v2_clientpollstate)
- 🔌 [CMsgGCCStrike15_v2_ClientReportPlayer](#cmsggccstrike15_v2_clientreportplayer)
- 🔌 [CMsgGCCStrike15_v2_ClientReportResponse](#cmsggccstrike15_v2_clientreportresponse)
- 🔌 [CMsgGCCStrike15_v2_ClientReportServer](#cmsggccstrike15_v2_clientreportserver)
- 🔌 [CMsgGCCStrike15_v2_ClientReportValidation](#cmsggccstrike15_v2_clientreportvalidation)
- 🔌 [CMsgGCCStrike15_v2_ClientRequestJoinFriendData](#cmsggccstrike15_v2_clientrequestjoinfrienddata)
- 🔌 [CMsgGCCStrike15_v2_ClientRequestJoinServerData](#cmsggccstrike15_v2_clientrequestjoinserverdata)
- 🔌 [CMsgGCCStrike15_v2_ClientRequestOffers](#cmsggccstrike15_v2_clientrequestoffers)
- 🔌 [CMsgGCCStrike15_v2_ClientRequestPlayersProfile](#cmsggccstrike15_v2_clientrequestplayersprofile)
- 🔌 [CMsgGCCStrike15_v2_ClientRequestSouvenir](#cmsggccstrike15_v2_clientrequestsouvenir)
- 🔌 [CMsgGCCStrike15_v2_ClientRequestWatchInfoFriends](#cmsggccstrike15_v2_clientrequestwatchinfofriends)
- 🔌 [CMsgGCCStrike15_v2_ClientSubmitSurveyVote](#cmsggccstrike15_v2_clientsubmitsurveyvote)
- 🔌 [CMsgGCCStrike15_v2_ClientToGCChat](#cmsggccstrike15_v2_clienttogcchat)
- 🔌 [CMsgGCCStrike15_v2_ClientToGCRequestElevate](#cmsggccstrike15_v2_clienttogcrequestelevate)
- 🔌 [CMsgGCCStrike15_v2_ClientToGCRequestTicket](#cmsggccstrike15_v2_clienttogcrequestticket)
- 🔌 [CMsgGCCStrike15_v2_ClientVarValueNotificationInfo](#cmsggccstrike15_v2_clientvarvaluenotificationinfo)
- 🔌 [CMsgGCCStrike15_v2_Fantasy](#cmsggccstrike15_v2_fantasy)
- 🔌 [CMsgGCCStrike15_v2_Fantasy_FantasySlot](#cmsggccstrike15_v2_fantasy_fantasyslot)
- 🔌 [CMsgGCCStrike15_v2_Fantasy_FantasyTeam](#cmsggccstrike15_v2_fantasy_fantasyteam)
- 🔌 [CMsgGCCStrike15_v2_GC2ClientInitSystem](#cmsggccstrike15_v2_gc2clientinitsystem)
- 🔌 [CMsgGCCStrike15_v2_GC2ClientInitSystem_Response](#cmsggccstrike15_v2_gc2clientinitsystem_response)
- 🔌 [CMsgGCCStrike15_v2_GC2ClientNotifyXPShop](#cmsggccstrike15_v2_gc2clientnotifyxpshop)
- 🔌 [CMsgGCCStrike15_v2_GC2ClientRefuseSecureMode](#cmsggccstrike15_v2_gc2clientrefusesecuremode)
- 🔌 [CMsgGCCStrike15_v2_GC2ClientRequestValidation](#cmsggccstrike15_v2_gc2clientrequestvalidation)
- 🔌 [CMsgGCCStrike15_v2_GC2ClientTextMsg](#cmsggccstrike15_v2_gc2clienttextmsg)
- 🔌 [CMsgGCCStrike15_v2_GC2ClientTournamentInfo](#cmsggccstrike15_v2_gc2clienttournamentinfo)
- 🔌 [CMsgGCCStrike15_v2_GC2ServerReservationUpdate](#cmsggccstrike15_v2_gc2serverreservationupdate)
- 🔌 [CMsgGCCStrike15_v2_GCToClientChat](#cmsggccstrike15_v2_gctoclientchat)
- 🔌 [CMsgGCCStrike15_v2_GetEventFavorites_Request](#cmsggccstrike15_v2_geteventfavorites_request)
- 🔌 [CMsgGCCStrike15_v2_GetEventFavorites_Response](#cmsggccstrike15_v2_geteventfavorites_response)
- 🔌 [CMsgGCCStrike15_v2_GiftsLeaderboardRequest](#cmsggccstrike15_v2_giftsleaderboardrequest)
- 🔌 [CMsgGCCStrike15_v2_GiftsLeaderboardResponse](#cmsggccstrike15_v2_giftsleaderboardresponse)
- 🔌 [CMsgGCCStrike15_v2_GiftsLeaderboardResponse_GiftLeaderboardEntry](#cmsggccstrike15_v2_giftsleaderboardresponse_giftleaderboardentry)
- 🔌 [CMsgGCCStrike15_v2_MatchEndRewardDropsNotification](#cmsggccstrike15_v2_matchendrewarddropsnotification)
- 🔌 [CMsgGCCStrike15_v2_MatchEndRunRewardDrops](#cmsggccstrike15_v2_matchendrunrewarddrops)
- 🔌 [CMsgGCCStrike15_v2_MatchList](#cmsggccstrike15_v2_matchlist)
- 🔌 [CMsgGCCStrike15_v2_MatchListRequestCurrentLiveGames](#cmsggccstrike15_v2_matchlistrequestcurrentlivegames)
- 🔌 [CMsgGCCStrike15_v2_MatchListRequestFullGameInfo](#cmsggccstrike15_v2_matchlistrequestfullgameinfo)
- 🔌 [CMsgGCCStrike15_v2_MatchListRequestLiveGameForUser](#cmsggccstrike15_v2_matchlistrequestlivegameforuser)
- 🔌 [CMsgGCCStrike15_v2_MatchListRequestRecentUserGames](#cmsggccstrike15_v2_matchlistrequestrecentusergames)
- 🔌 [CMsgGCCStrike15_v2_MatchListRequestTournamentGames](#cmsggccstrike15_v2_matchlistrequesttournamentgames)
- 🔌 [CMsgGCCStrike15_v2_MatchListTournamentOperatorMgmt](#cmsggccstrike15_v2_matchlisttournamentoperatormgmt)
- 🔌 [CMsgGCCStrike15_v2_MatchmakingClient2GCHello](#cmsggccstrike15_v2_matchmakingclient2gchello)
- 🔌 [CMsgGCCStrike15_v2_MatchmakingClient2ServerPing](#cmsggccstrike15_v2_matchmakingclient2serverping)
- 🔌 [CMsgGCCStrike15_v2_MatchmakingGC2ClientAbandon](#cmsggccstrike15_v2_matchmakinggc2clientabandon)
- 🔌 [CMsgGCCStrike15_v2_MatchmakingGC2ClientHello](#cmsggccstrike15_v2_matchmakinggc2clienthello)
- 🔌 [CMsgGCCStrike15_v2_MatchmakingGC2ClientReserve](#cmsggccstrike15_v2_matchmakinggc2clientreserve)
- 🔌 [CMsgGCCStrike15_v2_MatchmakingGC2ClientSearchStats](#cmsggccstrike15_v2_matchmakinggc2clientsearchstats)
- 🔌 [CMsgGCCStrike15_v2_MatchmakingGC2ClientUpdate](#cmsggccstrike15_v2_matchmakinggc2clientupdate)
- 🔌 [CMsgGCCStrike15_v2_MatchmakingGC2ClientUpdate_Note](#cmsggccstrike15_v2_matchmakinggc2clientupdate_note)
- 🔌 [CMsgGCCStrike15_v2_MatchmakingGC2ServerConfirm](#cmsggccstrike15_v2_matchmakinggc2serverconfirm)
- 🔌 [CMsgGCCStrike15_v2_MatchmakingGC2ServerReserve](#cmsggccstrike15_v2_matchmakinggc2serverreserve)
- 🔌 [CMsgGCCStrike15_v2_MatchmakingOperator2GCBlogUpdate](#cmsggccstrike15_v2_matchmakingoperator2gcblogupdate)
- 🔌 [CMsgGCCStrike15_v2_MatchmakingServerReservationResponse](#cmsggccstrike15_v2_matchmakingserverreservationresponse)
- 🔌 [CMsgGCCStrike15_v2_MatchmakingServerRoundStats](#cmsggccstrike15_v2_matchmakingserverroundstats)
- 🔌 [CMsgGCCStrike15_v2_MatchmakingServerRoundStats_DropInfo](#cmsggccstrike15_v2_matchmakingserverroundstats_dropinfo)
- 🔌 [CMsgGCCStrike15_v2_MatchmakingStart](#cmsggccstrike15_v2_matchmakingstart)
- 🔌 [CMsgGCCStrike15_v2_MatchmakingStop](#cmsggccstrike15_v2_matchmakingstop)
- 🔌 [CMsgGCCStrike15_v2_Party_Invite](#cmsggccstrike15_v2_party_invite)
- 🔌 [CMsgGCCStrike15_v2_Party_Register](#cmsggccstrike15_v2_party_register)
- 🔌 [CMsgGCCStrike15_v2_Party_Search](#cmsggccstrike15_v2_party_search)
- 🔌 [CMsgGCCStrike15_v2_Party_SearchResults](#cmsggccstrike15_v2_party_searchresults)
- 🔌 [CMsgGCCStrike15_v2_Party_SearchResults_Entry](#cmsggccstrike15_v2_party_searchresults_entry)
- 🔌 [CMsgGCCStrike15_v2_PlayerOverwatchCaseAssignment](#cmsggccstrike15_v2_playeroverwatchcaseassignment)
- 🔌 [CMsgGCCStrike15_v2_PlayerOverwatchCaseStatus](#cmsggccstrike15_v2_playeroverwatchcasestatus)
- 🔌 [CMsgGCCStrike15_v2_PlayerOverwatchCaseUpdate](#cmsggccstrike15_v2_playeroverwatchcaseupdate)
- 🔌 [CMsgGCCStrike15_v2_PlayersProfile](#cmsggccstrike15_v2_playersprofile)
- 🔌 [CMsgGCCStrike15_v2_Predictions](#cmsggccstrike15_v2_predictions)
- 🔌 [CMsgGCCStrike15_v2_Predictions_GroupMatchTeamPick](#cmsggccstrike15_v2_predictions_groupmatchteampick)
- 🔌 [CMsgGCCStrike15_v2_PremierSeasonSummary](#cmsggccstrike15_v2_premierseasonsummary)
- 🔌 [CMsgGCCStrike15_v2_PremierSeasonSummary_DataPerMap](#cmsggccstrike15_v2_premierseasonsummary_datapermap)
- 🔌 [CMsgGCCStrike15_v2_PremierSeasonSummary_DataPerWeek](#cmsggccstrike15_v2_premierseasonsummary_dataperweek)
- 🔌 [CMsgGCCStrike15_v2_Server2GCClientValidate](#cmsggccstrike15_v2_server2gcclientvalidate)
- 🔌 [CMsgGCCStrike15_v2_ServerNotificationForUserPenalty](#cmsggccstrike15_v2_servernotificationforuserpenalty)
- 🔌 [CMsgGCCStrike15_v2_ServerVarValueNotificationInfo](#cmsggccstrike15_v2_servervarvaluenotificationinfo)
- 🔌 [CMsgGCCStrike15_v2_SetEventFavorite](#cmsggccstrike15_v2_seteventfavorite)
- 🔌 [CMsgGCCStrike15_v2_SetPlayerLeaderboardSafeName](#cmsggccstrike15_v2_setplayerleaderboardsafename)
- 🔌 [CMsgGCCStrike15_v2_WatchInfoUsers](#cmsggccstrike15_v2_watchinfousers)
- 🔌 [CMsgGCClientDisplayNotification](#cmsggcclientdisplaynotification)
- 🔌 [CMsgGCClientVersionUpdated](#cmsggcclientversionupdated)
- 🔌 [CMsgGCCollectItem](#cmsggccollectitem)
- 🔌 [CMsgGCCstrike15_v2_ClientRedeemFreeReward](#cmsggccstrike15_v2_clientredeemfreereward)
- 🔌 [CMsgGCCstrike15_v2_ClientRedeemMissionReward](#cmsggccstrike15_v2_clientredeemmissionreward)
- 🔌 [CMsgGCCstrike15_v2_GC2ServerNotifyXPRewarded](#cmsggccstrike15_v2_gc2servernotifyxprewarded)
- 🔌 [CMsgGCDev_SchemaReservationRequest](#cmsggcdev_schemareservationrequest)
- 🔌 [CMsgGCError](#cmsggcerror)
- 🔌 [CMsgGCGiftedItems](#cmsggcgifteditems)
- 🔌 [CMsgGCHAccountPhoneNumberChange](#cmsggchaccountphonenumberchange)
- 🔌 [CMsgGCHInviteUserToLobby](#cmsggchinviteusertolobby)
- 🔌 [CMsgGCHRecurringSubscriptionStatusChange](#cmsggchrecurringsubscriptionstatuschange)
- 🔌 [CMsgGCHVacVerificationChange](#cmsggchvacverificationchange)
- 🔌 [CMsgGCIncrementKillCountResponse](#cmsggcincrementkillcountresponse)
- 🔌 [CMsgGCItemCustomizationNotification](#cmsggcitemcustomizationnotification)
- 🔌 [CMsgGCItemPreviewItemBoughtNotification](#cmsggcitempreviewitemboughtnotification)
- 🔌 [CMsgGCMultiplexMessage](#cmsggcmultiplexmessage)
- 🔌 [CMsgGCMultiplexMessage_Response](#cmsggcmultiplexmessage_response)
- 🔌 [CMsgGCNameItemNotification](#cmsggcnameitemnotification)
- 🔌 [CMsgGCReportAbuse](#cmsggcreportabuse)
- 🔌 [CMsgGCReportAbuseResponse](#cmsggcreportabuseresponse)
- 🔌 [CMsgGCRequestAnnouncements](#cmsggcrequestannouncements)
- 🔌 [CMsgGCRequestAnnouncementsResponse](#cmsggcrequestannouncementsresponse)
- 🔌 [CMsgGCRequestSessionIP](#cmsggcrequestsessionip)
- 🔌 [CMsgGCRequestSessionIPResponse](#cmsggcrequestsessionipresponse)
- 🔌 [CMsgGCServerVersionUpdated](#cmsggcserverversionupdated)
- 🔌 [CMsgGCShowItemsPickedUp](#cmsggcshowitemspickedup)
- 🔌 [CMsgGCStorePurchaseCancel](#cmsggcstorepurchasecancel)
- 🔌 [CMsgGCStorePurchaseCancelResponse](#cmsggcstorepurchasecancelresponse)
- 🔌 [CMsgGCStorePurchaseFinalize](#cmsggcstorepurchasefinalize)
- 🔌 [CMsgGCStorePurchaseFinalizeResponse](#cmsggcstorepurchasefinalizeresponse)
- 🔌 [CMsgGCStorePurchaseInit](#cmsggcstorepurchaseinit)
- 🔌 [CMsgGCStorePurchaseInitResponse](#cmsggcstorepurchaseinitresponse)
- 🔌 [CMsgGCToClientSteamDatagramTicket](#cmsggctoclientsteamdatagramticket)
- 🔌 [CMsgGCToGCBannedWordListBroadcast](#cmsggctogcbannedwordlistbroadcast)
- 🔌 [CMsgGCToGCBannedWordListUpdated](#cmsggctogcbannedwordlistupdated)
- 🔌 [CMsgGCToGCBroadcastConsoleCommand](#cmsggctogcbroadcastconsolecommand)
- 🔌 [CMsgGCToGCDirtyMultipleSDOCache](#cmsggctogcdirtymultiplesdocache)
- 🔌 [CMsgGCToGCDirtySDOCache](#cmsggctogcdirtysdocache)
- 🔌 [CMsgGCToGCIsTrustedServer](#cmsggctogcistrustedserver)
- 🔌 [CMsgGCToGCIsTrustedServerResponse](#cmsggctogcistrustedserverresponse)
- 🔌 [CMsgGCToGCRequestPassportItemGrant](#cmsggctogcrequestpassportitemgrant)
- 🔌 [CMsgGCToGCUpdateSQLKeyValue](#cmsggctogcupdatesqlkeyvalue)
- 🔌 [CMsgGCToGCWebAPIAccountChanged](#cmsggctogcwebapiaccountchanged)
- 🔌 [CMsgGCUpdateSessionIP](#cmsggcupdatesessionip)
- 🔌 [CMsgGCUserTrackTimePlayedConsecutively](#cmsggcusertracktimeplayedconsecutively)
- 🔌 [CMsgGC_GlobalGame_Play](#cmsggc_globalgame_play)
- 🔌 [CMsgGC_GlobalGame_Subscribe](#cmsggc_globalgame_subscribe)
- 🔌 [CMsgGC_GlobalGame_Unsubscribe](#cmsggc_globalgame_unsubscribe)
- 🔌 [CMsgGC_ServerQuestUpdateData](#cmsggc_serverquestupdatedata)
- 🔌 [CMsgGameServerInfo](#cmsggameserverinfo)
- 📋 [CMsgGameServerInfo_ServerType](#cmsggameserverinfo_servertype)
- 🔌 [CMsgIPCAddress](#cmsgipcaddress)
- 🔌 [CMsgIncrementKillCountAttribute](#cmsgincrementkillcountattribute)
- 🔌 [CMsgInvitationCreated](#cmsginvitationcreated)
- 🔌 [CMsgInviteToParty](#cmsginvitetoparty)
- 🔌 [CMsgItemAcknowledged](#cmsgitemacknowledged)
- 🔌 [CMsgItemAcknowledged__DEPRECATED](#cmsgitemacknowledged__deprecated)
- 🔌 [CMsgKickFromParty](#cmsgkickfromparty)
- 🔌 [CMsgLANServerAvailable](#cmsglanserveravailable)
- 🔌 [CMsgLeaveParty](#cmsgleaveparty)
- 🔌 [CMsgLegacySource1ClientWelcome](#cmsglegacysource1clientwelcome)
- 🔌 [CMsgLegacySource1ClientWelcome_Location](#cmsglegacysource1clientwelcome_location)
- 🔌 [CMsgModifyItemAttribute](#cmsgmodifyitemattribute)
- 🔌 [CMsgOpenCrate](#cmsgopencrate)
- 🔌 [CMsgPartyInviteResponse](#cmsgpartyinviteresponse)
- 🔌 [CMsgPlaceDecalEvent](#cmsgplacedecalevent)
- 🔌 [CMsgPlayerBulletHit](#cmsgplayerbullethit)
- 🔌 [CMsgPlayerInfo](#cmsgplayerinfo)
- 🔌 [CMsgProtoBufHeader](#cmsgprotobufheader)
- 🔌 [CMsgQAngle](#cmsgqangle)
- 🔌 [CMsgQuaternion](#cmsgquaternion)
- 🔌 [CMsgRGBA](#cmsgrgba)
- 🔌 [CMsgRecurringMissionSchema](#cmsgrecurringmissionschema)
- 🔌 [CMsgRecurringMissionSchema_MissionTemplateList](#cmsgrecurringmissionschema_missiontemplatelist)
- 🔌 [CMsgReplayUploadedToYouTube](#cmsgreplayuploadedtoyoutube)
- 🔌 [CMsgReplicateConVars](#cmsgreplicateconvars)
- 🔌 [CMsgRequestInventoryRefresh](#cmsgrequestinventoryrefresh)
- 🔌 [CMsgRequestRecurringMissionSchedule](#cmsgrequestrecurringmissionschedule)
- 🔌 [CMsgSDONoMemcached](#cmsgsdonomemcached)
- 🔌 [CMsgSOCacheHaveVersion](#cmsgsocachehaveversion)
- 🔌 [CMsgSOCacheSubscribed](#cmsgsocachesubscribed)
- 🔌 [CMsgSOCacheSubscribed_SubscribedType](#cmsgsocachesubscribed_subscribedtype)
- 🔌 [CMsgSOCacheSubscriptionCheck](#cmsgsocachesubscriptioncheck)
- 🔌 [CMsgSOCacheSubscriptionRefresh](#cmsgsocachesubscriptionrefresh)
- 🔌 [CMsgSOCacheUnsubscribed](#cmsgsocacheunsubscribed)
- 🔌 [CMsgSOCacheVersion](#cmsgsocacheversion)
- 🔌 [CMsgSOIDOwner](#cmsgsoidowner)
- 🔌 [CMsgSOMultipleObjects](#cmsgsomultipleobjects)
- 🔌 [CMsgSOMultipleObjects_SingleObject](#cmsgsomultipleobjects_singleobject)
- 🔌 [CMsgSOSingleObject](#cmsgsosingleobject)
- 🔌 [CMsgSerializedSOCache](#cmsgserializedsocache)
- 🔌 [CMsgSerializedSOCache_Cache](#cmsgserializedsocache_cache)
- 🔌 [CMsgSerializedSOCache_Cache_Version](#cmsgserializedsocache_cache_version)
- 🔌 [CMsgSerializedSOCache_TypeCache](#cmsgserializedsocache_typecache)
- 🔌 [CMsgServerAvailable](#cmsgserveravailable)
- 🔌 [CMsgServerHello](#cmsgserverhello)
- 🔌 [CMsgServerNetworkStats](#cmsgservernetworkstats)
- 🔌 [CMsgServerNetworkStats_Player](#cmsgservernetworkstats_player)
- 🔌 [CMsgServerNetworkStats_Port](#cmsgservernetworkstats_port)
- 🔌 [CMsgServerPeer](#cmsgserverpeer)
- 🔌 [CMsgServerUserCmd](#cmsgserverusercmd)
- 🔌 [CMsgSetItemPositions](#cmsgsetitempositions)
- 🔌 [CMsgSetItemPositions_ItemPosition](#cmsgsetitempositions_itemposition)
- 🔌 [CMsgSortItems](#cmsgsortitems)
- 🔌 [CMsgSosSetLibraryStackFields](#cmsgsossetlibrarystackfields)
- 🔌 [CMsgSosSetSoundEventParams](#cmsgsossetsoundeventparams)
- 🔌 [CMsgSosStartSoundEvent](#cmsgsosstartsoundevent)
- 🔌 [CMsgSosStopSoundEvent](#cmsgsosstopsoundevent)
- 🔌 [CMsgSosStopSoundEventHash](#cmsgsosstopsoundeventhash)
- 🔌 [CMsgSource1LegacyGameEvent](#cmsgsource1legacygameevent)
- 🔌 [CMsgSource1LegacyGameEventList](#cmsgsource1legacygameeventlist)
- 🔌 [CMsgSource1LegacyGameEventList_descriptor_t](#cmsgsource1legacygameeventlist_descriptor_t)
- 🔌 [CMsgSource1LegacyGameEventList_key_t](#cmsgsource1legacygameeventlist_key_t)
- 🔌 [CMsgSource1LegacyGameEvent_key_t](#cmsgsource1legacygameevent_key_t)
- 🔌 [CMsgSource1LegacyListenEvents](#cmsgsource1legacylistenevents)
- 🔌 [CMsgSource2NetworkFlowQuality](#cmsgsource2networkflowquality)
- 🔌 [CMsgSource2PerfIntervalSample](#cmsgsource2perfintervalsample)
- 🔌 [CMsgSource2PerfIntervalSample_Tag](#cmsgsource2perfintervalsample_tag)
- 🔌 [CMsgSource2SystemSpecs](#cmsgsource2systemspecs)
- 🔌 [CMsgSource2VProfLiteReport](#cmsgsource2vproflitereport)
- 🔌 [CMsgSource2VProfLiteReportItem](#cmsgsource2vproflitereportitem)
- 🔌 [CMsgStoreGetUserData](#cmsgstoregetuserdata)
- 🔌 [CMsgStoreGetUserDataResponse](#cmsgstoregetuserdataresponse)
- 🔌 [CMsgSystemBroadcast](#cmsgsystembroadcast)
- 🔌 [CMsgTEArmorRicochet](#cmsgtearmorricochet)
- 🔌 [CMsgTEBaseBeam](#cmsgtebasebeam)
- 🔌 [CMsgTEBeamEntPoint](#cmsgtebeamentpoint)
- 🔌 [CMsgTEBeamEnts](#cmsgtebeaments)
- 🔌 [CMsgTEBeamPoints](#cmsgtebeampoints)
- 🔌 [CMsgTEBeamRing](#cmsgtebeamring)
- 🔌 [CMsgTEBloodStream](#cmsgtebloodstream)
- 🔌 [CMsgTEBubbleTrail](#cmsgtebubbletrail)
- 🔌 [CMsgTEBubbles](#cmsgtebubbles)
- 🔌 [CMsgTEDecal](#cmsgtedecal)
- 🔌 [CMsgTEDust](#cmsgtedust)
- 🔌 [CMsgTEEffectDispatch](#cmsgteeffectdispatch)
- 🔌 [CMsgTEEnergySplash](#cmsgteenergysplash)
- 🔌 [CMsgTEExplosion](#cmsgteexplosion)
- 🔌 [CMsgTEFireBullets](#cmsgtefirebullets)
- 🔌 [CMsgTEFireBullets_Extra](#cmsgtefirebullets_extra)
- 🔌 [CMsgTEFizz](#cmsgtefizz)
- 🔌 [CMsgTEGlowSprite](#cmsgteglowsprite)
- 🔌 [CMsgTEImpact](#cmsgteimpact)
- 🔌 [CMsgTELargeFunnel](#cmsgtelargefunnel)
- 🔌 [CMsgTEMuzzleFlash](#cmsgtemuzzleflash)
- 🔌 [CMsgTEPhysicsProp](#cmsgtephysicsprop)
- 🔌 [CMsgTEPlayerAnimEvent](#cmsgteplayeranimevent)
- 🔌 [CMsgTERadioIcon](#cmsgteradioicon)
- 🔌 [CMsgTEShatterSurface](#cmsgteshattersurface)
- 🔌 [CMsgTESmoke](#cmsgtesmoke)
- 🔌 [CMsgTESparks](#cmsgtesparks)
- 🔌 [CMsgTEWorldDecal](#cmsgteworlddecal)
- 🔌 [CMsgTransform](#cmsgtransform)
- 🔌 [CMsgUpdateItemSchema](#cmsgupdateitemschema)
- 🔌 [CMsgUseItem](#cmsguseitem)
- 🔌 [CMsgVDebugGameSessionIDEvent](#cmsgvdebuggamesessionidevent)
- 🔌 [CMsgVector](#cmsgvector)
- 🔌 [CMsgVector2D](#cmsgvector2d)
- 🔌 [CMsgVoiceAudio](#cmsgvoiceaudio)
- 🔌 [CMsg_CVars](#cmsg_cvars)
- 🔌 [CMsg_CVars_CVar](#cmsg_cvars_cvar)
- 🔌 [CNETMsg_DebugOverlay](#cnetmsg_debugoverlay)
- 🔌 [CNETMsg_NOP](#cnetmsg_nop)
- 🔌 [CNETMsg_SetConVar](#cnetmsg_setconvar)
- 🔌 [CNETMsg_SignonState](#cnetmsg_signonstate)
- 🔌 [CNETMsg_SpawnGroup_Load](#cnetmsg_spawngroup_load)
- 🔌 [CNETMsg_SpawnGroup_LoadCompleted](#cnetmsg_spawngroup_loadcompleted)
- 🔌 [CNETMsg_SpawnGroup_ManifestUpdate](#cnetmsg_spawngroup_manifestupdate)
- 🔌 [CNETMsg_SpawnGroup_SetCreationTick](#cnetmsg_spawngroup_setcreationtick)
- 🔌 [CNETMsg_SpawnGroup_Unload](#cnetmsg_spawngroup_unload)
- 🔌 [CNETMsg_SplitScreenUser](#cnetmsg_splitscreenuser)
- 🔌 [CNETMsg_StringCmd](#cnetmsg_stringcmd)
- 🔌 [CNETMsg_Tick](#cnetmsg_tick)
- 🔌 [CP2P_Ping](#cp2p_ping)
- 🔌 [CP2P_TextMessage](#cp2p_textmessage)
- 🔌 [CP2P_VRAvatarPosition](#cp2p_vravatarposition)
- 🔌 [CP2P_VRAvatarPosition_COrientation](#cp2p_vravatarposition_corientation)
- 🔌 [CP2P_Voice](#cp2p_voice)
- 📋 [CP2P_Voice_Handler_Flags](#cp2p_voice_handler_flags)
- 🔌 [CP2P_WatchSynchronization](#cp2p_watchsynchronization)
- 🔌 [CPreMatchInfoData](#cprematchinfodata)
- 🔌 [CPreMatchInfoData_TeamStats](#cprematchinfodata_teamstats)
- 🔌 [CPredictionEvent_Diagnostic](#cpredictionevent_diagnostic)
- 🔌 [CPredictionEvent_StringCommand](#cpredictionevent_stringcommand)
- 🔌 [CPredictionEvent_Teleport](#cpredictionevent_teleport)
- 🔌 [CProductInfo_SetRichPresenceLocalization_Request](#cproductinfo_setrichpresencelocalization_request)
- 🔌 [CProductInfo_SetRichPresenceLocalization_Request_LanguageSection](#cproductinfo_setrichpresencelocalization_request_languagesection)
- 🔌 [CProductInfo_SetRichPresenceLocalization_Request_Token](#cproductinfo_setrichpresencelocalization_request_token)
- 🔌 [CProductInfo_SetRichPresenceLocalization_Response](#cproductinfo_setrichpresencelocalization_response)
- 🔌 [CQuest_PublisherAddCommunityItemsToPlayer_Request](#cquest_publisheraddcommunityitemstoplayer_request)
- 🔌 [CQuest_PublisherAddCommunityItemsToPlayer_Request_Attribute](#cquest_publisheraddcommunityitemstoplayer_request_attribute)
- 🔌 [CQuest_PublisherAddCommunityItemsToPlayer_Response](#cquest_publisheraddcommunityitemstoplayer_response)
- 🔌 [CSGOInputHistoryEntryPB](#csgoinputhistoryentrypb)
- 🔌 [CSGOInterpolationInfoPB](#csgointerpolationinfopb)
- 🔌 [CSGOInterpolationInfoPB_CL](#csgointerpolationinfopb_cl)
- 🔌 [CSGOUserCmdPB](#csgousercmdpb)
- 🔌 [CSOAccountItemPersonalStore](#csoaccountitempersonalstore)
- 🔌 [CSOAccountKeychainRemoveToolCharges](#csoaccountkeychainremovetoolcharges)
- 🔌 [CSOAccountRecurringMission](#csoaccountrecurringmission)
- 🔌 [CSOAccountRecurringSubscription](#csoaccountrecurringsubscription)
- 🔌 [CSOAccountSeasonalOperation](#csoaccountseasonaloperation)
- 🔌 [CSOAccountXpShop](#csoaccountxpshop)
- 🔌 [CSOAccountXpShopBids](#csoaccountxpshopbids)
- 🔌 [CSOEconClaimCode](#csoeconclaimcode)
- 🔌 [CSOEconCoupon](#csoeconcoupon)
- 🔌 [CSOEconEquipSlot](#csoeconequipslot)
- 🔌 [CSOEconGameAccountClient](#csoecongameaccountclient)
- 🔌 [CSOEconItem](#csoeconitem)
- 🔌 [CSOEconItemAttribute](#csoeconitemattribute)
- 🔌 [CSOEconItemDropRateBonus](#csoeconitemdropratebonus)
- 🔌 [CSOEconItemEquipped](#csoeconitemequipped)
- 🔌 [CSOEconItemEventTicket](#csoeconitemeventticket)
- 🔌 [CSOEconItemLeagueViewPass](#csoeconitemleagueviewpass)
- 🔌 [CSOEconRentalHistory](#csoeconrentalhistory)
- 🔌 [CSOGameAccountSteamChina](#csogameaccountsteamchina)
- 🔌 [CSOItemCriteria](#csoitemcriteria)
- 🔌 [CSOItemCriteriaCondition](#csoitemcriteriacondition)
- 🔌 [CSOItemRecipe](#csoitemrecipe)
- 🔌 [CSOLobbyInvite](#csolobbyinvite)
- 🔌 [CSOPartyInvite](#csopartyinvite)
- 🔌 [CSOPersonaDataPublic](#csopersonadatapublic)
- 🔌 [CSOQuestProgress](#csoquestprogress)
- 🔌 [CSOVolatileItemClaimedRewards](#csovolatileitemclaimedrewards)
- 🔌 [CSOVolatileItemOffer](#csovolatileitemoffer)
- 🔌 [CSVCMsgList_GameEvents](#csvcmsglist_gameevents)
- 🔌 [CSVCMsgList_GameEvents_event_t](#csvcmsglist_gameevents_event_t)
- 🔌 [CSVCMsg_BSPDecal](#csvcmsg_bspdecal)
- 🔌 [CSVCMsg_Broadcast_Command](#csvcmsg_broadcast_command)
- 🔌 [CSVCMsg_ClassInfo](#csvcmsg_classinfo)
- 🔌 [CSVCMsg_ClassInfo_class_t](#csvcmsg_classinfo_class_t)
- 🔌 [CSVCMsg_ClearAllStringTables](#csvcmsg_clearallstringtables)
- 🔌 [CSVCMsg_CmdKeyValues](#csvcmsg_cmdkeyvalues)
- 🔌 [CSVCMsg_CreateStringTable](#csvcmsg_createstringtable)
- 🔌 [CSVCMsg_CrosshairAngle](#csvcmsg_crosshairangle)
- 🔌 [CSVCMsg_FixAngle](#csvcmsg_fixangle)
- 🔌 [CSVCMsg_FlattenedSerializer](#csvcmsg_flattenedserializer)
- 🔌 [CSVCMsg_FullFrameSplit](#csvcmsg_fullframesplit)
- 🔌 [CSVCMsg_GameEvent](#csvcmsg_gameevent)
- 🔌 [CSVCMsg_GameEventList](#csvcmsg_gameeventlist)
- 🔌 [CSVCMsg_GameEventList_descriptor_t](#csvcmsg_gameeventlist_descriptor_t)
- 🔌 [CSVCMsg_GameEventList_key_t](#csvcmsg_gameeventlist_key_t)
- 🔌 [CSVCMsg_GameEvent_key_t](#csvcmsg_gameevent_key_t)
- 🔌 [CSVCMsg_GameSessionConfiguration](#csvcmsg_gamesessionconfiguration)
- 🔌 [CSVCMsg_GetCvarValue](#csvcmsg_getcvarvalue)
- 🔌 [CSVCMsg_HLTVStatus](#csvcmsg_hltvstatus)
- 🔌 [CSVCMsg_HltvFixupOperatorStatus](#csvcmsg_hltvfixupoperatorstatus)
- 🔌 [CSVCMsg_HltvReplay](#csvcmsg_hltvreplay)
- 🔌 [CSVCMsg_Menu](#csvcmsg_menu)
- 🔌 [CSVCMsg_NextMsgPredicted](#csvcmsg_nextmsgpredicted)
- 🔌 [CSVCMsg_PacketEntities](#csvcmsg_packetentities)
- 🔌 [CSVCMsg_PacketEntities_alternate_baseline_t](#csvcmsg_packetentities_alternate_baseline_t)
- 🔌 [CSVCMsg_PacketEntities_non_transmitted_entities_t](#csvcmsg_packetentities_non_transmitted_entities_t)
- 🔌 [CSVCMsg_PacketEntities_outofpvs_entity_updates_t](#csvcmsg_packetentities_outofpvs_entity_updates_t)
- 🔌 [CSVCMsg_PacketReliable](#csvcmsg_packetreliable)
- 🔌 [CSVCMsg_PeerList](#csvcmsg_peerlist)
- 🔌 [CSVCMsg_Prefetch](#csvcmsg_prefetch)
- 🔌 [CSVCMsg_Print](#csvcmsg_print)
- 🔌 [CSVCMsg_RconServerDetails](#csvcmsg_rconserverdetails)
- 🔌 [CSVCMsg_SendTable](#csvcmsg_sendtable)
- 🔌 [CSVCMsg_SendTable_sendprop_t](#csvcmsg_sendtable_sendprop_t)
- 🔌 [CSVCMsg_ServerInfo](#csvcmsg_serverinfo)
- 🔌 [CSVCMsg_ServerSteamID](#csvcmsg_serversteamid)
- 🔌 [CSVCMsg_SetPause](#csvcmsg_setpause)
- 🔌 [CSVCMsg_SetView](#csvcmsg_setview)
- 🔌 [CSVCMsg_Sounds](#csvcmsg_sounds)
- 🔌 [CSVCMsg_Sounds_sounddata_t](#csvcmsg_sounds_sounddata_t)
- 🔌 [CSVCMsg_SplitScreen](#csvcmsg_splitscreen)
- 🔌 [CSVCMsg_StopSound](#csvcmsg_stopsound)
- 🔌 [CSVCMsg_TempEntities](#csvcmsg_tempentities)
- 🔌 [CSVCMsg_UpdateStringTable](#csvcmsg_updatestringtable)
- 🔌 [CSVCMsg_UserCommands](#csvcmsg_usercommands)
- 🔌 [CSVCMsg_UserMessage](#csvcmsg_usermessage)
- 🔌 [CSVCMsg_VoiceData](#csvcmsg_voicedata)
- 🔌 [CSVCMsg_VoiceInit](#csvcmsg_voiceinit)
- 🔌 [CSource2Metrics_MatchPerfSummary_Notification](#csource2metrics_matchperfsummary_notification)
- 🔌 [CSource2Metrics_MatchPerfSummary_Notification_Client](#csource2metrics_matchperfsummary_notification_client)
- 🔌 [CSteam_Voice_Encoding](#csteam_voice_encoding)
- 🔌 [CSubtickMoveStep](#csubtickmovestep)
- 🔌 [CUIFontFilePB](#cuifontfilepb)
- 🔌 [CUIFontFilePackagePB](#cuifontfilepackagepb)
- 🔌 [CUIFontFilePackagePB_CUIEncryptedFontFilePB](#cuifontfilepackagepb_cuiencryptedfontfilepb)
- 🔌 [CUserCmdBasePB](#cusercmdbasepb)
- 🔌 [CUserMessageAchievementEvent](#cusermessageachievementevent)
- 🔌 [CUserMessageAmmoDenied](#cusermessageammodenied)
- 🔌 [CUserMessageAnimStateGraphState](#cusermessageanimstategraphstate)
- 🔌 [CUserMessageAudioParameter](#cusermessageaudioparameter)
- 🔌 [CUserMessageCameraTransition](#cusermessagecameratransition)
- 🔌 [CUserMessageCameraTransition_Transition_DataDriven](#cusermessagecameratransition_transition_datadriven)
- 🔌 [CUserMessageCloseCaption](#cusermessageclosecaption)
- 🔌 [CUserMessageCloseCaptionDirect](#cusermessageclosecaptiondirect)
- 🔌 [CUserMessageCloseCaptionPlaceholder](#cusermessageclosecaptionplaceholder)
- 🔌 [CUserMessageColoredText](#cusermessagecoloredtext)
- 🔌 [CUserMessageCreditsMsg](#cusermessagecreditsmsg)
- 🔌 [CUserMessageCurrentTimescale](#cusermessagecurrenttimescale)
- 🔌 [CUserMessageDesiredTimescale](#cusermessagedesiredtimescale)
- 🔌 [CUserMessageFade](#cusermessagefade)
- 🔌 [CUserMessageGameTitle](#cusermessagegametitle)
- 🔌 [CUserMessageHapticsManagerEffect](#cusermessagehapticsmanagereffect)
- 🔌 [CUserMessageHapticsManagerPulse](#cusermessagehapticsmanagerpulse)
- 🔌 [CUserMessageHudMsg](#cusermessagehudmsg)
- 🔌 [CUserMessageHudText](#cusermessagehudtext)
- 🔌 [CUserMessageItemPickup](#cusermessageitempickup)
- 🔌 [CUserMessageLagCompensationError](#cusermessagelagcompensationerror)
- 🔌 [CUserMessageRequestDiagnostic](#cusermessagerequestdiagnostic)
- 🔌 [CUserMessageRequestDiagnostic_Diagnostic](#cusermessagerequestdiagnostic_diagnostic)
- 🔌 [CUserMessageRequestDllStatus](#cusermessagerequestdllstatus)
- 🔌 [CUserMessageRequestInventory](#cusermessagerequestinventory)
- 🔌 [CUserMessageRequestState](#cusermessagerequeststate)
- 🔌 [CUserMessageRequestUtilAction](#cusermessagerequestutilaction)
- 🔌 [CUserMessageResetHUD](#cusermessageresethud)
- 🔌 [CUserMessageRumble](#cusermessagerumble)
- 🔌 [CUserMessageSayText](#cusermessagesaytext)
- 🔌 [CUserMessageSayText2](#cusermessagesaytext2)
- 🔌 [CUserMessageSayTextChannel](#cusermessagesaytextchannel)
- 🔌 [CUserMessageScreenTilt](#cusermessagescreentilt)
- 🔌 [CUserMessageSendAudio](#cusermessagesendaudio)
- 🔌 [CUserMessageServerFrameTime](#cusermessageserverframetime)
- 🔌 [CUserMessageShake](#cusermessageshake)
- 🔌 [CUserMessageShakeDir](#cusermessageshakedir)
- 🔌 [CUserMessageShowMenu](#cusermessageshowmenu)
- 🔌 [CUserMessageTextMsg](#cusermessagetextmsg)
- 🔌 [CUserMessageUpdateCssClasses](#cusermessageupdatecssclasses)
- 🔌 [CUserMessageVoiceMask](#cusermessagevoicemask)
- 🔌 [CUserMessageWaterShake](#cusermessagewatershake)
- 🔌 [CUserMessage_Diagnostic_Response](#cusermessage_diagnostic_response)
- 🔌 [CUserMessage_Diagnostic_Response_Diagnostic](#cusermessage_diagnostic_response_diagnostic)
- 🔌 [CUserMessage_DllStatus](#cusermessage_dllstatus)
- 🔌 [CUserMessage_DllStatus_CModule](#cusermessage_dllstatus_cmodule)
- 🔌 [CUserMessage_DllStatus_CVDiagnostic](#cusermessage_dllstatus_cvdiagnostic)
- 🔌 [CUserMessage_ExtraUserData](#cusermessage_extrauserdata)
- 🔌 [CUserMessage_Inventory_Response](#cusermessage_inventory_response)
- 🔌 [CUserMessage_Inventory_Response_InventoryDetail](#cusermessage_inventory_response_inventorydetail)
- 🔌 [CUserMessage_NotifyResponseFound](#cusermessage_notifyresponsefound)
- 🔌 [CUserMessage_NotifyResponseFound_Criteria](#cusermessage_notifyresponsefound_criteria)
- 🔌 [CUserMessage_PlayResponseConditional](#cusermessage_playresponseconditional)
- 🔌 [CUserMessage_UtilMsg_Response](#cusermessage_utilmsg_response)
- 🔌 [CUserMessage_UtilMsg_Response_ItemDetail](#cusermessage_utilmsg_response_itemdetail)
- 🔌 [CUserMsg_CustomGameEvent](#cusermsg_customgameevent)
- 🔌 [CUserMsg_HudError](#cusermsg_huderror)
- 🔌 [CUserMsg_ParticleManager](#cusermsg_particlemanager)
- 🔌 [CUserMsg_ParticleManager_AddFan](#cusermsg_particlemanager_addfan)
- 🔌 [CUserMsg_ParticleManager_AddModellistOverrideElement](#cusermsg_particlemanager_addmodellistoverrideelement)
- 🔌 [CUserMsg_ParticleManager_ChangeControlPointAttachment](#cusermsg_particlemanager_changecontrolpointattachment)
- 🔌 [CUserMsg_ParticleManager_ClearModellistOverride](#cusermsg_particlemanager_clearmodellistoverride)
- 🔌 [CUserMsg_ParticleManager_CreateParticle](#cusermsg_particlemanager_createparticle)
- 🔌 [CUserMsg_ParticleManager_CreatePhysicsSim](#cusermsg_particlemanager_createphysicssim)
- 🔌 [CUserMsg_ParticleManager_DestroyParticle](#cusermsg_particlemanager_destroyparticle)
- 🔌 [CUserMsg_ParticleManager_DestroyParticleInvolving](#cusermsg_particlemanager_destroyparticleinvolving)
- 🔌 [CUserMsg_ParticleManager_DestroyParticleNamed](#cusermsg_particlemanager_destroyparticlenamed)
- 🔌 [CUserMsg_ParticleManager_DestroyPhysicsSim](#cusermsg_particlemanager_destroyphysicssim)
- 🔌 [CUserMsg_ParticleManager_FreezeParticleInvolving](#cusermsg_particlemanager_freezeparticleinvolving)
- 🔌 [CUserMsg_ParticleManager_ParticleCanFreeze](#cusermsg_particlemanager_particlecanfreeze)
- 🔌 [CUserMsg_ParticleManager_ParticleFreezeTransitionOverride](#cusermsg_particlemanager_particlefreezetransitionoverride)
- 🔌 [CUserMsg_ParticleManager_ParticleSkipToTime](#cusermsg_particlemanager_particleskiptotime)
- 🔌 [CUserMsg_ParticleManager_ReleaseParticleIndex](#cusermsg_particlemanager_releaseparticleindex)
- 🔌 [CUserMsg_ParticleManager_RemoveFan](#cusermsg_particlemanager_removefan)
- 🔌 [CUserMsg_ParticleManager_SetControlPointModel](#cusermsg_particlemanager_setcontrolpointmodel)
- 🔌 [CUserMsg_ParticleManager_SetControlPointSnapshot](#cusermsg_particlemanager_setcontrolpointsnapshot)
- 🔌 [CUserMsg_ParticleManager_SetMaterialOverride](#cusermsg_particlemanager_setmaterialoverride)
- 🔌 [CUserMsg_ParticleManager_SetParticleClusterGrowth](#cusermsg_particlemanager_setparticleclustergrowth)
- 🔌 [CUserMsg_ParticleManager_SetParticleFoWProperties](#cusermsg_particlemanager_setparticlefowproperties)
- 🔌 [CUserMsg_ParticleManager_SetParticleNamedValueContext](#cusermsg_particlemanager_setparticlenamedvaluecontext)
- 🔌 [CUserMsg_ParticleManager_SetParticleNamedValueContext_EHandleContext](#cusermsg_particlemanager_setparticlenamedvaluecontext_ehandlecontext)
- 🔌 [CUserMsg_ParticleManager_SetParticleNamedValueContext_FloatContextValue](#cusermsg_particlemanager_setparticlenamedvaluecontext_floatcontextvalue)
- 🔌 [CUserMsg_ParticleManager_SetParticleNamedValueContext_TransformContextValue](#cusermsg_particlemanager_setparticlenamedvaluecontext_transformcontextvalue)
- 🔌 [CUserMsg_ParticleManager_SetParticleNamedValueContext_VectorContextValue](#cusermsg_particlemanager_setparticlenamedvaluecontext_vectorcontextvalue)
- 🔌 [CUserMsg_ParticleManager_SetParticleShouldCheckFoW](#cusermsg_particlemanager_setparticleshouldcheckfow)
- 🔌 [CUserMsg_ParticleManager_SetParticleText](#cusermsg_particlemanager_setparticletext)
- 🔌 [CUserMsg_ParticleManager_SetSceneObjectGenericFlag](#cusermsg_particlemanager_setsceneobjectgenericflag)
- 🔌 [CUserMsg_ParticleManager_SetSceneObjectTintAndDesat](#cusermsg_particlemanager_setsceneobjecttintanddesat)
- 🔌 [CUserMsg_ParticleManager_SetTextureAttribute](#cusermsg_particlemanager_settextureattribute)
- 🔌 [CUserMsg_ParticleManager_SetVData](#cusermsg_particlemanager_setvdata)
- 🔌 [CUserMsg_ParticleManager_UpdateEntityPosition](#cusermsg_particlemanager_updateentityposition)
- 🔌 [CUserMsg_ParticleManager_UpdateFan](#cusermsg_particlemanager_updatefan)
- 🔌 [CUserMsg_ParticleManager_UpdateParticleEnt](#cusermsg_particlemanager_updateparticleent)
- 🔌 [CUserMsg_ParticleManager_UpdateParticleFallback](#cusermsg_particlemanager_updateparticlefallback)
- 🔌 [CUserMsg_ParticleManager_UpdateParticleFwd_OBSOLETE](#cusermsg_particlemanager_updateparticlefwd_obsolete)
- 🔌 [CUserMsg_ParticleManager_UpdateParticleOffset](#cusermsg_particlemanager_updateparticleoffset)
- 🔌 [CUserMsg_ParticleManager_UpdateParticleOrient_OBSOLETE](#cusermsg_particlemanager_updateparticleorient_obsolete)
- 🔌 [CUserMsg_ParticleManager_UpdateParticleSetFrozen](#cusermsg_particlemanager_updateparticlesetfrozen)
- 🔌 [CUserMsg_ParticleManager_UpdateParticleShouldDraw](#cusermsg_particlemanager_updateparticleshoulddraw)
- 🔌 [CUserMsg_ParticleManager_UpdateParticleTransform](#cusermsg_particlemanager_updateparticletransform)
- 🔌 [CUserMsg_ParticleManager_UpdateParticle_OBSOLETE](#cusermsg_particlemanager_updateparticle_obsolete)
- 🔌 [CVDiagnostic](#cvdiagnostic)
- 🔌 [CWorkshop_AddSpecialPayment_Request](#cworkshop_addspecialpayment_request)
- 🔌 [CWorkshop_AddSpecialPayment_Response](#cworkshop_addspecialpayment_response)
- 🔌 [CWorkshop_GetContributors_Request](#cworkshop_getcontributors_request)
- 🔌 [CWorkshop_GetContributors_Response](#cworkshop_getcontributors_response)
- 🔌 [CWorkshop_PopulateItemDescriptions_Request](#cworkshop_populateitemdescriptions_request)
- 🔌 [CWorkshop_PopulateItemDescriptions_Request_ItemDescriptionsLanguageBlock](#cworkshop_populateitemdescriptions_request_itemdescriptionslanguageblock)
- 🔌 [CWorkshop_PopulateItemDescriptions_Request_SingleItemDescription](#cworkshop_populateitemdescriptions_request_singleitemdescription)
- 🔌 [CWorkshop_SetItemPaymentRules_Request](#cworkshop_setitempaymentrules_request)
- 🔌 [CWorkshop_SetItemPaymentRules_Request_PartnerItemPaymentRule](#cworkshop_setitempaymentrules_request_partneritempaymentrule)
- 🔌 [CWorkshop_SetItemPaymentRules_Request_WorkshopDirectPaymentRule](#cworkshop_setitempaymentrules_request_workshopdirectpaymentrule)
- 🔌 [CWorkshop_SetItemPaymentRules_Request_WorkshopItemPaymentRule](#cworkshop_setitempaymentrules_request_workshopitempaymentrule)
- 🔌 [CWorkshop_SetItemPaymentRules_Response](#cworkshop_setitempaymentrules_response)
- 📋 [DIALOG_TYPE](#dialog_type)
- 🔌 [DataCenterPing](#datacenterping)
- 🔌 [DeepPlayerMatchEvent](#deepplayermatchevent)
- 🔌 [DeepPlayerStatsEntry](#deepplayerstatsentry)
- 🔌 [DetailedSearchStatistic](#detailedsearchstatistic)
- 📋 [EBaseClientMessages](#ebaseclientmessages)
- 📋 [EBaseEntityMessages](#ebaseentitymessages)
- 📋 [EBaseGameEvents](#ebasegameevents)
- 📋 [EBasePredictionEvents](#ebasepredictionevents)
- 📋 [EBaseUserMessages](#ebaseusermessages)
- 📋 [ECSPredictionEvents](#ecspredictionevents)
- 📋 [ECSUsrMsg_DisconnectToLobby_Action](#ecsusrmsg_disconnecttolobby_action)
- 📋 [EClientPersonaStateFlag](#eclientpersonastateflag)
- 📋 [EClientReportingVersion](#eclientreportingversion)
- 📋 [EClientUIEvent](#eclientuievent)
- 📋 [ECodecUsagePlatform](#ecodecusageplatform)
- 📋 [ECodecUsageReason](#ecodecusagereason)
- 📋 [ECommunityItemAttribute](#ecommunityitemattribute)
- 📋 [ECommunityItemClass](#ecommunityitemclass)
- 📋 [ECsgoGCMsg](#ecsgogcmsg)
- 📋 [ECsgoGameEvents](#ecsgogameevents)
- 📋 [ECsgoSteamUserStat](#ecsgosteamuserstat)
- 📋 [ECstrike15UserMessages](#ecstrike15usermessages)
- 📋 [EDemoCommands](#edemocommands)
- 📋 [EGCBaseClientMsg](#egcbaseclientmsg)
- 📋 [EGCBaseMsg](#egcbasemsg)
- 📋 [EGCBaseProtoObjectTypes](#egcbaseprotoobjecttypes)
- 📋 [EGCItemCustomizationNotification](#egcitemcustomizationnotification)
- 📋 [EGCItemMsg](#egcitemmsg)
- 📋 [EGCMsgResponse](#egcmsgresponse)
- 📋 [EGCSystemMsg](#egcsystemmsg)
- 📋 [EGCToGCMsg](#egctogcmsg)
- 📋 [EHapticPulseType](#ehapticpulsetype)
- 📋 [EHitGroup](#ehitgroup)
- 📋 [EInitSystemResult](#einitsystemresult)
- 📋 [EMsg](#emsg)
- 📋 [EMsgClanAccountFlags](#emsgclanaccountflags)
- 📋 [ENetworkDisconnectionReason](#enetworkdisconnectionreason)
- 📋 [EProtoDebugVisiblity](#eprotodebugvisiblity)
- 📋 [EQueryCvarValueStatus](#equerycvarvaluestatus)
- 📋 [ESOMsg](#esomsg)
- 📋 [ESplitScreenMessageType](#esplitscreenmessagetype)
- 📋 [ESteamReviewScore](#esteamreviewscore)
- 📋 [ETEProtobufIds](#eteprotobufids)
- 📋 [ETeam](#eteam)
- 📋 [EUnlockStyle](#eunlockstyle)
- 📋 [EWeaponType](#eweapontype)
- 📋 [GCClientLauncherType](#gcclientlaunchertype)
- 📋 [GCConnectionStatus](#gcconnectionstatus)
- 📋 [GCProtoBufMsgSrc](#gcprotobufmsgsrc)
- 📋 [GC_BannedWordType](#gc_bannedwordtype)
- 🔌 [GameServerPing](#gameserverping)
- 🔌 [GlobalStatistics](#globalstatistics)
- 🔌 [IpAddressMask](#ipaddressmask)
- 🔌 [MLDemoHeader](#mldemoheader)
- 🔌 [MLDict](#mldict)
- 🔌 [MLEvent](#mlevent)
- 🔌 [MLGameState](#mlgamestate)
- 🔌 [MLMatchState](#mlmatchstate)
- 🔌 [MLPlayerState](#mlplayerstate)
- 🔌 [MLRoundState](#mlroundstate)
- 🔌 [MLTick](#mltick)
- 🔌 [MLWeaponState](#mlweaponstate)
- 🔌 [MatchEndItemUpdates](#matchenditemupdates)
- 📋 [NET_Messages](#net_messages)
- 🔌 [NetMessageConnectionClosed](#netmessageconnectionclosed)
- 🔌 [NetMessageConnectionCrashed](#netmessageconnectioncrashed)
- 🔌 [NetMessagePacketEnd](#netmessagepacketend)
- 🔌 [NetMessagePacketStart](#netmessagepacketstart)
- 🔌 [NetMessageSplitscreenUserChanged](#netmessagesplitscreenuserchanged)
- 🔌 [OperationalStatisticDescription](#operationalstatisticdescription)
- 🔌 [OperationalStatisticElement](#operationalstatisticelement)
- 🔌 [OperationalStatisticsPacket](#operationalstatisticspacket)
- 🔌 [OperationalVarValue](#operationalvarvalue)
- 📋 [P2P_Messages](#p2p_messages)
- 📋 [PARTICLE_MESSAGE](#particle_message)
- 🔌 [PlayerCommendationInfo](#playercommendationinfo)
- 🔌 [PlayerDecalDigitalSignature](#playerdecaldigitalsignature)
- 🔌 [PlayerMedalsInfo](#playermedalsinfo)
- 🔌 [PlayerQuestData](#playerquestdata)
- 🔌 [PlayerQuestData_QuestItemData](#playerquestdata_questitemdata)
- 🔌 [PlayerRankingInfo](#playerrankinginfo)
- 🔌 [PlayerRankingInfo_PerMapRank](#playerrankinginfo_permaprank)
- 📋 [PrefetchType](#prefetchtype)
- 🔌 [ProtoFlattenedSerializerField_t](#protoflattenedserializerfield_t)
- 🔌 [ProtoFlattenedSerializerField_t_polymorphic_field_t](#protoflattenedserializerfield_t_polymorphic_field_t)
- 🔌 [ProtoFlattenedSerializer_t](#protoflattenedserializer_t)
- 📋 [QuestType](#questtype)
- 📋 [ReplayEventType_t](#replayeventtype_t)
- 📋 [RequestPause_t](#requestpause_t)
- 📋 [SVC_Messages](#svc_messages)
- 📋 [SVC_Messages_LowFrequency](#svc_messages_lowfrequency)
- 🔌 [ScoreLeaderboardData](#scoreleaderboarddata)
- 🔌 [ScoreLeaderboardData_AccountEntries](#scoreleaderboarddata_accountentries)
- 🔌 [ScoreLeaderboardData_Entry](#scoreleaderboarddata_entry)
- 🔌 [ServerHltvInfo](#serverhltvinfo)
- 📋 [SignonState_t](#signonstate_t)
- 📋 [SpawnGroupFlags_t](#spawngroupflags_t)
- 🔌 [TournamentEvent](#tournamentevent)
- 🔌 [TournamentMatchSetup](#tournamentmatchsetup)
- 🔌 [TournamentPlayer](#tournamentplayer)
- 🔌 [TournamentTeam](#tournamentteam)
- 🔌 [VacNetShot](#vacnetshot)
- 📋 [VoiceDataFormat_t](#voicedataformat_t)
- 🔌 [WatchableMatchInfo](#watchablematchinfo)
- 🔌 [XpProgressData](#xpprogressdata)
- 📋 [eRollType](#erolltype)

## 🔌 AccountActivity

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<AccountActivity\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Activity` | `uint` | get, set | - |
| `Mode` | `uint` | get, set | - |
| `Map` | `uint` | get, set | - |
| `Matchid` | `ulong` | get, set | - |



---

## 📋 Bidirectional_Messages

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `bi_RebroadcastGameEvent` | `16` | - |
| `bi_RebroadcastSource` | `17` | - |
| `bi_GameEvent` | `18` | - |
| `bi_PredictionEvent` | `19` | - |



---

## 📋 Bidirectional_Messages_LowFrequency

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `bi_RelayInfo` | `700` | - |
| `bi_RelayPacket` | `701` | - |



---

## 🔌 C2S_CONNECTION_Message

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<C2S_CONNECTION_Message\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AddonName` | `string` | get, set | - |
| `LocalhostSameProcessCheck` | `C2S_CONNECT_SameProcessCheck` | get | - |



---

## 🔌 C2S_CONNECT_Message

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<C2S_CONNECT_Message\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `HostVersion` | `uint` | get, set | - |
| `AuthProtocol` | `uint` | get, set | - |
| `ChallengeNumber` | `uint` | get, set | - |
| `ReservationCookie` | `ulong` | get, set | - |
| `LowViolence` | `bool` | get, set | - |
| `EncryptedPassword` | `byte[]` | get, set | - |
| `Splitplayers` | `IProtobufRepeatedFieldSubMessageType\<CCLCMsg_SplitPlayerConnect\>` | get | - |
| `AuthSteam` | `byte[]` | get, set | - |
| `ChallengeContext` | `string` | get, set | - |
| `LocalhostSameProcessCheck` | `C2S_CONNECT_SameProcessCheck` | get | - |



---

## 🔌 C2S_CONNECT_SameProcessCheck

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<C2S_CONNECT_SameProcessCheck\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `LocalhostProcessId` | `ulong` | get, set | - |
| `Key` | `ulong` | get, set | - |



---

## 🔌 CAttribute_String

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`



---

## 🔌 CBaseUserCmdExecutionNotes

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CBaseUserCmdExecutionNotes\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `IgnoredReason` | `string` | get, set | - |



---

## 🔌 CBaseUserCmdPB

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CBaseUserCmdPB\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `LegacyCommandNumber` | `int` | get, set | - |
| `ClientTick` | `int` | get, set | - |
| `PredictionOffsetTicksX256` | `uint` | get, set | - |
| `ButtonsPb` | `CInButtonStatePB` | get | - |
| `Viewangles` | `QAngle` | get, set | - |
| `Forwardmove` | `float` | get, set | - |
| `Leftmove` | `float` | get, set | - |
| `Upmove` | `float` | get, set | - |
| `Impulse` | `int` | get, set | - |
| `Weaponselect` | `int` | get, set | - |
| `RandomSeed` | `int` | get, set | - |
| `Mousedx` | `int` | get, set | - |
| `Mousedy` | `int` | get, set | - |
| `PawnEntityHandle` | `uint` | get, set | - |
| `SubtickMoves` | `IProtobufRepeatedFieldSubMessageType\<CSubtickMoveStep\>` | get | - |
| `MoveCrc` | `byte[]` | get, set | - |
| `ConsumedServerAngleChanges` | `uint` | get, set | - |
| `CmdFlags` | `int` | get, set | - |
| `ExecutionNotes` | `CBaseUserCmdExecutionNotes` | get | - |



---

## 🔌 CBidirMsg_PredictionEvent

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CBidirMsg_PredictionEvent\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EventId` | `uint` | get, set | - |
| `EventData` | `byte[]` | get, set | - |
| `SyncType` | `uint` | get, set | - |
| `SyncValUint32` | `uint` | get, set | - |



---

## 📋 CBidirMsg_PredictionEvent_ESyncType

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `ST_Tick` | `0` | - |
| `ST_UserCmdNum` | `1` | - |



---

## 🔌 CBidirMsg_RebroadcastGameEvent

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CBidirMsg_RebroadcastGameEvent\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Posttoserver` | `bool` | get, set | - |
| `Buftype` | `int` | get, set | - |
| `Clientbitcount` | `uint` | get, set | - |
| `Receivingclients` | `ulong` | get, set | - |



---

## 🔌 CBidirMsg_RebroadcastSource

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CBidirMsg_RebroadcastSource\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Eventsource` | `int` | get, set | - |



---

## 🔌 CCLCMsg_BaselineAck

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCLCMsg_BaselineAck\>`

**实现接口:** `INetMessage\<CCLCMsg_BaselineAck\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `BaselineTick` | `int` | get, set | - |
| `BaselineNr` | `int` | get, set | - |



---

## 🔌 CCLCMsg_ClientInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCLCMsg_ClientInfo\>`

**实现接口:** `INetMessage\<CCLCMsg_ClientInfo\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SendTableCrc` | `uint` | get, set | - |
| `ServerCount` | `uint` | get, set | - |
| `IsHltv` | `bool` | get, set | - |
| `FriendsId` | `uint` | get, set | - |
| `FriendsName` | `string` | get, set | - |



---

## 🔌 CCLCMsg_CmdKeyValues

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCLCMsg_CmdKeyValues\>`

**实现接口:** `INetMessage\<CCLCMsg_CmdKeyValues\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Data` | `byte[]` | get, set | - |



---

## 🔌 CCLCMsg_Diagnostic

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCLCMsg_Diagnostic\>`

**实现接口:** `INetMessage\<CCLCMsg_Diagnostic\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SystemSpecs` | `CMsgSource2SystemSpecs` | get | - |
| `VprofReport` | `CMsgSource2VProfLiteReport` | get | - |
| `DownstreamFlow` | `CMsgSource2NetworkFlowQuality` | get | - |
| `UpstreamFlow` | `CMsgSource2NetworkFlowQuality` | get | - |
| `PerfSamples` | `IProtobufRepeatedFieldSubMessageType\<CMsgSource2PerfIntervalSample\>` | get | - |



---

## 🔌 CCLCMsg_HltvFixupOperatorTick

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCLCMsg_HltvFixupOperatorTick\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Tick` | `int` | get, set | - |
| `PropsData` | `byte[]` | get, set | - |
| `Origin` | `Vector` | get, set | - |
| `EyeAngles` | `QAngle` | get, set | - |
| `ObserverMode` | `int` | get, set | - |
| `CameramanScoreboard` | `bool` | get, set | - |
| `ObserverTarget` | `int` | get, set | - |
| `ViewOffset` | `Vector` | get, set | - |



---

## 🔌 CCLCMsg_HltvReplay

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCLCMsg_HltvReplay\>`

**实现接口:** `INetMessage\<CCLCMsg_HltvReplay\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Request` | `int` | get, set | - |
| `SlowdownLength` | `float` | get, set | - |
| `SlowdownRate` | `float` | get, set | - |
| `PrimaryTarget` | `int` | get, set | - |
| `EventTime` | `float` | get, set | - |



---

## 🔌 CCLCMsg_ListenEvents

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCLCMsg_ListenEvents\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EventMask` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |



---

## 🔌 CCLCMsg_LoadingProgress

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCLCMsg_LoadingProgress\>`

**实现接口:** `INetMessage\<CCLCMsg_LoadingProgress\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Progress` | `int` | get, set | - |



---

## 🔌 CCLCMsg_Move

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCLCMsg_Move\>`

**实现接口:** `INetMessage\<CCLCMsg_Move\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Data` | `byte[]` | get, set | - |
| `LastCommandNumber` | `uint` | get, set | - |



---

## 🔌 CCLCMsg_RconServerDetails

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCLCMsg_RconServerDetails\>`

**实现接口:** `INetMessage\<CCLCMsg_RconServerDetails\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Token` | `byte[]` | get, set | - |



---

## 🔌 CCLCMsg_RequestPause

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCLCMsg_RequestPause\>`

**实现接口:** `INetMessage\<CCLCMsg_RequestPause\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PauseType` | `RequestPause_t` | get, set | - |
| `PauseGroup` | `int` | get, set | - |



---

## 🔌 CCLCMsg_RespondCvarValue

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCLCMsg_RespondCvarValue\>`

**实现接口:** `INetMessage\<CCLCMsg_RespondCvarValue\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Cookie` | `int` | get, set | - |
| `StatusCode` | `int` | get, set | - |
| `Name` | `string` | get, set | - |
| `Value` | `string` | get, set | - |



---

## 🔌 CCLCMsg_ServerStatus

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCLCMsg_ServerStatus\>`

**实现接口:** `INetMessage\<CCLCMsg_ServerStatus\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Simplified` | `bool` | get, set | - |



---

## 🔌 CCLCMsg_SplitPlayerConnect

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCLCMsg_SplitPlayerConnect\>`

**实现接口:** `INetMessage\<CCLCMsg_SplitPlayerConnect\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Playername` | `string` | get, set | - |



---

## 🔌 CCLCMsg_SplitPlayerDisconnect

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCLCMsg_SplitPlayerDisconnect\>`

**实现接口:** `INetMessage\<CCLCMsg_SplitPlayerDisconnect\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Slot` | `int` | get, set | - |



---

## 🔌 CCLCMsg_VoiceData

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCLCMsg_VoiceData\>`

**实现接口:** `INetMessage\<CCLCMsg_VoiceData\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Audio` | `CMsgVoiceAudio` | get | - |
| `Xuid` | `ulong` | get, set | - |
| `Tick` | `uint` | get, set | - |



---

## 🔌 CCSPredictionEvent_AddAimPunch

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSPredictionEvent_AddAimPunch\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PunchAngle` | `QAngle` | get, set | - |
| `WhenTick` | `uint` | get, set | - |
| `WhenTickFrac` | `float` | get, set | - |



---

## 🔌 CCSPredictionEvent_DamageTag

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSPredictionEvent_DamageTag\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `FlinchModSmall` | `float` | get, set | - |
| `FlinchModLarge` | `float` | get, set | - |
| `FriendlyFireDamageReductionRatio` | `float` | get, set | - |



---

## 🔌 CCSUsrMsgPreMatchSayText

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsgPreMatchSayText\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AccountId` | `uint` | get, set | - |
| `Text` | `string` | get, set | - |
| `AllChat` | `bool` | get, set | - |



---

## 🔌 CCSUsrMsg_AchievementEvent

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_AchievementEvent\>`

**实现接口:** `INetMessage\<CCSUsrMsg_AchievementEvent\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Achievement` | `int` | get, set | - |
| `Count` | `int` | get, set | - |
| `UserId` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_AdjustMoney

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_AdjustMoney\>`

**实现接口:** `INetMessage\<CCSUsrMsg_AdjustMoney\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Amount` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_AmmoDenied

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_AmmoDenied\>`

**实现接口:** `INetMessage\<CCSUsrMsg_AmmoDenied\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Ammoidx` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_BarTime

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_BarTime\>`

**实现接口:** `INetMessage\<CCSUsrMsg_BarTime\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Time` | `string` | get, set | - |



---

## 🔌 CCSUsrMsg_CallVoteFailed

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_CallVoteFailed\>`

**实现接口:** `INetMessage\<CCSUsrMsg_CallVoteFailed\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Reason` | `int` | get, set | - |
| `Time` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_ClientInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_ClientInfo\>`

**实现接口:** `INetMessage\<CCSUsrMsg_ClientInfo\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Dummy` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_CloseCaption

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_CloseCaption\>`

**实现接口:** `INetMessage\<CCSUsrMsg_CloseCaption\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Hash` | `uint` | get, set | - |
| `Duration` | `int` | get, set | - |
| `FromPlayer` | `bool` | get, set | - |
| `Cctoken` | `string` | get, set | - |



---

## 🔌 CCSUsrMsg_CloseCaptionDirect

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_CloseCaptionDirect\>`

**实现接口:** `INetMessage\<CCSUsrMsg_CloseCaptionDirect\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Hash` | `uint` | get, set | - |
| `Duration` | `int` | get, set | - |
| `FromPlayer` | `bool` | get, set | - |



---

## 🔌 CCSUsrMsg_CounterStrafe

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_CounterStrafe\>`

**实现接口:** `INetMessage\<CCSUsrMsg_CounterStrafe\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PressToReleaseNs` | `int` | get, set | - |
| `TotalKeysDown` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_CurrentRoundOdds

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_CurrentRoundOdds\>`

**实现接口:** `INetMessage\<CCSUsrMsg_CurrentRoundOdds\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Odds` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_CurrentTimescale

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_CurrentTimescale\>`

**实现接口:** `INetMessage\<CCSUsrMsg_CurrentTimescale\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CurTimescale` | `float` | get, set | - |



---

## 🔌 CCSUsrMsg_Damage

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_Damage\>`

**实现接口:** `INetMessage\<CCSUsrMsg_Damage\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Amount` | `int` | get, set | - |
| `InflictorWorldPos` | `Vector` | get, set | - |
| `VictimEntindex` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_DamagePrediction

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_DamagePrediction\>`

**实现接口:** `INetMessage\<CCSUsrMsg_DamagePrediction\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CommandNum` | `int` | get, set | - |
| `PelletIdx` | `int` | get, set | - |
| `VictimSlot` | `int` | get, set | - |
| `VictimStartingHealth` | `int` | get, set | - |
| `VictimDamage` | `int` | get, set | - |
| `ShootPos` | `Vector` | get, set | - |
| `ShootDir` | `QAngle` | get, set | - |
| `AimPunch` | `QAngle` | get, set | - |



---

## 🔌 CCSUsrMsg_DeepStats

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_DeepStats\>`

**实现接口:** `INetMessage\<CCSUsrMsg_DeepStats\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Stats` | `CMsgGCCStrike15_ClientDeepStats` | get | - |



---

## 🔌 CCSUsrMsg_DesiredTimescale

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_DesiredTimescale\>`

**实现接口:** `INetMessage\<CCSUsrMsg_DesiredTimescale\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `DesiredTimescale` | `float` | get, set | - |
| `DurationRealtimeSec` | `float` | get, set | - |
| `InterpolatorType` | `int` | get, set | - |
| `StartBlendTime` | `float` | get, set | - |



---

## 🔌 CCSUsrMsg_DisconnectToLobby

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_DisconnectToLobby\>`

**实现接口:** `INetMessage\<CCSUsrMsg_DisconnectToLobby\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Dummy` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_EndOfMatchAllPlayersData

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_EndOfMatchAllPlayersData\>`

**实现接口:** `INetMessage\<CCSUsrMsg_EndOfMatchAllPlayersData\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Allplayerdata` | `IProtobufRepeatedFieldSubMessageType\<CCSUsrMsg_EndOfMatchAllPlayersData_PlayerData\>` | get | - |
| `Scene` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_EndOfMatchAllPlayersData_Accolade

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_EndOfMatchAllPlayersData_Accolade\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Eaccolade` | `int` | get, set | - |
| `Value` | `float` | get, set | - |
| `Position` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_EndOfMatchAllPlayersData_PlayerData

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_EndOfMatchAllPlayersData_PlayerData\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Slot` | `int` | get, set | - |
| `Xuid` | `ulong` | get, set | - |
| `Name` | `string` | get, set | - |
| `Teamnumber` | `int` | get, set | - |
| `Nomination` | `CCSUsrMsg_EndOfMatchAllPlayersData_Accolade` | get | - |
| `Items` | `IProtobufRepeatedFieldSubMessageType\<CEconItemPreviewDataBlock\>` | get | - |
| `Playercolor` | `int` | get, set | - |
| `Isbot` | `bool` | get, set | - |



---

## 🔌 CCSUsrMsg_EntityOutlineHighlight

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_EntityOutlineHighlight\>`

**实现接口:** `INetMessage\<CCSUsrMsg_EntityOutlineHighlight\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Entidx` | `int` | get, set | - |
| `Removehighlight` | `bool` | get, set | - |



---

## 🔌 CCSUsrMsg_Fade

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_Fade\>`

**实现接口:** `INetMessage\<CCSUsrMsg_Fade\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Duration` | `int` | get, set | - |
| `HoldTime` | `int` | get, set | - |
| `Flags` | `int` | get, set | - |
| `Clr` | `Color` | get, set | - |



---

## 🔌 CCSUsrMsg_GameTitle

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_GameTitle\>`

**实现接口:** `INetMessage\<CCSUsrMsg_GameTitle\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Dummy` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_Geiger

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_Geiger\>`

**实现接口:** `INetMessage\<CCSUsrMsg_Geiger\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Range` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_HintText

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_HintText\>`

**实现接口:** `INetMessage\<CCSUsrMsg_HintText\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Message` | `string` | get, set | - |



---

## 🔌 CCSUsrMsg_HudMsg

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_HudMsg\>`

**实现接口:** `INetMessage\<CCSUsrMsg_HudMsg\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Channel` | `int` | get, set | - |
| `Pos` | `Vector2D` | get, set | - |
| `Clr1` | `Color` | get, set | - |
| `Clr2` | `Color` | get, set | - |
| `Effect` | `int` | get, set | - |
| `FadeInTime` | `float` | get, set | - |
| `FadeOutTime` | `float` | get, set | - |
| `HoldTime` | `float` | get, set | - |
| `FxTime` | `float` | get, set | - |
| `Text` | `string` | get, set | - |



---

## 🔌 CCSUsrMsg_HudText

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_HudText\>`

**实现接口:** `INetMessage\<CCSUsrMsg_HudText\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Text` | `string` | get, set | - |



---

## 🔌 CCSUsrMsg_ItemDrop

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_ItemDrop\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Itemid` | `long` | get, set | - |
| `Death` | `bool` | get, set | - |



---

## 🔌 CCSUsrMsg_ItemPickup

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_ItemPickup\>`

**实现接口:** `INetMessage\<CCSUsrMsg_ItemPickup\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Item` | `string` | get, set | - |



---

## 🔌 CCSUsrMsg_KeyHintText

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_KeyHintText\>`

**实现接口:** `INetMessage\<CCSUsrMsg_KeyHintText\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Messages` | `IProtobufRepeatedFieldValueType\<string\>` | get | - |



---

## 🔌 CCSUsrMsg_KillCam

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_KillCam\>`

**实现接口:** `INetMessage\<CCSUsrMsg_KillCam\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ObsMode` | `int` | get, set | - |
| `FirstTarget` | `int` | get, set | - |
| `SecondTarget` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_MarkAchievement

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_MarkAchievement\>`

**实现接口:** `INetMessage\<CCSUsrMsg_MarkAchievement\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Achievement` | `string` | get, set | - |



---

## 🔌 CCSUsrMsg_MatchEndConditions

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_MatchEndConditions\>`

**实现接口:** `INetMessage\<CCSUsrMsg_MatchEndConditions\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Fraglimit` | `int` | get, set | - |
| `MpMaxrounds` | `int` | get, set | - |
| `MpWinlimit` | `int` | get, set | - |
| `MpTimelimit` | `float` | get, set | - |



---

## 🔌 CCSUsrMsg_MatchStatsUpdate

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_MatchStatsUpdate\>`

**实现接口:** `INetMessage\<CCSUsrMsg_MatchStatsUpdate\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Update` | `string` | get, set | - |



---

## 🔌 CCSUsrMsg_PlayerDecalDigitalSignature

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_PlayerDecalDigitalSignature\>`

**实现接口:** `INetMessage\<CCSUsrMsg_PlayerDecalDigitalSignature\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Data` | `PlayerDecalDigitalSignature` | get | - |



---

## 🔌 CCSUsrMsg_PlayerStatsUpdate

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_PlayerStatsUpdate\>`

**实现接口:** `INetMessage\<CCSUsrMsg_PlayerStatsUpdate\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Version` | `int` | get, set | - |
| `Stats` | `IProtobufRepeatedFieldSubMessageType\<CCSUsrMsg_PlayerStatsUpdate_Stat\>` | get | - |
| `Ehandle` | `uint` | get, set | - |
| `Crc` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_PlayerStatsUpdate_Stat

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_PlayerStatsUpdate_Stat\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Idx` | `int` | get, set | - |
| `Delta` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_PostRoundDamageReport

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_PostRoundDamageReport\>`

**实现接口:** `INetMessage\<CCSUsrMsg_PostRoundDamageReport\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `OtherXuid` | `ulong` | get, set | - |
| `GivenKillType` | `int` | get, set | - |
| `GivenHealthRemoved` | `int` | get, set | - |
| `GivenNumHits` | `int` | get, set | - |
| `TakenKillType` | `int` | get, set | - |
| `TakenHealthRemoved` | `int` | get, set | - |
| `TakenNumHits` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_ProcessSpottedEntityUpdate

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_ProcessSpottedEntityUpdate\>`

**实现接口:** `INetMessage\<CCSUsrMsg_ProcessSpottedEntityUpdate\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `NewUpdate` | `bool` | get, set | - |
| `EntityUpdates` | `IProtobufRepeatedFieldSubMessageType\<CCSUsrMsg_ProcessSpottedEntityUpdate_SpottedEntityUpdate\>` | get | - |



---

## 🔌 CCSUsrMsg_ProcessSpottedEntityUpdate_SpottedEntityUpdate

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_ProcessSpottedEntityUpdate_SpottedEntityUpdate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityIdx` | `int` | get, set | - |
| `ClassId` | `int` | get, set | - |
| `OriginX` | `int` | get, set | - |
| `OriginY` | `int` | get, set | - |
| `OriginZ` | `int` | get, set | - |
| `AngleY` | `int` | get, set | - |
| `Defuser` | `bool` | get, set | - |
| `PlayerHasDefuser` | `bool` | get, set | - |
| `PlayerHasC4` | `bool` | get, set | - |



---

## 🔌 CCSUsrMsg_QuestProgress

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_QuestProgress\>`

**实现接口:** `INetMessage\<CCSUsrMsg_QuestProgress\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `QuestId` | `uint` | get, set | - |
| `NormalPoints` | `uint` | get, set | - |
| `BonusPoints` | `uint` | get, set | - |
| `IsEventQuest` | `bool` | get, set | - |



---

## 🔌 CCSUsrMsg_RadioText

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_RadioText\>`

**实现接口:** `INetMessage\<CCSUsrMsg_RadioText\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MsgDst` | `int` | get, set | - |
| `Client` | `int` | get, set | - |
| `MsgName` | `string` | get, set | - |
| `Params` | `IProtobufRepeatedFieldValueType\<string\>` | get | - |



---

## 🔌 CCSUsrMsg_RawAudio

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_RawAudio\>`

**实现接口:** `INetMessage\<CCSUsrMsg_RawAudio\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Pitch` | `int` | get, set | - |
| `Entidx` | `int` | get, set | - |
| `Duration` | `float` | get, set | - |
| `VoiceFilename` | `string` | get, set | - |



---

## 🔌 CCSUsrMsg_RecurringMissionSchema

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_RecurringMissionSchema\>`

**实现接口:** `INetMessage\<CCSUsrMsg_RecurringMissionSchema\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Period` | `uint` | get, set | - |
| `MissionSchema` | `byte[]` | get, set | - |



---

## 🔌 CCSUsrMsg_ReloadEffect

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_ReloadEffect\>`

**实现接口:** `INetMessage\<CCSUsrMsg_ReloadEffect\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Entidx` | `int` | get, set | - |
| `Actanim` | `int` | get, set | - |
| `OriginX` | `float` | get, set | - |
| `OriginY` | `float` | get, set | - |
| `OriginZ` | `float` | get, set | - |



---

## 🔌 CCSUsrMsg_ReportHit

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_ReportHit\>`

**实现接口:** `INetMessage\<CCSUsrMsg_ReportHit\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PosX` | `float` | get, set | - |
| `PosY` | `float` | get, set | - |
| `Timestamp` | `float` | get, set | - |
| `PosZ` | `float` | get, set | - |



---

## 🔌 CCSUsrMsg_RequestState

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_RequestState\>`

**实现接口:** `INetMessage\<CCSUsrMsg_RequestState\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Dummy` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_ResetHud

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_ResetHud\>`

**实现接口:** `INetMessage\<CCSUsrMsg_ResetHud\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Reset` | `bool` | get, set | - |



---

## 🔌 CCSUsrMsg_RoundBackupFilenames

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_RoundBackupFilenames\>`

**实现接口:** `INetMessage\<CCSUsrMsg_RoundBackupFilenames\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Count` | `int` | get, set | - |
| `Index` | `int` | get, set | - |
| `Filename` | `string` | get, set | - |
| `Nicename` | `string` | get, set | - |



---

## 🔌 CCSUsrMsg_RoundEndReportData

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_RoundEndReportData\>`

**实现接口:** `INetMessage\<CCSUsrMsg_RoundEndReportData\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `InitConditions` | `CCSUsrMsg_RoundEndReportData_InitialConditions` | get | - |
| `AllRerEventData` | `IProtobufRepeatedFieldSubMessageType\<CCSUsrMsg_RoundEndReportData_RerEvent\>` | get | - |



---

## 🔌 CCSUsrMsg_RoundEndReportData_InitialConditions

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_RoundEndReportData_InitialConditions\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CtEquipValue` | `int` | get, set | - |
| `TEquipValue` | `int` | get, set | - |
| `TerroristOdds` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_RoundEndReportData_RerEvent

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_RoundEndReportData_RerEvent\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Timestamp` | `float` | get, set | - |
| `TerroristOdds` | `int` | get, set | - |
| `CtAlive` | `int` | get, set | - |
| `TAlive` | `int` | get, set | - |
| `VictimData` | `CCSUsrMsg_RoundEndReportData_RerEvent_Victim` | get | - |
| `ObjectiveData` | `CCSUsrMsg_RoundEndReportData_RerEvent_Objective` | get | - |
| `AllDamageData` | `IProtobufRepeatedFieldSubMessageType\<CCSUsrMsg_RoundEndReportData_RerEvent_Damage\>` | get | - |



---

## 🔌 CCSUsrMsg_RoundEndReportData_RerEvent_Damage

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_RoundEndReportData_RerEvent_Damage\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `OtherPlayerslot` | `int` | get, set | - |
| `OtherXuid` | `ulong` | get, set | - |
| `HealthRemoved` | `int` | get, set | - |
| `NumHits` | `int` | get, set | - |
| `ReturnHealthRemoved` | `int` | get, set | - |
| `ReturnNumHits` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_RoundEndReportData_RerEvent_Objective

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_RoundEndReportData_RerEvent_Objective\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Type` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_RoundEndReportData_RerEvent_Victim

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_RoundEndReportData_RerEvent_Victim\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TeamNumber` | `int` | get, set | - |
| `Playerslot` | `int` | get, set | - |
| `Xuid` | `ulong` | get, set | - |
| `Color` | `int` | get, set | - |
| `IsBot` | `bool` | get, set | - |
| `IsDead` | `bool` | get, set | - |



---

## 🔌 CCSUsrMsg_Rumble

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_Rumble\>`

**实现接口:** `INetMessage\<CCSUsrMsg_Rumble\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Index` | `int` | get, set | - |
| `Data` | `int` | get, set | - |
| `Flags` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_SSUI

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_SSUI\>`

**实现接口:** `INetMessage\<CCSUsrMsg_SSUI\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Show` | `bool` | get, set | - |
| `StartTime` | `float` | get, set | - |
| `EndTime` | `float` | get, set | - |



---

## 🔌 CCSUsrMsg_ScoreLeaderboardData

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_ScoreLeaderboardData\>`

**实现接口:** `INetMessage\<CCSUsrMsg_ScoreLeaderboardData\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Data` | `ScoreLeaderboardData` | get | - |



---

## 🔌 CCSUsrMsg_SendAudio

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_SendAudio\>`

**实现接口:** `INetMessage\<CCSUsrMsg_SendAudio\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `RadioSound` | `string` | get, set | - |



---

## 🔌 CCSUsrMsg_SendLastKillerDamageToClient

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_SendLastKillerDamageToClient\>`

**实现接口:** `INetMessage\<CCSUsrMsg_SendLastKillerDamageToClient\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `NumHitsGiven` | `int` | get, set | - |
| `DamageGiven` | `int` | get, set | - |
| `NumHitsTaken` | `int` | get, set | - |
| `DamageTaken` | `int` | get, set | - |
| `ActualDamageGiven` | `int` | get, set | - |
| `ActualDamageTaken` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_SendPlayerItemDrops

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_SendPlayerItemDrops\>`

**实现接口:** `INetMessage\<CCSUsrMsg_SendPlayerItemDrops\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityUpdates` | `IProtobufRepeatedFieldSubMessageType\<CEconItemPreviewDataBlock\>` | get | - |



---

## 🔌 CCSUsrMsg_SendPlayerItemFound

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_SendPlayerItemFound\>`

**实现接口:** `INetMessage\<CCSUsrMsg_SendPlayerItemFound\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Iteminfo` | `CEconItemPreviewDataBlock` | get | - |
| `Playerslot` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_SendPlayerLoadout

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_SendPlayerLoadout\>`

**实现接口:** `INetMessage\<CCSUsrMsg_SendPlayerLoadout\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Loadout` | `IProtobufRepeatedFieldSubMessageType\<CCSUsrMsg_SendPlayerLoadout_LoadoutItem\>` | get | - |
| `Playerslot` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_SendPlayerLoadout_LoadoutItem

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_SendPlayerLoadout_LoadoutItem\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EconItem` | `CEconItemPreviewDataBlock` | get | - |
| `Team` | `int` | get, set | - |
| `Slot` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_ServerRankRevealAll

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_ServerRankRevealAll\>`

**实现接口:** `INetMessage\<CCSUsrMsg_ServerRankRevealAll\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SecondsTillShutdown` | `int` | get, set | - |
| `Reservation` | `CMsgGCCStrike15_v2_MatchmakingGC2ServerReserve` | get | - |



---

## 🔌 CCSUsrMsg_ServerRankUpdate

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_ServerRankUpdate\>`

**实现接口:** `INetMessage\<CCSUsrMsg_ServerRankUpdate\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `RankUpdate` | `IProtobufRepeatedFieldSubMessageType\<CCSUsrMsg_ServerRankUpdate_RankUpdate\>` | get | - |



---

## 🔌 CCSUsrMsg_ServerRankUpdate_RankUpdate

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_ServerRankUpdate_RankUpdate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AccountId` | `int` | get, set | - |
| `RankOld` | `int` | get, set | - |
| `RankNew` | `int` | get, set | - |
| `NumWins` | `int` | get, set | - |
| `RankChange` | `float` | get, set | - |
| `RankTypeId` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_Shake

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_Shake\>`

**实现接口:** `INetMessage\<CCSUsrMsg_Shake\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Command` | `int` | get, set | - |
| `LocalAmplitude` | `float` | get, set | - |
| `Frequency` | `float` | get, set | - |
| `Duration` | `float` | get, set | - |



---

## 🔌 CCSUsrMsg_ShootInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_ShootInfo\>`

**实现接口:** `INetMessage\<CCSUsrMsg_ShootInfo\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `FrameNumber` | `int` | get, set | - |
| `HitboxTransforms` | `IProtobufRepeatedFieldSubMessageType\<CMsgTransform\>` | get | - |
| `ShootPos` | `Vector` | get, set | - |
| `ShootDir` | `QAngle` | get, set | - |



---

## 🔌 CCSUsrMsg_ShowMenu

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_ShowMenu\>`

**实现接口:** `INetMessage\<CCSUsrMsg_ShowMenu\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `BitsValidSlots` | `int` | get, set | - |
| `DisplayTime` | `int` | get, set | - |
| `MenuString` | `string` | get, set | - |



---

## 🔌 CCSUsrMsg_StopSpectatorMode

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_StopSpectatorMode\>`

**实现接口:** `INetMessage\<CCSUsrMsg_StopSpectatorMode\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Dummy` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_SurvivalStats

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_SurvivalStats\>`

**实现接口:** `INetMessage\<CCSUsrMsg_SurvivalStats\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Xuid` | `ulong` | get, set | - |
| `Facts` | `IProtobufRepeatedFieldSubMessageType\<CCSUsrMsg_SurvivalStats_Fact\>` | get | - |
| `Users` | `IProtobufRepeatedFieldSubMessageType\<CCSUsrMsg_SurvivalStats_Placement\>` | get | - |
| `Damages` | `IProtobufRepeatedFieldSubMessageType\<CCSUsrMsg_SurvivalStats_Damage\>` | get | - |
| `Ticknumber` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_SurvivalStats_Damage

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_SurvivalStats_Damage\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Xuid` | `ulong` | get, set | - |
| `To` | `int` | get, set | - |
| `ToHits` | `int` | get, set | - |
| `From` | `int` | get, set | - |
| `FromHits` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_SurvivalStats_Fact

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_SurvivalStats_Fact\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Type` | `int` | get, set | - |
| `Display` | `int` | get, set | - |
| `Value` | `int` | get, set | - |
| `Interestingness` | `float` | get, set | - |



---

## 🔌 CCSUsrMsg_SurvivalStats_Placement

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_SurvivalStats_Placement\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Xuid` | `ulong` | get, set | - |
| `Teamnumber` | `int` | get, set | - |
| `Placement` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_Train

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_Train\>`

**实现接口:** `INetMessage\<CCSUsrMsg_Train\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Train` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_UpdateScreenHealthBar

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_UpdateScreenHealthBar\>`

**实现接口:** `INetMessage\<CCSUsrMsg_UpdateScreenHealthBar\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Entidx` | `int` | get, set | - |
| `HealthratioOld` | `float` | get, set | - |
| `HealthratioNew` | `float` | get, set | - |
| `Style` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_VGUIMenu

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_VGUIMenu\>`

**实现接口:** `INetMessage\<CCSUsrMsg_VGUIMenu\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | get, set | - |
| `Show` | `bool` | get, set | - |
| `Keys` | `IProtobufRepeatedFieldSubMessageType\<CCSUsrMsg_VGUIMenu_Keys\>` | get | - |



---

## 🔌 CCSUsrMsg_VGUIMenu_Keys

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_VGUIMenu_Keys\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | get, set | - |
| `Value` | `string` | get, set | - |



---

## 🔌 CCSUsrMsg_VoiceMask

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_VoiceMask\>`

**实现接口:** `INetMessage\<CCSUsrMsg_VoiceMask\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlayerMasks` | `IProtobufRepeatedFieldSubMessageType\<CCSUsrMsg_VoiceMask_PlayerMask\>` | get | - |
| `PlayerModEnable` | `bool` | get, set | - |



---

## 🔌 CCSUsrMsg_VoiceMask_PlayerMask

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_VoiceMask_PlayerMask\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `GameRulesMask` | `int` | get, set | - |
| `BanMasks` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_VoteFailed

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_VoteFailed\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Team` | `int` | get, set | - |
| `Reason` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_VotePass

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_VotePass\>`

**实现接口:** `INetMessage\<CCSUsrMsg_VotePass\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Team` | `int` | get, set | - |
| `VoteType` | `int` | get, set | - |
| `DispStr` | `string` | get, set | - |
| `DetailsStr` | `string` | get, set | - |



---

## 🔌 CCSUsrMsg_VoteSetup

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_VoteSetup\>`

**实现接口:** `INetMessage\<CCSUsrMsg_VoteSetup\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PotentialIssues` | `IProtobufRepeatedFieldValueType\<string\>` | get | - |



---

## 🔌 CCSUsrMsg_VoteStart

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_VoteStart\>`

**实现接口:** `INetMessage\<CCSUsrMsg_VoteStart\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Team` | `int` | get, set | - |
| `PlayerSlot` | `int` | get, set | - |
| `VoteType` | `int` | get, set | - |
| `DispStr` | `string` | get, set | - |
| `DetailsStr` | `string` | get, set | - |
| `OtherTeamStr` | `string` | get, set | - |
| `IsYesNoVote` | `bool` | get, set | - |
| `PlayerSlotTarget` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_WeaponSound

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_WeaponSound\>`

**实现接口:** `INetMessage\<CCSUsrMsg_WeaponSound\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Entidx` | `int` | get, set | - |
| `OriginX` | `float` | get, set | - |
| `OriginY` | `float` | get, set | - |
| `OriginZ` | `float` | get, set | - |
| `Sound` | `string` | get, set | - |
| `GameTimestamp` | `float` | get, set | - |
| `SourceSoundscapeid` | `uint` | get, set | - |



---

## 🔌 CCSUsrMsg_XRankGet

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_XRankGet\>`

**实现接口:** `INetMessage\<CCSUsrMsg_XRankGet\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ModeIdx` | `int` | get, set | - |
| `Controller` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_XRankUpd

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_XRankUpd\>`

**实现接口:** `INetMessage\<CCSUsrMsg_XRankUpd\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ModeIdx` | `int` | get, set | - |
| `Controller` | `int` | get, set | - |
| `Ranking` | `int` | get, set | - |



---

## 🔌 CCSUsrMsg_XpUpdate

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCSUsrMsg_XpUpdate\>`

**实现接口:** `INetMessage\<CCSUsrMsg_XpUpdate\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Data` | `CMsgGCCstrike15_v2_GC2ServerNotifyXPRewarded` | get | - |



---

## 🔌 CChinaAgreementSessions_StartAgreementSessionInGame_Request

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CChinaAgreementSessions_StartAgreementSessionInGame_Request\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Appid` | `uint` | get, set | - |
| `Steamid` | `ulong` | get, set | - |
| `ClientIpaddress` | `string` | get, set | - |



---

## 🔌 CChinaAgreementSessions_StartAgreementSessionInGame_Response

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CChinaAgreementSessions_StartAgreementSessionInGame_Response\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AgreementUrl` | `string` | get, set | - |



---

## 🔌 CClientHeaderOverwatchEvidence

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CClientHeaderOverwatchEvidence\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Accountid` | `uint` | get, set | - |
| `Caseid` | `ulong` | get, set | - |



---

## 🔌 CClientMsg_ClientUIEvent

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CClientMsg_ClientUIEvent\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Event` | `EClientUIEvent` | get, set | - |
| `EntEhandle` | `uint` | get, set | - |
| `ClientEhandle` | `uint` | get, set | - |
| `Data1` | `string` | get, set | - |
| `Data2` | `string` | get, set | - |



---

## 🔌 CClientMsg_CustomGameEvent

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CClientMsg_CustomGameEvent\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EventName` | `string` | get, set | - |
| `Data` | `byte[]` | get, set | - |



---

## 🔌 CClientMsg_CustomGameEventBounce

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CClientMsg_CustomGameEventBounce\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EventName` | `string` | get, set | - |
| `Data` | `byte[]` | get, set | - |
| `PlayerSlot` | `int` | get, set | - |



---

## 🔌 CClientMsg_DevPaletteVisibilityChangedEvent

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CClientMsg_DevPaletteVisibilityChangedEvent\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Visible` | `bool` | get, set | - |



---

## 🔌 CClientMsg_ListenForResponseFound

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CClientMsg_ListenForResponseFound\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlayerSlot` | `int` | get, set | - |



---

## 🔌 CClientMsg_RotateAnchor

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CClientMsg_RotateAnchor\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Angle` | `float` | get, set | - |



---

## 🔌 CClientMsg_WorldUIControllerHasPanelChangedEvent

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CClientMsg_WorldUIControllerHasPanelChangedEvent\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `HasPanel` | `bool` | get, set | - |
| `ClientEhandle` | `uint` | get, set | - |
| `LiteralHandType` | `uint` | get, set | - |



---

## 🔌 CCommunity_GamePersonalDataCategoryInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCommunity_GamePersonalDataCategoryInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Type` | `string` | get, set | - |
| `LocalizationToken` | `string` | get, set | - |
| `TemplateFile` | `string` | get, set | - |



---

## 🔌 CCommunity_GetGamePersonalDataCategories_Request

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCommunity_GetGamePersonalDataCategories_Request\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Appid` | `uint` | get, set | - |



---

## 🔌 CCommunity_GetGamePersonalDataCategories_Response

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCommunity_GetGamePersonalDataCategories_Response\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Categories` | `IProtobufRepeatedFieldSubMessageType\<CCommunity_GamePersonalDataCategoryInfo\>` | get | - |
| `AppAssetsBasename` | `string` | get, set | - |



---

## 🔌 CCommunity_GetGamePersonalDataEntries_Request

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCommunity_GetGamePersonalDataEntries_Request\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Appid` | `uint` | get, set | - |
| `Steamid` | `ulong` | get, set | - |
| `Type` | `string` | get, set | - |
| `ContinueToken` | `string` | get, set | - |



---

## 🔌 CCommunity_GetGamePersonalDataEntries_Response

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCommunity_GetGamePersonalDataEntries_Response\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Gceresult` | `uint` | get, set | - |
| `Entries` | `IProtobufRepeatedFieldValueType\<string\>` | get | - |
| `ContinueToken` | `string` | get, set | - |
| `ContinueText` | `string` | get, set | - |



---

## 🔌 CCommunity_TerminateGamePersonalDataEntries_Request

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCommunity_TerminateGamePersonalDataEntries_Request\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Appid` | `uint` | get, set | - |
| `Steamid` | `ulong` | get, set | - |



---

## 🔌 CCommunity_TerminateGamePersonalDataEntries_Response

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CCommunity_TerminateGamePersonalDataEntries_Response\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Gceresult` | `uint` | get, set | - |



---

## 🔌 CDataGCCStrike15_v2_MatchInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDataGCCStrike15_v2_MatchInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Matchid` | `ulong` | get, set | - |
| `Matchtime` | `uint` | get, set | - |
| `Watchablematchinfo` | `WatchableMatchInfo` | get | - |
| `RoundstatsLegacy` | `CMsgGCCStrike15_v2_MatchmakingServerRoundStats` | get | - |
| `Roundstatsall` | `IProtobufRepeatedFieldSubMessageType\<CMsgGCCStrike15_v2_MatchmakingServerRoundStats\>` | get | - |



---

## 🔌 CDataGCCStrike15_v2_TournamentGroup

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDataGCCStrike15_v2_TournamentGroup\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Groupid` | `uint` | get, set | - |
| `Name` | `string` | get, set | - |
| `Desc` | `string` | get, set | - |
| `PicksDeprecated` | `uint` | get, set | - |
| `Teams` | `IProtobufRepeatedFieldSubMessageType\<CDataGCCStrike15_v2_TournamentGroupTeam\>` | get | - |
| `StageIds` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `Picklockuntiltime` | `uint` | get, set | - |
| `Pickableteams` | `uint` | get, set | - |
| `PointsPerPick` | `uint` | get, set | - |
| `Picks` | `IProtobufRepeatedFieldSubMessageType\<CDataGCCStrike15_v2_TournamentGroup_Picks\>` | get | - |



---

## 🔌 CDataGCCStrike15_v2_TournamentGroupTeam

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDataGCCStrike15_v2_TournamentGroupTeam\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TeamId` | `int` | get, set | - |
| `Score` | `int` | get, set | - |
| `Correctpick` | `bool` | get, set | - |



---

## 🔌 CDataGCCStrike15_v2_TournamentGroup_Picks

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDataGCCStrike15_v2_TournamentGroup_Picks\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Pickids` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |



---

## 🔌 CDataGCCStrike15_v2_TournamentInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDataGCCStrike15_v2_TournamentInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Sections` | `IProtobufRepeatedFieldSubMessageType\<CDataGCCStrike15_v2_TournamentSection\>` | get | - |
| `TournamentEvent` | `TournamentEvent` | get | - |
| `TournamentTeams` | `IProtobufRepeatedFieldSubMessageType\<TournamentTeam\>` | get | - |



---

## 🔌 CDataGCCStrike15_v2_TournamentMatchDraft

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDataGCCStrike15_v2_TournamentMatchDraft\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EventId` | `int` | get, set | - |
| `EventStageId` | `int` | get, set | - |
| `TeamId0` | `int` | get, set | - |
| `TeamId1` | `int` | get, set | - |
| `MapsCount` | `int` | get, set | - |
| `MapsCurrent` | `int` | get, set | - |
| `TeamIdStart` | `int` | get, set | - |
| `TeamIdVeto1` | `int` | get, set | - |
| `TeamIdPickn` | `int` | get, set | - |
| `Drafts` | `IProtobufRepeatedFieldSubMessageType\<CDataGCCStrike15_v2_TournamentMatchDraft_Entry\>` | get | - |
| `VoteMapid0` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `VoteMapid1` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `VoteMapid2` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `VoteMapid3` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `VoteMapid4` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `VoteMapid5` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `VoteStartingSide` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `VotePhase` | `int` | get, set | - |
| `VotePhaseStart` | `float` | get, set | - |
| `VotePhaseLength` | `float` | get, set | - |



---

## 🔌 CDataGCCStrike15_v2_TournamentMatchDraft_Entry

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDataGCCStrike15_v2_TournamentMatchDraft_Entry\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Mapid` | `int` | get, set | - |
| `TeamIdCt` | `int` | get, set | - |



---

## 🔌 CDataGCCStrike15_v2_TournamentSection

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDataGCCStrike15_v2_TournamentSection\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Sectionid` | `uint` | get, set | - |
| `Name` | `string` | get, set | - |
| `Desc` | `string` | get, set | - |
| `Groups` | `IProtobufRepeatedFieldSubMessageType\<CDataGCCStrike15_v2_TournamentGroup\>` | get | - |



---

## 🔌 CDemoAnimationData

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDemoAnimationData\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityId` | `int` | get, set | - |
| `StartTick` | `int` | get, set | - |
| `EndTick` | `int` | get, set | - |
| `Data` | `byte[]` | get, set | - |
| `DataChecksum` | `long` | get, set | - |



---

## 🔌 CDemoAnimationHeader

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDemoAnimationHeader\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityId` | `int` | get, set | - |
| `Tick` | `int` | get, set | - |
| `Data` | `byte[]` | get, set | - |



---

## 🔌 CDemoClassInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDemoClassInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Classes` | `IProtobufRepeatedFieldSubMessageType\<CDemoClassInfo_class_t\>` | get | - |



---

## 🔌 CDemoClassInfo_class_t

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDemoClassInfo_class_t\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ClassId` | `int` | get, set | - |
| `NetworkName` | `string` | get, set | - |
| `TableName` | `string` | get, set | - |



---

## 🔌 CDemoConsoleCmd

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDemoConsoleCmd\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Cmdstring` | `string` | get, set | - |



---

## 🔌 CDemoCustomData

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDemoCustomData\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CallbackIndex` | `int` | get, set | - |
| `Data` | `byte[]` | get, set | - |



---

## 🔌 CDemoCustomDataCallbacks

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDemoCustomDataCallbacks\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SaveId` | `IProtobufRepeatedFieldValueType\<string\>` | get | - |



---

## 🔌 CDemoFileHeader

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDemoFileHeader\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `DemoFileStamp` | `string` | get, set | - |
| `PatchVersion` | `int` | get, set | - |
| `ServerName` | `string` | get, set | - |
| `ClientName` | `string` | get, set | - |
| `MapName` | `string` | get, set | - |
| `GameDirectory` | `string` | get, set | - |
| `FullpacketsVersion` | `int` | get, set | - |
| `AllowClientsideEntities` | `bool` | get, set | - |
| `AllowClientsideParticles` | `bool` | get, set | - |
| `Addons` | `string` | get, set | - |
| `DemoVersionName` | `string` | get, set | - |
| `DemoVersionGuid` | `string` | get, set | - |
| `BuildNum` | `int` | get, set | - |
| `Game` | `string` | get, set | - |
| `ServerStartTick` | `int` | get, set | - |



---

## 🔌 CDemoFileInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDemoFileInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlaybackTime` | `float` | get, set | - |
| `PlaybackTicks` | `int` | get, set | - |
| `PlaybackFrames` | `int` | get, set | - |
| `GameInfo` | `CGameInfo` | get | - |



---

## 🔌 CDemoFullPacket

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDemoFullPacket\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `StringTable` | `CDemoStringTables` | get | - |
| `Packet` | `CDemoPacket` | get | - |



---

## 🔌 CDemoPacket

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDemoPacket\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Data` | `byte[]` | get, set | - |



---

## 🔌 CDemoRecovery

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDemoRecovery\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `InitialSpawnGroup` | `CDemoRecovery_DemoInitialSpawnGroupEntry` | get | - |
| `SpawnGroupMessage` | `byte[]` | get, set | - |



---

## 🔌 CDemoRecovery_DemoInitialSpawnGroupEntry

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDemoRecovery_DemoInitialSpawnGroupEntry\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Spawngrouphandle` | `uint` | get, set | - |
| `WasCreated` | `bool` | get, set | - |



---

## 🔌 CDemoSaveGame

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDemoSaveGame\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Data` | `byte[]` | get, set | - |
| `SteamId` | `ulong` | get, set | - |
| `Signature` | `ulong` | get, set | - |
| `Version` | `int` | get, set | - |



---

## 🔌 CDemoSendTables

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDemoSendTables\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Data` | `byte[]` | get, set | - |



---

## 🔌 CDemoSpawnGroups

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDemoSpawnGroups\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Msgs` | `IProtobufRepeatedFieldValueType\<byte[]\>` | get | - |



---

## 🔌 CDemoSpawnGroupsHLTVBroadcast

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDemoSpawnGroupsHLTVBroadcast\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Data` | `byte[]` | get, set | - |



---

## 🔌 CDemoStop

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDemoStop\>`



---

## 🔌 CDemoStringTables

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDemoStringTables\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Tables` | `IProtobufRepeatedFieldSubMessageType\<CDemoStringTables_table_t\>` | get | - |



---

## 🔌 CDemoStringTables_items_t

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDemoStringTables_items_t\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Str` | `string` | get, set | - |
| `Data` | `byte[]` | get, set | - |



---

## 🔌 CDemoStringTables_table_t

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDemoStringTables_table_t\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TableName` | `string` | get, set | - |
| `Items` | `IProtobufRepeatedFieldSubMessageType\<CDemoStringTables_items_t\>` | get | - |
| `ItemsClientside` | `IProtobufRepeatedFieldSubMessageType\<CDemoStringTables_items_t\>` | get | - |
| `TableFlags` | `int` | get, set | - |



---

## 🔌 CDemoSyncTick

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDemoSyncTick\>`



---

## 🔌 CDemoUserCmd

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CDemoUserCmd\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CmdNumber` | `int` | get, set | - |
| `Data` | `byte[]` | get, set | - |



---

## 🔌 CEconItemPreviewDataBlock

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CEconItemPreviewDataBlock\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Accountid` | `uint` | get, set | - |
| `Itemid` | `ulong` | get, set | - |
| `Defindex` | `uint` | get, set | - |
| `Paintindex` | `uint` | get, set | - |
| `Rarity` | `uint` | get, set | - |
| `Quality` | `uint` | get, set | - |
| `Paintwear` | `uint` | get, set | - |
| `Paintseed` | `uint` | get, set | - |
| `Killeaterscoretype` | `uint` | get, set | - |
| `Killeatervalue` | `uint` | get, set | - |
| `Customname` | `string` | get, set | - |
| `Stickers` | `IProtobufRepeatedFieldSubMessageType\<CEconItemPreviewDataBlock_Sticker\>` | get | - |
| `Inventory` | `uint` | get, set | - |
| `Origin` | `uint` | get, set | - |
| `Questid` | `uint` | get, set | - |
| `Dropreason` | `uint` | get, set | - |
| `Musicindex` | `uint` | get, set | - |
| `Entindex` | `int` | get, set | - |
| `Petindex` | `uint` | get, set | - |
| `Keychains` | `IProtobufRepeatedFieldSubMessageType\<CEconItemPreviewDataBlock_Sticker\>` | get | - |
| `Style` | `uint` | get, set | - |
| `Variations` | `IProtobufRepeatedFieldSubMessageType\<CEconItemPreviewDataBlock_Sticker\>` | get | - |
| `UpgradeLevel` | `uint` | get, set | - |



---

## 🔌 CEconItemPreviewDataBlock_Sticker

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CEconItemPreviewDataBlock_Sticker\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Slot` | `uint` | get, set | - |
| `StickerId` | `uint` | get, set | - |
| `Wear` | `float` | get, set | - |
| `Scale` | `float` | get, set | - |
| `Rotation` | `float` | get, set | - |
| `TintId` | `uint` | get, set | - |
| `OffsetX` | `float` | get, set | - |
| `OffsetY` | `float` | get, set | - |
| `OffsetZ` | `float` | get, set | - |
| `Pattern` | `uint` | get, set | - |
| `HighlightReel` | `uint` | get, set | - |
| `WrappedSticker` | `uint` | get, set | - |



---

## 🔌 CEngineGotvSyncPacket

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CEngineGotvSyncPacket\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MatchId` | `ulong` | get, set | - |
| `InstanceId` | `uint` | get, set | - |
| `Signupfragment` | `uint` | get, set | - |
| `Currentfragment` | `uint` | get, set | - |
| `Tickrate` | `float` | get, set | - |
| `Tick` | `uint` | get, set | - |
| `Rtdelay` | `float` | get, set | - |
| `Rcvage` | `float` | get, set | - |
| `KeyframeInterval` | `float` | get, set | - |
| `Cdndelay` | `uint` | get, set | - |



---

## 🔌 CEntityMessageDoSpark

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CEntityMessageDoSpark\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Origin` | `Vector` | get, set | - |
| `Entityindex` | `int` | get, set | - |
| `Radius` | `float` | get, set | - |
| `Color` | `uint` | get, set | - |
| `Beams` | `uint` | get, set | - |
| `Thick` | `float` | get, set | - |
| `Duration` | `float` | get, set | - |
| `EntityMsg` | `CEntityMsg` | get | - |



---

## 🔌 CEntityMessageFixAngle

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CEntityMessageFixAngle\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Relative` | `bool` | get, set | - |
| `Angle` | `QAngle` | get, set | - |
| `EntityMsg` | `CEntityMsg` | get | - |



---

## 🔌 CEntityMessagePlayJingle

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CEntityMessagePlayJingle\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityMsg` | `CEntityMsg` | get | - |



---

## 🔌 CEntityMessagePropagateForce

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CEntityMessagePropagateForce\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Impulse` | `Vector` | get, set | - |
| `EntityMsg` | `CEntityMsg` | get | - |



---

## 🔌 CEntityMessageRemoveAllDecals

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CEntityMessageRemoveAllDecals\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `RemoveDecals` | `bool` | get, set | - |
| `EntityMsg` | `CEntityMsg` | get | - |



---

## 🔌 CEntityMessageScreenOverlay

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CEntityMessageScreenOverlay\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `StartEffect` | `bool` | get, set | - |
| `EntityMsg` | `CEntityMsg` | get | - |



---

## 🔌 CEntityMsg

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CEntityMsg\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TargetEntity` | `uint` | get, set | - |



---

## 🔌 CGCStorePurchaseInit_LineItem

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CGCStorePurchaseInit_LineItem\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ItemDefId` | `uint` | get, set | - |
| `Quantity` | `uint` | get, set | - |
| `CostInLocalCurrency` | `ulong` | get, set | - |
| `PurchaseType` | `uint` | get, set | - |
| `SupplementalData` | `ulong` | get, set | - |



---

## 🔌 CGCToGCMsgMasterAck

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CGCToGCMsgMasterAck\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `DirIndex` | `uint` | get, set | - |
| `GcType` | `uint` | get, set | - |



---

## 🔌 CGCToGCMsgMasterAck_Response

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CGCToGCMsgMasterAck_Response\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Eresult` | `int` | get, set | - |



---

## 🔌 CGCToGCMsgMasterStartupComplete

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CGCToGCMsgMasterStartupComplete\>`



---

## 🔌 CGCToGCMsgRouted

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CGCToGCMsgRouted\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MsgType` | `uint` | get, set | - |
| `SenderId` | `ulong` | get, set | - |
| `NetMessage` | `byte[]` | get, set | - |
| `Ip` | `uint` | get, set | - |



---

## 🔌 CGCToGCMsgRoutedReply

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CGCToGCMsgRoutedReply\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MsgType` | `uint` | get, set | - |
| `NetMessage` | `byte[]` | get, set | - |



---

## 🔌 CGameInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CGameInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Dota` | `CGameInfo_CDotaGameInfo` | get | - |
| `Cs` | `CGameInfo_CCSGameInfo` | get | - |



---

## 🔌 CGameInfo_CCSGameInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CGameInfo_CCSGameInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `RoundStartTicks` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |



---

## 🔌 CGameInfo_CDotaGameInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CGameInfo_CDotaGameInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MatchId` | `ulong` | get, set | - |
| `GameMode` | `int` | get, set | - |
| `GameWinner` | `int` | get, set | - |
| `PlayerInfo` | `IProtobufRepeatedFieldSubMessageType\<CGameInfo_CDotaGameInfo_CPlayerInfo\>` | get | - |
| `Leagueid` | `uint` | get, set | - |
| `PicksBans` | `IProtobufRepeatedFieldSubMessageType\<CGameInfo_CDotaGameInfo_CHeroSelectEvent\>` | get | - |
| `RadiantTeamId` | `uint` | get, set | - |
| `DireTeamId` | `uint` | get, set | - |
| `RadiantTeamTag` | `string` | get, set | - |
| `DireTeamTag` | `string` | get, set | - |
| `EndTime` | `uint` | get, set | - |



---

## 🔌 CGameInfo_CDotaGameInfo_CHeroSelectEvent

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CGameInfo_CDotaGameInfo_CHeroSelectEvent\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `IsPick` | `bool` | get, set | - |
| `Team` | `uint` | get, set | - |
| `HeroId` | `int` | get, set | - |



---

## 🔌 CGameInfo_CDotaGameInfo_CPlayerInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CGameInfo_CDotaGameInfo_CPlayerInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `HeroName` | `string` | get, set | - |
| `PlayerName` | `string` | get, set | - |
| `IsFakeClient` | `bool` | get, set | - |
| `Steamid` | `ulong` | get, set | - |
| `GameTeam` | `int` | get, set | - |



---

## 🔌 CGameServers_AggregationQuery_Request

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CGameServers_AggregationQuery_Request\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Filter` | `string` | get, set | - |
| `GroupFields` | `IProtobufRepeatedFieldValueType\<string\>` | get | - |



---

## 🔌 CGameServers_AggregationQuery_Response

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CGameServers_AggregationQuery_Response\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Groups` | `IProtobufRepeatedFieldSubMessageType\<CGameServers_AggregationQuery_Response_Group\>` | get | - |



---

## 🔌 CGameServers_AggregationQuery_Response_Group

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CGameServers_AggregationQuery_Response_Group\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `GroupValues` | `IProtobufRepeatedFieldValueType\<string\>` | get | - |
| `ServersEmpty` | `uint` | get, set | - |
| `ServersFull` | `uint` | get, set | - |
| `ServersTotal` | `uint` | get, set | - |
| `PlayersHumans` | `uint` | get, set | - |
| `PlayersBots` | `uint` | get, set | - |
| `PlayerCapacity` | `uint` | get, set | - |



---

## 🔌 CInButtonStatePB

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CInButtonStatePB\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Buttonstate1` | `ulong` | get, set | - |
| `Buttonstate2` | `ulong` | get, set | - |
| `Buttonstate3` | `ulong` | get, set | - |



---

## 📋 CLC_Messages

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `clc_ClientInfo` | `20` | - |
| `clc_Move` | `21` | - |
| `clc_VoiceData` | `22` | - |
| `clc_BaselineAck` | `23` | - |
| `clc_RespondCvarValue` | `25` | - |
| `clc_LoadingProgress` | `27` | - |
| `clc_SplitPlayerConnect` | `28` | - |
| `clc_SplitPlayerDisconnect` | `30` | - |
| `clc_ServerStatus` | `31` | - |
| `clc_RequestPause` | `33` | - |
| `clc_CmdKeyValues` | `34` | - |
| `clc_RconServerDetails` | `35` | - |
| `clc_HltvReplay` | `36` | - |
| `clc_Diagnostic` | `37` | - |



---

## 🔌 CMsgAccountDetails

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgAccountDetails\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Valid` | `bool` | get, set | - |
| `AccountName` | `string` | get, set | - |
| `PublicProfile` | `bool` | get, set | - |
| `PublicInventory` | `bool` | get, set | - |
| `VacBanned` | `bool` | get, set | - |
| `CyberCafe` | `bool` | get, set | - |
| `SchoolAccount` | `bool` | get, set | - |
| `FreeTrialAccount` | `bool` | get, set | - |
| `Subscribed` | `bool` | get, set | - |
| `LowViolence` | `bool` | get, set | - |
| `Limited` | `bool` | get, set | - |
| `Trusted` | `bool` | get, set | - |
| `Package` | `uint` | get, set | - |
| `TimeCached` | `uint` | get, set | - |
| `AccountLocked` | `bool` | get, set | - |
| `CommunityBanned` | `bool` | get, set | - |
| `TradeBanned` | `bool` | get, set | - |
| `EligibleForCommunityMarket` | `bool` | get, set | - |



---

## 🔌 CMsgAcknowledgeRentalExpiration

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgAcknowledgeRentalExpiration\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CrateItemId` | `ulong` | get, set | - |



---

## 🔌 CMsgAdjustEquipSlot

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgAdjustEquipSlot\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ClassId` | `uint` | get, set | - |
| `SlotId` | `uint` | get, set | - |
| `ItemId` | `ulong` | get, set | - |



---

## 🔌 CMsgAdjustEquipSlots

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgAdjustEquipSlots\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Slots` | `IProtobufRepeatedFieldSubMessageType\<CMsgAdjustEquipSlot\>` | get | - |
| `ChangeNum` | `uint` | get, set | - |



---

## 🔌 CMsgApplyEggEssence

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgApplyEggEssence\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EssenceItemId` | `ulong` | get, set | - |
| `EggItemId` | `ulong` | get, set | - |



---

## 🔌 CMsgApplyPennantUpgrade

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgApplyPennantUpgrade\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UpgradeItemId` | `ulong` | get, set | - |
| `PennantItemId` | `ulong` | get, set | - |



---

## 🔌 CMsgApplyStatTrakSwap

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgApplyStatTrakSwap\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ToolItemId` | `ulong` | get, set | - |
| `Item1ItemId` | `ulong` | get, set | - |
| `Item2ItemId` | `ulong` | get, set | - |



---

## 🔌 CMsgApplySticker

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgApplySticker\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `StickerItemId` | `ulong` | get, set | - |
| `ItemItemId` | `ulong` | get, set | - |
| `StickerSlot` | `uint` | get, set | - |
| `BaseitemDefidx` | `uint` | get, set | - |
| `StickerWear` | `float` | get, set | - |
| `StickerRotation` | `float` | get, set | - |
| `StickerScale` | `float` | get, set | - |
| `StickerOffsetX` | `float` | get, set | - |
| `StickerOffsetY` | `float` | get, set | - |
| `StickerOffsetZ` | `float` | get, set | - |
| `StickerWearTarget` | `float` | get, set | - |



---

## 🔌 CMsgApplyStrangePart

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgApplyStrangePart\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `StrangePartItemId` | `ulong` | get, set | - |
| `ItemItemId` | `ulong` | get, set | - |



---

## 🔌 CMsgCStrike15Welcome

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgCStrike15Welcome\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `StoreItemHash` | `uint` | get, set | - |
| `Timeplayedconsecutively` | `uint` | get, set | - |
| `TimeFirstPlayed` | `uint` | get, set | - |
| `LastTimePlayed` | `uint` | get, set | - |
| `LastIpAddress` | `uint` | get, set | - |
| `Gscookieid` | `ulong` | get, set | - |
| `Uniqueid` | `ulong` | get, set | - |



---

## 🔌 CMsgCasketItem

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgCasketItem\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CasketItemId` | `ulong` | get, set | - |
| `ItemItemId` | `ulong` | get, set | - |



---

## 🔌 CMsgClearDecalsForEntityEvent

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgClearDecalsForEntityEvent\>`

**实现接口:** `INetMessage\<CMsgClearDecalsForEntityEvent\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Flagstoclear` | `uint` | get, set | - |
| `Entityhandle` | `uint` | get, set | - |



---

## 🔌 CMsgClearEntityDecalsEvent

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgClearEntityDecalsEvent\>`

**实现接口:** `INetMessage\<CMsgClearEntityDecalsEvent\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Flagstoclear` | `uint` | get, set | - |



---

## 🔌 CMsgClearWorldDecalsEvent

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgClearWorldDecalsEvent\>`

**实现接口:** `INetMessage\<CMsgClearWorldDecalsEvent\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Flagstoclear` | `uint` | get, set | - |



---

## 🔌 CMsgClientHello

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgClientHello\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Version` | `uint` | get, set | - |
| `SocacheHaveVersions` | `IProtobufRepeatedFieldSubMessageType\<CMsgSOCacheHaveVersion\>` | get | - |
| `ClientSessionNeed` | `uint` | get, set | - |
| `ClientLauncher` | `uint` | get, set | - |
| `PartnerSrcid` | `uint` | get, set | - |
| `PartnerAccountid` | `uint` | get, set | - |
| `PartnerAccountflags` | `uint` | get, set | - |
| `PartnerAccountbalance` | `uint` | get, set | - |
| `SteamLauncher` | `uint` | get, set | - |



---

## 🔌 CMsgClientWelcome

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgClientWelcome\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Version` | `uint` | get, set | - |
| `GameData` | `byte[]` | get, set | - |
| `OutofdateSubscribedCaches` | `IProtobufRepeatedFieldSubMessageType\<CMsgSOCacheSubscribed\>` | get | - |
| `UptodateSubscribedCaches` | `IProtobufRepeatedFieldSubMessageType\<CMsgSOCacheSubscriptionCheck\>` | get | - |
| `Location` | `CMsgClientWelcome_Location` | get | - |
| `GameData2` | `byte[]` | get, set | - |
| `Rtime32GcWelcomeTimestamp` | `uint` | get, set | - |
| `Currency` | `uint` | get, set | - |
| `Balance` | `uint` | get, set | - |
| `BalanceUrl` | `string` | get, set | - |
| `TxnCountryCode` | `string` | get, set | - |



---

## 🔌 CMsgClientWelcome_Location

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgClientWelcome_Location\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Latitude` | `float` | get, set | - |
| `Longitude` | `float` | get, set | - |
| `Country` | `string` | get, set | - |



---

## 🔌 CMsgConVarValue

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgConVarValue\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | get, set | - |
| `Value` | `string` | get, set | - |



---

## 🔌 CMsgConnectionStatus

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgConnectionStatus\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Status` | `GCConnectionStatus` | get, set | - |
| `ClientSessionNeed` | `uint` | get, set | - |
| `QueuePosition` | `int` | get, set | - |
| `QueueSize` | `int` | get, set | - |
| `WaitSeconds` | `int` | get, set | - |
| `EstimatedWaitSecondsRemaining` | `int` | get, set | - |



---

## 🔌 CMsgConsumableExhausted

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgConsumableExhausted\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ItemDefId` | `int` | get, set | - |



---

## 🔌 CMsgCsgoSteamUserStatChange

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgCsgoSteamUserStatChange\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Ecsgosteamuserstat` | `int` | get, set | - |
| `Delta` | `int` | get, set | - |
| `Absolute` | `bool` | get, set | - |



---

## 🔌 CMsgDevNewItemRequest

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgDevNewItemRequest\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Receiver` | `ulong` | get, set | - |
| `Criteria` | `CSOItemCriteria` | get | - |



---

## 🔌 CMsgEffectData

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgEffectData\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Origin` | `Vector` | get, set | - |
| `Start` | `Vector` | get, set | - |
| `Normal` | `Vector` | get, set | - |
| `Angles` | `QAngle` | get, set | - |
| `Entity` | `uint` | get, set | - |
| `Otherentity` | `uint` | get, set | - |
| `Scale` | `float` | get, set | - |
| `Magnitude` | `float` | get, set | - |
| `Radius` | `float` | get, set | - |
| `Surfaceprop` | `uint` | get, set | - |
| `Effectindex` | `ulong` | get, set | - |
| `Damagetype` | `uint` | get, set | - |
| `Material` | `uint` | get, set | - |
| `Hitbox` | `uint` | get, set | - |
| `Color` | `uint` | get, set | - |
| `Flags` | `uint` | get, set | - |
| `Attachmentindex` | `int` | get, set | - |
| `Effectname` | `uint` | get, set | - |
| `Attachmentname` | `uint` | get, set | - |



---

## 🔌 CMsgGCBannedWord

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCBannedWord\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `WordId` | `uint` | get, set | - |
| `WordType` | `GC_BannedWordType` | get, set | - |
| `Word` | `string` | get, set | - |



---

## 🔌 CMsgGCBannedWordListRequest

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCBannedWordListRequest\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `BanListGroupId` | `uint` | get, set | - |
| `WordId` | `uint` | get, set | - |



---

## 🔌 CMsgGCBannedWordListResponse

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCBannedWordListResponse\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `BanListGroupId` | `uint` | get, set | - |
| `WordList` | `IProtobufRepeatedFieldSubMessageType\<CMsgGCBannedWord\>` | get | - |



---

## 🔌 CMsgGCCStrike15_ClientDeepStats

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_ClientDeepStats\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AccountId` | `uint` | get, set | - |
| `Range` | `CMsgGCCStrike15_ClientDeepStats_DeepStatsRange` | get | - |
| `Matches` | `IProtobufRepeatedFieldSubMessageType\<CMsgGCCStrike15_ClientDeepStats_DeepStatsMatch\>` | get | - |



---

## 🔌 CMsgGCCStrike15_ClientDeepStats_DeepStatsMatch

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_ClientDeepStats_DeepStatsMatch\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Player` | `DeepPlayerStatsEntry` | get | - |
| `Events` | `IProtobufRepeatedFieldSubMessageType\<DeepPlayerMatchEvent\>` | get | - |



---

## 🔌 CMsgGCCStrike15_ClientDeepStats_DeepStatsRange

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_ClientDeepStats_DeepStatsRange\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Begin` | `uint` | get, set | - |
| `End` | `uint` | get, set | - |
| `Frozen` | `bool` | get, set | - |



---

## 🔌 CMsgGCCStrike15_GotvSyncPacket

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_GotvSyncPacket\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Data` | `CEngineGotvSyncPacket` | get | - |



---

## 🔌 CMsgGCCStrike15_v2_AccountPrivacySettings

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_AccountPrivacySettings\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Settings` | `IProtobufRepeatedFieldSubMessageType\<CMsgGCCStrike15_v2_AccountPrivacySettings_Setting\>` | get | - |



---

## 🔌 CMsgGCCStrike15_v2_AccountPrivacySettings_Setting

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_AccountPrivacySettings_Setting\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SettingType` | `uint` | get, set | - |
| `SettingValue` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_Account_RequestCoPlays

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_Account_RequestCoPlays\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Players` | `IProtobufRepeatedFieldSubMessageType\<CMsgGCCStrike15_v2_Account_RequestCoPlays_Player\>` | get | - |
| `Servertime` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_Account_RequestCoPlays_Player

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_Account_RequestCoPlays_Player\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Accountid` | `uint` | get, set | - |
| `Rtcoplay` | `uint` | get, set | - |
| `Online` | `bool` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_AcknowledgePenalty

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_AcknowledgePenalty\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Acknowledged` | `int` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_BetaEnrollment

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_BetaEnrollment\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Eresult` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_Client2GCEconPreviewDataBlockRequest

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_Client2GCEconPreviewDataBlockRequest\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ParamS` | `ulong` | get, set | - |
| `ParamA` | `ulong` | get, set | - |
| `ParamD` | `ulong` | get, set | - |
| `ParamM` | `ulong` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_Client2GCEconPreviewDataBlockResponse

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_Client2GCEconPreviewDataBlockResponse\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Iteminfo` | `CEconItemPreviewDataBlock` | get | - |



---

## 🔌 CMsgGCCStrike15_v2_Client2GCRequestPrestigeCoin

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_Client2GCRequestPrestigeCoin\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Defindex` | `uint` | get, set | - |
| `Upgradeid` | `ulong` | get, set | - |
| `Hours` | `uint` | get, set | - |
| `Prestigetime` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_Client2GCStreamUnlock

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_Client2GCStreamUnlock\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Ticket` | `ulong` | get, set | - |
| `Os` | `int` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_Client2GCTextMsg

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_Client2GCTextMsg\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Id` | `uint` | get, set | - |
| `Args` | `IProtobufRepeatedFieldValueType\<byte[]\>` | get | - |



---

## 🔌 CMsgGCCStrike15_v2_Client2GcAckXPShopTracks

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_Client2GcAckXPShopTracks\>`



---

## 🔌 CMsgGCCStrike15_v2_ClientAccountBalance

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientAccountBalance\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Amount` | `ulong` | get, set | - |
| `Url` | `string` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_ClientAuthKeyCode

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientAuthKeyCode\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Eventid` | `uint` | get, set | - |
| `Code` | `string` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_ClientCommendPlayer

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientCommendPlayer\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AccountId` | `uint` | get, set | - |
| `MatchId` | `ulong` | get, set | - |
| `Commendation` | `PlayerCommendationInfo` | get | - |
| `Tokens` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_ClientGCRankUpdate

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientGCRankUpdate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Rankings` | `IProtobufRepeatedFieldSubMessageType\<PlayerRankingInfo\>` | get | - |



---

## 🔌 CMsgGCCStrike15_v2_ClientLogonFatalError

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientLogonFatalError\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Errorcode` | `uint` | get, set | - |
| `Message` | `string` | get, set | - |
| `Country` | `string` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_ClientNetworkConfig

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientNetworkConfig\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Data` | `byte[]` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_ClientPartyJoinRelay

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientPartyJoinRelay\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Accountid` | `uint` | get, set | - |
| `Lobbyid` | `ulong` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_ClientPartyWarning

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientPartyWarning\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Entries` | `IProtobufRepeatedFieldSubMessageType\<CMsgGCCStrike15_v2_ClientPartyWarning_Entry\>` | get | - |



---

## 🔌 CMsgGCCStrike15_v2_ClientPartyWarning_Entry

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientPartyWarning_Entry\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Accountid` | `uint` | get, set | - |
| `Warntype` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_ClientPerfReport

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientPerfReport\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Entries` | `IProtobufRepeatedFieldSubMessageType\<CMsgGCCStrike15_v2_ClientPerfReport_Entry\>` | get | - |



---

## 🔌 CMsgGCCStrike15_v2_ClientPerfReport_Entry

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientPerfReport_Entry\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Perfcounter` | `uint` | get, set | - |
| `Length` | `uint` | get, set | - |
| `Reference` | `byte[]` | get, set | - |
| `Actual` | `byte[]` | get, set | - |
| `Sourceid` | `uint` | get, set | - |
| `Status` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_ClientPlayerDecalSign

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientPlayerDecalSign\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Data` | `PlayerDecalDigitalSignature` | get | - |
| `Itemid` | `ulong` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_ClientPollState

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientPollState\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Pollid` | `uint` | get, set | - |
| `Names` | `IProtobufRepeatedFieldValueType\<string\>` | get | - |
| `Values` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |



---

## 🔌 CMsgGCCStrike15_v2_ClientReportPlayer

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientReportPlayer\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AccountId` | `uint` | get, set | - |
| `RptAimbot` | `uint` | get, set | - |
| `RptWallhack` | `uint` | get, set | - |
| `RptSpeedhack` | `uint` | get, set | - |
| `RptTeamharm` | `uint` | get, set | - |
| `RptTextabuse` | `uint` | get, set | - |
| `RptVoiceabuse` | `uint` | get, set | - |
| `MatchId` | `ulong` | get, set | - |
| `ReportFromDemo` | `bool` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_ClientReportResponse

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientReportResponse\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ConfirmationId` | `ulong` | get, set | - |
| `AccountId` | `uint` | get, set | - |
| `ServerIp` | `uint` | get, set | - |
| `ResponseType` | `uint` | get, set | - |
| `ResponseResult` | `uint` | get, set | - |
| `Tokens` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_ClientReportServer

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientReportServer\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `RptPoorperf` | `uint` | get, set | - |
| `RptAbusivemodels` | `uint` | get, set | - |
| `RptBadmotd` | `uint` | get, set | - |
| `RptListingabuse` | `uint` | get, set | - |
| `RptInventoryabuse` | `uint` | get, set | - |
| `MatchId` | `ulong` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_ClientReportValidation

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientReportValidation\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `FileReport` | `string` | get, set | - |
| `CommandLine` | `string` | get, set | - |
| `TotalFiles` | `uint` | get, set | - |
| `InternalError` | `uint` | get, set | - |
| `TrustTime` | `uint` | get, set | - |
| `CountPending` | `uint` | get, set | - |
| `CountCompleted` | `uint` | get, set | - |
| `ProcessId` | `uint` | get, set | - |
| `Osversion` | `int` | get, set | - |
| `Clientreportversion` | `uint` | get, set | - |
| `StatusId` | `uint` | get, set | - |
| `Diagnostic1` | `uint` | get, set | - |
| `Diagnostic2` | `ulong` | get, set | - |
| `Diagnostic3` | `ulong` | get, set | - |
| `LastLaunchData` | `string` | get, set | - |
| `ReportCount` | `uint` | get, set | - |
| `ClientTime` | `ulong` | get, set | - |
| `Diagnostic4` | `ulong` | get, set | - |
| `Diagnostic5` | `ulong` | get, set | - |
| `Diagnostics` | `IProtobufRepeatedFieldSubMessageType\<CVDiagnostic\>` | get | - |



---

## 🔌 CMsgGCCStrike15_v2_ClientRequestJoinFriendData

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientRequestJoinFriendData\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Version` | `uint` | get, set | - |
| `AccountId` | `uint` | get, set | - |
| `JoinToken` | `uint` | get, set | - |
| `JoinIpp` | `uint` | get, set | - |
| `Res` | `CMsgGCCStrike15_v2_MatchmakingGC2ClientReserve` | get | - |
| `Errormsg` | `string` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_ClientRequestJoinServerData

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientRequestJoinServerData\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Version` | `uint` | get, set | - |
| `AccountId` | `uint` | get, set | - |
| `Serverid` | `ulong` | get, set | - |
| `ServerIp` | `uint` | get, set | - |
| `ServerPort` | `uint` | get, set | - |
| `Res` | `CMsgGCCStrike15_v2_MatchmakingGC2ClientReserve` | get | - |
| `Errormsg` | `string` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_ClientRequestOffers

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientRequestOffers\>`



---

## 🔌 CMsgGCCStrike15_v2_ClientRequestPlayersProfile

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientRequestPlayersProfile\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `RequestIdDeprecated` | `uint` | get, set | - |
| `AccountIdsDeprecated` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `AccountId` | `uint` | get, set | - |
| `RequestLevel` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_ClientRequestSouvenir

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientRequestSouvenir\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Itemid` | `ulong` | get, set | - |
| `Matchid` | `ulong` | get, set | - |
| `Eventid` | `int` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_ClientRequestWatchInfoFriends

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientRequestWatchInfoFriends\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `RequestId` | `uint` | get, set | - |
| `AccountIds` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `Serverid` | `ulong` | get, set | - |
| `Matchid` | `ulong` | get, set | - |
| `ClientLauncher` | `uint` | get, set | - |
| `DataCenterPings` | `IProtobufRepeatedFieldSubMessageType\<DataCenterPing\>` | get | - |



---

## 🔌 CMsgGCCStrike15_v2_ClientSubmitSurveyVote

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientSubmitSurveyVote\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SurveyId` | `uint` | get, set | - |
| `Vote` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_ClientToGCChat

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientToGCChat\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MatchId` | `ulong` | get, set | - |
| `Text` | `string` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_ClientToGCRequestElevate

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientToGCRequestElevate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Stage` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_ClientToGCRequestTicket

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientToGCRequestTicket\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AuthorizedSteamId` | `ulong` | get, set | - |
| `AuthorizedPublicIp` | `uint` | get, set | - |
| `GameserverSteamId` | `ulong` | get, set | - |
| `GameserverSdrRouting` | `string` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_ClientVarValueNotificationInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ClientVarValueNotificationInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ValueName` | `string` | get, set | - |
| `ValueInt` | `int` | get, set | - |
| `ServerAddr` | `uint` | get, set | - |
| `ServerPort` | `uint` | get, set | - |
| `ChokedBlocks` | `IProtobufRepeatedFieldValueType\<string\>` | get | - |



---

## 🔌 CMsgGCCStrike15_v2_Fantasy

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_Fantasy\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EventId` | `uint` | get, set | - |
| `Teams` | `IProtobufRepeatedFieldSubMessageType\<CMsgGCCStrike15_v2_Fantasy_FantasyTeam\>` | get | - |



---

## 🔌 CMsgGCCStrike15_v2_Fantasy_FantasySlot

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_Fantasy_FantasySlot\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Type` | `int` | get, set | - |
| `Pick` | `int` | get, set | - |
| `Itemid` | `ulong` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_Fantasy_FantasyTeam

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_Fantasy_FantasyTeam\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Sectionid` | `int` | get, set | - |
| `Slots` | `IProtobufRepeatedFieldSubMessageType\<CMsgGCCStrike15_v2_Fantasy_FantasySlot\>` | get | - |



---

## 🔌 CMsgGCCStrike15_v2_GC2ClientInitSystem

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_GC2ClientInitSystem\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Load` | `bool` | get, set | - |
| `Name` | `string` | get, set | - |
| `Outputname` | `string` | get, set | - |
| `KeyData` | `byte[]` | get, set | - |
| `ShaHash` | `byte[]` | get, set | - |
| `Cookie` | `int` | get, set | - |
| `Manifest` | `string` | get, set | - |
| `SystemPackage` | `byte[]` | get, set | - |
| `LoadSystem` | `bool` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_GC2ClientInitSystem_Response

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_GC2ClientInitSystem_Response\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Success` | `bool` | get, set | - |
| `Diagnostic` | `string` | get, set | - |
| `ShaHash` | `byte[]` | get, set | - |
| `Response` | `int` | get, set | - |
| `ErrorCode1` | `int` | get, set | - |
| `ErrorCode2` | `int` | get, set | - |
| `Handle` | `long` | get, set | - |
| `EinitResult` | `EInitSystemResult` | get, set | - |
| `AuxSystem1` | `int` | get, set | - |
| `AuxSystem2` | `int` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_GC2ClientNotifyXPShop

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_GC2ClientNotifyXPShop\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Prematch` | `CSOAccountXpShop` | get | - |
| `Postmatch` | `CSOAccountXpShop` | get | - |
| `CurrentXp` | `uint` | get, set | - |
| `CurrentLevel` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_GC2ClientRefuseSecureMode

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_GC2ClientRefuseSecureMode\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `FileReport` | `string` | get, set | - |
| `OfferInsecureMode` | `bool` | get, set | - |
| `OfferSecureMode` | `bool` | get, set | - |
| `ShowUnsignedUi` | `bool` | get, set | - |
| `KickUser` | `bool` | get, set | - |
| `ShowTrustedUi` | `bool` | get, set | - |
| `ShowWarningNotTrusted` | `bool` | get, set | - |
| `ShowWarningNotTrusted2` | `bool` | get, set | - |
| `FilesPreventedTrusted` | `string` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_GC2ClientRequestValidation

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_GC2ClientRequestValidation\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `FullReport` | `bool` | get, set | - |
| `Module` | `string` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_GC2ClientTextMsg

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_GC2ClientTextMsg\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Id` | `uint` | get, set | - |
| `Type` | `uint` | get, set | - |
| `Payload` | `byte[]` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_GC2ClientTournamentInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_GC2ClientTournamentInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Eventid` | `uint` | get, set | - |
| `Stageid` | `uint` | get, set | - |
| `GameType` | `uint` | get, set | - |
| `Teamids` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |



---

## 🔌 CMsgGCCStrike15_v2_GC2ServerReservationUpdate

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_GC2ServerReservationUpdate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ViewersExternalTotal` | `uint` | get, set | - |
| `ViewersExternalSteam` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_GCToClientChat

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_GCToClientChat\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AccountId` | `uint` | get, set | - |
| `Text` | `string` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_GetEventFavorites_Request

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_GetEventFavorites_Request\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AllEvents` | `bool` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_GetEventFavorites_Response

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_GetEventFavorites_Response\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AllEvents` | `bool` | get, set | - |
| `JsonFavorites` | `string` | get, set | - |
| `JsonFeatured` | `string` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_GiftsLeaderboardRequest

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_GiftsLeaderboardRequest\>`



---

## 🔌 CMsgGCCStrike15_v2_GiftsLeaderboardResponse

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_GiftsLeaderboardResponse\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Servertime` | `uint` | get, set | - |
| `TimePeriodSeconds` | `uint` | get, set | - |
| `TotalGiftsGiven` | `uint` | get, set | - |
| `TotalGivers` | `uint` | get, set | - |
| `Entries` | `IProtobufRepeatedFieldSubMessageType\<CMsgGCCStrike15_v2_GiftsLeaderboardResponse_GiftLeaderboardEntry\>` | get | - |



---

## 🔌 CMsgGCCStrike15_v2_GiftsLeaderboardResponse_GiftLeaderboardEntry

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_GiftsLeaderboardResponse_GiftLeaderboardEntry\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Accountid` | `uint` | get, set | - |
| `Gifts` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_MatchEndRewardDropsNotification

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_MatchEndRewardDropsNotification\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Iteminfo` | `CEconItemPreviewDataBlock` | get | - |



---

## 🔌 CMsgGCCStrike15_v2_MatchEndRunRewardDrops

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_MatchEndRunRewardDrops\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Serverinfo` | `CMsgGCCStrike15_v2_MatchmakingServerReservationResponse` | get | - |
| `MatchEndQuestData` | `CMsgGC_ServerQuestUpdateData` | get | - |



---

## 🔌 CMsgGCCStrike15_v2_MatchList

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_MatchList\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Msgrequestid` | `uint` | get, set | - |
| `Accountid` | `uint` | get, set | - |
| `Servertime` | `uint` | get, set | - |
| `Matches` | `IProtobufRepeatedFieldSubMessageType\<CDataGCCStrike15_v2_MatchInfo\>` | get | - |
| `Streams` | `IProtobufRepeatedFieldSubMessageType\<TournamentTeam\>` | get | - |
| `Tournamentinfo` | `CDataGCCStrike15_v2_TournamentInfo` | get | - |



---

## 🔌 CMsgGCCStrike15_v2_MatchListRequestCurrentLiveGames

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_MatchListRequestCurrentLiveGames\>`



---

## 🔌 CMsgGCCStrike15_v2_MatchListRequestFullGameInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_MatchListRequestFullGameInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Matchid` | `ulong` | get, set | - |
| `Outcomeid` | `ulong` | get, set | - |
| `Token` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_MatchListRequestLiveGameForUser

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_MatchListRequestLiveGameForUser\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Accountid` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_MatchListRequestRecentUserGames

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_MatchListRequestRecentUserGames\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Accountid` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_MatchListRequestTournamentGames

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_MatchListRequestTournamentGames\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Eventid` | `int` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_MatchListTournamentOperatorMgmt

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_MatchListTournamentOperatorMgmt\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Eventid` | `int` | get, set | - |
| `Matches` | `IProtobufRepeatedFieldSubMessageType\<CDataGCCStrike15_v2_MatchInfo\>` | get | - |
| `Accountid` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_MatchmakingClient2GCHello

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_MatchmakingClient2GCHello\>`



---

## 🔌 CMsgGCCStrike15_v2_MatchmakingClient2ServerPing

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_MatchmakingClient2ServerPing\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Gameserverpings` | `IProtobufRepeatedFieldSubMessageType\<GameServerPing\>` | get | - |
| `OffsetIndex` | `int` | get, set | - |
| `FinalBatch` | `int` | get, set | - |
| `DataCenterPings` | `IProtobufRepeatedFieldSubMessageType\<DataCenterPing\>` | get | - |
| `MaxPing` | `uint` | get, set | - |
| `TestToken` | `uint` | get, set | - |
| `SearchKey` | `byte[]` | get, set | - |
| `Notes` | `IProtobufRepeatedFieldSubMessageType\<CMsgGCCStrike15_v2_MatchmakingGC2ClientUpdate_Note\>` | get | - |
| `DebugMessage` | `string` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_MatchmakingGC2ClientAbandon

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_MatchmakingGC2ClientAbandon\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AccountId` | `uint` | get, set | - |
| `AbandonedMatch` | `CMsgGCCStrike15_v2_MatchmakingGC2ClientReserve` | get | - |
| `PenaltySeconds` | `uint` | get, set | - |
| `PenaltyReason` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_MatchmakingGC2ClientHello

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_MatchmakingGC2ClientHello\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AccountId` | `uint` | get, set | - |
| `Ongoingmatch` | `CMsgGCCStrike15_v2_MatchmakingGC2ClientReserve` | get | - |
| `GlobalStats` | `GlobalStatistics` | get | - |
| `PenaltySeconds` | `uint` | get, set | - |
| `PenaltyReason` | `uint` | get, set | - |
| `VacBanned` | `int` | get, set | - |
| `Ranking` | `PlayerRankingInfo` | get | - |
| `Commendation` | `PlayerCommendationInfo` | get | - |
| `Medals` | `PlayerMedalsInfo` | get | - |
| `MyCurrentEvent` | `TournamentEvent` | get | - |
| `MyCurrentEventTeams` | `IProtobufRepeatedFieldSubMessageType\<TournamentTeam\>` | get | - |
| `MyCurrentTeam` | `TournamentTeam` | get | - |
| `MyCurrentEventStages` | `IProtobufRepeatedFieldSubMessageType\<TournamentEvent\>` | get | - |
| `SurveyVote` | `uint` | get, set | - |
| `Activity` | `AccountActivity` | get | - |
| `PlayerLevel` | `int` | get, set | - |
| `PlayerCurXp` | `int` | get, set | - |
| `PlayerXpBonusFlags` | `int` | get, set | - |
| `Rankings` | `IProtobufRepeatedFieldSubMessageType\<PlayerRankingInfo\>` | get | - |
| `Owcaseid` | `ulong` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_MatchmakingGC2ClientReserve

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_MatchmakingGC2ClientReserve\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Serverid` | `ulong` | get, set | - |
| `DirectUdpIp` | `uint` | get, set | - |
| `DirectUdpPort` | `uint` | get, set | - |
| `Reservationid` | `ulong` | get, set | - |
| `Reservation` | `CMsgGCCStrike15_v2_MatchmakingGC2ServerReserve` | get | - |
| `Map` | `string` | get, set | - |
| `ServerAddress` | `string` | get, set | - |
| `GsPing` | `DataCenterPing` | get | - |
| `GsLocationId` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_MatchmakingGC2ClientSearchStats

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_MatchmakingGC2ClientSearchStats\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `GsLocationId` | `uint` | get, set | - |
| `DataCenterId` | `uint` | get, set | - |
| `NumLockedIn` | `uint` | get, set | - |
| `NumFoundNearby` | `uint` | get, set | - |
| `NoteLevel` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_MatchmakingGC2ClientUpdate

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_MatchmakingGC2ClientUpdate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Matchmaking` | `int` | get, set | - |
| `WaitingAccountIdSessions` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `Error` | `string` | get, set | - |
| `OngoingmatchAccountIdSessions` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `GlobalStats` | `GlobalStatistics` | get | - |
| `FailpingAccountIdSessions` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `PenaltyAccountIdSessions` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `FailreadyAccountIdSessions` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `VacbannedAccountIdSessions` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `ServerIpaddressMask` | `IpAddressMask` | get | - |
| `Notes` | `IProtobufRepeatedFieldSubMessageType\<CMsgGCCStrike15_v2_MatchmakingGC2ClientUpdate_Note\>` | get | - |
| `PenaltyAccountIdSessionsGreen` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `InsufficientlevelSessions` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `VsncheckAccountIdSessions` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `LauncherMismatchSessions` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `InsecureAccountIdSessions` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |



---

## 🔌 CMsgGCCStrike15_v2_MatchmakingGC2ClientUpdate_Note

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_MatchmakingGC2ClientUpdate_Note\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Type` | `int` | get, set | - |
| `RegionId` | `int` | get, set | - |
| `RegionR` | `float` | get, set | - |
| `Distance` | `float` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_MatchmakingGC2ServerConfirm

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_MatchmakingGC2ServerConfirm\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Token` | `uint` | get, set | - |
| `Stamp` | `uint` | get, set | - |
| `Exchange` | `ulong` | get, set | - |
| `Retry` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_MatchmakingGC2ServerReserve

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_MatchmakingGC2ServerReserve\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AccountIds` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `GameType` | `uint` | get, set | - |
| `MatchId` | `ulong` | get, set | - |
| `ServerVersion` | `uint` | get, set | - |
| `Flags` | `uint` | get, set | - |
| `Rankings` | `IProtobufRepeatedFieldSubMessageType\<PlayerRankingInfo\>` | get | - |
| `EncryptionKey` | `ulong` | get, set | - |
| `EncryptionKeyPub` | `ulong` | get, set | - |
| `PartyIds` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `Whitelist` | `IProtobufRepeatedFieldSubMessageType\<IpAddressMask\>` | get | - |
| `TvMasterSteamid` | `ulong` | get, set | - |
| `TournamentEvent` | `TournamentEvent` | get | - |
| `TournamentTeams` | `IProtobufRepeatedFieldSubMessageType\<TournamentTeam\>` | get | - |
| `TournamentCastersAccountIds` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `TvRelaySteamid` | `ulong` | get, set | - |
| `PreMatchData` | `CPreMatchInfoData` | get | - |
| `TvControl` | `uint` | get, set | - |
| `OpVarValues` | `IProtobufRepeatedFieldSubMessageType\<OperationalVarValue\>` | get | - |
| `SocacheControl` | `uint` | get, set | - |
| `TeammateColors` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `MatchIdAdditional` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_MatchmakingOperator2GCBlogUpdate

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_MatchmakingOperator2GCBlogUpdate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MainPostUrl` | `string` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_MatchmakingServerReservationResponse

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_MatchmakingServerReservationResponse\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Reservationid` | `ulong` | get, set | - |
| `Reservation` | `CMsgGCCStrike15_v2_MatchmakingGC2ServerReserve` | get | - |
| `Map` | `string` | get, set | - |
| `GcReservationSent` | `ulong` | get, set | - |
| `ServerVersion` | `uint` | get, set | - |
| `TvInfo` | `ServerHltvInfo` | get | - |
| `RewardPlayerAccounts` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `IdlePlayerAccounts` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `RewardItemAttrDefIdx` | `uint` | get, set | - |
| `RewardItemAttrValue` | `uint` | get, set | - |
| `RewardItemAttrRewardIdx` | `uint` | get, set | - |
| `RewardDropList` | `uint` | get, set | - |
| `TournamentTag` | `string` | get, set | - |
| `LegacySteamdatagramPort` | `uint` | get, set | - |
| `SteamdatagramRouting` | `uint` | get, set | - |
| `TestToken` | `uint` | get, set | - |
| `Flags` | `uint` | get, set | - |
| `SystemLoad` | `uint` | get, set | - |
| `CpusOnline` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_MatchmakingServerRoundStats

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_MatchmakingServerRoundStats\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Reservationid` | `ulong` | get, set | - |
| `Reservation` | `CMsgGCCStrike15_v2_MatchmakingGC2ServerReserve` | get | - |
| `Map` | `string` | get, set | - |
| `Round` | `int` | get, set | - |
| `Kills` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `Assists` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `Deaths` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `Scores` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `Pings` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `RoundResult` | `int` | get, set | - |
| `MatchResult` | `int` | get, set | - |
| `TeamScores` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `Confirm` | `CMsgGCCStrike15_v2_MatchmakingGC2ServerConfirm` | get | - |
| `ReservationStage` | `int` | get, set | - |
| `MatchDuration` | `int` | get, set | - |
| `EnemyKills` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `EnemyHeadshots` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `Enemy3ks` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `Enemy4ks` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `Enemy5ks` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `Mvps` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `SpectatorsCount` | `uint` | get, set | - |
| `SpectatorsCountTv` | `uint` | get, set | - |
| `SpectatorsCountLnk` | `uint` | get, set | - |
| `EnemyKillsAgg` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `DropInfo` | `CMsgGCCStrike15_v2_MatchmakingServerRoundStats_DropInfo` | get | - |
| `BSwitchedTeams` | `bool` | get, set | - |
| `Enemy2ks` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `PlayerSpawned` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `TeamSpawnCount` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `MaxRounds` | `uint` | get, set | - |
| `MapId` | `int` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_MatchmakingServerRoundStats_DropInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_MatchmakingServerRoundStats_DropInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AccountMvp` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_MatchmakingStart

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_MatchmakingStart\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AccountIds` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `GameType` | `uint` | get, set | - |
| `TicketData` | `string` | get, set | - |
| `ClientVersion` | `uint` | get, set | - |
| `TournamentMatch` | `TournamentMatchSetup` | get | - |
| `PrimeOnly` | `bool` | get, set | - |
| `TvControl` | `uint` | get, set | - |
| `LobbyId` | `ulong` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_MatchmakingStop

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_MatchmakingStop\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Abandon` | `int` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_Party_Invite

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_Party_Invite\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Accountid` | `uint` | get, set | - |
| `Lobbyid` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_Party_Register

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_Party_Register\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Id` | `uint` | get, set | - |
| `Ver` | `uint` | get, set | - |
| `Apr` | `uint` | get, set | - |
| `Ark` | `uint` | get, set | - |
| `Nby` | `uint` | get, set | - |
| `Grp` | `uint` | get, set | - |
| `Slots` | `uint` | get, set | - |
| `Launcher` | `uint` | get, set | - |
| `GameType` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_Party_Search

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_Party_Search\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Ver` | `uint` | get, set | - |
| `Apr` | `uint` | get, set | - |
| `Ark` | `uint` | get, set | - |
| `Grps` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `Launcher` | `uint` | get, set | - |
| `GameType` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_Party_SearchResults

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_Party_SearchResults\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Entries` | `IProtobufRepeatedFieldSubMessageType\<CMsgGCCStrike15_v2_Party_SearchResults_Entry\>` | get | - |



---

## 🔌 CMsgGCCStrike15_v2_Party_SearchResults_Entry

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_Party_SearchResults_Entry\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Id` | `uint` | get, set | - |
| `Grp` | `uint` | get, set | - |
| `GameType` | `uint` | get, set | - |
| `Apr` | `uint` | get, set | - |
| `Ark` | `uint` | get, set | - |
| `Loc` | `uint` | get, set | - |
| `Accountid` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_PlayerOverwatchCaseAssignment

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_PlayerOverwatchCaseAssignment\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Caseid` | `ulong` | get, set | - |
| `Caseurl` | `string` | get, set | - |
| `Verdict` | `uint` | get, set | - |
| `Timestamp` | `uint` | get, set | - |
| `Throttleseconds` | `uint` | get, set | - |
| `Suspectid` | `uint` | get, set | - |
| `Fractionid` | `uint` | get, set | - |
| `Numrounds` | `uint` | get, set | - |
| `Fractionrounds` | `uint` | get, set | - |
| `Streakconvictions` | `int` | get, set | - |
| `Reason` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_PlayerOverwatchCaseStatus

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_PlayerOverwatchCaseStatus\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Caseid` | `ulong` | get, set | - |
| `Statusid` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_PlayerOverwatchCaseUpdate

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_PlayerOverwatchCaseUpdate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Caseid` | `ulong` | get, set | - |
| `Suspectid` | `uint` | get, set | - |
| `Fractionid` | `uint` | get, set | - |
| `RptAimbot` | `uint` | get, set | - |
| `RptWallhack` | `uint` | get, set | - |
| `RptSpeedhack` | `uint` | get, set | - |
| `RptTeamharm` | `uint` | get, set | - |
| `Reason` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_PlayersProfile

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_PlayersProfile\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `RequestId` | `uint` | get, set | - |
| `AccountProfiles` | `IProtobufRepeatedFieldSubMessageType\<CMsgGCCStrike15_v2_MatchmakingGC2ClientHello\>` | get | - |



---

## 🔌 CMsgGCCStrike15_v2_Predictions

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_Predictions\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EventId` | `uint` | get, set | - |
| `GroupMatchTeamPicks` | `IProtobufRepeatedFieldSubMessageType\<CMsgGCCStrike15_v2_Predictions_GroupMatchTeamPick\>` | get | - |



---

## 🔌 CMsgGCCStrike15_v2_Predictions_GroupMatchTeamPick

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_Predictions_GroupMatchTeamPick\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Sectionid` | `int` | get, set | - |
| `Groupid` | `int` | get, set | - |
| `Index` | `int` | get, set | - |
| `Teamid` | `int` | get, set | - |
| `Itemid` | `ulong` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_PremierSeasonSummary

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_PremierSeasonSummary\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AccountId` | `uint` | get, set | - |
| `SeasonId` | `uint` | get, set | - |
| `DataPerWeek` | `IProtobufRepeatedFieldSubMessageType\<CMsgGCCStrike15_v2_PremierSeasonSummary_DataPerWeek\>` | get | - |
| `DataPerMap` | `IProtobufRepeatedFieldSubMessageType\<CMsgGCCStrike15_v2_PremierSeasonSummary_DataPerMap\>` | get | - |



---

## 🔌 CMsgGCCStrike15_v2_PremierSeasonSummary_DataPerMap

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_PremierSeasonSummary_DataPerMap\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MapId` | `uint` | get, set | - |
| `Wins` | `uint` | get, set | - |
| `Ties` | `uint` | get, set | - |
| `Losses` | `uint` | get, set | - |
| `Rounds` | `uint` | get, set | - |
| `Kills` | `uint` | get, set | - |
| `Headshots` | `uint` | get, set | - |
| `Assists` | `uint` | get, set | - |
| `Deaths` | `uint` | get, set | - |
| `Mvps` | `uint` | get, set | - |
| `Rounds3k` | `uint` | get, set | - |
| `Rounds4k` | `uint` | get, set | - |
| `Rounds5k` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_PremierSeasonSummary_DataPerWeek

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_PremierSeasonSummary_DataPerWeek\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `WeekId` | `ulong` | get, set | - |
| `RankId` | `uint` | get, set | - |
| `MatchesPlayed` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_Server2GCClientValidate

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_Server2GCClientValidate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Accountid` | `uint` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_ServerNotificationForUserPenalty

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ServerNotificationForUserPenalty\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AccountId` | `uint` | get, set | - |
| `Reason` | `uint` | get, set | - |
| `Seconds` | `uint` | get, set | - |
| `CommunicationCooldown` | `bool` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_ServerVarValueNotificationInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_ServerVarValueNotificationInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Accountid` | `uint` | get, set | - |
| `Viewangles` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `Type` | `uint` | get, set | - |
| `Userdata` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |



---

## 🔌 CMsgGCCStrike15_v2_SetEventFavorite

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_SetEventFavorite\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Eventid` | `ulong` | get, set | - |
| `IsFavorite` | `bool` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_SetPlayerLeaderboardSafeName

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_SetPlayerLeaderboardSafeName\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `LeaderboardSafeName` | `string` | get, set | - |



---

## 🔌 CMsgGCCStrike15_v2_WatchInfoUsers

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCStrike15_v2_WatchInfoUsers\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `RequestId` | `uint` | get, set | - |
| `AccountIds` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `WatchableMatchInfos` | `IProtobufRepeatedFieldSubMessageType\<WatchableMatchInfo\>` | get | - |
| `ExtendedTimeout` | `uint` | get, set | - |



---

## 🔌 CMsgGCClientDisplayNotification

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCClientDisplayNotification\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `NotificationTitleLocalizationKey` | `string` | get, set | - |
| `NotificationBodyLocalizationKey` | `string` | get, set | - |
| `BodySubstringKeys` | `IProtobufRepeatedFieldValueType\<string\>` | get | - |
| `BodySubstringValues` | `IProtobufRepeatedFieldValueType\<string\>` | get | - |



---

## 🔌 CMsgGCClientVersionUpdated

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCClientVersionUpdated\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ClientVersion` | `uint` | get, set | - |



---

## 🔌 CMsgGCCollectItem

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCollectItem\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CollectionItemId` | `ulong` | get, set | - |
| `SubjectItemId` | `ulong` | get, set | - |



---

## 🔌 CMsgGCCstrike15_v2_ClientRedeemFreeReward

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCstrike15_v2_ClientRedeemFreeReward\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `GenerationTime` | `uint` | get, set | - |
| `RedeemableBalance` | `uint` | get, set | - |
| `Items` | `IProtobufRepeatedFieldValueType\<ulong\>` | get | - |



---

## 🔌 CMsgGCCstrike15_v2_ClientRedeemMissionReward

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCstrike15_v2_ClientRedeemMissionReward\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CampaignId` | `uint` | get, set | - |
| `RedeemId` | `uint` | get, set | - |
| `RedeemableBalance` | `uint` | get, set | - |
| `ExpectedCost` | `uint` | get, set | - |
| `BidControl` | `int` | get, set | - |



---

## 🔌 CMsgGCCstrike15_v2_GC2ServerNotifyXPRewarded

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCCstrike15_v2_GC2ServerNotifyXPRewarded\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `XpProgressData` | `IProtobufRepeatedFieldSubMessageType\<XpProgressData\>` | get | - |
| `AccountId` | `uint` | get, set | - |
| `CurrentXp` | `uint` | get, set | - |
| `CurrentLevel` | `uint` | get, set | - |
| `UpgradedDefidx` | `uint` | get, set | - |
| `OperationPointsAwarded` | `uint` | get, set | - |
| `FreeRewards` | `uint` | get, set | - |
| `XpTrailRemaining` | `uint` | get, set | - |
| `XpTrailXpNeeded` | `int` | get, set | - |
| `XpTrailLevel` | `uint` | get, set | - |



---

## 🔌 CMsgGCDev_SchemaReservationRequest

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCDev_SchemaReservationRequest\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SchemaTypename` | `string` | get, set | - |
| `InstanceName` | `string` | get, set | - |
| `Context` | `ulong` | get, set | - |
| `Id` | `ulong` | get, set | - |



---

## 🔌 CMsgGCError

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCError\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ErrorText` | `string` | get, set | - |



---

## 🔌 CMsgGCGiftedItems

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCGiftedItems\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Accountid` | `uint` | get, set | - |
| `Giftdefindex` | `uint` | get, set | - |
| `MaxGiftsPossible` | `uint` | get, set | - |
| `NumEligibleRecipients` | `uint` | get, set | - |
| `RecipientsAccountids` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |



---

## 🔌 CMsgGCHAccountPhoneNumberChange

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCHAccountPhoneNumberChange\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Steamid` | `ulong` | get, set | - |
| `Appid` | `uint` | get, set | - |
| `PhoneId` | `ulong` | get, set | - |
| `IsVerified` | `bool` | get, set | - |
| `IsIdentifying` | `bool` | get, set | - |



---

## 🔌 CMsgGCHInviteUserToLobby

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCHInviteUserToLobby\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Steamid` | `ulong` | get, set | - |
| `Appid` | `uint` | get, set | - |
| `SteamidInvited` | `ulong` | get, set | - |
| `SteamidLobby` | `ulong` | get, set | - |



---

## 🔌 CMsgGCHRecurringSubscriptionStatusChange

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCHRecurringSubscriptionStatusChange\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Steamid` | `ulong` | get, set | - |
| `Appid` | `uint` | get, set | - |
| `Agreementid` | `ulong` | get, set | - |
| `Active` | `bool` | get, set | - |



---

## 🔌 CMsgGCHVacVerificationChange

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCHVacVerificationChange\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Steamid` | `ulong` | get, set | - |
| `Appid` | `uint` | get, set | - |
| `IsVerified` | `bool` | get, set | - |



---

## 🔌 CMsgGCIncrementKillCountResponse

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCIncrementKillCountResponse\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `KillerAccountId` | `uint` | get, set | - |
| `NumKills` | `uint` | get, set | - |
| `ItemDef` | `uint` | get, set | - |
| `LevelType` | `uint` | get, set | - |



---

## 🔌 CMsgGCItemCustomizationNotification

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCItemCustomizationNotification\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ItemId` | `IProtobufRepeatedFieldValueType\<ulong\>` | get | - |
| `Request` | `uint` | get, set | - |
| `ExtraData` | `IProtobufRepeatedFieldValueType\<ulong\>` | get | - |



---

## 🔌 CMsgGCItemPreviewItemBoughtNotification

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCItemPreviewItemBoughtNotification\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ItemDefIndex` | `uint` | get, set | - |



---

## 🔌 CMsgGCMultiplexMessage

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCMultiplexMessage\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Msgtype` | `uint` | get, set | - |
| `Payload` | `byte[]` | get, set | - |
| `Steamids` | `IProtobufRepeatedFieldValueType\<ulong\>` | get | - |
| `Replytogc` | `bool` | get, set | - |



---

## 🔌 CMsgGCMultiplexMessage_Response

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCMultiplexMessage_Response\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Msgtype` | `uint` | get, set | - |



---

## 🔌 CMsgGCNameItemNotification

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCNameItemNotification\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlayerSteamid` | `ulong` | get, set | - |
| `ItemDefIndex` | `uint` | get, set | - |
| `ItemNameCustom` | `string` | get, set | - |



---

## 🔌 CMsgGCReportAbuse

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCReportAbuse\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TargetSteamId` | `ulong` | get, set | - |
| `Description` | `string` | get, set | - |
| `Gid` | `ulong` | get, set | - |
| `AbuseType` | `uint` | get, set | - |
| `ContentType` | `uint` | get, set | - |
| `TargetGameServerIp` | `uint` | get, set | - |
| `TargetGameServerPort` | `uint` | get, set | - |



---

## 🔌 CMsgGCReportAbuseResponse

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCReportAbuseResponse\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TargetSteamId` | `ulong` | get, set | - |
| `Result` | `uint` | get, set | - |
| `ErrorMessage` | `string` | get, set | - |



---

## 🔌 CMsgGCRequestAnnouncements

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCRequestAnnouncements\>`



---

## 🔌 CMsgGCRequestAnnouncementsResponse

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCRequestAnnouncementsResponse\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AnnouncementTitle` | `string` | get, set | - |
| `Announcement` | `string` | get, set | - |
| `NextmatchTitle` | `string` | get, set | - |
| `Nextmatch` | `string` | get, set | - |



---

## 🔌 CMsgGCRequestSessionIP

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCRequestSessionIP\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Steamid` | `ulong` | get, set | - |



---

## 🔌 CMsgGCRequestSessionIPResponse

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCRequestSessionIPResponse\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Ip` | `uint` | get, set | - |



---

## 🔌 CMsgGCServerVersionUpdated

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCServerVersionUpdated\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ServerVersion` | `uint` | get, set | - |



---

## 🔌 CMsgGCShowItemsPickedUp

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCShowItemsPickedUp\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlayerSteamid` | `ulong` | get, set | - |



---

## 🔌 CMsgGCStorePurchaseCancel

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCStorePurchaseCancel\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TxnId` | `ulong` | get, set | - |



---

## 🔌 CMsgGCStorePurchaseCancelResponse

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCStorePurchaseCancelResponse\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Result` | `uint` | get, set | - |



---

## 🔌 CMsgGCStorePurchaseFinalize

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCStorePurchaseFinalize\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TxnId` | `ulong` | get, set | - |



---

## 🔌 CMsgGCStorePurchaseFinalizeResponse

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCStorePurchaseFinalizeResponse\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Result` | `uint` | get, set | - |
| `ItemIds` | `IProtobufRepeatedFieldValueType\<ulong\>` | get | - |



---

## 🔌 CMsgGCStorePurchaseInit

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCStorePurchaseInit\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Country` | `string` | get, set | - |
| `Language` | `int` | get, set | - |
| `Currency` | `int` | get, set | - |
| `LineItems` | `IProtobufRepeatedFieldSubMessageType\<CGCStorePurchaseInit_LineItem\>` | get | - |



---

## 🔌 CMsgGCStorePurchaseInitResponse

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCStorePurchaseInitResponse\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Result` | `int` | get, set | - |
| `TxnId` | `ulong` | get, set | - |
| `Url` | `string` | get, set | - |
| `ItemIds` | `IProtobufRepeatedFieldValueType\<ulong\>` | get | - |



---

## 🔌 CMsgGCToClientSteamDatagramTicket

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCToClientSteamDatagramTicket\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SerializedTicket` | `byte[]` | get, set | - |



---

## 🔌 CMsgGCToGCBannedWordListBroadcast

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCToGCBannedWordListBroadcast\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Broadcast` | `CMsgGCBannedWordListResponse` | get | - |



---

## 🔌 CMsgGCToGCBannedWordListUpdated

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCToGCBannedWordListUpdated\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `GroupId` | `uint` | get, set | - |



---

## 🔌 CMsgGCToGCBroadcastConsoleCommand

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCToGCBroadcastConsoleCommand\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ConCommand` | `string` | get, set | - |



---

## 🔌 CMsgGCToGCDirtyMultipleSDOCache

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCToGCDirtyMultipleSDOCache\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SdoType` | `uint` | get, set | - |
| `KeyUint64` | `IProtobufRepeatedFieldValueType\<ulong\>` | get | - |



---

## 🔌 CMsgGCToGCDirtySDOCache

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCToGCDirtySDOCache\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SdoType` | `uint` | get, set | - |
| `KeyUint64` | `ulong` | get, set | - |



---

## 🔌 CMsgGCToGCIsTrustedServer

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCToGCIsTrustedServer\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SteamId` | `ulong` | get, set | - |



---

## 🔌 CMsgGCToGCIsTrustedServerResponse

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCToGCIsTrustedServerResponse\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `IsTrusted` | `bool` | get, set | - |



---

## 🔌 CMsgGCToGCRequestPassportItemGrant

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCToGCRequestPassportItemGrant\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SteamId` | `ulong` | get, set | - |
| `LeagueId` | `uint` | get, set | - |
| `RewardFlag` | `int` | get, set | - |



---

## 🔌 CMsgGCToGCUpdateSQLKeyValue

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCToGCUpdateSQLKeyValue\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `KeyName` | `string` | get, set | - |



---

## 🔌 CMsgGCToGCWebAPIAccountChanged

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCToGCWebAPIAccountChanged\>`



---

## 🔌 CMsgGCUpdateSessionIP

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCUpdateSessionIP\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Steamid` | `ulong` | get, set | - |
| `Ip` | `uint` | get, set | - |



---

## 🔌 CMsgGCUserTrackTimePlayedConsecutively

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGCUserTrackTimePlayedConsecutively\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `State` | `uint` | get, set | - |



---

## 🔌 CMsgGC_GlobalGame_Play

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGC_GlobalGame_Play\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Ticket` | `ulong` | get, set | - |
| `Gametimems` | `uint` | get, set | - |
| `Msperpoint` | `uint` | get, set | - |



---

## 🔌 CMsgGC_GlobalGame_Subscribe

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGC_GlobalGame_Subscribe\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Ticket` | `ulong` | get, set | - |



---

## 🔌 CMsgGC_GlobalGame_Unsubscribe

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGC_GlobalGame_Unsubscribe\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Timeleft` | `int` | get, set | - |



---

## 🔌 CMsgGC_ServerQuestUpdateData

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGC_ServerQuestUpdateData\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlayerQuestData` | `IProtobufRepeatedFieldSubMessageType\<PlayerQuestData\>` | get | - |
| `BinaryData` | `byte[]` | get, set | - |
| `MmGameMode` | `uint` | get, set | - |
| `Missionlbsdata` | `ScoreLeaderboardData` | get | - |
| `Flags` | `uint` | get, set | - |



---

## 🔌 CMsgGameServerInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgGameServerInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ServerPublicIpAddr` | `uint` | get, set | - |
| `ServerPrivateIpAddr` | `uint` | get, set | - |
| `ServerPort` | `uint` | get, set | - |
| `ServerTvPort` | `uint` | get, set | - |
| `ServerKey` | `string` | get, set | - |
| `ServerHibernation` | `bool` | get, set | - |
| `ServerType` | `CMsgGameServerInfo_ServerType` | get, set | - |
| `ServerRegion` | `uint` | get, set | - |
| `ServerLoadavg` | `float` | get, set | - |
| `ServerTvBroadcastTime` | `float` | get, set | - |
| `ServerGameTime` | `float` | get, set | - |
| `ServerRelayConnectedSteamId` | `ulong` | get, set | - |
| `RelaySlotsMax` | `uint` | get, set | - |
| `RelaysConnected` | `int` | get, set | - |
| `RelayClientsConnected` | `int` | get, set | - |
| `RelayedGameServerSteamId` | `ulong` | get, set | - |
| `ParentRelayCount` | `uint` | get, set | - |
| `TvSecretCode` | `ulong` | get, set | - |



---

## 📋 CMsgGameServerInfo_ServerType

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `UNSPECIFIED` | `0` | - |
| `GAME` | `1` | - |
| `PROXY` | `2` | - |



---

## 🔌 CMsgIPCAddress

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgIPCAddress\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ComputerGuid` | `ulong` | get, set | - |
| `ProcessId` | `uint` | get, set | - |



---

## 🔌 CMsgIncrementKillCount

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`



---

## 🔌 CMsgInvitationCreated

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgInvitationCreated\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `GroupId` | `ulong` | get, set | - |
| `SteamId` | `ulong` | get, set | - |



---

## 🔌 CMsgInviteToParty

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgInviteToParty\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SteamId` | `ulong` | get, set | - |
| `ClientVersion` | `uint` | get, set | - |
| `TeamInvite` | `uint` | get, set | - |



---

## 🔌 CMsgItemAcknowledged

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgItemAcknowledged\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Iteminfo` | `CEconItemPreviewDataBlock` | get | - |



---

## 🔌 CMsgItemAcknowledged__DEPRECATED

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgItemAcknowledged__DEPRECATED\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AccountId` | `uint` | get, set | - |
| `Inventory` | `uint` | get, set | - |
| `DefIndex` | `uint` | get, set | - |
| `Quality` | `uint` | get, set | - |
| `Rarity` | `uint` | get, set | - |
| `Origin` | `uint` | get, set | - |
| `ItemId` | `ulong` | get, set | - |



---

## 🔌 CMsgKickFromParty

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgKickFromParty\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SteamId` | `ulong` | get, set | - |



---

## 🔌 CMsgLANServerAvailable

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgLANServerAvailable\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `LobbyId` | `ulong` | get, set | - |



---

## 🔌 CMsgLeaveParty

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgLeaveParty\>`



---

## 🔌 CMsgLegacySource1ClientWelcome

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgLegacySource1ClientWelcome\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Version` | `uint` | get, set | - |
| `GameData` | `byte[]` | get, set | - |
| `OutofdateSubscribedCaches` | `IProtobufRepeatedFieldSubMessageType\<CMsgSOCacheSubscribed\>` | get | - |
| `UptodateSubscribedCaches` | `IProtobufRepeatedFieldSubMessageType\<CMsgSOCacheSubscriptionCheck\>` | get | - |
| `Location` | `CMsgLegacySource1ClientWelcome_Location` | get | - |
| `GameData2` | `byte[]` | get, set | - |
| `Rtime32GcWelcomeTimestamp` | `uint` | get, set | - |
| `Currency` | `uint` | get, set | - |
| `Balance` | `uint` | get, set | - |
| `BalanceUrl` | `string` | get, set | - |
| `TxnCountryCode` | `string` | get, set | - |



---

## 🔌 CMsgLegacySource1ClientWelcome_Location

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgLegacySource1ClientWelcome_Location\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Latitude` | `float` | get, set | - |
| `Longitude` | `float` | get, set | - |
| `Country` | `string` | get, set | - |



---

## 🔌 CMsgModifyItem

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`



---

## 🔌 CMsgOpenCrate

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgOpenCrate\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ToolItemId` | `ulong` | get, set | - |
| `SubjectItemId` | `ulong` | get, set | - |
| `ForRental` | `bool` | get, set | - |
| `PointsRemaining` | `uint` | get, set | - |



---

## 🔌 CMsgPartyInviteResponse

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgPartyInviteResponse\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PartyId` | `ulong` | get, set | - |
| `Accept` | `bool` | get, set | - |
| `ClientVersion` | `uint` | get, set | - |
| `TeamInvite` | `uint` | get, set | - |



---

## 🔌 CMsgPlaceDecalEvent

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgPlaceDecalEvent\>`

**实现接口:** `INetMessage\<CMsgPlaceDecalEvent\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Position` | `Vector` | get, set | - |
| `Normal` | `Vector` | get, set | - |
| `Saxis` | `Vector` | get, set | - |
| `Boneindex` | `int` | get, set | - |
| `Triangleindex` | `int` | get, set | - |
| `Flags` | `uint` | get, set | - |
| `Color` | `uint` | get, set | - |
| `RandomSeed` | `int` | get, set | - |
| `DecalGroupName` | `uint` | get, set | - |
| `SizeOverride` | `float` | get, set | - |
| `Entityhandle` | `uint` | get, set | - |
| `MaterialId` | `ulong` | get, set | - |
| `SequenceName` | `uint` | get, set | - |



---

## 🔌 CMsgPlayerBulletHit

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgPlayerBulletHit\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AttackerSlot` | `int` | get, set | - |
| `VictimSlot` | `int` | get, set | - |
| `VictimPos` | `Vector` | get, set | - |
| `HitGroup` | `int` | get, set | - |
| `Damage` | `int` | get, set | - |
| `PenetrationCount` | `int` | get, set | - |
| `IsKill` | `bool` | get, set | - |



---

## 🔌 CMsgPlayerInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgPlayerInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | get, set | - |
| `Xuid` | `ulong` | get, set | - |
| `Userid` | `int` | get, set | - |
| `Steamid` | `ulong` | get, set | - |
| `Fakeplayer` | `bool` | get, set | - |
| `Ishltv` | `bool` | get, set | - |



---

## 🔌 CMsgProtoBufHeader

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgProtoBufHeader\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ClientSteamId` | `ulong` | get, set | - |
| `ClientSessionId` | `int` | get, set | - |
| `SourceAppId` | `uint` | get, set | - |
| `JobIdSource` | `ulong` | get, set | - |
| `JobIdTarget` | `ulong` | get, set | - |
| `TargetJobName` | `string` | get, set | - |
| `Eresult` | `int` | get, set | - |
| `ErrorMessage` | `string` | get, set | - |
| `Ip` | `uint` | get, set | - |
| `GcMsgSrc` | `GCProtoBufMsgSrc` | get, set | - |
| `GcDirIndexSource` | `uint` | get, set | - |



---

## 🔌 CMsgQAngle

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgQAngle\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `X` | `float` | get, set | - |
| `Y` | `float` | get, set | - |
| `Z` | `float` | get, set | - |



---

## 🔌 CMsgQuaternion

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgQuaternion\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `X` | `float` | get, set | - |
| `Y` | `float` | get, set | - |
| `Z` | `float` | get, set | - |
| `W` | `float` | get, set | - |



---

## 🔌 CMsgRGBA

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgRGBA\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `R` | `int` | get, set | - |
| `G` | `int` | get, set | - |
| `B` | `int` | get, set | - |
| `A` | `int` | get, set | - |



---

## 🔌 CMsgRecurringMissionSchema

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgRecurringMissionSchema\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Missions` | `IProtobufRepeatedFieldSubMessageType\<CMsgRecurringMissionSchema_MissionTemplateList\>` | get | - |



---

## 🔌 CMsgRecurringMissionSchema_MissionTemplateList

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgRecurringMissionSchema_MissionTemplateList\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Period` | `uint` | get, set | - |
| `MissionTemplates` | `IProtobufRepeatedFieldValueType\<byte[]\>` | get | - |



---

## 🔌 CMsgReplayUploadedToYouTube

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgReplayUploadedToYouTube\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `YoutubeUrl` | `string` | get, set | - |
| `YoutubeAccountName` | `string` | get, set | - |
| `SessionId` | `ulong` | get, set | - |



---

## 🔌 CMsgReplicateConVars

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgReplicateConVars\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Convars` | `IProtobufRepeatedFieldSubMessageType\<CMsgConVarValue\>` | get | - |



---

## 🔌 CMsgRequestInventoryRefresh

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgRequestInventoryRefresh\>`



---

## 🔌 CMsgRequestRecurringMissionSchedule

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgRequestRecurringMissionSchedule\>`



---

## 🔌 CMsgSDONoMemcached

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSDONoMemcached\>`



---

## 🔌 CMsgSOCacheHaveVersion

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSOCacheHaveVersion\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Soid` | `CMsgSOIDOwner` | get | - |
| `Version` | `ulong` | get, set | - |



---

## 🔌 CMsgSOCacheSubscribed

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSOCacheSubscribed\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Objects` | `IProtobufRepeatedFieldSubMessageType\<CMsgSOCacheSubscribed_SubscribedType\>` | get | - |
| `Version` | `ulong` | get, set | - |
| `OwnerSoid` | `CMsgSOIDOwner` | get | - |



---

## 🔌 CMsgSOCacheSubscribed_SubscribedType

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSOCacheSubscribed_SubscribedType\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TypeId` | `int` | get, set | - |
| `ObjectData` | `IProtobufRepeatedFieldValueType\<byte[]\>` | get | - |



---

## 🔌 CMsgSOCacheSubscriptionCheck

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSOCacheSubscriptionCheck\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Version` | `ulong` | get, set | - |
| `OwnerSoid` | `CMsgSOIDOwner` | get | - |



---

## 🔌 CMsgSOCacheSubscriptionRefresh

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSOCacheSubscriptionRefresh\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `OwnerSoid` | `CMsgSOIDOwner` | get | - |



---

## 🔌 CMsgSOCacheUnsubscribed

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSOCacheUnsubscribed\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `OwnerSoid` | `CMsgSOIDOwner` | get | - |



---

## 🔌 CMsgSOCacheVersion

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSOCacheVersion\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Version` | `ulong` | get, set | - |



---

## 🔌 CMsgSOIDOwner

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSOIDOwner\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Type` | `uint` | get, set | - |
| `Id` | `ulong` | get, set | - |



---

## 🔌 CMsgSOMultipleObjects

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSOMultipleObjects\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ObjectsModified` | `IProtobufRepeatedFieldSubMessageType\<CMsgSOMultipleObjects_SingleObject\>` | get | - |
| `Version` | `ulong` | get, set | - |
| `OwnerSoid` | `CMsgSOIDOwner` | get | - |



---

## 🔌 CMsgSOMultipleObjects_SingleObject

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSOMultipleObjects_SingleObject\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TypeId` | `int` | get, set | - |
| `ObjectData` | `byte[]` | get, set | - |



---

## 🔌 CMsgSOSingleObject

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSOSingleObject\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TypeId` | `int` | get, set | - |
| `ObjectData` | `byte[]` | get, set | - |
| `Version` | `ulong` | get, set | - |
| `OwnerSoid` | `CMsgSOIDOwner` | get | - |



---

## 🔌 CMsgSerializedSOCache

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSerializedSOCache\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `FileVersion` | `uint` | get, set | - |
| `Caches` | `IProtobufRepeatedFieldSubMessageType\<CMsgSerializedSOCache_Cache\>` | get | - |
| `GcSocacheFileVersion` | `uint` | get, set | - |



---

## 🔌 CMsgSerializedSOCache_Cache

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSerializedSOCache_Cache\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Type` | `uint` | get, set | - |
| `Id` | `ulong` | get, set | - |
| `Versions` | `IProtobufRepeatedFieldSubMessageType\<CMsgSerializedSOCache_Cache_Version\>` | get | - |
| `TypeCaches` | `IProtobufRepeatedFieldSubMessageType\<CMsgSerializedSOCache_TypeCache\>` | get | - |



---

## 🔌 CMsgSerializedSOCache_Cache_Version

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSerializedSOCache_Cache_Version\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Service` | `uint` | get, set | - |
| `Version` | `ulong` | get, set | - |



---

## 🔌 CMsgSerializedSOCache_TypeCache

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSerializedSOCache_TypeCache\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Type` | `uint` | get, set | - |
| `Objects` | `IProtobufRepeatedFieldValueType\<byte[]\>` | get | - |
| `ServiceId` | `uint` | get, set | - |



---

## 🔌 CMsgServerAvailable

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgServerAvailable\>`



---

## 🔌 CMsgServerHello

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgServerHello\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Version` | `uint` | get, set | - |
| `SocacheHaveVersions` | `IProtobufRepeatedFieldSubMessageType\<CMsgSOCacheHaveVersion\>` | get | - |
| `LegacyClientSessionNeed` | `uint` | get, set | - |
| `ClientLauncher` | `uint` | get, set | - |
| `LegacySteamdatagramRouting` | `byte[]` | get, set | - |
| `RequiredInternalAddr` | `uint` | get, set | - |
| `SteamdatagramLogin` | `byte[]` | get, set | - |
| `SocacheControl` | `uint` | get, set | - |



---

## 🔌 CMsgServerNetworkStats

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgServerNetworkStats\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Dedicated` | `bool` | get, set | - |
| `CpuUsage` | `int` | get, set | - |
| `MemoryUsedMb` | `int` | get, set | - |
| `MemoryFreeMb` | `int` | get, set | - |
| `Uptime` | `int` | get, set | - |
| `SpawnCount` | `int` | get, set | - |
| `NumClients` | `int` | get, set | - |
| `NumBots` | `int` | get, set | - |
| `NumSpectators` | `int` | get, set | - |
| `NumTvRelays` | `int` | get, set | - |
| `Fps` | `float` | get, set | - |
| `Ports` | `IProtobufRepeatedFieldSubMessageType\<CMsgServerNetworkStats_Port\>` | get | - |
| `AvgPingMs` | `float` | get, set | - |
| `AvgEngineLatencyOut` | `float` | get, set | - |
| `AvgPacketsOut` | `float` | get, set | - |
| `AvgPacketsIn` | `float` | get, set | - |
| `AvgLossOut` | `float` | get, set | - |
| `AvgLossIn` | `float` | get, set | - |
| `AvgDataOut` | `float` | get, set | - |
| `AvgDataIn` | `float` | get, set | - |
| `TotalDataIn` | `ulong` | get, set | - |
| `TotalPacketsIn` | `ulong` | get, set | - |
| `TotalDataOut` | `ulong` | get, set | - |
| `TotalPacketsOut` | `ulong` | get, set | - |
| `Players` | `IProtobufRepeatedFieldSubMessageType\<CMsgServerNetworkStats_Player\>` | get | - |



---

## 🔌 CMsgServerNetworkStats_Player

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgServerNetworkStats_Player\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Steamid` | `ulong` | get, set | - |
| `RemoteAddr` | `string` | get, set | - |
| `PingAvgMs` | `int` | get, set | - |
| `PacketLossPct` | `float` | get, set | - |
| `IsBot` | `bool` | get, set | - |
| `LossIn` | `float` | get, set | - |
| `LossOut` | `float` | get, set | - |
| `EngineLatencyMs` | `int` | get, set | - |



---

## 🔌 CMsgServerNetworkStats_Port

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgServerNetworkStats_Port\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Port` | `int` | get, set | - |
| `Name` | `string` | get, set | - |



---

## 🔌 CMsgServerPeer

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgServerPeer\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlayerSlot` | `int` | get, set | - |
| `Steamid` | `ulong` | get, set | - |
| `Ipc` | `CMsgIPCAddress` | get | - |
| `TheyHearYou` | `bool` | get, set | - |
| `YouHearThem` | `bool` | get, set | - |
| `IsListenserverHost` | `bool` | get, set | - |



---

## 🔌 CMsgServerUserCmd

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgServerUserCmd\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Data` | `byte[]` | get, set | - |
| `CmdNumber` | `int` | get, set | - |
| `PlayerSlot` | `int` | get, set | - |
| `ServerTickExecuted` | `int` | get, set | - |
| `ClientTick` | `int` | get, set | - |



---

## 🔌 CMsgSetItemPositions

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSetItemPositions\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ItemPositions` | `IProtobufRepeatedFieldSubMessageType\<CMsgSetItemPositions_ItemPosition\>` | get | - |



---

## 🔌 CMsgSetItemPositions_ItemPosition

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSetItemPositions_ItemPosition\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `LegacyItemId` | `uint` | get, set | - |
| `Position` | `uint` | get, set | - |
| `ItemId` | `ulong` | get, set | - |



---

## 🔌 CMsgSortItems

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSortItems\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SortType` | `uint` | get, set | - |



---

## 🔌 CMsgSosSetLibraryStackFields

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSosSetLibraryStackFields\>`

**实现接口:** `INetMessage\<CMsgSosSetLibraryStackFields\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `StackHash` | `uint` | get, set | - |
| `PackedFields` | `byte[]` | get, set | - |



---

## 🔌 CMsgSosSetSoundEventParams

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSosSetSoundEventParams\>`

**实现接口:** `INetMessage\<CMsgSosSetSoundEventParams\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SoundeventGuid` | `int` | get, set | - |
| `PackedParams` | `byte[]` | get, set | - |



---

## 🔌 CMsgSosStartSoundEvent

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSosStartSoundEvent\>`

**实现接口:** `INetMessage\<CMsgSosStartSoundEvent\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SoundeventGuid` | `int` | get, set | - |
| `SoundeventHash` | `uint` | get, set | - |
| `SourceEntityIndex` | `int` | get, set | - |
| `Seed` | `int` | get, set | - |
| `PackedParams` | `byte[]` | get, set | - |
| `StartTime` | `float` | get, set | - |



---

## 🔌 CMsgSosStopSoundEvent

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSosStopSoundEvent\>`

**实现接口:** `INetMessage\<CMsgSosStopSoundEvent\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SoundeventGuid` | `int` | get, set | - |



---

## 🔌 CMsgSosStopSoundEventHash

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSosStopSoundEventHash\>`

**实现接口:** `INetMessage\<CMsgSosStopSoundEventHash\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SoundeventHash` | `uint` | get, set | - |
| `SourceEntityIndex` | `int` | get, set | - |



---

## 🔌 CMsgSource1LegacyGameEvent

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSource1LegacyGameEvent\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EventName` | `string` | get, set | - |
| `Eventid` | `int` | get, set | - |
| `Keys` | `IProtobufRepeatedFieldSubMessageType\<CMsgSource1LegacyGameEvent_key_t\>` | get | - |
| `ServerTick` | `int` | get, set | - |
| `Passthrough` | `int` | get, set | - |



---

## 🔌 CMsgSource1LegacyGameEventList

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSource1LegacyGameEventList\>`

**实现接口:** `INetMessage\<CMsgSource1LegacyGameEventList\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Descriptors` | `IProtobufRepeatedFieldSubMessageType\<CMsgSource1LegacyGameEventList_descriptor_t\>` | get | - |



---

## 🔌 CMsgSource1LegacyGameEventList_descriptor_t

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSource1LegacyGameEventList_descriptor_t\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Eventid` | `int` | get, set | - |
| `Name` | `string` | get, set | - |
| `Keys` | `IProtobufRepeatedFieldSubMessageType\<CMsgSource1LegacyGameEventList_key_t\>` | get | - |



---

## 🔌 CMsgSource1LegacyGameEventList_key_t

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSource1LegacyGameEventList_key_t\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Type` | `int` | get, set | - |
| `Name` | `string` | get, set | - |



---

## 🔌 CMsgSource1LegacyGameEvent_key_t

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSource1LegacyGameEvent_key_t\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Type` | `int` | get, set | - |
| `ValString` | `string` | get, set | - |
| `ValFloat` | `float` | get, set | - |
| `ValLong` | `int` | get, set | - |
| `ValShort` | `int` | get, set | - |
| `ValByte` | `int` | get, set | - |
| `ValBool` | `bool` | get, set | - |
| `ValUint64` | `ulong` | get, set | - |



---

## 🔌 CMsgSource1LegacyListenEvents

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSource1LegacyListenEvents\>`

**实现接口:** `INetMessage\<CMsgSource1LegacyListenEvents\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Playerslot` | `int` | get, set | - |
| `Eventarraybits` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |



---

## 🔌 CMsgSource2NetworkFlowQuality

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSource2NetworkFlowQuality\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Duration` | `uint` | get, set | - |
| `BytesTotal` | `ulong` | get, set | - |
| `BytesTotalReliable` | `ulong` | get, set | - |
| `BytesTotalVoice` | `ulong` | get, set | - |
| `BytesSecP95` | `uint` | get, set | - |
| `BytesSecP99` | `uint` | get, set | - |
| `EnginemsgsTotal` | `uint` | get, set | - |
| `EnginemsgsSecP95` | `uint` | get, set | - |
| `EnginemsgsSecP99` | `uint` | get, set | - |
| `NetframesTotal` | `uint` | get, set | - |
| `NetframesDropped` | `uint` | get, set | - |
| `NetframesOutoforder` | `uint` | get, set | - |
| `NetframesSizeExceedsMtu` | `uint` | get, set | - |
| `NetframesSizeP95` | `uint` | get, set | - |
| `NetframesSizeP99` | `uint` | get, set | - |
| `TicksTotal` | `uint` | get, set | - |
| `TicksGood` | `uint` | get, set | - |
| `TicksGoodAlmostLate` | `uint` | get, set | - |
| `TicksFixedDropped` | `uint` | get, set | - |
| `TicksFixedLate` | `uint` | get, set | - |
| `TicksBadDropped` | `uint` | get, set | - |
| `TicksBadLate` | `uint` | get, set | - |
| `TicksBadOther` | `uint` | get, set | - |
| `TickMissrateSamplesTotal` | `uint` | get, set | - |
| `TickMissrateSamplesPerfect` | `uint` | get, set | - |
| `TickMissrateSamplesPerfectnet` | `uint` | get, set | - |
| `TickMissratenetP75X10` | `uint` | get, set | - |
| `TickMissratenetP95X10` | `uint` | get, set | - |
| `TickMissratenetP99X10` | `uint` | get, set | - |
| `RecvmarginP1` | `int` | get, set | - |
| `RecvmarginP5` | `int` | get, set | - |
| `RecvmarginP25` | `int` | get, set | - |
| `RecvmarginP50` | `int` | get, set | - |
| `RecvmarginP75` | `int` | get, set | - |
| `RecvmarginP95` | `int` | get, set | - |
| `NetframeJitterP50` | `uint` | get, set | - |
| `NetframeJitterP99` | `uint` | get, set | - |
| `IntervalPeakjitterP50` | `uint` | get, set | - |
| `IntervalPeakjitterP95` | `uint` | get, set | - |
| `PacketMisdeliveryRateP50X4` | `uint` | get, set | - |
| `PacketMisdeliveryRateP95X4` | `uint` | get, set | - |
| `NetPingP5` | `uint` | get, set | - |
| `NetPingP50` | `uint` | get, set | - |
| `NetPingP95` | `uint` | get, set | - |



---

## 🔌 CMsgSource2PerfIntervalSample

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSource2PerfIntervalSample\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `FrameTimeMaxMs` | `float` | get, set | - |
| `FrameTimeAvgMs` | `float` | get, set | - |
| `FrameTimeMinMs` | `float` | get, set | - |
| `FrameCount` | `int` | get, set | - |
| `FrameTimeTotalMs` | `float` | get, set | - |
| `Tags` | `IProtobufRepeatedFieldSubMessageType\<CMsgSource2PerfIntervalSample_Tag\>` | get | - |



---

## 🔌 CMsgSource2PerfIntervalSample_Tag

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSource2PerfIntervalSample_Tag\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Tag` | `string` | get, set | - |
| `MaxValue` | `uint` | get, set | - |



---

## 🔌 CMsgSource2SystemSpecs

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSource2SystemSpecs\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CpuId` | `string` | get, set | - |
| `CpuBrand` | `string` | get, set | - |
| `CpuModel` | `uint` | get, set | - |
| `CpuNumPhysical` | `uint` | get, set | - |
| `RamPhysicalTotalMb` | `uint` | get, set | - |
| `GpuRendersystemDllName` | `string` | get, set | - |
| `GpuVendorId` | `uint` | get, set | - |
| `GpuDriverName` | `string` | get, set | - |
| `GpuDriverVersionHigh` | `uint` | get, set | - |
| `GpuDriverVersionLow` | `uint` | get, set | - |
| `GpuDxSupportLevel` | `uint` | get, set | - |
| `GpuTextureMemorySizeMb` | `uint` | get, set | - |
| `BackbufferWidth` | `uint` | get, set | - |
| `BackbufferHeight` | `uint` | get, set | - |



---

## 🔌 CMsgSource2VProfLiteReport

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSource2VProfLiteReport\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Total` | `CMsgSource2VProfLiteReportItem` | get | - |
| `Items` | `IProtobufRepeatedFieldSubMessageType\<CMsgSource2VProfLiteReportItem\>` | get | - |
| `DiscardedFrames` | `uint` | get, set | - |



---

## 🔌 CMsgSource2VProfLiteReportItem

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSource2VProfLiteReportItem\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | get, set | - |
| `ActiveSamples` | `uint` | get, set | - |
| `ActiveSamples1secmax` | `uint` | get, set | - |
| `UsecMax` | `uint` | get, set | - |
| `UsecAvgActive` | `uint` | get, set | - |
| `UsecP50Active` | `uint` | get, set | - |
| `UsecP99Active` | `uint` | get, set | - |
| `UsecAvgAll` | `uint` | get, set | - |
| `UsecP50All` | `uint` | get, set | - |
| `UsecP99All` | `uint` | get, set | - |
| `Usec1secmaxAvgActive` | `uint` | get, set | - |
| `Usec1secmaxP50Active` | `uint` | get, set | - |
| `Usec1secmaxP95Active` | `uint` | get, set | - |
| `Usec1secmaxP99Active` | `uint` | get, set | - |
| `Usec1secmaxAvgAll` | `uint` | get, set | - |
| `Usec1secmaxP50All` | `uint` | get, set | - |
| `Usec1secmaxP95All` | `uint` | get, set | - |
| `Usec1secmaxP99All` | `uint` | get, set | - |



---

## 🔌 CMsgStoreGetUserData

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgStoreGetUserData\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PriceSheetVersion` | `uint` | get, set | - |
| `Currency` | `int` | get, set | - |



---

## 🔌 CMsgStoreGetUserDataResponse

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgStoreGetUserDataResponse\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Result` | `int` | get, set | - |
| `CurrencyDeprecated` | `int` | get, set | - |
| `CountryDeprecated` | `string` | get, set | - |
| `PriceSheetVersion` | `uint` | get, set | - |
| `PriceSheet` | `byte[]` | get, set | - |



---

## 🔌 CMsgSystemBroadcast

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgSystemBroadcast\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Message` | `string` | get, set | - |



---

## 🔌 CMsgTEArmorRicochet

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTEArmorRicochet\>`

**实现接口:** `INetMessage\<CMsgTEArmorRicochet\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Pos` | `Vector` | get, set | - |
| `Dir` | `Vector` | get, set | - |



---

## 🔌 CMsgTEBaseBeam

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTEBaseBeam\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Modelindex` | `ulong` | get, set | - |
| `Haloindex` | `ulong` | get, set | - |
| `Startframe` | `uint` | get, set | - |
| `Framerate` | `uint` | get, set | - |
| `Life` | `float` | get, set | - |
| `Width` | `float` | get, set | - |
| `Endwidth` | `float` | get, set | - |
| `Fadelength` | `uint` | get, set | - |
| `Amplitude` | `float` | get, set | - |
| `Color` | `uint` | get, set | - |
| `Speed` | `uint` | get, set | - |
| `Flags` | `uint` | get, set | - |



---

## 🔌 CMsgTEBeamEntPoint

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTEBeamEntPoint\>`

**实现接口:** `INetMessage\<CMsgTEBeamEntPoint\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Base` | `CMsgTEBaseBeam` | get | - |
| `Startentity` | `uint` | get, set | - |
| `Endentity` | `uint` | get, set | - |
| `Start` | `Vector` | get, set | - |
| `End` | `Vector` | get, set | - |



---

## 🔌 CMsgTEBeamEnts

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTEBeamEnts\>`

**实现接口:** `INetMessage\<CMsgTEBeamEnts\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Base` | `CMsgTEBaseBeam` | get | - |
| `Startentity` | `uint` | get, set | - |
| `Endentity` | `uint` | get, set | - |



---

## 🔌 CMsgTEBeamPoints

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTEBeamPoints\>`

**实现接口:** `INetMessage\<CMsgTEBeamPoints\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Base` | `CMsgTEBaseBeam` | get | - |
| `Start` | `Vector` | get, set | - |
| `End` | `Vector` | get, set | - |



---

## 🔌 CMsgTEBeamRing

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTEBeamRing\>`

**实现接口:** `INetMessage\<CMsgTEBeamRing\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Base` | `CMsgTEBaseBeam` | get | - |
| `Startentity` | `uint` | get, set | - |
| `Endentity` | `uint` | get, set | - |



---

## 🔌 CMsgTEBloodStream

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTEBloodStream\>`

**实现接口:** `INetMessage\<CMsgTEBloodStream\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Origin` | `Vector` | get, set | - |
| `Direction` | `Vector` | get, set | - |
| `Color` | `uint` | get, set | - |
| `Amount` | `uint` | get, set | - |



---

## 🔌 CMsgTEBubbleTrail

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTEBubbleTrail\>`

**实现接口:** `INetMessage\<CMsgTEBubbleTrail\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Mins` | `Vector` | get, set | - |
| `Maxs` | `Vector` | get, set | - |
| `Waterz` | `float` | get, set | - |
| `Count` | `uint` | get, set | - |
| `Speed` | `float` | get, set | - |



---

## 🔌 CMsgTEBubbles

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTEBubbles\>`

**实现接口:** `INetMessage\<CMsgTEBubbles\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Mins` | `Vector` | get, set | - |
| `Maxs` | `Vector` | get, set | - |
| `Height` | `float` | get, set | - |
| `Count` | `uint` | get, set | - |
| `Speed` | `float` | get, set | - |



---

## 🔌 CMsgTEDecal

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTEDecal\>`

**实现接口:** `INetMessage\<CMsgTEDecal\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Origin` | `Vector` | get, set | - |
| `Start` | `Vector` | get, set | - |
| `Entity` | `int` | get, set | - |
| `Hitbox` | `uint` | get, set | - |
| `Index` | `uint` | get, set | - |



---

## 🔌 CMsgTEDust

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTEDust\>`

**实现接口:** `INetMessage\<CMsgTEDust\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Origin` | `Vector` | get, set | - |
| `Size` | `float` | get, set | - |
| `Speed` | `float` | get, set | - |
| `Direction` | `Vector` | get, set | - |



---

## 🔌 CMsgTEEffectDispatch

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTEEffectDispatch\>`

**实现接口:** `INetMessage\<CMsgTEEffectDispatch\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Effectdata` | `CMsgEffectData` | get | - |



---

## 🔌 CMsgTEEnergySplash

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTEEnergySplash\>`

**实现接口:** `INetMessage\<CMsgTEEnergySplash\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Pos` | `Vector` | get, set | - |
| `Dir` | `Vector` | get, set | - |
| `Explosive` | `bool` | get, set | - |



---

## 🔌 CMsgTEExplosion

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTEExplosion\>`

**实现接口:** `INetMessage\<CMsgTEExplosion\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Origin` | `Vector` | get, set | - |
| `Flags` | `uint` | get, set | - |
| `Normal` | `Vector` | get, set | - |
| `Radius` | `uint` | get, set | - |
| `Magnitude` | `uint` | get, set | - |
| `AffectRagdolls` | `bool` | get, set | - |
| `SoundName` | `string` | get, set | - |
| `ExplosionType` | `uint` | get, set | - |
| `CreateDebris` | `bool` | get, set | - |
| `DebrisOrigin` | `Vector` | get, set | - |
| `DebrisSurfaceprop` | `uint` | get, set | - |



---

## 🔌 CMsgTEFireBullets

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTEFireBullets\>`

**实现接口:** `INetMessage\<CMsgTEFireBullets\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Origin` | `Vector` | get, set | - |
| `Angles` | `QAngle` | get, set | - |
| `WeaponId` | `uint` | get, set | - |
| `Mode` | `uint` | get, set | - |
| `Seed` | `uint` | get, set | - |
| `Player` | `uint` | get, set | - |
| `Inaccuracy` | `float` | get, set | - |
| `RecoilIndex` | `float` | get, set | - |
| `Spread` | `float` | get, set | - |
| `SoundType` | `int` | get, set | - |
| `ItemDefIndex` | `uint` | get, set | - |
| `SoundDspEffect` | `uint` | get, set | - |
| `EntOrigin` | `Vector` | get, set | - |
| `NumBulletsRemaining` | `uint` | get, set | - |
| `AttackType` | `uint` | get, set | - |
| `PlayerInair` | `bool` | get, set | - |
| `PlayerScoped` | `bool` | get, set | - |
| `Tick` | `int` | get, set | - |
| `Extra` | `CMsgTEFireBullets_Extra` | get | - |



---

## 🔌 CMsgTEFireBullets_Extra

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTEFireBullets_Extra\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AimPunch` | `QAngle` | get, set | - |
| `AttackTickCount` | `int` | get, set | - |
| `AttackTickFrac` | `float` | get, set | - |
| `RenderTickCount` | `int` | get, set | - |
| `RenderTickFrac` | `float` | get, set | - |
| `InaccuracyMove` | `float` | get, set | - |
| `InaccuracyAir` | `float` | get, set | - |
| `Type` | `int` | get, set | - |



---

## 🔌 CMsgTEFizz

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTEFizz\>`

**实现接口:** `INetMessage\<CMsgTEFizz\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Entity` | `int` | get, set | - |
| `Density` | `uint` | get, set | - |
| `Current` | `int` | get, set | - |



---

## 🔌 CMsgTEGlowSprite

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTEGlowSprite\>`

**实现接口:** `INetMessage\<CMsgTEGlowSprite\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Origin` | `Vector` | get, set | - |
| `Scale` | `float` | get, set | - |
| `Life` | `float` | get, set | - |
| `Brightness` | `uint` | get, set | - |



---

## 🔌 CMsgTEImpact

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTEImpact\>`

**实现接口:** `INetMessage\<CMsgTEImpact\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Origin` | `Vector` | get, set | - |
| `Normal` | `Vector` | get, set | - |
| `Type` | `uint` | get, set | - |



---

## 🔌 CMsgTELargeFunnel

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTELargeFunnel\>`

**实现接口:** `INetMessage\<CMsgTELargeFunnel\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Origin` | `Vector` | get, set | - |
| `Reversed` | `uint` | get, set | - |



---

## 🔌 CMsgTEMuzzleFlash

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTEMuzzleFlash\>`

**实现接口:** `INetMessage\<CMsgTEMuzzleFlash\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Origin` | `Vector` | get, set | - |
| `Angles` | `QAngle` | get, set | - |
| `Scale` | `float` | get, set | - |
| `Type` | `uint` | get, set | - |



---

## 🔌 CMsgTEPhysicsProp

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTEPhysicsProp\>`

**实现接口:** `INetMessage\<CMsgTEPhysicsProp\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Origin` | `Vector` | get, set | - |
| `Velocity` | `Vector` | get, set | - |
| `Angles` | `QAngle` | get, set | - |
| `Skin` | `uint` | get, set | - |
| `Flags` | `uint` | get, set | - |
| `Effects` | `uint` | get, set | - |
| `Color` | `uint` | get, set | - |
| `Modelindex` | `ulong` | get, set | - |
| `UnusedBreakmodelsnottomake` | `uint` | get, set | - |
| `Scale` | `float` | get, set | - |
| `Dmgpos` | `Vector` | get, set | - |
| `Dmgdir` | `Vector` | get, set | - |
| `Dmgtype` | `int` | get, set | - |



---

## 🔌 CMsgTEPlayerAnimEvent

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTEPlayerAnimEvent\>`

**实现接口:** `INetMessage\<CMsgTEPlayerAnimEvent\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Player` | `uint` | get, set | - |
| `Event` | `uint` | get, set | - |
| `Data` | `int` | get, set | - |



---

## 🔌 CMsgTERadioIcon

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTERadioIcon\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Player` | `uint` | get, set | - |



---

## 🔌 CMsgTEShatterSurface

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTEShatterSurface\>`

**实现接口:** `INetMessage\<CMsgTEShatterSurface\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Origin` | `Vector` | get, set | - |
| `Angles` | `QAngle` | get, set | - |
| `Force` | `Vector` | get, set | - |
| `Forcepos` | `Vector` | get, set | - |
| `Width` | `float` | get, set | - |
| `Height` | `float` | get, set | - |
| `Shardsize` | `float` | get, set | - |
| `Surfacetype` | `uint` | get, set | - |
| `Frontcolor` | `uint` | get, set | - |
| `Backcolor` | `uint` | get, set | - |



---

## 🔌 CMsgTESmoke

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTESmoke\>`

**实现接口:** `INetMessage\<CMsgTESmoke\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Origin` | `Vector` | get, set | - |
| `Scale` | `float` | get, set | - |



---

## 🔌 CMsgTESparks

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTESparks\>`

**实现接口:** `INetMessage\<CMsgTESparks\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Origin` | `Vector` | get, set | - |
| `Magnitude` | `uint` | get, set | - |
| `Length` | `uint` | get, set | - |
| `Direction` | `Vector` | get, set | - |



---

## 🔌 CMsgTEWorldDecal

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTEWorldDecal\>`

**实现接口:** `INetMessage\<CMsgTEWorldDecal\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Origin` | `Vector` | get, set | - |
| `Normal` | `Vector` | get, set | - |
| `Index` | `uint` | get, set | - |



---

## 🔌 CMsgTransform

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgTransform\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Position` | `Vector` | get, set | - |
| `Scale` | `float` | get, set | - |
| `Orientation` | `CMsgQuaternion` | get | - |



---

## 🔌 CMsgUpdateItemSchema

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgUpdateItemSchema\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ItemsGame` | `byte[]` | get, set | - |
| `ItemSchemaVersion` | `uint` | get, set | - |
| `ItemsGameUrl` | `string` | get, set | - |



---

## 🔌 CMsgUseItem

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgUseItem\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ItemId` | `ulong` | get, set | - |
| `TargetSteamId` | `ulong` | get, set | - |
| `GiftPotentialTargets` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `DuelClassLock` | `uint` | get, set | - |
| `InitiatorSteamId` | `ulong` | get, set | - |



---

## 🔌 CMsgVDebugGameSessionIDEvent

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgVDebugGameSessionIDEvent\>`

**实现接口:** `INetMessage\<CMsgVDebugGameSessionIDEvent\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Clientid` | `int` | get, set | - |
| `Gamesessionid` | `string` | get, set | - |



---

## 🔌 CMsgVector

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgVector\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `X` | `float` | get, set | - |
| `Y` | `float` | get, set | - |
| `Z` | `float` | get, set | - |
| `W` | `float` | get, set | - |



---

## 🔌 CMsgVector2D

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgVector2D\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `X` | `float` | get, set | - |
| `Y` | `float` | get, set | - |



---

## 🔌 CMsgVoiceAudio

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgVoiceAudio\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Format` | `VoiceDataFormat_t` | get, set | - |
| `VoiceData` | `byte[]` | get, set | - |
| `SequenceBytes` | `int` | get, set | - |
| `SectionNumber` | `uint` | get, set | - |
| `SampleRate` | `uint` | get, set | - |
| `UncompressedSampleOffset` | `uint` | get, set | - |
| `NumPackets` | `uint` | get, set | - |
| `PacketOffsets` | `IProtobufRepeatedFieldValueType\<uint\>` | get, set | - |
| `VoiceLevel` | `float` | get, set | - |



---

## 🔌 CMsg_CVars

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsg_CVars\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Cvars` | `IProtobufRepeatedFieldSubMessageType\<CMsg_CVars_CVar\>` | get | - |



---

## 🔌 CMsg_CVars_CVar

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsg_CVars_CVar\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | get, set | - |
| `Value` | `string` | get, set | - |



---

## 🔌 CNETMsg_DebugOverlay

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CNETMsg_DebugOverlay\>`

**实现接口:** `INetMessage\<CNETMsg_DebugOverlay\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Etype` | `int` | get, set | - |
| `Vectors` | `IProtobufRepeatedFieldValueType\<Vector\>` | get | - |
| `Colors` | `IProtobufRepeatedFieldValueType\<Color\>` | get | - |
| `Dimensions` | `IProtobufRepeatedFieldValueType\<float\>` | get | - |
| `Times` | `IProtobufRepeatedFieldValueType\<float\>` | get | - |
| `Bools` | `IProtobufRepeatedFieldValueType\<bool\>` | get | - |
| `Uint64s` | `IProtobufRepeatedFieldValueType\<ulong\>` | get | - |
| `Strings` | `IProtobufRepeatedFieldValueType\<string\>` | get | - |



---

## 🔌 CNETMsg_NOP

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CNETMsg_NOP\>`

**实现接口:** `INetMessage\<CNETMsg_NOP\>`, `IDisposable`



---

## 🔌 CNETMsg_SetConVar

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CNETMsg_SetConVar\>`

**实现接口:** `INetMessage\<CNETMsg_SetConVar\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Convars` | `CMsg_CVars` | get | - |



---

## 🔌 CNETMsg_SignonState

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CNETMsg_SignonState\>`

**实现接口:** `INetMessage\<CNETMsg_SignonState\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SignonState` | `SignonState_t` | get, set | - |
| `SpawnCount` | `uint` | get, set | - |
| `NumServerPlayers` | `uint` | get, set | - |
| `PlayersNetworkids` | `IProtobufRepeatedFieldValueType\<string\>` | get | - |
| `MapName` | `string` | get, set | - |
| `Addons` | `string` | get, set | - |



---

## 🔌 CNETMsg_SpawnGroup_Load

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CNETMsg_SpawnGroup_Load\>`

**实现接口:** `INetMessage\<CNETMsg_SpawnGroup_Load\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Worldname` | `string` | get, set | - |
| `Entitylumpname` | `string` | get, set | - |
| `Entityfiltername` | `string` | get, set | - |
| `Spawngrouphandle` | `uint` | get, set | - |
| `Spawngroupownerhandle` | `uint` | get, set | - |
| `WorldOffsetPos` | `Vector` | get, set | - |
| `WorldOffsetAngle` | `QAngle` | get, set | - |
| `Spawngroupmanifest` | `byte[]` | get, set | - |
| `Flags` | `uint` | get, set | - |
| `Tickcount` | `int` | get, set | - |
| `Manifestincomplete` | `bool` | get, set | - |
| `Localnamefixup` | `string` | get, set | - |
| `Parentnamefixup` | `string` | get, set | - |
| `Manifestloadpriority` | `int` | get, set | - |
| `Worldgroupid` | `uint` | get, set | - |
| `Creationsequence` | `uint` | get, set | - |
| `Savegamefilename` | `string` | get, set | - |
| `Spawngroupparenthandle` | `uint` | get, set | - |
| `Leveltransition` | `bool` | get, set | - |
| `Worldgroupname` | `string` | get, set | - |



---

## 🔌 CNETMsg_SpawnGroup_LoadCompleted

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CNETMsg_SpawnGroup_LoadCompleted\>`

**实现接口:** `INetMessage\<CNETMsg_SpawnGroup_LoadCompleted\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Spawngrouphandle` | `uint` | get, set | - |



---

## 🔌 CNETMsg_SpawnGroup_ManifestUpdate

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CNETMsg_SpawnGroup_ManifestUpdate\>`

**实现接口:** `INetMessage\<CNETMsg_SpawnGroup_ManifestUpdate\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Spawngrouphandle` | `uint` | get, set | - |
| `Spawngroupmanifest` | `byte[]` | get, set | - |
| `Manifestincomplete` | `bool` | get, set | - |



---

## 🔌 CNETMsg_SpawnGroup_SetCreationTick

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CNETMsg_SpawnGroup_SetCreationTick\>`

**实现接口:** `INetMessage\<CNETMsg_SpawnGroup_SetCreationTick\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Spawngrouphandle` | `uint` | get, set | - |
| `Tickcount` | `int` | get, set | - |
| `Creationsequence` | `uint` | get, set | - |



---

## 🔌 CNETMsg_SpawnGroup_Unload

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CNETMsg_SpawnGroup_Unload\>`

**实现接口:** `INetMessage\<CNETMsg_SpawnGroup_Unload\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Spawngrouphandle` | `uint` | get, set | - |
| `Flags` | `uint` | get, set | - |
| `Tickcount` | `int` | get, set | - |



---

## 🔌 CNETMsg_SplitScreenUser

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CNETMsg_SplitScreenUser\>`

**实现接口:** `INetMessage\<CNETMsg_SplitScreenUser\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Slot` | `int` | get, set | - |



---

## 🔌 CNETMsg_StringCmd

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CNETMsg_StringCmd\>`

**实现接口:** `INetMessage\<CNETMsg_StringCmd\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Command` | `string` | get, set | - |
| `PredictionSync` | `uint` | get, set | - |



---

## 🔌 CNETMsg_Tick

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CNETMsg_Tick\>`

**实现接口:** `INetMessage\<CNETMsg_Tick\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Tick` | `uint` | get, set | - |
| `HostComputationtime` | `uint` | get, set | - |
| `HostComputationtimeStdDeviation` | `uint` | get, set | - |
| `LegacyHostLoss` | `uint` | get, set | - |
| `HostUnfilteredFrametime` | `uint` | get, set | - |
| `HltvReplayFlags` | `uint` | get, set | - |
| `ExpectedLongTick` | `uint` | get, set | - |
| `ExpectedLongTickReason` | `string` | get, set | - |
| `HostFrameDroppedPctX10` | `uint` | get, set | - |
| `HostFrameIrregularArrivalPctX10` | `uint` | get, set | - |



---

## 🔌 CP2P_Ping

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CP2P_Ping\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SendTime` | `ulong` | get, set | - |
| `IsReply` | `bool` | get, set | - |



---

## 🔌 CP2P_TextMessage

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CP2P_TextMessage\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Text` | `byte[]` | get, set | - |



---

## 🔌 CP2P_VRAvatarPosition

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CP2P_VRAvatarPosition\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `BodyParts` | `IProtobufRepeatedFieldSubMessageType\<CP2P_VRAvatarPosition_COrientation\>` | get | - |
| `HatId` | `int` | get, set | - |
| `SceneId` | `int` | get, set | - |
| `WorldScale` | `int` | get, set | - |



---

## 🔌 CP2P_VRAvatarPosition_COrientation

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CP2P_VRAvatarPosition_COrientation\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Pos` | `Vector` | get, set | - |
| `Ang` | `QAngle` | get, set | - |



---

## 🔌 CP2P_Voice

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CP2P_Voice\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Audio` | `CMsgVoiceAudio` | get | - |
| `BroadcastGroup` | `uint` | get, set | - |



---

## 📋 CP2P_Voice_Handler_Flags

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `Played_Audio` | `1` | - |



---

## 🔌 CP2P_WatchSynchronization

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CP2P_WatchSynchronization\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `DemoTick` | `int` | get, set | - |
| `Paused` | `bool` | get, set | - |
| `TvListenVoiceIndices` | `ulong` | get, set | - |
| `DotaSpectatorMode` | `int` | get, set | - |
| `DotaSpectatorWatchingBroadcaster` | `bool` | get, set | - |
| `DotaSpectatorHeroIndex` | `int` | get, set | - |
| `DotaSpectatorAutospeed` | `int` | get, set | - |
| `DotaReplaySpeed` | `int` | get, set | - |



---

## 🔌 CPreMatchInfoData

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CPreMatchInfoData\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PredictionsPct` | `int` | get, set | - |
| `Draft` | `CDataGCCStrike15_v2_TournamentMatchDraft` | get | - |
| `Stats` | `IProtobufRepeatedFieldSubMessageType\<CPreMatchInfoData_TeamStats\>` | get | - |
| `Wins` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |



---

## 🔌 CPreMatchInfoData_TeamStats

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CPreMatchInfoData_TeamStats\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MatchInfoIdxtxt` | `int` | get, set | - |
| `MatchInfoTxt` | `string` | get, set | - |
| `MatchInfoTeams` | `IProtobufRepeatedFieldValueType\<string\>` | get | - |



---

## 🔌 CPredictionEvent_Diagnostic

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CPredictionEvent_Diagnostic\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Id` | `uint` | get, set | - |
| `RequestedSync` | `uint` | get, set | - |
| `RequestedPlayerIndex` | `uint` | get, set | - |
| `ExecutionSync` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |



---

## 🔌 CPredictionEvent_StringCommand

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CPredictionEvent_StringCommand\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Command` | `string` | get, set | - |



---

## 🔌 CPredictionEvent_Teleport

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CPredictionEvent_Teleport\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Origin` | `Vector` | get, set | - |
| `Angles` | `QAngle` | get, set | - |
| `DropToGroundRange` | `float` | get, set | - |



---

## 🔌 CProductInfo_SetRichPresenceLocalization_Request

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CProductInfo_SetRichPresenceLocalization_Request\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Appid` | `uint` | get, set | - |
| `Languages` | `IProtobufRepeatedFieldSubMessageType\<CProductInfo_SetRichPresenceLocalization_Request_LanguageSection\>` | get | - |
| `Steamid` | `ulong` | get, set | - |



---

## 🔌 CProductInfo_SetRichPresenceLocalization_Request_LanguageSection

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CProductInfo_SetRichPresenceLocalization_Request_LanguageSection\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Language` | `string` | get, set | - |
| `Tokens` | `IProtobufRepeatedFieldSubMessageType\<CProductInfo_SetRichPresenceLocalization_Request_Token\>` | get | - |



---

## 🔌 CProductInfo_SetRichPresenceLocalization_Request_Token

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CProductInfo_SetRichPresenceLocalization_Request_Token\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Token` | `string` | get, set | - |
| `Value` | `string` | get, set | - |



---

## 🔌 CProductInfo_SetRichPresenceLocalization_Response

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CProductInfo_SetRichPresenceLocalization_Response\>`



---

## 🔌 CQuest_PublisherAddCommunityItemsToPlayer_Request

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CQuest_PublisherAddCommunityItemsToPlayer_Request\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Steamid` | `ulong` | get, set | - |
| `Appid` | `uint` | get, set | - |
| `MatchItemType` | `uint` | get, set | - |
| `MatchItemClass` | `uint` | get, set | - |
| `PrefixItemName` | `string` | get, set | - |
| `Attributes` | `IProtobufRepeatedFieldSubMessageType\<CQuest_PublisherAddCommunityItemsToPlayer_Request_Attribute\>` | get | - |
| `Note` | `string` | get, set | - |



---

## 🔌 CQuest_PublisherAddCommunityItemsToPlayer_Request_

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`



---

## 🔌 CQuest_PublisherAddCommunityItemsToPlayer_Response

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CQuest_PublisherAddCommunityItemsToPlayer_Response\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ItemsMatched` | `uint` | get, set | - |
| `ItemsGranted` | `uint` | get, set | - |



---

## 🔌 CSGOInputHistoryEntryPB

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSGOInputHistoryEntryPB\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ViewAngles` | `QAngle` | get, set | - |
| `RenderTickCount` | `int` | get, set | - |
| `RenderTickFraction` | `float` | get, set | - |
| `PlayerTickCount` | `int` | get, set | - |
| `PlayerTickFraction` | `float` | get, set | - |
| `ClInterp` | `CSGOInterpolationInfoPB_CL` | get | - |
| `SvInterp0` | `CSGOInterpolationInfoPB` | get | - |
| `SvInterp1` | `CSGOInterpolationInfoPB` | get | - |
| `PlayerInterp` | `CSGOInterpolationInfoPB` | get | - |
| `FrameNumber` | `int` | get, set | - |
| `TargetEntIndex` | `int` | get, set | - |
| `ShootPosition` | `Vector` | get, set | - |
| `TargetHeadPosCheck` | `Vector` | get, set | - |
| `TargetAbsPosCheck` | `Vector` | get, set | - |
| `TargetAbsAngCheck` | `QAngle` | get, set | - |



---

## 🔌 CSGOInterpolationInfoPB

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSGOInterpolationInfoPB\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SrcTick` | `int` | get, set | - |
| `DstTick` | `int` | get, set | - |
| `Frac` | `float` | get, set | - |



---

## 🔌 CSGOInterpolationInfoPB_CL

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSGOInterpolationInfoPB_CL\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Frac` | `float` | get, set | - |



---

## 🔌 CSGOUserCmdPB

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSGOUserCmdPB\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Base` | `CBaseUserCmdPB` | get | - |
| `InputHistory` | `IProtobufRepeatedFieldSubMessageType\<CSGOInputHistoryEntryPB\>` | get | - |
| `Attack1StartHistoryIndex` | `int` | get, set | - |
| `Attack2StartHistoryIndex` | `int` | get, set | - |
| `LeftHandDesired` | `bool` | get, set | - |
| `IsPredictingBodyShotFx` | `bool` | get, set | - |
| `IsPredictingHeadShotFx` | `bool` | get, set | - |
| `IsPredictingKillRagdolls` | `bool` | get, set | - |



---

## 🔌 CSOAccountItemPersonalStore

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOAccountItemPersonalStore\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `GenerationTime` | `uint` | get, set | - |
| `RedeemableBalance` | `uint` | get, set | - |
| `Items` | `IProtobufRepeatedFieldValueType\<ulong\>` | get | - |



---

## 🔌 CSOAccountKeychainRemoveToolCharges

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOAccountKeychainRemoveToolCharges\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Charges` | `uint` | get, set | - |



---

## 🔌 CSOAccountRecurringMission

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOAccountRecurringMission\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AccountId` | `uint` | get, set | - |
| `MissionId` | `uint` | get, set | - |
| `Period` | `uint` | get, set | - |
| `Progress` | `uint` | get, set | - |



---

## 🔌 CSOAccountRecurringSubscription

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOAccountRecurringSubscription\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TimeNextCycle` | `uint` | get, set | - |
| `TimeInitiated` | `uint` | get, set | - |



---

## 🔌 CSOAccountSeasonalOperation

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOAccountSeasonalOperation\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SeasonValue` | `uint` | get, set | - |
| `TierUnlocked` | `uint` | get, set | - |
| `PremiumTiers` | `uint` | get, set | - |
| `MissionId` | `uint` | get, set | - |
| `MissionsCompleted` | `uint` | get, set | - |
| `RedeemableBalance` | `uint` | get, set | - |
| `SeasonPassTime` | `uint` | get, set | - |



---

## 🔌 CSOAccountXpShop

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOAccountXpShop\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `GenerationTime` | `uint` | get, set | - |
| `RedeemableBalance` | `uint` | get, set | - |
| `XpTracks` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |



---

## 🔌 CSOAccountXpShopBids

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOAccountXpShopBids\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CampaignId` | `uint` | get, set | - |
| `RedeemId` | `uint` | get, set | - |
| `ExpectedCost` | `uint` | get, set | - |
| `GenerationTime` | `uint` | get, set | - |



---

## 🔌 CSOEconClaimCode

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOEconClaimCode\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AccountId` | `uint` | get, set | - |
| `CodeType` | `uint` | get, set | - |
| `TimeAcquired` | `uint` | get, set | - |
| `Code` | `string` | get, set | - |



---

## 🔌 CSOEconCoupon

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOEconCoupon\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Entryid` | `uint` | get, set | - |
| `Defidx` | `uint` | get, set | - |
| `ExpirationDate` | `uint` | get, set | - |



---

## 🔌 CSOEconEquipSlot

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOEconEquipSlot\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AccountId` | `uint` | get, set | - |
| `ClassId` | `uint` | get, set | - |
| `SlotId` | `uint` | get, set | - |
| `ItemId` | `ulong` | get, set | - |
| `ItemDefinition` | `uint` | get, set | - |



---

## 🔌 CSOEconGameAccountClient

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOEconGameAccountClient\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AdditionalBackpackSlots` | `uint` | get, set | - |
| `TradeBanExpiration` | `uint` | get, set | - |
| `BonusXpTimestampRefresh` | `uint` | get, set | - |
| `BonusXpUsedflags` | `uint` | get, set | - |
| `ElevatedState` | `uint` | get, set | - |
| `ElevatedTimestamp` | `uint` | get, set | - |



---

## 🔌 CSOEconItem

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOEconItem\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Id` | `ulong` | get, set | - |
| `AccountId` | `uint` | get, set | - |
| `Inventory` | `uint` | get, set | - |
| `DefIndex` | `uint` | get, set | - |
| `Quantity` | `uint` | get, set | - |
| `Level` | `uint` | get, set | - |
| `Quality` | `uint` | get, set | - |
| `Flags` | `uint` | get, set | - |
| `Origin` | `uint` | get, set | - |
| `CustomName` | `string` | get, set | - |
| `CustomDesc` | `string` | get, set | - |
| `Attribute` | `IProtobufRepeatedFieldSubMessageType\<CSOEconItemAttribute\>` | get | - |
| `InteriorItem` | `CSOEconItem` | get | - |
| `InUse` | `bool` | get, set | - |
| `Style` | `uint` | get, set | - |
| `OriginalId` | `ulong` | get, set | - |
| `EquippedState` | `IProtobufRepeatedFieldSubMessageType\<CSOEconItemEquipped\>` | get | - |
| `Rarity` | `uint` | get, set | - |



---

## 🔌 CSOEconItem

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`



---

## 🔌 CSOEconItemDropRateBonus

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOEconItemDropRateBonus\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AccountId` | `uint` | get, set | - |
| `ExpirationDate` | `uint` | get, set | - |
| `Bonus` | `float` | get, set | - |
| `BonusCount` | `uint` | get, set | - |
| `ItemId` | `ulong` | get, set | - |
| `DefIndex` | `uint` | get, set | - |



---

## 🔌 CSOEconItemEquipped

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOEconItemEquipped\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `NewClass` | `uint` | get, set | - |
| `NewSlot` | `uint` | get, set | - |



---

## 🔌 CSOEconItemEventTicket

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOEconItemEventTicket\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AccountId` | `uint` | get, set | - |
| `EventId` | `uint` | get, set | - |
| `ItemId` | `ulong` | get, set | - |



---

## 🔌 CSOEconItemLeagueViewPass

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOEconItemLeagueViewPass\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AccountId` | `uint` | get, set | - |
| `LeagueId` | `uint` | get, set | - |
| `Admin` | `uint` | get, set | - |
| `Itemindex` | `uint` | get, set | - |



---

## 🔌 CSOEconRentalHistory

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOEconRentalHistory\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AccountId` | `uint` | get, set | - |
| `CrateItemId` | `ulong` | get, set | - |
| `CrateDefIndex` | `uint` | get, set | - |
| `IssueDate` | `uint` | get, set | - |
| `ExpirationDate` | `uint` | get, set | - |



---

## 🔌 CSOGameAccountSteamChina

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOGameAccountSteamChina\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TimeLastUpdate` | `uint` | get, set | - |
| `TimeCommsBan` | `uint` | get, set | - |
| `TimePlayBan` | `uint` | get, set | - |



---

## 🔌 CSOItemCriteria

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOItemCriteria\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ItemLevel` | `uint` | get, set | - |
| `ItemQuality` | `int` | get, set | - |
| `ItemLevelSet` | `bool` | get, set | - |
| `ItemQualitySet` | `bool` | get, set | - |
| `InitialInventory` | `uint` | get, set | - |
| `InitialQuantity` | `uint` | get, set | - |
| `IgnoreEnabledFlag` | `bool` | get, set | - |
| `Conditions` | `IProtobufRepeatedFieldSubMessageType\<CSOItemCriteriaCondition\>` | get | - |
| `ItemRarity` | `int` | get, set | - |
| `ItemRaritySet` | `bool` | get, set | - |
| `RecentOnly` | `bool` | get, set | - |



---

## 🔌 CSOItemCriteriaCondition

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOItemCriteriaCondition\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Op` | `int` | get, set | - |
| `Field` | `string` | get, set | - |
| `Required` | `bool` | get, set | - |
| `FloatValue` | `float` | get, set | - |
| `StringValue` | `string` | get, set | - |



---

## 🔌 CSOItemRecipe

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOItemRecipe\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `DefIndex` | `uint` | get, set | - |
| `Name` | `string` | get, set | - |
| `NA` | `string` | get, set | - |
| `DescInputs` | `string` | get, set | - |
| `DescOutputs` | `string` | get, set | - |
| `DiA` | `string` | get, set | - |
| `DiB` | `string` | get, set | - |
| `DiC` | `string` | get, set | - |
| `DoA` | `string` | get, set | - |
| `DoB` | `string` | get, set | - |
| `DoC` | `string` | get, set | - |
| `RequiresAllSameClass` | `bool` | get, set | - |
| `RequiresAllSameSlot` | `bool` | get, set | - |
| `ClassUsageForOutput` | `int` | get, set | - |
| `SlotUsageForOutput` | `int` | get, set | - |
| `SetForOutput` | `int` | get, set | - |
| `InputItemsCriteria` | `IProtobufRepeatedFieldSubMessageType\<CSOItemCriteria\>` | get | - |
| `OutputItemsCriteria` | `IProtobufRepeatedFieldSubMessageType\<CSOItemCriteria\>` | get | - |
| `InputItemDupeCounts` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |



---

## 🔌 CSOLobbyInvite

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOLobbyInvite\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `GroupId` | `ulong` | get, set | - |
| `SenderId` | `ulong` | get, set | - |
| `SenderName` | `string` | get, set | - |



---

## 🔌 CSOPartyInvite

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOPartyInvite\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `GroupId` | `ulong` | get, set | - |
| `SenderId` | `ulong` | get, set | - |
| `SenderName` | `string` | get, set | - |



---

## 🔌 CSOPersonaDataPublic

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOPersonaDataPublic\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlayerLevel` | `int` | get, set | - |
| `Commendation` | `PlayerCommendationInfo` | get | - |
| `ElevatedState` | `bool` | get, set | - |
| `XpTrailTimestampRefresh` | `uint` | get, set | - |
| `XpTrailLevel` | `uint` | get, set | - |



---

## 🔌 CSOQuestProgress

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOQuestProgress\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Questid` | `uint` | get, set | - |
| `PointsRemaining` | `uint` | get, set | - |
| `BonusPoints` | `uint` | get, set | - |



---

## 🔌 CSOVolatileItemClaimedRewards

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOVolatileItemClaimedRewards\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Defidx` | `uint` | get, set | - |
| `Reward` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `GenerationTime` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |



---

## 🔌 CSOVolatileItemOffer

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSOVolatileItemOffer\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Defidx` | `uint` | get, set | - |
| `FauxItemid` | `IProtobufRepeatedFieldValueType\<ulong\>` | get | - |
| `GenerationTime` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |



---

## 🔌 CSVCMsgList_GameEvents

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsgList_GameEvents\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Events` | `IProtobufRepeatedFieldSubMessageType\<CSVCMsgList_GameEvents_event_t\>` | get | - |



---

## 🔌 CSVCMsgList_GameEvents_event_t

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsgList_GameEvents_event_t\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Tick` | `int` | get, set | - |
| `Event` | `CSVCMsg_GameEvent` | get | - |



---

## 🔌 CSVCMsg_BSPDecal

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_BSPDecal\>`

**实现接口:** `INetMessage\<CSVCMsg_BSPDecal\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Pos` | `Vector` | get, set | - |
| `DecalTextureIndex` | `int` | get, set | - |
| `EntityIndex` | `int` | get, set | - |
| `ModelIndex` | `int` | get, set | - |
| `LowPriority` | `bool` | get, set | - |



---

## 🔌 CSVCMsg_Broadcast_Command

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_Broadcast_Command\>`

**实现接口:** `INetMessage\<CSVCMsg_Broadcast_Command\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Cmd` | `string` | get, set | - |



---

## 🔌 CSVCMsg_ClassInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_ClassInfo\>`

**实现接口:** `INetMessage\<CSVCMsg_ClassInfo\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CreateOnClient` | `bool` | get, set | - |
| `Classes` | `IProtobufRepeatedFieldSubMessageType\<CSVCMsg_ClassInfo_class_t\>` | get | - |



---

## 🔌 CSVCMsg_ClassInfo_class_t

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_ClassInfo_class_t\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ClassId` | `int` | get, set | - |
| `ClassName` | `string` | get, set | - |



---

## 🔌 CSVCMsg_ClearAllStringTables

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_ClearAllStringTables\>`

**实现接口:** `INetMessage\<CSVCMsg_ClearAllStringTables\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Mapname` | `string` | get, set | - |
| `CreateTablesSkipped` | `bool` | get, set | - |



---

## 🔌 CSVCMsg_CmdKeyValues

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_CmdKeyValues\>`

**实现接口:** `INetMessage\<CSVCMsg_CmdKeyValues\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Data` | `byte[]` | get, set | - |



---

## 🔌 CSVCMsg_CreateStringTable

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_CreateStringTable\>`

**实现接口:** `INetMessage\<CSVCMsg_CreateStringTable\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | get, set | - |
| `NumEntries` | `int` | get, set | - |
| `UserDataFixedSize` | `bool` | get, set | - |
| `UserDataSize` | `int` | get, set | - |
| `UserDataSizeBits` | `int` | get, set | - |
| `Flags` | `int` | get, set | - |
| `StringData` | `byte[]` | get, set | - |
| `UncompressedSize` | `int` | get, set | - |
| `DataCompressed` | `bool` | get, set | - |
| `UsingVarintBitcounts` | `bool` | get, set | - |



---

## 🔌 CSVCMsg_CrosshairAngle

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_CrosshairAngle\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Angle` | `QAngle` | get, set | - |



---

## 🔌 CSVCMsg_FixAngle

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_FixAngle\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Relative` | `bool` | get, set | - |
| `Angle` | `QAngle` | get, set | - |



---

## 🔌 CSVCMsg_FlattenedSerializer

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_FlattenedSerializer\>`

**实现接口:** `INetMessage\<CSVCMsg_FlattenedSerializer\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Serializers` | `IProtobufRepeatedFieldSubMessageType\<ProtoFlattenedSerializer_t\>` | get | - |
| `Symbols` | `IProtobufRepeatedFieldValueType\<string\>` | get | - |
| `Fields` | `IProtobufRepeatedFieldSubMessageType\<ProtoFlattenedSerializerField_t\>` | get | - |



---

## 🔌 CSVCMsg_FullFrameSplit

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_FullFrameSplit\>`

**实现接口:** `INetMessage\<CSVCMsg_FullFrameSplit\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Tick` | `int` | get, set | - |
| `Section` | `int` | get, set | - |
| `Total` | `int` | get, set | - |
| `Data` | `byte[]` | get, set | - |



---

## 🔌 CSVCMsg_GameEvent

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_GameEvent\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EventName` | `string` | get, set | - |
| `Eventid` | `int` | get, set | - |
| `Keys` | `IProtobufRepeatedFieldSubMessageType\<CSVCMsg_GameEvent_key_t\>` | get | - |



---

## 🔌 CSVCMsg_GameEventList

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_GameEventList\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Descriptors` | `IProtobufRepeatedFieldSubMessageType\<CSVCMsg_GameEventList_descriptor_t\>` | get | - |



---

## 🔌 CSVCMsg_GameEventList_descriptor_t

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_GameEventList_descriptor_t\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Eventid` | `int` | get, set | - |
| `Name` | `string` | get, set | - |
| `Keys` | `IProtobufRepeatedFieldSubMessageType\<CSVCMsg_GameEventList_key_t\>` | get | - |



---

## 🔌 CSVCMsg_GameEventList_key_t

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_GameEventList_key_t\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Type` | `int` | get, set | - |
| `Name` | `string` | get, set | - |



---

## 🔌 CSVCMsg_GameEvent_key_t

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_GameEvent_key_t\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Type` | `int` | get, set | - |
| `ValString` | `string` | get, set | - |
| `ValFloat` | `float` | get, set | - |
| `ValLong` | `int` | get, set | - |
| `ValShort` | `int` | get, set | - |
| `ValByte` | `int` | get, set | - |
| `ValBool` | `bool` | get, set | - |
| `ValUint64` | `ulong` | get, set | - |



---

## 🔌 CSVCMsg_GameSessionConfiguration

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_GameSessionConfiguration\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `IsMultiplayer` | `bool` | get, set | - |
| `IsLoadsavegame` | `bool` | get, set | - |
| `IsBackgroundMap` | `bool` | get, set | - |
| `IsHeadless` | `bool` | get, set | - |
| `MinClientLimit` | `uint` | get, set | - |
| `MaxClientLimit` | `uint` | get, set | - |
| `MaxClients` | `uint` | get, set | - |
| `TickInterval` | `uint` | get, set | - |
| `Hostname` | `string` | get, set | - |
| `Savegamename` | `string` | get, set | - |
| `S1Mapname` | `string` | get, set | - |
| `Gamemode` | `string` | get, set | - |
| `ServerIpAddress` | `string` | get, set | - |
| `Data` | `byte[]` | get, set | - |
| `IsLocalonly` | `bool` | get, set | - |
| `NoSteamServer` | `bool` | get, set | - |
| `IsTransition` | `bool` | get, set | - |
| `Previouslevel` | `string` | get, set | - |
| `Landmarkname` | `string` | get, set | - |



---

## 🔌 CSVCMsg_GetCvarValue

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_GetCvarValue\>`

**实现接口:** `INetMessage\<CSVCMsg_GetCvarValue\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Cookie` | `int` | get, set | - |
| `CvarName` | `string` | get, set | - |



---

## 🔌 CSVCMsg_HLTVStatus

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_HLTVStatus\>`

**实现接口:** `INetMessage\<CSVCMsg_HLTVStatus\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Master` | `string` | get, set | - |
| `Clients` | `int` | get, set | - |
| `Slots` | `int` | get, set | - |
| `Proxies` | `int` | get, set | - |



---

## 🔌 CSVCMsg_HltvFixupOperatorStatus

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_HltvFixupOperatorStatus\>`

**实现接口:** `INetMessage\<CSVCMsg_HltvFixupOperatorStatus\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Mode` | `uint` | get, set | - |
| `OverrideOperatorName` | `string` | get, set | - |



---

## 🔌 CSVCMsg_HltvReplay

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_HltvReplay\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Delay` | `int` | get, set | - |
| `PrimaryTarget` | `int` | get, set | - |
| `ReplayStopAt` | `int` | get, set | - |
| `ReplayStartAt` | `int` | get, set | - |
| `ReplaySlowdownBegin` | `int` | get, set | - |
| `ReplaySlowdownEnd` | `int` | get, set | - |
| `ReplaySlowdownRate` | `float` | get, set | - |
| `Reason` | `int` | get, set | - |



---

## 🔌 CSVCMsg_Menu

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_Menu\>`

**实现接口:** `INetMessage\<CSVCMsg_Menu\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `DialogType` | `int` | get, set | - |
| `MenuKeyValues` | `byte[]` | get, set | - |



---

## 🔌 CSVCMsg_NextMsgPredicted

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_NextMsgPredicted\>`

**实现接口:** `INetMessage\<CSVCMsg_NextMsgPredicted\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PredictedByPlayerSlot` | `int` | get, set | - |
| `MessageTypeId` | `uint` | get, set | - |



---

## 🔌 CSVCMsg_PacketEntities

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_PacketEntities\>`

**实现接口:** `INetMessage\<CSVCMsg_PacketEntities\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MaxEntries` | `int` | get, set | - |
| `UpdatedEntries` | `int` | get, set | - |
| `LegacyIsDelta` | `bool` | get, set | - |
| `UpdateBaseline` | `bool` | get, set | - |
| `Baseline` | `int` | get, set | - |
| `DeltaFrom` | `int` | get, set | - |
| `EntityData` | `byte[]` | get, set | - |
| `PendingFullFrame` | `bool` | get, set | - |
| `ActiveSpawngroupHandle` | `uint` | get, set | - |
| `MaxSpawngroupCreationsequence` | `uint` | get, set | - |
| `LastCmdNumberExecuted` | `uint` | get, set | - |
| `LastCmdNumberRecvDelta` | `int` | get, set | - |
| `ServerTick` | `uint` | get, set | - |
| `SerializedEntities` | `byte[]` | get, set | - |
| `AlternateBaselines` | `IProtobufRepeatedFieldSubMessageType\<CSVCMsg_PacketEntities_alternate_baseline_t\>` | get | - |
| `HasPvsVisBitsDeprecated` | `uint` | get, set | - |
| `CmdRecvStatus` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `NonTransmittedEntities` | `CSVCMsg_PacketEntities_non_transmitted_entities_t` | get | - |
| `CqStarvedCommandTicks` | `uint` | get, set | - |
| `CqDiscardedCommandTicks` | `uint` | get, set | - |
| `OutofpvsEntityUpdates` | `CSVCMsg_PacketEntities_outofpvs_entity_updates_t` | get | - |
| `DevPadding` | `byte[]` | get, set | - |



---

## 🔌 CSVCMsg_PacketEntities_alternate_baseline_t

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_PacketEntities_alternate_baseline_t\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityIndex` | `int` | get, set | - |
| `BaselineIndex` | `int` | get, set | - |



---

## 🔌 CSVCMsg_PacketEntities_non_transmitted_entities_t

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_PacketEntities_non_transmitted_entities_t\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `HeaderCount` | `int` | get, set | - |
| `Data` | `byte[]` | get, set | - |



---

## 🔌 CSVCMsg_PacketEntities_outofpvs_entity_updates_t

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_PacketEntities_outofpvs_entity_updates_t\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Count` | `int` | get, set | - |
| `Data` | `byte[]` | get, set | - |



---

## 🔌 CSVCMsg_PacketReliable

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_PacketReliable\>`

**实现接口:** `INetMessage\<CSVCMsg_PacketReliable\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Tick` | `int` | get, set | - |
| `Messagessize` | `int` | get, set | - |
| `State` | `bool` | get, set | - |



---

## 🔌 CSVCMsg_PeerList

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_PeerList\>`

**实现接口:** `INetMessage\<CSVCMsg_PeerList\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Peer` | `IProtobufRepeatedFieldSubMessageType\<CMsgServerPeer\>` | get | - |



---

## 🔌 CSVCMsg_Prefetch

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_Prefetch\>`

**实现接口:** `INetMessage\<CSVCMsg_Prefetch\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SoundIndex` | `int` | get, set | - |
| `ResourceType` | `PrefetchType` | get, set | - |



---

## 🔌 CSVCMsg_Print

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_Print\>`

**实现接口:** `INetMessage\<CSVCMsg_Print\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Text` | `string` | get, set | - |



---

## 🔌 CSVCMsg_RconServerDetails

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_RconServerDetails\>`

**实现接口:** `INetMessage\<CSVCMsg_RconServerDetails\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Token` | `byte[]` | get, set | - |
| `Details` | `string` | get, set | - |



---

## 🔌 CSVCMsg_SendTable

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_SendTable\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `IsEnd` | `bool` | get, set | - |
| `NetTableName` | `string` | get, set | - |
| `NeedsDecoder` | `bool` | get, set | - |
| `Props` | `IProtobufRepeatedFieldSubMessageType\<CSVCMsg_SendTable_sendprop_t\>` | get | - |



---

## 🔌 CSVCMsg_SendTable_sendprop_t

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_SendTable_sendprop_t\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Type` | `int` | get, set | - |
| `VarName` | `string` | get, set | - |
| `Flags` | `int` | get, set | - |
| `Priority` | `int` | get, set | - |
| `DtName` | `string` | get, set | - |
| `NumElements` | `int` | get, set | - |
| `LowValue` | `float` | get, set | - |
| `HighValue` | `float` | get, set | - |
| `NumBits` | `int` | get, set | - |



---

## 🔌 CSVCMsg_ServerInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_ServerInfo\>`

**实现接口:** `INetMessage\<CSVCMsg_ServerInfo\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Protocol` | `int` | get, set | - |
| `ServerCount` | `int` | get, set | - |
| `IsDedicated` | `bool` | get, set | - |
| `IsHltv` | `bool` | get, set | - |
| `COs` | `int` | get, set | - |
| `MaxClients` | `int` | get, set | - |
| `MaxClasses` | `int` | get, set | - |
| `PlayerSlot` | `int` | get, set | - |
| `TickInterval` | `float` | get, set | - |
| `GameDir` | `string` | get, set | - |
| `MapName` | `string` | get, set | - |
| `SkyName` | `string` | get, set | - |
| `HostName` | `string` | get, set | - |
| `AddonName` | `string` | get, set | - |
| `GameSessionConfig` | `CSVCMsg_GameSessionConfiguration` | get | - |
| `GameSessionManifest` | `byte[]` | get, set | - |



---

## 🔌 CSVCMsg_ServerSteamID

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_ServerSteamID\>`

**实现接口:** `INetMessage\<CSVCMsg_ServerSteamID\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SteamId` | `ulong` | get, set | - |



---

## 🔌 CSVCMsg_SetPause

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_SetPause\>`

**实现接口:** `INetMessage\<CSVCMsg_SetPause\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Paused` | `bool` | get, set | - |



---

## 🔌 CSVCMsg_SetView

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_SetView\>`

**实现接口:** `INetMessage\<CSVCMsg_SetView\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityIndex` | `int` | get, set | - |
| `Slot` | `int` | get, set | - |



---

## 🔌 CSVCMsg_Sounds

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_Sounds\>`

**实现接口:** `INetMessage\<CSVCMsg_Sounds\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ReliableSound` | `bool` | get, set | - |
| `Sounds` | `IProtobufRepeatedFieldSubMessageType\<CSVCMsg_Sounds_sounddata_t\>` | get | - |



---

## 🔌 CSVCMsg_Sounds_sounddata_t

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_Sounds_sounddata_t\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `OriginX` | `int` | get, set | - |
| `OriginY` | `int` | get, set | - |
| `OriginZ` | `int` | get, set | - |
| `Volume` | `uint` | get, set | - |
| `DelayValue` | `float` | get, set | - |
| `SequenceNumber` | `int` | get, set | - |
| `EntityIndex` | `int` | get, set | - |
| `Channel` | `int` | get, set | - |
| `Pitch` | `int` | get, set | - |
| `Flags` | `int` | get, set | - |
| `SoundNum` | `uint` | get, set | - |
| `SoundNumHandle` | `uint` | get, set | - |
| `SpeakerEntity` | `int` | get, set | - |
| `RandomSeed` | `int` | get, set | - |
| `SoundLevel` | `int` | get, set | - |
| `IsSentence` | `bool` | get, set | - |
| `IsAmbient` | `bool` | get, set | - |
| `Guid` | `uint` | get, set | - |
| `SoundResourceId` | `ulong` | get, set | - |



---

## 🔌 CSVCMsg_SplitScreen

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_SplitScreen\>`

**实现接口:** `INetMessage\<CSVCMsg_SplitScreen\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Type` | `ESplitScreenMessageType` | get, set | - |
| `Slot` | `int` | get, set | - |
| `PlayerIndex` | `int` | get, set | - |



---

## 🔌 CSVCMsg_StopSound

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_StopSound\>`

**实现接口:** `INetMessage\<CSVCMsg_StopSound\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Guid` | `uint` | get, set | - |



---

## 🔌 CSVCMsg_TempEntities

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_TempEntities\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Reliable` | `bool` | get, set | - |
| `NumEntries` | `int` | get, set | - |
| `EntityData` | `byte[]` | get, set | - |



---

## 🔌 CSVCMsg_UpdateStringTable

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_UpdateStringTable\>`

**实现接口:** `INetMessage\<CSVCMsg_UpdateStringTable\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TableId` | `int` | get, set | - |
| `NumChangedEntries` | `int` | get, set | - |
| `StringData` | `byte[]` | get, set | - |



---

## 🔌 CSVCMsg_UserCommands

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_UserCommands\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Commands` | `IProtobufRepeatedFieldSubMessageType\<CMsgServerUserCmd\>` | get | - |



---

## 🔌 CSVCMsg_UserMessage

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_UserMessage\>`

**实现接口:** `INetMessage\<CSVCMsg_UserMessage\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MsgType` | `int` | get, set | - |
| `MsgData` | `byte[]` | get, set | - |
| `Passthrough` | `int` | get, set | - |



---

## 🔌 CSVCMsg_VoiceData

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_VoiceData\>`

**实现接口:** `INetMessage\<CSVCMsg_VoiceData\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Audio` | `CMsgVoiceAudio` | get | - |
| `Client` | `int` | get, set | - |
| `Proximity` | `bool` | get, set | - |
| `Xuid` | `ulong` | get, set | - |
| `AudibleMask` | `int` | get, set | - |
| `Tick` | `uint` | get, set | - |
| `Passthrough` | `int` | get, set | - |



---

## 🔌 CSVCMsg_VoiceInit

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSVCMsg_VoiceInit\>`

**实现接口:** `INetMessage\<CSVCMsg_VoiceInit\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Quality` | `int` | get, set | - |
| `Codec` | `string` | get, set | - |
| `Version` | `int` | get, set | - |



---

## 🔌 CSource2Metrics_MatchPerfSummary_Notification

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSource2Metrics_MatchPerfSummary_Notification\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Appid` | `uint` | get, set | - |
| `GameMode` | `string` | get, set | - |
| `ServerBuildId` | `uint` | get, set | - |
| `ServerPopid` | `uint` | get, set | - |
| `ServerProfile` | `CMsgSource2VProfLiteReport` | get | - |
| `Clients` | `IProtobufRepeatedFieldSubMessageType\<CSource2Metrics_MatchPerfSummary_Notification_Client\>` | get | - |
| `Map` | `string` | get, set | - |



---

## 🔌 CSource2Metrics_MatchPerfSummary_Notification_Client

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSource2Metrics_MatchPerfSummary_Notification_Client\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SystemSpecs` | `CMsgSource2SystemSpecs` | get | - |
| `Profile` | `CMsgSource2VProfLiteReport` | get | - |
| `BuildId` | `uint` | get, set | - |
| `DownstreamFlow` | `CMsgSource2NetworkFlowQuality` | get | - |
| `UpstreamFlow` | `CMsgSource2NetworkFlowQuality` | get | - |
| `Steamid` | `ulong` | get, set | - |
| `PerfSamples` | `IProtobufRepeatedFieldSubMessageType\<CMsgSource2PerfIntervalSample\>` | get | - |



---

## 🔌 CSteam_Voice_Encoding

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSteam_Voice_Encoding\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `VoiceData` | `byte[]` | get, set | - |



---

## 🔌 CSubtickMoveStep

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CSubtickMoveStep\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Button` | `ulong` | get, set | - |
| `Pressed` | `bool` | get, set | - |
| `When` | `float` | get, set | - |
| `AnalogForwardDelta` | `float` | get, set | - |
| `AnalogLeftDelta` | `float` | get, set | - |
| `PitchDelta` | `float` | get, set | - |
| `YawDelta` | `float` | get, set | - |



---

## 🔌 CUIFontFilePB

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUIFontFilePB\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `FontFileName` | `string` | get, set | - |
| `OpentypeFontData` | `byte[]` | get, set | - |



---

## 🔌 CUIFontFilePackagePB

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUIFontFilePackagePB\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PackageVersion` | `uint` | get, set | - |
| `EncryptedFontFiles` | `IProtobufRepeatedFieldSubMessageType\<CUIFontFilePackagePB_CUIEncryptedFontFilePB\>` | get | - |



---

## 🔌 CUIFontFilePackagePB_CUIEncryptedFontFilePB

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUIFontFilePackagePB_CUIEncryptedFontFilePB\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EncryptedContents` | `byte[]` | get, set | - |



---

## 🔌 CUserCmdBasePB

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserCmdBasePB\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Base` | `CBaseUserCmdPB` | get | - |



---

## 🔌 CUserMessageAchievementEvent

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageAchievementEvent\>`

**实现接口:** `INetMessage\<CUserMessageAchievementEvent\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Achievement` | `uint` | get, set | - |



---

## 🔌 CUserMessageAmmoDenied

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageAmmoDenied\>`

**实现接口:** `INetMessage\<CUserMessageAmmoDenied\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AmmoId` | `uint` | get, set | - |



---

## 🔌 CUserMessageAnimStateGraphState

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageAnimStateGraphState\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityIndex` | `int` | get, set | - |
| `Data` | `byte[]` | get, set | - |



---

## 🔌 CUserMessageAudioParameter

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageAudioParameter\>`

**实现接口:** `INetMessage\<CUserMessageAudioParameter\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ParameterType` | `uint` | get, set | - |
| `NameHashCode` | `uint` | get, set | - |
| `Value` | `float` | get, set | - |
| `IntValue` | `uint` | get, set | - |



---

## 🔌 CUserMessageCameraTransition

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageCameraTransition\>`

**实现接口:** `INetMessage\<CUserMessageCameraTransition\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CameraType` | `uint` | get, set | - |
| `Duration` | `float` | get, set | - |
| `ParamsDataDriven` | `CUserMessageCameraTransition_Transition_DataDriven` | get | - |



---

## 🔌 CUserMessageCameraTransition_Transition_DataDriven

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageCameraTransition_Transition_DataDriven\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Filename` | `string` | get, set | - |
| `AttachEntIndex` | `int` | get, set | - |
| `Duration` | `float` | get, set | - |



---

## 🔌 CUserMessageCloseCaption

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageCloseCaption\>`

**实现接口:** `INetMessage\<CUserMessageCloseCaption\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Hash` | `uint` | get, set | - |
| `Duration` | `float` | get, set | - |
| `FromPlayer` | `bool` | get, set | - |
| `EntIndex` | `int` | get, set | - |



---

## 🔌 CUserMessageCloseCaptionDirect

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageCloseCaptionDirect\>`

**实现接口:** `INetMessage\<CUserMessageCloseCaptionDirect\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Hash` | `uint` | get, set | - |
| `Duration` | `float` | get, set | - |
| `FromPlayer` | `bool` | get, set | - |
| `EntIndex` | `int` | get, set | - |



---

## 🔌 CUserMessageCloseCaptionPlaceholder

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageCloseCaptionPlaceholder\>`

**实现接口:** `INetMessage\<CUserMessageCloseCaptionPlaceholder\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `String` | `string` | get, set | - |
| `Duration` | `float` | get, set | - |
| `FromPlayer` | `bool` | get, set | - |
| `EntIndex` | `int` | get, set | - |



---

## 🔌 CUserMessageColoredText

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageColoredText\>`

**实现接口:** `INetMessage\<CUserMessageColoredText\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Color` | `uint` | get, set | - |
| `Text` | `string` | get, set | - |
| `Reset` | `bool` | get, set | - |
| `ContextPlayerSlot` | `int` | get, set | - |
| `ContextValue` | `int` | get, set | - |
| `ContextTeamId` | `int` | get, set | - |



---

## 🔌 CUserMessageCreditsMsg

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageCreditsMsg\>`

**实现接口:** `INetMessage\<CUserMessageCreditsMsg\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Rolltype` | `eRollType` | get, set | - |
| `LogoLength` | `float` | get, set | - |



---

## 🔌 CUserMessageCurrentTimescale

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageCurrentTimescale\>`

**实现接口:** `INetMessage\<CUserMessageCurrentTimescale\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Current` | `float` | get, set | - |



---

## 🔌 CUserMessageDesiredTimescale

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageDesiredTimescale\>`

**实现接口:** `INetMessage\<CUserMessageDesiredTimescale\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Desired` | `float` | get, set | - |
| `Acceleration` | `float` | get, set | - |
| `Minblendrate` | `float` | get, set | - |
| `Blenddeltamultiplier` | `float` | get, set | - |



---

## 🔌 CUserMessageFade

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageFade\>`

**实现接口:** `INetMessage\<CUserMessageFade\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Duration` | `uint` | get, set | - |
| `HoldTime` | `uint` | get, set | - |
| `Flags` | `uint` | get, set | - |
| `Color` | `uint` | get, set | - |



---

## 🔌 CUserMessageGameTitle

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageGameTitle\>`

**实现接口:** `INetMessage\<CUserMessageGameTitle\>`, `IDisposable`



---

## 🔌 CUserMessageHapticsManagerEffect

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageHapticsManagerEffect\>`

**实现接口:** `INetMessage\<CUserMessageHapticsManagerEffect\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `HandId` | `int` | get, set | - |
| `EffectNameHashCode` | `uint` | get, set | - |
| `EffectScale` | `float` | get, set | - |



---

## 🔌 CUserMessageHapticsManagerPulse

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageHapticsManagerPulse\>`

**实现接口:** `INetMessage\<CUserMessageHapticsManagerPulse\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `HandId` | `int` | get, set | - |
| `EffectAmplitude` | `float` | get, set | - |
| `EffectFrequency` | `float` | get, set | - |
| `EffectDuration` | `float` | get, set | - |



---

## 🔌 CUserMessageHudMsg

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageHudMsg\>`

**实现接口:** `INetMessage\<CUserMessageHudMsg\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Channel` | `uint` | get, set | - |
| `X` | `float` | get, set | - |
| `Y` | `float` | get, set | - |
| `Color1` | `uint` | get, set | - |
| `Color2` | `uint` | get, set | - |
| `Effect` | `uint` | get, set | - |
| `Message` | `string` | get, set | - |



---

## 🔌 CUserMessageHudText

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageHudText\>`

**实现接口:** `INetMessage\<CUserMessageHudText\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Message` | `string` | get, set | - |



---

## 🔌 CUserMessageItemPickup

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageItemPickup\>`

**实现接口:** `INetMessage\<CUserMessageItemPickup\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Itemname` | `string` | get, set | - |



---

## 🔌 CUserMessageLagCompensationError

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageLagCompensationError\>`

**实现接口:** `INetMessage\<CUserMessageLagCompensationError\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Distance` | `float` | get, set | - |



---

## 🔌 CUserMessageRequestDiagnostic

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageRequestDiagnostic\>`

**实现接口:** `INetMessage\<CUserMessageRequestDiagnostic\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Diagnostics` | `IProtobufRepeatedFieldSubMessageType\<CUserMessageRequestDiagnostic_Diagnostic\>` | get | - |



---

## 🔌 CUserMessageRequestDiagnostic_Diagnostic

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageRequestDiagnostic_Diagnostic\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Index` | `int` | get, set | - |
| `Offset` | `long` | get, set | - |
| `Param` | `int` | get, set | - |
| `Length` | `int` | get, set | - |
| `Type` | `int` | get, set | - |
| `Base` | `long` | get, set | - |
| `Range` | `long` | get, set | - |
| `Extent` | `long` | get, set | - |
| `Detail` | `long` | get, set | - |
| `Name` | `string` | get, set | - |
| `Alias` | `string` | get, set | - |
| `Vardetail` | `byte[]` | get, set | - |
| `Context` | `int` | get, set | - |



---

## 🔌 CUserMessageRequestDllStatus

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageRequestDllStatus\>`

**实现接口:** `INetMessage\<CUserMessageRequestDllStatus\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `DllAction` | `string` | get, set | - |
| `FullReport` | `bool` | get, set | - |



---

## 🔌 CUserMessageRequestInventory

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageRequestInventory\>`

**实现接口:** `INetMessage\<CUserMessageRequestInventory\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Inventory` | `int` | get, set | - |
| `Offset` | `int` | get, set | - |
| `Options` | `int` | get, set | - |



---

## 🔌 CUserMessageRequestState

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageRequestState\>`

**实现接口:** `INetMessage\<CUserMessageRequestState\>`, `IDisposable`



---

## 🔌 CUserMessageRequestUtilAction

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageRequestUtilAction\>`

**实现接口:** `INetMessage\<CUserMessageRequestUtilAction\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Util1` | `int` | get, set | - |
| `Util2` | `int` | get, set | - |
| `Util3` | `int` | get, set | - |
| `Util4` | `int` | get, set | - |
| `Util5` | `int` | get, set | - |



---

## 🔌 CUserMessageResetHUD

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageResetHUD\>`

**实现接口:** `INetMessage\<CUserMessageResetHUD\>`, `IDisposable`



---

## 🔌 CUserMessageRumble

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageRumble\>`

**实现接口:** `INetMessage\<CUserMessageRumble\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Index` | `int` | get, set | - |
| `Data` | `int` | get, set | - |
| `Flags` | `int` | get, set | - |



---

## 🔌 CUserMessageSayText

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageSayText\>`

**实现接口:** `INetMessage\<CUserMessageSayText\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Playerindex` | `int` | get, set | - |
| `Text` | `string` | get, set | - |
| `Chat` | `bool` | get, set | - |



---

## 🔌 CUserMessageSayText2

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageSayText2\>`

**实现接口:** `INetMessage\<CUserMessageSayText2\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Entityindex` | `int` | get, set | - |
| `Chat` | `bool` | get, set | - |
| `Messagename` | `string` | get, set | - |
| `Param1` | `string` | get, set | - |
| `Param2` | `string` | get, set | - |
| `Param3` | `string` | get, set | - |
| `Param4` | `string` | get, set | - |



---

## 🔌 CUserMessageSayTextChannel

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageSayTextChannel\>`

**实现接口:** `INetMessage\<CUserMessageSayTextChannel\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Player` | `int` | get, set | - |
| `Channel` | `int` | get, set | - |
| `Text` | `string` | get, set | - |



---

## 🔌 CUserMessageScreenTilt

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageScreenTilt\>`

**实现接口:** `INetMessage\<CUserMessageScreenTilt\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Command` | `uint` | get, set | - |
| `EaseInOut` | `bool` | get, set | - |
| `Angle` | `Vector` | get, set | - |
| `Duration` | `float` | get, set | - |
| `Time` | `float` | get, set | - |



---

## 🔌 CUserMessageSendAudio

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageSendAudio\>`

**实现接口:** `INetMessage\<CUserMessageSendAudio\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Soundname` | `string` | get, set | - |
| `Stop` | `bool` | get, set | - |



---

## 🔌 CUserMessageServerFrameTime

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageServerFrameTime\>`

**实现接口:** `INetMessage\<CUserMessageServerFrameTime\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `FrameTime` | `float` | get, set | - |



---

## 🔌 CUserMessageShake

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageShake\>`

**实现接口:** `INetMessage\<CUserMessageShake\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Command` | `uint` | get, set | - |
| `Amplitude` | `float` | get, set | - |
| `Frequency` | `float` | get, set | - |
| `Duration` | `float` | get, set | - |



---

## 🔌 CUserMessageShakeDir

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageShakeDir\>`

**实现接口:** `INetMessage\<CUserMessageShakeDir\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Shake` | `CUserMessageShake` | get | - |
| `Direction` | `Vector` | get, set | - |



---

## 🔌 CUserMessageShowMenu

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageShowMenu\>`

**实现接口:** `INetMessage\<CUserMessageShowMenu\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Validslots` | `uint` | get, set | - |
| `Displaytime` | `uint` | get, set | - |
| `Needmore` | `bool` | get, set | - |
| `Menustring` | `string` | get, set | - |



---

## 🔌 CUserMessageTextMsg

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageTextMsg\>`

**实现接口:** `INetMessage\<CUserMessageTextMsg\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Dest` | `uint` | get, set | - |
| `Param` | `IProtobufRepeatedFieldValueType\<string\>` | get | - |



---

## 🔌 CUserMessageUpdateCssClasses

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageUpdateCssClasses\>`

**实现接口:** `INetMessage\<CUserMessageUpdateCssClasses\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TargetWorldPanel` | `int` | get, set | - |
| `CssClasses` | `string` | get, set | - |
| `IsAdd` | `bool` | get, set | - |



---

## 🔌 CUserMessageVoiceMask

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageVoiceMask\>`

**实现接口:** `INetMessage\<CUserMessageVoiceMask\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `GamerulesMasks` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `BanMasks` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `ModEnable` | `bool` | get, set | - |



---

## 🔌 CUserMessageWaterShake

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessageWaterShake\>`

**实现接口:** `INetMessage\<CUserMessageWaterShake\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Command` | `uint` | get, set | - |
| `Amplitude` | `float` | get, set | - |
| `Frequency` | `float` | get, set | - |
| `Duration` | `float` | get, set | - |



---

## 🔌 CUserMessage_Diagnostic_Response

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessage_Diagnostic_Response\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Diagnostics` | `IProtobufRepeatedFieldSubMessageType\<CUserMessage_Diagnostic_Response_Diagnostic\>` | get | - |
| `BuildVersion` | `int` | get, set | - |
| `Instance` | `int` | get, set | - |
| `StartTime` | `long` | get, set | - |
| `Osversion` | `int` | get, set | - |
| `Platform` | `int` | get, set | - |



---

## 🔌 CUserMessage_Diagnostic_Response_Diagnostic

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessage_Diagnostic_Response_Diagnostic\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Index` | `int` | get, set | - |
| `Offset` | `long` | get, set | - |
| `Param` | `int` | get, set | - |
| `Length` | `int` | get, set | - |
| `Detail` | `byte[]` | get, set | - |
| `Base` | `long` | get, set | - |
| `Range` | `long` | get, set | - |
| `Type` | `int` | get, set | - |
| `Name` | `string` | get, set | - |
| `Alias` | `string` | get, set | - |
| `Backup` | `byte[]` | get, set | - |
| `Context` | `int` | get, set | - |
| `Control` | `long` | get, set | - |
| `Augment` | `long` | get, set | - |
| `Placebo` | `long` | get, set | - |



---

## 🔌 CUserMessage_DllStatus

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessage_DllStatus\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `FileReport` | `string` | get, set | - |
| `CommandLine` | `string` | get, set | - |
| `TotalFiles` | `uint` | get, set | - |
| `ProcessId` | `uint` | get, set | - |
| `Osversion` | `int` | get, set | - |
| `ClientTime` | `ulong` | get, set | - |
| `Diagnostics` | `IProtobufRepeatedFieldSubMessageType\<CUserMessage_DllStatus_CVDiagnostic\>` | get | - |
| `Modules` | `IProtobufRepeatedFieldSubMessageType\<CUserMessage_DllStatus_CModule\>` | get | - |



---

## 🔌 CUserMessage_DllStatus_CModule

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessage_DllStatus_CModule\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `BaseAddr` | `ulong` | get, set | - |
| `Name` | `string` | get, set | - |
| `Size` | `uint` | get, set | - |
| `Timestamp` | `uint` | get, set | - |



---

## 🔌 CUserMessage_DllStatus_CVDiagnostic

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessage_DllStatus_CVDiagnostic\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Id` | `uint` | get, set | - |
| `Extended` | `uint` | get, set | - |
| `Value` | `ulong` | get, set | - |
| `StringValue` | `string` | get, set | - |



---

## 🔌 CUserMessage_ExtraUserData

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessage_ExtraUserData\>`

**实现接口:** `INetMessage\<CUserMessage_ExtraUserData\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Item` | `int` | get, set | - |
| `Value1` | `long` | get, set | - |
| `Value2` | `long` | get, set | - |
| `Detail1` | `IProtobufRepeatedFieldValueType\<byte[]\>` | get | - |
| `Detail2` | `IProtobufRepeatedFieldValueType\<byte[]\>` | get | - |



---

## 🔌 CUserMessage_Inventory_Response

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessage_Inventory_Response\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Crc` | `uint` | get, set | - |
| `ItemCount` | `int` | get, set | - |
| `Osversion` | `int` | get, set | - |
| `PerfTime` | `int` | get, set | - |
| `ClientTimestamp` | `int` | get, set | - |
| `Platform` | `int` | get, set | - |
| `Inventories` | `IProtobufRepeatedFieldSubMessageType\<CUserMessage_Inventory_Response_InventoryDetail\>` | get | - |
| `Inventories2` | `IProtobufRepeatedFieldSubMessageType\<CUserMessage_Inventory_Response_InventoryDetail\>` | get | - |
| `Inventories3` | `IProtobufRepeatedFieldSubMessageType\<CUserMessage_Inventory_Response_InventoryDetail\>` | get | - |
| `InvType` | `int` | get, set | - |
| `BuildVersion` | `int` | get, set | - |
| `Instance` | `int` | get, set | - |
| `StartTime` | `long` | get, set | - |



---

## 🔌 CUserMessage_Inventory_Response_InventoryDetail

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessage_Inventory_Response_InventoryDetail\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Index` | `int` | get, set | - |
| `Primary` | `long` | get, set | - |
| `Offset` | `long` | get, set | - |
| `First` | `long` | get, set | - |
| `Base` | `long` | get, set | - |
| `Name` | `string` | get, set | - |
| `BaseName` | `string` | get, set | - |
| `BaseDetail` | `int` | get, set | - |
| `BaseTime` | `int` | get, set | - |
| `BaseHash` | `int` | get, set | - |



---

## 🔌 CUserMessage_NotifyResponseFound

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessage_NotifyResponseFound\>`

**实现接口:** `INetMessage\<CUserMessage_NotifyResponseFound\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntIndex` | `int` | get, set | - |
| `RuleName` | `string` | get, set | - |
| `ResponseValue` | `string` | get, set | - |
| `ResponseConcept` | `string` | get, set | - |
| `Criteria` | `IProtobufRepeatedFieldSubMessageType\<CUserMessage_NotifyResponseFound_Criteria\>` | get | - |
| `IntCriteriaNames` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `IntCriteriaValues` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `FloatCriteriaNames` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `FloatCriteriaValues` | `IProtobufRepeatedFieldValueType\<float\>` | get | - |
| `SymbolCriteriaNames` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `SymbolCriteriaValues` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `SpeakResult` | `int` | get, set | - |



---

## 🔌 CUserMessage_NotifyResponseFound_Criteria

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessage_NotifyResponseFound_Criteria\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `NameSymbol` | `uint` | get, set | - |
| `Value` | `string` | get, set | - |



---

## 🔌 CUserMessage_PlayResponseConditional

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessage_PlayResponseConditional\>`

**实现接口:** `INetMessage\<CUserMessage_PlayResponseConditional\>`, `IDisposable`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntIndex` | `int` | get, set | - |
| `PlayerSlots` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `Response` | `string` | get, set | - |
| `EntOrigin` | `Vector` | get, set | - |
| `PreDelay` | `float` | get, set | - |
| `MixPriority` | `int` | get, set | - |



---

## 🔌 CUserMessage_UtilMsg_Response

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessage_UtilMsg_Response\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Crc` | `uint` | get, set | - |
| `ItemCount` | `int` | get, set | - |
| `Crc2` | `uint` | get, set | - |
| `ItemCount2` | `int` | get, set | - |
| `CrcPart` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `CrcPart2` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `ClientTimestamp` | `int` | get, set | - |
| `Platform` | `int` | get, set | - |
| `Itemdetails` | `IProtobufRepeatedFieldSubMessageType\<CUserMessage_UtilMsg_Response_ItemDetail\>` | get | - |
| `Itemgroup` | `int` | get, set | - |
| `TotalCount` | `int` | get, set | - |
| `TotalCount2` | `int` | get, set | - |



---

## 🔌 CUserMessage_UtilMsg_Response_ItemDetail

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMessage_UtilMsg_Response_ItemDetail\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Index` | `int` | get, set | - |
| `Hash` | `int` | get, set | - |
| `Crc` | `int` | get, set | - |
| `Name` | `string` | get, set | - |



---

## 🔌 CUserMsg_CustomGameEvent

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_CustomGameEvent\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EventName` | `string` | get, set | - |
| `Data` | `byte[]` | get, set | - |



---

## 🔌 CUserMsg_HudError

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_HudError\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `OrderId` | `int` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Type` | `PARTICLE_MESSAGE` | get, set | - |
| `Index` | `uint` | get, set | - |
| `ReleaseParticleIndex` | `CUserMsg_ParticleManager_ReleaseParticleIndex` | get | - |
| `CreateParticle` | `CUserMsg_ParticleManager_CreateParticle` | get | - |
| `DestroyParticle` | `CUserMsg_ParticleManager_DestroyParticle` | get | - |
| `DestroyParticleInvolving` | `CUserMsg_ParticleManager_DestroyParticleInvolving` | get | - |
| `UpdateParticle` | `CUserMsg_ParticleManager_UpdateParticle_OBSOLETE` | get | - |
| `UpdateParticleFwd` | `CUserMsg_ParticleManager_UpdateParticleFwd_OBSOLETE` | get | - |
| `UpdateParticleOrient` | `CUserMsg_ParticleManager_UpdateParticleOrient_OBSOLETE` | get | - |
| `UpdateParticleFallback` | `CUserMsg_ParticleManager_UpdateParticleFallback` | get | - |
| `UpdateParticleOffset` | `CUserMsg_ParticleManager_UpdateParticleOffset` | get, set | - |
| `UpdateParticleEnt` | `CUserMsg_ParticleManager_UpdateParticleEnt` | get | - |
| `UpdateParticleShouldDraw` | `CUserMsg_ParticleManager_UpdateParticleShouldDraw` | get | - |
| `UpdateParticleSetFrozen` | `CUserMsg_ParticleManager_UpdateParticleSetFrozen` | get | - |
| `ChangeControlPointAttachment` | `CUserMsg_ParticleManager_ChangeControlPointAttachment` | get | - |
| `UpdateEntityPosition` | `CUserMsg_ParticleManager_UpdateEntityPosition` | get | - |
| `SetParticleFowProperties` | `CUserMsg_ParticleManager_SetParticleFoWProperties` | get | - |
| `SetParticleText` | `CUserMsg_ParticleManager_SetParticleText` | get | - |
| `SetParticleShouldCheckFow` | `CUserMsg_ParticleManager_SetParticleShouldCheckFoW` | get | - |
| `SetControlPointModel` | `CUserMsg_ParticleManager_SetControlPointModel` | get | - |
| `SetControlPointSnapshot` | `CUserMsg_ParticleManager_SetControlPointSnapshot` | get | - |
| `SetTextureAttribute` | `CUserMsg_ParticleManager_SetTextureAttribute` | get | - |
| `SetSceneObjectGenericFlag` | `CUserMsg_ParticleManager_SetSceneObjectGenericFlag` | get | - |
| `SetSceneObjectTintAndDesat` | `CUserMsg_ParticleManager_SetSceneObjectTintAndDesat` | get | - |
| `DestroyParticleNamed` | `CUserMsg_ParticleManager_DestroyParticleNamed` | get | - |
| `ParticleSkipToTime` | `CUserMsg_ParticleManager_ParticleSkipToTime` | get | - |
| `ParticleCanFreeze` | `CUserMsg_ParticleManager_ParticleCanFreeze` | get | - |
| `SetNamedValueContext` | `CUserMsg_ParticleManager_SetParticleNamedValueContext` | get | - |
| `UpdateParticleTransform` | `CUserMsg_ParticleManager_UpdateParticleTransform` | get | - |
| `ParticleFreezeTransitionOverride` | `CUserMsg_ParticleManager_ParticleFreezeTransitionOverride` | get | - |
| `FreezeParticleInvolving` | `CUserMsg_ParticleManager_FreezeParticleInvolving` | get | - |
| `AddModellistOverrideElement` | `CUserMsg_ParticleManager_AddModellistOverrideElement` | get | - |
| `ClearModellistOverride` | `CUserMsg_ParticleManager_ClearModellistOverride` | get | - |
| `CreatePhysicsSim` | `CUserMsg_ParticleManager_CreatePhysicsSim` | get | - |
| `DestroyPhysicsSim` | `CUserMsg_ParticleManager_DestroyPhysicsSim` | get | - |
| `SetVdata` | `CUserMsg_ParticleManager_SetVData` | get | - |
| `SetMaterialOverride` | `CUserMsg_ParticleManager_SetMaterialOverride` | get | - |
| `AddFan` | `CUserMsg_ParticleManager_AddFan` | get | - |
| `UpdateFan` | `CUserMsg_ParticleManager_UpdateFan` | get | - |
| `SetParticleClusterGrowth` | `CUserMsg_ParticleManager_SetParticleClusterGrowth` | get | - |
| `RemoveFan` | `CUserMsg_ParticleManager_RemoveFan` | get | - |



---

## 🔌 CUserMsg_ParticleManager_AddFan

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_AddFan\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Active` | `bool` | get, set | - |
| `BoundsMins` | `Vector` | get, set | - |
| `BoundsMaxs` | `Vector` | get, set | - |
| `FanOrigin` | `Vector` | get, set | - |
| `FanOriginOffset` | `Vector` | get, set | - |
| `FanDirection` | `Vector` | get, set | - |
| `Force` | `float` | get, set | - |
| `FanForceCurve` | `string` | get, set | - |
| `Falloff` | `bool` | get, set | - |
| `PullTowardsPoint` | `bool` | get, set | - |
| `CurveMinDist` | `float` | get, set | - |
| `CurveMaxDist` | `float` | get, set | - |
| `FanType` | `uint` | get, set | - |
| `ConeStartRadius` | `float` | get, set | - |
| `ConeEndRadius` | `float` | get, set | - |
| `ConeLength` | `float` | get, set | - |
| `EntityHandle` | `uint` | get, set | - |
| `AttachmentName` | `string` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_AddModellistOverrideElement

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_AddModellistOverrideElement\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ModelName` | `string` | get, set | - |
| `SpawnProbability` | `float` | get, set | - |
| `Groupid` | `uint` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_ChangeControlPointAttachment

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_ChangeControlPointAttachment\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AttachmentOld` | `int` | get, set | - |
| `AttachmentNew` | `int` | get, set | - |
| `EntityHandle` | `uint` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_ClearModellistOverride

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_ClearModellistOverride\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Groupid` | `uint` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_CreateParticle

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_CreateParticle\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ParticleNameIndex` | `ulong` | get, set | - |
| `AttachType` | `int` | get, set | - |
| `EntityHandle` | `uint` | get, set | - |
| `EntityHandleForModifiers` | `uint` | get, set | - |
| `ApplyVoiceBanRules` | `bool` | get, set | - |
| `TeamBehavior` | `int` | get, set | - |
| `ControlPointConfiguration` | `string` | get, set | - |
| `Cluster` | `bool` | get, set | - |
| `EndcapTime` | `float` | get, set | - |
| `AggregationPosition` | `Vector` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_CreatePhysicsSim

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_CreatePhysicsSim\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PropGroupName` | `string` | get, set | - |
| `UseHighQualitySimulation` | `bool` | get, set | - |
| `MaxParticleCount` | `uint` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_DestroyParticle

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_DestroyParticle\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `DestroyImmediately` | `bool` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_DestroyParticleInvolving

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_DestroyParticleInvolving\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `DestroyImmediately` | `bool` | get, set | - |
| `EntityHandle` | `uint` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_DestroyParticleNamed

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_DestroyParticleNamed\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ParticleNameIndex` | `ulong` | get, set | - |
| `EntityHandle` | `uint` | get, set | - |
| `DestroyImmediately` | `bool` | get, set | - |
| `PlayEndcap` | `bool` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_DestroyPhysicsSim

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_DestroyPhysicsSim\>`



---

## 🔌 CUserMsg_ParticleManager_FreezeParticleInvolving

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_FreezeParticleInvolving\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SetFrozen` | `bool` | get, set | - |
| `TransitionDuration` | `float` | get, set | - |
| `EntityHandle` | `uint` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_ParticleCanFreeze

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_ParticleCanFreeze\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CanFreeze` | `bool` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_ParticleFreezeTransitionOverride

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_ParticleFreezeTransitionOverride\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `FreezeTransitionOverride` | `float` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_ParticleSkipToTime

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_ParticleSkipToTime\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SkipToTime` | `float` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_ReleaseParticleIndex

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_ReleaseParticleIndex\>`



---

## 🔌 CUserMsg_ParticleManager_RemoveFan

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_RemoveFan\>`



---

## 🔌 CUserMsg_ParticleManager_SetControlPointModel

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_SetControlPointModel\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ControlPoint` | `int` | get, set | - |
| `ModelName` | `string` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_SetControlPointSnapshot

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_SetControlPointSnapshot\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ControlPoint` | `int` | get, set | - |
| `SnapshotName` | `string` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_SetMaterialOverride

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_SetMaterialOverride\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MaterialName` | `string` | get, set | - |
| `IncludeChildren` | `bool` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_SetParticleClusterGrowth

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_SetParticleClusterGrowth\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Duration` | `float` | get, set | - |
| `Origin` | `Vector` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_SetParticleFoWProperties

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_SetParticleFoWProperties\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `FowControlPoint` | `int` | get, set | - |
| `FowControlPoint2` | `int` | get, set | - |
| `FowRadius` | `float` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_SetParticleNamedValueContext

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_SetParticleNamedValueContext\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `FloatValues` | `IProtobufRepeatedFieldSubMessageType\<CUserMsg_ParticleManager_SetParticleNamedValueContext_FloatContextValue\>` | get | - |
| `VectorValues` | `IProtobufRepeatedFieldSubMessageType\<CUserMsg_ParticleManager_SetParticleNamedValueContext_VectorContextValue\>` | get | - |
| `TransformValues` | `IProtobufRepeatedFieldSubMessageType\<CUserMsg_ParticleManager_SetParticleNamedValueContext_TransformContextValue\>` | get | - |
| `EhandleValues` | `IProtobufRepeatedFieldSubMessageType\<CUserMsg_ParticleManager_SetParticleNamedValueContext_EHandleContext\>` | get | - |



---

## 🔌 CUserMsg_ParticleManager_SetParticleNamedValueContext_EHandleContext

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_SetParticleNamedValueContext_EHandleContext\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ValueNameHash` | `uint` | get, set | - |
| `EntIndex` | `uint` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_SetParticleNamedValueContext_FloatContextValue

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_SetParticleNamedValueContext_FloatContextValue\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ValueNameHash` | `uint` | get, set | - |
| `Value` | `float` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_SetParticleNamedValueContext_TransformContextValue

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_SetParticleNamedValueContext_TransformContextValue\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ValueNameHash` | `uint` | get, set | - |
| `Angles` | `QAngle` | get, set | - |
| `Translation` | `Vector` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_SetParticleNamedValueContext_VectorContextValue

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_SetParticleNamedValueContext_VectorContextValue\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ValueNameHash` | `uint` | get, set | - |
| `Value` | `Vector` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_SetParticleShouldCheckFoW

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_SetParticleShouldCheckFoW\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CheckFow` | `bool` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_SetParticleText

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_SetParticleText\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Text` | `string` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_SetSceneObjectGenericFlag

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_SetSceneObjectGenericFlag\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `FlagValue` | `bool` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_SetSceneObjectTintAndDesat

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_SetSceneObjectTintAndDesat\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Tint` | `uint` | get, set | - |
| `Desat` | `float` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_SetTexture

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`



---

## 🔌 CUserMsg_ParticleManager_SetVData

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_SetVData\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `VdataName` | `string` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_UpdateEntityPosition

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_UpdateEntityPosition\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EntityHandle` | `uint` | get, set | - |
| `Position` | `Vector` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_UpdateFan

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_UpdateFan\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Active` | `bool` | get, set | - |
| `FanOrigin` | `Vector` | get, set | - |
| `FanOriginOffset` | `Vector` | get, set | - |
| `FanDirection` | `Vector` | get, set | - |
| `FanRampRatio` | `float` | get, set | - |
| `BoundsMins` | `Vector` | get, set | - |
| `BoundsMaxs` | `Vector` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_UpdateParticleEnt

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_UpdateParticleEnt\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ControlPoint` | `int` | get, set | - |
| `EntityHandle` | `uint` | get, set | - |
| `AttachType` | `int` | get, set | - |
| `Attachment` | `int` | get, set | - |
| `FallbackPosition` | `Vector` | get, set | - |
| `IncludeWearables` | `bool` | get, set | - |
| `OffsetPosition` | `Vector` | get, set | - |
| `OffsetAngles` | `QAngle` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_UpdateParticleFallback

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_UpdateParticleFallback\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ControlPoint` | `int` | get, set | - |
| `Position` | `Vector` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_UpdateParticleFwd_OBSOLETE

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_UpdateParticleFwd_OBSOLETE\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ControlPoint` | `int` | get, set | - |
| `Forward` | `Vector` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_UpdateParticleOffset

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_UpdateParticleOffset\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ControlPoint` | `int` | get, set | - |
| `OriginOffset` | `Vector` | get, set | - |
| `AngleOffset` | `QAngle` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_UpdateParticleOrient_OBSOLETE

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_UpdateParticleOrient_OBSOLETE\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ControlPoint` | `int` | get, set | - |
| `Forward` | `Vector` | get, set | - |
| `DeprecatedRight` | `Vector` | get, set | - |
| `Up` | `Vector` | get, set | - |
| `Left` | `Vector` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_UpdateParticleSetFrozen

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_UpdateParticleSetFrozen\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SetFrozen` | `bool` | get, set | - |
| `TransitionDuration` | `float` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_UpdateParticleShouldDraw

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_UpdateParticleShouldDraw\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ShouldDraw` | `bool` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_UpdateParticleTransform

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_UpdateParticleTransform\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ControlPoint` | `int` | get, set | - |
| `Position` | `Vector` | get, set | - |
| `Orientation` | `CMsgQuaternion` | get | - |
| `InterpolationInterval` | `float` | get, set | - |



---

## 🔌 CUserMsg_ParticleManager_UpdateParticle_OBSOLETE

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CUserMsg_ParticleManager_UpdateParticle_OBSOLETE\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ControlPoint` | `int` | get, set | - |
| `Position` | `Vector` | get, set | - |



---

## 🔌 CVDiagnostic

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CVDiagnostic\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Id` | `uint` | get, set | - |
| `Extended` | `uint` | get, set | - |
| `Value` | `ulong` | get, set | - |
| `StringValue` | `string` | get, set | - |



---

## 🔌 CWorkshop_AddSpecialPayment_Request

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CWorkshop_AddSpecialPayment_Request\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Appid` | `uint` | get, set | - |
| `Gameitemid` | `uint` | get, set | - |
| `Date` | `string` | get, set | - |
| `PaymentUsUsd` | `ulong` | get, set | - |
| `PaymentRowUsd` | `ulong` | get, set | - |



---

## 🔌 CWorkshop_AddSpecialPayment_Response

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CWorkshop_AddSpecialPayment_Response\>`



---

## 🔌 CWorkshop_GetContributors_Request

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CWorkshop_GetContributors_Request\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Appid` | `uint` | get, set | - |
| `Gameitemid` | `uint` | get, set | - |



---

## 🔌 CWorkshop_GetContributors_Response

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CWorkshop_GetContributors_Response\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Contributors` | `IProtobufRepeatedFieldValueType\<ulong\>` | get | - |



---

## 🔌 CWorkshop_PopulateItemDescriptions_Request

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CWorkshop_PopulateItemDescriptions_Request\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Appid` | `uint` | get, set | - |
| `Languages` | `IProtobufRepeatedFieldSubMessageType\<CWorkshop_PopulateItemDescriptions_Request_ItemDescriptionsLanguageBlock\>` | get | - |



---

## 🔌 CWorkshop_PopulateItemDescriptions_Request_ItemDescriptionsLanguageBlock

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CWorkshop_PopulateItemDescriptions_Request_ItemDescriptionsLanguageBlock\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Language` | `string` | get, set | - |
| `Descriptions` | `IProtobufRepeatedFieldSubMessageType\<CWorkshop_PopulateItemDescriptions_Request_SingleItemDescription\>` | get | - |



---

## 🔌 CWorkshop_PopulateItemDescriptions_Request_SingleItemDescription

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CWorkshop_PopulateItemDescriptions_Request_SingleItemDescription\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Gameitemid` | `uint` | get, set | - |
| `ItemDescription` | `string` | get, set | - |
| `OnePerAccount` | `bool` | get, set | - |



---

## 🔌 CWorkshop_SetItemPaymentRules_Request

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CWorkshop_SetItemPaymentRules_Request\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Appid` | `uint` | get, set | - |
| `Gameitemid` | `uint` | get, set | - |
| `AssociatedWorkshopFiles` | `IProtobufRepeatedFieldSubMessageType\<CWorkshop_SetItemPaymentRules_Request_WorkshopItemPaymentRule\>` | get | - |
| `PartnerAccounts` | `IProtobufRepeatedFieldSubMessageType\<CWorkshop_SetItemPaymentRules_Request_PartnerItemPaymentRule\>` | get | - |
| `ValidateOnly` | `bool` | get, set | - |
| `MakeWorkshopFilesSubscribable` | `bool` | get, set | - |
| `AssociatedWorkshopFileForDirectPayments` | `CWorkshop_SetItemPaymentRules_Request_WorkshopDirectPaymentRule` | get | - |



---

## 🔌 CWorkshop_SetItemPaymentRules_Request_PartnerItemPaymentRule

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CWorkshop_SetItemPaymentRules_Request_PartnerItemPaymentRule\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AccountId` | `uint` | get, set | - |
| `RevenuePercentage` | `float` | get, set | - |
| `RuleDescription` | `string` | get, set | - |



---

## 🔌 CWorkshop_SetItemPaymentRules_Request_WorkshopDirectPaymentRule

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CWorkshop_SetItemPaymentRules_Request_WorkshopDirectPaymentRule\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `WorkshopFileId` | `ulong` | get, set | - |
| `RuleDescription` | `string` | get, set | - |



---

## 🔌 CWorkshop_SetItemPaymentRules_Request_WorkshopItemPaymentRule

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CWorkshop_SetItemPaymentRules_Request_WorkshopItemPaymentRule\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `WorkshopFileId` | `ulong` | get, set | - |
| `RevenuePercentage` | `float` | get, set | - |
| `RuleDescription` | `string` | get, set | - |
| `RuleType` | `uint` | get, set | - |



---

## 🔌 CWorkshop_SetItemPaymentRules_Response

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CWorkshop_SetItemPaymentRules_Response\>`



---

## 📋 DIALOG_TYPE

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `DIALOG_MSG` | `0` | - |
| `DIALOG_MENU` | `1` | - |
| `DIALOG_TEXT` | `2` | - |
| `DIALOG_ENTRY` | `3` | - |
| `DIALOG_ASKCONNECT` | `4` | - |



---

## 🔌 DataCenterPing

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<DataCenterPing\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `DataCenterId` | `uint` | get, set | - |
| `Ping` | `int` | get, set | - |



---

## 🔌 DeepPlayerMatchEvent

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<DeepPlayerMatchEvent\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Accountid` | `uint` | get, set | - |
| `MatchId` | `ulong` | get, set | - |
| `EventId` | `uint` | get, set | - |
| `EventType` | `uint` | get, set | - |
| `BPlayingCt` | `bool` | get, set | - |
| `UserPosX` | `int` | get, set | - |
| `UserPosY` | `int` | get, set | - |
| `UserPosZ` | `int` | get, set | - |
| `UserDefidx` | `uint` | get, set | - |
| `OtherPosX` | `int` | get, set | - |
| `OtherPosY` | `int` | get, set | - |
| `OtherPosZ` | `int` | get, set | - |
| `OtherDefidx` | `uint` | get, set | - |
| `EventData` | `int` | get, set | - |



---

## 🔌 DeepPlayerStatsEntry

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<DeepPlayerStatsEntry\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Accountid` | `uint` | get, set | - |
| `MatchId` | `ulong` | get, set | - |
| `MmGameMode` | `uint` | get, set | - |
| `Mapid` | `uint` | get, set | - |
| `BStartingCt` | `bool` | get, set | - |
| `MatchOutcome` | `uint` | get, set | - |
| `RoundsWon` | `uint` | get, set | - |
| `RoundsLost` | `uint` | get, set | - |
| `StatScore` | `uint` | get, set | - |
| `StatDeaths` | `uint` | get, set | - |
| `StatMvps` | `uint` | get, set | - |
| `EnemyKills` | `uint` | get, set | - |
| `EnemyHeadshots` | `uint` | get, set | - |
| `Enemy2ks` | `uint` | get, set | - |
| `Enemy3ks` | `uint` | get, set | - |
| `Enemy4ks` | `uint` | get, set | - |
| `TotalDamage` | `uint` | get, set | - |
| `EngagementsEntryCount` | `uint` | get, set | - |
| `EngagementsEntryWins` | `uint` | get, set | - |
| `Engagements1v1Count` | `uint` | get, set | - |
| `Engagements1v1Wins` | `uint` | get, set | - |
| `Engagements1v2Count` | `uint` | get, set | - |
| `Engagements1v2Wins` | `uint` | get, set | - |
| `UtilityCount` | `uint` | get, set | - |
| `UtilitySuccess` | `uint` | get, set | - |
| `FlashCount` | `uint` | get, set | - |
| `FlashSuccess` | `uint` | get, set | - |
| `Mates` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |



---

## 🔌 DetailedSearchStatistic

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<DetailedSearchStatistic\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `GameType` | `uint` | get, set | - |
| `SearchTimeAvg` | `uint` | get, set | - |
| `PlayersSearching` | `uint` | get, set | - |



---

## 📋 EBaseClientMessages

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `CM_CustomGameEvent` | `280` | - |
| `CM_CustomGameEventBounce` | `281` | - |
| `CM_ClientUIEvent` | `282` | - |
| `CM_DevPaletteVisibilityChanged` | `283` | - |
| `CM_WorldUIControllerHasPanelChanged` | `284` | - |
| `CM_RotateAnchor` | `285` | - |
| `CM_ListenForResponseFound` | `286` | - |
| `CM_MAX_BASE` | `300` | - |



---

## 📋 EBaseEntityMessages

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `EM_PlayJingle` | `136` | - |
| `EM_ScreenOverlay` | `137` | - |
| `EM_RemoveAllDecals` | `138` | - |
| `EM_PropagateForce` | `139` | - |
| `EM_DoSpark` | `140` | - |
| `EM_FixAngle` | `141` | - |



---

## 📋 EBaseGameEvents

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `GE_VDebugGameSessionIDEvent` | `200` | - |
| `GE_PlaceDecalEvent` | `201` | - |
| `GE_ClearWorldDecalsEvent` | `202` | - |
| `GE_ClearEntityDecalsEvent` | `203` | - |
| `GE_ClearDecalsForEntityEvent` | `204` | - |
| `GE_Source1LegacyGameEventList` | `205` | - |
| `GE_Source1LegacyListenEvents` | `206` | - |
| `GE_Source1LegacyGameEvent` | `207` | - |
| `GE_SosStartSoundEvent` | `208` | - |
| `GE_SosStopSoundEvent` | `209` | - |
| `GE_SosSetSoundEventParams` | `210` | - |
| `GE_SosSetLibraryStackFields` | `211` | - |
| `GE_SosStopSoundEventHash` | `212` | - |



---

## 📋 EBasePredictionEvents

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `BPE_StringCommand` | `128` | - |
| `BPE_Teleport` | `130` | - |
| `BPE_Diagnostic` | `16384` | - |



---

## 📋 EBaseUserMessages

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `UM_AchievementEvent` | `101` | - |
| `UM_CloseCaption` | `102` | - |
| `UM_CloseCaptionDirect` | `103` | - |
| `UM_CurrentTimescale` | `104` | - |
| `UM_DesiredTimescale` | `105` | - |
| `UM_Fade` | `106` | - |
| `UM_GameTitle` | `107` | - |
| `UM_HudMsg` | `110` | - |
| `UM_HudText` | `111` | - |
| `UM_ColoredText` | `113` | - |
| `UM_RequestState` | `114` | - |
| `UM_ResetHUD` | `115` | - |
| `UM_Rumble` | `116` | - |
| `UM_SayText` | `117` | - |
| `UM_SayText2` | `118` | - |
| `UM_SayTextChannel` | `119` | - |
| `UM_Shake` | `120` | - |
| `UM_ShakeDir` | `121` | - |
| `UM_WaterShake` | `122` | - |
| `UM_TextMsg` | `124` | - |
| `UM_ScreenTilt` | `125` | - |
| `UM_VoiceMask` | `128` | - |
| `UM_SendAudio` | `130` | - |
| `UM_ItemPickup` | `131` | - |
| `UM_AmmoDenied` | `132` | - |
| `UM_ShowMenu` | `134` | - |
| `UM_CreditsMsg` | `135` | - |
| `UM_CloseCaptionPlaceholder` | `142` | - |
| `UM_CameraTransition` | `143` | - |
| `UM_AudioParameter` | `144` | - |
| `UM_ParticleManager` | `145` | - |
| `UM_HudError` | `146` | - |
| `UM_CustomGameEvent` | `148` | - |
| `UM_AnimGraphUpdate` | `149` | - |
| `UM_HapticsManagerPulse` | `150` | - |
| `UM_HapticsManagerEffect` | `151` | - |
| `UM_UpdateCssClasses` | `153` | - |
| `UM_ServerFrameTime` | `154` | - |
| `UM_LagCompensationError` | `155` | - |
| `UM_RequestDllStatus` | `156` | - |
| `UM_RequestUtilAction` | `157` | - |
| `UM_UtilActionResponse` | `158` | - |
| `UM_DllStatusResponse` | `159` | - |
| `UM_RequestInventory` | `160` | - |
| `UM_InventoryResponse` | `161` | - |
| `UM_RequestDiagnostic` | `162` | - |
| `UM_DiagnosticResponse` | `163` | - |
| `UM_ExtraUserData` | `164` | - |
| `UM_NotifyResponseFound` | `165` | - |
| `UM_PlayResponseConditional` | `166` | - |
| `UM_MAX_BASE` | `200` | - |



---

## 📋 ECSPredictionEvents

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `CSPE_DamageTag` | `1` | - |
| `CSPE_AddAimPunch` | `3` | - |



---

## 📋 ECSUsrMsg_DisconnectToLobby_Action

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `k_ECSUsrMsg_DisconnectToLobby_Action_Default` | `0` | - |
| `k_ECSUsrMsg_DisconnectToLobby_Action_GoQueue` | `1` | - |



---

## 📋 EClientPersonaStateFlag

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `k_EClientPersonaStateFlagStatus` | `1` | - |
| `k_EClientPersonaStateFlagPlayerName` | `2` | - |
| `k_EClientPersonaStateFlagQueryPort` | `4` | - |
| `k_EClientPersonaStateFlagSourceID` | `8` | - |
| `k_EClientPersonaStateFlagPresence` | `16` | - |
| `k_EClientPersonaStateFlagLastSeen` | `64` | - |
| `k_EClientPersonaStateFlagUserClanRank` | `128` | - |
| `k_EClientPersonaStateGameExtraInfo` | `256` | - |
| `k_EClientPersonaStateGameDataBlob` | `512` | - |
| `k_EClientPersonaStateFlagClanData` | `1024` | - |
| `k_EClientPersonaStateFlagFacebook` | `2048` | - |
| `k_EClientPersonaStateFlagRichPresence` | `4096` | - |
| `k_EClientPersonaStateFlagBroadcast` | `8192` | - |
| `k_EClientPersonaStateFlagWatching` | `16384` | - |



---

## 📋 EClientReportingVersion

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `k_EClientReportingVersion_OldVersion` | `0` | - |
| `k_EClientReportingVersion_BetaVersion` | `1` | - |
| `k_EClientReportingVersion_SupportsTrustedMode` | `2` | - |



---

## 📋 EClientUIEvent

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `EClientUIEvent_Invalid` | `0` | - |
| `EClientUIEvent_DialogFinished` | `1` | - |
| `EClientUIEvent_FireOutput` | `2` | - |



---

## 📋 ECodecUsagePlatform

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `k_ECodecUsagePlatformUnknown` | `0` | - |
| `k_ECodecUsagePlatformWindows` | `1` | - |
| `k_ECodecUsagePlatformMacOS` | `2` | - |
| `k_ECodecUsagePlatformLinux` | `3` | - |
| `k_ECodecUsagePlatformSteamDeck` | `4` | - |



---

## 📋 ECodecUsageReason

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `k_ECodecUsageReasonUnknown` | `0` | - |
| `k_ECodecUsageReasonRemotePlay` | `1` | - |
| `k_ECodecUsageReasonBroadcasting` | `2` | - |
| `k_ECodecUsageReasonGameVideo` | `3` | - |



---

## 📋 ECommunityItem

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `k_ECommunityItemAttribute_Invalid` | `0` | - |
| `k_ECommunityItemAttribute_CardBorder` | `1` | - |
| `k_ECommunityItemAttribute_Level` | `2` | - |
| `k_ECommunityItemAttribute_IssueNumber` | `3` | - |
| `k_ECommunityItemAttribute_TradableTime` | `4` | - |
| `k_ECommunityItemAttribute_StorePackageID` | `5` | - |
| `k_ECommunityItemAttribute_CommunityItemAppID` | `6` | - |
| `k_ECommunityItemAttribute_CommunityItemType` | `7` | - |
| `k_ECommunityItemAttribute_ProfileModiferEnabled` | `8` | - |
| `k_ECommunityItemAttribute_ExpiryTime` | `9` | - |



---

## 📋 ECommunityItemClass

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `k_ECommunityItemClass_Invalid` | `0` | - |
| `k_ECommunityItemClass_Badge` | `1` | - |
| `k_ECommunityItemClass_GameCard` | `2` | - |
| `k_ECommunityItemClass_ProfileBackground` | `3` | - |
| `k_ECommunityItemClass_Emoticon` | `4` | - |
| `k_ECommunityItemClass_BoosterPack` | `5` | - |
| `k_ECommunityItemClass_Consumable` | `6` | - |
| `k_ECommunityItemClass_GameGoo` | `7` | - |
| `k_ECommunityItemClass_ProfileModifier` | `8` | - |
| `k_ECommunityItemClass_Scene` | `9` | - |
| `k_ECommunityItemClass_SalienItem` | `10` | - |



---

## 📋 ECsgoGCMsg

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `k_EMsgGCCStrike15_v2_Base` | `9100` | - |
| `k_EMsgGCCStrike15_v2_MatchmakingStart` | `9101` | - |
| `k_EMsgGCCStrike15_v2_MatchmakingStop` | `9102` | - |
| `k_EMsgGCCStrike15_v2_MatchmakingClient2ServerPing` | `9103` | - |
| `k_EMsgGCCStrike15_v2_MatchmakingGC2ClientUpdate` | `9104` | - |
| `k_EMsgGCCStrike15_v2_MatchmakingServerReservationResponse` | `9106` | - |
| `k_EMsgGCCStrike15_v2_MatchmakingGC2ClientReserve` | `9107` | - |
| `k_EMsgGCCStrike15_v2_MatchmakingClient2GCHello` | `9109` | - |
| `k_EMsgGCCStrike15_v2_MatchmakingGC2ClientHello` | `9110` | - |
| `k_EMsgGCCStrike15_v2_MatchmakingGC2ClientAbandon` | `9112` | - |
| `k_EMsgGCCStrike15_v2_MatchmakingOperator2GCBlogUpdate` | `9117` | - |
| `k_EMsgGCCStrike15_v2_ServerNotificationForUserPenalty` | `9118` | - |
| `k_EMsgGCCStrike15_v2_ClientReportPlayer` | `9119` | - |
| `k_EMsgGCCStrike15_v2_ClientReportServer` | `9120` | - |
| `k_EMsgGCCStrike15_v2_ClientCommendPlayer` | `9121` | - |
| `k_EMsgGCCStrike15_v2_ClientReportResponse` | `9122` | - |
| `k_EMsgGCCStrike15_v2_ClientCommendPlayerQuery` | `9123` | - |
| `k_EMsgGCCStrike15_v2_ClientCommendPlayerQueryResponse` | `9124` | - |
| `k_EMsgGCCStrike15_v2_WatchInfoUsers` | `9126` | - |
| `k_EMsgGCCStrike15_v2_ClientRequestPlayersProfile` | `9127` | - |
| `k_EMsgGCCStrike15_v2_PlayersProfile` | `9128` | - |
| `k_EMsgGCCStrike15_v2_PlayerOverwatchCaseUpdate` | `9131` | - |
| `k_EMsgGCCStrike15_v2_PlayerOverwatchCaseAssignment` | `9132` | - |
| `k_EMsgGCCStrike15_v2_PlayerOverwatchCaseStatus` | `9133` | - |
| `k_EMsgGCCStrike15_v2_GC2ClientTextMsg` | `9134` | - |
| `k_EMsgGCCStrike15_v2_Client2GCTextMsg` | `9135` | - |
| `k_EMsgGCCStrike15_v2_MatchEndRunRewardDrops` | `9136` | - |
| `k_EMsgGCCStrike15_v2_MatchEndRewardDropsNotification` | `9137` | - |
| `k_EMsgGCCStrike15_v2_ClientRequestWatchInfoFriends2` | `9138` | - |
| `k_EMsgGCCStrike15_v2_MatchList` | `9139` | - |
| `k_EMsgGCCStrike15_v2_MatchListRequestCurrentLiveGames` | `9140` | - |
| `k_EMsgGCCStrike15_v2_MatchListRequestRecentUserGames` | `9141` | - |
| `k_EMsgGCCStrike15_v2_GC2ServerReservationUpdate` | `9142` | - |
| `k_EMsgGCCStrike15_v2_ClientVarValueNotificationInfo` | `9144` | - |
| `k_EMsgGCCStrike15_v2_MatchListRequestTournamentGames` | `9146` | - |
| `k_EMsgGCCStrike15_v2_MatchListRequestFullGameInfo` | `9147` | - |
| `k_EMsgGCCStrike15_v2_GiftsLeaderboardRequest` | `9148` | - |
| `k_EMsgGCCStrike15_v2_GiftsLeaderboardResponse` | `9149` | - |
| `k_EMsgGCCStrike15_v2_ServerVarValueNotificationInfo` | `9150` | - |
| `k_EMsgGCCStrike15_v2_ClientSubmitSurveyVote` | `9152` | - |
| `k_EMsgGCCStrike15_v2_Server2GCClientValidate` | `9153` | - |
| `k_EMsgGCCStrike15_v2_MatchListRequestLiveGameForUser` | `9154` | - |
| `k_EMsgGCCStrike15_v2_Client2GCEconPreviewDataBlockRequest` | `9156` | - |
| `k_EMsgGCCStrike15_v2_Client2GCEconPreviewDataBlockResponse` | `9157` | - |
| `k_EMsgGCCStrike15_v2_AccountPrivacySettings` | `9158` | - |
| `k_EMsgGCCStrike15_v2_SetMyActivityInfo` | `9159` | - |
| `k_EMsgGCCStrike15_v2_MatchListRequestTournamentPredictions` | `9160` | - |
| `k_EMsgGCCStrike15_v2_MatchListUploadTournamentPredictions` | `9161` | - |
| `k_EMsgGCCStrike15_v2_DraftSummary` | `9162` | - |
| `k_EMsgGCCStrike15_v2_ClientRequestJoinFriendData` | `9163` | - |
| `k_EMsgGCCStrike15_v2_ClientRequestJoinServerData` | `9164` | - |
| `k_EMsgGCCStrike15_v2_GC2ClientTournamentInfo` | `9167` | - |
| `k_EMsgGC_GlobalGame_Subscribe` | `9168` | - |
| `k_EMsgGC_GlobalGame_Unsubscribe` | `9169` | - |
| `k_EMsgGC_GlobalGame_Play` | `9170` | - |
| `k_EMsgGCCStrike15_v2_AcknowledgePenalty` | `9171` | - |
| `k_EMsgGCCStrike15_v2_Client2GCRequestPrestigeCoin` | `9172` | - |
| `k_EMsgGCCStrike15_v2_GC2ClientGlobalStats` | `9173` | - |
| `k_EMsgGCCStrike15_v2_Client2GCStreamUnlock` | `9174` | - |
| `k_EMsgGCCStrike15_v2_FantasyRequestClientData` | `9175` | - |
| `k_EMsgGCCStrike15_v2_FantasyUpdateClientData` | `9176` | - |
| `k_EMsgGCCStrike15_v2_GCToClientSteamdatagramTicket` | `9177` | - |
| `k_EMsgGCCStrike15_v2_ClientToGCRequestTicket` | `9178` | - |
| `k_EMsgGCCStrike15_v2_ClientToGCRequestElevate` | `9179` | - |
| `k_EMsgGCCStrike15_v2_GlobalChat` | `9180` | - |
| `k_EMsgGCCStrike15_v2_GlobalChat_Subscribe` | `9181` | - |
| `k_EMsgGCCStrike15_v2_GlobalChat_Unsubscribe` | `9182` | - |
| `k_EMsgGCCStrike15_v2_ClientAuthKeyCode` | `9183` | - |
| `k_EMsgGCCStrike15_v2_GotvSyncPacket` | `9184` | - |
| `k_EMsgGCCStrike15_v2_ClientPlayerDecalSign` | `9185` | - |
| `k_EMsgGCCStrike15_v2_ClientLogonFatalError` | `9187` | - |
| `k_EMsgGCCStrike15_v2_ClientPollState` | `9188` | - |
| `k_EMsgGCCStrike15_v2_Party_Register` | `9189` | - |
| `k_EMsgGCCStrike15_v2_Party_Unregister` | `9190` | - |
| `k_EMsgGCCStrike15_v2_Party_Search` | `9191` | - |
| `k_EMsgGCCStrike15_v2_Party_Invite` | `9192` | - |
| `k_EMsgGCCStrike15_v2_Account_RequestCoPlays` | `9193` | - |
| `k_EMsgGCCStrike15_v2_ClientGCRankUpdate` | `9194` | - |
| `k_EMsgGCCStrike15_v2_ClientRequestOffers` | `9195` | - |
| `k_EMsgGCCStrike15_v2_ClientAccountBalance` | `9196` | - |
| `k_EMsgGCCStrike15_v2_ClientPartyJoinRelay` | `9197` | - |
| `k_EMsgGCCStrike15_v2_ClientPartyWarning` | `9198` | - |
| `k_EMsgGCCStrike15_v2_SetEventFavorite` | `9200` | - |
| `k_EMsgGCCStrike15_v2_GetEventFavorites_Request` | `9201` | - |
| `k_EMsgGCCStrike15_v2_ClientPerfReport` | `9202` | - |
| `k_EMsgGCCStrike15_v2_GetEventFavorites_Response` | `9203` | - |
| `k_EMsgGCCStrike15_v2_ClientRequestSouvenir` | `9204` | - |
| `k_EMsgGCCStrike15_v2_ClientReportValidation` | `9205` | - |
| `k_EMsgGCCStrike15_v2_GC2ClientRefuseSecureMode` | `9206` | - |
| `k_EMsgGCCStrike15_v2_GC2ClientRequestValidation` | `9207` | - |
| `k_EMsgGCCStrike15_v2_ClientRedeemMissionReward` | `9209` | - |
| `k_EMsgGCCStrike15_ClientDeepStats` | `9210` | - |
| `k_EMsgGCCStrike15_StartAgreementSessionInGame` | `9211` | - |
| `k_EMsgGCCStrike15_v2_GC2ClientInitSystem` | `9212` | - |
| `k_EMsgGCCStrike15_v2_GC2ClientInitSystem_Response` | `9213` | - |
| `k_EMsgGCCStrike15_v2_PrivateQueues` | `9214` | - |
| `k_EMsgGCCStrike15_v2_MatchListTournamentOperatorMgmt` | `9215` | - |
| `k_EMsgGCCStrike15_v2_BetaEnrollment` | `9217` | - |
| `k_EMsgGCCStrike15_v2_SetPlayerLeaderboardSafeName` | `9218` | - |
| `k_EMsgGCCStrike15_v2_ClientRedeemFreeReward` | `9219` | - |
| `k_EMsgGCCStrike15_v2_ClientNetworkConfig` | `9220` | - |
| `k_EMsgGCCStrike15_v2_GC2ClientNotifyXPShop` | `9221` | - |
| `k_EMsgGCCStrike15_v2_Client2GcAckXPShopTracks` | `9222` | - |
| `k_EMsgGCCStrike15_v2_MatchmakingGC2ClientSearchStats` | `9223` | - |
| `k_EMsgGCCStrike15_v2_PremierSeasonSummary` | `9224` | - |
| `k_EMsgGCCStrike15_v2_RequestRecurringMissionSchedule` | `9225` | - |
| `k_EMsgGCCStrike15_v2_RecurringMissionSchema` | `9226` | - |
| `k_EMsgGCCStrike15_v2_VolatileItemClaimReward` | `9227` | - |



---

## 📋 ECsgoGameEvents

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `GE_PlayerAnimEventId` | `450` | - |
| `GE_RadioIconEventId` | `451` | - |
| `GE_FireBulletsId` | `452` | - |
| `GE_PlayerBulletHitId` | `453` | - |



---

## 📋 ECsgoSteamUserStat

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `k_ECsgoSteamUserStat_XpEarnedGames` | `1` | - |
| `k_ECsgoSteamUserStat_MatchWinsCompetitive` | `2` | - |
| `k_ECsgoSteamUserStat_SurvivedDangerZone` | `3` | - |



---

## 📋 ECstrike15UserMessages

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `CS_UM_VGUIMenu` | `301` | - |
| `CS_UM_Geiger` | `302` | - |
| `CS_UM_Train` | `303` | - |
| `CS_UM_HudText` | `304` | - |
| `CS_UM_SayText` | `305` | - |
| `CS_UM_SayText2` | `306` | - |
| `CS_UM_TextMsg` | `307` | - |
| `CS_UM_HudMsg` | `308` | - |
| `CS_UM_ResetHud` | `309` | - |
| `CS_UM_GameTitle` | `310` | - |
| `CS_UM_Shake` | `312` | - |
| `CS_UM_Fade` | `313` | - |
| `CS_UM_Rumble` | `314` | - |
| `CS_UM_CloseCaption` | `315` | - |
| `CS_UM_CloseCaptionDirect` | `316` | - |
| `CS_UM_SendAudio` | `317` | - |
| `CS_UM_RawAudio` | `318` | - |
| `CS_UM_VoiceMask` | `319` | - |
| `CS_UM_RequestState` | `320` | - |
| `CS_UM_Damage` | `321` | - |
| `CS_UM_RadioText` | `322` | - |
| `CS_UM_HintText` | `323` | - |
| `CS_UM_KeyHintText` | `324` | - |
| `CS_UM_ProcessSpottedEntityUpdate` | `325` | - |
| `CS_UM_ReloadEffect` | `326` | - |
| `CS_UM_AdjustMoney` | `327` | - |
| `CS_UM_UpdateTeamMoney` | `328` | - |
| `CS_UM_StopSpectatorMode` | `329` | - |
| `CS_UM_KillCam` | `330` | - |
| `CS_UM_DesiredTimescale` | `331` | - |
| `CS_UM_CurrentTimescale` | `332` | - |
| `CS_UM_AchievementEvent` | `333` | - |
| `CS_UM_MatchEndConditions` | `334` | - |
| `CS_UM_DisconnectToLobby` | `335` | - |
| `CS_UM_PlayerStatsUpdate` | `336` | - |
| `CS_UM_ClientInfo` | `339` | - |
| `CS_UM_XRankGet` | `340` | - |
| `CS_UM_XRankUpd` | `341` | - |
| `CS_UM_CallVoteFailed` | `345` | - |
| `CS_UM_VoteStart` | `346` | - |
| `CS_UM_VotePass` | `347` | - |
| `CS_UM_VoteFailed` | `348` | - |
| `CS_UM_VoteSetup` | `349` | - |
| `CS_UM_ServerRankRevealAll` | `350` | - |
| `CS_UM_SendLastKillerDamageToClient` | `351` | - |
| `CS_UM_ServerRankUpdate` | `352` | - |
| `CS_UM_ItemPickup` | `353` | - |
| `CS_UM_ShowMenu` | `354` | - |
| `CS_UM_BarTime` | `355` | - |
| `CS_UM_AmmoDenied` | `356` | - |
| `CS_UM_MarkAchievement` | `357` | - |
| `CS_UM_MatchStatsUpdate` | `358` | - |
| `CS_UM_ItemDrop` | `359` | - |
| `CS_UM_SendPlayerItemDrops` | `361` | - |
| `CS_UM_RoundBackupFilenames` | `362` | - |
| `CS_UM_SendPlayerItemFound` | `363` | - |
| `CS_UM_ReportHit` | `364` | - |
| `CS_UM_XpUpdate` | `365` | - |
| `CS_UM_QuestProgress` | `366` | - |
| `CS_UM_ScoreLeaderboardData` | `367` | - |
| `CS_UM_PlayerDecalDigitalSignature` | `368` | - |
| `CS_UM_WeaponSound` | `369` | - |
| `CS_UM_UpdateScreenHealthBar` | `370` | - |
| `CS_UM_EntityOutlineHighlight` | `371` | - |
| `CS_UM_SSUI` | `372` | - |
| `CS_UM_SurvivalStats` | `373` | - |
| `CS_UM_DisconnectToLobby2` | `374` | - |
| `CS_UM_EndOfMatchAllPlayersData` | `375` | - |
| `CS_UM_PostRoundDamageReport` | `376` | - |
| `CS_UM_RoundEndReportData` | `379` | - |
| `CS_UM_CurrentRoundOdds` | `380` | - |
| `CS_UM_DeepStats` | `381` | - |
| `CS_UM_ShootInfo` | `383` | - |
| `CS_UM_CounterStrafe` | `385` | - |
| `CS_UM_DamagePrediction` | `386` | - |
| `CS_UM_RecurringMissionSchema` | `387` | - |
| `CS_UM_SendPlayerLoadout` | `388` | - |



---

## 📋 EDemoCommands

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `DEM_Error` | `-1` | - |
| `DEM_Stop` | `0` | - |
| `DEM_FileHeader` | `1` | - |
| `DEM_FileInfo` | `2` | - |
| `DEM_SyncTick` | `3` | - |
| `DEM_SendTables` | `4` | - |
| `DEM_ClassInfo` | `5` | - |
| `DEM_StringTables` | `6` | - |
| `DEM_Packet` | `7` | - |
| `DEM_SignonPacket` | `8` | - |
| `DEM_ConsoleCmd` | `9` | - |
| `DEM_CustomData` | `10` | - |
| `DEM_CustomDataCallbacks` | `11` | - |
| `DEM_UserCmd` | `12` | - |
| `DEM_FullPacket` | `13` | - |
| `DEM_SaveGame` | `14` | - |
| `DEM_SpawnGroups` | `15` | - |
| `DEM_AnimationData` | `16` | - |
| `DEM_AnimationHeader` | `17` | - |
| `DEM_Recovery` | `18` | - |
| `DEM_Max` | `19` | - |
| `DEM_IsCompressed` | `64` | - |



---

## 📋 EGCBaseClientMsg

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `k_EMsgGCClientWelcome` | `4004` | - |
| `k_EMsgGCServerWelcome` | `4005` | - |
| `k_EMsgGCClientHello` | `4006` | - |
| `k_EMsgGCServerHello` | `4007` | - |
| `k_EMsgGCClientConnectionStatus` | `4009` | - |
| `k_EMsgGCServerConnectionStatus` | `4010` | - |
| `k_EMsgGCClientHelloPartner` | `4011` | - |
| `k_EMsgGCClientHelloPW` | `4012` | - |
| `k_EMsgGCClientHelloR2` | `4013` | - |
| `k_EMsgGCClientHelloR3` | `4014` | - |
| `k_EMsgGCClientHelloR4` | `4015` | - |



---

## 📋 EGCBaseMsg

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `k_EMsgGCSystemMessage` | `4001` | - |
| `k_EMsgGCReplicateConVars` | `4002` | - |
| `k_EMsgGCConVarUpdated` | `4003` | - |
| `k_EMsgGCInQueue` | `4008` | - |
| `k_EMsgGCInviteToParty` | `4501` | - |
| `k_EMsgGCInvitationCreated` | `4502` | - |
| `k_EMsgGCPartyInviteResponse` | `4503` | - |
| `k_EMsgGCKickFromParty` | `4504` | - |
| `k_EMsgGCLeaveParty` | `4505` | - |
| `k_EMsgGCServerAvailable` | `4506` | - |
| `k_EMsgGCClientConnectToServer` | `4507` | - |
| `k_EMsgGCGameServerInfo` | `4508` | - |
| `k_EMsgGCError` | `4509` | - |
| `k_EMsgGCReplay_UploadedToYouTube` | `4510` | - |
| `k_EMsgGCLANServerAvailable` | `4511` | - |



---

## 📋 EGCBaseProtoObjectTypes

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `k_EProtoObjectPartyInvite` | `1001` | - |
| `k_EProtoObjectLobbyInvite` | `1002` | - |



---

## 📋 EGCItemCustomizationNotification

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `k_EGCItemCustomizationNotification_NameItem` | `1006` | - |
| `k_EGCItemCustomizationNotification_UnlockCrate` | `1007` | - |
| `k_EGCItemCustomizationNotification_XRayItemReveal` | `1008` | - |
| `k_EGCItemCustomizationNotification_XRayItemClaim` | `1009` | - |
| `k_EGCItemCustomizationNotification_CasketTooFull` | `1011` | - |
| `k_EGCItemCustomizationNotification_CasketContents` | `1012` | - |
| `k_EGCItemCustomizationNotification_CasketAdded` | `1013` | - |
| `k_EGCItemCustomizationNotification_CasketRemoved` | `1014` | - |
| `k_EGCItemCustomizationNotification_CasketInvFull` | `1015` | - |
| `k_EGCItemCustomizationNotification_NameBaseItem` | `1019` | - |
| `k_EGCItemCustomizationNotification_RemoveItemName` | `1030` | - |
| `k_EGCItemCustomizationNotification_RemoveSticker` | `1053` | - |
| `k_EGCItemCustomizationNotification_ExtractSticker` | `1054` | - |
| `k_EGCItemCustomizationNotification_EncapsulateSticker` | `1055` | - |
| `k_EGCItemCustomizationNotification_ApplySticker` | `1086` | - |
| `k_EGCItemCustomizationNotification_StatTrakSwap` | `1088` | - |
| `k_EGCItemCustomizationNotification_RemovePatch` | `1089` | - |
| `k_EGCItemCustomizationNotification_ApplyPatch` | `1090` | - |
| `k_EGCItemCustomizationNotification_ApplyKeychain` | `1091` | - |
| `k_EGCItemCustomizationNotification_RemoveKeychain` | `1092` | - |
| `k_EGCItemCustomizationNotification_ActivateFanToken` | `9178` | - |
| `k_EGCItemCustomizationNotification_ActivateOperationCoin` | `9179` | - |
| `k_EGCItemCustomizationNotification_GraffitiUnseal` | `9185` | - |
| `k_EGCItemCustomizationNotification_GenerateSouvenir` | `9204` | - |
| `k_EGCItemCustomizationNotification_ClientRedeemMissionReward` | `9209` | - |
| `k_EGCItemCustomizationNotification_ClientRedeemFreeReward` | `9219` | - |
| `k_EGCItemCustomizationNotification_XpShopUseTicket` | `9221` | - |
| `k_EGCItemCustomizationNotification_XpShopAckTracks` | `9222` | - |



---

## 📋 EGCItemMsg

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `k_EMsgGCBase` | `1000` | - |
| `k_EMsgGCSetItemPosition` | `1001` | - |
| `k_EMsgGCCraft` | `1002` | - |
| `k_EMsgGCCraftResponse` | `1003` | - |
| `k_EMsgGCDelete` | `1004` | - |
| `k_EMsgGCVerifyCacheSubscription` | `1005` | - |
| `k_EMsgGCNameItem` | `1006` | - |
| `k_EMsgGCUnlockCrate_DEPRECATED` | `1007` | - |
| `k_EMsgGCUnlockCrateResponse` | `1008` | - |
| `k_EMsgGCPaintItem` | `1009` | - |
| `k_EMsgGCPaintItemResponse` | `1010` | - |
| `k_EMsgGCGoldenWrenchBroadcast` | `1011` | - |
| `k_EMsgGCMOTDRequest` | `1012` | - |
| `k_EMsgGCMOTDRequestResponse` | `1013` | - |
| `k_EMsgGCAddItemToSocket_DEPRECATED` | `1014` | - |
| `k_EMsgGCAddItemToSocketResponse_DEPRECATED` | `1015` | - |
| `k_EMsgGCAddSocketToBaseItem_DEPRECATED` | `1016` | - |
| `k_EMsgGCAddSocketToItem_DEPRECATED` | `1017` | - |
| `k_EMsgGCAddSocketToItemResponse_DEPRECATED` | `1018` | - |
| `k_EMsgGCNameBaseItem` | `1019` | - |
| `k_EMsgGCNameBaseItemResponse` | `1020` | - |
| `k_EMsgGCRemoveSocketItem_DEPRECATED` | `1021` | - |
| `k_EMsgGCRemoveSocketItemResponse_DEPRECATED` | `1022` | - |
| `k_EMsgGCCustomizeItemTexture` | `1023` | - |
| `k_EMsgGCCustomizeItemTextureResponse` | `1024` | - |
| `k_EMsgGCUseItemRequest` | `1025` | - |
| `k_EMsgGCUseItemResponse` | `1026` | - |
| `k_EMsgGCGiftedItems_DEPRECATED` | `1027` | - |
| `k_EMsgGCRemoveItemName` | `1030` | - |
| `k_EMsgGCRemoveItemPaint` | `1031` | - |
| `k_EMsgGCGiftWrapItem` | `1032` | - |
| `k_EMsgGCGiftWrapItemResponse` | `1033` | - |
| `k_EMsgGCDeliverGift` | `1034` | - |
| `k_EMsgGCDeliverGiftResponseGiver` | `1035` | - |
| `k_EMsgGCDeliverGiftResponseReceiver` | `1036` | - |
| `k_EMsgGCUnwrapGiftRequest` | `1037` | - |
| `k_EMsgGCUnwrapGiftResponse` | `1038` | - |
| `k_EMsgGCSetItemStyle` | `1039` | - |
| `k_EMsgGCUsedClaimCodeItem` | `1040` | - |
| `k_EMsgGCSortItems` | `1041` | - |
| `k_EMsgGC_RevolvingLootList_DEPRECATED` | `1042` | - |
| `k_EMsgGCLookupAccount` | `1043` | - |
| `k_EMsgGCLookupAccountResponse` | `1044` | - |
| `k_EMsgGCLookupAccountName` | `1045` | - |
| `k_EMsgGCLookupAccountNameResponse` | `1046` | - |
| `k_EMsgGCUpdateItemSchema` | `1049` | - |
| `k_EMsgGCRemoveCustomTexture` | `1051` | - |
| `k_EMsgGCRemoveCustomTextureResponse` | `1052` | - |
| `k_EMsgGCRemoveMakersMark` | `1053` | - |
| `k_EMsgGCRemoveMakersMarkResponse` | `1054` | - |
| `k_EMsgGCRemoveUniqueCraftIndex` | `1055` | - |
| `k_EMsgGCRemoveUniqueCraftIndexResponse` | `1056` | - |
| `k_EMsgGCSaxxyBroadcast` | `1057` | - |
| `k_EMsgGCBackpackSortFinished` | `1058` | - |
| `k_EMsgGCCollectItem` | `1061` | - |
| `k_EMsgGCItemAcknowledged__DEPRECATED` | `1062` | - |
| `k_EMsgGC_ReportAbuse` | `1065` | - |
| `k_EMsgGC_ReportAbuseResponse` | `1066` | - |
| `k_EMsgGCNameItemNotification` | `1068` | - |
| `k_EMsgGCApplyConsumableEffects` | `1069` | - |
| `k_EMsgGCConsumableExhausted` | `1070` | - |
| `k_EMsgGCShowItemsPickedUp` | `1071` | - |
| `k_EMsgGCClientDisplayNotification` | `1072` | - |
| `k_EMsgGCApplyStrangePart` | `1073` | - |
| `k_EMsgGC_IncrementKillCountAttribute` | `1074` | - |
| `k_EMsgGC_IncrementKillCountResponse` | `1075` | - |
| `k_EMsgGCApplyPennantUpgrade` | `1076` | - |
| `k_EMsgGCSetItemPositions` | `1077` | - |
| `k_EMsgGCApplyEggEssence` | `1078` | - |
| `k_EMsgGCNameEggEssenceResponse` | `1079` | - |
| `k_EMsgGCPaintKitItem` | `1080` | - |
| `k_EMsgGCPaintKitBaseItem` | `1081` | - |
| `k_EMsgGCPaintKitItemResponse` | `1082` | - |
| `k_EMsgGCGiftedItems` | `1083` | - |
| `k_EMsgGCUnlockItemStyle` | `1084` | - |
| `k_EMsgGCUnlockItemStyleResponse` | `1085` | - |
| `k_EMsgGCApplySticker` | `1086` | - |
| `k_EMsgGCItemAcknowledged` | `1087` | - |
| `k_EMsgGCStatTrakSwap` | `1088` | - |
| `k_EMsgGCUserTrackTimePlayedConsecutively` | `1089` | - |
| `k_EMsgGCItemCustomizationNotification` | `1090` | - |
| `k_EMsgGCModifyItemAttribute` | `1091` | - |
| `k_EMsgGCCasketItemAdd` | `1092` | - |
| `k_EMsgGCCasketItemExtract` | `1093` | - |
| `k_EMsgGCCasketItemLoadContents` | `1094` | - |
| `k_EMsgGCTradingBase` | `1500` | - |
| `k_EMsgGCTrading_InitiateTradeRequest` | `1501` | - |
| `k_EMsgGCTrading_InitiateTradeResponse` | `1502` | - |
| `k_EMsgGCTrading_StartSession` | `1503` | - |
| `k_EMsgGCTrading_SetItem` | `1504` | - |
| `k_EMsgGCTrading_RemoveItem` | `1505` | - |
| `k_EMsgGCTrading_UpdateTradeInfo` | `1506` | - |
| `k_EMsgGCTrading_SetReadiness` | `1507` | - |
| `k_EMsgGCTrading_ReadinessResponse` | `1508` | - |
| `k_EMsgGCTrading_SessionClosed` | `1509` | - |
| `k_EMsgGCTrading_CancelSession` | `1510` | - |
| `k_EMsgGCTrading_TradeChatMsg` | `1511` | - |
| `k_EMsgGCTrading_ConfirmOffer` | `1512` | - |
| `k_EMsgGCTrading_TradeTypingChatMsg` | `1513` | - |
| `k_EMsgGCServerBrowser_FavoriteServer` | `1601` | - |
| `k_EMsgGCServerBrowser_BlacklistServer` | `1602` | - |
| `k_EMsgGCServerRentalsBase` | `1700` | - |
| `k_EMsgGCItemPreviewCheckStatus` | `1701` | - |
| `k_EMsgGCItemPreviewStatusResponse` | `1702` | - |
| `k_EMsgGCItemPreviewRequest` | `1703` | - |
| `k_EMsgGCItemPreviewRequestResponse` | `1704` | - |
| `k_EMsgGCItemPreviewExpire` | `1705` | - |
| `k_EMsgGCItemPreviewExpireNotification` | `1706` | - |
| `k_EMsgGCItemPreviewItemBoughtNotification` | `1707` | - |
| `k_EMsgGCDev_NewItemRequest` | `2001` | - |
| `k_EMsgGCDev_NewItemRequestResponse` | `2002` | - |
| `k_EMsgGCDev_PaintKitDropItem` | `2003` | - |
| `k_EMsgGCDev_SchemaReservationRequest` | `2004` | - |
| `k_EMsgGCStoreGetUserData` | `2500` | - |
| `k_EMsgGCStoreGetUserDataResponse` | `2501` | - |
| `k_EMsgGCStorePurchaseInit_DEPRECATED` | `2502` | - |
| `k_EMsgGCStorePurchaseInitResponse_DEPRECATED` | `2503` | - |
| `k_EMsgGCStorePurchaseFinalize` | `2504` | - |
| `k_EMsgGCStorePurchaseFinalizeResponse` | `2505` | - |
| `k_EMsgGCStorePurchaseCancel` | `2506` | - |
| `k_EMsgGCStorePurchaseCancelResponse` | `2507` | - |
| `k_EMsgGCStorePurchaseQueryTxn` | `2508` | - |
| `k_EMsgGCStorePurchaseQueryTxnResponse` | `2509` | - |
| `k_EMsgGCStorePurchaseInit` | `2510` | - |
| `k_EMsgGCStorePurchaseInitResponse` | `2511` | - |
| `k_EMsgGCBannedWordListRequest` | `2512` | - |
| `k_EMsgGCBannedWordListResponse` | `2513` | - |
| `k_EMsgGCToGCBannedWordListBroadcast` | `2514` | - |
| `k_EMsgGCToGCBannedWordListUpdated` | `2515` | - |
| `k_EMsgGCToGCDirtySDOCache` | `2516` | - |
| `k_EMsgGCToGCDirtyMultipleSDOCache` | `2517` | - |
| `k_EMsgGCToGCUpdateSQLKeyValue` | `2518` | - |
| `k_EMsgGCToGCIsTrustedServer` | `2519` | - |
| `k_EMsgGCToGCIsTrustedServerResponse` | `2520` | - |
| `k_EMsgGCToGCBroadcastConsoleCommand` | `2521` | - |
| `k_EMsgGCServerVersionUpdated` | `2522` | - |
| `k_EMsgGCToGCWebAPIAccountChanged` | `2524` | - |
| `k_EMsgGCRequestAnnouncements` | `2525` | - |
| `k_EMsgGCRequestAnnouncementsResponse` | `2526` | - |
| `k_EMsgGCRequestPassportItemGrant` | `2527` | - |
| `k_EMsgGCClientVersionUpdated` | `2528` | - |
| `k_EMsgGCRecurringSubscriptionStatus` | `2530` | - |
| `k_EMsgGCAdjustEquipSlotsManual` | `2531` | - |
| `k_EMsgGCAdjustEquipSlotsShuffle` | `2532` | - |
| `k_EMsgGCOpenCrate` | `2534` | - |
| `k_EMsgGCAcknowledgeRentalExpiration` | `2535` | - |
| `k_EMsgGCVolatileItemLoadContents` | `2536` | - |



---

## 📋 EGCMsgResponse

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `k_EGCMsgResponseOK` | `0` | - |
| `k_EGCMsgResponseDenied` | `1` | - |
| `k_EGCMsgResponseServerError` | `2` | - |
| `k_EGCMsgResponseTimeout` | `3` | - |
| `k_EGCMsgResponseInvalid` | `4` | - |
| `k_EGCMsgResponseNoMatch` | `5` | - |
| `k_EGCMsgResponseUnknownError` | `6` | - |
| `k_EGCMsgResponseNotLoggedOn` | `7` | - |
| `k_EGCMsgFailedToCreate` | `8` | - |
| `k_EGCMsgLimitExceeded` | `9` | - |
| `k_EGCMsgCommitUnfinalized` | `10` | - |



---

## 📋 EGCSystemMsg

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `k_EGCMsgInvalid` | `0` | - |
| `k_EGCMsgMulti` | `1` | - |
| `k_EGCMsgGenericReply` | `10` | - |
| `k_EGCMsgSystemBase` | `50` | - |
| `k_EGCMsgAchievementAwarded` | `51` | - |
| `k_EGCMsgConCommand` | `52` | - |
| `k_EGCMsgStartPlaying` | `53` | - |
| `k_EGCMsgStopPlaying` | `54` | - |
| `k_EGCMsgStartGameserver` | `55` | - |
| `k_EGCMsgStopGameserver` | `56` | - |
| `k_EGCMsgWGRequest` | `57` | - |
| `k_EGCMsgWGResponse` | `58` | - |
| `k_EGCMsgGetUserGameStatsSchema` | `59` | - |
| `k_EGCMsgGetUserGameStatsSchemaResponse` | `60` | - |
| `k_EGCMsgGetUserStatsDEPRECATED` | `61` | - |
| `k_EGCMsgGetUserStatsResponse` | `62` | - |
| `k_EGCMsgAppInfoUpdated` | `63` | - |
| `k_EGCMsgValidateSession` | `64` | - |
| `k_EGCMsgValidateSessionResponse` | `65` | - |
| `k_EGCMsgLookupAccountFromInput` | `66` | - |
| `k_EGCMsgSendHTTPRequest` | `67` | - |
| `k_EGCMsgSendHTTPRequestResponse` | `68` | - |
| `k_EGCMsgPreTestSetup` | `69` | - |
| `k_EGCMsgRecordSupportAction` | `70` | - |
| `k_EGCMsgGetAccountDetails_DEPRECATED` | `71` | - |
| `k_EGCMsgReceiveInterAppMessage` | `73` | - |
| `k_EGCMsgFindAccounts` | `74` | - |
| `k_EGCMsgPostAlert` | `75` | - |
| `k_EGCMsgGetLicenses` | `76` | - |
| `k_EGCMsgGetUserStats` | `77` | - |
| `k_EGCMsgGetCommands` | `78` | - |
| `k_EGCMsgGetCommandsResponse` | `79` | - |
| `k_EGCMsgAddFreeLicense` | `80` | - |
| `k_EGCMsgAddFreeLicenseResponse` | `81` | - |
| `k_EGCMsgGetIPLocation` | `82` | - |
| `k_EGCMsgGetIPLocationResponse` | `83` | - |
| `k_EGCMsgSystemStatsSchema` | `84` | - |
| `k_EGCMsgGetSystemStats` | `85` | - |
| `k_EGCMsgGetSystemStatsResponse` | `86` | - |
| `k_EGCMsgSendEmail` | `87` | - |
| `k_EGCMsgSendEmailResponse` | `88` | - |
| `k_EGCMsgGetEmailTemplate` | `89` | - |
| `k_EGCMsgGetEmailTemplateResponse` | `90` | - |
| `k_EGCMsgGrantGuestPass` | `91` | - |
| `k_EGCMsgGrantGuestPassResponse` | `92` | - |
| `k_EGCMsgGetAccountDetails` | `93` | - |
| `k_EGCMsgGetAccountDetailsResponse` | `94` | - |
| `k_EGCMsgGetPersonaNames` | `95` | - |
| `k_EGCMsgGetPersonaNamesResponse` | `96` | - |
| `k_EGCMsgMultiplexMsg` | `97` | - |
| `k_EGCMsgMultiplexMsgResponse` | `98` | - |
| `k_EGCMsgWebAPIRegisterInterfaces` | `101` | - |
| `k_EGCMsgWebAPIJobRequest` | `102` | - |
| `k_EGCMsgWebAPIJobRequestHttpResponse` | `104` | - |
| `k_EGCMsgWebAPIJobRequestForwardResponse` | `105` | - |
| `k_EGCMsgMemCachedGet` | `200` | - |
| `k_EGCMsgMemCachedGetResponse` | `201` | - |
| `k_EGCMsgMemCachedSet` | `202` | - |
| `k_EGCMsgMemCachedDelete` | `203` | - |
| `k_EGCMsgMemCachedStats` | `204` | - |
| `k_EGCMsgMemCachedStatsResponse` | `205` | - |
| `k_EGCMsgMasterSetDirectory` | `220` | - |
| `k_EGCMsgMasterSetDirectoryResponse` | `221` | - |
| `k_EGCMsgMasterSetWebAPIRouting` | `222` | - |
| `k_EGCMsgMasterSetWebAPIRoutingResponse` | `223` | - |
| `k_EGCMsgMasterSetClientMsgRouting` | `224` | - |
| `k_EGCMsgMasterSetClientMsgRoutingResponse` | `225` | - |
| `k_EGCMsgSetOptions` | `226` | - |
| `k_EGCMsgSetOptionsResponse` | `227` | - |
| `k_EGCMsgSystemBase2` | `500` | - |
| `k_EGCMsgGetPurchaseTrustStatus` | `501` | - |
| `k_EGCMsgGetPurchaseTrustStatusResponse` | `502` | - |
| `k_EGCMsgUpdateSession` | `503` | - |
| `k_EGCMsgGCAccountVacStatusChange` | `504` | - |
| `k_EGCMsgCheckFriendship` | `505` | - |
| `k_EGCMsgCheckFriendshipResponse` | `506` | - |
| `k_EGCMsgGetPartnerAccountLink` | `507` | - |
| `k_EGCMsgGetPartnerAccountLinkResponse` | `508` | - |
| `k_EGCMsgDPPartnerMicroTxns` | `512` | - |
| `k_EGCMsgDPPartnerMicroTxnsResponse` | `513` | - |
| `k_EGCMsgVacVerificationChange` | `518` | - |
| `k_EGCMsgAccountPhoneNumberChange` | `519` | - |
| `k_EGCMsgInviteUserToLobby` | `523` | - |
| `k_EGCMsgGetGamePersonalDataCategoriesRequest` | `524` | - |
| `k_EGCMsgGetGamePersonalDataCategoriesResponse` | `525` | - |
| `k_EGCMsgGetGamePersonalDataEntriesRequest` | `526` | - |
| `k_EGCMsgGetGamePersonalDataEntriesResponse` | `527` | - |
| `k_EGCMsgTerminateGamePersonalDataEntriesRequest` | `528` | - |
| `k_EGCMsgTerminateGamePersonalDataEntriesResponse` | `529` | - |
| `k_EGCMsgRecurringSubscriptionStatusChange` | `530` | - |
| `k_EGCMsgDirectServiceMethod` | `531` | - |
| `k_EGCMsgDirectServiceMethodResponse` | `532` | - |



---

## 📋 EGCToGCMsg

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `k_EGCToGCMsgMasterAck` | `150` | - |
| `k_EGCToGCMsgMasterAckResponse` | `151` | - |
| `k_EGCToGCMsgRouted` | `152` | - |
| `k_EGCToGCMsgRoutedReply` | `153` | - |
| `k_EMsgUpdateSessionIP` | `154` | - |
| `k_EMsgRequestSessionIP` | `155` | - |
| `k_EMsgRequestSessionIPResponse` | `156` | - |
| `k_EGCToGCMsgMasterStartupComplete` | `157` | - |



---

## 📋 EHapticPulseType

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `VR_HAND_HAPTIC_PULSE_LIGHT` | `0` | - |
| `VR_HAND_HAPTIC_PULSE_MEDIUM` | `1` | - |
| `VR_HAND_HAPTIC_PULSE_STRONG` | `2` | - |



---

## 📋 EHitGroup

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `EHG_Generic` | `0` | - |
| `EHG_Head` | `1` | - |
| `EHG_Chest` | `2` | - |
| `EHG_Stomach` | `3` | - |
| `EHG_LeftArm` | `4` | - |
| `EHG_RightArm` | `5` | - |
| `EHG_LeftLeg` | `6` | - |
| `EHG_RightLeg` | `7` | - |
| `EHG_Gear` | `8` | - |
| `EHG_Miss` | `9` | - |



---

## 📋 EInitSystemResult

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `k_EInitSystemResult_Invalid` | `0` | - |
| `k_EInitSystemResult_Success` | `1` | - |
| `k_EInitSystemResult_None` | `2` | - |
| `k_EInitSystemResult_NotFound` | `3` | - |
| `k_EInitSystemResult_Existing` | `4` | - |
| `k_EInitSystemResult_FailedOpen` | `5` | - |
| `k_EInitSystemResult_Mismatch` | `6` | - |
| `k_EInitSystemResult_FailedInit` | `7` | - |
| `k_EInitSystemResult_Max` | `8` | - |



---

## 📋 EMsg

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `k_EMsgInvalid` | `0` | - |
| `k_EMsgMulti` | `1` | - |
| `k_EMsgProtobufWrapped` | `2` | - |
| `k_EMsgBaseGeneral` | `100` | - |
| `k_EMsgGenericReply` | `100` | - |
| `k_EMsgDestJobFailed` | `113` | - |
| `k_EMsgAlert` | `115` | - |
| `k_EMsgSCIDRequest` | `120` | - |
| `k_EMsgSCIDResponse` | `121` | - |
| `k_EMsgJobHeartbeat` | `123` | - |
| `k_EMsgHubConnect` | `124` | - |
| `k_EMsgSubscribe` | `126` | - |
| `k_EMRouteMessage` | `127` | - |
| `k_EMsgWGRequest` | `130` | - |
| `k_EMsgWGResponse` | `131` | - |
| `k_EMsgKeepAlive` | `132` | - |
| `k_EMsgWebAPIJobRequest` | `133` | - |
| `k_EMsgWebAPIJobResponse` | `134` | - |
| `k_EMsgClientSessionStart` | `135` | - |
| `k_EMsgClientSessionEnd` | `136` | - |
| `k_EMsgClientSessionUpdate` | `137` | - |
| `k_EMsgStatsDeprecated` | `138` | - |
| `k_EMsgPing` | `139` | - |
| `k_EMsgPingResponse` | `140` | - |
| `k_EMsgStats` | `141` | - |
| `k_EMsgRequestFullStatsBlock` | `142` | - |
| `k_EMsgLoadDBOCacheItem` | `143` | - |
| `k_EMsgLoadDBOCacheItemResponse` | `144` | - |
| `k_EMsgInvalidateDBOCacheItems` | `145` | - |
| `k_EMsgServiceMethod` | `146` | - |
| `k_EMsgServiceMethodResponse` | `147` | - |
| `k_EMsgClientPackageVersions` | `148` | - |
| `k_EMsgTimestampRequest` | `149` | - |
| `k_EMsgTimestampResponse` | `150` | - |
| `k_EMsgServiceMethodCallFromClient` | `151` | - |
| `k_EMsgServiceMethodSendToClient` | `152` | - |
| `k_EMsgBaseShell` | `200` | - |
| `k_EMsgAssignSysID` | `200` | - |
| `k_EMsgExit` | `201` | - |
| `k_EMsgDirRequest` | `202` | - |
| `k_EMsgDirResponse` | `203` | - |
| `k_EMsgZipRequest` | `204` | - |
| `k_EMsgZipResponse` | `205` | - |
| `k_EMsgUpdateRecordResponse` | `215` | - |
| `k_EMsgUpdateCreditCardRequest` | `221` | - |
| `k_EMsgUpdateUserBanResponse` | `225` | - |
| `k_EMsgPrepareToExit` | `226` | - |
| `k_EMsgContentDescriptionUpdate` | `227` | - |
| `k_EMsgTestResetServer` | `228` | - |
| `k_EMsgUniverseChanged` | `229` | - |
| `k_EMsgShellConfigInfoUpdate` | `230` | - |
| `k_EMsgRequestWindowsEventLogEntries` | `233` | - |
| `k_EMsgProvideWindowsEventLogEntries` | `234` | - |
| `k_EMsgShellSearchLogs` | `235` | - |
| `k_EMsgShellSearchLogsResponse` | `236` | - |
| `k_EMsgShellCheckWindowsUpdates` | `237` | - |
| `k_EMsgShellCheckWindowsUpdatesResponse` | `238` | - |
| `k_EMsgTestFlushDelayedSQL` | `240` | - |
| `k_EMsgTestFlushDelayedSQLResponse` | `241` | - |
| `k_EMsgEnsureExecuteScheduledTask_TEST` | `242` | - |
| `k_EMsgEnsureExecuteScheduledTaskResponse_TEST` | `243` | - |
| `k_EMsgUpdateScheduledTaskEnableState_TEST` | `244` | - |
| `k_EMsgUpdateScheduledTaskEnableStateResponse_TEST` | `245` | - |
| `k_EMsgContentDescriptionDeltaUpdate` | `246` | - |
| `k_EMsgGMShellAndServerAddressUpdates` | `247` | - |
| `k_EMsgBaseGM` | `300` | - |
| `k_EMsgHeartbeat` | `300` | - |
| `k_EMsgShellFailed` | `301` | - |
| `k_EMsgExitShells` | `307` | - |
| `k_EMsgExitShell` | `308` | - |
| `k_EMsgGracefulExitShell` | `309` | - |
| `k_EMsgLicenseProcessingComplete` | `316` | - |
| `k_EMsgSetTestFlag` | `317` | - |
| `k_EMsgQueuedEmailsComplete` | `318` | - |
| `k_EMsgGMDRMSync` | `320` | - |
| `k_EMsgPhysicalBoxInventory` | `321` | - |
| `k_EMsgUpdateConfigFile` | `322` | - |
| `k_EMsgTestInitDB` | `323` | - |
| `k_EMsgGMWriteConfigToSQL` | `324` | - |
| `k_EMsgGMLoadActivationCodes` | `325` | - |
| `k_EMsgGMQueueForFBS` | `326` | - |
| `k_EMsgGMSchemaConversionResults` | `327` | - |
| `k_EMsgGMWriteShellFailureToSQL` | `329` | - |
| `k_EMsgGMWriteStatsToSOS` | `330` | - |
| `k_EMsgGMGetServiceMethodRouting` | `331` | - |
| `k_EMsgGMGetServiceMethodRoutingResponse` | `332` | - |
| `k_EMsgGMTestNextBuildSchemaConversion` | `334` | - |
| `k_EMsgGMTestNextBuildSchemaConversionResponse` | `335` | - |
| `k_EMsgExpectShellRestart` | `336` | - |
| `k_EMsgHotFixProgress` | `337` | - |
| `k_EMsgGMStatsForwardToAdminConnections` | `338` | - |
| `k_EMsgGMGetModifiedConVars` | `339` | - |
| `k_EMsgGMGetModifiedConVarsResponse` | `340` | - |
| `k_EMsgBaseAIS` | `400` | - |
| `k_EMsgAISRequestContentDescription` | `402` | - |
| `k_EMsgAISUpdateAppInfo` | `403` | - |
| `k_EMsgAISGetPackageChangeNumber` | `405` | - |
| `k_EMsgAISGetPackageChangeNumberResponse` | `406` | - |
| `k_EMsgAIGetAppGCFlags` | `423` | - |
| `k_EMsgAIGetAppGCFlagsResponse` | `424` | - |
| `k_EMsgAIGetAppList` | `425` | - |
| `k_EMsgAIGetAppListResponse` | `426` | - |
| `k_EMsgAISGetCouponDefinition` | `429` | - |
| `k_EMsgAISGetCouponDefinitionResponse` | `430` | - |
| `k_EMsgAISUpdateSubordinateContentDescription` | `431` | - |
| `k_EMsgAISUpdateSubordinateContentDescriptionResponse` | `432` | - |
| `k_EMsgAISTestEnableGC` | `433` | - |
| `k_EMsgBaseAM` | `500` | - |
| `k_EMsgAMUpdateUserBanRequest` | `504` | - |
| `k_EMsgAMAddLicense` | `505` | - |
| `k_EMsgAMSendSystemIMToUser` | `508` | - |
| `k_EMsgAMExtendLicense` | `509` | - |
| `k_EMsgAMAddMinutesToLicense` | `510` | - |
| `k_EMsgAMCancelLicense` | `511` | - |
| `k_EMsgAMInitPurchase` | `512` | - |
| `k_EMsgAMPurchaseResponse` | `513` | - |
| `k_EMsgAMGetFinalPrice` | `514` | - |
| `k_EMsgAMGetFinalPriceResponse` | `515` | - |
| `k_EMsgAMGetLegacyGameKey` | `516` | - |
| `k_EMsgAMGetLegacyGameKeyResponse` | `517` | - |
| `k_EMsgAMFindHungTransactions` | `518` | - |
| `k_EMsgAMSetAccountTrustedRequest` | `519` | - |
| `k_EMsgAMCancelPurchase` | `522` | - |
| `k_EMsgAMNewChallenge` | `523` | - |
| `k_EMsgAMLoadOEMTickets` | `524` | - |
| `k_EMsgAMFixPendingPurchase` | `525` | - |
| `k_EMsgAMFixPendingPurchaseResponse` | `526` | - |
| `k_EMsgAMIsUserBanned` | `527` | - |
| `k_EMsgAMRegisterKey` | `528` | - |
| `k_EMsgAMLoadActivationCodes` | `529` | - |
| `k_EMsgAMLoadActivationCodesResponse` | `530` | - |
| `k_EMsgAMLookupKeyResponse` | `531` | - |
| `k_EMsgAMLookupKey` | `532` | - |
| `k_EMsgAMChatCleanup` | `533` | - |
| `k_EMsgAMClanCleanup` | `534` | - |
| `k_EMsgAMFixPendingRefund` | `535` | - |
| `k_EMsgAMReverseChargeback` | `536` | - |
| `k_EMsgAMReverseChargebackResponse` | `537` | - |
| `k_EMsgAMClanCleanupList` | `538` | - |
| `k_EMsgAMGetLicenses` | `539` | - |
| `k_EMsgAMGetLicensesResponse` | `540` | - |
| `k_EMsgAMSendCartRepurchase` | `541` | - |
| `k_EMsgAMSendCartRepurchaseResponse` | `542` | - |
| `k_EMsgAllowUserToPlayQuery` | `550` | - |
| `k_EMsgAllowUserToPlayResponse` | `551` | - |
| `k_EMsgAMVerfiyUser` | `552` | - |
| `k_EMsgAMClientNotPlaying` | `553` | - |
| `k_EMsgAMClientRequestFriendship` | `554` | - |
| `k_EMsgAMRelayPublishStatus` | `555` | - |
| `k_EMsgAMInitPurchaseResponse` | `560` | - |
| `k_EMsgAMRevokePurchaseResponse` | `561` | - |
| `k_EMsgAMRefreshGuestPasses` | `563` | - |
| `k_EMsgAMGrantGuestPasses` | `566` | - |
| `k_EMsgAMClanDataUpdated` | `567` | - |
| `k_EMsgAMReloadAccount` | `568` | - |
| `k_EMsgAMClientChatMsgRelay` | `569` | - |
| `k_EMsgAMChatMulti` | `570` | - |
| `k_EMsgAMClientChatInviteRelay` | `571` | - |
| `k_EMsgAMChatInvite` | `572` | - |
| `k_EMsgAMClientJoinChatRelay` | `573` | - |
| `k_EMsgAMClientChatMemberInfoRelay` | `574` | - |
| `k_EMsgAMPublishChatMemberInfo` | `575` | - |
| `k_EMsgAMClientAcceptFriendInvite` | `576` | - |
| `k_EMsgAMChatEnter` | `577` | - |
| `k_EMsgAMClientPublishRemovalFromSource` | `578` | - |
| `k_EMsgAMChatActionResult` | `579` | - |
| `k_EMsgAMFindAccounts` | `580` | - |
| `k_EMsgAMFindAccountsResponse` | `581` | - |
| `k_EMsgAMIsAccountNameInUse` | `582` | - |
| `k_EMsgAMIsAccountNameInUseResponse` | `583` | - |
| `k_EMsgAMSetAccountFlags` | `584` | - |
| `k_EMsgAMCreateClan` | `586` | - |
| `k_EMsgAMCreateClanResponse` | `587` | - |
| `k_EMsgAMGetClanDetails` | `588` | - |
| `k_EMsgAMGetClanDetailsResponse` | `589` | - |
| `k_EMsgAMSetPersonaName` | `590` | - |
| `k_EMsgAMSetAvatar` | `591` | - |
| `k_EMsgAMAuthenticateUser` | `592` | - |
| `k_EMsgAMAuthenticateUserResponse` | `593` | - |
| `k_EMsgAMP2PIntroducerMessage` | `596` | - |
| `k_EMsgClientChatAction` | `597` | - |
| `k_EMsgAMClientChatActionRelay` | `598` | - |
| `k_EMsgBaseVS` | `600` | - |
| `k_EMsgReqChallenge` | `600` | - |
| `k_EMsgVACResponse` | `601` | - |
| `k_EMsgReqChallengeTest` | `602` | - |
| `k_EMsgVSMarkCheat` | `604` | - |
| `k_EMsgVSAddCheat` | `605` | - |
| `k_EMsgVSPurgeCodeModDB` | `606` | - |
| `k_EMsgVSGetChallengeResults` | `607` | - |
| `k_EMsgVSChallengeResultText` | `608` | - |
| `k_EMsgVSReportLingerer` | `609` | - |
| `k_EMsgVSRequestManagedChallenge` | `610` | - |
| `k_EMsgVSLoadDBFinished` | `611` | - |
| `k_EMsgBaseDRMS` | `625` | - |
| `k_EMsgDRMBuildBlobRequest` | `628` | - |
| `k_EMsgDRMBuildBlobResponse` | `629` | - |
| `k_EMsgDRMResolveGuidRequest` | `630` | - |
| `k_EMsgDRMResolveGuidResponse` | `631` | - |
| `k_EMsgDRMVariabilityReport` | `633` | - |
| `k_EMsgDRMVariabilityReportResponse` | `634` | - |
| `k_EMsgDRMStabilityReport` | `635` | - |
| `k_EMsgDRMStabilityReportResponse` | `636` | - |
| `k_EMsgDRMDetailsReportRequest` | `637` | - |
| `k_EMsgDRMDetailsReportResponse` | `638` | - |
| `k_EMsgDRMProcessFile` | `639` | - |
| `k_EMsgDRMAdminUpdate` | `640` | - |
| `k_EMsgDRMAdminUpdateResponse` | `641` | - |
| `k_EMsgDRMSync` | `642` | - |
| `k_EMsgDRMSyncResponse` | `643` | - |
| `k_EMsgDRMProcessFileResponse` | `644` | - |
| `k_EMsgDRMEmptyGuidCache` | `645` | - |
| `k_EMsgDRMEmptyGuidCacheResponse` | `646` | - |
| `k_EMsgBaseCS` | `650` | - |
| `k_EMsgBaseClient` | `700` | - |
| `k_EMsgClientLogOn_Deprecated` | `701` | - |
| `k_EMsgClientAnonLogOn_Deprecated` | `702` | - |
| `k_EMsgClientHeartBeat` | `703` | - |
| `k_EMsgClientVACResponse` | `704` | - |
| `k_EMsgClientGamesPlayed_obsolete` | `705` | - |
| `k_EMsgClientLogOff` | `706` | - |
| `k_EMsgClientNoUDPConnectivity` | `707` | - |
| `k_EMsgClientConnectionStats` | `710` | - |
| `k_EMsgClientPingResponse` | `712` | - |
| `k_EMsgClientRemoveFriend` | `714` | - |
| `k_EMsgClientGamesPlayedNoDataBlob` | `715` | - |
| `k_EMsgClientChangeStatus` | `716` | - |
| `k_EMsgClientVacStatusResponse` | `717` | - |
| `k_EMsgClientFriendMsg` | `718` | - |
| `k_EMsgClientGameConnect_obsolete` | `719` | - |
| `k_EMsgClientGamesPlayed2_obsolete` | `720` | - |
| `k_EMsgClientGameEnded_obsolete` | `721` | - |
| `k_EMsgClientSystemIM` | `726` | - |
| `k_EMsgClientSystemIMAck` | `727` | - |
| `k_EMsgClientGetLicenses` | `728` | - |
| `k_EMsgClientGetLegacyGameKey` | `730` | - |
| `k_EMsgClientContentServerLogOn_Deprecated` | `731` | - |
| `k_EMsgClientAckVACBan2` | `732` | - |
| `k_EMsgClientGetPurchaseReceipts` | `736` | - |
| `k_EMsgClientGamesPlayed3_obsolete` | `738` | - |
| `k_EMsgClientAckGuestPass` | `740` | - |
| `k_EMsgClientRedeemGuestPass` | `741` | - |
| `k_EMsgClientGamesPlayed` | `742` | - |
| `k_EMsgClientRegisterKey` | `743` | - |
| `k_EMsgClientInviteUserToClan` | `744` | - |
| `k_EMsgClientAcknowledgeClanInvite` | `745` | - |
| `k_EMsgClientPurchaseWithMachineID` | `746` | - |
| `k_EMsgClientAppUsageEvent` | `747` | - |
| `k_EMsgClientLogOnResponse` | `751` | - |
| `k_EMsgClientSetHeartbeatRate` | `755` | - |
| `k_EMsgClientNotLoggedOnDeprecated` | `756` | - |
| `k_EMsgClientLoggedOff` | `757` | - |
| `k_EMsgGSApprove` | `758` | - |
| `k_EMsgGSDeny` | `759` | - |
| `k_EMsgGSKick` | `760` | - |
| `k_EMsgClientPurchaseResponse` | `763` | - |
| `k_EMsgClientPing` | `764` | - |
| `k_EMsgClientNOP` | `765` | - |
| `k_EMsgClientPersonaState` | `766` | - |
| `k_EMsgClientFriendsList` | `767` | - |
| `k_EMsgClientAccountInfo` | `768` | - |
| `k_EMsgClientNewsUpdate` | `771` | - |
| `k_EMsgClientGameConnectDeny` | `773` | - |
| `k_EMsgGSStatusReply` | `774` | - |
| `k_EMsgClientGameConnectTokens` | `779` | - |
| `k_EMsgClientLicenseList` | `780` | - |
| `k_EMsgClientVACBanStatus` | `782` | - |
| `k_EMsgClientCMList` | `783` | - |
| `k_EMsgClientEncryptPct` | `784` | - |
| `k_EMsgClientGetLegacyGameKeyResponse` | `785` | - |
| `k_EMsgClientAddFriend` | `791` | - |
| `k_EMsgClientAddFriendResponse` | `792` | - |
| `k_EMsgClientAckGuestPassResponse` | `796` | - |
| `k_EMsgClientRedeemGuestPassResponse` | `797` | - |
| `k_EMsgClientUpdateGuestPassesList` | `798` | - |
| `k_EMsgClientChatMsg` | `799` | - |
| `k_EMsgClientChatInvite` | `800` | - |
| `k_EMsgClientJoinChat` | `801` | - |
| `k_EMsgClientChatMemberInfo` | `802` | - |
| `k_EMsgClientLogOnWithCredentials_Deprecated` | `803` | - |
| `k_EMsgClientPasswordChangeResponse` | `805` | - |
| `k_EMsgClientChatEnter` | `807` | - |
| `k_EMsgClientFriendRemovedFromSource` | `808` | - |
| `k_EMsgClientCreateChat` | `809` | - |
| `k_EMsgClientCreateChatResponse` | `810` | - |
| `k_EMsgClientP2PIntroducerMessage` | `813` | - |
| `k_EMsgClientChatActionResult` | `814` | - |
| `k_EMsgClientRequestFriendData` | `815` | - |
| `k_EMsgClientGetUserStats` | `818` | - |
| `k_EMsgClientGetUserStatsResponse` | `819` | - |
| `k_EMsgClientStoreUserStats` | `820` | - |
| `k_EMsgClientStoreUserStatsResponse` | `821` | - |
| `k_EMsgClientClanState` | `822` | - |
| `k_EMsgClientServiceModule` | `830` | - |
| `k_EMsgClientServiceCall` | `831` | - |
| `k_EMsgClientServiceCallResponse` | `832` | - |
| `k_EMsgClientNatTraversalStatEvent` | `839` | - |
| `k_EMsgClientSteamUsageEvent` | `842` | - |
| `k_EMsgClientCheckPassword` | `845` | - |
| `k_EMsgClientResetPassword` | `846` | - |
| `k_EMsgClientCheckPasswordResponse` | `848` | - |
| `k_EMsgClientResetPasswordResponse` | `849` | - |
| `k_EMsgClientSessionToken` | `850` | - |
| `k_EMsgClientDRMProblemReport` | `851` | - |
| `k_EMsgClientSetIgnoreFriend` | `855` | - |
| `k_EMsgClientSetIgnoreFriendResponse` | `856` | - |
| `k_EMsgClientGetAppOwnershipTicket` | `857` | - |
| `k_EMsgClientGetAppOwnershipTicketResponse` | `858` | - |
| `k_EMsgClientGetLobbyListResponse` | `860` | - |
| `k_EMsgClientServerList` | `880` | - |
| `k_EMsgClientDRMBlobRequest` | `896` | - |
| `k_EMsgClientDRMBlobResponse` | `897` | - |
| `k_EMsgBaseGameServer` | `900` | - |
| `k_EMsgGSDisconnectNotice` | `901` | - |
| `k_EMsgGSStatus` | `903` | - |
| `k_EMsgGSUserPlaying` | `905` | - |
| `k_EMsgGSStatus2` | `906` | - |
| `k_EMsgGSStatusUpdate_Unused` | `907` | - |
| `k_EMsgGSServerType` | `908` | - |
| `k_EMsgGSPlayerList` | `909` | - |
| `k_EMsgGSGetUserAchievementStatus` | `910` | - |
| `k_EMsgGSGetUserAchievementStatusResponse` | `911` | - |
| `k_EMsgGSGetPlayStats` | `918` | - |
| `k_EMsgGSGetPlayStatsResponse` | `919` | - |
| `k_EMsgGSGetUserGroupStatus` | `920` | - |
| `k_EMsgAMGetUserGroupStatus` | `921` | - |
| `k_EMsgAMGetUserGroupStatusResponse` | `922` | - |
| `k_EMsgGSGetUserGroupStatusResponse` | `923` | - |
| `k_EMsgGSGetReputation` | `936` | - |
| `k_EMsgGSGetReputationResponse` | `937` | - |
| `k_EMsgGSAssociateWithClan` | `938` | - |
| `k_EMsgGSAssociateWithClanResponse` | `939` | - |
| `k_EMsgGSComputeNewPlayerCompatibility` | `940` | - |
| `k_EMsgGSComputeNewPlayerCompatibilityResponse` | `941` | - |
| `k_EMsgBaseAdmin` | `1000` | - |
| `k_EMsgAdminCmd` | `1000` | - |
| `k_EMsgAdminCmdResponse` | `1004` | - |
| `k_EMsgAdminLogListenRequest` | `1005` | - |
| `k_EMsgAdminLogEvent` | `1006` | - |
| `k_EMsgUniverseData` | `1010` | - |
| `k_EMsgAdminSpew` | `1019` | - |
| `k_EMsgAdminConsoleTitle` | `1020` | - |
| `k_EMsgAdminGCSpew` | `1023` | - |
| `k_EMsgAdminGCCommand` | `1024` | - |
| `k_EMsgAdminGCGetCommandList` | `1025` | - |
| `k_EMsgAdminGCGetCommandListResponse` | `1026` | - |
| `k_EMsgFBSConnectionData` | `1027` | - |
| `k_EMsgAdminMsgSpew` | `1028` | - |
| `k_EMsgBaseFBS` | `1100` | - |
| `k_EMsgFBSReqVersion` | `1100` | - |
| `k_EMsgFBSVersionInfo` | `1101` | - |
| `k_EMsgFBSForceRefresh` | `1102` | - |
| `k_EMsgFBSForceBounce` | `1103` | - |
| `k_EMsgFBSDeployPackage` | `1104` | - |
| `k_EMsgFBSDeployResponse` | `1105` | - |
| `k_EMsgFBSUpdateBootstrapper` | `1106` | - |
| `k_EMsgFBSSetState` | `1107` | - |
| `k_EMsgFBSApplyOSUpdates` | `1108` | - |
| `k_EMsgFBSRunCMDScript` | `1109` | - |
| `k_EMsgFBSRebootBox` | `1110` | - |
| `k_EMsgFBSSetBigBrotherMode` | `1111` | - |
| `k_EMsgFBSMinidumpServer` | `1112` | - |
| `k_EMsgFBSDeployHotFixPackage` | `1114` | - |
| `k_EMsgFBSDeployHotFixResponse` | `1115` | - |
| `k_EMsgFBSDownloadHotFix` | `1116` | - |
| `k_EMsgFBSDownloadHotFixResponse` | `1117` | - |
| `k_EMsgFBSUpdateTargetConfigFile` | `1118` | - |
| `k_EMsgFBSApplyAccountCred` | `1119` | - |
| `k_EMsgFBSApplyAccountCredResponse` | `1120` | - |
| `k_EMsgFBSSetShellCount` | `1121` | - |
| `k_EMsgFBSTerminateShell` | `1122` | - |
| `k_EMsgFBSQueryGMForRequest` | `1123` | - |
| `k_EMsgFBSQueryGMResponse` | `1124` | - |
| `k_EMsgFBSTerminateZombies` | `1125` | - |
| `k_EMsgFBSInfoFromBootstrapper` | `1126` | - |
| `k_EMsgFBSRebootBoxResponse` | `1127` | - |
| `k_EMsgFBSBootstrapperPackageRequest` | `1128` | - |
| `k_EMsgFBSBootstrapperPackageResponse` | `1129` | - |
| `k_EMsgFBSBootstrapperGetPackageChunk` | `1130` | - |
| `k_EMsgFBSBootstrapperGetPackageChunkResponse` | `1131` | - |
| `k_EMsgFBSBootstrapperPackageTransferProgress` | `1132` | - |
| `k_EMsgFBSRestartBootstrapper` | `1133` | - |
| `k_EMsgFBSPauseFrozenDumps` | `1134` | - |
| `k_EMsgBaseFileXfer` | `1200` | - |
| `k_EMsgFileXferRequest` | `1200` | - |
| `k_EMsgFileXferResponse` | `1201` | - |
| `k_EMsgFileXferData` | `1202` | - |
| `k_EMsgFileXferEnd` | `1203` | - |
| `k_EMsgFileXferDataAck` | `1204` | - |
| `k_EMsgBaseChannelAuth` | `1300` | - |
| `k_EMsgChannelAuthChallenge` | `1300` | - |
| `k_EMsgChannelAuthResponse` | `1301` | - |
| `k_EMsgChannelAuthResult` | `1302` | - |
| `k_EMsgChannelEncryptRequest` | `1303` | - |
| `k_EMsgChannelEncryptResponse` | `1304` | - |
| `k_EMsgChannelEncryptResult` | `1305` | - |
| `k_EMsgBaseBS` | `1400` | - |
| `k_EMsgBSPurchaseStart` | `1401` | - |
| `k_EMsgBSPurchaseResponse` | `1402` | - |
| `k_EMsgBSAuthenticateCCTrans` | `1403` | - |
| `k_EMsgBSAuthenticateCCTransResponse` | `1404` | - |
| `k_EMsgBSSettleComplete` | `1406` | - |
| `k_EMsgBSInitPayPalTxn` | `1408` | - |
| `k_EMsgBSInitPayPalTxnResponse` | `1409` | - |
| `k_EMsgBSGetPayPalUserInfo` | `1410` | - |
| `k_EMsgBSGetPayPalUserInfoResponse` | `1411` | - |
| `k_EMsgBSPaymentInstrBan` | `1417` | - |
| `k_EMsgBSPaymentInstrBanResponse` | `1418` | - |
| `k_EMsgBSInitGCBankXferTxn` | `1421` | - |
| `k_EMsgBSInitGCBankXferTxnResponse` | `1422` | - |
| `k_EMsgBSCommitGCTxn` | `1425` | - |
| `k_EMsgBSQueryTransactionStatus` | `1426` | - |
| `k_EMsgBSQueryTransactionStatusResponse` | `1427` | - |
| `k_EMsgBSQueryTxnExtendedInfo` | `1433` | - |
| `k_EMsgBSQueryTxnExtendedInfoResponse` | `1434` | - |
| `k_EMsgBSUpdateConversionRates` | `1435` | - |
| `k_EMsgBSPurchaseRunFraudChecks` | `1437` | - |
| `k_EMsgBSPurchaseRunFraudChecksResponse` | `1438` | - |
| `k_EMsgBSQueryBankInformation` | `1440` | - |
| `k_EMsgBSQueryBankInformationResponse` | `1441` | - |
| `k_EMsgBSValidateXsollaSignature` | `1445` | - |
| `k_EMsgBSValidateXsollaSignatureResponse` | `1446` | - |
| `k_EMsgBSQiwiWalletInvoice` | `1448` | - |
| `k_EMsgBSQiwiWalletInvoiceResponse` | `1449` | - |
| `k_EMsgBSUpdateInventoryFromProPack` | `1450` | - |
| `k_EMsgBSUpdateInventoryFromProPackResponse` | `1451` | - |
| `k_EMsgBSSendShippingRequest` | `1452` | - |
| `k_EMsgBSSendShippingRequestResponse` | `1453` | - |
| `k_EMsgBSGetProPackOrderStatus` | `1454` | - |
| `k_EMsgBSGetProPackOrderStatusResponse` | `1455` | - |
| `k_EMsgBSCheckJobRunning` | `1456` | - |
| `k_EMsgBSCheckJobRunningResponse` | `1457` | - |
| `k_EMsgBSResetPackagePurchaseRateLimit` | `1458` | - |
| `k_EMsgBSResetPackagePurchaseRateLimitResponse` | `1459` | - |
| `k_EMsgBSUpdatePaymentData` | `1460` | - |
| `k_EMsgBSUpdatePaymentDataResponse` | `1461` | - |
| `k_EMsgBSGetBillingAddress` | `1462` | - |
| `k_EMsgBSGetBillingAddressResponse` | `1463` | - |
| `k_EMsgBSGetCreditCardInfo` | `1464` | - |
| `k_EMsgBSGetCreditCardInfoResponse` | `1465` | - |
| `k_EMsgBSRemoveExpiredPaymentData` | `1468` | - |
| `k_EMsgBSRemoveExpiredPaymentDataResponse` | `1469` | - |
| `k_EMsgBSConvertToCurrentKeys` | `1470` | - |
| `k_EMsgBSConvertToCurrentKeysResponse` | `1471` | - |
| `k_EMsgBSInitPurchase` | `1472` | - |
| `k_EMsgBSInitPurchaseResponse` | `1473` | - |
| `k_EMsgBSCompletePurchase` | `1474` | - |
| `k_EMsgBSCompletePurchaseResponse` | `1475` | - |
| `k_EMsgBSPruneCardUsageStats` | `1476` | - |
| `k_EMsgBSPruneCardUsageStatsResponse` | `1477` | - |
| `k_EMsgBSStoreBankInformation` | `1478` | - |
| `k_EMsgBSStoreBankInformationResponse` | `1479` | - |
| `k_EMsgBSVerifyPOSAKey` | `1480` | - |
| `k_EMsgBSVerifyPOSAKeyResponse` | `1481` | - |
| `k_EMsgBSReverseRedeemPOSAKey` | `1482` | - |
| `k_EMsgBSReverseRedeemPOSAKeyResponse` | `1483` | - |
| `k_EMsgBSQueryFindCreditCard` | `1484` | - |
| `k_EMsgBSQueryFindCreditCardResponse` | `1485` | - |
| `k_EMsgBSStatusInquiryPOSAKey` | `1486` | - |
| `k_EMsgBSStatusInquiryPOSAKeyResponse` | `1487` | - |
| `k_EMsgBSBoaCompraConfirmProductDelivery` | `1494` | - |
| `k_EMsgBSBoaCompraConfirmProductDeliveryResponse` | `1495` | - |
| `k_EMsgBSGenerateBoaCompraMD5` | `1496` | - |
| `k_EMsgBSGenerateBoaCompraMD5Response` | `1497` | - |
| `k_EMsgBSCommitWPTxn` | `1498` | - |
| `k_EMsgBSCommitAdyenTxn` | `1499` | - |
| `k_EMsgBaseATS` | `1500` | - |
| `k_EMsgATSStartStressTest` | `1501` | - |
| `k_EMsgATSStopStressTest` | `1502` | - |
| `k_EMsgATSRunFailServerTest` | `1503` | - |
| `k_EMsgATSUFSPerfTestTask` | `1504` | - |
| `k_EMsgATSUFSPerfTestResponse` | `1505` | - |
| `k_EMsgATSCycleTCM` | `1506` | - |
| `k_EMsgATSInitDRMSStressTest` | `1507` | - |
| `k_EMsgATSCallTest` | `1508` | - |
| `k_EMsgATSCallTestReply` | `1509` | - |
| `k_EMsgATSStartExternalStress` | `1510` | - |
| `k_EMsgATSExternalStressJobStart` | `1511` | - |
| `k_EMsgATSExternalStressJobQueued` | `1512` | - |
| `k_EMsgATSExternalStressJobRunning` | `1513` | - |
| `k_EMsgATSExternalStressJobStopped` | `1514` | - |
| `k_EMsgATSExternalStressJobStopAll` | `1515` | - |
| `k_EMsgATSExternalStressActionResult` | `1516` | - |
| `k_EMsgATSStarted` | `1517` | - |
| `k_EMsgATSCSPerfTestTask` | `1518` | - |
| `k_EMsgATSCSPerfTestResponse` | `1519` | - |
| `k_EMsgBaseDP` | `1600` | - |
| `k_EMsgDPSetPublishingState` | `1601` | - |
| `k_EMsgDPUniquePlayersStat` | `1603` | - |
| `k_EMsgDPStreamingUniquePlayersStat` | `1604` | - |
| `k_EMsgDPBlockingStats` | `1607` | - |
| `k_EMsgDPNatTraversalStats` | `1608` | - |
| `k_EMsgDPCloudStats` | `1612` | - |
| `k_EMsgDPGetPlayerCount` | `1615` | - |
| `k_EMsgDPGetPlayerCountResponse` | `1616` | - |
| `k_EMsgDPGameServersPlayersStats` | `1617` | - |
| `k_EMsgClientDPCheckSpecialSurvey` | `1620` | - |
| `k_EMsgClientDPCheckSpecialSurveyResponse` | `1621` | - |
| `k_EMsgClientDPSendSpecialSurveyResponse` | `1622` | - |
| `k_EMsgClientDPSendSpecialSurveyResponseReply` | `1623` | - |
| `k_EMsgDPStoreSaleStatistics` | `1624` | - |
| `k_EMsgDPPartnerMicroTxns` | `1628` | - |
| `k_EMsgDPPartnerMicroTxnsResponse` | `1629` | - |
| `k_EMsgDPVRUniquePlayersStat` | `1631` | - |
| `k_EMsgBaseCM` | `1700` | - |
| `k_EMsgCMSetAllowState` | `1701` | - |
| `k_EMsgCMSpewAllowState` | `1702` | - |
| `k_EMsgCMSessionRejected` | `1703` | - |
| `k_EMsgCMSetSecrets` | `1704` | - |
| `k_EMsgCMGetSecrets` | `1705` | - |
| `k_EMsgBaseGC` | `2200` | - |
| `k_EMsgGCCmdRevive` | `2203` | - |
| `k_EMsgGCCmdDown` | `2206` | - |
| `k_EMsgGCCmdDeploy` | `2207` | - |
| `k_EMsgGCCmdDeployResponse` | `2208` | - |
| `k_EMsgGCCmdSwitch` | `2209` | - |
| `k_EMsgAMRefreshSessions` | `2210` | - |
| `k_EMsgGCAchievementAwarded` | `2212` | - |
| `k_EMsgGCSystemMessage` | `2213` | - |
| `k_EMsgGCCmdStatus` | `2216` | - |
| `k_EMsgGCRegisterWebInterfaces_Deprecated` | `2217` | - |
| `k_EMsgGCGetAccountDetails_DEPRECATED` | `2218` | - |
| `k_EMsgGCInterAppMessage` | `2219` | - |
| `k_EMsgGCGetEmailTemplate` | `2220` | - |
| `k_EMsgGCGetEmailTemplateResponse` | `2221` | - |
| `k_EMsgGCHRelay` | `2222` | - |
| `k_EMsgGCHRelayToClient` | `2223` | - |
| `k_EMsgGCHUpdateSession` | `2224` | - |
| `k_EMsgGCHRequestUpdateSession` | `2225` | - |
| `k_EMsgGCHRequestStatus` | `2226` | - |
| `k_EMsgGCHRequestStatusResponse` | `2227` | - |
| `k_EMsgGCHAccountVacStatusChange` | `2228` | - |
| `k_EMsgGCHSpawnGC` | `2229` | - |
| `k_EMsgGCHSpawnGCResponse` | `2230` | - |
| `k_EMsgGCHKillGC` | `2231` | - |
| `k_EMsgGCHKillGCResponse` | `2232` | - |
| `k_EMsgGCHAccountTradeBanStatusChange` | `2233` | - |
| `k_EMsgGCHAccountLockStatusChange` | `2234` | - |
| `k_EMsgGCHVacVerificationChange` | `2235` | - |
| `k_EMsgGCHAccountPhoneNumberChange` | `2236` | - |
| `k_EMsgGCHAccountTwoFactorChange` | `2237` | - |
| `k_EMsgGCHInviteUserToLobby` | `2238` | - |
| `k_EMsgGCHUpdateMultipleSessions` | `2239` | - |
| `k_EMsgGCHMarkAppSessionsAuthoritative` | `2240` | - |
| `k_EMsgGCHRecurringSubscriptionStatusChange` | `2241` | - |
| `k_EMsgGCHAppCheersReceived` | `2242` | - |
| `k_EMsgGCHAppCheersGetAllowedTypes` | `2243` | - |
| `k_EMsgGCHAppCheersGetAllowedTypesResponse` | `2244` | - |
| `k_EMsgGCHRoutingRulesFromGCHtoGM` | `2245` | - |
| `k_EMsgGCHRoutingRulesToGCHfromGM` | `2246` | - |
| `k_EMsgUpdateCMMessageRateRules` | `2247` | - |
| `k_EMsgBaseP2P` | `2500` | - |
| `k_EMsgP2PIntroducerMessage` | `2502` | - |
| `k_EMsgBaseSM` | `2900` | - |
| `k_EMsgSMExpensiveReport` | `2902` | - |
| `k_EMsgSMHourlyReport` | `2903` | - |
| `k_EMsgSMPartitionRenames` | `2905` | - |
| `k_EMsgSMMonitorSpace` | `2906` | - |
| `k_EMsgSMTestNextBuildSchemaConversion` | `2907` | - |
| `k_EMsgSMTestNextBuildSchemaConversionResponse` | `2908` | - |
| `k_EMsgBaseTest` | `3000` | - |
| `k_EMsgFailServer` | `3000` | - |
| `k_EMsgJobHeartbeatTest` | `3001` | - |
| `k_EMsgJobHeartbeatTestResponse` | `3002` | - |
| `k_EMsgBaseFTSRange` | `3100` | - |
| `k_EMsgBaseCCSRange` | `3150` | - |
| `k_EMsgCCSDeleteAllCommentsByAuthor` | `3161` | - |
| `k_EMsgCCSDeleteAllCommentsByAuthorResponse` | `3162` | - |
| `k_EMsgBaseLBSRange` | `3200` | - |
| `k_EMsgLBSSetScore` | `3201` | - |
| `k_EMsgLBSSetScoreResponse` | `3202` | - |
| `k_EMsgLBSFindOrCreateLB` | `3203` | - |
| `k_EMsgLBSFindOrCreateLBResponse` | `3204` | - |
| `k_EMsgLBSGetLBEntries` | `3205` | - |
| `k_EMsgLBSGetLBEntriesResponse` | `3206` | - |
| `k_EMsgLBSGetLBList` | `3207` | - |
| `k_EMsgLBSGetLBListResponse` | `3208` | - |
| `k_EMsgLBSSetLBDetails` | `3209` | - |
| `k_EMsgLBSDeleteLB` | `3210` | - |
| `k_EMsgLBSDeleteLBEntry` | `3211` | - |
| `k_EMsgLBSResetLB` | `3212` | - |
| `k_EMsgLBSResetLBResponse` | `3213` | - |
| `k_EMsgLBSDeleteLBResponse` | `3214` | - |
| `k_EMsgBaseOGS` | `3400` | - |
| `k_EMsgOGSBeginSession` | `3401` | - |
| `k_EMsgOGSBeginSessionResponse` | `3402` | - |
| `k_EMsgOGSEndSession` | `3403` | - |
| `k_EMsgOGSEndSessionResponse` | `3404` | - |
| `k_EMsgOGSWriteAppSessionRow` | `3406` | - |
| `k_EMsgBaseBRP` | `3600` | - |
| `k_EMsgBRPPostTransactionTax` | `3629` | - |
| `k_EMsgBRPPostTransactionTaxResponse` | `3630` | - |
| `k_EMsgBaseAMRange2` | `4000` | - |
| `k_EMsgAMCreateChat` | `4001` | - |
| `k_EMsgAMCreateChatResponse` | `4002` | - |
| `k_EMsgAMSetProfileURL` | `4005` | - |
| `k_EMsgAMGetAccountEmailAddress` | `4006` | - |
| `k_EMsgAMGetAccountEmailAddressResponse` | `4007` | - |
| `k_EMsgAMRequestClanData` | `4008` | - |
| `k_EMsgAMRouteToClients` | `4009` | - |
| `k_EMsgAMLeaveClan` | `4010` | - |
| `k_EMsgAMClanPermissions` | `4011` | - |
| `k_EMsgAMClanPermissionsResponse` | `4012` | - |
| `k_EMsgAMCreateClanEventDummyForRateLimiting` | `4013` | - |
| `k_EMsgAMUpdateClanEventDummyForRateLimiting` | `4015` | - |
| `k_EMsgAMSetClanPermissionSettings` | `4021` | - |
| `k_EMsgAMSetClanPermissionSettingsResponse` | `4022` | - |
| `k_EMsgAMGetClanPermissionSettings` | `4023` | - |
| `k_EMsgAMGetClanPermissionSettingsResponse` | `4024` | - |
| `k_EMsgAMPublishChatRoomInfo` | `4025` | - |
| `k_EMsgClientChatRoomInfo` | `4026` | - |
| `k_EMsgAMGetClanHistory` | `4039` | - |
| `k_EMsgAMGetClanHistoryResponse` | `4040` | - |
| `k_EMsgAMGetClanPermissionBits` | `4041` | - |
| `k_EMsgAMGetClanPermissionBitsResponse` | `4042` | - |
| `k_EMsgAMSetClanPermissionBits` | `4043` | - |
| `k_EMsgAMSetClanPermissionBitsResponse` | `4044` | - |
| `k_EMsgAMSessionInfoRequest` | `4045` | - |
| `k_EMsgAMSessionInfoResponse` | `4046` | - |
| `k_EMsgAMValidateWGToken` | `4047` | - |
| `k_EMsgAMGetClanRank` | `4050` | - |
| `k_EMsgAMGetClanRankResponse` | `4051` | - |
| `k_EMsgAMSetClanRank` | `4052` | - |
| `k_EMsgAMSetClanRankResponse` | `4053` | - |
| `k_EMsgAMGetClanPOTW` | `4054` | - |
| `k_EMsgAMGetClanPOTWResponse` | `4055` | - |
| `k_EMsgAMSetClanPOTW` | `4056` | - |
| `k_EMsgAMSetClanPOTWResponse` | `4057` | - |
| `k_EMsgAMDumpUser` | `4059` | - |
| `k_EMsgAMKickUserFromClan` | `4060` | - |
| `k_EMsgAMAddFounderToClan` | `4061` | - |
| `k_EMsgAMValidateWGTokenResponse` | `4062` | - |
| `k_EMsgAMSetAccountDetails` | `4064` | - |
| `k_EMsgAMGetChatBanList` | `4065` | - |
| `k_EMsgAMGetChatBanListResponse` | `4066` | - |
| `k_EMsgAMUnBanFromChat` | `4067` | - |
| `k_EMsgAMSetClanDetails` | `4068` | - |
| `k_EMsgUGSGetUserGameStats` | `4073` | - |
| `k_EMsgUGSGetUserGameStatsResponse` | `4074` | - |
| `k_EMsgAMCheckClanMembership` | `4075` | - |
| `k_EMsgAMGetClanMembers` | `4076` | - |
| `k_EMsgAMGetClanMembersResponse` | `4077` | - |
| `k_EMsgAMNotifyChatOfClanChange` | `4079` | - |
| `k_EMsgAMResubmitPurchase` | `4080` | - |
| `k_EMsgAMAddFriend` | `4081` | - |
| `k_EMsgAMAddFriendResponse` | `4082` | - |
| `k_EMsgAMRemoveFriend` | `4083` | - |
| `k_EMsgAMDumpClan` | `4084` | - |
| `k_EMsgAMChangeClanOwner` | `4085` | - |
| `k_EMsgAMCancelEasyCollect` | `4086` | - |
| `k_EMsgAMCancelEasyCollectResponse` | `4087` | - |
| `k_EMsgAMClansInCommon` | `4090` | - |
| `k_EMsgAMClansInCommonResponse` | `4091` | - |
| `k_EMsgAMIsValidAccountID` | `4092` | - |
| `k_EMsgAMWipeFriendsList` | `4095` | - |
| `k_EMsgAMSetIgnored` | `4096` | - |
| `k_EMsgAMClansInCommonCountResponse` | `4097` | - |
| `k_EMsgAMFriendsList` | `4098` | - |
| `k_EMsgAMFriendsListResponse` | `4099` | - |
| `k_EMsgAMFriendsInCommon` | `4100` | - |
| `k_EMsgAMFriendsInCommonResponse` | `4101` | - |
| `k_EMsgAMFriendsInCommonCountResponse` | `4102` | - |
| `k_EMsgAMClansInCommonCount` | `4103` | - |
| `k_EMsgAMChallengeVerdict` | `4104` | - |
| `k_EMsgAMChallengeNotification` | `4105` | - |
| `k_EMsgAMFindGSByIP` | `4106` | - |
| `k_EMsgAMFoundGSByIP` | `4107` | - |
| `k_EMsgAMGiftRevoked` | `4108` | - |
| `k_EMsgAMUserClanList` | `4110` | - |
| `k_EMsgAMUserClanListResponse` | `4111` | - |
| `k_EMsgAMGetAccountDetails2` | `4112` | - |
| `k_EMsgAMGetAccountDetailsResponse2` | `4113` | - |
| `k_EMsgAMSetCommunityProfileSettings` | `4114` | - |
| `k_EMsgAMSetCommunityProfileSettingsResponse` | `4115` | - |
| `k_EMsgAMGetCommunityPrivacyState` | `4116` | - |
| `k_EMsgAMGetCommunityPrivacyStateResponse` | `4117` | - |
| `k_EMsgAMCheckClanInviteRateLimiting` | `4118` | - |
| `k_EMsgUGSGetUserAchievementStatus` | `4119` | - |
| `k_EMsgAMGetIgnored` | `4120` | - |
| `k_EMsgAMGetIgnoredResponse` | `4121` | - |
| `k_EMsgAMSetIgnoredResponse` | `4122` | - |
| `k_EMsgAMSetFriendRelationshipNone` | `4123` | - |
| `k_EMsgAMGetFriendRelationship` | `4124` | - |
| `k_EMsgAMGetFriendRelationshipResponse` | `4125` | - |
| `k_EMsgAMServiceModulesCache` | `4126` | - |
| `k_EMsgAMServiceModulesCall` | `4127` | - |
| `k_EMsgAMServiceModulesCallResponse` | `4128` | - |
| `k_EMsgCommunityAddFriendNews` | `4140` | - |
| `k_EMsgAMFindClanUser` | `4143` | - |
| `k_EMsgAMFindClanUserResponse` | `4144` | - |
| `k_EMsgAMBanFromChat` | `4145` | - |
| `k_EMsgAMGetUserNewsSubscriptions` | `4147` | - |
| `k_EMsgAMGetUserNewsSubscriptionsResponse` | `4148` | - |
| `k_EMsgAMSetUserNewsSubscriptions` | `4149` | - |
| `k_EMsgAMSendQueuedEmails` | `4152` | - |
| `k_EMsgAMSetLicenseFlags` | `4153` | - |
| `k_EMsgCommunityDeleteUserNews` | `4155` | - |
| `k_EMsgAMGetAccountStatus` | `4158` | - |
| `k_EMsgAMGetAccountStatusResponse` | `4159` | - |
| `k_EMsgAMEditBanReason` | `4160` | - |
| `k_EMsgAMCheckClanMembershipResponse` | `4161` | - |
| `k_EMsgAMProbeClanMembershipList` | `4162` | - |
| `k_EMsgAMProbeClanMembershipListResponse` | `4163` | - |
| `k_EMsgUGSGetUserAchievementStatusResponse` | `4164` | - |
| `k_EMsgAMGetFriendsLobbies` | `4165` | - |
| `k_EMsgAMGetFriendsLobbiesResponse` | `4166` | - |
| `k_EMsgAMGetUserFriendNewsResponse` | `4172` | - |
| `k_EMsgCommunityGetUserFriendNews` | `4173` | - |
| `k_EMsgAMGetUserClansNewsResponse` | `4174` | - |
| `k_EMsgAMGetUserClansNews` | `4175` | - |
| `k_EMsgAMGetPreviousCBAccount` | `4184` | - |
| `k_EMsgAMGetPreviousCBAccountResponse` | `4185` | - |
| `k_EMsgAMGetUserLicenseHistory` | `4190` | - |
| `k_EMsgAMGetUserLicenseHistoryResponse` | `4191` | - |
| `k_EMsgAMSupportChangePassword` | `4194` | - |
| `k_EMsgAMSupportChangeEmail` | `4195` | - |
| `k_EMsgAMResetUserVerificationGSByIP` | `4197` | - |
| `k_EMsgAMUpdateGSPlayStats` | `4198` | - |
| `k_EMsgAMSupportEnableOrDisable` | `4199` | - |
| `k_EMsgAMGetPurchaseStatus` | `4206` | - |
| `k_EMsgAMSupportIsAccountEnabled` | `4209` | - |
| `k_EMsgAMSupportIsAccountEnabledResponse` | `4210` | - |
| `k_EMsgUGSGetUserStats` | `4211` | - |
| `k_EMsgAMGSSearch` | `4213` | - |
| `k_EMsgChatServerRouteFriendMsg` | `4219` | - |
| `k_EMsgAMTicketAuthRequestOrResponse` | `4220` | - |
| `k_EMsgAMAddFreeLicense` | `4224` | - |
| `k_EMsgAMValidateEmailLink` | `4231` | - |
| `k_EMsgAMValidateEmailLinkResponse` | `4232` | - |
| `k_EMsgUGSStoreUserStats` | `4236` | - |
| `k_EMsgAMDeleteStoredCard` | `4241` | - |
| `k_EMsgAMRevokeLegacyGameKeys` | `4242` | - |
| `k_EMsgAMGetWalletDetails` | `4244` | - |
| `k_EMsgAMGetWalletDetailsResponse` | `4245` | - |
| `k_EMsgAMDeleteStoredPaymentInfo` | `4246` | - |
| `k_EMsgAMGetStoredPaymentSummary` | `4247` | - |
| `k_EMsgAMGetStoredPaymentSummaryResponse` | `4248` | - |
| `k_EMsgAMGetWalletConversionRate` | `4249` | - |
| `k_EMsgAMGetWalletConversionRateResponse` | `4250` | - |
| `k_EMsgAMConvertWallet` | `4251` | - |
| `k_EMsgAMConvertWalletResponse` | `4252` | - |
| `k_EMsgAMSetPreApproval` | `4255` | - |
| `k_EMsgAMSetPreApprovalResponse` | `4256` | - |
| `k_EMsgAMCreateRefund` | `4258` | - |
| `k_EMsgAMCreateChargeback` | `4260` | - |
| `k_EMsgAMCreateDispute` | `4262` | - |
| `k_EMsgAMClearDispute` | `4264` | - |
| `k_EMsgAMCreateFinancialAdjustment` | `4265` | - |
| `k_EMsgAMPlayerNicknameList` | `4266` | - |
| `k_EMsgAMPlayerNicknameListResponse` | `4267` | - |
| `k_EMsgAMGetUserCurrentGameInfo` | `4269` | - |
| `k_EMsgAMGetUserCurrentGameInfoResponse` | `4270` | - |
| `k_EMsgAMGetGSPlayerList` | `4271` | - |
| `k_EMsgAMGetGSPlayerListResponse` | `4272` | - |
| `k_EMsgAMGetSteamIDForMicroTxn` | `4278` | - |
| `k_EMsgAMGetSteamIDForMicroTxnResponse` | `4279` | - |
| `k_EMsgAMSetPartnerMember` | `4280` | - |
| `k_EMsgAMRemovePublisherUser` | `4281` | - |
| `k_EMsgAMGetUserLicenseList` | `4282` | - |
| `k_EMsgAMGetUserLicenseListResponse` | `4283` | - |
| `k_EMsgAMReloadGameGroupPolicy` | `4284` | - |
| `k_EMsgAMAddFreeLicenseResponse` | `4285` | - |
| `k_EMsgAMVACStatusUpdate` | `4286` | - |
| `k_EMsgAMGetAccountDetails` | `4287` | - |
| `k_EMsgAMGetAccountDetailsResponse` | `4288` | - |
| `k_EMsgAMGetPlayerLinkDetails` | `4289` | - |
| `k_EMsgAMGetPlayerLinkDetailsResponse` | `4290` | - |
| `k_EMsgAMGetAccountFlagsForWGSpoofing` | `4294` | - |
| `k_EMsgAMGetAccountFlagsForWGSpoofingResponse` | `4295` | - |
| `k_EMsgAMGetClanOfficers` | `4298` | - |
| `k_EMsgAMGetClanOfficersResponse` | `4299` | - |
| `k_EMsgAMNameChange` | `4300` | - |
| `k_EMsgAMGetNameHistory` | `4301` | - |
| `k_EMsgAMGetNameHistoryResponse` | `4302` | - |
| `k_EMsgAMUpdateProviderStatus` | `4305` | - |
| `k_EMsgAMSupportRemoveAccountSecurity` | `4307` | - |
| `k_EMsgAMIsAccountInCaptchaGracePeriod` | `4308` | - |
| `k_EMsgAMIsAccountInCaptchaGracePeriodResponse` | `4309` | - |
| `k_EMsgAMAccountPS3Unlink` | `4310` | - |
| `k_EMsgAMAccountPS3UnlinkResponse` | `4311` | - |
| `k_EMsgUGSStoreUserStatsResponse` | `4312` | - |
| `k_EMsgAMGetAccountPSNInfo` | `4313` | - |
| `k_EMsgAMGetAccountPSNInfoResponse` | `4314` | - |
| `k_EMsgAMAuthenticatedPlayerList` | `4315` | - |
| `k_EMsgAMGetUserGifts` | `4316` | - |
| `k_EMsgAMGetUserGiftsResponse` | `4317` | - |
| `k_EMsgAMTransferLockedGifts` | `4320` | - |
| `k_EMsgAMTransferLockedGiftsResponse` | `4321` | - |
| `k_EMsgAMPlayerHostedOnGameServer` | `4322` | - |
| `k_EMsgAMGetAccountBanInfo` | `4323` | - |
| `k_EMsgAMGetAccountBanInfoResponse` | `4324` | - |
| `k_EMsgAMRecordBanEnforcement` | `4325` | - |
| `k_EMsgAMRollbackGiftTransfer` | `4326` | - |
| `k_EMsgAMRollbackGiftTransferResponse` | `4327` | - |
| `k_EMsgAMHandlePendingTransaction` | `4328` | - |
| `k_EMsgAMRequestClanDetails` | `4329` | - |
| `k_EMsgAMDeleteStoredPaypalAgreement` | `4330` | - |
| `k_EMsgAMGameServerUpdate` | `4331` | - |
| `k_EMsgAMGameServerRemove` | `4332` | - |
| `k_EMsgAMGetPaypalAgreements` | `4333` | - |
| `k_EMsgAMGetPaypalAgreementsResponse` | `4334` | - |
| `k_EMsgAMGameServerPlayerCompatibilityCheck` | `4335` | - |
| `k_EMsgAMGameServerPlayerCompatibilityCheckResponse` | `4336` | - |
| `k_EMsgAMRenewLicense` | `4337` | - |
| `k_EMsgAMGetAccountCommunityBanInfo` | `4338` | - |
| `k_EMsgAMGetAccountCommunityBanInfoResponse` | `4339` | - |
| `k_EMsgAMGameServerAccountChangePassword` | `4340` | - |
| `k_EMsgAMGameServerAccountDeleteAccount` | `4341` | - |
| `k_EMsgAMRenewAgreement` | `4342` | - |
| `k_EMsgAMXsollaPayment` | `4344` | - |
| `k_EMsgAMXsollaPaymentResponse` | `4345` | - |
| `k_EMsgAMAcctAllowedToPurchase` | `4346` | - |
| `k_EMsgAMAcctAllowedToPurchaseResponse` | `4347` | - |
| `k_EMsgAMSwapKioskDeposit` | `4348` | - |
| `k_EMsgAMSwapKioskDepositResponse` | `4349` | - |
| `k_EMsgAMSetUserGiftUnowned` | `4350` | - |
| `k_EMsgAMSetUserGiftUnownedResponse` | `4351` | - |
| `k_EMsgAMClaimUnownedUserGift` | `4352` | - |
| `k_EMsgAMClaimUnownedUserGiftResponse` | `4353` | - |
| `k_EMsgAMSetClanName` | `4354` | - |
| `k_EMsgAMSetClanNameResponse` | `4355` | - |
| `k_EMsgAMGrantCoupon` | `4356` | - |
| `k_EMsgAMGrantCouponResponse` | `4357` | - |
| `k_EMsgAMIsPackageRestrictedInUserCountry` | `4358` | - |
| `k_EMsgAMIsPackageRestrictedInUserCountryResponse` | `4359` | - |
| `k_EMsgAMHandlePendingTransactionResponse` | `4360` | - |
| `k_EMsgAMGrantGuestPasses2` | `4361` | - |
| `k_EMsgAMGrantGuestPasses2Response` | `4362` | - |
| `k_EMsgAMGetPlayerBanDetails` | `4365` | - |
| `k_EMsgAMGetPlayerBanDetailsResponse` | `4366` | - |
| `k_EMsgAMFinalizePurchase` | `4367` | - |
| `k_EMsgAMFinalizePurchaseResponse` | `4368` | - |
| `k_EMsgAMPersonaChangeResponse` | `4372` | - |
| `k_EMsgAMGetClanDetailsForForumCreation` | `4373` | - |
| `k_EMsgAMGetClanDetailsForForumCreationResponse` | `4374` | - |
| `k_EMsgAMGetPendingNotificationCount` | `4375` | - |
| `k_EMsgAMGetPendingNotificationCountResponse` | `4376` | - |
| `k_EMsgAMPasswordHashUpgrade` | `4377` | - |
| `k_EMsgAMBoaCompraPayment` | `4380` | - |
| `k_EMsgAMBoaCompraPaymentResponse` | `4381` | - |
| `k_EMsgAMCompleteExternalPurchase` | `4383` | - |
| `k_EMsgAMCompleteExternalPurchaseResponse` | `4384` | - |
| `k_EMsgAMResolveNegativeWalletCredits` | `4385` | - |
| `k_EMsgAMResolveNegativeWalletCreditsResponse` | `4386` | - |
| `k_EMsgAMPlayerGetClanBasicDetails` | `4389` | - |
| `k_EMsgAMPlayerGetClanBasicDetailsResponse` | `4390` | - |
| `k_EMsgAMMOLPayment` | `4391` | - |
| `k_EMsgAMMOLPaymentResponse` | `4392` | - |
| `k_EMsgGetUserIPCountry` | `4393` | - |
| `k_EMsgGetUserIPCountryResponse` | `4394` | - |
| `k_EMsgNotificationOfSuspiciousActivity` | `4395` | - |
| `k_EMsgAMDegicaPayment` | `4396` | - |
| `k_EMsgAMDegicaPaymentResponse` | `4397` | - |
| `k_EMsgAMEClubPayment` | `4398` | - |
| `k_EMsgAMEClubPaymentResponse` | `4399` | - |
| `k_EMsgAMPayPalPaymentsHubPayment` | `4400` | - |
| `k_EMsgAMPayPalPaymentsHubPaymentResponse` | `4401` | - |
| `k_EMsgAMTwoFactorRecoverAuthenticatorRequest` | `4402` | - |
| `k_EMsgAMTwoFactorRecoverAuthenticatorResponse` | `4403` | - |
| `k_EMsgAMSmart2PayPayment` | `4404` | - |
| `k_EMsgAMSmart2PayPaymentResponse` | `4405` | - |
| `k_EMsgAMValidatePasswordResetCodeAndSendSmsRequest` | `4406` | - |
| `k_EMsgAMValidatePasswordResetCodeAndSendSmsResponse` | `4407` | - |
| `k_EMsgAMGetAccountResetDetailsRequest` | `4408` | - |
| `k_EMsgAMGetAccountResetDetailsResponse` | `4409` | - |
| `k_EMsgAMBitPayPayment` | `4410` | - |
| `k_EMsgAMBitPayPaymentResponse` | `4411` | - |
| `k_EMsgAMSendAccountInfoUpdate` | `4412` | - |
| `k_EMsgAMSendScheduledGift` | `4413` | - |
| `k_EMsgAMNodwinPayment` | `4414` | - |
| `k_EMsgAMNodwinPaymentResponse` | `4415` | - |
| `k_EMsgAMResolveWalletRevoke` | `4416` | - |
| `k_EMsgAMResolveWalletReverseRevoke` | `4417` | - |
| `k_EMsgAMFundedPayment` | `4418` | - |
| `k_EMsgAMFundedPaymentResponse` | `4419` | - |
| `k_EMsgAMRequestPersonaUpdateForChatServer` | `4420` | - |
| `k_EMsgAMPerfectWorldPayment` | `4421` | - |
| `k_EMsgAMPerfectWorldPaymentResponse` | `4422` | - |
| `k_EMsgAMECommPayPayment` | `4423` | - |
| `k_EMsgAMECommPayPaymentResponse` | `4424` | - |
| `k_EMsgAMSetRemoteClientID` | `4425` | - |
| `k_EMsgBasePSRange` | `5000` | - |
| `k_EMsgPSCreateShoppingCart` | `5001` | - |
| `k_EMsgPSCreateShoppingCartResponse` | `5002` | - |
| `k_EMsgPSIsValidShoppingCart` | `5003` | - |
| `k_EMsgPSIsValidShoppingCartResponse` | `5004` | - |
| `k_EMsgPSRemoveLineItemFromShoppingCart` | `5007` | - |
| `k_EMsgPSRemoveLineItemFromShoppingCartResponse` | `5008` | - |
| `k_EMsgPSGetShoppingCartContents` | `5009` | - |
| `k_EMsgPSGetShoppingCartContentsResponse` | `5010` | - |
| `k_EMsgPSAddWalletCreditToShoppingCart` | `5011` | - |
| `k_EMsgPSAddWalletCreditToShoppingCartResponse` | `5012` | - |
| `k_EMsgBaseUFSRange` | `5200` | - |
| `k_EMsgClientUFSUploadFileRequest` | `5202` | - |
| `k_EMsgClientUFSUploadFileResponse` | `5203` | - |
| `k_EMsgClientUFSUploadFileChunk` | `5204` | - |
| `k_EMsgClientUFSUploadFileFinished` | `5205` | - |
| `k_EMsgClientUFSGetFileListForApp` | `5206` | - |
| `k_EMsgClientUFSGetFileListForAppResponse` | `5207` | - |
| `k_EMsgClientUFSDownloadRequest` | `5210` | - |
| `k_EMsgClientUFSDownloadResponse` | `5211` | - |
| `k_EMsgClientUFSDownloadChunk` | `5212` | - |
| `k_EMsgClientUFSLoginRequest` | `5213` | - |
| `k_EMsgClientUFSLoginResponse` | `5214` | - |
| `k_EMsgUFSReloadPartitionInfo` | `5215` | - |
| `k_EMsgClientUFSTransferHeartbeat` | `5216` | - |
| `k_EMsgUFSSynchronizeFile` | `5217` | - |
| `k_EMsgUFSSynchronizeFileResponse` | `5218` | - |
| `k_EMsgClientUFSDeleteFileRequest` | `5219` | - |
| `k_EMsgClientUFSDeleteFileResponse` | `5220` | - |
| `k_EMsgClientUFSGetUGCDetails` | `5226` | - |
| `k_EMsgClientUFSGetUGCDetailsResponse` | `5227` | - |
| `k_EMsgUFSUpdateFileFlags` | `5228` | - |
| `k_EMsgUFSUpdateFileFlagsResponse` | `5229` | - |
| `k_EMsgClientUFSGetSingleFileInfo` | `5230` | - |
| `k_EMsgClientUFSGetSingleFileInfoResponse` | `5231` | - |
| `k_EMsgClientUFSShareFile` | `5232` | - |
| `k_EMsgClientUFSShareFileResponse` | `5233` | - |
| `k_EMsgUFSReloadAccount` | `5234` | - |
| `k_EMsgUFSReloadAccountResponse` | `5235` | - |
| `k_EMsgUFSUpdateRecordBatched` | `5236` | - |
| `k_EMsgUFSUpdateRecordBatchedResponse` | `5237` | - |
| `k_EMsgUFSMigrateFile` | `5238` | - |
| `k_EMsgUFSMigrateFileResponse` | `5239` | - |
| `k_EMsgUFSGetUGCURLs` | `5240` | - |
| `k_EMsgUFSGetUGCURLsResponse` | `5241` | - |
| `k_EMsgUFSHttpUploadFileFinishRequest` | `5242` | - |
| `k_EMsgUFSHttpUploadFileFinishResponse` | `5243` | - |
| `k_EMsgUFSDownloadStartRequest` | `5244` | - |
| `k_EMsgUFSDownloadStartResponse` | `5245` | - |
| `k_EMsgUFSDownloadChunkRequest` | `5246` | - |
| `k_EMsgUFSDownloadChunkResponse` | `5247` | - |
| `k_EMsgUFSDownloadFinishRequest` | `5248` | - |
| `k_EMsgUFSDownloadFinishResponse` | `5249` | - |
| `k_EMsgUFSFlushURLCache` | `5250` | - |
| `k_EMsgClientUFSUploadCommit` | `5251` | - |
| `k_EMsgClientUFSUploadCommitResponse` | `5252` | - |
| `k_EMsgUFSMigrateFileAppID` | `5253` | - |
| `k_EMsgUFSMigrateFileAppIDResponse` | `5254` | - |
| `k_EMsgBaseClient2` | `5400` | - |
| `k_EMsgClientRequestForgottenPasswordEmail` | `5401` | - |
| `k_EMsgClientRequestForgottenPasswordEmailResponse` | `5402` | - |
| `k_EMsgClientCreateAccountResponse` | `5403` | - |
| `k_EMsgClientResetForgottenPassword` | `5404` | - |
| `k_EMsgClientResetForgottenPasswordResponse` | `5405` | - |
| `k_EMsgClientInformOfResetForgottenPassword` | `5407` | - |
| `k_EMsgClientInformOfResetForgottenPasswordResponse` | `5408` | - |
| `k_EMsgClientAnonUserLogOn_Deprecated` | `5409` | - |
| `k_EMsgClientGamesPlayedWithDataBlob` | `5410` | - |
| `k_EMsgClientUpdateUserGameInfo` | `5411` | - |
| `k_EMsgClientFileToDownload` | `5412` | - |
| `k_EMsgClientFileToDownloadResponse` | `5413` | - |
| `k_EMsgClientLBSSetScore` | `5414` | - |
| `k_EMsgClientLBSSetScoreResponse` | `5415` | - |
| `k_EMsgClientLBSFindOrCreateLB` | `5416` | - |
| `k_EMsgClientLBSFindOrCreateLBResponse` | `5417` | - |
| `k_EMsgClientLBSGetLBEntries` | `5418` | - |
| `k_EMsgClientLBSGetLBEntriesResponse` | `5419` | - |
| `k_EMsgClientChatDeclined` | `5426` | - |
| `k_EMsgClientFriendMsgIncoming` | `5427` | - |
| `k_EMsgClientAuthList_Deprecated` | `5428` | - |
| `k_EMsgClientTicketAuthComplete` | `5429` | - |
| `k_EMsgClientIsLimitedAccount` | `5430` | - |
| `k_EMsgClientRequestAuthList` | `5431` | - |
| `k_EMsgClientAuthList` | `5432` | - |
| `k_EMsgClientStat` | `5433` | - |
| `k_EMsgClientP2PConnectionInfo` | `5434` | - |
| `k_EMsgClientP2PConnectionFailInfo` | `5435` | - |
| `k_EMsgClientGetDepotDecryptionKey` | `5438` | - |
| `k_EMsgClientGetDepotDecryptionKeyResponse` | `5439` | - |
| `k_EMsgClientEnableTestLicense` | `5443` | - |
| `k_EMsgClientEnableTestLicenseResponse` | `5444` | - |
| `k_EMsgClientDisableTestLicense` | `5445` | - |
| `k_EMsgClientDisableTestLicenseResponse` | `5446` | - |
| `k_EMsgClientRequestValidationMail` | `5448` | - |
| `k_EMsgClientRequestValidationMailResponse` | `5449` | - |
| `k_EMsgClientCheckAppBetaPassword` | `5450` | - |
| `k_EMsgClientCheckAppBetaPasswordResponse` | `5451` | - |
| `k_EMsgClientToGC` | `5452` | - |
| `k_EMsgClientFromGC` | `5453` | - |
| `k_EMsgClientEmailAddrInfo` | `5456` | - |
| `k_EMsgClientPasswordChange3` | `5457` | - |
| `k_EMsgClientEmailChange3` | `5458` | - |
| `k_EMsgClientPersonalQAChange3` | `5459` | - |
| `k_EMsgClientResetForgottenPassword3` | `5460` | - |
| `k_EMsgClientRequestForgottenPasswordEmail3` | `5461` | - |
| `k_EMsgClientNewLoginKey` | `5463` | - |
| `k_EMsgClientNewLoginKeyAccepted` | `5464` | - |
| `k_EMsgClientLogOnWithHash_Deprecated` | `5465` | - |
| `k_EMsgClientStoreUserStats2` | `5466` | - |
| `k_EMsgClientStatsUpdated` | `5467` | - |
| `k_EMsgClientActivateOEMLicense` | `5468` | - |
| `k_EMsgClientRegisterOEMMachine` | `5469` | - |
| `k_EMsgClientRegisterOEMMachineResponse` | `5470` | - |
| `k_EMsgClientRequestedClientStats` | `5480` | - |
| `k_EMsgClientStat2Int32` | `5481` | - |
| `k_EMsgClientStat2` | `5482` | - |
| `k_EMsgClientVerifyPassword` | `5483` | - |
| `k_EMsgClientVerifyPasswordResponse` | `5484` | - |
| `k_EMsgClientDRMDownloadRequest` | `5485` | - |
| `k_EMsgClientDRMDownloadResponse` | `5486` | - |
| `k_EMsgClientDRMFinalResult` | `5487` | - |
| `k_EMsgClientGetFriendsWhoPlayGame` | `5488` | - |
| `k_EMsgClientGetFriendsWhoPlayGameResponse` | `5489` | - |
| `k_EMsgClientOGSBeginSession` | `5490` | - |
| `k_EMsgClientOGSBeginSessionResponse` | `5491` | - |
| `k_EMsgClientOGSEndSession` | `5492` | - |
| `k_EMsgClientOGSEndSessionResponse` | `5493` | - |
| `k_EMsgClientOGSWriteRow` | `5494` | - |
| `k_EMsgClientGetPeerContentInfo` | `5495` | - |
| `k_EMsgClientGetPeerContentInfoResponse` | `5496` | - |
| `k_EMsgClientStartPeerContentServer` | `5497` | - |
| `k_EMsgClientStartPeerContentServerResponse` | `5498` | - |
| `k_EMsgClientServerUnavailable` | `5500` | - |
| `k_EMsgClientServersAvailable` | `5501` | - |
| `k_EMsgClientRegisterAuthTicketWithCM` | `5502` | - |
| `k_EMsgClientGCMsgFailed` | `5503` | - |
| `k_EMsgClientMicroTxnAuthRequest` | `5504` | - |
| `k_EMsgClientMicroTxnAuthorize` | `5505` | - |
| `k_EMsgClientMicroTxnAuthorizeResponse` | `5506` | - |
| `k_EMsgClientGetMicroTxnInfo` | `5508` | - |
| `k_EMsgClientGetMicroTxnInfoResponse` | `5509` | - |
| `k_EMsgClientDeregisterWithServer` | `5511` | - |
| `k_EMsgClientSubscribeToPersonaFeed` | `5512` | - |
| `k_EMsgClientLogon` | `5514` | - |
| `k_EMsgClientGetClientDetails` | `5515` | - |
| `k_EMsgClientGetClientDetailsResponse` | `5516` | - |
| `k_EMsgClientReportOverlayDetourFailure` | `5517` | - |
| `k_EMsgClientGetClientAppList` | `5518` | - |
| `k_EMsgClientGetClientAppListResponse` | `5519` | - |
| `k_EMsgClientInstallClientApp` | `5520` | - |
| `k_EMsgClientInstallClientAppResponse` | `5521` | - |
| `k_EMsgClientUninstallClientApp` | `5522` | - |
| `k_EMsgClientUninstallClientAppResponse` | `5523` | - |
| `k_EMsgClientSetClientAppUpdateState` | `5524` | - |
| `k_EMsgClientSetClientAppUpdateStateResponse` | `5525` | - |
| `k_EMsgClientRequestEncryptedAppTicket` | `5526` | - |
| `k_EMsgClientRequestEncryptedAppTicketResponse` | `5527` | - |
| `k_EMsgClientWalletInfoUpdate` | `5528` | - |
| `k_EMsgClientLBSSetUGC` | `5529` | - |
| `k_EMsgClientLBSSetUGCResponse` | `5530` | - |
| `k_EMsgClientAMGetClanOfficers` | `5531` | - |
| `k_EMsgClientAMGetClanOfficersResponse` | `5532` | - |
| `k_EMsgClientFriendProfileInfo` | `5535` | - |
| `k_EMsgClientFriendProfileInfoResponse` | `5536` | - |
| `k_EMsgClientUpdateMachineAuth` | `5537` | - |
| `k_EMsgClientUpdateMachineAuthResponse` | `5538` | - |
| `k_EMsgClientReadMachineAuth` | `5539` | - |
| `k_EMsgClientReadMachineAuthResponse` | `5540` | - |
| `k_EMsgClientRequestMachineAuth` | `5541` | - |
| `k_EMsgClientRequestMachineAuthResponse` | `5542` | - |
| `k_EMsgClientScreenshotsChanged` | `5543` | - |
| `k_EMsgClientGetCDNAuthToken` | `5546` | - |
| `k_EMsgClientGetCDNAuthTokenResponse` | `5547` | - |
| `k_EMsgClientDownloadRateStatistics` | `5548` | - |
| `k_EMsgClientRequestAccountData` | `5549` | - |
| `k_EMsgClientRequestAccountDataResponse` | `5550` | - |
| `k_EMsgClientResetForgottenPassword4` | `5551` | - |
| `k_EMsgClientHideFriend` | `5552` | - |
| `k_EMsgClientFriendsGroupsList` | `5553` | - |
| `k_EMsgClientGetClanActivityCounts` | `5554` | - |
| `k_EMsgClientGetClanActivityCountsResponse` | `5555` | - |
| `k_EMsgClientOGSReportString` | `5556` | - |
| `k_EMsgClientOGSReportBug` | `5557` | - |
| `k_EMsgClientSentLogs` | `5558` | - |
| `k_EMsgClientLogonGameServer` | `5559` | - |
| `k_EMsgAMClientCreateFriendsGroup` | `5560` | - |
| `k_EMsgAMClientCreateFriendsGroupResponse` | `5561` | - |
| `k_EMsgAMClientDeleteFriendsGroup` | `5562` | - |
| `k_EMsgAMClientDeleteFriendsGroupResponse` | `5563` | - |
| `k_EMsgAMClientManageFriendsGroup` | `5564` | - |
| `k_EMsgAMClientManageFriendsGroupResponse` | `5565` | - |
| `k_EMsgAMClientAddFriendToGroup` | `5566` | - |
| `k_EMsgAMClientAddFriendToGroupResponse` | `5567` | - |
| `k_EMsgAMClientRemoveFriendFromGroup` | `5568` | - |
| `k_EMsgAMClientRemoveFriendFromGroupResponse` | `5569` | - |
| `k_EMsgClientAMGetPersonaNameHistory` | `5570` | - |
| `k_EMsgClientAMGetPersonaNameHistoryResponse` | `5571` | - |
| `k_EMsgClientRequestFreeLicense` | `5572` | - |
| `k_EMsgClientRequestFreeLicenseResponse` | `5573` | - |
| `k_EMsgClientDRMDownloadRequestWithCrashData` | `5574` | - |
| `k_EMsgClientAuthListAck` | `5575` | - |
| `k_EMsgClientItemAnnouncements` | `5576` | - |
| `k_EMsgClientRequestItemAnnouncements` | `5577` | - |
| `k_EMsgClientFriendMsgEchoToSender` | `5578` | - |
| `k_EMsgClientCommentNotifications` | `5582` | - |
| `k_EMsgClientRequestCommentNotifications` | `5583` | - |
| `k_EMsgClientPersonaChangeResponse` | `5584` | - |
| `k_EMsgClientRequestWebAPIAuthenticateUserNonce` | `5585` | - |
| `k_EMsgClientRequestWebAPIAuthenticateUserNonceResponse` | `5586` | - |
| `k_EMsgClientPlayerNicknameList` | `5587` | - |
| `k_EMsgAMClientSetPlayerNickname` | `5588` | - |
| `k_EMsgAMClientSetPlayerNicknameResponse` | `5589` | - |
| `k_EMsgClientGetNumberOfCurrentPlayersDP` | `5592` | - |
| `k_EMsgClientGetNumberOfCurrentPlayersDPResponse` | `5593` | - |
| `k_EMsgClientServiceMethodLegacy` | `5594` | - |
| `k_EMsgClientServiceMethodLegacyResponse` | `5595` | - |
| `k_EMsgClientFriendUserStatusPublished` | `5596` | - |
| `k_EMsgClientCurrentUIMode` | `5597` | - |
| `k_EMsgClientVanityURLChangedNotification` | `5598` | - |
| `k_EMsgClientUserNotifications` | `5599` | - |
| `k_EMsgBaseDFS` | `5600` | - |
| `k_EMsgDFSGetFile` | `5601` | - |
| `k_EMsgDFSInstallLocalFile` | `5602` | - |
| `k_EMsgDFSConnection` | `5603` | - |
| `k_EMsgDFSConnectionReply` | `5604` | - |
| `k_EMsgClientDFSAuthenticateRequest` | `5605` | - |
| `k_EMsgClientDFSAuthenticateResponse` | `5606` | - |
| `k_EMsgClientDFSEndSession` | `5607` | - |
| `k_EMsgDFSPurgeFile` | `5608` | - |
| `k_EMsgDFSRouteFile` | `5609` | - |
| `k_EMsgDFSGetFileFromServer` | `5610` | - |
| `k_EMsgDFSAcceptedResponse` | `5611` | - |
| `k_EMsgDFSRequestPingback` | `5612` | - |
| `k_EMsgDFSRecvTransmitFile` | `5613` | - |
| `k_EMsgDFSSendTransmitFile` | `5614` | - |
| `k_EMsgDFSRequestPingback2` | `5615` | - |
| `k_EMsgDFSResponsePingback2` | `5616` | - |
| `k_EMsgClientDFSDownloadStatus` | `5617` | - |
| `k_EMsgDFSStartTransfer` | `5618` | - |
| `k_EMsgDFSTransferComplete` | `5619` | - |
| `k_EMsgDFSRouteFileResponse` | `5620` | - |
| `k_EMsgClientNetworkingCertRequest` | `5621` | - |
| `k_EMsgClientNetworkingCertRequestResponse` | `5622` | - |
| `k_EMsgClientChallengeRequest` | `5623` | - |
| `k_EMsgClientChallengeResponse` | `5624` | - |
| `k_EMsgBadgeCraftedNotification` | `5625` | - |
| `k_EMsgClientNetworkingMobileCertRequest` | `5626` | - |
| `k_EMsgClientNetworkingMobileCertRequestResponse` | `5627` | - |
| `k_EMsgBaseMDS` | `5800` | - |
| `k_EMsgMDSGetDepotDecryptionKey` | `5812` | - |
| `k_EMsgMDSGetDepotDecryptionKeyResponse` | `5813` | - |
| `k_EMsgMDSContentServerConfigRequest` | `5827` | - |
| `k_EMsgMDSContentServerConfig` | `5828` | - |
| `k_EMsgMDSGetDepotManifest` | `5829` | - |
| `k_EMsgMDSGetDepotManifestResponse` | `5830` | - |
| `k_EMsgMDSGetDepotManifestChunk` | `5831` | - |
| `k_EMsgMDSGetDepotChunk` | `5832` | - |
| `k_EMsgMDSGetDepotChunkResponse` | `5833` | - |
| `k_EMsgMDSGetDepotChunkChunk` | `5834` | - |
| `k_EMsgMDSToCSFlushChunk` | `5844` | - |
| `k_EMsgMDSMigrateChunk` | `5847` | - |
| `k_EMsgMDSMigrateChunkResponse` | `5848` | - |
| `k_EMsgMDSToCSFlushManifest` | `5849` | - |
| `k_EMsgCSBase` | `6200` | - |
| `k_EMsgCSPing` | `6201` | - |
| `k_EMsgCSPingResponse` | `6202` | - |
| `k_EMsgGMSBase` | `6400` | - |
| `k_EMsgGMSGameServerReplicate` | `6401` | - |
| `k_EMsgClientGMSServerQuery` | `6403` | - |
| `k_EMsgGMSClientServerQueryResponse` | `6404` | - |
| `k_EMsgAMGMSGameServerUpdate` | `6405` | - |
| `k_EMsgAMGMSGameServerRemove` | `6406` | - |
| `k_EMsgGameServerOutOfDate` | `6407` | - |
| `k_EMsgDeviceAuthorizationBase` | `6500` | - |
| `k_EMsgClientAuthorizeLocalDeviceRequest` | `6501` | - |
| `k_EMsgClientAuthorizeLocalDeviceResponse` | `6502` | - |
| `k_EMsgClientDeauthorizeDeviceRequest` | `6503` | - |
| `k_EMsgClientDeauthorizeDevice` | `6504` | - |
| `k_EMsgClientUseLocalDeviceAuthorizations` | `6505` | - |
| `k_EMsgClientGetAuthorizedDevices` | `6506` | - |
| `k_EMsgClientGetAuthorizedDevicesResponse` | `6507` | - |
| `k_EMsgAMNotifySessionDeviceAuthorized` | `6508` | - |
| `k_EMsgClientAuthorizeLocalDeviceNotification` | `6509` | - |
| `k_EMsgMMSBase` | `6600` | - |
| `k_EMsgClientMMSCreateLobby` | `6601` | - |
| `k_EMsgClientMMSCreateLobbyResponse` | `6602` | - |
| `k_EMsgClientMMSJoinLobby` | `6603` | - |
| `k_EMsgClientMMSJoinLobbyResponse` | `6604` | - |
| `k_EMsgClientMMSLeaveLobby` | `6605` | - |
| `k_EMsgClientMMSLeaveLobbyResponse` | `6606` | - |
| `k_EMsgClientMMSGetLobbyList` | `6607` | - |
| `k_EMsgClientMMSGetLobbyListResponse` | `6608` | - |
| `k_EMsgClientMMSSetLobbyData` | `6609` | - |
| `k_EMsgClientMMSSetLobbyDataResponse` | `6610` | - |
| `k_EMsgClientMMSGetLobbyData` | `6611` | - |
| `k_EMsgClientMMSLobbyData` | `6612` | - |
| `k_EMsgClientMMSSendLobbyChatMsg` | `6613` | - |
| `k_EMsgClientMMSLobbyChatMsg` | `6614` | - |
| `k_EMsgClientMMSSetLobbyOwner` | `6615` | - |
| `k_EMsgClientMMSSetLobbyOwnerResponse` | `6616` | - |
| `k_EMsgClientMMSSetLobbyGameServer` | `6617` | - |
| `k_EMsgClientMMSLobbyGameServerSet` | `6618` | - |
| `k_EMsgClientMMSUserJoinedLobby` | `6619` | - |
| `k_EMsgClientMMSUserLeftLobby` | `6620` | - |
| `k_EMsgClientMMSInviteToLobby` | `6621` | - |
| `k_EMsgClientMMSFlushFrenemyListCache` | `6622` | - |
| `k_EMsgClientMMSFlushFrenemyListCacheResponse` | `6623` | - |
| `k_EMsgClientMMSSetLobbyLinked` | `6624` | - |
| `k_EMsgClientMMSSetRatelimitPolicyOnClient` | `6625` | - |
| `k_EMsgClientMMSGetLobbyStatus` | `6626` | - |
| `k_EMsgClientMMSGetLobbyStatusResponse` | `6627` | - |
| `k_EMsgMMSGetLobbyList` | `6628` | - |
| `k_EMsgMMSGetLobbyListResponse` | `6629` | - |
| `k_EMsgNonStdMsgBase` | `6800` | - |
| `k_EMsgNonStdMsgMemcached` | `6801` | - |
| `k_EMsgNonStdMsgHTTPServer` | `6802` | - |
| `k_EMsgNonStdMsgHTTPClient` | `6803` | - |
| `k_EMsgNonStdMsgWGResponse` | `6804` | - |
| `k_EMsgNonStdMsgPHPSimulator` | `6805` | - |
| `k_EMsgNonStdMsgChase` | `6806` | - |
| `k_EMsgNonStdMsgDFSTransfer` | `6807` | - |
| `k_EMsgNonStdMsgTests` | `6808` | - |
| `k_EMsgNonStdMsgUMQpipeAAPL` | `6809` | - |
| `k_EMSgNonStdMsgSyslog` | `6810` | - |
| `k_EMsgNonStdMsgLogsink` | `6811` | - |
| `k_EMsgNonStdMsgSteam2Emulator` | `6812` | - |
| `k_EMsgNonStdMsgRTMPServer` | `6813` | - |
| `k_EMsgNonStdMsgWebSocket` | `6814` | - |
| `k_EMsgNonStdMsgRedis` | `6815` | - |
| `k_EMsgUDSBase` | `7000` | - |
| `k_EMsgClientUDSP2PSessionStarted` | `7001` | - |
| `k_EMsgClientUDSP2PSessionEnded` | `7002` | - |
| `k_EMsgUDSRenderUserAuth` | `7003` | - |
| `k_EMsgUDSRenderUserAuthResponse` | `7004` | - |
| `k_EMsgClientInviteToGame` | `7005` | - |
| `k_EMsgUDSHasSession` | `7006` | - |
| `k_EMsgUDSHasSessionResponse` | `7007` | - |
| `k_EMsgMPASBase` | `7100` | - |
| `k_EMsgMPASVacBanReset` | `7101` | - |
| `k_EMsgKGSBase` | `7200` | - |
| `k_EMsgUCMBase` | `7300` | - |
| `k_EMsgClientUCMAddScreenshot` | `7301` | - |
| `k_EMsgClientUCMAddScreenshotResponse` | `7302` | - |
| `k_EMsgUCMResetCommunityContent` | `7307` | - |
| `k_EMsgUCMResetCommunityContentResponse` | `7308` | - |
| `k_EMsgClientUCMDeleteScreenshot` | `7309` | - |
| `k_EMsgClientUCMDeleteScreenshotResponse` | `7310` | - |
| `k_EMsgClientUCMPublishFile` | `7311` | - |
| `k_EMsgClientUCMPublishFileResponse` | `7312` | - |
| `k_EMsgClientUCMDeletePublishedFile` | `7315` | - |
| `k_EMsgClientUCMDeletePublishedFileResponse` | `7316` | - |
| `k_EMsgClientUCMUpdatePublishedFile` | `7325` | - |
| `k_EMsgClientUCMUpdatePublishedFileResponse` | `7326` | - |
| `k_EMsgUCMUpdatePublishedFile` | `7327` | - |
| `k_EMsgUCMUpdatePublishedFileResponse` | `7328` | - |
| `k_EMsgUCMUpdatePublishedFileStat` | `7331` | - |
| `k_EMsgUCMReloadPublishedFile` | `7337` | - |
| `k_EMsgUCMReloadUserFileListCaches` | `7338` | - |
| `k_EMsgUCMPublishedFileReported` | `7339` | - |
| `k_EMsgUCMPublishedFilePreviewAdd` | `7341` | - |
| `k_EMsgUCMPublishedFilePreviewAddResponse` | `7342` | - |
| `k_EMsgUCMPublishedFilePreviewRemove` | `7343` | - |
| `k_EMsgUCMPublishedFilePreviewRemoveResponse` | `7344` | - |
| `k_EMsgUCMPublishedFileSubscribed` | `7349` | - |
| `k_EMsgUCMPublishedFileUnsubscribed` | `7350` | - |
| `k_EMsgUCMPublishFile` | `7351` | - |
| `k_EMsgUCMPublishFileResponse` | `7352` | - |
| `k_EMsgUCMPublishedFileChildAdd` | `7353` | - |
| `k_EMsgUCMPublishedFileChildAddResponse` | `7354` | - |
| `k_EMsgUCMPublishedFileChildRemove` | `7355` | - |
| `k_EMsgUCMPublishedFileChildRemoveResponse` | `7356` | - |
| `k_EMsgUCMPublishedFileParentChanged` | `7359` | - |
| `k_EMsgClientUCMSetUserPublishedFileAction` | `7364` | - |
| `k_EMsgClientUCMSetUserPublishedFileActionResponse` | `7365` | - |
| `k_EMsgClientUCMEnumeratePublishedFilesByUserAction` | `7366` | - |
| `k_EMsgClientUCMEnumeratePublishedFilesByUserActionResponse` | `7367` | - |
| `k_EMsgUCMGetUserSubscribedFiles` | `7369` | - |
| `k_EMsgUCMGetUserSubscribedFilesResponse` | `7370` | - |
| `k_EMsgUCMFixStatsPublishedFile` | `7371` | - |
| `k_EMsgClientUCMEnumerateUserSubscribedFilesWithUpdates` | `7378` | - |
| `k_EMsgClientUCMEnumerateUserSubscribedFilesWithUpdatesResponse` | `7379` | - |
| `k_EMsgUCMPublishedFileContentUpdated` | `7380` | - |
| `k_EMsgClientUCMPublishedFileUpdated` | `7381` | - |
| `k_EMsgFSBase` | `7500` | - |
| `k_EMsgClientRichPresenceUpload` | `7501` | - |
| `k_EMsgClientRichPresenceRequest` | `7502` | - |
| `k_EMsgClientRichPresenceInfo` | `7503` | - |
| `k_EMsgFSRichPresenceRequest` | `7504` | - |
| `k_EMsgFSRichPresenceResponse` | `7505` | - |
| `k_EMsgFSComputeFrenematrix` | `7506` | - |
| `k_EMsgFSComputeFrenematrixResponse` | `7507` | - |
| `k_EMsgFSPlayStatusNotification` | `7508` | - |
| `k_EMsgFSAddOrRemoveFollower` | `7510` | - |
| `k_EMsgFSAddOrRemoveFollowerResponse` | `7511` | - |
| `k_EMsgFSUpdateFollowingList` | `7512` | - |
| `k_EMsgFSCommentNotification` | `7513` | - |
| `k_EMsgFSCommentNotificationViewed` | `7514` | - |
| `k_EMsgClientFSGetFollowerCount` | `7515` | - |
| `k_EMsgClientFSGetFollowerCountResponse` | `7516` | - |
| `k_EMsgClientFSGetIsFollowing` | `7517` | - |
| `k_EMsgClientFSGetIsFollowingResponse` | `7518` | - |
| `k_EMsgClientFSEnumerateFollowingList` | `7519` | - |
| `k_EMsgClientFSEnumerateFollowingListResponse` | `7520` | - |
| `k_EMsgFSGetPendingNotificationCount` | `7521` | - |
| `k_EMsgFSGetPendingNotificationCountResponse` | `7522` | - |
| `k_EMsgClientChatOfflineMessageNotification` | `7523` | - |
| `k_EMsgClientChatRequestOfflineMessageCount` | `7524` | - |
| `k_EMsgClientChatGetFriendMessageHistory` | `7525` | - |
| `k_EMsgClientChatGetFriendMessageHistoryResponse` | `7526` | - |
| `k_EMsgClientChatGetFriendMessageHistoryForOfflineMessages` | `7527` | - |
| `k_EMsgClientFSGetFriendsSteamLevels` | `7528` | - |
| `k_EMsgClientFSGetFriendsSteamLevelsResponse` | `7529` | - |
| `k_EMsgAMRequestFriendData` | `7530` | - |
| `k_EMsgDRMRange2` | `7600` | - |
| `k_EMsgCEGVersionSetEnableDisableRequest` | `7600` | - |
| `k_EMsgCEGVersionSetEnableDisableResponse` | `7601` | - |
| `k_EMsgCEGPropStatusDRMSRequest` | `7602` | - |
| `k_EMsgCEGPropStatusDRMSResponse` | `7603` | - |
| `k_EMsgCEGWhackFailureReportRequest` | `7604` | - |
| `k_EMsgCEGWhackFailureReportResponse` | `7605` | - |
| `k_EMsgDRMSFetchVersionSet` | `7606` | - |
| `k_EMsgDRMSFetchVersionSetResponse` | `7607` | - |
| `k_EMsgEconBase` | `7700` | - |
| `k_EMsgEconTrading_InitiateTradeRequest` | `7701` | - |
| `k_EMsgEconTrading_InitiateTradeProposed` | `7702` | - |
| `k_EMsgEconTrading_InitiateTradeResponse` | `7703` | - |
| `k_EMsgEconTrading_InitiateTradeResult` | `7704` | - |
| `k_EMsgEconTrading_StartSession` | `7705` | - |
| `k_EMsgEconTrading_CancelTradeRequest` | `7706` | - |
| `k_EMsgEconFlushInventoryCache` | `7707` | - |
| `k_EMsgEconFlushInventoryCacheResponse` | `7708` | - |
| `k_EMsgEconCDKeyProcessTransaction` | `7711` | - |
| `k_EMsgEconCDKeyProcessTransactionResponse` | `7712` | - |
| `k_EMsgEconGetErrorLogs` | `7713` | - |
| `k_EMsgEconGetErrorLogsResponse` | `7714` | - |
| `k_EMsgRMRange` | `7800` | - |
| `k_EMsgRMTestVerisignOTP` | `7800` | - |
| `k_EMsgRMTestVerisignOTPResponse` | `7801` | - |
| `k_EMsgRMDeleteMemcachedKeys` | `7803` | - |
| `k_EMsgRMRemoteInvoke` | `7804` | - |
| `k_EMsgBadLoginIPList` | `7805` | - |
| `k_EMsgRMMsgTraceAddTrigger` | `7806` | - |
| `k_EMsgRMMsgTraceRemoveTrigger` | `7807` | - |
| `k_EMsgRMMsgTraceEvent` | `7808` | - |
| `k_EMsgUGSBase` | `7900` | - |
| `k_EMsgUGSUpdateGlobalStats` | `7900` | - |
| `k_EMsgClientUGSGetGlobalStats` | `7901` | - |
| `k_EMsgClientUGSGetGlobalStatsResponse` | `7902` | - |
| `k_EMsgStoreBase` | `8000` | - |
| `k_EMsgUMQBase` | `8100` | - |
| `k_EMsgUMQLogonRequest` | `8100` | - |
| `k_EMsgUMQLogonResponse` | `8101` | - |
| `k_EMsgUMQLogoffRequest` | `8102` | - |
| `k_EMsgUMQLogoffResponse` | `8103` | - |
| `k_EMsgUMQSendChatMessage` | `8104` | - |
| `k_EMsgUMQIncomingChatMessage` | `8105` | - |
| `k_EMsgUMQPoll` | `8106` | - |
| `k_EMsgUMQPollResults` | `8107` | - |
| `k_EMsgUMQ2AM_ClientMsgBatch` | `8108` | - |
| `k_EMsgWorkshopBase` | `8200` | - |
| `k_EMsgWebAPIBase` | `8300` | - |
| `k_EMsgWebAPIValidateOAuth2Token` | `8300` | - |
| `k_EMsgWebAPIValidateOAuth2TokenResponse` | `8301` | - |
| `k_EMsgWebAPIRegisterGCInterfaces` | `8303` | - |
| `k_EMsgWebAPIInvalidateOAuthClientCache` | `8304` | - |
| `k_EMsgWebAPIInvalidateOAuthTokenCache` | `8305` | - |
| `k_EMsgWebAPISetSecrets` | `8306` | - |
| `k_EMsgBackpackBase` | `8400` | - |
| `k_EMsgBackpackAddToCurrency` | `8401` | - |
| `k_EMsgBackpackAddToCurrencyResponse` | `8402` | - |
| `k_EMsgCREBase` | `8500` | - |
| `k_EMsgCREItemVoteSummary` | `8503` | - |
| `k_EMsgCREItemVoteSummaryResponse` | `8504` | - |
| `k_EMsgCREUpdateUserPublishedItemVote` | `8507` | - |
| `k_EMsgCREUpdateUserPublishedItemVoteResponse` | `8508` | - |
| `k_EMsgCREGetUserPublishedItemVoteDetails` | `8509` | - |
| `k_EMsgCREGetUserPublishedItemVoteDetailsResponse` | `8510` | - |
| `k_EMsgSecretsBase` | `8600` | - |
| `k_EMsgSecretsRequestCredentialPair` | `8600` | - |
| `k_EMsgSecretsCredentialPairResponse` | `8601` | - |
| `k_EMsgBoxMonitorBase` | `8700` | - |
| `k_EMsgBoxMonitorReportRequest` | `8700` | - |
| `k_EMsgBoxMonitorReportResponse` | `8701` | - |
| `k_EMsgLogsinkBase` | `8800` | - |
| `k_EMsgLogsinkWriteReport` | `8800` | - |
| `k_EMsgPICSBase` | `8900` | - |
| `k_EMsgClientPICSChangesSinceRequest` | `8901` | - |
| `k_EMsgClientPICSChangesSinceResponse` | `8902` | - |
| `k_EMsgClientPICSProductInfoRequest` | `8903` | - |
| `k_EMsgClientPICSProductInfoResponse` | `8904` | - |
| `k_EMsgClientPICSAccessTokenRequest` | `8905` | - |
| `k_EMsgClientPICSAccessTokenResponse` | `8906` | - |
| `k_EMsgWorkerProcess` | `9000` | - |
| `k_EMsgWorkerProcessPingRequest` | `9000` | - |
| `k_EMsgWorkerProcessPingResponse` | `9001` | - |
| `k_EMsgWorkerProcessShutdown` | `9002` | - |
| `k_EMsgDRMWorkerProcess` | `9100` | - |
| `k_EMsgDRMWorkerProcessDRMAndSign` | `9100` | - |
| `k_EMsgDRMWorkerProcessDRMAndSignResponse` | `9101` | - |
| `k_EMsgDRMWorkerProcessSteamworksInfoRequest` | `9102` | - |
| `k_EMsgDRMWorkerProcessSteamworksInfoResponse` | `9103` | - |
| `k_EMsgDRMWorkerProcessInstallDRMDLLRequest` | `9104` | - |
| `k_EMsgDRMWorkerProcessInstallDRMDLLResponse` | `9105` | - |
| `k_EMsgDRMWorkerProcessSecretIdStringRequest` | `9106` | - |
| `k_EMsgDRMWorkerProcessSecretIdStringResponse` | `9107` | - |
| `k_EMsgDRMWorkerProcessInstallProcessedFilesRequest` | `9110` | - |
| `k_EMsgDRMWorkerProcessInstallProcessedFilesResponse` | `9111` | - |
| `k_EMsgDRMWorkerProcessExamineBlobRequest` | `9112` | - |
| `k_EMsgDRMWorkerProcessExamineBlobResponse` | `9113` | - |
| `k_EMsgDRMWorkerProcessDescribeSecretRequest` | `9114` | - |
| `k_EMsgDRMWorkerProcessDescribeSecretResponse` | `9115` | - |
| `k_EMsgDRMWorkerProcessBackfillOriginalRequest` | `9116` | - |
| `k_EMsgDRMWorkerProcessBackfillOriginalResponse` | `9117` | - |
| `k_EMsgDRMWorkerProcessValidateDRMDLLRequest` | `9118` | - |
| `k_EMsgDRMWorkerProcessValidateDRMDLLResponse` | `9119` | - |
| `k_EMsgDRMWorkerProcessValidateFileRequest` | `9120` | - |
| `k_EMsgDRMWorkerProcessValidateFileResponse` | `9121` | - |
| `k_EMsgDRMWorkerProcessSplitAndInstallRequest` | `9122` | - |
| `k_EMsgDRMWorkerProcessSplitAndInstallResponse` | `9123` | - |
| `k_EMsgDRMWorkerProcessGetBlobRequest` | `9124` | - |
| `k_EMsgDRMWorkerProcessGetBlobResponse` | `9125` | - |
| `k_EMsgDRMWorkerProcessEvaluateCrashRequest` | `9126` | - |
| `k_EMsgDRMWorkerProcessEvaluateCrashResponse` | `9127` | - |
| `k_EMsgDRMWorkerProcessAnalyzeFileRequest` | `9128` | - |
| `k_EMsgDRMWorkerProcessAnalyzeFileResponse` | `9129` | - |
| `k_EMsgDRMWorkerProcessUnpackBlobRequest` | `9130` | - |
| `k_EMsgDRMWorkerProcessUnpackBlobResponse` | `9131` | - |
| `k_EMsgDRMWorkerProcessInstallAllRequest` | `9132` | - |
| `k_EMsgDRMWorkerProcessInstallAllResponse` | `9133` | - |
| `k_EMsgTestWorkerProcess` | `9200` | - |
| `k_EMsgTestWorkerProcessLoadUnloadModuleRequest` | `9200` | - |
| `k_EMsgTestWorkerProcessLoadUnloadModuleResponse` | `9201` | - |
| `k_EMsgTestWorkerProcessServiceModuleCallRequest` | `9202` | - |
| `k_EMsgTestWorkerProcessServiceModuleCallResponse` | `9203` | - |
| `k_EMsgQuestServerBase` | `9300` | - |
| `k_EMsgClientGetEmoticonList` | `9330` | - |
| `k_EMsgClientEmoticonList` | `9331` | - |
| `k_EMsgSLCBase` | `9400` | - |
| `k_EMsgSLCUserSessionStatus` | `9400` | - |
| `k_EMsgSLCRequestUserSessionStatus` | `9401` | - |
| `k_EMsgSLCSharedLicensesLockStatus` | `9402` | - |
| `k_EMsgClientSharedLibraryLockStatus` | `9405` | - |
| `k_EMsgClientSharedLibraryStopPlaying` | `9406` | - |
| `k_EMsgSLCOwnerLibraryChanged` | `9407` | - |
| `k_EMsgSLCSharedLibraryChanged` | `9408` | - |
| `k_EMsgRemoteClientBase` | `9500` | - |
| `k_EMsgRemoteClientAuth_OBSOLETE` | `9500` | - |
| `k_EMsgRemoteClientAuthResponse_OBSOLETE` | `9501` | - |
| `k_EMsgRemoteClientAppStatus` | `9502` | - |
| `k_EMsgRemoteClientStartStream` | `9503` | - |
| `k_EMsgRemoteClientStartStreamResponse` | `9504` | - |
| `k_EMsgRemoteClientPing` | `9505` | - |
| `k_EMsgRemoteClientPingResponse` | `9506` | - |
| `k_EMsgClientUnlockH264` | `9507` | - |
| `k_EMsgClientUnlockH264Response` | `9508` | - |
| `k_EMsgRemoteClientAcceptEULA` | `9509` | - |
| `k_EMsgRemoteClientGetControllerConfig` | `9510` | - |
| `k_EMsgRemoteClientGetControllerConfigResponse` | `9511` | - |
| `k_EMsgRemoteClientStreamingEnabled` | `9512` | - |
| `k_EMsgClientUnlockHEVC_OBSOLETE` | `9513` | - |
| `k_EMsgClientUnlockHEVCResponse_OBSOLETE` | `9514` | - |
| `k_EMsgRemoteClientStatusRequest` | `9515` | - |
| `k_EMsgRemoteClientStatusResponse` | `9516` | - |
| `k_EMsgClientConcurrentSessionsBase` | `9600` | - |
| `k_EMsgClientPlayingSessionState` | `9600` | - |
| `k_EMsgClientKickPlayingSession` | `9601` | - |
| `k_EMsgClientBroadcastBase` | `9700` | - |
| `k_EMsgClientBroadcastInit` | `9700` | - |
| `k_EMsgClientBroadcastFrames` | `9701` | - |
| `k_EMsgClientBroadcastDisconnect` | `9702` | - |
| `k_EMsgClientBroadcastUploadConfig` | `9704` | - |
| `k_EMsgBaseClient3` | `9800` | - |
| `k_EMsgClientVoiceCallPreAuthorize` | `9800` | - |
| `k_EMsgClientVoiceCallPreAuthorizeResponse` | `9801` | - |
| `k_EMsgClientServerTimestampRequest` | `9802` | - |
| `k_EMsgClientServerTimestampResponse` | `9803` | - |
| `k_EMsgServiceMethodCallFromClientNonAuthed` | `9804` | - |
| `k_EMsgClientHello` | `9805` | - |
| `k_EMsgClientEnableOrDisableDownloads` | `9806` | - |
| `k_EMsgClientEnableOrDisableDownloadsResponse` | `9807` | - |
| `k_EMsgClientLANP2PBase` | `9900` | - |
| `k_EMsgClientLANP2PRequestChunk` | `9900` | - |
| `k_EMsgClientLANP2PRequestChunkResponse` | `9901` | - |
| `k_EMsgClientPeerChunkRequest` | `9902` | - |
| `k_EMsgClientPeerChunkResponse` | `9903` | - |
| `k_EMsgClientLANP2PMax` | `9999` | - |
| `k_EMsgBaseWatchdogServer` | `10000` | - |
| `k_EMsgNotifyWatchdog` | `10000` | - |
| `k_EMsgClientSiteLicenseBase` | `10100` | - |
| `k_EMsgClientSiteLicenseSiteInfoNotification` | `10100` | - |
| `k_EMsgClientSiteLicenseCheckout` | `10101` | - |
| `k_EMsgClientSiteLicenseCheckoutResponse` | `10102` | - |
| `k_EMsgClientSiteLicenseGetAvailableSeats` | `10103` | - |
| `k_EMsgClientSiteLicenseGetAvailableSeatsResponse` | `10104` | - |
| `k_EMsgClientSiteLicenseGetContentCacheInfo` | `10105` | - |
| `k_EMsgClientSiteLicenseGetContentCacheInfoResponse` | `10106` | - |
| `k_EMsgBaseChatServer` | `12000` | - |
| `k_EMsgChatServerGetPendingNotificationCount` | `12000` | - |
| `k_EMsgChatServerGetPendingNotificationCountResponse` | `12001` | - |
| `k_EMsgBaseSecretServer` | `12100` | - |
| `k_EMsgServerSecretChanged` | `12100` | - |
| `k_EMsgBaseWG` | `12200` | - |
| `k_EMsgWGConnectionProtocolError` | `12200` | - |
| `k_EMsgWGConnectionValidateUserToken` | `12201` | - |
| `k_EMsgWGConnectionValidateUserTokenResponse` | `12202` | - |
| `k_EMsgWGConnectionLegacyWGRequest` | `12203` | - |
| `k_EMsgWGConnectionLegacyWGResponse` | `12204` | - |



---

## 📋 EMsgClanAccountFlags

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `k_EMsgClanAccountFlagPublic` | `1` | - |
| `k_EMsgClanAccountFlagLarge` | `2` | - |
| `k_EMsgClanAccountFlagLocked` | `4` | - |
| `k_EMsgClanAccountFlagDisabled` | `8` | - |
| `k_EMsgClanAccountFlagOGG` | `16` | - |



---

## 📋 ENetworkDisconnectionReason

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `NETWORK_DISCONNECT_INVALID` | `0` | - |
| `NETWORK_DISCONNECT_SHUTDOWN` | `1` | - |
| `NETWORK_DISCONNECT_DISCONNECT_BY_USER` | `2` | - |
| `NETWORK_DISCONNECT_DISCONNECT_BY_SERVER` | `3` | - |
| `NETWORK_DISCONNECT_LOST` | `4` | - |
| `NETWORK_DISCONNECT_OVERFLOW` | `5` | - |
| `NETWORK_DISCONNECT_STEAM_BANNED` | `6` | - |
| `NETWORK_DISCONNECT_STEAM_INUSE` | `7` | - |
| `NETWORK_DISCONNECT_STEAM_TICKET` | `8` | - |
| `NETWORK_DISCONNECT_STEAM_LOGON` | `9` | - |
| `NETWORK_DISCONNECT_STEAM_AUTHCANCELLED` | `10` | - |
| `NETWORK_DISCONNECT_STEAM_AUTHALREADYUSED` | `11` | - |
| `NETWORK_DISCONNECT_STEAM_AUTHINVALID` | `12` | - |
| `NETWORK_DISCONNECT_STEAM_VACBANSTATE` | `13` | - |
| `NETWORK_DISCONNECT_STEAM_LOGGED_IN_ELSEWHERE` | `14` | - |
| `NETWORK_DISCONNECT_STEAM_VAC_CHECK_TIMEDOUT` | `15` | - |
| `NETWORK_DISCONNECT_STEAM_DROPPED` | `16` | - |
| `NETWORK_DISCONNECT_STEAM_OWNERSHIP` | `17` | - |
| `NETWORK_DISCONNECT_SERVERINFO_OVERFLOW` | `18` | - |
| `NETWORK_DISCONNECT_TICKMSG_OVERFLOW` | `19` | - |
| `NETWORK_DISCONNECT_STRINGTABLEMSG_OVERFLOW` | `20` | - |
| `NETWORK_DISCONNECT_DELTAENTMSG_OVERFLOW` | `21` | - |
| `NETWORK_DISCONNECT_TEMPENTMSG_OVERFLOW` | `22` | - |
| `NETWORK_DISCONNECT_SOUNDSMSG_OVERFLOW` | `23` | - |
| `NETWORK_DISCONNECT_SNAPSHOTOVERFLOW` | `24` | - |
| `NETWORK_DISCONNECT_SNAPSHOTERROR` | `25` | - |
| `NETWORK_DISCONNECT_RELIABLEOVERFLOW` | `26` | - |
| `NETWORK_DISCONNECT_BADDELTATICK` | `27` | - |
| `NETWORK_DISCONNECT_NOMORESPLITS` | `28` | - |
| `NETWORK_DISCONNECT_TIMEDOUT` | `29` | - |
| `NETWORK_DISCONNECT_DISCONNECTED` | `30` | - |
| `NETWORK_DISCONNECT_LEAVINGSPLIT` | `31` | - |
| `NETWORK_DISCONNECT_DIFFERENTCLASSTABLES` | `32` | - |
| `NETWORK_DISCONNECT_BADRELAYPASSWORD` | `33` | - |
| `NETWORK_DISCONNECT_BADSPECTATORPASSWORD` | `34` | - |
| `NETWORK_DISCONNECT_HLTVRESTRICTED` | `35` | - |
| `NETWORK_DISCONNECT_NOSPECTATORS` | `36` | - |
| `NETWORK_DISCONNECT_HLTVUNAVAILABLE` | `37` | - |
| `NETWORK_DISCONNECT_HLTVSTOP` | `38` | - |
| `NETWORK_DISCONNECT_KICKED` | `39` | - |
| `NETWORK_DISCONNECT_BANADDED` | `40` | - |
| `NETWORK_DISCONNECT_KICKBANADDED` | `41` | - |
| `NETWORK_DISCONNECT_HLTVDIRECT` | `42` | - |
| `NETWORK_DISCONNECT_PURESERVER_CLIENTEXTRA` | `43` | - |
| `NETWORK_DISCONNECT_PURESERVER_MISMATCH` | `44` | - |
| `NETWORK_DISCONNECT_USERCMD` | `45` | - |
| `NETWORK_DISCONNECT_REJECTED_BY_GAME` | `46` | - |
| `NETWORK_DISCONNECT_MESSAGE_PARSE_ERROR` | `47` | - |
| `NETWORK_DISCONNECT_INVALID_MESSAGE_ERROR` | `48` | - |
| `NETWORK_DISCONNECT_BAD_SERVER_PASSWORD` | `49` | - |
| `NETWORK_DISCONNECT_DIRECT_CONNECT_RESERVATION` | `50` | - |
| `NETWORK_DISCONNECT_CONNECTION_FAILURE` | `51` | - |
| `NETWORK_DISCONNECT_NO_PEER_GROUP_HANDLERS` | `52` | - |
| `NETWORK_DISCONNECT_RECONNECTION` | `53` | - |
| `NETWORK_DISCONNECT_LOOPSHUTDOWN` | `54` | - |
| `NETWORK_DISCONNECT_LOOPDEACTIVATE` | `55` | - |
| `NETWORK_DISCONNECT_HOST_ENDGAME` | `56` | - |
| `NETWORK_DISCONNECT_LOOP_LEVELLOAD_ACTIVATE` | `57` | - |
| `NETWORK_DISCONNECT_CREATE_SERVER_FAILED` | `58` | - |
| `NETWORK_DISCONNECT_EXITING` | `59` | - |
| `NETWORK_DISCONNECT_REQUEST_HOSTSTATE_IDLE` | `60` | - |
| `NETWORK_DISCONNECT_REQUEST_HOSTSTATE_HLTVRELAY` | `61` | - |
| `NETWORK_DISCONNECT_CLIENT_CONSISTENCY_FAIL` | `62` | - |
| `NETWORK_DISCONNECT_CLIENT_UNABLE_TO_CRC_MAP` | `63` | - |
| `NETWORK_DISCONNECT_CLIENT_NO_MAP` | `64` | - |
| `NETWORK_DISCONNECT_CLIENT_DIFFERENT_MAP` | `65` | - |
| `NETWORK_DISCONNECT_SERVER_REQUIRES_STEAM` | `66` | - |
| `NETWORK_DISCONNECT_STEAM_DENY_MISC` | `67` | - |
| `NETWORK_DISCONNECT_STEAM_DENY_BAD_ANTI_CHEAT` | `68` | - |
| `NETWORK_DISCONNECT_SERVER_SHUTDOWN` | `69` | - |
| `NETWORK_DISCONNECT_REPLAY_INCOMPATIBLE` | `71` | - |
| `NETWORK_DISCONNECT_CONNECT_REQUEST_TIMEDOUT` | `72` | - |
| `NETWORK_DISCONNECT_SERVER_INCOMPATIBLE` | `73` | - |
| `NETWORK_DISCONNECT_LOCALPROBLEM_MANYRELAYS` | `74` | - |
| `NETWORK_DISCONNECT_LOCALPROBLEM_HOSTEDSERVERPRIMARYRELAY` | `75` | - |
| `NETWORK_DISCONNECT_LOCALPROBLEM_NETWORKCONFIG` | `76` | - |
| `NETWORK_DISCONNECT_LOCALPROBLEM_OTHER` | `77` | - |
| `NETWORK_DISCONNECT_REMOTE_TIMEOUT` | `79` | - |
| `NETWORK_DISCONNECT_REMOTE_TIMEOUT_CONNECTING` | `80` | - |
| `NETWORK_DISCONNECT_REMOTE_OTHER` | `81` | - |
| `NETWORK_DISCONNECT_REMOTE_BADCRYPT` | `82` | - |
| `NETWORK_DISCONNECT_REMOTE_CERTNOTTRUSTED` | `83` | - |
| `NETWORK_DISCONNECT_UNUSUAL` | `84` | - |
| `NETWORK_DISCONNECT_INTERNAL_ERROR` | `85` | - |
| `NETWORK_DISCONNECT_REJECT_BADCHALLENGE` | `128` | - |
| `NETWORK_DISCONNECT_REJECT_NOLOBBY` | `129` | - |
| `NETWORK_DISCONNECT_REJECT_BACKGROUND_MAP` | `130` | - |
| `NETWORK_DISCONNECT_REJECT_SINGLE_PLAYER` | `131` | - |
| `NETWORK_DISCONNECT_REJECT_HIDDEN_GAME` | `132` | - |
| `NETWORK_DISCONNECT_REJECT_LANRESTRICT` | `133` | - |
| `NETWORK_DISCONNECT_REJECT_BADPASSWORD` | `134` | - |
| `NETWORK_DISCONNECT_REJECT_SERVERFULL` | `135` | - |
| `NETWORK_DISCONNECT_REJECT_INVALIDRESERVATION` | `136` | - |
| `NETWORK_DISCONNECT_REJECT_FAILEDCHANNEL` | `137` | - |
| `NETWORK_DISCONNECT_REJECT_CONNECT_FROM_LOBBY` | `138` | - |
| `NETWORK_DISCONNECT_REJECT_RESERVED_FOR_LOBBY` | `139` | - |
| `NETWORK_DISCONNECT_REJECT_INVALIDKEYLENGTH` | `140` | - |
| `NETWORK_DISCONNECT_REJECT_OLDPROTOCOL` | `141` | - |
| `NETWORK_DISCONNECT_REJECT_NEWPROTOCOL` | `142` | - |
| `NETWORK_DISCONNECT_REJECT_INVALIDCONNECTION` | `143` | - |
| `NETWORK_DISCONNECT_REJECT_INVALIDCERTLEN` | `144` | - |
| `NETWORK_DISCONNECT_REJECT_INVALIDSTEAMCERTLEN` | `145` | - |
| `NETWORK_DISCONNECT_REJECT_STEAM` | `146` | - |
| `NETWORK_DISCONNECT_REJECT_SERVERAUTHDISABLED` | `147` | - |
| `NETWORK_DISCONNECT_REJECT_SERVERCDKEYAUTHINVALID` | `148` | - |
| `NETWORK_DISCONNECT_REJECT_BANNED` | `149` | - |
| `NETWORK_DISCONNECT_KICKED_TEAMKILLING` | `150` | - |
| `NETWORK_DISCONNECT_KICKED_TK_START` | `151` | - |
| `NETWORK_DISCONNECT_KICKED_UNTRUSTEDACCOUNT` | `152` | - |
| `NETWORK_DISCONNECT_KICKED_CONVICTEDACCOUNT` | `153` | - |
| `NETWORK_DISCONNECT_KICKED_COMPETITIVECOOLDOWN` | `154` | - |
| `NETWORK_DISCONNECT_KICKED_TEAMHURTING` | `155` | - |
| `NETWORK_DISCONNECT_KICKED_HOSTAGEKILLING` | `156` | - |
| `NETWORK_DISCONNECT_KICKED_VOTEDOFF` | `157` | - |
| `NETWORK_DISCONNECT_KICKED_IDLE` | `158` | - |
| `NETWORK_DISCONNECT_KICKED_SUICIDE` | `159` | - |
| `NETWORK_DISCONNECT_KICKED_NOSTEAMLOGIN` | `160` | - |
| `NETWORK_DISCONNECT_KICKED_NOSTEAMTICKET` | `161` | - |
| `NETWORK_DISCONNECT_KICKED_INPUTAUTOMATION` | `162` | - |
| `NETWORK_DISCONNECT_KICKED_VACNETABNORMALBEHAVIOR` | `163` | - |
| `NETWORK_DISCONNECT_KICKED_INSECURECLIENT` | `164` | - |



---

## 📋 EProtoDebugVisiblity

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `k_EProtoDebugVisibility_Always` | `0` | - |
| `k_EProtoDebugVisibility_Server` | `70` | - |
| `k_EProtoDebugVisibility_ValveServer` | `80` | - |
| `k_EProtoDebugVisibility_GC` | `90` | - |
| `k_EProtoDebugVisibility_Never` | `100` | - |



---

## 📋 EQueryCvarValueStatus

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `eQueryCvarValueStatus_ValueIntact` | `0` | - |
| `eQueryCvarValueStatus_CvarNotFound` | `1` | - |
| `eQueryCvarValueStatus_NotACvar` | `2` | - |
| `eQueryCvarValueStatus_CvarProtected` | `3` | - |



---

## 📋 ESOMsg

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `k_ESOMsg_Create` | `21` | - |
| `k_ESOMsg_Update` | `22` | - |
| `k_ESOMsg_Destroy` | `23` | - |
| `k_ESOMsg_CacheSubscribed` | `24` | - |
| `k_ESOMsg_CacheUnsubscribed` | `25` | - |
| `k_ESOMsg_UpdateMultiple` | `26` | - |
| `k_ESOMsg_CacheSubscriptionCheck` | `27` | - |
| `k_ESOMsg_CacheSubscriptionRefresh` | `28` | - |



---

## 📋 ESplitScreenMessageType

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `MSG_SPLITSCREEN_ADDUSER` | `0` | - |
| `MSG_SPLITSCREEN_REMOVEUSER` | `1` | - |



---

## 📋 ESteamReviewScore

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `k_ESteamReviewScore_OverwhelminglyPositive` | `9` | - |
| `k_ESteamReviewScore_VeryPositive` | `8` | - |
| `k_ESteamReviewScore_Positive` | `7` | - |
| `k_ESteamReviewScore_MostlyPositive` | `6` | - |
| `k_ESteamReviewScore_Mixed` | `5` | - |
| `k_ESteamReviewScore_MostlyNegative` | `4` | - |
| `k_ESteamReviewScore_Negative` | `3` | - |
| `k_ESteamReviewScore_VeryNegative` | `2` | - |
| `k_ESteamReviewScore_OverwhelminglyNegative` | `1` | - |
| `k_ESteamReviewScore_None` | `0` | - |



---

## 📋 ETEProtobufIds

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `TE_EffectDispatchId` | `400` | - |
| `TE_ArmorRicochetId` | `401` | - |
| `TE_BeamEntPointId` | `402` | - |
| `TE_BeamEntsId` | `403` | - |
| `TE_BeamPointsId` | `404` | - |
| `TE_BeamRingId` | `405` | - |
| `TE_BubblesId` | `408` | - |
| `TE_BubbleTrailId` | `409` | - |
| `TE_DecalId` | `410` | - |
| `TE_WorldDecalId` | `411` | - |
| `TE_EnergySplashId` | `412` | - |
| `TE_FizzId` | `413` | - |
| `TE_ShatterSurfaceId` | `414` | - |
| `TE_GlowSpriteId` | `415` | - |
| `TE_ImpactId` | `416` | - |
| `TE_MuzzleFlashId` | `417` | - |
| `TE_BloodStreamId` | `418` | - |
| `TE_ExplosionId` | `419` | - |
| `TE_DustId` | `420` | - |
| `TE_LargeFunnelId` | `421` | - |
| `TE_SparksId` | `422` | - |
| `TE_PhysicsPropId` | `423` | - |
| `TE_SmokeId` | `426` | - |



---

## 📋 ETeam

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `ET_Unknown` | `0` | - |
| `ET_Spectator` | `1` | - |
| `ET_Terrorist` | `2` | - |
| `ET_CT` | `3` | - |



---

## 📋 EUnlockStyle

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `k_UnlockStyle_Succeeded` | `0` | - |
| `k_UnlockStyle_Failed_PreReq` | `1` | - |
| `k_UnlockStyle_Failed_CantAfford` | `2` | - |
| `k_UnlockStyle_Failed_CantCommit` | `3` | - |
| `k_UnlockStyle_Failed_CantLockCache` | `4` | - |
| `k_UnlockStyle_Failed_CantAffordAttrib` | `5` | - |



---

## 📋 EWeaponType

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `EWT_Knife` | `0` | - |
| `EWT_Pistol` | `1` | - |
| `EWT_SubMachineGun` | `2` | - |
| `EWT_Rifle` | `3` | - |
| `EWT_Shotgun` | `4` | - |
| `EWT_SniperRifle` | `5` | - |
| `EWT_MachineGun` | `6` | - |
| `EWT_C4` | `7` | - |
| `EWT_Grenade` | `8` | - |
| `EWT_Equipment` | `9` | - |
| `EWT_StackableItem` | `10` | - |
| `EWT_Unknown` | `11` | - |



---

## 📋 GCClientLauncherType

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `GCClientLauncherType_DEFAULT` | `0` | - |
| `GCClientLauncherType_PERFECTWORLD` | `1` | - |
| `GCClientLauncherType_STEAMCHINA` | `2` | - |
| `GCClientLauncherType_SOURCE2` | `3` | - |



---

## 📋 GCConnectionStatus

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `GCConnectionStatus_HAVE_SESSION` | `0` | - |
| `GCConnectionStatus_GC_GOING_DOWN` | `1` | - |
| `GCConnectionStatus_NO_SESSION` | `2` | - |
| `GCConnectionStatus_NO_SESSION_IN_LOGON_QUEUE` | `3` | - |
| `GCConnectionStatus_NO_STEAM` | `4` | - |



---

## 📋 GCProtoBufMsgSrc

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `GCProtoBufMsgSrc_Unspecified` | `0` | - |
| `GCProtoBufMsgSrc_FromSystem` | `1` | - |
| `GCProtoBufMsgSrc_FromSteamID` | `2` | - |
| `GCProtoBufMsgSrc_FromGC` | `3` | - |
| `GCProtoBufMsgSrc_ReplySystem` | `4` | - |



---

## 📋 GC_BannedWordType

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `GC_BANNED_WORD_DISABLE_WORD` | `0` | - |
| `GC_BANNED_WORD_ENABLE_WORD` | `1` | - |



---

## 🔌 GameServerPing

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<GameServerPing\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Ping` | `int` | get, set | - |
| `Ip` | `uint` | get, set | - |
| `Instances` | `uint` | get, set | - |



---

## 🔌 GlobalStatistics

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<GlobalStatistics\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PlayersOnline` | `uint` | get, set | - |
| `ServersOnline` | `uint` | get, set | - |
| `PlayersSearching` | `uint` | get, set | - |
| `ServersAvailable` | `uint` | get, set | - |
| `OngoingMatches` | `uint` | get, set | - |
| `SearchTimeAvg` | `uint` | get, set | - |
| `SearchStatistics` | `IProtobufRepeatedFieldSubMessageType\<DetailedSearchStatistic\>` | get | - |
| `MainPostUrl` | `string` | get, set | - |
| `RequiredAppidVersion` | `uint` | get, set | - |
| `PricesheetVersion` | `uint` | get, set | - |
| `TwitchStreamsVersion` | `uint` | get, set | - |
| `ActiveTournamentEventid` | `uint` | get, set | - |
| `ActiveSurveyId` | `uint` | get, set | - |
| `Rtime32Cur` | `uint` | get, set | - |
| `RequiredAppidVersion2` | `uint` | get, set | - |



---

## 🔌 IpAddressMask

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<IpAddressMask\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `A` | `uint` | get, set | - |
| `B` | `uint` | get, set | - |
| `C` | `uint` | get, set | - |
| `D` | `uint` | get, set | - |
| `Bits` | `uint` | get, set | - |
| `Token` | `uint` | get, set | - |



---

## 🔌 MLDemoHeader

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<MLDemoHeader\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MapName` | `string` | get, set | - |
| `TickRate` | `int` | get, set | - |
| `Version` | `uint` | get, set | - |
| `SteamUniverse` | `uint` | get, set | - |



---

## 🔌 MLDict

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<MLDict\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Key` | `string` | get, set | - |
| `ValString` | `string` | get, set | - |
| `ValInt` | `int` | get, set | - |
| `ValFloat` | `float` | get, set | - |



---

## 🔌 MLEvent

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<MLEvent\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EventName` | `string` | get, set | - |
| `Data` | `IProtobufRepeatedFieldSubMessageType\<MLDict\>` | get | - |



---

## 🔌 MLGameState

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<MLGameState\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Match` | `MLMatchState` | get | - |
| `Round` | `MLRoundState` | get | - |
| `Players` | `IProtobufRepeatedFieldSubMessageType\<MLPlayerState\>` | get | - |



---

## 🔌 MLMatchState

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<MLMatchState\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `GameMode` | `string` | get, set | - |
| `Phase` | `string` | get, set | - |
| `Round` | `int` | get, set | - |
| `ScoreCt` | `int` | get, set | - |
| `ScoreT` | `int` | get, set | - |



---

## 🔌 MLPlayerState

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<MLPlayerState\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AccountId` | `int` | get, set | - |
| `PlayerSlot` | `int` | get, set | - |
| `Entindex` | `int` | get, set | - |
| `Name` | `string` | get, set | - |
| `Clan` | `string` | get, set | - |
| `Team` | `ETeam` | get, set | - |
| `Abspos` | `Vector` | get, set | - |
| `Eyeangle` | `QAngle` | get, set | - |
| `EyeangleFwd` | `Vector` | get, set | - |
| `Health` | `int` | get, set | - |
| `Armor` | `int` | get, set | - |
| `Flashed` | `float` | get, set | - |
| `Smoked` | `float` | get, set | - |
| `Money` | `int` | get, set | - |
| `RoundKills` | `int` | get, set | - |
| `RoundKillhs` | `int` | get, set | - |
| `Burning` | `float` | get, set | - |
| `Helmet` | `bool` | get, set | - |
| `DefuseKit` | `bool` | get, set | - |
| `Weapons` | `IProtobufRepeatedFieldSubMessageType\<MLWeaponState\>` | get | - |



---

## 🔌 MLRoundState

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<MLRoundState\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Phase` | `string` | get, set | - |
| `WinTeam` | `ETeam` | get, set | - |
| `BombState` | `string` | get, set | - |



---

## 🔌 MLTick

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<MLTick\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TickCount` | `int` | get, set | - |
| `State` | `MLGameState` | get | - |
| `Events` | `IProtobufRepeatedFieldSubMessageType\<MLEvent\>` | get | - |



---

## 🔌 MLWeaponState

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<MLWeaponState\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Index` | `int` | get, set | - |
| `Name` | `string` | get, set | - |
| `Type` | `EWeaponType` | get, set | - |
| `AmmoClip` | `int` | get, set | - |
| `AmmoClipMax` | `int` | get, set | - |
| `AmmoReserve` | `int` | get, set | - |
| `State` | `string` | get, set | - |
| `RecoilIndex` | `float` | get, set | - |



---

## 🔌 MatchEndItemUpdates

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<MatchEndItemUpdates\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ItemId` | `ulong` | get, set | - |
| `ItemAttrDefidx` | `uint` | get, set | - |
| `ItemAttrDeltaValue` | `uint` | get, set | - |



---

## 📋 NET_Messages

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `net_NOP` | `0` | - |
| `net_Disconnect_Legacy` | `1` | - |
| `net_SplitScreenUser` | `3` | - |
| `net_Tick` | `4` | - |
| `net_StringCmd` | `5` | - |
| `net_SetConVar` | `6` | - |
| `net_SignonState` | `7` | - |
| `net_SpawnGroup_Load` | `8` | - |
| `net_SpawnGroup_ManifestUpdate` | `9` | - |
| `net_SpawnGroup_SetCreationTick` | `11` | - |
| `net_SpawnGroup_Unload` | `12` | - |
| `net_SpawnGroup_LoadCompleted` | `13` | - |
| `net_DebugOverlay` | `15` | - |



---

## 🔌 NetMessageConnectionClosed

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<NetMessageConnectionClosed\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Reason` | `uint` | get, set | - |
| `Message` | `string` | get, set | - |



---

## 🔌 NetMessageConnectionCrashed

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<NetMessageConnectionCrashed\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Reason` | `uint` | get, set | - |
| `Message` | `string` | get, set | - |



---

## 🔌 NetMessagePacketEnd

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<NetMessagePacketEnd\>`



---

## 🔌 NetMessagePacketStart

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<NetMessagePacketStart\>`



---

## 🔌 NetMessageSplitscreenUserChanged

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<NetMessageSplitscreenUserChanged\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Slot` | `uint` | get, set | - |



---

## 🔌 OperationalStatisticDescription

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<OperationalStatisticDescription\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | get, set | - |
| `Idkey` | `uint` | get, set | - |



---

## 🔌 OperationalStatisticElement

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<OperationalStatisticElement\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Idkey` | `uint` | get, set | - |
| `Values` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |



---

## 🔌 OperationalStatisticsPacket

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<OperationalStatisticsPacket\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Packetid` | `int` | get, set | - |
| `Mstimestamp` | `int` | get, set | - |
| `Values` | `IProtobufRepeatedFieldSubMessageType\<OperationalStatisticElement\>` | get | - |



---

## 🔌 OperationalVarValue

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<OperationalVarValue\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Name` | `string` | get, set | - |
| `Ivalue` | `int` | get, set | - |
| `Fvalue` | `float` | get, set | - |
| `Svalue` | `byte[]` | get, set | - |



---

## 📋 P2P_Messages

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `p2p_TextMessage` | `256` | - |
| `p2p_Voice` | `257` | - |
| `p2p_Ping` | `258` | - |
| `p2p_VRAvatarPosition` | `259` | - |
| `p2p_WatchSynchronization` | `260` | - |
| `p2p_FightingGame_GameData` | `261` | - |
| `p2p_FightingGame_Connection` | `262` | - |



---

## 📋 PARTICLE_MESSAGE

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `GAME_PARTICLE_MANAGER_EVENT_CREATE` | `0` | - |
| `GAME_PARTICLE_MANAGER_EVENT_UPDATE` | `1` | - |
| `GAME_PARTICLE_MANAGER_EVENT_UPDATE_FORWARD` | `2` | - |
| `GAME_PARTICLE_MANAGER_EVENT_UPDATE_ORIENTATION` | `3` | - |
| `GAME_PARTICLE_MANAGER_EVENT_UPDATE_FALLBACK` | `4` | - |
| `GAME_PARTICLE_MANAGER_EVENT_UPDATE_ENT` | `5` | - |
| `GAME_PARTICLE_MANAGER_EVENT_UPDATE_OFFSET` | `6` | - |
| `GAME_PARTICLE_MANAGER_EVENT_DESTROY` | `7` | - |
| `GAME_PARTICLE_MANAGER_EVENT_DESTROY_INVOLVING` | `8` | - |
| `GAME_PARTICLE_MANAGER_EVENT_RELEASE` | `9` | - |
| `GAME_PARTICLE_MANAGER_EVENT_LATENCY` | `10` | - |
| `GAME_PARTICLE_MANAGER_EVENT_SHOULD_DRAW` | `11` | - |
| `GAME_PARTICLE_MANAGER_EVENT_FROZEN` | `12` | - |
| `GAME_PARTICLE_MANAGER_EVENT_CHANGE_CONTROL_POINT_ATTACHMENT` | `13` | - |
| `GAME_PARTICLE_MANAGER_EVENT_UPDATE_ENTITY_POSITION` | `14` | - |
| `GAME_PARTICLE_MANAGER_EVENT_SET_FOW_PROPERTIES` | `15` | - |
| `GAME_PARTICLE_MANAGER_EVENT_SET_TEXT` | `16` | - |
| `GAME_PARTICLE_MANAGER_EVENT_SET_SHOULD_CHECK_FOW` | `17` | - |
| `GAME_PARTICLE_MANAGER_EVENT_SET_CONTROL_POINT_MODEL` | `18` | - |
| `GAME_PARTICLE_MANAGER_EVENT_SET_CONTROL_POINT_SNAPSHOT` | `19` | - |
| `GAME_PARTICLE_MANAGER_EVENT_SET_TEXTURE_ATTRIBUTE` | `20` | - |
| `GAME_PARTICLE_MANAGER_EVENT_SET_SCENE_OBJECT_GENERIC_FLAG` | `21` | - |
| `GAME_PARTICLE_MANAGER_EVENT_SET_SCENE_OBJECT_TINT_AND_DESAT` | `22` | - |
| `GAME_PARTICLE_MANAGER_EVENT_DESTROY_NAMED` | `23` | - |
| `GAME_PARTICLE_MANAGER_EVENT_SKIP_TO_TIME` | `24` | - |
| `GAME_PARTICLE_MANAGER_EVENT_CAN_FREEZE` | `25` | - |
| `GAME_PARTICLE_MANAGER_EVENT_SET_NAMED_VALUE_CONTEXT` | `26` | - |
| `GAME_PARTICLE_MANAGER_EVENT_UPDATE_TRANSFORM` | `27` | - |
| `GAME_PARTICLE_MANAGER_EVENT_FREEZE_TRANSITION_OVERRIDE` | `28` | - |
| `GAME_PARTICLE_MANAGER_EVENT_FREEZE_INVOLVING` | `29` | - |
| `GAME_PARTICLE_MANAGER_EVENT_ADD_MODELLIST_OVERRIDE_ELEMENT` | `30` | - |
| `GAME_PARTICLE_MANAGER_EVENT_CLEAR_MODELLIST_OVERRIDE` | `31` | - |
| `GAME_PARTICLE_MANAGER_EVENT_CREATE_PHYSICS_SIM` | `32` | - |
| `GAME_PARTICLE_MANAGER_EVENT_DESTROY_PHYSICS_SIM` | `33` | - |
| `GAME_PARTICLE_MANAGER_EVENT_SET_VDATA` | `34` | - |
| `GAME_PARTICLE_MANAGER_EVENT_SET_MATERIAL_OVERRIDE` | `35` | - |
| `GAME_PARTICLE_MANAGER_EVENT_ADD_FAN` | `36` | - |
| `GAME_PARTICLE_MANAGER_EVENT_UPDATE_FAN` | `37` | - |
| `GAME_PARTICLE_MANAGER_EVENT_SET_CLUSTER_GROWTH` | `38` | - |
| `GAME_PARTICLE_MANAGER_EVENT_REMOVE_FAN` | `39` | - |



---

## 🔌 PlayerCommendationInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<PlayerCommendationInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `CmdFriendly` | `uint` | get, set | - |
| `CmdTeaching` | `uint` | get, set | - |
| `CmdLeader` | `uint` | get, set | - |



---

## 🔌 PlayerDecalDigitalSignature

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<PlayerDecalDigitalSignature\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Signature` | `byte[]` | get, set | - |
| `Accountid` | `uint` | get, set | - |
| `Rtime` | `uint` | get, set | - |
| `Endpos` | `IProtobufRepeatedFieldValueType\<float\>` | get | - |
| `Startpos` | `IProtobufRepeatedFieldValueType\<float\>` | get | - |
| `Left` | `IProtobufRepeatedFieldValueType\<float\>` | get | - |
| `TxDefidx` | `uint` | get, set | - |
| `Entindex` | `int` | get, set | - |
| `Hitbox` | `uint` | get, set | - |
| `Creationtime` | `float` | get, set | - |
| `Equipslot` | `uint` | get, set | - |
| `TraceId` | `uint` | get, set | - |
| `Normal` | `IProtobufRepeatedFieldValueType\<float\>` | get | - |
| `TintId` | `uint` | get, set | - |



---

## 🔌 PlayerMedalsInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<PlayerMedalsInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `DisplayItemsDefidx` | `IProtobufRepeatedFieldValueType\<uint\>` | get | - |
| `FeaturedDisplayItemDefidx` | `uint` | get, set | - |



---

## 🔌 PlayerQuestData

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<PlayerQuestData\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `QuesterAccountId` | `uint` | get, set | - |
| `QuestItemData` | `IProtobufRepeatedFieldSubMessageType\<PlayerQuestData_QuestItemData\>` | get | - |
| `XpProgressData` | `IProtobufRepeatedFieldSubMessageType\<XpProgressData\>` | get | - |
| `TimePlayed` | `uint` | get, set | - |
| `MmGameMode` | `uint` | get, set | - |
| `ItemUpdates` | `IProtobufRepeatedFieldSubMessageType\<MatchEndItemUpdates\>` | get | - |
| `OperationPointsEligible` | `bool` | get, set | - |
| `Userstatchanges` | `IProtobufRepeatedFieldSubMessageType\<CMsgCsgoSteamUserStatChange\>` | get | - |



---

## 🔌 PlayerQuestData_QuestItemData

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<PlayerQuestData_QuestItemData\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `QuestId` | `ulong` | get, set | - |
| `QuestNormalPointsEarned` | `int` | get, set | - |
| `QuestBonusPointsEarned` | `int` | get, set | - |
| `QuestNormalPointsRequired` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `QuestRewardXp` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |
| `QuestPeriod` | `int` | get, set | - |
| `QuestType` | `QuestType` | get, set | - |



---

## 🔌 PlayerRankingInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<PlayerRankingInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AccountId` | `uint` | get, set | - |
| `RankId` | `uint` | get, set | - |
| `Wins` | `uint` | get, set | - |
| `RankChange` | `float` | get, set | - |
| `RankTypeId` | `uint` | get, set | - |
| `TvControl` | `uint` | get, set | - |
| `RankWindowStats` | `ulong` | get, set | - |
| `LeaderboardName` | `string` | get, set | - |
| `RankIfWin` | `uint` | get, set | - |
| `RankIfLose` | `uint` | get, set | - |
| `RankIfTie` | `uint` | get, set | - |
| `PerMapRank` | `IProtobufRepeatedFieldSubMessageType\<PlayerRankingInfo_PerMapRank\>` | get | - |
| `LeaderboardNameStatus` | `uint` | get, set | - |
| `HighestRank` | `uint` | get, set | - |
| `RankExpiry` | `uint` | get, set | - |



---

## 🔌 PlayerRankingInfo_PerMapRank

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<PlayerRankingInfo_PerMapRank\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `MapId` | `uint` | get, set | - |
| `RankId` | `uint` | get, set | - |
| `Wins` | `uint` | get, set | - |



---

## 📋 PrefetchType

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `PFT_SOUND` | `0` | - |



---

## 🔌 ProtoFlattenedSerializerField_t

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<ProtoFlattenedSerializerField_t\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `VarTypeSym` | `int` | get, set | - |
| `VarNameSym` | `int` | get, set | - |
| `BitCount` | `int` | get, set | - |
| `LowValue` | `float` | get, set | - |
| `HighValue` | `float` | get, set | - |
| `EncodeFlags` | `int` | get, set | - |
| `FieldSerializerNameSym` | `int` | get, set | - |
| `FieldSerializerVersion` | `int` | get, set | - |
| `SendNodeSym` | `int` | get, set | - |
| `VarEncoderSym` | `int` | get, set | - |
| `PolymorphicTypes` | `IProtobufRepeatedFieldSubMessageType\<ProtoFlattenedSerializerField_t_polymorphic_field_t\>` | get | - |
| `VarSerializerSym` | `int` | get, set | - |



---

## 🔌 ProtoFlattenedSerializerField_t_polymorphic_field_t

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<ProtoFlattenedSerializerField_t_polymorphic_field_t\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `PolymorphicFieldSerializerNameSym` | `int` | get, set | - |
| `PolymorphicFieldSerializerVersion` | `int` | get, set | - |



---

## 🔌 ProtoFlattenedSerializer_t

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<ProtoFlattenedSerializer_t\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SerializerNameSym` | `int` | get, set | - |
| `SerializerVersion` | `int` | get, set | - |
| `FieldsIndex` | `IProtobufRepeatedFieldValueType\<int\>` | get | - |



---

## 📋 QuestType

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `k_EQuestType_Operation` | `1` | - |
| `k_EQuestType_RecurringMission` | `2` | - |



---

## 📋 ReplayEventType_t

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `REPLAY_EVENT_CANCEL` | `0` | - |
| `REPLAY_EVENT_DEATH` | `1` | - |
| `REPLAY_EVENT_GENERIC` | `2` | - |
| `REPLAY_EVENT_STUCK_NEED_FULL_UPDATE` | `3` | - |
| `REPLAY_EVENT_VICTORY` | `4` | - |



---

## 📋 RequestPause_t

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `RP_PAUSE` | `0` | - |
| `RP_UNPAUSE` | `1` | - |
| `RP_TOGGLEPAUSE` | `2` | - |



---

## 📋 SVC_Messages

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `svc_ServerInfo` | `40` | - |
| `svc_FlattenedSerializer` | `41` | - |
| `svc_ClassInfo` | `42` | - |
| `svc_SetPause` | `43` | - |
| `svc_CreateStringTable` | `44` | - |
| `svc_UpdateStringTable` | `45` | - |
| `svc_VoiceInit` | `46` | - |
| `svc_VoiceData` | `47` | - |
| `svc_Print` | `48` | - |
| `svc_Sounds` | `49` | - |
| `svc_SetView` | `50` | - |
| `svc_ClearAllStringTables` | `51` | - |
| `svc_CmdKeyValues` | `52` | - |
| `svc_BSPDecal` | `53` | - |
| `svc_SplitScreen` | `54` | - |
| `svc_PacketEntities` | `55` | - |
| `svc_Prefetch` | `56` | - |
| `svc_Menu` | `57` | - |
| `svc_GetCvarValue` | `58` | - |
| `svc_StopSound` | `59` | - |
| `svc_PeerList` | `60` | - |
| `svc_PacketReliable` | `61` | - |
| `svc_HLTVStatus` | `62` | - |
| `svc_ServerSteamID` | `63` | - |
| `svc_FullFrameSplit` | `70` | - |
| `svc_RconServerDetails` | `71` | - |
| `svc_UserMessage` | `72` | - |
| `svc_Broadcast_Command` | `74` | - |
| `svc_HltvFixupOperatorStatus` | `75` | - |
| `svc_UserCmds` | `76` | - |
| `svc_NextMsgPredicted` | `77` | - |



---

## 📋 SVC_Messages_LowFrequency

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `svc_dummy` | `600` | - |



---

## 🔌 ScoreLeaderboardData

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<ScoreLeaderboardData\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `QuestId` | `ulong` | get, set | - |
| `Score` | `uint` | get, set | - |
| `Accountentries` | `IProtobufRepeatedFieldSubMessageType\<ScoreLeaderboardData_AccountEntries\>` | get | - |
| `Matchentries` | `IProtobufRepeatedFieldSubMessageType\<ScoreLeaderboardData_Entry\>` | get | - |
| `LeaderboardName` | `string` | get, set | - |



---

## 🔌 ScoreLeaderboardData_AccountEntries

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<ScoreLeaderboardData_AccountEntries\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Accountid` | `uint` | get, set | - |
| `Entries` | `IProtobufRepeatedFieldSubMessageType\<ScoreLeaderboardData_Entry\>` | get | - |



---

## 🔌 ScoreLeaderboardData_Entry

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<ScoreLeaderboardData_Entry\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Tag` | `uint` | get, set | - |
| `Val` | `uint` | get, set | - |



---

## 🔌 ServerHltvInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<ServerHltvInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TvUdpPort` | `uint` | get, set | - |
| `TvWatchKey` | `ulong` | get, set | - |
| `TvSlots` | `uint` | get, set | - |
| `TvClients` | `uint` | get, set | - |
| `TvProxies` | `uint` | get, set | - |
| `TvTime` | `uint` | get, set | - |
| `GameType` | `uint` | get, set | - |
| `GameMapgroup` | `string` | get, set | - |
| `GameMap` | `string` | get, set | - |
| `TvMasterSteamid` | `ulong` | get, set | - |
| `TvLocalSlots` | `uint` | get, set | - |
| `TvLocalClients` | `uint` | get, set | - |
| `TvLocalProxies` | `uint` | get, set | - |
| `TvRelaySlots` | `uint` | get, set | - |
| `TvRelayClients` | `uint` | get, set | - |
| `TvRelayProxies` | `uint` | get, set | - |
| `TvRelayAddress` | `uint` | get, set | - |
| `TvRelayPort` | `uint` | get, set | - |
| `TvRelaySteamid` | `ulong` | get, set | - |
| `Flags` | `uint` | get, set | - |



---

## 📋 SignonState_t

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `SIGNONSTATE_NONE` | `0` | - |
| `SIGNONSTATE_CHALLENGE` | `1` | - |
| `SIGNONSTATE_CONNECTED` | `2` | - |
| `SIGNONSTATE_NEW` | `3` | - |
| `SIGNONSTATE_PRESPAWN` | `4` | - |
| `SIGNONSTATE_SPAWN` | `5` | - |
| `SIGNONSTATE_FULL` | `6` | - |
| `SIGNONSTATE_CHANGELEVEL` | `7` | - |



---

## 📋 SpawnGroupFlags_t

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `SPAWN_GROUP_LOAD_ENTITIES_FROM_SAVE` | `1` | - |
| `SPAWN_GROUP_DONT_SPAWN_ENTITIES` | `2` | - |
| `SPAWN_GROUP_SYNCHRONOUS_SPAWN` | `4` | - |
| `SPAWN_GROUP_IS_INITIAL_SPAWN_GROUP` | `8` | - |
| `SPAWN_GROUP_CREATE_CLIENT_ONLY_ENTITIES` | `16` | - |
| `SPAWN_GROUP_BLOCK_UNTIL_LOADED` | `64` | - |
| `SPAWN_GROUP_LOAD_STREAMING_DATA` | `128` | - |
| `SPAWN_GROUP_CREATE_NEW_SCENE_WORLD` | `256` | - |



---

## 🔌 TournamentEvent

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<TournamentEvent\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EventId` | `int` | get, set | - |
| `EventTag` | `string` | get, set | - |
| `EventName` | `string` | get, set | - |
| `EventTimeStart` | `uint` | get, set | - |
| `EventTimeEnd` | `uint` | get, set | - |
| `EventPublic` | `int` | get, set | - |
| `EventStageId` | `int` | get, set | - |
| `EventStageName` | `string` | get, set | - |
| `ActiveSectionId` | `uint` | get, set | - |



---

## 🔌 TournamentMatchSetup

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<TournamentMatchSetup\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `EventId` | `int` | get, set | - |
| `TeamIdCt` | `int` | get, set | - |
| `TeamIdT` | `int` | get, set | - |
| `EventStageId` | `int` | get, set | - |



---

## 🔌 TournamentPlayer

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<TournamentPlayer\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `AccountId` | `uint` | get, set | - |
| `PlayerNick` | `string` | get, set | - |
| `PlayerName` | `string` | get, set | - |
| `PlayerDob` | `uint` | get, set | - |
| `PlayerFlag` | `string` | get, set | - |
| `PlayerLocation` | `string` | get, set | - |
| `PlayerDesc` | `string` | get, set | - |



---

## 🔌 TournamentTeam

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<TournamentTeam\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `TeamId` | `int` | get, set | - |
| `TeamTag` | `string` | get, set | - |
| `TeamFlag` | `string` | get, set | - |
| `TeamName` | `string` | get, set | - |
| `Players` | `IProtobufRepeatedFieldSubMessageType\<TournamentPlayer\>` | get | - |



---

## 🔌 VacNetShot

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<VacNetShot\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SteamidPlayer` | `ulong` | get, set | - |
| `RoundNumber` | `int` | get, set | - |
| `HitType` | `int` | get, set | - |
| `WeaponType` | `int` | get, set | - |
| `DistanceToHurtTarget` | `float` | get, set | - |
| `DeltaYawWindow` | `IProtobufRepeatedFieldValueType\<float\>` | get | - |
| `DeltaPitchWindow` | `IProtobufRepeatedFieldValueType\<float\>` | get | - |



---

## 📋 VoiceDataFormat_t

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `VOICEDATA_FORMAT_STEAM` | `0` | - |
| `VOICEDATA_FORMAT_ENGINE` | `1` | - |
| `VOICEDATA_FORMAT_OPUS` | `2` | - |



---

## 🔌 WatchableMatchInfo

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<WatchableMatchInfo\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ServerIp` | `uint` | get, set | - |
| `TvPort` | `uint` | get, set | - |
| `TvSpectators` | `uint` | get, set | - |
| `TvTime` | `uint` | get, set | - |
| `TvWatchPassword` | `byte[]` | get, set | - |
| `ClDecryptdataKey` | `ulong` | get, set | - |
| `ClDecryptdataKeyPub` | `ulong` | get, set | - |
| `GameType` | `uint` | get, set | - |
| `GameMapgroup` | `string` | get, set | - |
| `GameMap` | `string` | get, set | - |
| `ServerId` | `ulong` | get, set | - |
| `MatchId` | `ulong` | get, set | - |
| `ReservationId` | `ulong` | get, set | - |



---

## 🔌 XpProgressData

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<XpProgressData\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `XpPoints` | `uint` | get, set | - |
| `XpCategory` | `int` | get, set | - |



---

## 📋 eRollType

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `enum`

### 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `ROLL_NONE` | `-1` | - |
| `ROLL_STATS` | `0` | - |
| `ROLL_CREDITS` | `1` | - |
| `ROLL_LATE_JOIN_LOGO` | `2` | - |
| `ROLL_OUTTRO` | `3` | - |



---

