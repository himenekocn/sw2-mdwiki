<a id="steamencryptedappticket"></a>

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

**用法示例:**
```csharp
var decrypted = new byte[1024]; uint size = 1024; bool success = SteamEncryptedAppTicket.BDecryptTicket(encryptedTicket, (uint)encryptedTicket.Length, decrypted, ref size, key, key.Length);
```

### BIsTicketForApp (静态)

```csharp
bool BIsTicketForApp(byte[] rgubTicketDecrypted, uint cubTicketDecrypted, AppId_t nAppID)
```

**参数:**

- `rgubTicketDecrypted` (`byte[]`)
- `cubTicketDecrypted` (`uint`)
- `nAppID` (`AppId_t`)

**返回值:** `bool`

**用法示例:**
```csharp
bool isValid = SteamEncryptedAppTicket.BIsTicketForApp(ticketData, (uint)ticketData.Length, new AppId_t(480));
```

### GetTicketIssueTime (静态)

```csharp
uint GetTicketIssueTime(byte[] rgubTicketDecrypted, uint cubTicketDecrypted)
```

**参数:**

- `rgubTicketDecrypted` (`byte[]`)
- `cubTicketDecrypted` (`uint`)

**返回值:** `uint`

**用法示例:**
```csharp
uint issueTime = SteamEncryptedAppTicket.GetTicketIssueTime(decryptedTicket, decryptedTicket.Length);
```

### GetTicketSteamID (静态)

```csharp
void GetTicketSteamID(byte[] rgubTicketDecrypted, uint cubTicketDecrypted, out CSteamID psteamID)
```

**参数:**

- `rgubTicketDecrypted` (`byte[]`)
- `cubTicketDecrypted` (`uint`)
- `psteamID` (`out CSteamID`)

**用法示例:**
```csharp
SteamEncryptedAppTicket.GetTicketSteamID(decryptedTicket, (uint)decryptedTicket.Length, out CSteamID steamID);
```

### GetTicketAppID (静态)

```csharp
uint GetTicketAppID(byte[] rgubTicketDecrypted, uint cubTicketDecrypted)
```

**参数:**

- `rgubTicketDecrypted` (`byte[]`)
- `cubTicketDecrypted` (`uint`)

**返回值:** `uint`

**用法示例:**
```csharp
uint appId = SteamEncryptedAppTicket.GetTicketAppID(decryptedTicket, decryptedTicket.Length);
```

### BUserOwnsAppInTicket (静态)

```csharp
bool BUserOwnsAppInTicket(byte[] rgubTicketDecrypted, uint cubTicketDecrypted, AppId_t nAppID)
```

**参数:**

- `rgubTicketDecrypted` (`byte[]`)
- `cubTicketDecrypted` (`uint`)
- `nAppID` (`AppId_t`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ownsApp = SteamEncryptedAppTicket.BUserOwnsAppInTicket(ticketData, (uint)ticketData.Length, new AppId_t(480));
```

### BUserIsVacBanned (静态)

```csharp
bool BUserIsVacBanned(byte[] rgubTicketDecrypted, uint cubTicketDecrypted)
```

**参数:**

- `rgubTicketDecrypted` (`byte[]`)
- `cubTicketDecrypted` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
bool isVacBanned = SteamEncryptedAppTicket.BUserIsVacBanned(ticketData, (uint)ticketData.Length);
```

### GetUserVariableData (静态)

```csharp
byte[] GetUserVariableData(byte[] rgubTicketDecrypted, uint cubTicketDecrypted, out uint pcubUserData)
```

**参数:**

- `rgubTicketDecrypted` (`byte[]`)
- `cubTicketDecrypted` (`uint`)
- `pcubUserData` (`out uint`)

**返回值:** `byte[]`

**用法示例:**
```csharp
byte[] ticketData = GetDecryptedTicket();
uint userDataLength;
byte[] userVariableData = SteamEncryptedAppTicket.GetUserVariableData(ticketData, (uint)ticketData.Length, out userDataLength);
```

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

**用法示例:**
```csharp
bool isValid = SteamEncryptedAppTicket.BIsTicketSigned(ticketData, (uint)ticketData.Length, rsaKey, (uint)rsaKey.Length);
```

