# 📦 SteamGameServerUGC

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### CreateQueryUserUGCRequest (静态)

```csharp
UGCQueryHandle_t CreateQueryUserUGCRequest(AccountID_t unAccountID, EUserUGCList eListType, EUGCMatchingUGCType eMatchingUGCType, EUserUGCListSortOrder eSortOrder, AppId_t nCreatorAppID, AppId_t nConsumerAppID, uint unPage)
```

查询与用户关联的用户生成内容（UGC）。创建者应用ID或消费者应用ID必须有效，并设置为当前运行的应用。分页参数 `unPage` 应从 1 开始。

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
SteamGameServerUGC.CreateQueryUserUGCRequest(123456789, EUserUGCList.Value, EUGCMatchingUGCType.Value, EUserUGCListSortOrder.Value, 0u, 0u, 1);
```

### CreateQueryAllUGCRequest (静态)

```csharp
UGCQueryHandle_t CreateQueryAllUGCRequest(EUGCQuery eQueryType, EUGCMatchingUGCType eMatchingeMatchingUGCTypeFileType, AppId_t nCreatorAppID, AppId_t nConsumerAppID, uint unPage)
```

<para>查询所有匹配的用户生成内容 (UGC)。创建者应用 ID 或消费者应用 ID 必须有效，并设置为当前运行的应用。分页参数 (unPage) 应从 1 开始。</para>

**参数:**

- `eQueryType` (`EUGCQuery`)
- `eMatchingeMatchingUGCTypeFileType` (`EUGCMatchingUGCType`)
- `nCreatorAppID` (`AppId_t`)
- `nConsumerAppID` (`AppId_t`)
- `unPage` (`uint`)

**返回值:** `UGCQueryHandle_t`

**用法示例:**
```csharp
UGCQueryHandle_t handle = SteamGameServerUGC.CreateQueryAllUGCRequest(EUGCQuery.Value, EUGCMatchingUGCType.Value, AppId_t.Zero, AppId_t.Zero, 1);
```

### CreateQueryAllUGCRequest (静态)

```csharp
UGCQueryHandle_t CreateQueryAllUGCRequest(EUGCQuery eQueryType, EUGCMatchingUGCType eMatchingeMatchingUGCTypeFileType, AppId_t nCreatorAppID, AppId_t nConsumerAppID, string pchCursor = null)
```

<para> 使用新的深度分页接口查询所有匹配的用户生成内容（UGC）。创建者应用 ID 或消费者应用 ID 必须有效，并设置为当前运行的应用。pchCursor 应设置为 NULL 或 "*" 以获取第一个结果集。</para>

**参数:**

- `eQueryType` (`EUGCQuery`)
- `eMatchingeMatchingUGCTypeFileType` (`EUGCMatchingUGCType`)
- `nCreatorAppID` (`AppId_t`)
- `nConsumerAppID` (`AppId_t`)
- `pchCursor` (`string`) = `null`

**返回值:** `UGCQueryHandle_t`

**用法示例:**
```csharp
UGCQueryHandle_t handle = SteamGameServerUGC.CreateQueryAllUGCRequest(EUGCQuery.Value, EUGCMatchingUGCType.Value, AppId_t.Zero, AppId_t.Zero, "*");
```

### CreateQueryUGCDetailsRequest (静态)

```csharp
UGCQueryHandle_t CreateQueryUGCDetailsRequest(PublishedFileId_t[] pvecPublishedFileID, uint unNumPublishedFileIDs)
```

<para> 查询给定已发布文件 ID 的详细信息（RequestUGCDetails 调用已弃用并由本方法替代）</para>

**参数:**

- `pvecPublishedFileID` (`PublishedFileId_t[]`)
- `unNumPublishedFileIDs` (`uint`)

**返回值:** `UGCQueryHandle_t`

**用法示例:**
```csharp
SteamGameServerUGC.CreateQueryUGCDetailsRequest(new PublishedFileId_t[] { new PublishedFileId_t(123456) }, 1);
```

### SendQueryUGCRequest (静态)

```csharp
SteamAPICall_t SendQueryUGCRequest(UGCQueryHandle_t handle)
```

<para> 将查询发送至 Steam</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamGameServerUGC.SendQueryUGCRequest(myUGCQueryHandle);
```

