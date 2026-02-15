# 📦 SteamGameServerUGC

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### CreateQueryUserUGCRequest (静态)

```csharp
UGCQueryHandle_t CreateQueryUserUGCRequest(AccountID_t unAccountID, EUserUGCList eListType, EUGCMatchingUGCType eMatchingUGCType, EUserUGCListSortOrder eSortOrder, AppId_t nCreatorAppID, AppId_t nConsumerAppID, uint unPage)
```

<para> Query UGC associated with a user. Creator app id or consumer app id must be valid and be set to the current running app. unPage should start at 1.</para>

**参数:**

- `unAccountID` (`AccountID_t`)
- `eListType` (`EUserUGCList`)
- `eMatchingUGCType` (`EUGCMatchingUGCType`)
- `eSortOrder` (`EUserUGCListSortOrder`)
- `nCreatorAppID` (`AppId_t`)
- `nConsumerAppID` (`AppId_t`)
- `unPage` (`uint`)

**返回值:** `UGCQueryHandle_t`

### CreateQueryAllUGCRequest (静态)

```csharp
UGCQueryHandle_t CreateQueryAllUGCRequest(EUGCQuery eQueryType, EUGCMatchingUGCType eMatchingeMatchingUGCTypeFileType, AppId_t nCreatorAppID, AppId_t nConsumerAppID, uint unPage)
```

<para> Query for all matching UGC. Creator app id or consumer app id must be valid and be set to the current running app. unPage should start at 1.</para>

**参数:**

- `eQueryType` (`EUGCQuery`)
- `eMatchingeMatchingUGCTypeFileType` (`EUGCMatchingUGCType`)
- `nCreatorAppID` (`AppId_t`)
- `nConsumerAppID` (`AppId_t`)
- `unPage` (`uint`)

**返回值:** `UGCQueryHandle_t`

### CreateQueryAllUGCRequest (静态)

```csharp
UGCQueryHandle_t CreateQueryAllUGCRequest(EUGCQuery eQueryType, EUGCMatchingUGCType eMatchingeMatchingUGCTypeFileType, AppId_t nCreatorAppID, AppId_t nConsumerAppID, string pchCursor = null)
```

<para> Query for all matching UGC using the new deep paging interface. Creator app id or consumer app id must be valid and be set to the current running app. pchCursor should be set to NULL or "*" to get the first result set.</para>

**参数:**

- `eQueryType` (`EUGCQuery`)
- `eMatchingeMatchingUGCTypeFileType` (`EUGCMatchingUGCType`)
- `nCreatorAppID` (`AppId_t`)
- `nConsumerAppID` (`AppId_t`)
- `pchCursor` (`string`) = `null`

**返回值:** `UGCQueryHandle_t`

### CreateQueryUGCDetailsRequest (静态)

```csharp
UGCQueryHandle_t CreateQueryUGCDetailsRequest(PublishedFileId_t[] pvecPublishedFileID, uint unNumPublishedFileIDs)
```

<para> Query for the details of the given published file ids (the RequestUGCDetails call is deprecated and replaced with this)</para>

**参数:**

- `pvecPublishedFileID` (`PublishedFileId_t[]`)
- `unNumPublishedFileIDs` (`uint`)

**返回值:** `UGCQueryHandle_t`

### SendQueryUGCRequest (静态)

```csharp
SteamAPICall_t SendQueryUGCRequest(UGCQueryHandle_t handle)
```

<para> Send the query to Steam</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)

**返回值:** `SteamAPICall_t`

### GetQueryUGCResult (静态)

```csharp
bool GetQueryUGCResult(UGCQueryHandle_t handle, uint index, out SteamUGCDetails_t pDetails)
```

<para> Retrieve an individual result after receiving the callback for querying UGC</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)
- `pDetails` (`out SteamUGCDetails_t`)

**返回值:** `bool`

### GetQueryUGCNumTags (静态)

