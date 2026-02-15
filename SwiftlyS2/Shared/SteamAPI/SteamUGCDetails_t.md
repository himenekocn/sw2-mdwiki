# 🏗️ SteamUGCDetails_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_nPublishedFileId` | `PublishedFileId_t` | - | - |
| `m_eResult` | `EResult` | - | - |
| `m_eFileType` | `EWorkshopFileType` | - | - |
| `m_nCreatorAppID` | `AppId_t` | - | - |
| `m_nConsumerAppID` | `AppId_t` | - | - |
| `m_ulSteamIDOwner` | `ulong` | - | - |
| `m_rtimeCreated` | `uint` | - | - |
| `m_rtimeUpdated` | `uint` | - | - |
| `m_eVisibility` | `ERemoteStoragePublishedFileVisibility` | - | - |
| `m_bBanned` | `bool` | - | - |
| `m_bAcceptedForUse` | `bool` | - | - |
| `m_bTagsTruncated` | `bool` | - | - |
| `m_hFile` | `UGCHandle_t` | - | - |
| `m_hPreviewFile` | `UGCHandle_t` | - | - |
| `m_nPreviewFileSize` | `int` | - | - |
| `m_unVotesUp` | `uint` | - | - |
| `m_unVotesDown` | `uint` | - | - |
| `m_flScore` | `float` | - | - |
| `m_unNumChildren` | `uint` | - | - |

## ⚙️ 方法

### list

```csharp
their list(not always applicable)
```

**参数:**

- `applicable` (`not always`)

**返回值:** `their`

**用法示例:**
```csharp
SteamUGCDetails_t.list();
```

### file

```csharp
primary file(for legacy items which only support one file)
```

**参数:**

- `file` (`for legacy items which only support one`)

**返回值:** `primary`

**用法示例:**
```csharp
SteamUGCDetails_t.primary_file()
```

### files

```csharp
all files(non-legacy )
```

**参数:**

- `` (`non-legacy`)

**返回值:** `all`

**用法示例:**
```csharp
SteamUGCDetails_t.files();
```

