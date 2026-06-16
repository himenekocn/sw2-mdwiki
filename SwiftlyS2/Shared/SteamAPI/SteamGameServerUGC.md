<a id="steamgameserverugc"></a>

# 📦 SteamGameServerUGC

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### CreateQueryUserUGCRequest (静态)

```csharp
UGCQueryHandle_t CreateQueryUserUGCRequest(AccountID_t unAccountID, EUserUGCList eListType, EUGCMatchingUGCType eMatchingUGCType, EUserUGCListSortOrder eSortOrder, AppId_t nCreatorAppID, AppId_t nConsumerAppID, uint unPage)
```

<para> 查询与用户关联的UGC。创建者应用ID或消费者应用ID必须有效，并设置为当前运行的应用。unPage应从1开始。</para>

**参数:**

- `unAccountID` (`AccountID_t`)
- `eListType` (`EUserUGCList`)
- `eMatchingUGCType` (`EUGCMatchingUGCType`)
- `eSortOrder` (`EUserUGCListSortOrder`)
- `nCreatorAppID` (`AppId_t`)
- `nConsumerAppID` (`AppId_t`)
- `unPage` (`uint`)

**返回值:** `UGCQueryHandle_t`

**用法示例:**
```csharp
var queryHandle = SteamGameServerUGC.CreateQueryUserUGCRequest(new AccountID_t(123), EUserUGCList.Published, EUGCMatchingUGCType.Items, EUserUGCListSortOrder.CreatedDesc, new AppId_t(480), new AppId_t(480), 1);
```

### CreateQueryAllUGCRequest (静态)

```csharp
UGCQueryHandle_t CreateQueryAllUGCRequest(EUGCQuery eQueryType, EUGCMatchingUGCType eMatchingeMatchingUGCTypeFileType, AppId_t nCreatorAppID, AppId_t nConsumerAppID, uint unPage)
```

<para> 查询所有匹配的用户生成内容（UGC）。创建者应用ID或消费者应用ID必须有效且设置为当前运行的应用。unPage应从1开始。</para>

**参数:**

- `eQueryType` (`EUGCQuery`)
- `eMatchingeMatchingUGCTypeFileType` (`EUGCMatchingUGCType`)
- `nCreatorAppID` (`AppId_t`)
- `nConsumerAppID` (`AppId_t`)
- `unPage` (`uint`)

**返回值:** `UGCQueryHandle_t`

**用法示例:**
```csharp
var queryHandle = SteamGameServerUGC.CreateQueryAllUGCRequest(EUGCQuery.k_EUGCQuery_RankedByVote, EUGCMatchingUGCType.k_EUGCMatchingUGCType_Items, new AppId_t(480), new AppId_t(480), 1);
```

### CreateQueryAllUGCRequest (静态)

```csharp
UGCQueryHandle_t CreateQueryAllUGCRequest(EUGCQuery eQueryType, EUGCMatchingUGCType eMatchingeMatchingUGCTypeFileType, AppId_t nCreatorAppID, AppId_t nConsumerAppID, string pchCursor = null)
```

<para> 使用新的深度分页接口查询所有匹配的用户生成内容(UGC)。创建者应用ID或消费者应用ID必须有效且设置为当前运行的应用。pchCursor应设置为NULL或"*"以获取第一组结果。</para>

**参数:**

- `eQueryType` (`EUGCQuery`)
- `eMatchingeMatchingUGCTypeFileType` (`EUGCMatchingUGCType`)
- `nCreatorAppID` (`AppId_t`)
- `nConsumerAppID` (`AppId_t`)
- `pchCursor` (`string`) = `null`

**返回值:** `UGCQueryHandle_t`

**用法示例:**
```csharp
var queryHandle = SteamGameServerUGC.CreateQueryAllUGCRequest(EUGCQuery.k_EUGCQuery_RankedByVote, EUGCMatchingUGCType.k_EUGCMatchingUGCType_Items, new AppId_t(480), new AppId_t(480), "*");
```

### CreateQueryUGCDetailsRequest (静态)

```csharp
UGCQueryHandle_t CreateQueryUGCDetailsRequest(PublishedFileId_t[] pvecPublishedFileID, uint unNumPublishedFileIDs)
```

<para> 查询指定已发布文件ID的详细信息（RequestUGCDetails调用已被弃用，由本调用替代）</para>

**参数:**

- `pvecPublishedFileID` (`PublishedFileId_t[]`)
- `unNumPublishedFileIDs` (`uint`)

**返回值:** `UGCQueryHandle_t`

**用法示例:**
```csharp
var publishedFileIds = new PublishedFileId_t[] { new PublishedFileId_t(123456) };
var queryHandle = SteamGameServerUGC.CreateQueryUGCDetailsRequest(publishedFileIds, 1);
```

### SendQueryUGCRequest (静态)

```csharp
SteamAPICall_t SendQueryUGCRequest(UGCQueryHandle_t handle)
```

<para>向Steam发送查询</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
var apiCall = SteamGameServerUGC.SendQueryUGCRequest(queryHandle);
```

### GetQueryUGCResult (静态)

```csharp
bool GetQueryUGCResult(UGCQueryHandle_t handle, uint index, out SteamUGCDetails_t pDetails)
```

<para> 在收到查询UGC的回调后，检索单个结果</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)
- `pDetails` (`out SteamUGCDetails_t`)

**返回值:** `bool`

**用法示例:**
```csharp
UGCQueryHandle_t handle = default;
SteamUGCDetails_t details;
bool success = SteamGameServerUGC.GetQueryUGCResult(handle, 0, out details);
```

### GetQueryUGCNumTags (静态)

```csharp
uint GetQueryUGCNumTags(UGCQueryHandle_t handle, uint index)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)

