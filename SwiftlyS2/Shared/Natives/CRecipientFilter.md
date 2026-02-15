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

### FromPlayers (静态)

```csharp
CRecipientFilter FromPlayers(params int[] players)
```

**参数:**

- `players` (`params int[]`)

**返回值:** `CRecipientFilter`

### FromSingle (静态)

```csharp
CRecipientFilter FromSingle(int player)
```

**参数:**

- `player` (`int`)

**返回值:** `CRecipientFilter`

### ToMask

```csharp
ulong ToMask()
```

**返回值:** `ulong`

### AddAllPlayers

```csharp
void AddAllPlayers()
```

### RemoveAllPlayers

```csharp
void RemoveAllPlayers()
```

### AddRecipient

```csharp
void AddRecipient(int playerid)
```

**参数:**

- `playerid` (`int`)

### RemoveRecipient

```csharp
void RemoveRecipient(int playerid)
```

**参数:**

- `playerid` (`int`)

### GetRecipientCount

```csharp
int GetRecipientCount()
```

**返回值:** `int`

### GetRecipients

```csharp
IEnumerable<int> GetRecipients()
```

**返回值:** `IEnumerable\<int\>`