```csharp
uint GetQueryUGCNumTags(UGCQueryHandle_t handle, uint index)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)

**返回值:** `uint`

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

### GetQueryUGCNumAdditionalPreviews (静态)

```csharp
uint GetQueryUGCNumAdditionalPreviews(UGCQueryHandle_t handle, uint index)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)

**返回值:** `uint`

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

### GetQueryUGCNumKeyValueTags (静态)

```csharp
uint GetQueryUGCNumKeyValueTags(UGCQueryHandle_t handle, uint index)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)

**返回值:** `uint`

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

### GetQueryUGCKeyValueTag (静态)

```csharp
bool GetQueryUGCKeyValueTag(UGCQueryHandle_t handle, uint index, string pchKey, out string pchValue, uint cchValueSize)
```

<para> Return the first value matching the pchKey. Note that a key may map to multiple values. Returns false if there was an error or no matching value was found.</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)
- `pchKey` (`string`)
- `pchValue` (`out string`)
- `cchValueSize` (`uint`)

**返回值:** `bool`

### GetNumSupportedGameVersions (静态)

```csharp
uint GetNumSupportedGameVersions(UGCQueryHandle_t handle, uint index)
```

<para> Some items can specify that they have a version that is valid for a range of game versions (Steam branch)</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `index` (`uint`)

**返回值:** `uint`

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

### ReleaseQueryUGCRequest (静态)

```csharp
bool ReleaseQueryUGCRequest(UGCQueryHandle_t handle)
```

<para> Release the request to free up memory, after retrieving results</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)

**返回值:** `bool`

### AddRequiredTag (静态)

```csharp
bool AddRequiredTag(UGCQueryHandle_t handle, string pTagName)
```

<para> Options to set for querying UGC</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `pTagName` (`string`)

**返回值:** `bool`

### AddRequiredTagGroup (静态)

```csharp
bool AddRequiredTagGroup(UGCQueryHandle_t handle, System.Collections.Generic.IList<string> pTagGroups)
```

<para> match any of the tags in this group</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `pTagGroups` (`System.Collections.Generic.IList\<string\>`)

**返回值:** `bool`

### AddExcludedTag (静态)

```csharp
bool AddExcludedTag(UGCQueryHandle_t handle, string pTagName)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `pTagName` (`string`)

**返回值:** `bool`

### SetReturnOnlyIDs (静态)

```csharp
bool SetReturnOnlyIDs(UGCQueryHandle_t handle, bool bReturnOnlyIDs)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `bReturnOnlyIDs` (`bool`)

**返回值:** `bool`

### SetReturnKeyValueTags (静态)

```csharp
bool SetReturnKeyValueTags(UGCQueryHandle_t handle, bool bReturnKeyValueTags)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `bReturnKeyValueTags` (`bool`)

**返回值:** `bool`

### SetReturnLongDescription (静态)

```csharp
bool SetReturnLongDescription(UGCQueryHandle_t handle, bool bReturnLongDescription)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `bReturnLongDescription` (`bool`)

**返回值:** `bool`

### SetReturnMetadata (静态)

```csharp
bool SetReturnMetadata(UGCQueryHandle_t handle, bool bReturnMetadata)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `bReturnMetadata` (`bool`)

**返回值:** `bool`

### SetReturnChildren (静态)

```csharp
bool SetReturnChildren(UGCQueryHandle_t handle, bool bReturnChildren)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `bReturnChildren` (`bool`)

**返回值:** `bool`

### SetReturnAdditionalPreviews (静态)

```csharp
bool SetReturnAdditionalPreviews(UGCQueryHandle_t handle, bool bReturnAdditionalPreviews)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `bReturnAdditionalPreviews` (`bool`)

**返回值:** `bool`

### SetReturnTotalOnly (静态)

```csharp
bool SetReturnTotalOnly(UGCQueryHandle_t handle, bool bReturnTotalOnly)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `bReturnTotalOnly` (`bool`)

**返回值:** `bool`

### SetReturnPlaytimeStats (静态)

```csharp
bool SetReturnPlaytimeStats(UGCQueryHandle_t handle, uint unDays)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `unDays` (`uint`)

