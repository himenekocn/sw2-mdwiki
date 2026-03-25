# 📦 SteamGameServerUGC

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### CreateQueryUserUGCRequest (静态)

```csharp
UGCQueryHandle_t CreateQueryUserUGCRequest(AccountID_t unAccountID, EUserUGCList eListType, EUGCMatchingUGCType eMatchingUGCType, EUserUGCListSortOrder eSortOrder, AppId_t nCreatorAppID, AppId_t nConsumerAppID, uint unPage)
```

查询与用户关联的用户生成内容（UGC）。创作者应用 ID 或消费者应用 ID 必须有效，并设置为当前运行的应用程序。未分页起始页码应设为 1。

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
var queryHandle = SteamGameServerUGC.CreateQueryUserUGCRequest(accountId, EUserUGCList.Value, EUGCMatchingUGCType.Value, EUserUGCListSortOrder.Value, appId, appId, 1u);
```

### CreateQueryAllUGCRequest (静态)

```csharp
UGCQueryHandle_t CreateQueryAllUGCRequest(EUGCQuery eQueryType, EUGCMatchingUGCType eMatchingeMatchingUGCTypeFileType, AppId_t nCreatorAppID, AppId_t nConsumerAppID, uint unPage)
```

查询所有匹配的 UGC。创建者应用 ID 或消费者应用 ID 必须有效并设置为当前运行的应用。unPage 应从 1 开始。

**参数:**

- `eQueryType` (`EUGCQuery`)
- `eMatchingeMatchingUGCTypeFileType` (`EUGCMatchingUGCType`)
- `nCreatorAppID` (`AppId_t`)
- `nConsumerAppID` (`AppId_t`)
- `unPage` (`uint`)

**返回值:** `UGCQueryHandle_t`

**用法示例:**
```csharp
var query = SteamGameServerUGC.CreateQueryAllUGCRequest(EUGCQuery.RankedByTrend, EUGCMatchingUGCType.Items, 480u, 480u, 1);
```

### CreateQueryAllUGCRequest (静态)

```csharp
UGCQueryHandle_t CreateQueryAllUGCRequest(EUGCQuery eQueryType, EUGCMatchingUGCType eMatchingeMatchingUGCTypeFileType, AppId_t nCreatorAppID, AppId_t nConsumerAppID, string pchCursor = null)
```

使用新的深度分页接口查询所有匹配的UGC（用户生成内容）。必须提供有效的创作者应用 ID 或消费者应用 ID，且需设置为当前运行的应用程序。pchCursor 应设置为 NULL 或 "*" 以获取第一组结果集。

**参数:**

- `eQueryType` (`EUGCQuery`)
- `eMatchingeMatchingUGCTypeFileType` (`EUGCMatchingUGCType`)
- `nCreatorAppID` (`AppId_t`)
- `nConsumerAppID` (`AppId_t`)
- `pchCursor` (`string`) = `null`

**返回值:** `UGCQueryHandle_t`

**用法示例:**
```csharp
var handle = SteamGameServerUGC.CreateQueryAllUGCRequest(EUGCQuery.RankedByTrend, EUGCMatchingUGCType.Items, currentAppId, currentAppId, "*");
```

### CreateQueryUGCDetailsRequest (静态)

```csharp
UGCQueryHandle_t CreateQueryUGCDetailsRequest(PublishedFileId_t[] pvecPublishedFileID, uint unNumPublishedFileIDs)
```

<para>查询给定已发布文件 ID 的详细信息（RequestUGCDetails 调用已弃用，由本接口替代）</para>

**参数:**

- `pvecPublishedFileID` (`PublishedFileId_t[]`)
- `unNumPublishedFileIDs` (`uint`)

**返回值:** `UGCQueryHandle_t`

**用法示例:**
```csharp
PublishedFileId_t[] fileIds = { publishedFileId1, publishedFileId2 };
UGCQueryHandle_t queryHandle = SteamGameServerUGC.CreateQueryUGCDetailsRequest(fileIds, (uint)fileIds.Length);
```

### SendQueryUGCRequest (静态)

```csharp
SteamAPICall_t SendQueryUGCRequest(UGCQueryHandle_t handle)
```

<para>向 Steam 发送查询</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServerUGC.SendQueryUGCRequest(handle);
```

### GetQueryUGCResult (静态)