**返回值:** `uint`

**用法示例:**
```csharp
UGCQueryHandle_t handle = default;
uint tagCount = SteamGameServerUGC.GetQueryUGCNumTags(handle, 0);
```

### GetQueryUGCTag (静态)

```csharp
bool GetQueryUGCTag(UGCQueryHandle_t handle, uint index, uint indexTag, out string pchValue, uint cchValueSize)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)
- `indexTag` (`uint`)
- `pchValue` (`out string`)
- `cchValueSize` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
UGCQueryHandle_t handle = default; string tagValue; bool success = SteamGameServerUGC.GetQueryUGCTag(handle, 0, 0, out tagValue, 256);
```

### GetQueryUGCTagDisplayName (静态)

```csharp
bool GetQueryUGCTagDisplayName(UGCQueryHandle_t handle, uint index, uint indexTag, out string pchValue, uint cchValueSize)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)
- `indexTag` (`uint`)
- `pchValue` (`out string`)
- `cchValueSize` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUGC.GetQueryUGCTagDisplayName(handle, 0, 0, out string tagName, 256);
```

### GetQueryUGCPreviewURL (静态)

```csharp
bool GetQueryUGCPreviewURL(UGCQueryHandle_t handle, uint index, out string pchURL, uint cchURLSize)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)
- `pchURL` (`out string`)
- `cchURLSize` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUGC.GetQueryUGCPreviewURL(handle, 0, out string url, 256);
```

### GetQueryUGCMetadata (静态)

```csharp
bool GetQueryUGCMetadata(UGCQueryHandle_t handle, uint index, out string pchMetadata, uint cchMetadatasize)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)
- `pchMetadata` (`out string`)
- `cchMetadatasize` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
string metadata;
bool success = SteamGameServerUGC.GetQueryUGCMetadata(handle, 0, out metadata, 1024);
```

### GetQueryUGCChildren (静态)

```csharp
bool GetQueryUGCChildren(UGCQueryHandle_t handle, uint index, PublishedFileId_t[] pvecPublishedFileID, uint cMaxEntries)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)
- `pvecPublishedFileID` (`PublishedFileId_t[]`)
- `cMaxEntries` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
PublishedFileId_t[] children = new PublishedFileId_t[10];
bool success = SteamGameServerUGC.GetQueryUGCChildren(handle, 0, children, 10);
```

### GetQueryUGCStatistic (静态)

```csharp
bool GetQueryUGCStatistic(UGCQueryHandle_t handle, uint index, EItemStatistic eStatType, out ulong pStatValue)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)
- `eStatType` (`EItemStatistic`)
- `pStatValue` (`out ulong`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUGC.GetQueryUGCStatistic(handle, 0, EItemStatistic.NumSubscriptions, out ulong statValue);
```

### GetQueryUGCNumAdditionalPreviews (静态)

```csharp
uint GetQueryUGCNumAdditionalPreviews(UGCQueryHandle_t handle, uint index)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)

**返回值:** `uint`

**用法示例:**
```csharp
UGCQueryHandle_t handle = new UGCQueryHandle_t(12345);
uint numPreviews = SteamGameServerUGC.GetQueryUGCNumAdditionalPreviews(handle, 0);
```

### GetQueryUGCAdditionalPreview (静态)

```csharp
bool GetQueryUGCAdditionalPreview(UGCQueryHandle_t handle, uint index, uint previewIndex, out string pchURLOrVideoID, uint cchURLSize, out string pchOriginalFileName, uint cchOriginalFileNameSize, out EItemPreviewType pPreviewType)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)
- `previewIndex` (`uint`)
- `pchURLOrVideoID` (`out string`)
- `cchURLSize` (`uint`)
- `pchOriginalFileName` (`out string`)
- `cchOriginalFileNameSize` (`uint`)
- `pPreviewType` (`out EItemPreviewType`)

**返回值:** `bool`

**用法示例:**
```csharp
var result = SteamGameServerUGC.GetQueryUGCAdditionalPreview(handle, 0, 0, out string url, 256, out string fileName, 256, out EItemPreviewType previewType);
```

### GetQueryUGCNumKeyValueTags (静态)

```csharp
uint GetQueryUGCNumKeyValueTags(UGCQueryHandle_t handle, uint index)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)

**返回值:** `uint`

**用法示例:**
```csharp
UGCQueryHandle_t handle = default;
uint tagCount = SteamGameServerUGC.GetQueryUGCNumKeyValueTags(handle, 0);
```

### GetQueryUGCKeyValueTag (静态)

```csharp
bool GetQueryUGCKeyValueTag(UGCQueryHandle_t handle, uint index, uint keyValueTagIndex, out string pchKey, uint cchKeySize, out string pchValue, uint cchValueSize)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)
- `keyValueTagIndex` (`uint`)
- `pchKey` (`out string`)
- `cchKeySize` (`uint`)
- `pchValue` (`out string`)
- `cchValueSize` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUGC.GetQueryUGCKeyValueTag(handle, 0, 0, out string key, 256, out string value, 256);
```

### GetQueryUGCKeyValueTag (静态)

```csharp
bool GetQueryUGCKeyValueTag(UGCQueryHandle_t handle, uint index, string pchKey, out string pchValue, uint cchValueSize)
```

<para> 返回与pchKey匹配的第一个值。请注意，一个键可能映射到多个值。如果发生错误或未找到匹配的值，则返回false。</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)
- `pchKey` (`string`)
- `pchValue` (`out string`)
- `cchValueSize` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUGC.GetQueryUGCKeyValueTag(handle, 0, "tag_key", out string value, 256);
```