**返回值:** `bool`

### SetLanguage (静态)

```csharp
bool SetLanguage(UGCQueryHandle_t handle, string pchLanguage)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `pchLanguage` (`string`)

**返回值:** `bool`

### SetAllowCachedResponse (静态)

```csharp
bool SetAllowCachedResponse(UGCQueryHandle_t handle, uint unMaxAgeSeconds)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `unMaxAgeSeconds` (`uint`)

**返回值:** `bool`

### SetAdminQuery (静态)

```csharp
bool SetAdminQuery(UGCUpdateHandle_t handle, bool bAdminQuery)
```

<para> admin queries return hidden items</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `bAdminQuery` (`bool`)

**返回值:** `bool`

### SetCloudFileNameFilter (静态)

```csharp
bool SetCloudFileNameFilter(UGCQueryHandle_t handle, string pMatchCloudFileName)
```

<para> Options only for querying user UGC</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `pMatchCloudFileName` (`string`)

**返回值:** `bool`

### SetMatchAnyTag (静态)

```csharp
bool SetMatchAnyTag(UGCQueryHandle_t handle, bool bMatchAnyTag)
```

<para> Options only for querying all UGC</para>

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `bMatchAnyTag` (`bool`)

**返回值:** `bool`

### SetSearchText (静态)

```csharp
bool SetSearchText(UGCQueryHandle_t handle, string pSearchText)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `pSearchText` (`string`)

**返回值:** `bool`

### SetRankedByTrendDays (静态)

```csharp
bool SetRankedByTrendDays(UGCQueryHandle_t handle, uint unDays)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `unDays` (`uint`)

**返回值:** `bool`

### SetTimeCreatedDateRange (静态)

```csharp
bool SetTimeCreatedDateRange(UGCQueryHandle_t handle, uint rtStart, uint rtEnd)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `rtStart` (`uint`)
- `rtEnd` (`uint`)

**返回值:** `bool`

### SetTimeUpdatedDateRange (静态)

```csharp
bool SetTimeUpdatedDateRange(UGCQueryHandle_t handle, uint rtStart, uint rtEnd)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `rtStart` (`uint`)
- `rtEnd` (`uint`)

**返回值:** `bool`

### AddRequiredKeyValueTag (静态)

```csharp
bool AddRequiredKeyValueTag(UGCQueryHandle_t handle, string pKey, string pValue)
```

**参数:**

- `handle` (`UGCQueryHandle_t`)
- `pKey` (`string`)
- `pValue` (`string`)

**返回值:** `bool`

### RequestUGCDetails (静态)

```csharp
SteamAPICall_t RequestUGCDetails(PublishedFileId_t nPublishedFileID, uint unMaxAgeSeconds)
```

<para> DEPRECATED - Use CreateQueryUGCDetailsRequest call above instead!</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)
- `unMaxAgeSeconds` (`uint`)

**返回值:** `SteamAPICall_t`

### CreateItem (静态)

```csharp
SteamAPICall_t CreateItem(AppId_t nConsumerAppId, EWorkshopFileType eFileType)
```

<para> Steam Workshop Creator API</para> <para> create new item for this app with no content attached yet</para>

**参数:**

- `nConsumerAppId` (`AppId_t`)
- `eFileType` (`EWorkshopFileType`)

**返回值:** `SteamAPICall_t`

### StartItemUpdate (静态)

```csharp
UGCUpdateHandle_t StartItemUpdate(AppId_t nConsumerAppId, PublishedFileId_t nPublishedFileID)
```

<para> start an UGC item update. Set changed properties before commiting update with CommitItemUpdate()</para>

**参数:**

- `nConsumerAppId` (`AppId_t`)
- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `UGCUpdateHandle_t`

### SetItemTitle (静态)

```csharp
bool SetItemTitle(UGCUpdateHandle_t handle, string pchTitle)
```

<para> change the title of an UGC item</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchTitle` (`string`)

**返回值:** `bool`

### SetItemDescription (静态)

```csharp
bool SetItemDescription(UGCUpdateHandle_t handle, string pchDescription)
```

<para> change the description of an UGC item</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchDescription` (`string`)