### GetQueryUGCResult (静态)

```csharp
bool GetQueryUGCResult(UGCQueryHandle_t handle, uint index, out SteamUGCDetails_t pDetails)
```

<para> 在接收查询用户生成内容（UGC）的回调后，获取单个结果</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)
- `pDetails` (`out SteamUGCDetails_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamUGCDetails_t details;
bool success = SteamGameServerUGC.GetQueryUGCResult(queryHandle, 0, out details);
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
uint numTags = SteamGameServerUGC.GetQueryUGCNumTags(0u, 0u);
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
bool success = SteamGameServerUGC.GetQueryUGCTag(UGCQueryHandle_t.Invalid, 0u, 0u, out tagValue, 256u);
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
string displayName;
bool result = SteamGameServerUGC.GetQueryUGCTagDisplayName(UGCQueryHandle_t.Invalid, 0u, 0u, out displayName, 256u);
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
bool success = SteamGameServerUGC.GetQueryUGCPreviewURL(UGCQueryHandle_t.Invalid, 0, out url, 256);
Console.WriteLine($"URL: {url}, Success: {success}");
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
string metadata = "";
bool result = SteamGameServerUGC.GetQueryUGCMetadata(UGCQueryHandle_t.Invalid, 0, out metadata, 256);
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
SteamGameServerUGC.GetQueryUGCChildren(handle, index, new PublishedFileId_t[1], 1);
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
ulong statValue;
bool success = SteamGameServerUGC.GetQueryUGCStatistic(handle, 0u, EItemStatistic.Value, out statValue);
Console.WriteLine($"Stat: {statValue}, Success: {success}");
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
uint count = SteamGameServerUGC.GetQueryUGCNumAdditionalPreviews(myHandle, 0);
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
string url = "";
string filename = "";
EItemPreviewType previewType;
bool result = SteamGameServerUGC.GetQueryUGCAdditionalPreview(handle, 0, 0, out url, 256, out filename, 256, out previewType);
Console.WriteLine($"URL: {url}, File: {filename}, Type: {previewType}");
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
uint tagCount = SteamGameServerUGC.GetQueryUGCNumKeyValueTags(UGCQueryHandle_t.Invalid, 0);
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
string key = "", value = "";
SteamGameServerUGC.GetQueryUGCKeyValueTag(0u, 0u, 0u, out key, 256u, out value, 256u);
```

### GetQueryUGCKeyValueTag (静态)

```csharp
bool GetQueryUGCKeyValueTag(UGCQueryHandle_t handle, uint index, string pchKey, out string pchValue, uint cchValueSize)
```

<para> 返回与 pchKey 匹配的第一个值。请注意，一个键可能映射到多个值。如果发生错误或未找到匹配的值，则返回 false。</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)
- `pchKey` (`string`)
- `pchValue` (`out string`)
- `cchValueSize` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
string value;
bool result = SteamGameServerUGC.GetQueryUGCKeyValueTag(UGCQueryHandle_t.Invalid, 0u, "author", out value, 256u);
```

### GetNumSupportedGameVersions (静态)

```csharp
uint GetNumSupportedGameVersions(UGCQueryHandle_t handle, uint index)
```

<para>某些项可以指定其版本适用于一系列游戏版本（Steam 分支）</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)

**返回值:** `uint`

**用法示例:**
```csharp
uint count = SteamGameServerUGC.GetNumSupportedGameVersions(UGCQueryHandle_t.Invalid, 0);
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
string branchMin, branchMax;
SteamGameServerUGC.GetSupportedGameVersionData(UGCQueryHandle_t.Invalid, 0u, 0u, out branchMin, out branchMax, 256u);
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
uint[] descriptors = new uint[10];
uint count = SteamGameServerUGC.GetQueryUGCContentDescriptors(handle, 0, out EUGCContentDescriptorID desc, (uint)descriptors.Length);
```

### ReleaseQueryUGCRequest (静态)

```csharp
bool ReleaseQueryUGCRequest(UGCQueryHandle_t handle)
```

<para> 在获取结果后，释放请求以释放内存</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUGC.ReleaseQueryUGCRequest(myHandle);
```