### GetNumSupportedGameVersions (静态)

```csharp
uint GetNumSupportedGameVersions(UGCQueryHandle_t handle, uint index)
```

<para> 某些物品可以指定其版本适用于一系列游戏版本（Steam分支）</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)

**返回值:** `uint`

**用法示例:**
```csharp
UGCQueryHandle_t handle = default;
uint numVersions = SteamGameServerUGC.GetNumSupportedGameVersions(handle, 0);
```

### GetSupportedGameVersionData (静态)

```csharp
bool GetSupportedGameVersionData(UGCQueryHandle_t handle, uint index, uint versionIndex, out string pchGameBranchMin, out string pchGameBranchMax, uint cchGameBranchSize)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)
- `versionIndex` (`uint`)
- `pchGameBranchMin` (`out string`)
- `pchGameBranchMax` (`out string`)
- `cchGameBranchSize` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUGC.GetSupportedGameVersionData(handle, 0, 0, out string min, out string max, 256);
```

### GetQueryUGCContentDescriptors (静态)

```csharp
uint GetQueryUGCContentDescriptors(UGCQueryHandle_t handle, uint index, out EUGCContentDescriptorID pvecDescriptors, uint cMaxEntries)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)
- `pvecDescriptors` (`out EUGCContentDescriptorID`)
- `cMaxEntries` (`uint`)

**返回值:** `uint`

**用法示例:**
```csharp
EUGCContentDescriptorID descriptor;
uint count = SteamGameServerUGC.GetQueryUGCContentDescriptors(handle, 0, out descriptor, 1);
```

### ReleaseQueryUGCRequest (静态)

```csharp
bool ReleaseQueryUGCRequest(UGCQueryHandle_t handle)
```

<para> 在检索结果后释放请求以释放内存</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUGC.ReleaseQueryUGCRequest(queryHandle);
```

### AddRequiredTag (静态)

```csharp
bool AddRequiredTag(UGCQueryHandle_t handle, string pTagName)
```

<para> 用于查询UGC的选项设置</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `pTagName` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUGC.AddRequiredTag(queryHandle, "Survival");
```

### AddRequiredTagGroup (静态)

```csharp
bool AddRequiredTagGroup(UGCQueryHandle_t handle, System.Collections.Generic.IList<string> pTagGroups)
```

<para> 匹配此组中的任意标签</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `pTagGroups` (`System.Collections.Generic.IList\<string\>`)

**返回值:** `bool`

**用法示例:**
```csharp
var tags = new List<string> { "Action", "Multiplayer" };
SteamGameServerUGC.AddRequiredTagGroup(handle, tags);
```

### AddExcludedTag (静态)

```csharp
bool AddExcludedTag(UGCQueryHandle_t handle, string pTagName)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `pTagName` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
UGCQueryHandle_t handle = SteamGameServerUGC.CreateQueryAllUGCRequest(SteamWorks.Interop.SteamUGCEQuery.k_EUGCQuery_RankedByTrend, SteamWorks.Interop.SteamWorkshopFileType.k_EWorkshopFileTypeCommunity);
SteamGameServerUGC.AddExcludedTag(handle, "inappropriate");
```

### SetReturnOnlyIDs (静态)

```csharp
bool SetReturnOnlyIDs(UGCQueryHandle_t handle, bool bReturnOnlyIDs)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `bReturnOnlyIDs` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
UGCQueryHandle_t handle = default;
SteamGameServerUGC.SetReturnOnlyIDs(handle, true);
```

### SetReturnKeyValueTags (静态)

```csharp
bool SetReturnKeyValueTags(UGCQueryHandle_t handle, bool bReturnKeyValueTags)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `bReturnKeyValueTags` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
UGCQueryHandle_t handle = new UGCQueryHandle_t(12345);
SteamGameServerUGC.SetReturnKeyValueTags(handle, true);
```

### SetReturnLongDescription (静态)

```csharp
bool SetReturnLongDescription(UGCQueryHandle_t handle, bool bReturnLongDescription)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `bReturnLongDescription` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
UGCQueryHandle_t handle = new UGCQueryHandle_t(12345);
SteamGameServerUGC.SetReturnLongDescription(handle, true);
```

### SetReturnMetadata (静态)

```csharp
bool SetReturnMetadata(UGCQueryHandle_t handle, bool bReturnMetadata)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `bReturnMetadata` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
UGCQueryHandle_t queryHandle = new UGCQueryHandle_t(12345);
SteamGameServerUGC.SetReturnMetadata(queryHandle, true);
```

### SetReturnChildren (静态)

```csharp
bool SetReturnChildren(UGCQueryHandle_t handle, bool bReturnChildren)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `bReturnChildren` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUGC.SetReturnChildren(handle, true);
```

### SetReturnAdditionalPreviews (静态)

```csharp
bool SetReturnAdditionalPreviews(UGCQueryHandle_t handle, bool bReturnAdditionalPreviews)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `bReturnAdditionalPreviews` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
UGCQueryHandle_t handle = new UGCQueryHandle_t(12345);
SteamGameServerUGC.SetReturnAdditionalPreviews(handle, true);
```

### SetReturnTotalOnly (静态)

```csharp
bool SetReturnTotalOnly(UGCQueryHandle_t handle, bool bReturnTotalOnly)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `bReturnTotalOnly` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
UGCQueryHandle_t handle = new UGCQueryHandle_t(12345);
SteamGameServerUGC.SetReturnTotalOnly(handle, true);
```

### SetReturnPlaytimeStats (静态)

```csharp
bool SetReturnPlaytimeStats(UGCQueryHandle_t handle, uint unDays)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `unDays` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUGC.SetReturnPlaytimeStats(queryHandle, 7);
```

### SetLanguage (静态)

```csharp
bool SetLanguage(UGCQueryHandle_t handle, string pchLanguage)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `pchLanguage` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
UGCQueryHandle_t handle = new UGCQueryHandle_t(12345);
SteamGameServerUGC.SetLanguage(handle, "english");
```

### SetAllowCachedResponse (静态)

```csharp
bool SetAllowCachedResponse(UGCQueryHandle_t handle, uint unMaxAgeSeconds)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `unMaxAgeSeconds` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
UGCQueryHandle_t handle = new UGCQueryHandle_t(12345);
SteamGameServerUGC.SetAllowCachedResponse(handle, 3600);
```

### SetAdminQuery (静态)

```csharp
bool SetAdminQuery(UGCUpdateHandle_t handle, bool bAdminQuery)
```

<para>管理员查询返回隐藏项</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `bAdminQuery` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUGC.SetAdminQuery(handle, true);
```