**返回值:** `bool`

### SetItemUpdateLanguage (静态)

```csharp
bool SetItemUpdateLanguage(UGCUpdateHandle_t handle, string pchLanguage)
```

<para> specify the language of the title or description that will be set</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchLanguage` (`string`)

**返回值:** `bool`

### SetItemMetadata (静态)

```csharp
bool SetItemMetadata(UGCUpdateHandle_t handle, string pchMetaData)
```

<para> change the metadata of an UGC item (max = k_cchDeveloperMetadataMax)</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchMetaData` (`string`)

**返回值:** `bool`

### SetItemVisibility (静态)

```csharp
bool SetItemVisibility(UGCUpdateHandle_t handle, ERemoteStoragePublishedFileVisibility eVisibility)
```

<para> change the visibility of an UGC item</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `eVisibility` (`ERemoteStoragePublishedFileVisibility`)

**返回值:** `bool`

### SetItemTags (静态)

```csharp
bool SetItemTags(UGCUpdateHandle_t updateHandle, System.Collections.Generic.IList<string> pTags, bool bAllowAdminTags = false)
```

<para> change the tags of an UGC item</para>

**参数:**

- `updateHandle` (`UGCUpdateHandle_t`)
- `pTags` (`System.Collections.Generic.IList\<string\>`)
- `bAllowAdminTags` (`bool`) = `false`

**返回值:** `bool`

### SetItemContent (静态)

```csharp
bool SetItemContent(UGCUpdateHandle_t handle, string pszContentFolder)
```

<para> update item content from this local folder</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pszContentFolder` (`string`)

**返回值:** `bool`

### SetItemPreview (静态)

```csharp
bool SetItemPreview(UGCUpdateHandle_t handle, string pszPreviewFile)
```

<para> change preview image file for this item. pszPreviewFile points to local image file, which must be under 1MB in size</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pszPreviewFile` (`string`)

**返回值:** `bool`

### SetAllowLegacyUpload (静态)

```csharp
bool SetAllowLegacyUpload(UGCUpdateHandle_t handle, bool bAllowLegacyUpload)
```

<para> use legacy upload for a single small file. The parameter to SetItemContent() should either be a directory with one file or the full path to the file. The file must also be less than 10MB in size.</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `bAllowLegacyUpload` (`bool`)

**返回值:** `bool`

### RemoveAllItemKeyValueTags (静态)

```csharp
bool RemoveAllItemKeyValueTags(UGCUpdateHandle_t handle)
```

<para> remove all existing key-value tags (you can add new ones via the AddItemKeyValueTag function)</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)

**返回值:** `bool`

### RemoveItemKeyValueTags (静态)

```csharp
bool RemoveItemKeyValueTags(UGCUpdateHandle_t handle, string pchKey)
```

<para> remove any existing key-value tags with the specified key</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchKey` (`string`)

**返回值:** `bool`

### AddItemKeyValueTag (静态)

```csharp
bool AddItemKeyValueTag(UGCUpdateHandle_t handle, string pchKey, string pchValue)
```

<para> add new key-value tags for the item. Note that there can be multiple values for a tag.</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchKey` (`string`)
- `pchValue` (`string`)

**返回值:** `bool`

### AddItemPreviewFile (静态)

```csharp
bool AddItemPreviewFile(UGCUpdateHandle_t handle, string pszPreviewFile, EItemPreviewType type)
```

<para> add preview file for this item. pszPreviewFile points to local file, which must be under 1MB in size</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pszPreviewFile` (`string`)
- `type` (`EItemPreviewType`)

**返回值:** `bool`

### AddItemPreviewVideo (静态)

```csharp
bool AddItemPreviewVideo(UGCUpdateHandle_t handle, string pszVideoID)
```

<para> add preview video for this item</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pszVideoID` (`string`)

**返回值:** `bool`

### UpdateItemPreviewFile (静态)