### AddRequiredTag (静态)

```csharp
bool AddRequiredTag(UGCQueryHandle_t handle, string pTagName)
```

<para> 用于设置查询用户生成内容（UGC）的选项</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `pTagName` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = SteamGameServerUGC.AddRequiredTag(UGCQueryHandle_t.Invalid, "mytag");
```

### AddRequiredTagGroup (静态)

```csharp
bool AddRequiredTagGroup(UGCQueryHandle_t handle, System.Collections.Generic.IList<string> pTagGroups)
```

<para>匹配此组中的任意标签</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `pTagGroups` (`System.Collections.Generic.IList\<string\>`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUGC.AddRequiredTagGroup(handle, new List<string> { "tag1", "tag2" });
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
SteamGameServerUGC.AddExcludedTag(UGCQueryHandle_t.Invalid, "spam");
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
bool result = SteamGameServerUGC.SetReturnOnlyIDs(handle, true);
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
bool result = SteamGameServerUGC.SetReturnKeyValueTags(UGCQueryHandle_t.Invalid, true);
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
bool result = SteamGameServerUGC.SetReturnLongDescription(handle, true);
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
bool success = SteamGameServerUGC.SetReturnMetadata(UGCQueryHandle_t.Invalid, false);
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
bool result = SteamGameServerUGC.SetReturnChildren(UGCQueryHandle_t.Invalid, false);
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
bool result = SteamGameServerUGC.SetReturnAdditionalPreviews(UGCQueryHandle_t.Invalid, true);
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
bool result = SteamGameServerUGC.SetReturnTotalOnly(UGCQueryHandle_t.Invalid, true);
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
bool result = SteamGameServerUGC.SetReturnPlaytimeStats(handle, 7u);
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
SteamGameServerUGC.SetLanguage(handle, "en");
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
bool result = SteamGameServerUGC.SetAllowCachedResponse(myHandle, 300);
```

### SetAdminQuery (静态)

```csharp
bool SetAdminQuery(UGCUpdateHandle_t handle, bool bAdminQuery)
```

<para> 管理员查询返回隐藏项</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `bAdminQuery` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = SteamGameServerUGC.SetAdminQuery(handle, true);
```

### SetCloudFileNameFilter (静态)

```csharp
bool SetCloudFileNameFilter(UGCQueryHandle_t handle, string pMatchCloudFileName)
```

<para> 仅用于查询用户 UGC 的选项</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `pMatchCloudFileName` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = SteamGameServerUGC.SetCloudFileNameFilter(handle, "savegame.dat");
```

### SetMatchAnyTag (静态)

```csharp
bool SetMatchAnyTag(UGCQueryHandle_t handle, bool bMatchAnyTag)
```

<para> 仅用于查询所有 UGC 的选项</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `bMatchAnyTag` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = SteamGameServerUGC.SetMatchAnyTag(UGCQueryHandle_t.Invalid, false);
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
SteamGameServerUGC.SetSearchText(handle, "search term");
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
bool result = SteamGameServerUGC.SetRankedByTrendDays(handle, 7);
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
bool result = SteamGameServerUGC.SetTimeCreatedDateRange(handle, 1609459200u, 1612137600u);
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
bool success = SteamGameServerUGC.SetTimeUpdatedDateRange(handle, 1609459200u, 1612137600u);
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
bool result = SteamGameServerUGC.AddRequiredKeyValueTag(UGCQueryHandle_t.Invalid, "author", "valve");
```

### RequestUGCDetails (静态)

```csharp
SteamAPICall_t RequestUGCDetails(PublishedFileId_t nPublishedFileID, uint unMaxAgeSeconds)
```

<para> 已弃用 - 请改用上方的 CreateQueryUGCDetailsRequest 调用！</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)
- `unMaxAgeSeconds` (`uint`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t hCall = SteamGameServerUGC.RequestUGCDetails((PublishedFileId_t)123456u, 300);
```

