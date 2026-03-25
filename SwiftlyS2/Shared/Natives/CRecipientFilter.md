# 🏗️ CRecipientFilter

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `RecipientsMask` | `ulong` | - | - |
| `PredictedSlot` | `int` | - | - |
| `BufferType` | `NetChannelBufType_t` | - | - |
| `InitMessage` | `bool` | - | - |
| `DisabledPrediction` | `bool` | - | - |

## ⚙️ 方法

### FromMask (静态)

```csharp
CRecipientFilter FromMask(ulong playerMask)
```

**参数:**

- `playerMask` (`ulong`)

**返回值:** `CRecipientFilter`

**用法示例:**
```csharp
var filter = CRecipientFilter.FromMask(0x1);
```

### FromPlayers (静态)

```csharp
CRecipientFilter FromPlayers(params int[] players)
```

**参数:**

- `players` (`params int[]`)

**返回值:** `CRecipientFilter`

**用法示例:**
```csharp
var filter = CRecipientFilter.FromPlayers(1, 2, 3);
```

### FromSingle (静态)

```csharp
CRecipientFilter FromSingle(int player)
```

**参数:**

- `player` (`int`)

**返回值:** `CRecipientFilter`

**用法示例:**
```csharp
CRecipientFilter filter = CRecipientFilter.FromSingle(1);
```

### ToMask

```csharp
ulong ToMask()
```

**返回值:** `ulong`

**用法示例:**
```csharp
ulong mask = filter.ToMask();
```

### AddAllPlayers

```csharp
void AddAllPlayers()
```

**用法示例:**
```csharp
CRecipientFilter filter;
filter.AddAllPlayers();
```

### RemoveAllPlayers

```csharp
void RemoveAllPlayers()
```

**用法示例:**
```csharp
CRecipientFilter filter; filter.RemoveAllPlayers();
```

### AddRecipient

```csharp
void AddRecipient(int playerid)
```

**参数:**

- `playerid` (`int`)

**用法示例:**
```csharp
filter.AddRecipient(1);
```

### RemoveRecipient

```csharp
void RemoveRecipient(int playerid)
```

**参数:**

- `playerid` (`int`)

**用法示例:**
```csharp
filter.RemoveRecipient(playerid);
```

### GetRecipientCount

```csharp
int GetRecipientCount()
```

**返回值:** `int`

**用法示例:**
```csharp
int count = recipientFilter.GetRecipientCount();
```

### GetRecipients

```csharp
IEnumerable<int> GetRecipients()
```

**返回值:** `IEnumerable\<int\>`

**用法示例:**
```csharp
var recipients = existingFilter.GetRecipients();
```