```csharp
bool UpdateItemPreviewFile(UGCUpdateHandle_t handle, uint index, string pszPreviewFile)
```

<para> updates an existing preview file for this item. pszPreviewFile points to local file, which must be under 1MB in size</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `index` (`uint`)
- `pszPreviewFile` (`string`)

**返回值:** `bool`

### UpdateItemPreviewVideo (静态)

```csharp
bool UpdateItemPreviewVideo(UGCUpdateHandle_t handle, uint index, string pszVideoID)
```

<para> updates an existing preview video for this item</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `index` (`uint`)
- `pszVideoID` (`string`)

**返回值:** `bool`

### RemoveItemPreview (静态)

```csharp
bool RemoveItemPreview(UGCUpdateHandle_t handle, uint index)
```

<para> remove a preview by index starting at 0 (previews are sorted)</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `index` (`uint`)

**返回值:** `bool`

### AddContentDescriptor (静态)

```csharp
bool AddContentDescriptor(UGCUpdateHandle_t handle, EUGCContentDescriptorID descid)
```

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `descid` (`EUGCContentDescriptorID`)

**返回值:** `bool`

### RemoveContentDescriptor (静态)

```csharp
bool RemoveContentDescriptor(UGCUpdateHandle_t handle, EUGCContentDescriptorID descid)
```

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `descid` (`EUGCContentDescriptorID`)

**返回值:** `bool`

### SetRequiredGameVersions (静态)

```csharp
bool SetRequiredGameVersions(UGCUpdateHandle_t handle, string pszGameBranchMin, string pszGameBranchMax)
```