### CreateItem (静态)

```csharp
SteamAPICall_t CreateItem(AppId_t nConsumerAppId, EWorkshopFileType eFileType)
```

<para> Steam Workshop 创作者 API</para> <para> 为此应用创建一个尚未附加任何内容的新项目</para>

**参数:**

- `nConsumerAppId` (`AppId_t`)
- `eFileType` (`EWorkshopFileType`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServerUGC.CreateItem(123456, EWorkshopFileType.Value);
```

### StartItemUpdate (静态)

```csharp
UGCUpdateHandle_t StartItemUpdate(AppId_t nConsumerAppId, PublishedFileId_t nPublishedFileID)
```

<para>开始一个用户生成内容（UGC）项目的更新。在调用 CommitItemUpdate() 提交更新之前，请先设置已更改的属性。</para>

**参数:**

- `nConsumerAppId` (`AppId_t`)
- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `UGCUpdateHandle_t`

**用法示例:**
```csharp
var handle = SteamGameServerUGC.StartItemUpdate(123456, 987654321);
SteamGameServerUGC.CommitItemUpdate(handle);
```

### SetItemTitle (静态)

```csharp
bool SetItemTitle(UGCUpdateHandle_t handle, string pchTitle)
```

<para>更改 UGC 项目的标题</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchTitle` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUGC.SetItemTitle(UGCUpdateHandle_t.Invalid, "New Title");
```

### SetItemDescription (静态)

```csharp
bool SetItemDescription(UGCUpdateHandle_t handle, string pchDescription)
```

<para> 修改一个 UGC 物品的描述</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchDescription` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUGC.SetItemDescription(handle, "Updated description");
```

### SetItemUpdateLanguage (静态)

```csharp
bool SetItemUpdateLanguage(UGCUpdateHandle_t handle, string pchLanguage)
```

<para> 指定将要设置的标题或描述的语言 </para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchLanguage` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUGC.SetItemUpdateLanguage(handle, "English");
```

### SetItemMetadata (静态)

```csharp
bool SetItemMetadata(UGCUpdateHandle_t handle, string pchMetaData)
```

<para> 更改 UGC 项目的元数据（最大长度为 k_cchDeveloperMetadataMax）</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchMetaData` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUGC.SetItemMetadata(UGCUpdateHandle_t.Invalid, "Updated metadata");
```

### SetItemVisibility (静态)

```csharp
bool SetItemVisibility(UGCUpdateHandle_t handle, ERemoteStoragePublishedFileVisibility eVisibility)
```

<para>更改 UGC 项的可见性</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `eVisibility` (`ERemoteStoragePublishedFileVisibility`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUGC.SetItemVisibility(handle, ERemoteStoragePublishedFileVisibility.k_ERemoteStoragePublishedFileVisibilityPublic);
```

### SetItemTags (静态)

```csharp
bool SetItemTags(UGCUpdateHandle_t updateHandle, System.Collections.Generic.IList<string> pTags, bool bAllowAdminTags = false)
```

<para> 修改一个用户生成内容（UGC）项目的标签</para>

**参数:**

- `updateHandle` (`UGCUpdateHandle_t`)
- `pTags` (`System.Collections.Generic.IList\<string\>`)
- `bAllowAdminTags` (`bool`) = `false`

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUGC.SetItemTags(UGCUpdateHandle_t.Zero, new List<string> { "tag1", "tag2" }, false);
```

### SetItemContent (静态)

```csharp
bool SetItemContent(UGCUpdateHandle_t handle, string pszContentFolder)
```

<para> 从此本地文件夹更新项目内容</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pszContentFolder` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = SteamGameServerUGC.SetItemContent(handle, "content_folder_path");
```

### SetItemPreview (静态)

```csharp
bool SetItemPreview(UGCUpdateHandle_t handle, string pszPreviewFile)
```

<para> 更改此项目的预览图像文件。pszPreviewFile 指向本地图像文件，其大小必须小于 1MB。</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pszPreviewFile` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUGC.SetItemPreview(handle, "preview.jpg");
```

### SetAllowLegacyUpload (静态)

```csharp
bool SetAllowLegacyUpload(UGCUpdateHandle_t handle, bool bAllowLegacyUpload)
```

<para>对单个小型文件使用传统上传方式。SetItemContent() 方法的参数应为包含一个文件的目录，或文件的完整路径。文件大小也必须小于 10MB。</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `bAllowLegacyUpload` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = SteamGameServerUGC.SetAllowLegacyUpload(UGCUpdateHandle_t.Invalid, true);
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
bool success = SteamGameServerUGC.RemoveAllItemKeyValueTags(handle);
```

### RemoveItemKeyValueTags (静态)

```csharp
bool RemoveItemKeyValueTags(UGCUpdateHandle_t handle, string pchKey)
```

<para> 移除所有具有指定键的现有键值标签</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchKey` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUGC.RemoveItemKeyValueTags(handle, "exampleKey");
```

### AddItemKeyValueTag (静态)

```csharp
bool AddItemKeyValueTag(UGCUpdateHandle_t handle, string pchKey, string pchValue)
```

为该项添加新的键值标签。请注意，一个标签可以有多个值。

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchKey` (`string`)
- `pchValue` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUGC.AddItemKeyValueTag(handle, "author", "Valve");
```

### AddItemPreviewFile (静态)

```csharp
bool AddItemPreviewFile(UGCUpdateHandle_t handle, string pszPreviewFile, EItemPreviewType type)
```

<para> 为此项目添加预览文件。pszPreviewFile 指向本地文件，该文件大小必须小于 1MB。</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pszPreviewFile` (`string`)
- `type` (`EItemPreviewType`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = SteamGameServerUGC.AddItemPreviewFile(handle, "preview.jpg", EItemPreviewType.Image);
```

### AddItemPreviewVideo (静态)

```csharp
bool AddItemPreviewVideo(UGCUpdateHandle_t handle, string pszVideoID)
```

<para> 为此项目添加预览视频</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pszVideoID` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUGC.AddItemPreviewVideo(handle, "video123");
```

### UpdateItemPreviewFile (静态)

```csharp
bool UpdateItemPreviewFile(UGCUpdateHandle_t handle, uint index, string pszPreviewFile)
```

<para> 更新此项目的现有预览文件。pszPreviewFile 指向本地文件，该文件大小必须小于 1MB。</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `index` (`uint`)
- `pszPreviewFile` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = SteamGameServerUGC.UpdateItemPreviewFile(handle, 0u, "preview.jpg");
```

### UpdateItemPreviewVideo (静态)

```csharp
bool UpdateItemPreviewVideo(UGCUpdateHandle_t handle, uint index, string pszVideoID)
```

<para> 更新此项目的现有预览视频</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `index` (`uint`)
- `pszVideoID` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = SteamGameServerUGC.UpdateItemPreviewVideo(handle, 0, "video123");
```

### RemoveItemPreview (静态)

```csharp
bool RemoveItemPreview(UGCUpdateHandle_t handle, uint index)
```

<para> 通过从 0 开始的索引移除预览（预览已排序）</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `index` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUGC.RemoveItemPreview(handle, 0);
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
bool result = SteamGameServerUGC.AddContentDescriptor(handle, EUGCContentDescriptorID.Value);
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
bool result = SteamGameServerUGC.RemoveContentDescriptor(handle, EUGCContentDescriptorID.Value);
```

### SetRequiredGameVersions (静态)

```csharp
bool SetRequiredGameVersions(UGCUpdateHandle_t handle, string pszGameBranchMin, string pszGameBranchMax)
```

<para> 任何一个参数为空字符串意味着它将匹配该范围端点上的任何版本。此规则仅在内容实际发生更改时才会应用。</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pszGameBranchMin` (`string`)
- `pszGameBranchMax` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUGC.SetRequiredGameVersions(handle, "1.0", "2.5");
```

### SubmitItemUpdate (静态)

```csharp
SteamAPICall_t SubmitItemUpdate(UGCUpdateHandle_t handle, string pchChangeNote)
```

<para> 提交更新过程通过 StartItemUpdate() 方法启动</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchChangeNote` (`string`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamGameServerUGC.SubmitItemUpdate(updateHandle, "Updated item description");
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
var status = SteamGameServerUGC.GetItemUpdateProgress(default(UGCUpdateHandle_t), out bytesProcessed, out bytesTotal);
Console.WriteLine($"Status: {status}, Progress: {bytesProcessed}/{bytesTotal}");
```

### SetUserItemVote (静态)

```csharp
SteamAPICall_t SetUserItemVote(PublishedFileId_t nPublishedFileID, bool bVoteUp)
```

<para> Steam Workshop 消费者 API</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)
- `bVoteUp` (`bool`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamGameServerUGC.SetUserItemVote(new PublishedFileId_t(12345), true);
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
SteamAPICall_t call = SteamGameServerUGC.GetUserItemVote(PublishedFileId_t(12345));
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
SteamGameServerUGC.AddItemToFavorites(123456, 987654);
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
SteamGameServerUGC.RemoveItemFromFavorites(440, new PublishedFileId_t(12345));
```

### SubscribeItem (静态)

```csharp
SteamAPICall_t SubscribeItem(PublishedFileId_t nPublishedFileID)
```

订阅此项目，将尽快安装。

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamGameServerUGC.SubscribeItem(new PublishedFileId_t(12345));
```

### UnsubscribeItem (静态)

```csharp
SteamAPICall_t UnsubscribeItem(PublishedFileId_t nPublishedFileID)
```

<para>取消对此项目的订阅，游戏退出后将卸载</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamGameServerUGC.UnsubscribeItem(new PublishedFileId_t(12345));
```

### GetNumSubscribedItems (静态)

```csharp
uint GetNumSubscribedItems(bool bIncludeLocallyDisabled = false)
```

已订阅项的数量

**参数:**

- `bIncludeLocallyDisabled` (`bool`) = `false`

**返回值:** `uint`

**用法示例:**
```csharp
uint count = SteamGameServerUGC.GetNumSubscribedItems(true);
```

### GetSubscribedItems (静态)

```csharp
uint GetSubscribedItems(PublishedFileId_t[] pvecPublishedFileID, uint cMaxEntries, bool bIncludeLocallyDisabled = false)
```

所有已订阅项的发布文件ID

**参数:**

- `pvecPublishedFileID` (`PublishedFileId_t[]`)
- `cMaxEntries` (`uint`)
- `bIncludeLocallyDisabled` (`bool`) = `false`

**返回值:** `uint`

**用法示例:**
```csharp
uint[] fileIds = new uint[10];
uint count = SteamGameServerUGC.GetSubscribedItems(fileIds, (uint)fileIds.Length, false);
```

### GetItemState (静态)

```csharp
uint GetItemState(PublishedFileId_t nPublishedFileID)
```

<para> 获取此客户端上项目的 EItemState 标志</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `uint`

**用法示例:**
```csharp
uint state = SteamGameServerUGC.GetItemState(1234567890);
Console.WriteLine($"Item state: {state}");
```

### GetItemInstallInfo (静态)

```csharp
bool GetItemInstallInfo(PublishedFileId_t nPublishedFileID, out ulong punSizeOnDisk, out string pchFolder, uint cchFolderSize, out uint punTimeStamp)
```

<para> 获取已安装内容的信息，这些内容对应于其状态为 k_EItemStateInstalled 的项目。</para> <para> 如果设置了 k_EItemStateLegacyItem，则 pchFolder 包含的是旧版文件本身的路径（而非文件夹路径）。</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)
- `punSizeOnDisk` (`out ulong`)
- `pchFolder` (`out string`)
- `cchFolderSize` (`uint`)
- `punTimeStamp` (`out uint`)

**返回值:** `bool`

**用法示例:**
```csharp
ulong sizeOnDisk;
string folder;
uint timeStamp;
bool result = SteamGameServerUGC.GetItemInstallInfo(new PublishedFileId_t(12345), out sizeOnDisk, out folder, 260, out timeStamp);
```

### GetItemDownloadInfo (静态)

```csharp
bool GetItemDownloadInfo(PublishedFileId_t nPublishedFileID, out ulong punBytesDownloaded, out ulong punBytesTotal)
```

<para> 获取具有 k_EItemStateNeedsUpdate 状态的项目的待处理更新信息。一旦下载开始，punBytesTotal 将变为有效。</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)
- `punBytesDownloaded` (`out ulong`)
- `punBytesTotal` (`out ulong`)

