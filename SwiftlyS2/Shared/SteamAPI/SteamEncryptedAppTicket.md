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
byte[] encrypted = new byte[256]; uint encLen = 256; byte[] decrypted = new byte[256]; uint decLen = 0; byte[] key = new byte[32]; bool result = SteamEncryptedAppTicket.BDecryptTicket(encrypted, encLen, decrypted, ref decLen, key, 32);
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
byte[] ticket = GetDecryptedTicket(); bool isValid = SteamEncryptedAppTicket.BIsTicketForApp(ticket, (uint)ticket.Length, AppId_t.GameServer);
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
byte[] decryptedTicket = new byte[256]; uint issueTime = SteamEncryptedAppTicket.GetTicketIssueTime(decryptedTicket, (uint)decryptedTicket.Length);
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
byte[] ticket = new byte[1024]; CSteamID steamID; SteamEncryptedAppTicket.GetTicketSteamID(ticket, (uint)ticket.Length, out steamID);
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
byte[] ticket = new byte[256]; uint appId = SteamEncryptedAppTicket.GetTicketAppID(ticket, (uint)ticket.Length);
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
bool ownsApp = SteamEncryptedAppTicket.BUserOwnsAppInTicket(ticketData, (uint)ticketData.Length, 730);
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
byte[] ticket = System.Array.Empty<byte>();
bool isBanned = SteamEncryptedAppTicket.BUserIsVacBanned(ticket, 0);
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
byte[] ticket = new byte[256]; uint userDataLen; var userData = SteamEncryptedAppTicket.GetUserVariableData(ticket, (uint)ticket.Length, out userDataLen);
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
byte[] ticket = null; byte[] key = null; bool isValid = SteamEncryptedAppTicket.BIsTicketSigned(ticket, 0, key, 0);
```