<para> an empty string for either parameter means that it will match any version on that end of the range. This will only be applied if the actual content has been changed.</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pszGameBranchMin` (`string`)
- `pszGameBranchMax` (`string`)

**返回值:** `bool`

### SubmitItemUpdate (静态)

```csharp
SteamAPICall_t SubmitItemUpdate(UGCUpdateHandle_t handle, string pchChangeNote)
```

<para> commit update process started with StartItemUpdate()</para>

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `pchChangeNote` (`string`)

**返回值:** `SteamAPICall_t`

### GetItemUpdateProgress (静态)

```csharp
EItemUpdateStatus GetItemUpdateProgress(UGCUpdateHandle_t handle, out ulong punBytesProcessed, out ulong punBytesTotal)
```

**参数:**

- `handle` (`UGCUpdateHandle_t`)
- `punBytesProcessed` (`out ulong`)
- `punBytesTotal` (`out ulong`)

**返回值:** `EItemUpdateStatus`

### SetUserItemVote (静态)

```csharp
SteamAPICall_t SetUserItemVote(PublishedFileId_t nPublishedFileID, bool bVoteUp)
```

<para> Steam Workshop Consumer API</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)
- `bVoteUp` (`bool`)

**返回值:** `SteamAPICall_t`

### GetUserItemVote (静态)

```csharp
SteamAPICall_t GetUserItemVote(PublishedFileId_t nPublishedFileID)
```

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

### AddItemToFavorites (静态)

```csharp
SteamAPICall_t AddItemToFavorites(AppId_t nAppId, PublishedFileId_t nPublishedFileID)
```

**参数:**

- `nAppId` (`AppId_t`)
- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

### RemoveItemFromFavorites (静态)

```csharp
SteamAPICall_t RemoveItemFromFavorites(AppId_t nAppId, PublishedFileId_t nPublishedFileID)
```

**参数:**

- `nAppId` (`AppId_t`)
- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

### SubscribeItem (静态)

```csharp
SteamAPICall_t SubscribeItem(PublishedFileId_t nPublishedFileID)
```

<para> subscribe to this item, will be installed ASAP</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

### UnsubscribeItem (静态)

```csharp
SteamAPICall_t UnsubscribeItem(PublishedFileId_t nPublishedFileID)
```

<para> unsubscribe from this item, will be uninstalled after game quits</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

### GetNumSubscribedItems (静态)

```csharp
uint GetNumSubscribedItems(bool bIncludeLocallyDisabled = false)
```

<para> number of subscribed items</para>

**参数:**

- `bIncludeLocallyDisabled` (`bool`) = `false`

**返回值:** `uint`

### GetSubscribedItems (静态)

```csharp
uint GetSubscribedItems(PublishedFileId_t[] pvecPublishedFileID, uint cMaxEntries, bool bIncludeLocallyDisabled = false)
```

<para> all subscribed item PublishFileIDs</para>

**参数:**

- `pvecPublishedFileID` (`PublishedFileId_t[]`)
- `cMaxEntries` (`uint`)
- `bIncludeLocallyDisabled` (`bool`) = `false`

**返回值:** `uint`

### GetItemState (静态)

```csharp
uint GetItemState(PublishedFileId_t nPublishedFileID)
```

<para> get EItemState flags about item on this client</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `uint`

### GetItemInstallInfo (静态)

```csharp
bool GetItemInstallInfo(PublishedFileId_t nPublishedFileID, out ulong punSizeOnDisk, out string pchFolder, uint cchFolderSize, out uint punTimeStamp)
```

<para> get info about currently installed content on disc for items that have k_EItemStateInstalled set</para> <para> if k_EItemStateLegacyItem is set, pchFolder contains the path to the legacy file itself (not a folder)</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)
- `punSizeOnDisk` (`out ulong`)
- `pchFolder` (`out string`)
- `cchFolderSize` (`uint`)
- `punTimeStamp` (`out uint`)

**返回值:** `bool`

### GetItemDownloadInfo (静态)

```csharp
bool GetItemDownloadInfo(PublishedFileId_t nPublishedFileID, out ulong punBytesDownloaded, out ulong punBytesTotal)
```

<para> get info about pending update for items that have k_EItemStateNeedsUpdate set. punBytesTotal will be valid after download started once</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)
- `punBytesDownloaded` (`out ulong`)
- `punBytesTotal` (`out ulong`)

**返回值:** `bool`

### DownloadItem (静态)

```csharp
bool DownloadItem(PublishedFileId_t nPublishedFileID, bool bHighPriority)
```

<para> download new or update already installed item. If function returns true, wait for DownloadItemResult_t. If the item is already installed,</para> <para> then files on disk should not be used until callback received. If item is not subscribed to, it will be cached for some time.</para> <para> If bHighPriority is set, any other item download will be suspended and this item downloaded ASAP.</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)
- `bHighPriority` (`bool`)

**返回值:** `bool`

### BInitWorkshopForGameServer (静态)

```csharp
bool BInitWorkshopForGameServer(DepotId_t unWorkshopDepotID, string pszFolder)
```

<para> game servers can set a specific workshop folder before issuing any UGC commands.</para> <para> This is helpful if you want to support multiple game servers running out of the same install folder</para>

**参数:**

- `unWorkshopDepotID` (`DepotId_t`)
- `pszFolder` (`string`)

**返回值:** `bool`

### SuspendDownloads (静态)

```csharp
void SuspendDownloads(bool bSuspend)
```

<para> SuspendDownloads( true ) will suspend all workshop downloads until SuspendDownloads( false ) is called or the game ends</para>

**参数:**

- `bSuspend` (`bool`)

### StartPlaytimeTracking (静态)

```csharp
SteamAPICall_t StartPlaytimeTracking(PublishedFileId_t[] pvecPublishedFileID, uint unNumPublishedFileIDs)
```

<para> usage tracking</para>

**参数:**

- `pvecPublishedFileID` (`PublishedFileId_t[]`)
- `unNumPublishedFileIDs` (`uint`)

**返回值:** `SteamAPICall_t`

### StopPlaytimeTracking (静态)

```csharp
SteamAPICall_t StopPlaytimeTracking(PublishedFileId_t[] pvecPublishedFileID, uint unNumPublishedFileIDs)
```

**参数:**

- `pvecPublishedFileID` (`PublishedFileId_t[]`)
- `unNumPublishedFileIDs` (`uint`)

**返回值:** `SteamAPICall_t`

### StopPlaytimeTrackingForAllItems (静态)

```csharp
SteamAPICall_t StopPlaytimeTrackingForAllItems()
```

**返回值:** `SteamAPICall_t`

### AddDependency (静态)

```csharp
SteamAPICall_t AddDependency(PublishedFileId_t nParentPublishedFileID, PublishedFileId_t nChildPublishedFileID)
```

<para> parent-child relationship or dependency management</para>

**参数:**

- `nParentPublishedFileID` (`PublishedFileId_t`)
- `nChildPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

