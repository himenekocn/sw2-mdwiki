# 📦 SteamEncryptedAppTicket

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### BDecryptTicket (静态)

```csharp
bool BDecryptTicket(byte[] rgubTicketEncrypted, uint cubTicketEncrypted, byte[] rgubTicketDecrypted, ref uint pcubTicketDecrypted, byte[] rgubKey, int cubKey)
```

**参数:**

- `rgubTicketEncrypted` (`byte[]`)
- `cubTicketEncrypted` (`uint`)
- `rgubTicketDecrypted` (`byte[]`)
- `pcubTicketDecrypted` (`ref uint`)
- `rgubKey` (`byte[]`)
- `cubKey` (`int`)

**返回值:** `bool`

### BIsTicketForApp (静态)

```csharp
bool BIsTicketForApp(byte[] rgubTicketDecrypted, uint cubTicketDecrypted, AppId_t nAppID)
```

**参数:**

- `rgubTicketDecrypted` (`byte[]`)
- `cubTicketDecrypted` (`uint`)
- `nAppID` (`AppId_t`)

**返回值:** `bool`

### GetTicketIssueTime (静态)

```csharp
uint GetTicketIssueTime(byte[] rgubTicketDecrypted, uint cubTicketDecrypted)
```

**参数:**

- `rgubTicketDecrypted` (`byte[]`)
- `cubTicketDecrypted` (`uint`)

**返回值:** `uint`

### GetTicketSteamID (静态)

```csharp
void GetTicketSteamID(byte[] rgubTicketDecrypted, uint cubTicketDecrypted, out CSteamID psteamID)
```

**参数:**

- `rgubTicketDecrypted` (`byte[]`)
- `cubTicketDecrypted` (`uint`)
- `psteamID` (`out CSteamID`)

### GetTicketAppID (静态)

```csharp
uint GetTicketAppID(byte[] rgubTicketDecrypted, uint cubTicketDecrypted)
```

**参数:**

- `rgubTicketDecrypted` (`byte[]`)
- `cubTicketDecrypted` (`uint`)

**返回值:** `uint`

### BUserOwnsAppInTicket (静态)

```csharp
bool BUserOwnsAppInTicket(byte[] rgubTicketDecrypted, uint cubTicketDecrypted, AppId_t nAppID)
```

**参数:**

- `rgubTicketDecrypted` (`byte[]`)
- `cubTicketDecrypted` (`uint`)
- `nAppID` (`AppId_t`)

**返回值:** `bool`

### BUserIsVacBanned (静态)

```csharp
bool BUserIsVacBanned(byte[] rgubTicketDecrypted, uint cubTicketDecrypted)
```

**参数:**

- `rgubTicketDecrypted` (`byte[]`)
- `cubTicketDecrypted` (`uint`)

**返回值:** `bool`

### GetUserVariableData (静态)

```csharp
byte[] GetUserVariableData(byte[] rgubTicketDecrypted, uint cubTicketDecrypted, out uint pcubUserData)
```

**参数:**

- `rgubTicketDecrypted` (`byte[]`)
- `cubTicketDecrypted` (`uint`)
- `pcubUserData` (`out uint`)

**返回值:** `byte[]`

### BIsTicketSigned (静态)

```csharp
bool BIsTicketSigned(byte[] rgubTicketDecrypted, uint cubTicketDecrypted, byte[] pubRSAKey, uint cubRSAKey)
```

**参数:**

- `rgubTicketDecrypted` (`byte[]`)
- `cubTicketDecrypted` (`uint`)
- `pubRSAKey` (`byte[]`)
- `cubRSAKey` (`uint`)

**返回值:** `bool`