```csharp
bool GetQueryUGCResult(UGCQueryHandle_t handle, uint index, out SteamUGCDetails_t pDetails)
```

<para>在收到查询用户生成内容（UGC）的回调后，检索单个结果。</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)
- `pDetails` (`out SteamUGCDetails_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamUGCDetails_t details;
bool ok = SteamGameServerUGC.GetQueryUGCResult(handle, index, out details);
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
uint tagCount = SteamGameServerUGC.GetQueryUGCNumTags(queryHandle, 0);
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
string tagValue;
bool ok = SteamGameServerUGC.GetQueryUGCTag(handle, 0, 0, out tagValue, 256);
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
bool ok = SteamGameServerUGC.GetQueryUGCTagDisplayName(handle, 0, 0, out string value, 256);
if (ok) Console.WriteLine(value);
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
string url;
bool ok = SteamGameServerUGC.GetQueryUGCPreviewURL(handle, 0, out url, 512);
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
bool ok = SteamGameServerUGC.GetQueryUGCMetadata(handle, 0u, out metadata, 256u);
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
var ok = SteamGameServerUGC.GetQueryUGCChildren(queryHandle, 0u, children, (uint)children.Length);
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
ulong statValue; bool ok = SteamGameServerUGC.GetQueryUGCStatistic(queryHandle, 0u, EItemStatistic.Value, out statValue);
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
UGCQueryHandle_t handle = queryHandle;
uint previewCount = SteamGameServerUGC.GetQueryUGCNumAdditionalPreviews(handle, 0);
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
string url, fileName; EItemPreviewType previewType;
bool ok = SteamGameServerUGC.GetQueryUGCAdditionalPreview(handle, 0, 0, out url, 256, out fileName, 260, out previewType);
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
uint numTags = SteamGameServerUGC.GetQueryUGCNumKeyValueTags(handle, 0u);
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
string key, value;
bool ok = SteamGameServerUGC.GetQueryUGCKeyValueTag(handle, 0u, 0u, out key, 256u, out value, 256u);
```

### GetQueryUGCKeyValueTag (静态)

```csharp
bool GetQueryUGCKeyValueTag(UGCQueryHandle_t handle, uint index, string pchKey, out string pchValue, uint cchValueSize)
```

<para>返回与 pchKey 匹配的第一个值。请注意，一个键可能映射到多个值。如果发生错误或未找到匹配的值，则返回 false。</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)
- `pchKey` (`string`)
- `pchValue` (`out string`)
- `cchValueSize` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
string value; bool ok = SteamGameServerUGC.GetQueryUGCKeyValueTag(handle, 0, "map", out value, 256);
```

### GetNumSupportedGameVersions (静态)

```csharp
uint GetNumSupportedGameVersions(UGCQueryHandle_t handle, uint index)
```

<para>某些物品可以指定其版本在特定游戏版本范围（Steam 分支）内有效</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)

**返回值:** `uint`

**用法示例:**
```csharp
uint supportedVersions = SteamGameServerUGC.GetNumSupportedGameVersions(handle, 0);
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
string minVersion, maxVersion;
bool ok = SteamGameServerUGC.GetSupportedGameVersionData(handle, 0, 0, out minVersion, out maxVersion, 128);
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
EUGCContentDescriptorID descriptor; uint count = SteamGameServerUGC.GetQueryUGCContentDescriptors(handle, 0, out descriptor, 1);
```

### ReleaseQueryUGCRequest (静态)

```csharp
bool ReleaseQueryUGCRequest(UGCQueryHandle_t handle)
```

<para>在获取结果后，释放请求以释放内存。</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)

**返回值:** `bool`

**用法示例:**
```csharp
bool released = SteamGameServerUGC.ReleaseQueryUGCRequest(handle);
```

### AddRequiredTag (静态)

```csharp
bool AddRequiredTag(UGCQueryHandle_t handle, string pTagName)
```

<para>用于查询 UGC 的设置选项</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `pTagName` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerUGC.AddRequiredTag(handle, "maps");
```

### AddRequiredTagGroup (静态)

```csharp
bool AddRequiredTagGroup(UGCQueryHandle_t handle, System.Collections.Generic.IList<string> pTagGroups)
```

<para>匹配此组中的任何标签</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `pTagGroups` (`System.Collections.Generic.IList\<string\>`)

**返回值:** `bool`