**返回值:** `bool`

**用法示例:**
```csharp
ulong downloaded, total;
bool result = SteamGameServerUGC.GetItemDownloadInfo(new PublishedFileId_t(12345), out downloaded, out total);
Console.WriteLine($"Downloaded: {downloaded}, Total: {total}, Success: {result}");
```

### DownloadItem (静态)

```csharp
bool DownloadItem(PublishedFileId_t nPublishedFileID, bool bHighPriority)
```

<para>下载新项目或更新已安装的项目。如果函数返回 true，则等待 DownloadItemResult_t。如果项目已安装，则在收到回调之前不应使用磁盘上的文件。如果未订阅该项目，它将被缓存一段时间。</para> <para>如果设置了 bHighPriority，则将暂停任何其他项目的下载，并尽快下载此项目。</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)
- `bHighPriority` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerUGC.DownloadItem((PublishedFileId_t)12345, true);
if (success)
{
    // 等待 DownloadItemResult_t 回调后再使用文件
}
```

### BInitWorkshopForGameServer (静态)

```csharp
bool BInitWorkshopForGameServer(DepotId_t unWorkshopDepotID, string pszFolder)
```

<para>游戏服务器可以在发出任何 UGC 命令之前设置一个特定的工坊文件夹。</para> <para>如果您希望支持多个游戏服务器从同一个安装文件夹中运行，这会很有帮助。</para>

**参数:**

- `unWorkshopDepotID` (`DepotId_t`)
- `pszFolder` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerUGC.BInitWorkshopForGameServer(123456, "workshop_content");
```