### RemoveDependency (静态)

```csharp
SteamAPICall_t RemoveDependency(PublishedFileId_t nParentPublishedFileID, PublishedFileId_t nChildPublishedFileID)
```

**参数:**

- `nParentPublishedFileID` (`PublishedFileId_t`)
- `nChildPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

### AddAppDependency (静态)

```csharp
SteamAPICall_t AddAppDependency(PublishedFileId_t nPublishedFileID, AppId_t nAppID)
```

<para> add/remove app dependence/requirements (usually DLC)</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)
- `nAppID` (`AppId_t`)

**返回值:** `SteamAPICall_t`

### RemoveAppDependency (静态)

```csharp
SteamAPICall_t RemoveAppDependency(PublishedFileId_t nPublishedFileID, AppId_t nAppID)
```

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)
- `nAppID` (`AppId_t`)

**返回值:** `SteamAPICall_t`

### GetAppDependencies (静态)

```csharp
SteamAPICall_t GetAppDependencies(PublishedFileId_t nPublishedFileID)
```

<para> request app dependencies. note that whatever callback you register for GetAppDependenciesResult_t may be called multiple times</para> <para> until all app dependencies have been returned</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

### DeleteItem (静态)

```csharp
SteamAPICall_t DeleteItem(PublishedFileId_t nPublishedFileID)
```

<para> delete the item without prompting the user</para>

**参数:**

- `nPublishedFileID` (`PublishedFileId_t`)

**返回值:** `SteamAPICall_t`

### ShowWorkshopEULA (静态)

```csharp
bool ShowWorkshopEULA()
```

<para> Show the app's latest Workshop EULA to the user in an overlay window, where they can accept it or not</para>

**返回值:** `bool`

### GetWorkshopEULAStatus (静态)

```csharp
SteamAPICall_t GetWorkshopEULAStatus()
```

<para> Retrieve information related to the user's acceptance or not of the app's specific Workshop EULA</para>

**返回值:** `SteamAPICall_t`

### GetUserContentDescriptorPreferences (静态)

```csharp
uint GetUserContentDescriptorPreferences(out EUGCContentDescriptorID pvecDescriptors, uint cMaxEntries)
```

<para> Return the user's community content descriptor preferences</para>

**参数:**

- `pvecDescriptors` (`out EUGCContentDescriptorID`)
- `cMaxEntries` (`uint`)

**返回值:** `uint`

### SetItemsDisabledLocally (静态)

```csharp
bool SetItemsDisabledLocally(out PublishedFileId_t pvecPublishedFileIDs, uint unNumPublishedFileIDs, bool bDisabledLocally)
```

<para> Sets whether the item should be disabled locally or not. This means that it will not be returned in GetSubscribedItems() by default.</para>

**参数:**

- `pvecPublishedFileIDs` (`out PublishedFileId_t`)
- `unNumPublishedFileIDs` (`uint`)
- `bDisabledLocally` (`bool`)

**返回值:** `bool`

### SetSubscriptionsLoadOrder (静态)

```csharp
bool SetSubscriptionsLoadOrder(out PublishedFileId_t pvecPublishedFileIDs, uint unNumPublishedFileIDs)
```

<para> Set the local load order for these items. If there are any items not in the given list, they will sort by the time subscribed.</para>

**参数:**

- `pvecPublishedFileIDs` (`out PublishedFileId_t`)
- `unNumPublishedFileIDs` (`uint`)

**返回值:** `bool`