**用法示例:**
```csharp
bool added = SteamGameServerUGC.AddRequiredTagGroup(handle, tagGroups);
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
bool excluded = SteamGameServerUGC.AddExcludedTag(handle, "beta");
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
bool ok = SteamGameServerUGC.SetReturnKeyValueTags(handle, true);
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
SteamGameServerUGC.SetReturnLongDescription(existingHandle, true);
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
bool ok = SteamGameServerUGC.SetReturnMetadata(handle, true);
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
SteamGameServerUGC.SetReturnChildren(existingHandle, true);
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
var ok = SteamGameServerUGC.SetReturnAdditionalPreviews(handle, true);
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
UGCQueryHandle_t handle = default;
SteamGameServerUGC.SetReturnPlaytimeStats(handle, 7);
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
bool success = SteamGameServerUGC.SetLanguage(handle, "zh-CN");
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
SteamGameServerUGC.SetAllowCachedResponse(handle, 60u);
```

### SetAdminQuery (静态)

```csharp
bool SetAdminQuery(UGCUpdateHandle_t handle, bool bAdminQuery)
```

<para>管理员查询返回隐藏物品</para>

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

<para>仅用于查询用户 UGC 的选项</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `pMatchCloudFileName` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerUGC.SetCloudFileNameFilter(handle, "map_");
```

### SetMatchAnyTag (静态)

```csharp
bool SetMatchAnyTag(UGCQueryHandle_t handle, bool bMatchAnyTag)
```

仅用于查询所有用户生成内容的选项。

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `bMatchAnyTag` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerUGC.SetMatchAnyTag(handle, true);
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
bool ok = SteamGameServerUGC.SetSearchText(handle, "adventure");
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
bool ok = SteamGameServerUGC.SetRankedByTrendDays(handle, 7);
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
bool ok = SteamGameServerUGC.SetTimeCreatedDateRange(handle, 0u, 86400u);
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
bool ok = SteamGameServerUGC.SetTimeUpdatedDateRange(handle, 1700000000u, 1700086400u);
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
SteamGameServerUGC.AddRequiredKeyValueTag(handle, "mode", "hardcore");
```

### RequestUGCDetails (静态)

```csharp
SteamAPICall_t RequestUGCDetails(PublishedFileId_t nPublishedFileID, uint unMaxAgeSeconds)
```