### SuspendDownloads (静态)

```csharp
void SuspendDownloads(bool bSuspend)
```

<para>调用 SuspendDownloads( true ) 将会暂停所有工坊下载，直到调用 SuspendDownloads( false ) 或游戏结束为止</para>

**参数:**

- `bSuspend` (`bool`)

**用法示例:**
```csharp
SteamGameServerUGC.SuspendDownloads(true);
// ... 暂停期间 ...
SteamGameServerUGC.SuspendDownloads(false);
```

### StartPlaytimeTracking (静态)

```csharp
SteamAPICall_t StartPlaytimeTracking(PublishedFileId_t[] pvecPublishedFileID, uint unNumPublishedFileIDs)
```

<para>使用情况跟踪</para>

**参数:**

- `pvecPublishedFileID` (`PublishedFileId_t[]`)
- `unNumPublishedFileIDs` (`uint`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamGameServerUGC.StartPlaytimeTracking(new PublishedFileId_t[] { new PublishedFileId_t(12345) }, 1);
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
SteamGameServerUGC.StopPlaytimeTracking(new PublishedFileId_t[] { new PublishedFileId_t(12345) }, 1);
```

### StopPlaytimeTrackingForAllItems (静态)

```csharp
SteamAPICall_t StopPlaytimeTrackingForAllItems()
```

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamGameServerUGC.StopPlaytimeTrackingForAllItems();
```

### AddDependency (静态)

```csharp
SteamAPICall_t AddDependency(PublishedFileId_t nParentPublishedFileID, PublishedFileId_t nChildPublishedFileID)
```

<para> 父子关系或依赖管理</para>

**参数:**

- `nParentPublishedFileID` (`PublishedFileId_t`)
- `nChildPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamGameServerUGC.AddDependency(12345, 67890);
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
SteamGameServerUGC.RemoveDependency(parentId, childId);
```

### AddAppDependency (静态)

```csharp
SteamAPICall_t AddAppDependency(PublishedFileId_t nPublishedFileID, AppId_t nAppID)
```

<para> 添加/移除应用程序依赖项/要求（通常是DLC）</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)
- `nAppID` (`AppId_t`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamGameServerUGC.AddAppDependency(new PublishedFileId_t(12345), new AppId_t(67890));
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
SteamGameServerUGC.RemoveAppDependency(PublishedFileId_t(12345), AppId_t(400));
```

### GetAppDependencies (静态)

```csharp
SteamAPICall_t GetAppDependencies(PublishedFileId_t nPublishedFileID)
```

请求应用程序依赖项。请注意，您为 GetAppDependenciesResult_t 注册的任何回调都可能会被多次调用，直到所有应用程序依赖项都已返回。

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServerUGC.GetAppDependencies(123456789);
```

### DeleteItem (静态)

```csharp
SteamAPICall_t DeleteItem(PublishedFileId_t nPublishedFileID)
```

<para> 删除项目时不提示用户 </para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamGameServerUGC.DeleteItem(new PublishedFileId_t(12345));
```

### ShowWorkshopEULA (静态)

```csharp
bool ShowWorkshopEULA()
```

<para> 在一个覆盖窗口中向用户显示应用的最新 Workshop EULA，用户可以在其中接受或不接受。</para>

**返回值:** `bool`

**用法示例:**
```csharp
bool accepted = SteamGameServerUGC.ShowWorkshopEULA();
```

### GetWorkshopEULAStatus (静态)

```csharp
SteamAPICall_t GetWorkshopEULAStatus()
```

<para> 获取与用户是否接受应用特定工作坊 EULA 相关的信息</para>

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServerUGC.GetWorkshopEULAStatus();
```

### GetUserContentDescriptorPreferences (静态)

```csharp
uint GetUserContentDescriptorPreferences(out EUGCContentDescriptorID pvecDescriptors, uint cMaxEntries)
```

<para> 返回用户的社区内容描述符首选项</para>

**参数:**

- `pvecDescriptors` (`out EUGCContentDescriptorID`)
- `cMaxEntries` (`uint`)

**返回值:** `uint`

**用法示例:**
```csharp
uint count = SteamGameServerUGC.GetUserContentDescriptorPreferences(out EUGCContentDescriptorID[] descriptors, 10);
```

### SetItemsDisabledLocally (静态)

```csharp
bool SetItemsDisabledLocally(out PublishedFileId_t pvecPublishedFileIDs, uint unNumPublishedFileIDs, bool bDisabledLocally)
```

<para>设置该项是否应在本地被禁用。这意味着默认情况下，它将不会在 GetSubscribedItems() 中返回。</para>

**参数:**

- `pvecPublishedFileIDs` (`out PublishedFileId_t`)
- `unNumPublishedFileIDs` (`uint`)
- `bDisabledLocally` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
PublishedFileId_t[] fileIds = { new PublishedFileId_t(12345) };
SteamGameServerUGC.SetItemsDisabledLocally(fileIds, (uint)fileIds.Length, true);
```

### SetSubscriptionsLoadOrder (静态)

```csharp
bool SetSubscriptionsLoadOrder(out PublishedFileId_t pvecPublishedFileIDs, uint unNumPublishedFileIDs)
```

<para> 设置这些项目的本地加载顺序。如果存在给定列表中未包含的项目，它们将按订阅时间进行排序。</para>

**参数:**

- `pvecPublishedFileIDs` (`out PublishedFileId_t`)
- `unNumPublishedFileIDs` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint[] fileIds = { 123u, 456u };
SteamGameServerUGC.SetSubscriptionsLoadOrder(fileIds, (uint)fileIds.Length);
```

