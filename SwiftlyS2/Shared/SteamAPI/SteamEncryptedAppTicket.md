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
byte[] encrypted = new byte[1024]; uint decryptedSize = 1024; byte[] key = new byte[32];
bool result = SteamEncryptedAppTicket.BDecryptTicket(encrypted, (uint)encrypted.Length, new byte[1024], ref decryptedSize, key, key.Length);
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
bool result = SteamEncryptedAppTicket.BIsTicketForApp(ticketData, (uint)ticketData.Length, new AppId_t(440));
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
uint issueTime = SteamEncryptedAppTicket.GetTicketIssueTime(ticketData, (uint)ticketData.Length);
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
byte[] ticket = new byte[1024]; uint ticketSize = (uint)ticket.Length; CSteamID steamId;
SteamEncryptedAppTicket.GetTicketSteamID(ticket, ticketSize, out steamId);
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
uint appID = SteamEncryptedAppTicket.GetTicketAppID(ticketBytes, (uint)ticketBytes.Length);
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
bool owns = SteamEncryptedAppTicket.BUserOwnsAppInTicket(ticketData, (uint)ticketData.Length, new AppId_t(440));
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
bool isBanned = SteamEncryptedAppTicket.BUserIsVacBanned(ticketData, (uint)ticketData.Length);
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
byte[] userData = SteamEncryptedAppTicket.GetUserVariableData(ticketDecrypted, (uint)ticketDecrypted.Length, out uint userDataSize);
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
bool isSigned = SteamEncryptedAppTicket.BIsTicketSigned(ticketData, (uint)ticketData.Length, rsaKey, (uint)rsaKey.Length);
```