<para>已弃用 - 请使用上方的 CreateQueryUGCDetailsRequest 调用！</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)
- `unMaxAgeSeconds` (`uint`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServerUGC.RequestUGCDetails(publishedFileId, 60);
```

### CreateItem (静态)

```csharp
SteamAPICall_t CreateItem(AppId_t nConsumerAppId, EWorkshopFileType eFileType)
```

<para>Steam 工坊创作者 API</para> <para>为本应用创建一个新项目，当前尚未附加任何内容</para>

**参数:**

- `nConsumerAppId` (`AppId_t`)
- `eFileType` (`EWorkshopFileType`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServerUGC.CreateItem((AppId_t)480, EWorkshopFileType.Community);
```

### StartItemUpdate (静态)

```csharp
UGCUpdateHandle_t StartItemUpdate(AppId_t nConsumerAppId, PublishedFileId_t nPublishedFileID)
```

启动用户生成内容（UGC）项目更新。在调用 CommitItemUpdate() 提交更新之前，先设置已更改的属性。

**参数:**

- `nConsumerAppId` (`AppId_t`)
- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `UGCUpdateHandle_t`

**用法示例:**
```csharp
var updateHandle = SteamGameServerUGC.StartItemUpdate(480, 12345678901234567UL);
```

### SetItemTitle (静态)

```csharp
bool SetItemTitle(UGCUpdateHandle_t handle, string pchTitle)
```

<para>更改用户生成内容（UGC）项目的标题</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchTitle` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerUGC.SetItemTitle(handle, "My UGC Title");
```

### SetItemDescription (静态)

```csharp
bool SetItemDescription(UGCUpdateHandle_t handle, string pchDescription)
```

<para>更改用户生成内容（UGC）项目的描述</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchDescription` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUGC.SetItemDescription(handle, "新的UGC描述");
```

### SetItemUpdateLanguage (静态)

```csharp
bool SetItemUpdateLanguage(UGCUpdateHandle_t handle, string pchLanguage)
```

<para>指定将设置的标题或描述的语言</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchLanguage` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUGC.SetItemUpdateLanguage(updateHandle, "zh-CN");
```

### SetItemMetadata (静态)

```csharp
bool SetItemMetadata(UGCUpdateHandle_t handle, string pchMetaData)
```

<para>更改UGC项的元数据（最大值 = k_cchDeveloperMetadataMax）</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchMetaData` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerUGC.SetItemMetadata(updateHandle, "dev-meta");
```

### SetItemVisibility (静态)

```csharp
bool SetItemVisibility(UGCUpdateHandle_t handle, ERemoteStoragePublishedFileVisibility eVisibility)
```

<para>更改 UGC 项目的可见性</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `eVisibility` (`ERemoteStoragePublishedFileVisibility`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerUGC.SetItemVisibility(handle, ERemoteStoragePublishedFileVisibility.Public);
```

### SetItemTags (静态)

```csharp
bool SetItemTags(UGCUpdateHandle_t updateHandle, System.Collections.Generic.IList<string> pTags, bool bAllowAdminTags = false)
```

<para>更改用户生成内容（UGC）项目的标签</para>

**参数:**

- `updateHandle` (`UGCUpdateHandle_t`)
- `pTags` (`System.Collections.Generic.IList\<string\>`)
- `bAllowAdminTags` (`bool`) = `false`

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUGC.SetItemTags(updateHandle, tags, true);
```

### SetItemContent (静态)

```csharp
bool SetItemContent(UGCUpdateHandle_t handle, string pszContentFolder)
```

从该本地文件夹更新物品内容

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pszContentFolder` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUGC.SetItemContent(updateHandle, contentFolder);
```

### SetItemPreview (静态)

```csharp
bool SetItemPreview(UGCUpdateHandle_t handle, string pszPreviewFile)
```

<para>更改此物品的前预览图像文件。pszPreviewFile 指向本地图像文件，其大小必须小于 1MB。</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pszPreviewFile` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerUGC.SetItemPreview(handle, @"D:\preview.jpg");
```

### SetAllowLegacyUpload (静态)

```csharp
bool SetAllowLegacyUpload(UGCUpdateHandle_t handle, bool bAllowLegacyUpload)
```

<para>使用传统上传方式上传单个小文件。SetItemContent() 方法的参数应为包含单个文件的目录，或该文件的完整路径。此外，文件大小必须小于 10MB。</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `bAllowLegacyUpload` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerUGC.SetAllowLegacyUpload(handle, true);
```

### RemoveAllItemKeyValueTags (静态)

```csharp
bool RemoveAllItemKeyValueTags(UGCUpdateHandle_t handle)
```

<para>移除所有现有的键值标签（可通过 AddItemKeyValueTag 函数添加新标签）</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)

**返回值:** `bool`

**用法示例:**
```csharp
bool removed = SteamGameServerUGC.RemoveAllItemKeyValueTags(handle);
```

### RemoveItemKeyValueTags (静态)

```csharp
bool RemoveItemKeyValueTags(UGCUpdateHandle_t handle, string pchKey)
```

<para>移除所有具有指定键的现有键值标签</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchKey` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool removed = SteamGameServerUGC.RemoveItemKeyValueTags(handle, "MyKey");
```

### AddItemKeyValueTag (静态)

```csharp
bool AddItemKeyValueTag(UGCUpdateHandle_t handle, string pchKey, string pchValue)
```

为该项目添加新的键值标签。请注意，一个标签可以拥有多个值。

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchKey` (`string`)
- `pchValue` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUGC.AddItemKeyValueTag(handle, "genre", "rpg");
```

### AddItemPreviewFile (静态)

```csharp
bool AddItemPreviewFile(UGCUpdateHandle_t handle, string pszPreviewFile, EItemPreviewType type)
```

<para>为此物品添加预览文件。pszPreviewFile 指向本地文件，该文件大小必须小于 1MB。</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pszPreviewFile` (`string`)
- `type` (`EItemPreviewType`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUGC.AddItemPreviewFile(handle, @"C:\previews\item_preview.jpg", EItemPreviewType.Image);
```

### AddItemPreviewVideo (静态)

```csharp
bool AddItemPreviewVideo(UGCUpdateHandle_t handle, string pszVideoID)
```

为该项目添加预览视频

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pszVideoID` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerUGC.AddItemPreviewVideo(handle, "video123");
```

### UpdateItemPreviewFile (静态)

```csharp
bool UpdateItemPreviewFile(UGCUpdateHandle_t handle, uint index, string pszPreviewFile)
```

更新此项目的现有预览文件。pszPreviewFile 指向本地文件，其大小必须小于 1MB。

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `index` (`uint`)
- `pszPreviewFile` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerUGC.UpdateItemPreviewFile(handle, 0, @"C:\preview.jpg");
```

### UpdateItemPreviewVideo (静态)

```csharp
bool UpdateItemPreviewVideo(UGCUpdateHandle_t handle, uint index, string pszVideoID)
```

更新该项目的现有预览视频

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `index` (`uint`)
- `pszVideoID` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUGC.UpdateItemPreviewVideo(handle, 0, "1234567890");
if (success) Console.WriteLine("Preview video updated");
```

### RemoveItemPreview (静态)

```csharp
bool RemoveItemPreview(UGCUpdateHandle_t handle, uint index)
```

通过从 0 开始的索引移除预览（预览已排序）

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `index` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
bool removed = SteamGameServerUGC.RemoveItemPreview(handle, 0u);
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
bool success = SteamGameServerUGC.AddContentDescriptor(handle, EUGCContentDescriptorID.Value);
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
bool ok = SteamGameServerUGC.RemoveContentDescriptor(handle, EUGCContentDescriptorID.Invalid);
```

### SetRequiredGameVersions (静态)

```csharp
bool SetRequiredGameVersions(UGCUpdateHandle_t handle, string pszGameBranchMin, string pszGameBranchMax)
```

任一参数为空字符串表示将匹配该范围内的任意版本。仅当实际内容已更改时，此规则才会生效。

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pszGameBranchMin` (`string`)
- `pszGameBranchMax` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
UGCUpdateHandle_t handle = 12345;
bool ok = SteamGameServerUGC.SetRequiredGameVersions(handle, "1.0.0", "2.0.0");
```

### SubmitItemUpdate (静态)

```csharp
SteamAPICall_t SubmitItemUpdate(UGCUpdateHandle_t handle, string pchChangeNote)
```

<para>更新流程已通过 StartItemUpdate() 启动</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchChangeNote` (`string`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServerUGC.SubmitItemUpdate(handle, "已更新物品内容");
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
ulong bytesProcessed, bytesTotal;
var status = SteamGameServerUGC.GetItemUpdateProgress(handle, out bytesProcessed, out bytesTotal);
```

### SetUserItemVote (静态)

```csharp
SteamAPICall_t SetUserItemVote(PublishedFileId_t nPublishedFileID, bool bVoteUp)
```

<para>Steam 工坊消费者 API</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)
- `bVoteUp` (`bool`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServerUGC.SetUserItemVote(publishedFileId, true);
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
var apiCall = SteamGameServerUGC.GetUserItemVote(publishedFileId);
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
SteamAPICall_t call = SteamGameServerUGC.AddItemToFavorites((AppId_t)480, (PublishedFileId_t)1234567890UL);
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
var call = SteamGameServerUGC.RemoveItemFromFavorites((AppId_t)480, (PublishedFileId_t)12345678901234567UL);
```

### SubscribeItem (静态)

```csharp
SteamAPICall_t SubscribeItem(PublishedFileId_t nPublishedFileID)
```

<para>订阅此项目，将尽快安装</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
PublishedFileId_t fileId = (PublishedFileId_t)123456789UL;
SteamGameServerUGC.SubscribeItem(fileId);
```

### UnsubscribeItem (静态)

```csharp
SteamAPICall_t UnsubscribeItem(PublishedFileId_t nPublishedFileID)
```

<para>取消订阅此项，游戏退出后将被卸载</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServerUGC.UnsubscribeItem(publishedFileId);
```

### GetNumSubscribedItems (静态)

```csharp
uint GetNumSubscribedItems(bool bIncludeLocallyDisabled = false)
```

订阅项目的数量

**参数:**

- `bIncludeLocallyDisabled` (`bool`) = `false`

**返回值:** `uint`

**用法示例:**
```csharp
uint subscribedCount = SteamGameServerUGC.GetNumSubscribedItems(false);
Console.WriteLine(subscribedCount);
```

### GetSubscribedItems (静态)

```csharp
uint GetSubscribedItems(PublishedFileId_t[] pvecPublishedFileID, uint cMaxEntries, bool bIncludeLocallyDisabled = false)
```

所有已订阅项目的发布文件 ID

**参数:**

- `pvecPublishedFileID` (`PublishedFileId_t[]`)
- `cMaxEntries` (`uint`)
- `bIncludeLocallyDisabled` (`bool`) = `false`

**返回值:** `uint`

**用法示例:**
```csharp
PublishedFileId_t[] itemIds = default; uint subscribedCount = SteamGameServerUGC.GetSubscribedItems(itemIds, 100u, false);
```

### GetItemState (静态)

```csharp
uint GetItemState(PublishedFileId_t nPublishedFileID)
```

<para>获取此客户端上该物品的 EItemState 标志</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `uint`

**用法示例:**
```csharp
PublishedFileId_t fileId = default;
uint state = SteamGameServerUGC.GetItemState(fileId);
```

### GetItemInstallInfo (静态)

```csharp
bool GetItemInstallInfo(PublishedFileId_t nPublishedFileID, out ulong punSizeOnDisk, out string pchFolder, uint cchFolderSize, out uint punTimeStamp)
```

<para>获取当前安装在光盘上且已设置 k_EItemStateInstalled 标志的项目的相关信息</para><para>若设置了 k_EItemStateLegacyItem，则 pchFolder 包含旧版文件自身的路径（而非文件夹路径）</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)
- `punSizeOnDisk` (`out ulong`)
- `pchFolder` (`out string`)
- `cchFolderSize` (`uint`)
- `punTimeStamp` (`out uint`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerUGC.GetItemInstallInfo(publishedFileId, out ulong sizeOnDisk, out string folder, 260, out uint timeStamp);
```

### GetItemDownloadInfo (静态)

```csharp
bool GetItemDownloadInfo(PublishedFileId_t nPublishedFileID, out ulong punBytesDownloaded, out ulong punBytesTotal)
```

获取已设置 k_EItemStateNeedsUpdate 标志的项目的待更新信息。下载开始后，punBytesTotal 将首次有效。

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)
- `punBytesDownloaded` (`out ulong`)
- `punBytesTotal` (`out ulong`)

**返回值:** `bool`

**用法示例:**
```csharp
ulong downloaded, total;
if (SteamGameServerUGC.GetItemDownloadInfo(fileId, out downloaded, out total)) Console.WriteLine($"{downloaded}/{total}");
```

### DownloadItem (静态)

```csharp
bool DownloadItem(PublishedFileId_t nPublishedFileID, bool bHighPriority)
```

<para>下载新项或更新已安装的项。如果函数返回 true，请等待 DownloadItemResult_t 回调。若该项已安装，则在收到回调前不应使用磁盘上的文件。若未订阅该物品，则会在一段时间内进行缓存。</para><para>若设置 bHighPriority，则挂起其他所有物品的下载任务，并尽快优先下载该项。</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)
- `bHighPriority` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerUGC.DownloadItem((PublishedFileId_t)1234567890UL, true);
```

### BInitWorkshopForGameServer (静态)

```csharp
bool BInitWorkshopForGameServer(DepotId_t unWorkshopDepotID, string pszFolder)
```

<para>游戏服务器可在发出任何用户生成内容（UGC）命令之前，设置一个特定的创意工坊文件夹。</para> <para>若您需要支持多个从同一安装目录启动的游戏服务器，此功能将十分有用。</para>

**参数:**

- `unWorkshopDepotID` (`DepotId_t`)
- `pszFolder` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUGC.BInitWorkshopForGameServer((DepotId_t)1001, @"D:\Workshop");
```

### SuspendDownloads (静态)

```csharp
void SuspendDownloads(bool bSuspend)
```

SuspendDownloads(true) 将暂停所有创意工坊下载，直到调用 SuspendDownloads(false) 或游戏结束为止。

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

翻译：<para>使用跟踪</para>

**参数:**

- `pvecPublishedFileID` (`PublishedFileId_t[]`)
- `unNumPublishedFileIDs` (`uint`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamGameServerUGC.StartPlaytimeTracking(publishedFileIds, (uint)publishedFileIds.Length);
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
SteamGameServerUGC.StopPlaytimeTracking(publishedFileIds, (uint)publishedFileIds.Length);
```

### StopPlaytimeTrackingForAllItems (静态)

```csharp
SteamAPICall_t StopPlaytimeTrackingForAllItems()
```

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServerUGC.StopPlaytimeTrackingForAllItems();
```

### AddDependency (静态)

```csharp
SteamAPICall_t AddDependency(PublishedFileId_t nParentPublishedFileID, PublishedFileId_t nChildPublishedFileID)
```

父级与子级关系或依赖管理

**参数:**

- `nParentPublishedFileID` (`PublishedFileId_t`)
- `nChildPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServerUGC.AddDependency(12345678901234567ul, 23456789012345678ul);
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
SteamAPICall_t call = SteamGameServerUGC.RemoveDependency(parentFileId, childFileId);
```

### AddAppDependency (静态)

```csharp
SteamAPICall_t AddAppDependency(PublishedFileId_t nPublishedFileID, AppId_t nAppID)
```

<para>添加/移除应用程序依赖/需求（通常为 DLC）</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)
- `nAppID` (`AppId_t`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServerUGC.AddAppDependency(publishedFileId, appId);
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
SteamAPICall_t call = SteamGameServerUGC.RemoveAppDependency(publishedFileId, appId);
```

### GetAppDependencies (静态)

```csharp
SteamAPICall_t GetAppDependencies(PublishedFileId_t nPublishedFileID)
```

<para>请求应用程序依赖项。请注意，为 GetAppDependenciesResult_t 注册的回调函数可能会被多次调用，</para><para>直到所有应用程序依赖项返回完毕。</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServerUGC.GetAppDependencies(123456789UL);
```

### DeleteItem (静态)

```csharp
SteamAPICall_t DeleteItem(PublishedFileId_t nPublishedFileID)
```

<para>删除该项目，无需提示用户</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServerUGC.DeleteItem(publishedFileId);
```

### ShowWorkshopEULA (静态)

```csharp
bool ShowWorkshopEULA()
```

<para>在叠加窗口中向用户展示该应用最新的工坊最终用户许可协议（EULA），用户可选择接受或拒绝。</para>

**返回值:** `bool`

**用法示例:**
```csharp
bool shown = SteamGameServerUGC.ShowWorkshopEULA();
if (!shown) Console.WriteLine("EULA 未能显示");
```

### GetWorkshopEULAStatus (静态)

```csharp
SteamAPICall_t GetWorkshopEULAStatus()
```

<para>获取与用户是否接受应用程序特定创意工坊最终用户许可协议相关的信息。</para>

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
var call = SteamGameServerUGC.GetWorkshopEULAStatus();
```

### GetUserContentDescriptorPreferences (静态)

```csharp
uint GetUserContentDescriptorPreferences(out EUGCContentDescriptorID pvecDescriptors, uint cMaxEntries)
```

<para>返回用户的社区内容描述符偏好设置</para>

**参数:**

- `pvecDescriptors` (`out EUGCContentDescriptorID`)
- `cMaxEntries` (`uint`)

**返回值:** `uint`

**用法示例:**
```csharp
EUGCContentDescriptorID descriptor;
uint count = SteamGameServerUGC.GetUserContentDescriptorPreferences(out descriptor, 1);
```

### SetItemsDisabledLocally (静态)

```csharp
bool SetItemsDisabledLocally(out PublishedFileId_t pvecPublishedFileIDs, uint unNumPublishedFileIDs, bool bDisabledLocally)
```

<para>设置该项目是否应在本地禁用。这意味着在默认情况下，它不会出现在 GetSubscribedItems() 的返回结果中。</para>

**参数:**

- `pvecPublishedFileIDs` (`out PublishedFileId_t`)
- `unNumPublishedFileIDs` (`uint`)
- `bDisabledLocally` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
PublishedFileId_t fileId;
SteamGameServerUGC.SetItemsDisabledLocally(out fileId, 1u, true);
```

### SetSubscriptionsLoadOrder (静态)

```csharp
bool SetSubscriptionsLoadOrder(out PublishedFileId_t pvecPublishedFileIDs, uint unNumPublishedFileIDs)
```

设置这些物品的本地加载顺序。如果列表中未包含某些物品，它们将按订阅时间进行排序。

**参数:**

- `pvecPublishedFileIDs` (`out PublishedFileId_t`)
- `unNumPublishedFileIDs` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
PublishedFileId_t fileId;
bool ok = SteamGameServerUGC.SetSubscriptionsLoadOrder(out fileId, 1u);
```