### SetCloudFileNameFilter (静态)

```csharp
bool SetCloudFileNameFilter(UGCQueryHandle_t handle, string pMatchCloudFileName)
```

<para> 仅用于查询用户UGC的选项</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `pMatchCloudFileName` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUGC.SetCloudFileNameFilter(queryHandle, "savegame.dat");
```

### SetMatchAnyTag (静态)

```csharp
bool SetMatchAnyTag(UGCQueryHandle_t handle, bool bMatchAnyTag)
```

<para> 仅用于查询所有UGC的选项</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `bMatchAnyTag` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUGC.SetMatchAnyTag(queryHandle, true);
```

### SetSearchText (静态)

```csharp
bool SetSearchText(UGCQueryHandle_t handle, string pSearchText)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `pSearchText` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUGC.SetSearchText(handle, "example_search");
```

### SetRankedByTrendDays (静态)

```csharp
bool SetRankedByTrendDays(UGCQueryHandle_t handle, uint unDays)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `unDays` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
UGCQueryHandle_t handle = UGCQueryHandle_t.Invalid;
SteamGameServerUGC.SetRankedByTrendDays(handle, 7);
```

### SetTimeCreatedDateRange (静态)

```csharp
bool SetTimeCreatedDateRange(UGCQueryHandle_t handle, uint rtStart, uint rtEnd)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `rtStart` (`uint`)
- `rtEnd` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
UGCQueryHandle_t queryHandle = UGCQueryHandle_t.Invalid;
bool result = SteamGameServerUGC.SetTimeCreatedDateRange(queryHandle, 1609459200, 1640995200);
```

### SetTimeUpdatedDateRange (静态)

```csharp
bool SetTimeUpdatedDateRange(UGCQueryHandle_t handle, uint rtStart, uint rtEnd)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `rtStart` (`uint`)
- `rtEnd` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
UGCQueryHandle_t handle = UGCQueryHandle_t.Invalid;
SteamGameServerUGC.SetTimeUpdatedDateRange(handle, 1609459200, 1612137600);
```

### AddRequiredKeyValueTag (静态)

```csharp
bool AddRequiredKeyValueTag(UGCQueryHandle_t handle, string pKey, string pValue)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `pKey` (`string`)
- `pValue` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
UGCQueryHandle_t handle = SteamGameServerUGC.CreateQueryUserUploadedItems(SteamId, EUGCList.k_EUGCList_UserPublished);
bool success = SteamGameServerUGC.AddRequiredKeyValueTag(handle, "type", "map");
```

### RequestUGCDetails (静态)

```csharp
SteamAPICall_t RequestUGCDetails(PublishedFileId_t nPublishedFileID, uint unMaxAgeSeconds)
```

<para> 已弃用 - 请改用上述 CreateQueryUGCDetailsRequest 调用！</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)
- `unMaxAgeSeconds` (`uint`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServerUGC.RequestUGCDetails(new PublishedFileId_t(123456789), 300);
```

### CreateItem (静态)

```csharp
SteamAPICall_t CreateItem(AppId_t nConsumerAppId, EWorkshopFileType eFileType)
```

<para>Steam 创意工坊创建者 API</para>
<para>为此应用创建尚未附带内容的新项目</para>

**参数:**

- `nConsumerAppId` (`AppId_t`)
- `eFileType` (`EWorkshopFileType`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServerUGC.CreateItem(new AppId_t(480), EWorkshopFileType.k_EWorkshopFileTypeCommunity);
```

### StartItemUpdate (静态)

```csharp
UGCUpdateHandle_t StartItemUpdate(AppId_t nConsumerAppId, PublishedFileId_t nPublishedFileID)
```

<para> 启动UGC项目更新。在使用CommitItemUpdate()提交更新之前，设置已更改的属性。</para>

**参数:**

- `nConsumerAppId` (`AppId_t`)
- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `UGCUpdateHandle_t`

**用法示例:**
```csharp
var updateHandle = SteamGameServerUGC.StartItemUpdate(new AppId_t(480), new PublishedFileId_t(123456789));
```

### SetItemTitle (静态)

```csharp
bool SetItemTitle(UGCUpdateHandle_t handle, string pchTitle)
```

<para>更改UGC项目的标题</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchTitle` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUGC.SetItemTitle(updateHandle, "My Workshop Item");
```

### SetItemDescription (静态)

```csharp
bool SetItemDescription(UGCUpdateHandle_t handle, string pchDescription)
```

<para>更改UGC物品的描述</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchDescription` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = SteamGameServerUGC.SetItemDescription(existingHandle, "New item description");
```

### SetItemUpdateLanguage (静态)

```csharp
bool SetItemUpdateLanguage(UGCUpdateHandle_t handle, string pchLanguage)
```

<para>指定将要设置的标题或描述的语言</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchLanguage` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUGC.SetItemUpdateLanguage(updateHandle, "english");
```

### SetItemMetadata (静态)

```csharp
bool SetItemMetadata(UGCUpdateHandle_t handle, string pchMetaData)
```

<para>更改UGC元数据的元数据（最大长度 = k_cchDeveloperMetadataMax）</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchMetaData` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
UGCUpdateHandle_t handle = new UGCUpdateHandle_t(12345);
SteamGameServerUGC.SetItemMetadata(handle, "MyCustomMetadata");
```

### SetItemVisibility (静态)

```csharp
bool SetItemVisibility(UGCUpdateHandle_t handle, ERemoteStoragePublishedFileVisibility eVisibility)
```

<para>更改UGC项目的可见性</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `eVisibility` (`ERemoteStoragePublishedFileVisibility`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUGC.SetItemVisibility(updateHandle, ERemoteStoragePublishedFileVisibility.k_ERemoteStoragePublishedFileVisibilityPublic);
```

### SetItemTags (静态)

```csharp
bool SetItemTags(UGCUpdateHandle_t updateHandle, System.Collections.Generic.IList<string> pTags, bool bAllowAdminTags = false)
```

<para>更改UGC物品的标签</para>

**参数:**

- `updateHandle` (`UGCUpdateHandle_t`)
- `pTags` (`System.Collections.Generic.IList\<string\>`)
- `bAllowAdminTags` (`bool`) = `false`

**返回值:** `bool`

**用法示例:**
```csharp
var tags = new List<string> { "Action", "Multiplayer" };
SteamGameServerUGC.SetItemTags(updateHandle, tags, false);
```

### SetItemContent (静态)

```csharp
bool SetItemContent(UGCUpdateHandle_t handle, string pszContentFolder)
```

<para>从本地文件夹更新物品内容</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pszContentFolder` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUGC.SetItemContent(updateHandle, "C:/MyModContent");
```

### SetItemPreview (静态)

```csharp
bool SetItemPreview(UGCUpdateHandle_t handle, string pszPreviewFile)
```

<para>更改此物品的预览图像文件。pszPreviewFile指向本地图像文件，该文件大小必须低于1MB</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pszPreviewFile` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUGC.SetItemPreview(updateHandle, "preview.png");
```

### SetAllowLegacyUpload (静态)

```csharp
bool SetAllowLegacyUpload(UGCUpdateHandle_t handle, bool bAllowLegacyUpload)
```

<para> 对单个小文件使用旧版上传。SetItemContent() 的参数应为包含单一文件的目录或该文件的完整路径。文件大小必须小于 10MB。</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `bAllowLegacyUpload` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUGC.SetAllowLegacyUpload(handle, true);
```

### RemoveAllItemKeyValueTags (静态)

```csharp
bool RemoveAllItemKeyValueTags(UGCUpdateHandle_t handle)
```

<para> 移除所有现有的键值标签（您可以通过 AddItemKeyValueTag 函数添加新的标签）</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)

**返回值:** `bool`

**用法示例:**
```csharp
UGCUpdateHandle_t handle = default;
SteamGameServerUGC.RemoveAllItemKeyValueTags(handle);
```

### RemoveItemKeyValueTags (静态)

```csharp
bool RemoveItemKeyValueTags(UGCUpdateHandle_t handle, string pchKey)
```

<para> 移除所有具有指定键的键值标签</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchKey` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
UGCUpdateHandle_t updateHandle = new UGCUpdateHandle_t(12345);
SteamGameServerUGC.RemoveItemKeyValueTags(updateHandle, "category");
```

### AddItemKeyValueTag (静态)

```csharp
bool AddItemKeyValueTag(UGCUpdateHandle_t handle, string pchKey, string pchValue)
```

<para>为物品添加新的键值标签。注意一个标签可以有多个值。</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchKey` (`string`)
- `pchValue` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
UGCUpdateHandle_t handle = new UGCUpdateHandle_t(12345);
SteamGameServerUGC.AddItemKeyValueTag(handle, "category", "weapons");
```

### AddItemPreviewFile (静态)

```csharp
bool AddItemPreviewFile(UGCUpdateHandle_t handle, string pszPreviewFile, EItemPreviewType type)
```

<para> 为此物品添加预览文件。pszPreviewFile 指向本地文件，其大小必须小于 1MB</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pszPreviewFile` (`string`)
- `type` (`EItemPreviewType`)

**返回值:** `bool`

**用法示例:**
```csharp
var handle = SteamGameServerUGC.StartItemUpdate(appId, publishedFileId);
SteamGameServerUGC.AddItemPreviewFile(handle, "preview.jpg", EItemPreviewType.Image);
```

### AddItemPreviewVideo (静态)

```csharp
bool AddItemPreviewVideo(UGCUpdateHandle_t handle, string pszVideoID)
```

<para> 为此物品添加预览视频</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pszVideoID` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
UGCUpdateHandle_t updateHandle = new UGCUpdateHandle_t(12345);
SteamGameServerUGC.AddItemPreviewVideo(updateHandle, "dQw4w9WgXcQ");
```

### UpdateItemPreviewFile (静态)

```csharp
bool UpdateItemPreviewFile(UGCUpdateHandle_t handle, uint index, string pszPreviewFile)
```

<para>更新此项目的现有预览文件。pszPreviewFile指向本地文件，文件大小不得超过1MB</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `index` (`uint`)
- `pszPreviewFile` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
UGCUpdateHandle_t handle = default;
bool result = SteamGameServerUGC.UpdateItemPreviewFile(handle, 0, "preview.jpg");
```

### UpdateItemPreviewVideo (静态)

```csharp
bool UpdateItemPreviewVideo(UGCUpdateHandle_t handle, uint index, string pszVideoID)
```

<para>更新此物品的现有预览视频</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `index` (`uint`)
- `pszVideoID` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUGC.UpdateItemPreviewVideo(handle, 0, "dQw4w9WgXcQ");
```

### RemoveItemPreview (静态)

```csharp
bool RemoveItemPreview(UGCUpdateHandle_t handle, uint index)
```

<para> 按索引移除预览，索引从0开始（预览已排序）</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `index` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
UGCUpdateHandle_t updateHandle = SteamGameServerUGC.StartItemUpdate(AppId, publishedFileId);
SteamGameServerUGC.RemoveItemPreview(updateHandle, 0);
```

### AddContentDescriptor (静态)

```csharp
bool AddContentDescriptor(UGCUpdateHandle_t handle, EUGCContentDescriptorID descid)
```

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `descid` (`EUGCContentDescriptorID`)

**返回值:** `bool`

**用法示例:**
```csharp
UGCUpdateHandle_t handle = UGCUpdateHandle_t.Invalid;
SteamGameServerUGC.AddContentDescriptor(handle, EUGCContentDescriptorID.k_EUGCContentDescriptor_NudityOrSexualContent);
```

### RemoveContentDescriptor (静态)

```csharp
bool RemoveContentDescriptor(UGCUpdateHandle_t handle, EUGCContentDescriptorID descid)
```

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `descid` (`EUGCContentDescriptorID`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = SteamGameServerUGC.RemoveContentDescriptor(handle, EUGCContentDescriptorID.Nudity);
```

### SetRequiredGameVersions (静态)

```csharp
bool SetRequiredGameVersions(UGCUpdateHandle_t handle, string pszGameBranchMin, string pszGameBranchMax)
```

<para>任一参数的空字符串表示它将匹配该范围端点的任意版本。这仅在实际内容已被修改时才会应用。</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pszGameBranchMin` (`string`)
- `pszGameBranchMax` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUGC.SetRequiredGameVersions(updateHandle, "1.0", "");
```

### SubmitItemUpdate (静态)

```csharp
SteamAPICall_t SubmitItemUpdate(UGCUpdateHandle_t handle, string pchChangeNote)
```

<para> 通过 StartItemUpdate() 启动的提交更新过程</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchChangeNote` (`string`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
UGCUpdateHandle_t handle = SteamGameServerUGC.StartItemUpdate(AppId, publishedFileId);
SteamAPICall_t call = SteamGameServerUGC.SubmitItemUpdate(handle, "Updated item description");
```

### GetItemUpdateProgress (静态)

```csharp
EItemUpdateStatus GetItemUpdateProgress(UGCUpdateHandle_t handle, out ulong punBytesProcessed, out ulong punBytesTotal)
```

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `punBytesProcessed` (`out ulong`)
- `punBytesTotal` (`out ulong`)

**返回值:** `EItemUpdateStatus`

**用法示例:**
```csharp
var status = SteamGameServerUGC.GetItemUpdateProgress(handle, out ulong processed, out ulong total);
```

### SetUserItemVote (静态)

```csharp
SteamAPICall_t SetUserItemVote(PublishedFileId_t nPublishedFileID, bool bVoteUp)
```

<para>Steam创意工坊消费者API</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)
- `bVoteUp` (`bool`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServerUGC.SetUserItemVote(new PublishedFileId_t(123456789), true);
```

### GetUserItemVote (静态)

```csharp
SteamAPICall_t GetUserItemVote(PublishedFileId_t nPublishedFileID)
```

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
var callHandle = SteamGameServerUGC.GetUserItemVote(new PublishedFileId_t(123456789));
```

### AddItemToFavorites (静态)

```csharp
SteamAPICall_t AddItemToFavorites(AppId_t nAppId, PublishedFileId_t nPublishedFileID)
```

**参数:**

- `nAppId` (`AppId_t`)
- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
var callHandle = SteamGameServerUGC.AddItemToFavorites(new AppId_t(480), new PublishedFileId_t(123456789));
```

### RemoveItemFromFavorites (静态)

```csharp
SteamAPICall_t RemoveItemFromFavorites(AppId_t nAppId, PublishedFileId_t nPublishedFileID)
```

**参数:**

- `nAppId` (`AppId_t`)
- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamGameServerUGC.RemoveItemFromFavorites(new AppId_t(480), new PublishedFileId_t(123456789));
```

### SubscribeItem (静态)

```csharp
SteamAPICall_t SubscribeItem(PublishedFileId_t nPublishedFileID)
```

<para>订阅此物品，将尽快安装</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
var callHandle = SteamGameServerUGC.SubscribeItem(new PublishedFileId_t(123456789));
```

### UnsubscribeItem (静态)

```csharp
SteamAPICall_t UnsubscribeItem(PublishedFileId_t nPublishedFileID)
```

<para> 取消订阅此物品，将在游戏退出后卸载</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
PublishedFileId_t fileId = new PublishedFileId_t(123456789);
SteamAPICall_t callHandle = SteamGameServerUGC.UnsubscribeItem(fileId);
```

### GetNumSubscribedItems (静态)

```csharp
uint GetNumSubscribedItems(bool bIncludeLocallyDisabled = false)
```

<para>已订阅物品数量</para>

**参数:**

- `bIncludeLocallyDisabled` (`bool`) = `false`

**返回值:** `uint`

**用法示例:**
```csharp
uint count = SteamGameServerUGC.GetNumSubscribedItems(false);
```

### GetSubscribedItems (静态)

```csharp
uint GetSubscribedItems(PublishedFileId_t[] pvecPublishedFileID, uint cMaxEntries, bool bIncludeLocallyDisabled = false)
```

<para>所有已订阅物品的PublishFileID</para>

**参数:**

- `pvecPublishedFileID` (`PublishedFileId_t[]`)
- `cMaxEntries` (`uint`)
- `bIncludeLocallyDisabled` (`bool`) = `false`

**返回值:** `uint`

**用法示例:**
```csharp
PublishedFileId_t[] items = new PublishedFileId_t[10];
uint count = SteamGameServerUGC.GetSubscribedItems(items, 10, false);
```

### GetItemState (静态)

```csharp
uint GetItemState(PublishedFileId_t nPublishedFileID)
```

<para> 获取此客户端上关于物品的EItemState标志</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `uint`

**用法示例:**
```csharp
PublishedFileId_t fileId = new PublishedFileId_t(123456789);
uint state = SteamGameServerUGC.GetItemState(fileId);
```

### GetItemInstallInfo (静态)

```csharp
bool GetItemInstallInfo(PublishedFileId_t nPublishedFileID, out ulong punSizeOnDisk, out string pchFolder, uint cchFolderSize, out uint punTimeStamp)
```

<para> 获取磁盘上已安装且设置了 k_EItemStateInstalled 标志的当前内容信息</para>
<para> 如果设置了 k_EItemStateLegacyItem，则 pchFolder 包含传统文件本身的路径（而非文件夹）</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)
- `punSizeOnDisk` (`out ulong`)
- `pchFolder` (`out string`)
- `cchFolderSize` (`uint`)
- `punTimeStamp` (`out uint`)

**返回值:** `bool`

**用法示例:**
```csharp
bool installed = SteamGameServerUGC.GetItemInstallInfo(fileId, out ulong size, out string folder, 1024, out uint timestamp);
```

### GetItemDownloadInfo (静态)

```csharp
bool GetItemDownloadInfo(PublishedFileId_t nPublishedFileID, out ulong punBytesDownloaded, out ulong punBytesTotal)
```

<para>获取针对设置了k_EItemStateNeedsUpdate状态的待更新物品信息。punBytesTotal将在下载开始后有效一次</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)
- `punBytesDownloaded` (`out ulong`)
- `punBytesTotal` (`out ulong`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUGC.GetItemDownloadInfo(new PublishedFileId_t(12345), out ulong downloaded, out ulong total);
```

### DownloadItem (静态)

```csharp
bool DownloadItem(PublishedFileId_t nPublishedFileID, bool bHighPriority)
```

<para> 下载新项目或更新已安装的项目。若函数返回 true，则等待 DownloadItemResult_t。若项目已安装，</para> <para> 则在接收到回调前不应使用磁盘上的文件。若项目未订阅，它将被缓存一段时间。</para> <para> 若设置了 bHighPriority，则会暂停任何其他项目的下载，并尽快下载此项目。</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)
- `bHighPriority` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUGC.DownloadItem(new PublishedFileId_t(123456789), true);
```

### BInitWorkshopForGameServer (静态)

```csharp
bool BInitWorkshopForGameServer(DepotId_t unWorkshopDepotID, string pszFolder)
```

<para>游戏服务器在发出任何UGC命令前，可先设置一个特定的工坊文件夹。</para>
<para>若您希望支持从同一安装文件夹运行多个游戏服务器，此功能将非常实用。</para>

**参数:**

- `unWorkshopDepotID` (`DepotId_t`)
- `pszFolder` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUGC.BInitWorkshopForGameServer(new DepotId_t(12345), "workshop_content");
```

### SuspendDownloads (静态)

```csharp
void SuspendDownloads(bool bSuspend)
```

<para> SuspendDownloads( true ) 将暂停所有创意工坊下载，直至调用 SuspendDownloads( false ) 或游戏结束</para>

**参数:**

- `bSuspend` (`bool`)

**用法示例:**
```csharp
SteamGameServerUGC.SuspendDownloads(true);
SteamGameServerUGC.SuspendDownloads(false);
```

### StartPlaytimeTracking (静态)

```csharp
SteamAPICall_t StartPlaytimeTracking(PublishedFileId_t[] pvecPublishedFileID, uint unNumPublishedFileIDs)
```

<para>使用追踪</para>

**参数:**

- `pvecPublishedFileID` (`PublishedFileId_t[]`)
- `unNumPublishedFileIDs` (`uint`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
var fileIds = new PublishedFileId_t[] { new PublishedFileId_t(12345) };
SteamAPICall_t call = SteamGameServerUGC.StartPlaytimeTracking(fileIds, 1);
```

### StopPlaytimeTracking (静态)

```csharp
SteamAPICall_t StopPlaytimeTracking(PublishedFileId_t[] pvecPublishedFileID, uint unNumPublishedFileIDs)
```

**参数:**

- `pvecPublishedFileID` (`PublishedFileId_t[]`)
- `unNumPublishedFileIDs` (`uint`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
PublishedFileId_t[] ids = { new PublishedFileId_t(12345) };
SteamAPICall_t call = SteamGameServerUGC.StopPlaytimeTracking(ids, 1);
```

### StopPlaytimeTrackingForAllItems (静态)

```csharp
SteamAPICall_t StopPlaytimeTrackingForAllItems()
```

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t callHandle = SteamGameServerUGC.StopPlaytimeTrackingForAllItems();
```

### AddDependency (静态)

```csharp
SteamAPICall_t AddDependency(PublishedFileId_t nParentPublishedFileID, PublishedFileId_t nChildPublishedFileID)
```

<para>父子关系或依赖项管理</para>

**参数:**

- `nParentPublishedFileID` (`PublishedFileId_t`)
- `nChildPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
var callHandle = SteamGameServerUGC.AddDependency(new PublishedFileId_t(12345), new PublishedFileId_t(67890));
```

### RemoveDependency (静态)

```csharp
SteamAPICall_t RemoveDependency(PublishedFileId_t nParentPublishedFileID, PublishedFileId_t nChildPublishedFileID)
```

**参数:**

- `nParentPublishedFileID` (`PublishedFileId_t`)
- `nChildPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
var callHandle = SteamGameServerUGC.RemoveDependency(new PublishedFileId_t(12345), new PublishedFileId_t(67890));
```

### AddAppDependency (静态)

```csharp
SteamAPICall_t AddAppDependency(PublishedFileId_t nPublishedFileID, AppId_t nAppID)
```

<para> 添加/移除应用程序依赖/需求（通常为DLC）</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)
- `nAppID` (`AppId_t`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamGameServerUGC.AddAppDependency(new PublishedFileId_t(123456789), new AppId_t(440));
```

### RemoveAppDependency (静态)

```csharp
SteamAPICall_t RemoveAppDependency(PublishedFileId_t nPublishedFileID, AppId_t nAppID)
```

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)
- `nAppID` (`AppId_t`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServerUGC.RemoveAppDependency(new PublishedFileId_t(123456789), new AppId_t(440));
```

### GetAppDependencies (静态)

```csharp
SteamAPICall_t GetAppDependencies(PublishedFileId_t nPublishedFileID)
```

<para>请求应用依赖项。请注意，您为 GetAppDependenciesResult_t 注册的回调函数可能会被多次调用</para> <para>直到所有应用依赖项均已返回</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServerUGC.GetAppDependencies(new PublishedFileId_t(123456789));
```

### DeleteItem (静态)

```csharp
SteamAPICall_t DeleteItem(PublishedFileId_t nPublishedFileID)
```

<para> 删除项目时不提示用户</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
var publishedFileId = new PublishedFileId_t(123456789);
SteamAPICall_t callHandle = SteamGameServerUGC.DeleteItem(publishedFileId);
```

### ShowWorkshopEULA (静态)

```csharp
bool ShowWorkshopEULA()
```

<para> 在叠加窗口中向用户显示应用最新的工坊最终用户许可协议，用户可在此选择接受或拒绝</para>

**返回值:** `bool`

**用法示例:**
```csharp
bool accepted = SteamGameServerUGC.ShowWorkshopEULA();
```

### GetWorkshopEULAStatus (静态)

```csharp
SteamAPICall_t GetWorkshopEULAStatus()
```

<para> 检索用户是否接受应用特定工坊EULA的相关信息</para>

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t callHandle = SteamGameServerUGC.GetWorkshopEULAStatus();
```

### GetUserContentDescriptorPreferences (静态)

```csharp
uint GetUserContentDescriptorPreferences(out EUGCContentDescriptorID pvecDescriptors, uint cMaxEntries)
```

<para> 返回用户的社区内容描述符偏好</para>

**参数:**

- `pvecDescriptors` (`out EUGCContentDescriptorID`)
- `cMaxEntries` (`uint`)

**返回值:** `uint`

**用法示例:**
```csharp
EUGCContentDescriptorID[] descriptors = new EUGCContentDescriptorID[10];
uint count = SteamGameServerUGC.GetUserContentDescriptorPreferences(out descriptors[0], (uint)descriptors.Length);
```

### SetItemsDisabledLocally (静态)

```csharp
bool SetItemsDisabledLocally(out PublishedFileId_t pvecPublishedFileIDs, uint unNumPublishedFileIDs, bool bDisabledLocally)
```

<para> 设置项目是否应在本地禁用。这意味着默认情况下它不会在 GetSubscribedItems() 中返回。</para>

**参数:**

- `pvecPublishedFileIDs` (`out PublishedFileId_t`)
- `unNumPublishedFileIDs` (`uint`)
- `bDisabledLocally` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
PublishedFileId_t[] ids = new PublishedFileId_t[1] { new PublishedFileId_t(123456) };
bool result = SteamGameServerUGC.SetItemsDisabledLocally(out ids[0], 1, true);
```

### SetSubscriptionsLoadOrder (静态)

```csharp
bool SetSubscriptionsLoadOrder(out PublishedFileId_t pvecPublishedFileIDs, uint unNumPublishedFileIDs)
```

<para> 设置这些物品的本地加载顺序。如果存在未包含在给定列表中的物品，它们将按订阅时间排序。</para>

**参数:**

- `pvecPublishedFileIDs` (`out PublishedFileId_t`)
- `unNumPublishedFileIDs` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
PublishedFileId_t[] ids = new PublishedFileId_t[0];
bool result = SteamGameServerUGC.SetSubscriptionsLoadOrder(out ids[0], 0);
```

